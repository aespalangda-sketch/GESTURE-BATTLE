[index.html](https://github.com/user-attachments/files/32785425/index.html)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gesture Battle: Edu Cerdas V2</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Nunito:wght@400;700;900&display=swap" rel="stylesheet">
    
    <!-- MediaPipe Libraries for Computer Vision Hand Tracking -->
    <script src="https://cdn.jsdelivr.net/npm/@mediapipe/camera_utils/camera_utils.js" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/@mediapipe/control_utils/control_utils.js" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/@mediapipe/drawing_utils/drawing_utils.js" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/@mediapipe/hands/hands.js" crossorigin="anonymous"></script>
    
    <!-- Tone.js for Interactive Sound Synthesizers -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.49/Tone.js" crossorigin="anonymous"></script>
    
    <style>
        body {
            font-family: 'Nunito', sans-serif;
            background: #0f172a;
            overflow: hidden;
            touch-action: none;
            margin: 0;
            padding: 0;
            color: white;
            user-select: none;
        }
        h1, h2, h3, .game-font {
            font-family: 'Fredoka One', cursive;
        }
        #gameCanvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            z-index: 0;
        }
        .ui-layer {
            position: absolute;
            inset: 0;
            pointer-events: none;
            z-index: 10;
        }
        .interactive-layer {
            pointer-events: auto;
        }
        
        .form-select, .form-input {
            width: 100%;
            padding: 0.75rem 1rem;
            border-radius: 0.75rem;
            border: 2px solid #6366f1;
            background-color: #1e1b4b;
            color: white;
            font-weight: 700;
            outline: none;
            transition: all 0.2s ease;
        }
        .form-select:focus, .form-input:focus {
            border-color: #818cf8;
            box-shadow: 0 0 0 4px rgba(99, 102, 241, 0.35);
        }

        .loader {
            border: 5px solid #374151;
            border-top: 5px solid #6366f1;
            border-radius: 50%;
            width: 44px;
            height: 44px;
            animation: spin 0.9s linear infinite;
        }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        
        .score-box {
            backdrop-filter: blur(12px);
            background: rgba(15, 23, 42, 0.65);
            border: 3px solid;
        }

        /* Floating buttons */
        .float-btn {
            position: absolute;
            z-index: 50;
            background: rgba(15, 23, 42, 0.8);
            border: 2px solid #6366f1;
            border-radius: 50%;
            width: 45px;
            height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            pointer-events: auto;
            transition: all 0.2s ease;
            backdrop-filter: blur(5px);
        }
        .float-btn:hover { background: #6366f1; transform: scale(1.1); }
        .float-btn svg { width: 20px; height: 20px; fill: white; }

        /* Speed slider (gaya volume control) */
        .speed-slider {
            -webkit-appearance: none;
            appearance: none;
            width: 100%;
            height: 8px;
            border-radius: 999px;
            background: linear-gradient(to right, #312e81, #6366f1, #a5b4fc);
            outline: none;
            cursor: pointer;
        }
        .speed-slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 26px;
            height: 26px;
            border-radius: 50%;
            background: #f8fafc;
            border: 4px solid #6366f1;
            box-shadow: 0 0 12px rgba(99, 102, 241, 0.8), 0 2px 4px rgba(0,0,0,0.35);
            cursor: pointer;
            transition: transform 0.15s ease;
        }
        .speed-slider::-webkit-slider-thumb:hover { transform: scale(1.15); }
        .speed-slider::-moz-range-track {
            background: transparent;
        }
        .speed-slider::-moz-range-thumb {
            width: 26px;
            height: 26px;
            border-radius: 50%;
            background: #f8fafc;
            border: 4px solid #6366f1;
            box-shadow: 0 0 12px rgba(99, 102, 241, 0.8), 0 2px 4px rgba(0,0,0,0.35);
            cursor: pointer;
            transition: transform 0.15s ease;
        }
        .speed-slider::-moz-range-thumb:hover { transform: scale(1.15); }
    </style>
</head>
<body>

    <!-- ============ HALAMAN GERBANG PASSWORD (PALING DEPAN) ============ -->
    <div id="passwordScreen" class="fixed inset-0 z-[100] bg-slate-950 flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-slate-900 border border-slate-800 rounded-3xl shadow-[0_0_60px_rgba(99,102,241,0.35)] w-full max-w-md p-6 md:p-8 text-center">
            <h1 class="text-3xl md:text-4xl text-indigo-400 game-font mb-1 tracking-wide">Gesture Battle Edu</h1>
            <p class="text-slate-400 font-bold text-xs mb-6">Masukkan kata sandi untuk melanjutkan</p>

            <div class="mb-3">
                <input type="password" id="inpGatePassword" class="form-input text-center text-lg tracking-widest" placeholder="Kata Sandi" autocomplete="off">
            </div>
            <div id="gatePasswordError" class="hidden bg-red-900/80 border-2 border-red-500 text-red-200 px-3 py-2 rounded-xl mb-3 text-xs font-bold">
                Kata sandi salah. Silakan coba lagi.
            </div>
            <button id="btnUnlockGate" class="w-full bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-500 hover:to-purple-500 text-white text-lg font-bold py-3 rounded-2xl shadow-xl transition mb-6 game-font">
                Masuk
            </button>

            <div class="border-t border-slate-800 pt-5">
                <p class="text-slate-300 text-xs font-bold mb-3">Hubungi Admin / Pembuat</p>
                <div class="flex items-center justify-center gap-4 mb-4">
                    <a href="https://wa.me/6285397772345" target="_blank" rel="noopener" title="Hubungi via WhatsApp" class="flex flex-col items-center gap-1 text-slate-200 hover:opacity-80 transition">
                        <span class="w-12 h-12 rounded-full bg-white border-2 border-slate-300 flex items-center justify-center shadow-md">
                            <svg viewBox="0 0 32 32" class="w-7 h-7" fill="#000000"><path d="M16.004 3C9.377 3 4 8.373 4 15c0 2.386.692 4.611 1.885 6.49L4 29l7.71-1.845A11.94 11.94 0 0 0 16.004 27C22.63 27 28 21.627 28 15S22.63 3 16.004 3zm0 2c5.523 0 10 4.477 10 10s-4.477 10-10 10a9.96 9.96 0 0 1-5.09-1.395l-.365-.217-4.246 1.016 1.037-4.14-.238-.38A9.96 9.96 0 0 1 6.004 15c0-5.523 4.477-10 10-10zm-4.29 5.06c-.207 0-.542.078-.826.39-.284.312-1.084 1.059-1.084 2.582 0 1.523 1.11 2.996 1.264 3.203.155.207 2.148 3.437 5.312 4.68 2.626 1.031 3.162.824 3.734.773.572-.05 1.845-.754 2.105-1.484.26-.73.26-1.355.182-1.484-.078-.13-.284-.207-.594-.363-.31-.156-1.845-.91-2.13-1.014-.284-.104-.492-.156-.698.156-.207.312-.802 1.014-.983 1.222-.181.207-.362.234-.672.078-.31-.156-1.31-.484-2.494-1.545-.922-.822-1.545-1.836-1.727-2.148-.181-.312-.02-.48.137-.636.14-.14.31-.363.465-.545.155-.181.207-.312.31-.52.104-.208.052-.39-.026-.546-.078-.156-.68-1.68-.964-2.3-.26-.573-.526-.573-.72-.582z"/></svg>
                        </span>
                        <span class="text-[10px] font-bold">WhatsApp</span>
                    </a>
                    <a href="https://instagram.com/aes_435" target="_blank" rel="noopener" title="Instagram @aes_435" class="flex flex-col items-center gap-1 text-slate-200 hover:opacity-80 transition">
                        <span class="w-12 h-12 rounded-full bg-white border-2 border-slate-300 flex items-center justify-center shadow-md">
                            <svg viewBox="0 0 24 24" class="w-6 h-6" fill="#000000"><path d="M7 2C4.243 2 2 4.243 2 7v10c0 2.757 2.243 5 5 5h10c2.757 0 5-2.243 5-5V7c0-2.757-2.243-5-5-5H7zm0 2h10c1.654 0 3 1.346 3 3v10c0 1.654-1.346 3-3 3H7c-1.654 0-3-1.346-3-3V7c0-1.654 1.346-3 3-3zm11 1.5a1 1 0 1 0 0 2 1 1 0 0 0 0-2zM12 7a5 5 0 1 0 0 10 5 5 0 0 0 0-10zm0 2a3 3 0 1 1 0 6 3 3 0 0 1 0-6z"/></svg>
                        </span>
                        <span class="text-[10px] font-bold">@aes_435</span>
                    </a>
                    <a href="https://www.tiktok.com/@aes_435" target="_blank" rel="noopener" title="TikTok @aes_435" class="flex flex-col items-center gap-1 text-slate-200 hover:opacity-80 transition">
                        <span class="w-12 h-12 rounded-full bg-white border-2 border-slate-300 flex items-center justify-center shadow-md">
                            <svg viewBox="0 0 24 24" class="w-6 h-6" fill="#000000"><path d="M14 2h2.5c.27 1.62 1.24 3.03 2.6 3.9.9.58 1.96.93 3.1.98v2.55a7.6 7.6 0 0 1-3.35-.78 7.7 7.7 0 0 1-2.25-1.6v6.9c0 3.47-2.82 6.3-6.3 6.3A6.3 6.3 0 0 1 4 13.97a6.3 6.3 0 0 1 6.3-6.3c.33 0 .66.02.97.07v2.68a3.7 3.7 0 0 0-.97-.13 3.68 3.68 0 1 0 3.68 3.68V2z"/></svg>
                        </span>
                        <span class="text-[10px] font-bold">@aes_435</span>
                    </a>
                </div>

                <p class="text-slate-500 text-[11px] font-bold mb-1">Dibuat oleh AES</p>
                <p class="text-amber-400/90 text-[10px] font-bold leading-relaxed">
                    Jika Anda mendapatkan game ini dari sumber lain, harap hubungi admin di atas.
                </p>

            </div>
        </div>
    </div>

    <!-- Fullscreen Button -->
    <div id="btnFullscreen" class="float-btn right-4 top-4" title="Layar Penuh">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M32 32C14.3 32 0 46.3 0 64v96c0 17.7 14.3 32 32 32s32-14.3 32-32V96h64c17.7 0 32-14.3 32-32s-14.3-32-32-32H32zM64 352c0-17.7-14.3-32-32-32s-32 14.3-32 32v96c0 17.7 14.3 32 32 32h96c17.7 0 32-14.3 32-32s-14.3-32-32-32H64V352zM320 32c-17.7 0-32 14.3-32 32s14.3 32 32 32h64v64c0 17.7 14.3 32 32 32s32-14.3 32-32V64c0-17.7-14.3-32-32-32H320zM448 352c0-17.7-14.3-32-32-32s-32 14.3-32 32v64H320c-17.7 0-32 14.3-32 32s14.3 32 32 32h96c17.7 0 32-14.3 32-32V352z"/></svg>
    </div>

    <!-- Home Button (In Game) -->
    <div id="btnHome" class="float-btn left-4 top-4 hidden shadow-[0_0_15px_#ef4444] !border-red-500 hover:!bg-red-500" title="Kembali ke Menu">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path d="M575.8 255.5c0 18-15 32.1-32 32.1h-32l.7 160.2c.2 35.5-28.5 64.3-64 64.3H128.1c-35.3 0-64-28.7-64-64V287.6H32c-18 0-32-14-32-32.1c0-9 3-17 10-24L266.4 8c7-7 15-8 22-8s15 2 21 7L564.8 231.5c8 7 11 15 11 24z"/></svg>
    </div>

    <video id="input_video" class="hidden" autoplay playsinline></video>
    <canvas id="gameCanvas"></canvas>

    <div class="ui-layer flex flex-col justify-between">
        
        <!-- Heads-Up Display (HUD) Layer -->
        <div id="hudLayer" class="hidden w-full h-full relative">
            <!-- Player 1 Score (Left - Yellow) -->
            <div class="absolute top-4 left-20 score-box border-yellow-400 p-3 md:p-4 rounded-2xl text-center shadow-[0_0_20px_rgba(250,204,21,0.4)] w-36 md:w-44">
                <span class="text-xs font-black uppercase bg-yellow-400 text-black px-2 py-0.5 rounded-md mb-1 inline-block">Kiri</span>
                <h3 id="nameP1HUD" class="text-yellow-300 font-bold text-sm md:text-lg truncate">Siswa Kiri</h3>
                <p id="scoreP1" class="text-3xl md:text-4xl text-white game-font mt-1">0</p>
            </div>

            <!-- Player 2 Score (Right - Blue) -->
            <div class="absolute top-4 right-20 score-box border-blue-400 p-3 md:p-4 rounded-2xl text-center shadow-[0_0_20px_rgba(96,165,250,0.4)] w-36 md:w-44">
                <span class="text-xs font-black uppercase bg-blue-400 text-black px-2 py-0.5 rounded-md mb-1 inline-block">Kanan</span>
                <h3 id="nameP2HUD" class="text-blue-300 font-bold text-sm md:text-lg truncate">Siswa Kanan</h3>
                <p id="scoreP2" class="text-3xl md:text-4xl text-white game-font mt-1">0</p>
            </div>

            <!-- Central Question Display -->
            <div class="absolute top-4 left-1/2 transform -translate-x-1/2 flex flex-col items-center z-40">
                <div class="bg-slate-900/90 backdrop-blur-md px-6 py-1.5 rounded-full border border-slate-700 mb-2 shadow-md">
                    <p id="progressDisplay" class="text-indigo-300 font-extrabold text-sm tracking-wide">Soal: 1/30</p>
                </div>
                <div id="questionContainer" class="bg-indigo-900/95 backdrop-blur-xl shadow-[0_0_30px_rgba(99,102,241,0.5)] rounded-3xl p-4 md:p-6 text-center border-4 border-indigo-400 transform transition-all duration-300 scale-0 min-w-[320px] max-w-[650px]">
                    <h2 id="questionSubject" class="text-indigo-200 text-xs font-black uppercase tracking-widest mb-1">Matematika</h2>
                    <!-- Element Gambar Soal -->
                    <img id="questionImage" class="hidden max-h-32 md:max-h-40 mx-auto mb-2 rounded-xl border-2 border-indigo-300/50 object-contain shadow-md" src="" alt="Gambar Soal">
                    <p id="questionDisplay" class="text-lg md:text-3xl font-extrabold text-white game-font drop-shadow-md leading-snug">
                        Siap?
                    </p>
                </div>
            </div>
        </div>

        <!-- Setup Screen -->
        <div id="setupScreen" class="absolute inset-0 bg-slate-950/95 flex items-center justify-center z-50 interactive-layer overflow-y-auto py-8 px-4">
            <div class="bg-slate-900 p-6 md:p-8 rounded-3xl w-full max-w-3xl shadow-[0_0_50px_rgba(99,102,241,0.3)] border border-slate-800">
                <div class="text-center mb-6">
                    <h1 class="text-4xl md:text-5xl text-indigo-400 mb-1 game-font tracking-wide">Gesture Battle Edu</h1>
                    <p class="text-slate-400 font-bold text-sm">Cerdas Cermat Kinetik AI</p>
                </div>
                
                <div id="cameraStatus" class="flex flex-col items-center mb-4 bg-slate-800/80 p-3 rounded-2xl border border-slate-700">
                    <button id="btnEnableCamera" type="button" class="bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-500 hover:to-purple-500 text-white font-bold py-2.5 px-5 rounded-xl text-sm md:text-base transition-all shadow-lg flex items-center gap-2">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="w-5 h-5" fill="currentColor"><path d="M149.1 64.8L138.7 96H64C28.7 96 0 124.7 0 160V416c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V160c0-35.3-28.7-64-64-64H373.3L362.9 64.8C356.4 45.2 338.1 32 317.4 32H194.6c-20.7 0-39 13.2-45.5 32.8zM256 176a112 112 0 1 1 0 224 112 112 0 1 1 0-224zm0 48a64 64 0 1 0 0 128 64 64 0 1 0 0-128z"/></svg>
                        Aktifkan Kamera
                    </button>
                    <p id="cameraStatusText" class="text-slate-400 font-bold text-xs mt-2 text-center">Klik tombol di atas lalu izinkan akses kamera saat diminta browser</p>
                </div>

                <!-- Input Player Names -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div>
                        <input type="text" id="inpP1Name" class="form-input text-center text-lg text-yellow-400 font-bold bg-slate-800" value="Siswa Kiri" placeholder="Nama Siswa Kiri">
                    </div>
                    <div>
                        <input type="text" id="inpP2Name" class="form-input text-center text-lg text-blue-400 font-bold bg-slate-800" value="Siswa Kanan" placeholder="Nama Siswa Kanan">
                    </div>
                </div>

                <!-- Mode Selector -->
                <div class="flex space-x-2 mb-4 bg-slate-800/50 p-1.5 rounded-xl border border-slate-700">
                    <button id="btnModeAuto" class="flex-1 py-2 px-4 rounded-lg bg-indigo-600 text-white font-bold text-sm transition-all shadow-md">Bank Soal Otomatis</button>
                    <button id="btnModeCustom" class="flex-1 py-2 px-4 rounded-lg text-slate-400 hover:text-white font-bold text-sm transition-all">Edit Soal (Guru)</button>
                </div>

                <!-- Speed Selector -->
                <div class="mb-4 bg-slate-800/50 p-3 rounded-xl border border-slate-700">
                    <div class="flex justify-between items-center mb-2">
                        <label class="text-slate-300 font-bold text-xs">Kecepatan Turun Jawaban</label>
                        <span id="speedValueLabel" class="text-indigo-300 font-black text-xs bg-indigo-900/60 px-2.5 py-0.5 rounded-full">Normal</span>
                    </div>
                    <div class="flex items-center gap-3">
                        <span class="text-lg flex-shrink-0" title="Lambat">🐢</span>
                        <input type="range" id="sliderSpeed" min="0.5" max="2" step="0.1" value="1" class="speed-slider flex-1">
                        <span class="text-lg flex-shrink-0" title="Cepat">🐇</span>
                    </div>
                </div>

                <!-- Academic Configuration (AUTO) -->
                <div id="autoConfigMode" class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                    <div>
                        <label class="block text-slate-300 font-bold text-xs mb-1">Jenjang Pendidikan</label>
                        <select id="selJenjang" class="form-select text-sm py-2">
                            <option value="SD">SD (Sekolah Dasar)</option>
                            <option value="SMP">SMP (Sekolah Menengah Pertama)</option>
                            <option value="SMA">SMA (Sekolah Menengah Atas)</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-slate-300 font-bold text-xs mb-1">Kelas</label>
                        <select id="selKelas" class="form-select text-sm py-2">
                            <!-- Populated dynamically -->
                        </select>
                    </div>
                    <div>
                        <label class="block text-slate-300 font-bold text-xs mb-1">Mata Pelajaran</label>
                        <select id="selMapel" class="form-select text-sm py-2">
                            <option value="Matematika">Matematika</option>
                            <option value="IPA">IPA (Sains)</option>
                            <option value="IPS">IPS (Sosial)</option>
                            <option value="Pendidikan Pancasila">Pendidikan Pancasila</option>
                            <option value="Bahasa Inggris">Bahasa Inggris</option>
                            <option value="Bahasa Indonesia">Bahasa Indonesia</option>
                            <option value="Informatika">Informatika / TIK</option>
                            <option value="Penjas">Penjas (PJOK)</option>
                            <option value="Seni Budaya">Seni Budaya</option>
                            <option value="Prakarya">Prakarya</option>
                            <option value="Koding dan Kecerdasan Artifisial">Koding dan Kecerdasan Artifisial</option>
                            <option value="Pendidikan Agama Islam">Pendidikan Agama Islam</option>
                            <option value="Pendidikan Agama Kristen">Pendidikan Agama Kristen</option>
                            <option value="Pendidikan Agama Hindu">Pendidikan Agama Hindu</option>
                            <option value="Bahasa Arab">Bahasa Arab</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-slate-300 font-bold text-xs mb-1">Tingkat Kesulitan</label>
                        <select id="selTingkat" class="form-select text-sm py-2">
                            <option value="Mudah">Mudah</option>
                            <option value="Sedang">Sedang</option>
                            <option value="Sulit">Sulit</option>
                        </select>
                    </div>
                    <div class="md:col-span-2 bg-indigo-900/40 p-3 rounded-xl border border-indigo-500/30 flex items-center justify-between">
                        <label class="text-indigo-200 font-bold text-sm">Jumlah Soal (1 - 30):</label>
                        <input type="number" id="inpJumlah" class="form-input w-24 text-center text-xl font-black text-indigo-300 py-1" min="1" max="30" value="30">
                    </div>
                </div>

                <!-- Custom Configuration (CUSTOM) -->
                <div id="customConfigMode" class="hidden mb-6 flex flex-col space-y-3">
                    <div class="flex justify-between items-center gap-2">
                        <div class="bg-indigo-900/40 border border-indigo-500/50 text-indigo-200 text-xs p-2 rounded-xl flex-1">
                            <strong>Mode Guru:</strong> Buat, Simpan (Ekspor), atau Muat (Impor) file JSON soal.
                        </div>
                        <div class="flex gap-2">
                            <button id="btnExport" class="bg-emerald-600 hover:bg-emerald-500 text-white font-bold py-2 px-3 rounded-xl text-xs transition-all flex items-center gap-1 shadow-lg">
                                Ekspor JSON
                            </button>
                            <label class="bg-amber-600 hover:bg-amber-500 text-white font-bold py-2 px-3 rounded-xl text-xs transition-all flex items-center gap-1 shadow-lg cursor-pointer">
                                Impor JSON
                                <input type="file" id="inpImport" accept=".json,application/json,text/plain,*/*" class="hidden">
                            </label>
                        </div>
                    </div>
                    <div id="customQuestionsContainer" class="max-h-[35vh] overflow-y-auto pr-2 space-y-3 custom-scrollbar">
                        <!-- Custom Questions injected via JS -->
                    </div>
                    <button id="btnAddCustom" class="bg-slate-800 hover:bg-slate-700 text-indigo-400 font-bold py-2 rounded-xl border-2 border-dashed border-indigo-500/50 transition-all text-sm mt-1">
                        + Tambah Soal
                    </button>
                </div>
                
                <div id="setupError" class="hidden bg-red-900/80 border-2 border-red-500 text-red-200 px-4 py-3 rounded-xl mb-4 text-center font-bold text-sm shadow-lg"></div>

                <button id="btnStart" disabled class="w-full bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-500 hover:to-purple-500 disabled:from-slate-700 disabled:to-slate-800 disabled:cursor-not-allowed text-white text-xl md:text-2xl font-bold py-4 rounded-2xl shadow-xl transform transition hover:-translate-y-0.5 active:translate-y-0 game-font">
                    Gunakan Soal & Mulai Main
                </button>
            </div>
        </div>
        
        <!-- Game Over Screen -->
        <div id="gameOverScreen" class="hidden absolute inset-0 bg-slate-950/95 flex flex-col items-center justify-center z-50 interactive-layer p-4">
            <h1 class="text-4xl md:text-6xl text-white mb-8 game-font drop-shadow-lg text-center">Permainan Selesai!</h1>
            
            <div class="flex flex-wrap justify-center gap-6 md:gap-12 mb-8 items-center">
                <div class="flex flex-col items-center">
                    <h2 id="nameP1GO" class="text-yellow-400 font-bold text-xl md:text-2xl mb-2">Siswa Kiri</h2>
                    <div class="bg-slate-900 border-4 border-yellow-400 w-28 h-28 flex items-center justify-center rounded-3xl shadow-[0_0_35px_rgba(250,204,21,0.3)]">
                        <span id="finalScoreP1" class="text-5xl text-white game-font">0</span>
                    </div>
                </div>
                
                <div id="winnerBadge" class="bg-gradient-to-r from-indigo-500 to-pink-500 px-6 py-3 rounded-full shadow-2xl border-2 border-white my-2">
                    <span id="winnerText" class="text-white font-bold text-lg md:text-2xl game-font text-center block whitespace-pre-line leading-tight">SERI!</span>
                </div>

                <div class="flex flex-col items-center">
                    <h2 id="nameP2GO" class="text-blue-400 font-bold text-xl md:text-2xl mb-2">Siswa Kanan</h2>
                    <div class="bg-slate-900 border-4 border-blue-400 w-28 h-28 flex items-center justify-center rounded-3xl shadow-[0_0_35px_rgba(96,165,250,0.3)]">
                        <span id="finalScoreP2" class="text-5xl text-white game-font">0</span>
                    </div>
                </div>
            </div>

            <button id="btnRestart" class="bg-emerald-500 hover:bg-emerald-400 text-white text-2xl font-bold py-3 px-10 rounded-2xl shadow-xl transform transition hover:scale-105 active:scale-95 game-font">
                Main Lagi
            </button>
        </div>
    </div>

    <script>
        // --- GERBANG PASSWORD (Harus lolos sebelum mengakses game) ---
        const GATE_PASSWORD = "AES00GGB";
        const passwordScreen = document.getElementById('passwordScreen');
        const inpGatePassword = document.getElementById('inpGatePassword');
        const gatePasswordError = document.getElementById('gatePasswordError');
        const btnUnlockGate = document.getElementById('btnUnlockGate');

        function tryUnlockGate() {
            if (inpGatePassword.value === GATE_PASSWORD) {
                passwordScreen.classList.add('hidden');
                gatePasswordError.classList.add('hidden');
            } else {
                gatePasswordError.classList.remove('hidden');
                inpGatePassword.value = '';
                inpGatePassword.focus();
            }
        }
        btnUnlockGate.addEventListener('click', tryUnlockGate);
        inpGatePassword.addEventListener('keydown', (e) => { if (e.key === 'Enter') tryUnlockGate(); });

        // --- Fullscreen & Home Handlers ---
        const btnFullscreen = document.getElementById('btnFullscreen');
        const btnHome = document.getElementById('btnHome');

        btnFullscreen.addEventListener('click', () => {
            if (!document.fullscreenElement) {
                document.documentElement.requestFullscreen().catch(err => console.log(err));
            } else {
                document.exitFullscreen();
            }
        });

        btnHome.addEventListener('click', () => {
            gameState = 'SETUP';
            document.getElementById('hudLayer').classList.add('hidden');
            document.getElementById('btnHome').classList.add('hidden');
            document.getElementById('setupScreen').classList.remove('hidden');
            fallingItems = [];
            particles = [];
        });

        // --- UI Setup & Select Handlers ---
        const selJenjang = document.getElementById('selJenjang');
        const selKelas = document.getElementById('selKelas');
        
        const kelasMap = {
            'SD': ['1', '2', '3', '4', '5', '6'],
            'SMP': ['7', '8', '9'],
            'SMA': ['10', '11', '12']
        };

        function updateKelas() {
            const jenjang = selJenjang.value;
            selKelas.innerHTML = '';
            kelasMap[jenjang].forEach(kls => {
                const opt = document.createElement('option');
                opt.value = kls;
                opt.textContent = `Kelas ${kls}`;
                selKelas.appendChild(opt);
            });
        }
        selJenjang.addEventListener('change', updateKelas);
        updateKelas();

        // --- Tone.js Audio System ---
        let synthCorrect, synthWrong, synthStart;
        async function initAudio() {
            if (Tone.context.state !== 'running') await Tone.start();
            if (!synthCorrect) {
                synthCorrect = new Tone.PolySynth(Tone.Synth).toDestination();
                synthCorrect.volume.value = -6; 
                synthWrong = new Tone.MembraneSynth().toDestination();
                synthWrong.volume.value = -3;
                synthStart = new Tone.Synth().toDestination();
                synthStart.volume.value = -6;
            }
        }
        function playCorrectSound() { if(synthCorrect) synthCorrect.triggerAttackRelease(["C5", "E5", "G5"], "8n"); }
        function playWrongSound() { if(synthWrong) synthWrong.triggerAttackRelease("C2", "8n"); }
        function playStartSound() {
            if(!synthStart) return;
            const now = Tone.now();
            synthStart.triggerAttackRelease("C4", "8n", now);
            synthStart.triggerAttackRelease("E4", "8n", now + 0.12);
            synthStart.triggerAttackRelease("G4", "8n", now + 0.24);
            synthStart.triggerAttackRelease("C5", "4n", now + 0.36);
        }

        // --- DYNAMIC QUESTION GENERATOR ENGINE ---
        // Menjamin >30 soal unik yang spesifik per jenjang (SD/SMP/SMA) & Tingkat Kesulitan
        function generateQuestions(subject, jenjang, tingkat, count, kelas) {
            let questions = [];
            let generatedSet = new Set(); // To ensure uniqueness
            let attempts = 0;

            const getRandomInt = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;
            
            while(questions.length < count && attempts < 1000) {
                attempts++;
                let qText = "", ans = "", w1="", w2="", w3="";

                if (subject === 'Matematika') {
                    if (jenjang === 'SD') {
                        // SD: Aritmatika Dasar
                        let maxVal = tingkat === 'Mudah' ? 20 : (tingkat === 'Sedang' ? 50 : 100);
                        let ops = tingkat === 'Mudah' ? ['+', '-'] : ['+', '-', 'x'];
                        let op = ops[getRandomInt(0, ops.length - 1)];
                        let a = getRandomInt(1, maxVal);
                        let b = getRandomInt(1, op === 'x' ? Math.min(maxVal, 10) : maxVal);
                        
                        if (op === '-' && a < b) [a, b] = [b, a]; // Avoid negative for SD
                        
                        qText = `${a} ${op} ${b} = ... ?`;
                        ans = (op === '+' ? a+b : (op === '-' ? a-b : a*b)).toString();
                    } else if (jenjang === 'SMP') {
                        // SMP: Aljabar Dasar, Pecahan, Pangkat
                        let type = getRandomInt(1, 3);
                        if (type === 1) { // Persamaan Linear
                            let x = getRandomInt(2, tingkat==='Mudah'?5:15);
                            let y = getRandomInt(1, 10);
                            let result = (x * 2) + y;
                            qText = `Jika 2x + ${y} = ${result}, maka nilai x adalah?`;
                            ans = x.toString();
                        } else if (type === 2) { // Luas Bangun
                            let sisi = getRandomInt(4, tingkat==='Mudah'?10:25);
                            qText = `Luas persegi dengan sisi ${sisi} cm adalah?`;
                            ans = (sisi*sisi).toString();
                        } else { // Akar
                            let num = getRandomInt(5, tingkat==='Mudah'?10:20);
                            qText = `Hasil dari √${num*num} adalah?`;
                            ans = num.toString();
                        }
                    } else { // SMA
                        // SMA: Logaritma, Trigonometri, Turunan Dasar
                        let type = getRandomInt(1, 3);
                        if (type === 1) { // Turunan
                            let a = getRandomInt(2, tingkat==='Mudah'?6:8);
                            let n = getRandomInt(2, tingkat==='Mudah'?4:5);
                            qText = `Turunan pertama dari f(x) = ${a}x^${n} adalah?`;
                            ans = `${a*n}x^${n-1}`;
                        } else if (type === 2) { // Peluang/Kombinasi
                            let n = getRandomInt(3, 8);
                            qText = `Nilai dari ${n}! (Faktorial) adalah?`;
                            let fact = 1; for(let i=1; i<=n; i++) fact *= i;
                            ans = fact.toString();
                        } else { // Trigonometri
                            let angles = [0, 30, 45, 60, 90];
                            let ang = angles[getRandomInt(0, angles.length-1)];
                            let func = getRandomInt(0,1) === 0 ? 'Sin' : 'Cos';
                            qText = `Nilai ${func}(${ang}°) = ...`;
                            if(func === 'Sin') {
                                if(ang==0) ans="0"; else if(ang==30) ans="1/2"; else if(ang==45) ans="1/2 √2"; else if(ang==60) ans="1/2 √3"; else ans="1";
                            } else {
                                if(ang==0) ans="1"; else if(ang==30) ans="1/2 √3"; else if(ang==45) ans="1/2 √2"; else if(ang==60) ans="1/2"; else ans="0";
                            }
                        }
                    }
                    
                    // Generate Pengecoh Matematika yang masuk akal
                    let tempAns = parseInt(ans);
                    if(!isNaN(tempAns)) {
                        w1 = (tempAns + getRandomInt(1, 5)).toString();
                        w2 = (tempAns - getRandomInt(1, 5)).toString();
                        w3 = (tempAns + getRandomInt(6, 10)).toString();
                        if(w2 < 0 && jenjang === 'SD') w2 = (tempAns + 15).toString();
                    } else {
                        w1 = ans.replace(/[0-9]/, (m) => parseInt(m)+1);
                        w2 = ans.replace(/[0-9]/, (m) => Math.max(1, parseInt(m)-1));
                        w3 = "Tidak terdefinisi";
                    }
                } 
                else if (subject === 'Bahasa Inggris') {
                    if (jenjang === 'SD') { // Vocab
                        const vocab = [["Apple","Apel","Jeruk","Pisang","Mangga"], ["Red","Merah","Biru","Hijau","Kuning"], ["Cat","Kucing","Anjing","Tikus","Burung"], ["Book","Buku","Pensil","Meja","Tas"], ["Water","Air","Api","Tanah","Udara"], ["Sun","Matahari","Bulan","Bintang","Awan"], ["Hand","Tangan","Kaki","Kepala","Mata"], ["Dog","Anjing","Kucing","Kelinci","Ayam"], ["Blue","Biru","Merah","Hijau","Ungu"], ["Green","Hijau","Biru","Merah","Kuning"], ["Yellow","Kuning","Hijau","Biru","Merah"], ["House","Rumah","Sekolah","Kantor","Pasar"], ["School","Sekolah","Rumah","Pasar","Taman"], ["Chair","Kursi","Meja","Lemari","Pintu"], ["Table","Meja","Kursi","Lemari","Jendela"], ["Bird","Burung","Ikan","Kucing","Anjing"], ["Fish","Ikan","Burung","Ayam","Sapi"], ["Eye","Mata","Hidung","Telinga","Mulut"], ["Ear","Telinga","Mata","Hidung","Mulut"], ["Nose","Hidung","Mata","Telinga","Mulut"], ["Milk","Susu","Air","Teh","Kopi"], ["Bread","Roti","Nasi","Mie","Kue"], ["Rain","Hujan","Angin","Petir","Awan"], ["Moon","Bulan","Matahari","Bintang","Awan"], ["Star","Bintang","Bulan","Matahari","Awan"], ["Big","Besar","Kecil","Panjang","Pendek"], ["Small","Kecil","Besar","Tinggi","Rendah"], ["Happy","Senang","Sedih","Marah","Takut"], ["Sad","Sedih","Senang","Marah","Takut"], ["Friend","Teman","Musuh","Guru","Orang tua"]];
                        let v = vocab[getRandomInt(0, vocab.length-1)];
                        qText = `Apa arti dari kata "${v[0]}"?`;
                        [ans, w1, w2, w3] = [v[1], v[2], v[3], v[4]];
                    } else if (jenjang === 'SMP') { // Tenses / Basic Grammar
                        const verbs = [["go","went","gone"], ["eat","ate","eaten"], ["see","saw","seen"], ["write","wrote","written"], ["buy","bought","bought"], ["take","took","taken"], ["give","gave","given"], ["come","came","come"], ["make","made","made"], ["do","did","done"], ["drink","drank","drunk"], ["speak","spoke","spoken"], ["break","broke","broken"], ["drive","drove","driven"], ["sing","sang","sung"], ["run","ran","run"], ["swim","swam","swum"], ["fall","fell","fallen"], ["know","knew","known"], ["grow","grew","grown"], ["begin","began","begun"], ["choose","chose","chosen"], ["fly","flew","flown"], ["forget","forgot","forgotten"], ["hide","hid","hidden"], ["ride","rode","ridden"], ["rise","rose","risen"], ["steal","stole","stolen"], ["throw","threw","thrown"], ["wake","woke","woken"]];
                        let v = verbs[getRandomInt(0, verbs.length-1)];
                        qText = `Bentuk Past Tense (V2) dari "${v[0]}" adalah?`;
                        ans = v[1]; w1 = v[2]; w2 = v[0]+"ed"; w3 = v[0]+"ing";
                    } else { // SMA: Idioms / Complex
                        const idioms = [["Break a leg","Good luck","Hurt yourself","Dance well","Run fast"], ["Under the weather","Sick","Raining","Cold","Happy"], ["Piece of cake","Very easy","Dessert","Hard task","Sweet"], ["Hit the books","Belajar dengan giat","Memukul buku","Membeli buku","Membaca komik"], ["Once in a blue moon","Sangat jarang terjadi","Setiap bulan","Malam hari","Warna langit"], ["Cost an arm and a leg","Sangat mahal","Sangat murah","Menyakitkan","Butuh operasi"], ["Let the cat out of the bag","Membocorkan rahasia","Melepas kucing","Menyembunyikan sesuatu","Bermain dengan kucing"], ["Break the ice","Mencairkan suasana","Memecahkan es","Membuat dingin","Marah besar"], ["Bite the bullet","Menghadapi hal sulit dengan berani","Menggigit peluru","Menembak","Menghindar"], ["Call it a day","Mengakhiri pekerjaan untuk hari itu","Menyebutnya hari","Memulai hari","Bekerja lembur"], ["Get out of hand","Menjadi tidak terkendali","Keluar dari tangan","Melepaskan diri","Menyerah"], ["Hang in there","Bertahanlah","Menggantung di sana","Pergi ke sana","Berhenti mencoba"], ["Miss the boat","Kehilangan kesempatan","Ketinggalan kapal","Naik kapal","Berenang"], ["On the ball","Cepat tanggap dan kompeten","Bermain bola","Di atas bola","Malas bekerja"], ["Speak of the devil","Membicarakan seseorang yang tiba-tiba muncul","Berbicara dengan setan","Menakut-nakuti","Marah besar"], ["The ball is in your court","Keputusan ada di tanganmu","Bola ada di lapanganmu","Bermain tenis","Menunggu giliran"], ["Time flies","Waktu berlalu dengan cepat","Waktu terbang","Jam rusak","Terlambat"], ["Add fuel to the fire","Memperburuk keadaan","Menambah bahan bakar","Memadamkan api","Menyalakan lilin"], ["Beat around the bush","Berbicara berbelit-belit","Memukul semak","Berjalan mengelilingi","Bersembunyi"], ["Actions speak louder than words","Perbuatan lebih berarti daripada ucapan","Berteriak lebih keras","Diam lebih baik","Kata-kata lebih penting"], ["A blessing in disguise","Hikmah di balik musibah","Berkat yang tersembunyi secara harfiah","Kutukan","Keberuntungan buruk"], ["Burn the midnight oil","Belajar atau bekerja hingga larut malam","Membakar minyak","Tidur larut","Menyalakan lampu"], ["Get a taste of your own medicine","Menerima perlakuan yang sama seperti yang diberikan","Meminum obat sendiri","Sakit","Sembuh sendiri"], ["Kill two birds with one stone","Menyelesaikan dua hal sekaligus","Membunuh dua burung","Melempar batu","Berburu"], ["Let sleeping dogs lie","Jangan mengungkit masalah lama","Membiarkan anjing tidur","Mengganggu hewan","Diam saja"], ["Pull yourself together","Tenangkan dirimu","Menarik diri sendiri","Berkumpul bersama","Bekerja sama"], ["See eye to eye","Sependapat","Melihat mata ke mata secara harfiah","Bertengkar","Menghindar"], ["Speak your mind","Mengungkapkan pendapat dengan jujur","Berbicara dalam hati","Diam saja","Berbisik"], ["Take it with a grain of salt","Jangan terlalu percaya begitu saja","Menambahkan garam","Memasak dengan garam","Merasakan asin"], ["The best of both worlds","Mendapatkan keuntungan dari dua situasi","Dunia terbaik secara harfiah","Memilih salah satu","Kehilangan keduanya"]];
                        let v = idioms[getRandomInt(0, idioms.length-1)];
                        qText = `Apa makna dari idiom "${v[0]}"?`;
                        [ans, w1, w2, w3] = [v[1], v[2], v[3], v[4]];
                    }
                }
                else {
                    // Penanganan dinamis untuk mapel IPA, IPS, Bahasa Indonesia, TIK
                    // Untuk memastikan 30 unik, kita gabungkan template kalimat + array fakta
                    const factBanks = {
                        'IPA': {
                            'SD': [["Tumbuhan membuat makanan dengan proses yang disebut","Fotosintesis","Respirasi","Osmosis","Mencair"], ["Planet pusat tata surya adalah","Matahari","Bumi","Bulan","Mars"], ["Hewan pemakan daging disebut","Karnivora","Herbivora","Omnivora","Insektivora"], ["Hewan pemakan tumbuhan disebut","Herbivora","Karnivora","Omnivora","Insektivora"], ["Hewan pemakan segala disebut","Omnivora","Herbivora","Karnivora","Insektivora"], ["Alat pernapasan manusia adalah","Paru-paru","Jantung","Hati","Ginjal"], ["Alat pemompa darah dalam tubuh adalah","Jantung","Paru-paru","Hati","Ginjal"], ["Wujud benda yang bentuknya tetap adalah","Padat","Cair","Gas","Plasma"], ["Wujud benda yang mengikuti bentuk wadahnya adalah","Cair","Padat","Gas","Plasma"], ["Proses perubahan air menjadi uap disebut","Menguap","Mengembun","Membeku","Mencair"], ["Proses perubahan uap menjadi air disebut","Mengembun","Menguap","Membeku","Menyublim"], ["Proses perubahan air menjadi es disebut","Membeku","Mencair","Menguap","Menyublim"], ["Bagian tumbuhan yang menyerap air dan mineral adalah","Akar","Batang","Daun","Bunga"], ["Bagian tumbuhan tempat terjadinya fotosintesis adalah","Daun","Akar","Batang","Bunga"], ["Hewan yang berkembang biak dengan bertelur disebut","Ovipar","Vivipar","Ovovivipar","Membelah diri"], ["Hewan yang berkembang biak dengan melahirkan disebut","Vivipar","Ovipar","Ovovivipar","Membelah diri"], ["Gaya yang menyebabkan benda jatuh ke bawah disebut","Gravitasi","Gesekan","Magnet","Pegas"], ["Sumber energi utama di bumi adalah","Matahari","Bulan","Bintang","Angin"], ["Alat untuk melihat benda yang sangat kecil adalah","Mikroskop","Teleskop","Kaca pembesar","Periskop"], ["Alat untuk melihat benda yang jauh adalah","Teleskop","Mikroskop","Kaca pembesar","Periskop"], ["Satelit alami bumi adalah","Bulan","Matahari","Mars","Venus"], ["Planet terdekat dengan matahari adalah","Merkurius","Venus","Bumi","Mars"], ["Lapisan bumi yang paling luar disebut","Kerak bumi","Inti bumi","Mantel bumi","Atmosfer"], ["Pori-pori pada daun tempat tumbuhan bernapas disebut","Stomata","Fotosintesis","Respirasi","Transpirasi"], ["Organ yang berfungsi menyaring darah dalam tubuh adalah","Ginjal","Hati","Jantung","Paru-paru"], ["Rangka manusia berfungsi untuk","Menegakkan tubuh","Mencerna makanan","Memompa darah","Bernapas"], ["Contoh sumber energi yang dapat diperbarui adalah","Angin","Minyak bumi","Batu bara","Gas alam"], ["Contoh sumber energi yang tidak dapat diperbarui adalah","Batu bara","Angin","Air","Matahari"], ["Proses daur ulang air di alam disebut","Siklus air","Siklus karbon","Fotosintesis","Respirasi"], ["Alat indera untuk melihat adalah","Mata","Telinga","Hidung","Lidah"]],
                            'SMP': [["Simbol kimia untuk Air adalah","H2O","CO2","O2","NaCl"], ["Satuan gaya dalam SI adalah","Newton","Joule","Watt","Pascal"], ["Organ pencerna racun di tubuh adalah","Hati","Ginjal","Jantung","Paru-paru"], ["Satuan usaha dan energi dalam SI adalah","Joule","Newton","Watt","Pascal"], ["Satuan daya dalam SI adalah","Watt","Newton","Joule","Pascal"], ["Satuan tekanan dalam SI adalah","Pascal","Newton","Joule","Watt"], ["Zat yang mempercepat reaksi kimia tanpa ikut bereaksi disebut","Katalis","Reaktan","Produk","Pelarut"], ["Campuran homogen antara dua zat atau lebih disebut","Larutan","Suspensi","Koloid","Emulsi"], ["Perubahan wujud dari padat langsung menjadi gas disebut","Menyublim","Menguap","Mengembun","Mendeposisi"], ["Alat untuk mengukur kuat arus listrik adalah","Amperemeter","Voltmeter","Ohmmeter","Termometer"], ["Alat untuk mengukur tegangan listrik adalah","Voltmeter","Amperemeter","Ohmmeter","Barometer"], ["Satuan kuat arus listrik dalam SI adalah","Ampere","Volt","Ohm","Watt"], ["Hukum yang menyatakan hubungan arus, tegangan, dan hambatan adalah","Hukum Ohm","Hukum Newton","Hukum Pascal","Hukum Archimedes"], ["Fotosintesis pada tumbuhan menghasilkan","Oksigen dan Glukosa","Karbondioksida dan Air","Nitrogen dan Air","Hidrogen dan Oksigen"], ["Bagian sel yang mengatur seluruh aktivitas sel adalah","Inti sel (Nukleus)","Membran sel","Sitoplasma","Mitokondria"], ["Organel sel yang berfungsi sebagai penghasil energi adalah","Mitokondria","Nukleus","Ribosom","Lisosom"], ["Sistem organ yang berfungsi mengedarkan darah disebut","Sistem peredaran darah","Sistem pencernaan","Sistem pernapasan","Sistem ekskresi"], ["Zat yang bersifat asam memiliki pH","Kurang dari 7","Sama dengan 7","Lebih dari 7","Sama dengan 14"], ["Zat yang bersifat basa memiliki pH","Lebih dari 7","Kurang dari 7","Sama dengan 0","Sama dengan 7"], ["Getaran yang merambat dan menghasilkan bunyi disebut","Gelombang bunyi","Gelombang cahaya","Gelombang radio","Gelombang elektromagnetik"], ["Peristiwa pembelokan cahaya saat melewati dua medium berbeda disebut","Pembiasan","Pemantulan","Interferensi","Difraksi"], ["Bayangan pada cermin datar bersifat","Maya dan tegak","Nyata dan terbalik","Maya dan terbalik","Nyata dan tegak"], ["Gaya yang timbul akibat dua permukaan bersentuhan disebut","Gaya gesek","Gaya gravitasi","Gaya magnet","Gaya pegas"], ["Satuan energi kalor adalah","Kalori","Newton","Joule saja","Ampere"], ["Proses perpindahan panas tanpa zat perantara disebut","Radiasi","Konduksi","Konveksi","Isolasi"], ["Proses perpindahan panas melalui zat perantara yang ikut berpindah disebut","Konveksi","Konduksi","Radiasi","Isolasi"], ["Proses perpindahan panas melalui zat perantara tanpa zat itu berpindah disebut","Konduksi","Konveksi","Radiasi","Isolasi"], ["Bagian tumbuhan yang berfungsi sebagai alat kelamin betina adalah","Putik","Benang sari","Kelopak","Mahkota"], ["Bagian tumbuhan yang berfungsi sebagai alat kelamin jantan adalah","Benang sari","Putik","Kelopak","Mahkota"], ["Penyerbukan yang dibantu oleh serangga disebut","Entomogami","Anemogami","Hidrogami","Antropogami"]],
                            'SMA': [["Hukum Pewarisan Sifat ditemukan oleh","Mendel","Darwin","Newton","Einstein"], ["Ikatan antara logam & non-logam disebut","Ionik","Kovalen","Logam","Van der Waals"], ["Proses pembelahan sel tubuh disebut","Mitosis","Meiosis","Biner","Budding"], ["Proses pembelahan sel kelamin disebut","Meiosis","Mitosis","Biner","Budding"], ["Teori evolusi seleksi alam dikemukakan oleh","Charles Darwin","Gregor Mendel","Louis Pasteur","Robert Hooke"], ["Organel sel yang berperan dalam sintesis protein adalah","Ribosom","Mitokondria","Lisosom","Badan Golgi"], ["Satuan mol digunakan untuk menyatakan","Jumlah zat","Massa zat","Volume zat","Suhu zat"], ["Hukum kekekalan energi dikenal sebagai hukum","Termodinamika I","Termodinamika II","Newton I","Newton III"], ["Persamaan gas ideal dirumuskan sebagai","PV = nRT","E = mc kuadrat","F = ma","V = IR"], ["Reaksi eksoterm adalah reaksi yang","Melepaskan kalor","Menyerap kalor","Tidak melibatkan kalor","Menghasilkan gas saja"], ["Reaksi endoterm adalah reaksi yang","Menyerap kalor","Melepaskan kalor","Tidak melibatkan kalor","Menghasilkan gas saja"], ["Partikel penyusun inti atom yang bermuatan positif adalah","Proton","Elektron","Neutron","Foton"], ["Partikel penyusun inti atom yang tidak bermuatan adalah","Neutron","Proton","Elektron","Foton"], ["Partikel bermuatan negatif yang mengelilingi inti atom adalah","Elektron","Proton","Neutron","Foton"], ["Hukum Newton yang menyatakan aksi sama dengan reaksi adalah hukum Newton ke-","3","1","2","4"], ["Hukum Newton tentang kelembaman adalah hukum Newton ke-","1","2","3","4"], ["Proses respirasi sel menghasilkan energi dalam bentuk","ATP","ADP","DNA","RNA"], ["Materi genetik pembawa sifat keturunan adalah","DNA","ATP","Protein","Lipid"], ["Enzim yang mempercepat reaksi biokimia disebut juga","Biokatalisator","Substrat","Produk","Koenzim saja"], ["Fotosintesis mengubah energi cahaya menjadi energi","Kimia","Kinetik","Panas","Listrik"], ["Model atom orbital dikemukakan oleh","Niels Bohr","John Dalton","J.J. Thomson","Rutherford"], ["Model atom roti kismis dikemukakan oleh","J.J. Thomson","Niels Bohr","Rutherford","Dalton"], ["Bilangan Avogadro bernilai sekitar","6,02 x 10^23","3,14","9,8","1,6 x 10^-19"], ["Satuan kekuatan arus dalam rangkaian listrik adalah","Ampere","Volt","Ohm","Watt"], ["Gelombang elektromagnetik dengan panjang gelombang terpendek adalah","Sinar gamma","Gelombang radio","Sinar tampak","Inframerah"], ["Proses pindah silang pada pembelahan sel terjadi pada tahap","Meiosis I","Mitosis","Interfase","Meiosis II saja"], ["Senyawa yang tersusun dari satu jenis unsur disebut","Unsur","Senyawa","Campuran","Larutan"], ["Zat yang terbentuk dari gabungan dua unsur atau lebih secara kimia disebut","Senyawa","Unsur","Campuran","Larutan"], ["Hormon yang mengatur kadar gula darah adalah","Insulin","Adrenalin","Tiroksin","Estrogen"], ["Bagian otak yang mengatur keseimbangan tubuh adalah","Otak kecil (Serebelum)","Otak besar (Serebrum)","Sumsum tulang belakang","Batang otak saja"]],
                        },
                        'IPS': {
                            'SD': [["Ibu kota negara Indonesia adalah","Nusantara","Jakarta","Bandung","Surabaya"], ["Arah matahari terbit adalah","Timur","Barat","Utara","Selatan"], ["Mata uang Indonesia adalah","Rupiah","Dollar","Ringgit","Yen"], ["Presiden pertama Indonesia adalah","Soekarno","Soeharto","Habibie","Megawati"], ["Hari Kemerdekaan Indonesia diperingati tanggal","17 Agustus","1 Juni","28 Oktober","10 November"], ["Lambang negara Indonesia adalah","Garuda Pancasila","Bhinneka Tunggal Ika","Merah Putih","Pancasila saja"], ["Bendera Indonesia berwarna","Merah Putih","Merah Kuning","Putih Biru","Kuning Hijau"], ["Lagu kebangsaan Indonesia berjudul","Indonesia Raya","Garuda Pancasila","Bagimu Negeri","Halo-Halo Bandung"], ["Pulau terbesar di Indonesia adalah","Kalimantan","Jawa","Sumatra","Sulawesi"], ["Gunung tertinggi di Indonesia adalah","Puncak Jaya","Gunung Semeru","Gunung Merapi","Gunung Rinjani"], ["Kegiatan menghasilkan barang atau jasa disebut","Produksi","Distribusi","Konsumsi","Promosi"], ["Kegiatan menyalurkan barang dari produsen ke konsumen disebut","Distribusi","Produksi","Konsumsi","Promosi"], ["Kegiatan menggunakan atau memakai barang disebut","Konsumsi","Produksi","Distribusi","Promosi"], ["Tempat jual beli barang secara langsung disebut","Pasar","Bank","Koperasi","Kantor"], ["Alat tukar yang sah dalam kegiatan ekonomi disebut","Uang","Barang","Jasa","Emas saja"], ["Koperasi didirikan dengan tujuan untuk","Kesejahteraan anggota","Mencari untung sebesar-besarnya","Bersaing dengan pasar","Menjual saham"], ["Kenampakan alam berupa dataran tinggi disebut","Dataran tinggi","Lembah","Pantai","Delta"], ["Kenampakan alam tempat pertemuan air laut dan daratan disebut","Pantai","Dataran tinggi","Lembah","Gurun"], ["Peta yang menggambarkan seluruh permukaan bumi disebut","Atlas","Globe","Denah","Legenda"], ["Alat peraga berbentuk bola yang menggambarkan bumi disebut","Globe","Atlas","Peta","Denah"], ["Suku bangsa yang berasal dari Pulau Jawa adalah","Jawa","Batak","Minang","Dayak"], ["Suku bangsa yang berasal dari Sumatra Utara adalah","Batak","Jawa","Bugis","Dayak"], ["Rumah adat Toraja disebut","Tongkonan","Joglo","Gadang","Honai"], ["Rumah adat Jawa disebut","Joglo","Tongkonan","Gadang","Honai"], ["Tari Kecak berasal dari daerah","Bali","Jawa","Sumatra","Kalimantan"], ["Tari Piring berasal dari daerah","Sumatra Barat","Bali","Jawa Tengah","Papua"], ["Candi Prambanan terletak di provinsi","DI Yogyakarta","Jawa Timur","Jawa Barat","Bali"], ["Wayang kulit adalah kesenian tradisional dari","Jawa","Sumatra","Papua","Kalimantan"], ["Batik merupakan warisan budaya asli dari","Indonesia","Malaysia","Thailand","Filipina"], ["Proklamasi Kemerdekaan Indonesia dibacakan oleh","Soekarno-Hatta","Soeharto","Sudirman","Sutan Syahrir"]],
                            'SMP': [["Benua terluas di dunia adalah","Asia","Afrika","Amerika","Eropa"], ["Organisasi PBB singkatan dari","Perserikatan Bangsa-Bangsa","Persekutuan Bangsa Baru","Persatuan Bela Bangsa","Partai Bangsa Bersatu"], ["Candi Borobudur ada di provinsi","Jawa Tengah","Jawa Timur","Jawa Barat","Bali"], ["Samudra terluas di dunia adalah","Pasifik","Atlantik","Hindia","Arktik"], ["Benua yang terletak di kutub selatan adalah","Antartika","Asia","Afrika","Australia"], ["Organisasi kerja sama negara-negara Asia Tenggara adalah","ASEAN","PBB","Uni Eropa","OPEC"], ["Ilmu yang mempelajari tentang penduduk disebut","Demografi","Geografi","Ekonomi","Sosiologi"], ["Kegiatan ekonomi yang melibatkan permintaan dan penawaran disebut","Pasar","Produksi","Distribusi","Konsumsi"], ["Hukum yang menyatakan makin tinggi harga makin rendah permintaan disebut","Hukum permintaan","Hukum penawaran","Hukum Gossen","Hukum Engel"], ["Sistem ekonomi yang dianut Indonesia adalah","Ekonomi Pancasila","Kapitalisme murni","Sosialisme murni","Komunisme"], ["Peristiwa Sumpah Pemuda terjadi pada tanggal","28 Oktober 1928","17 Agustus 1945","1 Juni 1945","10 November 1945"], ["Peristiwa Rengasdengklok terjadi menjelang","Proklamasi Kemerdekaan","Sumpah Pemuda","Konferensi Meja Bundar","Perjanjian Renville"], ["Organisasi pergerakan nasional pertama di Indonesia adalah","Budi Utomo","Sarekat Islam","Indische Partij","PNI"], ["Perang Diponegoro terjadi di wilayah","Jawa Tengah","Jawa Barat","Sumatra","Kalimantan"], ["VOC adalah kongsi dagang milik","Belanda","Inggris","Portugis","Spanyol"], ["Rempah-rempah yang diperebutkan bangsa Eropa berasal dari","Maluku","Jawa","Sumatra","Kalimantan"], ["Letak geografis Indonesia berada di antara dua benua yaitu","Asia dan Australia","Asia dan Afrika","Eropa dan Asia","Amerika dan Afrika"], ["Letak geografis Indonesia berada di antara dua samudra yaitu","Pasifik dan Hindia","Atlantik dan Pasifik","Hindia dan Atlantik","Arktik dan Pasifik"], ["Iklim yang dimiliki wilayah Indonesia adalah","Tropis","Subtropis","Dingin","Kutub"], ["Fenomena naiknya suhu global akibat gas rumah kaca disebut","Pemanasan global","Efek Coriolis","La Nina","El Nino"], ["Bentuk kerja sama ekonomi antarnegara ASEAN disebut","AFTA","NAFTA","APEC","WTO"], ["Lembaga keuangan yang menghimpun dan menyalurkan dana masyarakat disebut","Bank","Pasar","Koperasi","Bursa saja"], ["Kegiatan jual beli saham dilakukan di","Bursa efek","Bank","Koperasi","Pasar tradisional"], ["Peta yang menunjukkan persebaran suatu fenomena disebut","Peta tematik","Peta umum","Atlas","Globe"], ["Skala peta menunjukkan","Perbandingan jarak peta dan jarak sebenarnya","Luas wilayah","Jumlah penduduk","Ketinggian tempat"], ["Interaksi sosial yang mengarah pada persatuan disebut","Asosiatif","Disosiatif","Konflik","Kontravensi"], ["Interaksi sosial yang mengarah pada perpecahan disebut","Disosiatif","Asosiatif","Kerja sama","Akomodasi"], ["Proses penyesuaian diri terhadap norma masyarakat disebut","Sosialisasi","Akulturasi","Asimilasi","Interaksi saja"], ["Percampuran dua kebudayaan tanpa menghilangkan unsur asli disebut","Akulturasi","Asimilasi","Sosialisasi","Disosiatif"], ["Percampuran dua kebudayaan yang melebur menjadi budaya baru disebut","Asimilasi","Akulturasi","Sosialisasi","Disosiatif"]],
                            'SMA': [["Paham ekonomi pasar bebas disebut","Kapitalisme","Sosialisme","Komunisme","Merkantilisme"], ["Letak astronomis Indonesia berada di garis","Khatulistiwa","Bujur Nol","Balik Utara","Batas Tanggal"], ["Konferensi Asia Afrika 1955 diadakan di","Bandung","Jakarta","Bogor","Bali"], ["Ilmu yang mempelajari perilaku manusia dalam memenuhi kebutuhan disebut","Ekonomi","Sosiologi","Antropologi","Geografi"], ["Kebijakan moneter dikeluarkan oleh","Bank Sentral","Kementerian Keuangan","DPR","Presiden"], ["Kebijakan fiskal berkaitan dengan","Pajak dan anggaran negara","Suku bunga","Nilai tukar","Jumlah uang beredar"], ["Inflasi adalah keadaan di mana","Harga barang naik terus-menerus","Harga barang turun terus","Nilai uang menguat","Produksi meningkat pesat"], ["Deflasi adalah keadaan di mana","Harga barang turun terus-menerus","Harga barang naik terus","Nilai uang melemah","Produksi menurun drastis"], ["Pendapatan nasional dapat dihitung dengan pendekatan","Produksi, Pendapatan, Pengeluaran","Produksi saja","Pengeluaran saja","Pendapatan saja"], ["Organisasi negara pengekspor minyak disebut","OPEC","ASEAN","WTO","IMF"], ["Lembaga keuangan internasional yang memberi pinjaman kepada negara berkembang adalah","IMF","ASEAN","OPEC","WHO"], ["Perang Dunia II berakhir pada tahun","1945","1939","1918","1950"], ["Perang Dunia I berakhir pada tahun","1918","1945","1939","1950"], ["Pemimpin gerakan non-blok dari Indonesia adalah","Soekarno","Soeharto","Hatta","Sjahrir"], ["Perjanjian yang mengakhiri konflik Indonesia-Belanda adalah","Konferensi Meja Bundar","Perjanjian Renville","Perjanjian Linggarjati","Perjanjian Roem-Royen"], ["Teori masuknya Hindu-Buddha ke Indonesia yang menyebut peran pedagang disebut","Teori Waisya","Teori Ksatria","Teori Brahmana","Teori Arus Balik"], ["Kerajaan maritim terbesar di Nusantara adalah","Sriwijaya","Majapahit","Mataram","Demak"], ["Kerajaan Islam pertama di Jawa adalah","Demak","Mataram","Banten","Cirebon"], ["Revolusi Industri pertama kali terjadi di","Inggris","Prancis","Jerman","Amerika Serikat"], ["Paham yang menekankan kepemilikan bersama alat produksi disebut","Sosialisme","Kapitalisme","Liberalisme","Merkantilisme"], ["Dampak globalisasi di bidang ekonomi antara lain","Perdagangan bebas antarnegara","Isolasi ekonomi","Proteksionisme total","Swasembada mutlak"], ["Bonus demografi adalah kondisi di mana","Usia produktif lebih banyak dari non-produktif","Penduduk menurun drastis","Usia lanjut mendominasi","Kelahiran nol"], ["Fenomena urbanisasi adalah perpindahan penduduk dari","Desa ke kota","Kota ke desa","Pulau ke pulau","Negara ke negara"], ["Teori lokasi industri dikemukakan oleh","Alfred Weber","Adam Smith","David Ricardo","Karl Marx"], ["Konsep pembangunan berkelanjutan menekankan pada","Keseimbangan ekonomi, sosial, dan lingkungan","Pertumbuhan ekonomi semata","Eksploitasi sumber daya maksimal","Industrialisasi cepat"], ["Batas wilayah laut teritorial Indonesia adalah sejauh","12 mil laut","200 mil laut","24 mil laut","6 mil laut"], ["Zona Ekonomi Eksklusif Indonesia adalah sejauh","200 mil laut","12 mil laut","24 mil laut","6 mil laut"], ["Proklamasi Kemerdekaan Indonesia dilaksanakan pada tahun","1945","1928","1949","1950"], ["Pengakuan kedaulatan Indonesia oleh Belanda terjadi pada tahun","1949","1945","1950","1928"], ["Dasar negara Indonesia yang disahkan PPKI adalah","Pancasila","UUD 1945 saja","Piagam Jakarta","Sumpah Pemuda"]],
                        },
                        'Bahasa Indonesia': {
                            'SD': [["Kalimat yang menyatakan perintah disebut kalimat","Perintah","Berita","Tanya","Seru"], ["Kalimat yang menyatakan pertanyaan disebut kalimat","Tanya","Berita","Perintah","Seru"], ["Kalimat yang mengungkapkan perasaan kuat disebut kalimat","Seru","Berita","Tanya","Perintah"], ["Kalimat yang menyampaikan informasi disebut kalimat","Berita","Tanya","Perintah","Seru"], ["Kata yang menunjukkan nama benda disebut","Kata benda","Kata kerja","Kata sifat","Kata keterangan"], ["Kata yang menunjukkan pekerjaan atau tindakan disebut","Kata kerja","Kata benda","Kata sifat","Kata keterangan"], ["Kata yang menerangkan sifat atau keadaan disebut","Kata sifat","Kata benda","Kata kerja","Kata ganti"], ["Lawan kata besar adalah","Kecil","Tinggi","Panjang","Berat"], ["Lawan kata tinggi adalah","Rendah","Kecil","Pendek saja","Sempit"], ["Persamaan kata senang adalah","Gembira","Sedih","Marah","Takut"], ["Persamaan kata cepat adalah","Kilat","Lambat","Diam","Pelan"], ["Puisi anak biasanya menggunakan bahasa yang","Sederhana dan indah","Rumit dan formal","Ilmiah","Baku hukum"], ["Cerita yang berisi tokoh hewan berperilaku seperti manusia disebut","Fabel","Legenda","Mite","Biografi"], ["Cerita rakyat tentang asal usul suatu tempat disebut","Legenda","Fabel","Mite","Biografi"], ["Bagian awal surat yang berisi sapaan disebut","Salam pembuka","Isi surat","Salam penutup","Alamat"], ["Bagian akhir surat yang berisi penutup disebut","Salam penutup","Salam pembuka","Isi surat","Tanggal"], ["Karangan yang menceritakan pengalaman pribadi disebut","Cerita pengalaman","Puisi","Pantun","Iklan"], ["Pantun bersajak","a-b-a-b","a-a-a-a","a-b-b-a","a-a-b-b"], ["Bagian pantun yang berisi maksud disebut","Isi","Sampiran","Sajak","Rima"], ["Bagian pantun yang berupa pembayang disebut","Sampiran","Isi","Sajak","Rima"], ["Huruf pertama pada awal kalimat ditulis dengan huruf","Kapital","Kecil","Tebal","Miring"], ["Tanda baca yang digunakan untuk mengakhiri kalimat berita adalah","Titik","Koma","Tanya","Seru"], ["Tanda baca yang digunakan untuk mengakhiri kalimat tanya adalah","Tanda tanya","Titik","Koma","Seru"], ["Tanda baca yang digunakan untuk mengakhiri kalimat seru adalah","Tanda seru","Titik","Koma","Tanya"], ["Kegiatan membaca dengan menyuarakan disebut membaca","Nyaring","Dalam hati","Cepat","Sekilas"], ["Kalimat utama dalam sebuah paragraf disebut","Kalimat utama","Kalimat penjelas","Kalimat penutup","Kalimat pembuka"], ["Kalimat yang menjelaskan kalimat utama disebut","Kalimat penjelas","Kalimat utama","Kalimat pembuka","Kalimat penutup"], ["Karya sastra lama berisi nasihat yang disampaikan turun-temurun disebut","Peribahasa","Pantun","Puisi modern","Novel"], ["Sinonim dari kata pintar adalah","Cerdas","Bodoh","Malas","Rajin saja"], ["Antonim dari kata gelap adalah","Terang","Hitam","Suram","Redup"]],
                            'SMP': [["Teks yang menjelaskan proses terjadinya suatu fenomena disebut teks","Eksplanasi","Deskripsi","Narasi","Argumentasi"], ["Teks yang menggambarkan suatu objek secara rinci disebut teks","Deskripsi","Eksplanasi","Narasi","Persuasi"], ["Teks yang menceritakan rangkaian peristiwa disebut teks","Narasi","Deskripsi","Eksposisi","Persuasi"], ["Teks yang berisi ajakan atau bujukan disebut teks","Persuasi","Eksplanasi","Deskripsi","Narasi"], ["Teks yang menyampaikan pendapat disertai argumen disebut teks","Argumentasi","Narasi","Deskripsi","Eksplanasi"], ["Struktur teks eksplanasi diawali dengan","Pernyataan umum","Orientasi","Resolusi","Koda"], ["Bagian akhir teks eksplanasi yang berisi kesimpulan disebut","Interpretasi","Orientasi","Komplikasi","Koda"], ["Kalimat yang menggunakan kata hubung sebab akibat termasuk kalimat","Kompleks","Simpleks","Majemuk setara","Tunggal"], ["Kata yang menunjukkan hubungan waktu seperti kemudian disebut konjungsi","Temporal","Kausalitas","Penambahan","Pertentangan"], ["Kata yang menunjukkan hubungan sebab akibat seperti karena disebut konjungsi","Kausalitas","Temporal","Penambahan","Pertentangan"], ["Puisi yang terikat oleh aturan bait, rima, dan irama disebut","Puisi lama","Puisi bebas","Puisi modern","Puisi kontemporer"], ["Puisi yang tidak terikat aturan disebut","Puisi bebas","Puisi lama","Pantun","Syair"], ["Majas yang membandingkan sesuatu secara langsung dengan kata seperti disebut","Simile","Metafora","Personifikasi","Hiperbola"], ["Majas yang memberikan sifat manusia pada benda mati disebut","Personifikasi","Simile","Metafora","Hiperbola"], ["Majas yang melebih-lebihkan suatu hal disebut","Hiperbola","Simile","Personifikasi","Metafora"], ["Teks yang berisi laporan hasil observasi disebut teks","Laporan hasil observasi","Eksplanasi","Deskripsi","Narasi"], ["Bagian teks berita yang menjawab unsur 5W+1H disebut","Isi berita","Judul berita","Kepala berita","Ekor berita"], ["Unsur intrinsik cerita yang berupa jalan cerita disebut","Alur","Tokoh","Latar","Tema"], ["Unsur intrinsik cerita yang berupa pelaku dalam cerita disebut","Tokoh","Alur","Latar","Amanat"], ["Unsur intrinsik cerita yang berupa tempat, waktu, dan suasana disebut","Latar","Alur","Tokoh","Tema"], ["Pesan moral yang ingin disampaikan pengarang disebut","Amanat","Tema","Alur","Latar"], ["Ide pokok yang mendasari sebuah cerita disebut","Tema","Amanat","Alur","Latar"], ["Surat yang digunakan untuk keperluan resmi kedinasan disebut","Surat dinas","Surat pribadi","Surat niaga","Surat lamaran saja"], ["Teks yang berisi ajakan untuk membeli produk disebut","Iklan","Berita","Laporan","Pidato"], ["Naskah yang dibacakan dalam pidato disebut teks","Pidato","Drama","Puisi","Cerpen"], ["Karya sastra yang dipentaskan dengan dialog para tokoh disebut","Drama","Cerpen","Novel","Puisi"], ["Cerita pendek yang selesai dibaca dalam sekali duduk disebut","Cerpen","Novel","Drama","Puisi"], ["Kalimat yang predikatnya berupa kata kerja aktif disebut kalimat","Aktif","Pasif","Majemuk","Tunggal"], ["Kalimat yang subjeknya dikenai suatu tindakan disebut kalimat","Pasif","Aktif","Majemuk","Tunggal"], ["Kalimat yang menyatakan hubungan pertentangan menggunakan konjungsi","Tetapi","Dan","Karena","Kemudian"]],
                            'SMA': [["Teks yang berisi kritik atau tanggapan terhadap karya disebut teks","Ulasan","Eksplanasi","Editorial","Anekdot"], ["Teks yang berisi opini redaksi media tentang isu aktual disebut teks","Editorial","Ulasan","Anekdot","Eksposisi"], ["Teks yang berisi cerita lucu namun mengandung sindiran disebut teks","Anekdot","Ulasan","Editorial","Eksplanasi"], ["Karya sastra berbentuk cerita panjang dengan alur kompleks disebut","Novel","Cerpen","Puisi","Drama"], ["Naskah akademik yang membahas suatu masalah secara ilmiah disebut","Karya ilmiah","Karya sastra","Teks narasi","Teks iklan"], ["Bagian karya ilmiah yang berisi rumusan masalah disebut","Pendahuluan","Kesimpulan","Daftar pustaka","Abstrak saja"], ["Bagian karya ilmiah yang berisi ringkasan penelitian disebut","Abstrak","Pendahuluan","Kesimpulan","Lampiran"], ["Sumber rujukan dalam karya ilmiah dicantumkan dalam","Daftar pustaka","Kata pengantar","Abstrak","Lampiran"], ["Gaya bahasa yang menggunakan pertentangan makna disebut majas","Ironi","Metafora","Simile","Personifikasi"], ["Gaya bahasa yang membandingkan dua hal secara implisit disebut majas","Metafora","Simile","Ironi","Litotes"], ["Majas yang merendahkan diri untuk merendah hati disebut","Litotes","Hiperbola","Ironi","Metafora"], ["Kritik sastra yang menilai unsur intrinsik dan ekstrinsik disebut","Kritik sastra","Resensi buku","Sinopsis","Ringkasan"], ["Ringkasan cerita yang menggambarkan garis besar isi buku disebut","Sinopsis","Resensi","Kritik sastra","Abstrak"], ["Puisi yang menggambarkan curahan hati penyair disebut puisi","Lirik","Naratif","Deskriptif","Epik"], ["Puisi yang menceritakan suatu kisah atau peristiwa disebut puisi","Naratif","Lirik","Deskriptif","Epik saja"], ["Kalimat yang berisi fakta dapat diperiksa kebenarannya disebut kalimat","Fakta","Opini","Persuasi","Ambigu"], ["Kalimat yang berisi pendapat pribadi disebut kalimat","Opini","Fakta","Deklaratif","Interogatif"], ["Debat memerlukan pihak yang mendukung mosi disebut tim","Afirmasi","Oposisi","Netral","Moderator"], ["Debat memerlukan pihak yang menolak mosi disebut tim","Oposisi","Afirmasi","Netral","Juri"], ["Pihak yang memimpin jalannya debat disebut","Moderator","Notulen","Juri","Peserta"], ["Teks yang menyajikan langkah-langkah melakukan sesuatu disebut teks","Prosedur","Eksplanasi","Deskripsi","Narasi"], ["Karya sastra Melayu klasik berbentuk cerita panjang disebut","Hikayat","Cerpen","Novel","Anekdot"], ["Bentuk puisi lama dua baris berisi sampiran dan isi disebut","Pantun karmina","Syair","Gurindam","Mantra"], ["Puisi lama yang setiap baitnya terdiri dari empat baris berisi nasihat disebut","Syair","Pantun","Gurindam","Mantra"], ["Puisi lama yang terdiri dari dua baris sebait dan berisi nasihat disebut","Gurindam","Syair","Pantun","Mantra"], ["Kalimat yang menggunakan konjungsi meskipun menyatakan hubungan","Konsesif (pertentangan)","Sebab akibat","Tujuan","Penjumlahan"], ["Kalimat yang menggunakan konjungsi agar menyatakan hubungan","Tujuan","Sebab akibat","Konsesif","Penjumlahan"], ["Proposal kegiatan biasanya memuat bagian","Latar belakang, tujuan, dan anggaran","Hanya judul saja","Hanya tanggal saja","Hanya nama panitia"], ["Laporan hasil kegiatan yang bersifat resmi disebut","Laporan kegiatan","Surat pribadi","Iklan","Pantun"], ["Ejaan resmi bahasa Indonesia yang berlaku saat ini disebut","EYD/Ejaan Bahasa Indonesia","Ejaan Van Ophuijsen","Ejaan Soewandi","Ejaan Republik saja"]],
                        },
                        'Informatika': {
                            'SD': [["Alat untuk mengetik pada komputer disebut","Keyboard","Mouse","Monitor","Speaker"], ["Alat untuk menggerakkan kursor pada komputer disebut","Mouse","Keyboard","Monitor","Printer"], ["Layar yang menampilkan gambar pada komputer disebut","Monitor","Keyboard","Mouse","CPU"], ["Bagian komputer yang menjadi otak pemroses disebut","CPU","Monitor","Mouse","Keyboard"], ["Alat untuk mencetak dokumen disebut","Printer","Scanner","Speaker","Monitor"], ["Alat untuk memindai dokumen menjadi file disebut","Scanner","Printer","Speaker","Proyektor"], ["Perangkat keras komputer disebut","Hardware","Software","Brainware","Netware"], ["Program atau aplikasi dalam komputer disebut","Software","Hardware","Brainware","Netware"], ["Orang yang mengoperasikan komputer disebut","Brainware","Hardware","Software","Netware"], ["Tempat menyimpan data secara permanen dalam komputer disebut","Hard disk","RAM","Monitor","Keyboard"], ["Media penyimpanan sementara saat komputer menyala disebut","RAM","Hard disk","ROM","Flashdisk saja"], ["Aplikasi untuk mengetik dokumen adalah","Microsoft Word","Microsoft Excel","Paint","Calculator"], ["Aplikasi untuk mengolah angka adalah","Microsoft Excel","Microsoft Word","Paint","Notepad"], ["Aplikasi untuk membuat presentasi adalah","Microsoft PowerPoint","Microsoft Word","Excel","Paint"], ["Jaringan komputer yang menghubungkan seluruh dunia disebut","Internet","LAN","Intranet","Bluetooth"], ["Alamat website biasanya diawali dengan","www atau http","ftp saja","com saja","net saja"], ["Program untuk menjelajah internet disebut","Browser","Editor","Compiler","Server"], ["Surat elektronik disebut","Email","SMS","Chat","Fax"], ["Tombol untuk menghapus huruf di depan kursor adalah","Delete","Enter","Shift","Tab"], ["Tombol untuk pindah baris baru pada dokumen adalah","Enter","Delete","Shift","Tab"], ["Ikon untuk menyimpan dokumen biasanya berbentuk","Disket","Amplop","Kunci","Bintang"], ["File dengan ekstensi .jpg biasanya berupa","Gambar","Dokumen teks","Video","Musik"], ["File dengan ekstensi .mp3 biasanya berupa","Musik/Audio","Gambar","Dokumen","Video"], ["Perangkat yang menghubungkan komputer ke internet disebut","Modem","Speaker","Printer","Scanner"], ["Sikap yang perlu dijaga saat menggunakan internet adalah","Etika berinternet","Membagikan data pribadi","Membuka semua tautan","Mengabaikan privasi"], ["Tempat penyimpanan data yang bisa dibawa-bawa disebut","Flashdisk","Hard disk saja","RAM","Motherboard"], ["Aplikasi untuk menggambar sederhana pada komputer adalah","Paint","Word","Excel","PowerPoint"], ["Perangkat yang mengeluarkan suara dari komputer disebut","Speaker","Microphone","Monitor","Keyboard"], ["Perangkat yang merekam suara ke komputer disebut","Microphone","Speaker","Monitor","Mouse"], ["Sistem operasi yang umum digunakan pada komputer adalah","Windows","Microsoft Word","Google Chrome","Photoshop"]],
                            'SMP': [["Bahasa yang digunakan untuk membuat halaman web disebut","HTML","Python","Java","C++"], ["Bahasa pemrograman yang populer untuk pemula adalah","Python","HTML","CSS","SQL"], ["Perangkat lunak yang mengatur seluruh sistem komputer disebut","Sistem operasi","Aplikasi","Driver","Antivirus"], ["Program yang melindungi komputer dari virus disebut","Antivirus","Browser","Compiler","Sistem operasi"], ["Satuan terkecil dalam sistem data biner adalah","Bit","Byte","Kilobyte","Megabyte"], ["Delapan bit disebut satu","Byte","Bit","Kilobyte","Megabyte"], ["Proses mengubah data menjadi informasi disebut","Pengolahan data","Penyimpanan data","Input data","Output data"], ["Algoritma adalah","Langkah-langkah penyelesaian masalah secara sistematis","Nama sebuah aplikasi","Jenis perangkat keras","Bahasa pemrograman saja"], ["Diagram alur yang menggambarkan algoritma disebut","Flowchart","Mind map","Diagram Venn","Tabel"], ["Simbol flowchart berbentuk oval biasanya menyatakan","Mulai/Selesai","Proses","Keputusan","Input/Output"], ["Simbol flowchart berbentuk belah ketupat menyatakan","Keputusan","Proses","Mulai/Selesai","Input/Output"], ["Jaringan komputer dalam area terbatas seperti sekolah disebut","LAN","WAN","Internet","Bluetooth"], ["Jaringan komputer yang mencakup area luas antarkota/negara disebut","WAN","LAN","PAN","Bluetooth"], ["Proses menyalin data dari internet ke komputer disebut","Download","Upload","Sinkronisasi","Backup"], ["Proses mengirim data dari komputer ke internet disebut","Upload","Download","Sinkronisasi","Restore"], ["Alamat unik setiap perangkat dalam jaringan disebut","IP Address","URL","Domain","Email"], ["Nama unik sebuah website disebut","Domain","IP Address","Port","Protokol"], ["Protokol keamanan pada website ditandai dengan","HTTPS","HTTP saja","FTP","SMTP"], ["Perangkat lunak yang mengubah kode program menjadi bahasa mesin disebut","Compiler","Browser","Editor","Debugger saja"], ["Kesalahan dalam program yang perlu diperbaiki disebut","Bug/Error","Fitur","Update","Patch saja"], ["Proses mencari dan memperbaiki kesalahan program disebut","Debugging","Compiling","Coding saja","Uploading"], ["Media penyimpanan berbasis awan disebut","Cloud storage","Hard disk","Flashdisk","RAM"], ["Berbagi data secara ilegal atau melanggar privasi merupakan pelanggaran","Etika digital","Fitur aplikasi","Kebijakan wajar","Standar internet"], ["Data yang diolah menjadi bentuk yang bermakna disebut","Informasi","Data mentah","Variabel","Fungsi saja"], ["Variabel dalam pemrograman digunakan untuk","Menyimpan nilai data","Menghapus program","Mencetak dokumen","Memutar musik"], ["Struktur perulangan dalam pemrograman disebut","Looping","Percabangan","Sequencing","Debugging"], ["Struktur percabangan dalam pemrograman disebut","Percabangan (if-else)","Looping","Sequencing","Array saja"], ["Kumpulan data sejenis yang disimpan berurutan disebut","Array","Variabel tunggal","Fungsi","Kelas saja"], ["Perangkat lunak untuk membuat dan mengedit gambar vektor adalah","CorelDraw/Illustrator","Word","Excel","Notepad"], ["Media sosial perlu digunakan secara bijak untuk menghindari","Cyberbullying","Produktivitas","Kreativitas","Edukasi saja"]],
                            'SMA': [["Bahasa pemrograman berorientasi objek yang populer adalah","Java","HTML","CSS","Markdown"], ["Struktur data yang bekerja dengan prinsip LIFO disebut","Stack","Queue","Array","Tree"], ["Struktur data yang bekerja dengan prinsip FIFO disebut","Queue","Stack","Array","Graph"], ["Algoritma pengurutan data yang membandingkan elemen bersebelahan disebut","Bubble sort","Binary search","Linear search","Quick select saja"], ["Metode pencarian data pada data terurut secara efisien disebut","Binary search","Bubble sort","Insertion sort","Selection sort"], ["Basis data yang menggunakan struktur tabel disebut","Basis data relasional","Basis data grafik","Basis data dokumen","Basis data kunci-nilai"], ["Bahasa untuk mengakses dan mengolah basis data disebut","SQL","HTML","Python saja","CSS"], ["Konsep menyimpan dan mengelola data melalui internet disebut","Cloud computing","Local computing","Edge computing saja","Quantum computing"], ["Teknologi yang memungkinkan mesin belajar dari data disebut","Machine learning","Basis data","Jaringan komputer","Sistem operasi"], ["Kecerdasan buatan dalam bahasa Inggris disingkat","AI (Artificial Intelligence)","IT","IoT","VR"], ["Jaringan perangkat yang saling terhubung dan bertukar data disebut Internet of","Things (IoT)","People","Data saja","Machines saja"], ["Teknologi yang menciptakan lingkungan simulasi tiga dimensi disebut","Virtual Reality","Augmented Reality","Cloud computing","Big Data"], ["Teknologi yang menggabungkan dunia nyata dan digital disebut","Augmented Reality","Virtual Reality","Cloud computing","Big Data"], ["Kumpulan data yang sangat besar dan kompleks disebut","Big Data","Small Data","Metadata saja","Database kecil"], ["Proses melindungi sistem dari serangan siber disebut","Keamanan siber (Cybersecurity)","Pemrograman","Basis data","Jaringan LAN"], ["Serangan yang mengunci data dan meminta tebusan disebut","Ransomware","Firewall","Antivirus","Cookie"], ["Program yang menyaring lalu lintas jaringan untuk keamanan disebut","Firewall","Ransomware","Malware","Spyware"], ["Perangkat lunak berbahaya secara umum disebut","Malware","Firmware","Freeware","Shareware"], ["Enkripsi data bertujuan untuk","Mengamankan kerahasiaan data","Mempercepat data","Memperbesar data","Menghapus data"], ["Model pengembangan perangkat lunak bertahap disebut model","Waterfall","Agile saja","Scrum saja","Kanban saja"], ["Metode pengembangan perangkat lunak yang fleksibel dan iteratif disebut","Agile","Waterfall","Spiral saja","V-Model saja"], ["Notasi untuk merancang alur logika program sebelum coding disebut","Pseudocode","Bytecode","Machine code","Source code saja"], ["Kode program yang belum dikompilasi disebut","Source code","Object code","Machine code","Bytecode saja"], ["Representasi bilangan yang digunakan komputer secara internal adalah","Biner","Desimal","Romawi","Oktal saja"], ["Satu kilobyte setara dengan","1024 byte","1000 byte","100 byte","10 byte"], ["Protokol yang digunakan untuk mengirim email disebut","SMTP","HTTP","FTP","DNS"], ["Sistem yang menerjemahkan nama domain menjadi alamat IP disebut","DNS","HTTP","FTP","SMTP"], ["Konsep berbagi sumber daya komputasi melalui internet disebut","Cloud computing","Edge computing saja","Fog computing saja","Grid computing saja"], ["Etika dalam pemanfaatan teknologi informasi disebut","Etika digital","Netiket saja","Hukum siber saja","Kebijakan privasi saja"], ["Hak cipta karya digital dilindungi oleh","Undang-undang Hak Cipta","Kebijakan aplikasi saja","Standar internet saja","Etika pengguna saja"]],
                        },
                        'Penjas': {
                            'SD': [["Olahraga yang menggunakan bola dan dimainkan dengan kaki disebut","Sepak bola","Bola voli","Bulu tangkis","Renang"], ["Olahraga yang dimainkan dengan raket dan kok disebut","Bulu tangkis","Sepak bola","Bola basket","Tenis meja"], ["Gerakan pemanasan sebelum berolahraga disebut","Pemanasan","Pendinginan","Peregangan statis saja","Relaksasi"], ["Gerakan pendinginan setelah berolahraga bertujuan untuk","Mengembalikan detak jantung normal","Meningkatkan detak jantung","Menambah cedera","Mempercepat lelah"], ["Cabang olahraga renang gaya bebas disebut juga","Freestyle/Crawl","Gaya dada","Gaya punggung","Gaya kupu-kupu"], ["Gaya renang yang posisi tubuhnya menghadap ke atas disebut","Gaya punggung","Gaya bebas","Gaya dada","Gaya kupu-kupu"], ["Jumlah pemain dalam satu tim sepak bola adalah","11 orang","5 orang","6 orang","7 orang"], ["Jumlah pemain dalam satu tim bola voli adalah","6 orang","11 orang","5 orang","7 orang"], ["Jumlah pemain dalam satu tim bola basket adalah","5 orang","11 orang","6 orang","7 orang"], ["Alat yang digunakan untuk memukul bola dalam permainan kasti adalah","Tongkat pemukul","Raket","Stik","Tangan"], ["Lari jarak pendek disebut lari","Sprint","Marathon","Estafet","Gawang"], ["Lari yang dilakukan secara beregu dengan tongkat estafet disebut lari","Estafet","Sprint","Marathon","Gawang"], ["Gerakan melompat dengan satu kaki disebut","Engklek/lompat satu kaki","Lompat jauh","Lompat tinggi","Lompat galah"], ["Cabang atletik yang mengukur jarak lompatan disebut","Lompat jauh","Lompat tinggi","Lompat galah","Lari gawang"], ["Cabang atletik yang mengukur ketinggian lompatan disebut","Lompat tinggi","Lompat jauh","Lari gawang","Tolak peluru"], ["Latihan untuk melatih kekuatan otot lengan adalah","Push up","Sit up","Lari","Renang saja"], ["Latihan untuk melatih kekuatan otot perut adalah","Sit up","Push up","Lompat tali","Jalan cepat"], ["Makanan bergizi seimbang penting untuk menjaga","Kesehatan tubuh","Kelelahan","Kebugaran semu","Berat badan naik saja"], ["Istirahat yang cukup setiap hari bertujuan untuk","Menjaga kesehatan tubuh","Menambah kelelahan","Mengurangi kebugaran","Menurunkan imun"], ["Olahraga yang dilakukan di air disebut","Renang","Sepak bola","Bulu tangkis","Senam"], ["Permainan tradisional yang menggunakan tali panjang untuk dilompati disebut","Lompat tali","Engklek","Gobak sodor","Congklak"], ["Permainan tradisional yang dimainkan dengan cara berlari menghindari lawan disebut","Gobak sodor","Congklak","Lompat tali","Engklek"], ["Sikap tubuh yang benar saat berdiri disebut sikap","Tegak","Membungkuk","Miring","Jongkok"], ["Gerakan meregangkan otot sebelum olahraga disebut","Stretching","Sprint","Cooling down","Warming up saja"], ["Cabang olahraga bela diri asli Indonesia adalah","Pencak silat","Karate","Taekwondo","Judo"], ["Cabang olahraga bela diri dari Jepang yang menggunakan pukulan dan tendangan adalah","Karate","Pencak silat","Taekwondo","Judo"], ["Permainan bulu tangkis dimainkan di lapangan berbentuk","Persegi panjang","Lingkaran","Segitiga","Oval"], ["Alat pelindung kepala saat bersepeda disebut","Helm","Sarung tangan","Pelindung lutut","Kacamata"], ["Kebugaran jasmani dapat dijaga dengan cara","Berolahraga teratur","Begadang setiap hari","Makan berlebihan","Malas bergerak"], ["Detak jantung yang meningkat saat berolahraga menandakan tubuh sedang","Bekerja lebih keras","Beristirahat","Sakit","Lemas"]],
                            'SMP': [["Teknik dasar mengumpan bola dalam sepak bola menggunakan kaki bagian dalam disebut","Passing","Dribbling","Shooting","Heading"], ["Teknik menggiring bola dalam sepak bola disebut","Dribbling","Passing","Shooting","Heading"], ["Teknik menyundul bola dalam sepak bola disebut","Heading","Passing","Dribbling","Shooting"], ["Teknik menembak bola ke gawang disebut","Shooting","Passing","Dribbling","Heading"], ["Servis dalam bola voli dilakukan untuk","Memulai permainan","Mengakhiri permainan","Bertahan","Mengganti pemain"], ["Teknik memantulkan bola dengan kedua lengan dalam bola voli disebut","Passing bawah","Smash","Blocking","Servis"], ["Teknik menahan serangan lawan di dekat net dalam bola voli disebut","Blocking","Passing","Smash","Servis"], ["Teknik pukulan keras dalam bola voli disebut","Smash","Passing","Blocking","Servis"], ["Teknik menggiring bola dalam bola basket disebut","Dribbling","Shooting","Passing","Rebound"], ["Teknik memasukkan bola ke ring disebut","Shooting","Dribbling","Passing","Rebound"], ["Teknik merebut bola pantul dalam bola basket disebut","Rebound","Shooting","Dribbling","Passing"], ["Lari jarak menengah biasanya menempuh jarak","800-1500 meter","100 meter","5000 meter","42 km"], ["Lari jarak jauh biasanya menempuh jarak di atas","3000 meter","100 meter","400 meter","800 meter saja"], ["Nomor lari yang melewati rintangan disebut lari","Gawang","Estafet","Sprint","Maraton"], ["Tolak peluru termasuk cabang olahraga","Atletik","Renang","Senam","Bela diri"], ["Lempar lembing termasuk cabang olahraga","Atletik","Renang","Senam","Bola besar"], ["Senam yang menggunakan alat seperti pita dan bola disebut senam","Ritmik","Lantai","Aerobik","Artistik"], ["Senam yang dilakukan tanpa alat di atas matras disebut senam","Lantai","Ritmik","Aerobik","Artistik"], ["Gerakan berguling ke depan dalam senam lantai disebut","Roll depan","Roll belakang","Kayang","Sikap lilin"], ["Gerakan melengkungkan badan ke belakang dalam senam lantai disebut","Kayang","Roll depan","Roll belakang","Sikap lilin"], ["Denyut nadi maksimal dapat dihitung dengan rumus","220 dikurangi usia","220 ditambah usia","Usia dikali 2","Usia dibagi 2"], ["Latihan kebugaran yang meningkatkan daya tahan jantung dan paru disebut latihan","Kardiorespirasi","Kekuatan otot","Kelenturan","Keseimbangan"], ["Latihan yang meningkatkan kelenturan tubuh disebut latihan","Fleksibilitas","Kekuatan","Kecepatan","Daya tahan"], ["Pola makan sehat sebelum berolahraga sebaiknya dilakukan","2-3 jam sebelumnya","Tepat saat olahraga","Setelah olahraga saja","Tidak perlu makan"], ["Cedera otot akibat peregangan berlebihan disebut","Keseleo/terkilir","Patah tulang","Memar saja","Kram otot"], ["Kram otot biasanya disebabkan oleh","Kelelahan dan kurang cairan","Terlalu banyak istirahat","Kelebihan gizi","Suhu dingin saja"], ["Renang gaya dada disebut juga gaya","Katak","Bebas","Punggung","Kupu-kupu"], ["Renang gaya kupu-kupu memerlukan gerakan kedua lengan secara","Bersamaan","Bergantian","Diam","Mengapung saja"], ["Bela diri pencak silat berasal dari negara","Indonesia","Jepang","Korea","Tiongkok"], ["Judo adalah olahraga bela diri yang berasal dari negara","Jepang","Indonesia","Korea","Tiongkok"]],
                            'SMA': [["Sistem energi yang digunakan tubuh pada aktivitas fisik intensitas tinggi durasi pendek adalah sistem","Anaerobik","Aerobik","Campuran saja","Oksidatif saja"], ["Sistem energi yang digunakan tubuh pada aktivitas fisik durasi panjang intensitas rendah adalah sistem","Aerobik","Anaerobik","Campuran saja","Fosfagen saja"], ["VO2 max digunakan untuk mengukur","Kapasitas aerobik maksimal tubuh","Kekuatan otot","Kelenturan sendi","Kecepatan reaksi"], ["Prinsip latihan yang menyatakan beban latihan harus meningkat bertahap disebut prinsip","Overload","FITT saja","Spesifikasi","Reversibilitas"], ["Prinsip FITT dalam latihan terdiri dari Frequency, Intensity, Time, dan","Type","Target","Training saja","Technique"], ["Cedera olahraga akibat robeknya ligamen disebut","Sprain","Strain","Fraktur","Memar"], ["Cedera olahraga akibat robeknya otot atau tendon disebut","Strain","Sprain","Fraktur","Memar"], ["Penanganan cedera akut dengan metode RICE meliputi Rest, Ice, Compression, dan","Elevation","Exercise","Endurance","Extension"], ["Sistem pertandingan yang mempertemukan semua tim disebut sistem","Setengah kompetisi","Gugur","Kombinasi saja","Poin saja"], ["Sistem pertandingan yang mengeliminasi tim yang kalah disebut sistem","Gugur","Setengah kompetisi","Round robin saja","Poin saja"], ["Wasit dalam pertandingan sepak bola dibantu oleh","Asisten wasit/hakim garis","Pelatih","Manajer tim","Suporter"], ["Peraturan offside berlaku dalam cabang olahraga","Sepak bola","Bola voli","Bola basket","Bulu tangkis"], ["Zona pertahanan dalam bola basket yang menjaga area tertentu disebut pertahanan","Zone defense","Man to man","Full court press saja","Fast break saja"], ["Pertahanan yang menjaga satu lawan satu pemain disebut pertahanan","Man to man","Zone defense","Full court press saja","Fast break saja"], ["Doping dalam olahraga adalah tindakan","Menggunakan zat terlarang untuk meningkatkan performa","Latihan tambahan","Pemanasan ekstra","Konsumsi air putih"], ["Organisasi anti-doping dunia disingkat","WADA","FIFA","IOC","WHO"], ["Induk organisasi sepak bola dunia adalah","FIFA","IOC","WADA","AFC saja"], ["Induk organisasi olimpiade dunia adalah","IOC","FIFA","WADA","AFC saja"], ["Denyut nadi latihan (target heart rate) dihitung berdasarkan persentase dari","Denyut nadi maksimal","Tekanan darah","Berat badan","Tinggi badan"], ["Kebugaran jasmani yang berkaitan dengan kesehatan meliputi daya tahan jantung paru dan","Komposisi tubuh","Kecepatan reaksi saja","Koordinasi saja","Keseimbangan saja"], ["Latihan interval menggabungkan periode latihan intensitas tinggi dengan","Periode pemulihan","Latihan intensitas tinggi terus menerus","Istirahat total","Peregangan statis saja"], ["Zat gizi utama sebagai sumber energi utama tubuh saat berolahraga adalah","Karbohidrat","Vitamin","Mineral","Serat"], ["Kebutuhan cairan tubuh saat berolahraga sebaiknya dipenuhi dengan","Air putih secara teratur","Menahan minum","Minuman bersoda","Kopi saja"], ["Pola hidup sehat mencakup keseimbangan antara aktivitas fisik, gizi, dan","Istirahat cukup","Begadang","Konsumsi gula berlebih","Rokok"], ["Senam aerobik bertujuan utama untuk melatih","Daya tahan kardiorespirasi","Kekuatan maksimal","Kelenturan saja","Keseimbangan saja"], ["Olahraga renang termasuk latihan yang baik untuk sistem","Kardiorespirasi dan otot tubuh","Hanya otot lengan","Hanya otot kaki","Hanya pernapasan"], ["Peraturan pertandingan bulu tangkis modern menggunakan sistem poin hingga","21 poin per game","11 poin per game","15 poin per game","25 poin per game"], ["Peraturan pertandingan bola voli modern menggunakan sistem poin hingga","25 poin per set","21 poin per set","15 poin per set","11 poin per set"], ["Aktivitas fisik teratur terbukti dapat menurunkan risiko","Penyakit jantung dan diabetes","Kecerdasan","Daya ingat","Produktivitas"], ["Manajemen waktu latihan yang baik mencakup pemanasan, latihan inti, dan","Pendinginan","Istirahat total","Tidur","Bermain gawai"]],
                        },
                        'Seni Budaya': {
                            'SD': [["Alat musik tradisional yang dipukul dan berasal dari Jawa disebut","Gamelan","Angklung","Sasando","Kolintang"], ["Alat musik tradisional yang terbuat dari bambu dan digoyangkan berasal dari Jawa Barat disebut","Angklung","Gamelan","Sasando","Kolintang"], ["Alat musik tradisional dari Nusa Tenggara Timur yang berbentuk seperti harpa disebut","Sasando","Angklung","Gamelan","Kolintang"], ["Alat musik tradisional dari Sulawesi Utara yang dipukul disebut","Kolintang","Sasando","Angklung","Gamelan"], ["Warna yang dihasilkan dari campuran merah dan kuning adalah","Oranye","Hijau","Ungu","Cokelat"], ["Warna yang dihasilkan dari campuran biru dan kuning adalah","Hijau","Oranye","Ungu","Cokelat"], ["Warna yang dihasilkan dari campuran merah dan biru adalah","Ungu","Hijau","Oranye","Cokelat"], ["Warna dasar yang tidak bisa dibuat dari campuran warna lain disebut warna","Primer","Sekunder","Tersier","Netral"], ["Gambar yang dibuat dengan menempel potongan kertas atau bahan lain disebut","Kolase","Mozaik","Montase","Lukisan"], ["Karya seni yang dibuat dari potongan bahan kecil yang disusun disebut","Mozaik","Kolase","Montase","Lukisan"], ["Tari tradisional yang menggambarkan sosok topeng biasanya disebut tari","Topeng","Kecak","Saman","Piring"], ["Tari yang dilakukan serentak sambil bertepuk tangan berasal dari Aceh disebut tari","Saman","Kecak","Piring","Topeng"], ["Alat musik yang dimainkan dengan cara ditiup adalah","Seruling","Gitar","Piano","Drum"], ["Alat musik yang dimainkan dengan cara dipetik adalah","Gitar","Seruling","Drum","Gong"], ["Alat musik yang dimainkan dengan cara dipukul adalah","Drum","Gitar","Seruling","Biola"], ["Lagu daerah Ampar-Ampar Pisang berasal dari daerah","Kalimantan Selatan","Jawa Tengah","Sumatra Barat","Maluku"], ["Lagu daerah Cublak-Cublak Suweng berasal dari daerah","Jawa Tengah","Kalimantan","Sumatra","Papua"], ["Kerajinan tangan yang dibuat dengan cara melipat kertas disebut","Origami","Mozaik","Kolase","Montase"], ["Teknik menggambar dengan mengarsir menggunakan pensil untuk memberi kesan gelap terang disebut teknik","Arsir","Blok","Dussel saja","Aquarel"], ["Warna yang memberikan kesan hangat contohnya adalah","Merah dan Kuning","Biru dan Hijau","Ungu dan Abu-abu","Hitam dan Putih"], ["Warna yang memberikan kesan dingin contohnya adalah","Biru dan Hijau","Merah dan Kuning","Oranye dan Merah muda","Cokelat dan Krem"], ["Membuat karya seni dengan menggabungkan berbagai gambar atau foto disebut","Montase","Kolase","Mozaik","Origami"], ["Nada dasar dalam notasi angka yang dilambangkan dengan angka 1 dibaca","Do","Re","Mi","Sol"], ["Tangga nada dalam musik terdiri dari tujuh nada yaitu do re mi fa sol la","Si","Ti saja","Ni saja","Ma saja"], ["Alat musik ritmis adalah alat musik yang tidak memiliki","Nada tertentu","Suara","Bentuk","Fungsi"], ["Alat musik melodis adalah alat musik yang memiliki","Nada tertentu","Bentuk saja","Warna saja","Berat tertentu"], ["Karya seni rupa tiga dimensi yang dapat dilihat dari segala arah disebut","Patung","Lukisan","Sketsa","Poster"], ["Karya seni rupa dua dimensi yang hanya dapat dilihat dari satu arah disebut","Lukisan","Patung","Diorama","Instalasi"], ["Batik merupakan salah satu contoh karya seni rupa","Terapan","Murni saja","Tiga dimensi saja","Instalasi"], ["Kerajinan anyaman biasanya menggunakan bahan seperti","Bambu dan rotan","Besi dan baja","Kaca dan plastik","Logam saja"]],
                            'SMP': [["Unsur seni rupa yang berupa titik-titik yang memanjang disebut","Garis","Bidang","Bentuk","Tekstur"], ["Unsur seni rupa yang memiliki panjang dan lebar disebut","Bidang","Garis","Bentuk","Ruang"], ["Unsur seni rupa yang memiliki panjang, lebar, dan tinggi disebut","Bentuk","Bidang","Garis","Warna"], ["Kesan permukaan suatu benda dalam karya seni rupa disebut","Tekstur","Warna","Ruang","Gelap terang"], ["Teknik melukis dengan cat air yang tipis dan transparan disebut teknik","Aquarel","Plakat","Dussel","Pointilis"], ["Teknik melukis dengan cat yang tebal dan pekat disebut teknik","Plakat","Aquarel","Dussel","Pointilis"], ["Teknik melukis dengan titik-titik kecil disebut teknik","Pointilis","Plakat","Aquarel","Dussel"], ["Ragam hias yang mengambil bentuk tumbuhan disebut ragam hias","Flora","Fauna","Geometris","Figuratif"], ["Ragam hias yang mengambil bentuk hewan disebut ragam hias","Fauna","Flora","Geometris","Figuratif"], ["Ragam hias yang berbentuk bidang geometri disebut ragam hias","Geometris","Flora","Fauna","Figuratif"], ["Musik yang berasal dari daerah tertentu dan diwariskan turun-temurun disebut musik","Tradisional","Modern","Kontemporer","Populer"], ["Alat musik yang mengiringi tari Jaipong berasal dari daerah","Jawa Barat","Jawa Tengah","Bali","Sumatra"], ["Tari kreasi baru adalah tari yang","Dikembangkan dari tari tradisi dengan sentuhan baru","Sama persis dengan tari tradisi","Berasal dari luar negeri saja","Tidak memiliki gerak"], ["Unsur utama dalam tari meliputi wiraga, wirama, dan","Wirasa","Wicara saja","Wibawa saja","Wisata saja"], ["Wiraga dalam seni tari berarti unsur","Gerak tubuh","Irama musik","Ekspresi rasa","Kostum"], ["Wirama dalam seni tari berarti unsur","Irama/musik pengiring","Gerak tubuh","Ekspresi rasa","Properti"], ["Wirasa dalam seni tari berarti unsur","Ekspresi/penjiwaan","Gerak tubuh","Irama musik","Kostum"], ["Musik ansambel adalah musik yang dimainkan secara","Berkelompok dengan beberapa alat musik","Sendiri saja","Tanpa alat musik","Hanya vokal saja"], ["Notasi musik yang menggunakan simbol angka disebut notasi","Angka","Balok","Huruf saja","Grafik saja"], ["Notasi musik yang menggunakan simbol pada garis paranada disebut notasi","Balok","Angka","Huruf saja","Grafik saja"], ["Teater tradisional Indonesia yang menggunakan boneka kulit disebut","Wayang kulit","Ludruk","Ketoprak","Lenong"], ["Teater tradisional dari Jawa Timur yang menampilkan lawakan disebut","Ludruk","Wayang kulit","Ketoprak","Lenong"], ["Seni kriya yang dibuat dengan teknik ukir umumnya menggunakan bahan","Kayu","Kain","Kertas","Plastik"], ["Seni kriya batik menggunakan alat khusus untuk melukis malam bernama","Canting","Kuas","Pahat","Cetakan"], ["Proses pewarnaan kain batik menggunakan lilin panas disebut teknik","Rintang warna","Celup ikat saja","Sablon saja","Cap saja"], ["Pameran karya seni rupa bertujuan untuk","Mengapresiasi dan mengomunikasikan karya","Menyembunyikan karya","Menjual bahan baku saja","Menghindari kritik"], ["Kritik seni yang bertujuan membangun disebut kritik","Konstruktif","Destruktif","Populer saja","Akademis saja"], ["Desain grafis termasuk dalam cabang seni rupa","Terapan","Murni","Pertunjukan","Musik"], ["Seni rupa murni dibuat dengan tujuan utama","Ekspresi keindahan","Fungsi praktis","Komersial semata","Dekorasi ruangan saja"], ["Seni rupa terapan dibuat dengan mempertimbangkan","Fungsi dan keindahan","Ekspresi semata","Filosofi saja","Kritik sosial saja"]],
                            'SMA': [["Aliran seni lukis yang menggambarkan objek sesuai kenyataan disebut aliran","Realisme","Impresionisme","Kubisme","Ekspresionisme"], ["Aliran seni lukis yang menggambarkan objek berdasarkan kesan sekilas disebut aliran","Impresionisme","Realisme","Kubisme","Naturalisme"], ["Aliran seni lukis yang menggambarkan objek dalam bentuk geometris disebut aliran","Kubisme","Realisme","Impresionisme","Surealisme"], ["Aliran seni lukis yang mengekspresikan emosi jiwa secara bebas disebut aliran","Ekspresionisme","Realisme","Naturalisme","Kubisme"], ["Aliran seni lukis yang menggambarkan alam mimpi dan alam bawah sadar disebut aliran","Surealisme","Realisme","Impresionisme","Kubisme"], ["Pelukis Indonesia yang terkenal dengan gaya realisme dan naturalisme adalah","Raden Saleh","Affandi","Basuki Abdullah saja","S. Sudjojono saja"], ["Pelukis Indonesia yang dikenal dengan gaya ekspresionis dan lukisan potret diri adalah","Affandi","Raden Saleh","Basuki Abdullah","S. Sudjojono"], ["Seni instalasi adalah karya seni yang","Menata objek dalam suatu ruang tertentu","Hanya berupa lukisan datar","Hanya berupa patung tunggal","Hanya musik"], ["Seni pertunjukan yang menggabungkan musik, tari, dan drama disebut","Seni teater/drama musikal","Seni rupa murni","Seni kriya","Desain produk"], ["Musik kontemporer adalah musik yang","Menggabungkan unsur tradisional dan modern secara eksperimental","Hanya musik klasik","Hanya musik tradisional murni","Tidak menggunakan alat musik"], ["Kritik seni akademis biasanya disampaikan oleh","Kritikus atau ahli seni","Penonton awam saja","Seniman itu sendiri saja","Media sosial saja"], ["Apresiasi seni adalah kegiatan","Menghargai dan menilai sebuah karya seni","Membuat karya seni","Menjual karya seni","Menghancurkan karya seni"], ["Tahapan apresiasi seni meliputi pengamatan, penghayatan, dan","Penilaian","Penjualan","Peniruan","Pengabaian"], ["Desain komunikasi visual berkaitan erat dengan bidang","Periklanan dan media","Pertanian","Kedokteran","Pertambangan"], ["Karya seni rupa kontemporer sering menggabungkan berbagai","Media dan teknik","Hanya cat minyak","Hanya pensil","Hanya tanah liat"], ["Musik tradisional yang dipentaskan dalam upacara adat memiliki fungsi","Ritual dan sosial budaya","Hiburan semata","Komersial semata","Pendidikan formal saja"], ["Tari yang berkembang dari istana kerajaan disebut tari","Klasik","Kreasi baru","Rakyat saja","Kontemporer saja"], ["Tari yang berkembang dan hidup di kalangan masyarakat umum disebut tari","Rakyat","Klasik","Istana saja","Kreasi baru saja"], ["Koreografi dalam seni tari berkaitan dengan","Penyusunan gerak tari","Pembuatan kostum","Pembuatan musik saja","Tata panggung saja"], ["Tata rias dan busana dalam pertunjukan seni berfungsi untuk","Mendukung karakter dan estetika pertunjukan","Menutupi kekurangan panggung","Menggantikan naskah","Mengurangi ekspresi"], ["Musik ansambel campuran menggabungkan alat musik","Melodis dan ritmis","Ritmis saja","Melodis saja","Harmonis saja"], ["Karya seni yang dibuat untuk tujuan komersial dan fungsi tertentu disebut seni","Terapan","Murni","Kontemporer saja","Instalasi saja"], ["Estetika dalam seni berkaitan dengan kajian tentang","Keindahan","Fungsi ekonomi","Bahan baku saja","Teknologi produksi"], ["Simbol dalam karya seni rupa berfungsi untuk","Menyampaikan makna tertentu","Menghias saja","Menutupi kekurangan teknik","Meningkatkan harga jual"], ["Proses kreasi seni umumnya diawali dengan tahap","Eksplorasi ide","Pameran","Penjualan","Kritik"], ["Pameran seni rupa tunggal menampilkan karya dari","Satu seniman","Banyak seniman berbeda aliran","Seniman internasional saja","Seniman anonim saja"], ["Pameran seni rupa kelompok menampilkan karya dari","Beberapa seniman","Satu seniman saja","Kurator saja","Kolektor saja"], ["Kurator dalam sebuah pameran seni bertugas","Mengelola dan mengonsep pameran","Membeli karya seni","Membuat karya seni","Menjual tiket"], ["Industri kreatif di bidang seni turut mendukung","Pertumbuhan ekonomi kreatif","Penurunan budaya lokal","Penghapusan tradisi","Isolasi budaya"], ["Pelestarian seni budaya tradisional penting dilakukan untuk menjaga","Identitas dan warisan budaya bangsa","Kepentingan komersial semata","Persaingan global saja","Modernisasi total"]],
                        },
                        "Prakarya": {
                            "SD": [["Kegiatan mendaur ulang barang bekas menjadi barang baru disebut", "Daur ulang", "Pembakaran sampah", "Penimbunan sampah", "Pembuangan sampah"], ["Kerajinan yang menggunakan bahan alam seperti daun kering dan biji-bijian disebut kerajinan bahan", "Alam", "Buatan", "Sintetis", "Logam"], ["Kerajinan yang menggunakan bahan plastik dan kain perca disebut kerajinan bahan", "Buatan", "Alam", "Organik", "Mentah"], ["Kegiatan menanam dan merawat tanaman hingga panen disebut", "Budidaya tanaman", "Pengolahan pangan", "Kerajinan tangan", "Rekayasa sederhana"], ["Kegiatan memelihara ikan hias di akuarium disebut budidaya", "Ikan hias", "Unggas", "Tanaman pangan", "Ternak besar"], ["Alat yang digunakan untuk memotong kertas dengan rapi adalah", "Gunting", "Penggaris", "Stapler", "Selotip"], ["Bahan yang digunakan untuk merekatkan dua bagian kerajinan adalah", "Lem", "Cutter", "Jarum", "Gunting"], ["Kerajinan yang dibuat dengan cara menganyam bilah bambu disebut", "Anyaman", "Ukiran", "Tenun", "Batik"], ["Proses mengubah bahan makanan mentah menjadi makanan siap santap disebut", "Pengolahan pangan", "Budidaya pangan", "Kerajinan pangan", "Distribusi pangan"], ["Sampah sisa sayuran dan buah termasuk jenis sampah", "Organik", "Anorganik", "Elektronik", "Berbahaya"], ["Sampah botol plastik dan kaleng termasuk jenis sampah", "Anorganik", "Organik", "Basah", "Beracun"], ["Tanah liat dapat diolah menjadi kerajinan berupa", "Gerabah", "Anyaman", "Batik", "Origami"], ["Kerajinan yang dibuat dengan melipat kertas hingga membentuk suatu benda disebut", "Origami", "Mozaik", "Kolase", "Anyaman"], ["Alat sederhana untuk menyiram tanaman adalah", "Gembor", "Sabit", "Cangkul", "Sekop"], ["Alat yang digunakan untuk menggemburkan tanah sebelum menanam adalah", "Cangkul", "Gembor", "Gunting", "Palu"], ["Bahan pangan yang berasal dari hewan misalnya", "Telur", "Bayam", "Wortel", "Kentang"], ["Bahan pangan yang berasal dari tumbuhan misalnya", "Bayam", "Telur", "Daging ayam", "Susu"], ["Kemasan makanan berfungsi untuk", "Melindungi dan menjaga kualitas makanan", "Mempercantik saja", "Menambah berat produk", "Menyulitkan penjualan"], ["Kerajinan meronce biasanya menggunakan bahan berupa", "Manik-manik", "Bambu", "Tanah liat", "Kain perca"], ["Membuat karya dari potongan kertas warna-warni yang ditempel disebut", "Kolase", "Origami", "Ukiran", "Batik"], ["Tanaman yang biasa dibudidayakan dalam pot di rumah disebut tanaman", "Hias", "Liar", "Pangan pokok", "Industri"], ["Ikan yang biasa dibudidayakan untuk dikonsumsi contohnya", "Ikan lele", "Ikan cupang", "Ikan koi", "Ikan hias"], ["Alat untuk mengukur panjang bahan kerajinan adalah", "Penggaris", "Gunting", "Lem", "Jarum"], ["Produk kerajinan dari kain perca yang dijahit disebut", "Kerajinan jahit perca", "Anyaman", "Ukiran", "Gerabah"], ["Kegiatan memelihara ayam untuk diambil telur dan dagingnya disebut budidaya", "Unggas", "Ikan", "Tanaman hias", "Tanaman pangan"], ["Bahan bekas yang aman didaur ulang menjadi tempat pensil misalnya", "Botol plastik", "Sisa makanan", "Baterai bekas", "Kaca pecah"], ["Karya kerajinan tiga dimensi dari tanah liat yang dibakar disebut", "Gerabah", "Batik", "Anyaman", "Kolase"], ["Sebelum membuat kerajinan, langkah pertama yang dilakukan adalah", "Merancang atau membuat sketsa", "Langsung memasarkan", "Membuang bahan", "Mencuci tangan saja"], ["Kegiatan menjual hasil karya prakarya kepada orang lain disebut", "Pemasaran", "Produksi", "Perencanaan", "Daur ulang"], ["Contoh kerajinan dari bahan alam berupa kerang adalah", "Hiasan dari kerang", "Anyaman bambu", "Batik tulis", "Origami kertas"]],
                            "SMP": [["Prakarya memiliki empat aspek utama yaitu kerajinan, rekayasa, budidaya, dan", "Pengolahan", "Pemasaran", "Distribusi", "Konsumsi"], ["Kerajinan yang memanfaatkan limbah organik menjadi karya bernilai disebut kerajinan", "Limbah organik", "Limbah anorganik", "Tekstil", "Logam"], ["Kerajinan yang memanfaatkan limbah anorganik seperti plastik dan kaleng disebut kerajinan", "Limbah anorganik", "Limbah organik", "Serat alam", "Kayu"], ["Teknik mengukir permukaan kayu untuk membuat motif disebut teknik", "Ukir", "Anyam", "Tenun", "Cor"], ["Teknik membentuk logam dengan cara dipanaskan dan dicetak disebut teknik", "Cor", "Ukir", "Anyam", "Jahit"], ["Serat alam yang berasal dari tumbuhan misalnya", "Kapas dan rami", "Wol", "Sutra ulat", "Nilon"], ["Serat yang berasal dari hewan misalnya", "Wol dan sutra", "Kapas", "Rami", "Poliester"], ["Rekayasa sederhana yang menghasilkan alat penjernih air disebut rekayasa bidang", "Teknologi tepat guna", "Kerajinan tangan", "Budidaya tanaman", "Pengolahan pangan"], ["Alat yang mengubah energi listrik menjadi gerak dalam rekayasa sederhana disebut", "Motor listrik", "Panel surya", "Baterai", "Sakelar"], ["Budidaya tanaman sayuran tanpa menggunakan tanah disebut", "Hidroponik", "Akuaponik", "Vertikultur", "Polikultur"], ["Budidaya ikan yang digabungkan dengan budidaya tanaman disebut", "Akuaponik", "Hidroponik", "Vertikultur", "Monokultur"], ["Menanam tanaman secara bertingkat pada lahan sempit disebut teknik", "Vertikultur", "Hidroponik", "Akuaponik", "Monokultur"], ["Budidaya ternak unggas pedaging misalnya budidaya", "Ayam broiler", "Ayam petelur", "Bebek hias", "Burung kicau"], ["Pengolahan bahan pangan setengah jadi misalnya pembuatan", "Tepung dari singkong", "Nasi goreng", "Sayur sop", "Es buah"], ["Pengawetan makanan dengan cara pengasapan bertujuan untuk", "Memperpanjang daya simpan", "Mempercepat pembusukan", "Mengubah warna saja", "Menambah berat"], ["Teknik pengawetan makanan dengan suhu rendah disebut", "Pendinginan", "Pemanasan", "Fermentasi saja", "Pengasapan"], ["Proses fermentasi digunakan dalam pembuatan", "Tempe dan tape", "Keripik", "Jus buah", "Salad"], ["Kemasan yang ramah lingkungan dan mudah terurai disebut kemasan", "Biodegradable", "Plastik sekali pakai", "Logam", "Styrofoam"], ["Desain kerajinan yang mempertimbangkan fungsi dan keindahan disebut prinsip", "Estetika dan ergonomis", "Ekonomi saja", "Produksi massal", "Distribusi cepat"], ["Tahapan produksi kerajinan diawali dengan", "Perencanaan dan desain", "Pemasaran", "Pengemasan", "Evaluasi"], ["Analisis kebutuhan pasar sebelum membuat produk disebut", "Riset pasar", "Produksi massal", "Distribusi", "Promosi"], ["Kegiatan mempromosikan produk agar dikenal masyarakat disebut", "Promosi", "Produksi", "Perencanaan", "Evaluasi"], ["Bahan limbah tekstil seperti kain perca dapat diolah menjadi", "Kerajinan tekstil", "Kerajinan logam", "Kerajinan kaca", "Kerajinan keramik"], ["Alat rekayasa sederhana yang memanfaatkan energi matahari disebut", "Panel surya", "Kincir angin", "Turbin air", "Generator diesel"], ["Budidaya tanaman hias bertujuan utama untuk", "Nilai keindahan dan ekonomi", "Bahan pangan pokok", "Bahan bakar", "Obat-obatan saja"], ["Teknik menenun benang menjadi kain disebut teknik", "Tenun", "Anyam", "Ukir", "Cor"], ["Pengemasan produk pangan yang baik harus memperhatikan", "Kebersihan dan keamanan", "Warna mencolok saja", "Harga murah saja", "Bentuk unik saja"], ["Wirausaha di bidang kerajinan perlu memperhitungkan", "Modal, produksi, dan pemasaran", "Modal saja", "Pemasaran saja", "Bahan baku saja"], ["Produk pengolahan pangan lokal berbahan singkong misalnya", "Keripik singkong", "Keripik kentang", "Kerupuk udang", "Abon sapi"], ["Teknik budidaya tanaman dengan menanam beberapa jenis tanaman sekaligus disebut", "Tumpang sari", "Monokultur", "Rotasi tanaman", "Hidroponik"]],
                            "SMA": [["Mata pelajaran Prakarya di SMA sering digabungkan dengan", "Kewirausahaan", "Olahraga", "Kesenian saja", "Bahasa asing"], ["Rencana usaha yang memuat visi, misi, dan strategi bisnis disebut", "Business plan", "Neraca keuangan", "Laporan laba rugi", "Katalog produk"], ["Kegiatan mengenali peluang usaha di lingkungan sekitar disebut", "Analisis peluang usaha", "Produksi massal", "Distribusi barang", "Promosi produk"], ["Sikap berani mengambil risiko dan berinovasi dalam usaha disebut jiwa", "Kewirausahaan", "Kepemimpinan formal", "Ketergantungan", "Konsumerisme"], ["Produk kerajinan yang dirancang berdasarkan kearifan lokal disebut produk", "Berbasis budaya lokal", "Impor", "Massal generik", "Tanpa identitas"], ["Proses produksi yang efisien bertujuan untuk", "Menekan biaya dan meningkatkan kualitas", "Menambah limbah", "Memperlambat produksi", "Mengurangi kualitas"], ["Strategi pemasaran 4P terdiri dari Product, Price, Place, dan", "Promotion", "People saja", "Process saja", "Profit saja"], ["Analisis kekuatan, kelemahan, peluang, dan ancaman usaha disebut analisis", "SWOT", "BEP", "ROI", "NPV"], ["Titik impas antara biaya dan pendapatan usaha disebut", "Break Even Point (BEP)", "Return on Investment", "Net profit margin", "Gross margin"], ["Modal usaha yang berasal dari milik sendiri disebut modal", "Sendiri (internal)", "Pinjaman", "Investasi asing", "Hibah pemerintah"], ["Modal usaha yang berasal dari pinjaman bank disebut modal", "Eksternal", "Internal", "Pribadi", "Hibah"], ["Kemasan produk yang menarik dan informatif berfungsi sebagai", "Media promosi dan pelindung produk", "Pemberat produk saja", "Penghias saja", "Penghambat distribusi"], ["Produk rekayasa teknologi tepat guna dirancang untuk", "Memecahkan masalah praktis di masyarakat", "Hiasan semata", "Koleksi pribadi", "Ekspor saja"], ["Budidaya perikanan skala besar untuk tujuan komersial disebut", "Akuakultur komersial", "Budidaya hias saja", "Konservasi saja", "Penangkapan liar"], ["Pengolahan pangan fungsional dirancang untuk", "Memberikan manfaat kesehatan tambahan", "Sekadar kenyang", "Menghabiskan bahan baku", "Menambah limbah"], ["Sertifikasi halal pada produk pangan bertujuan untuk", "Menjamin kehalalan produk bagi konsumen muslim", "Menambah harga jual saja", "Mempercantik kemasan", "Memperpanjang izin usaha"], ["Hak atas kekayaan intelektual pada desain produk disebut", "HAKI", "SIUP", "NPWP", "TDP"], ["Surat izin usaha yang wajib dimiliki pelaku usaha disebut", "SIUP", "HAKI", "NPWP saja", "Akta saja"], ["Inovasi produk bertujuan untuk", "Menciptakan nilai tambah dan daya saing", "Meniru produk lain", "Mengurangi kualitas", "Menambah biaya tanpa manfaat"], ["Segmentasi pasar berdasarkan usia, pendapatan, dan gaya hidup disebut segmentasi", "Demografis dan psikografis", "Geografis saja", "Politik saja", "Acak"], ["Kegiatan menyalurkan produk dari produsen ke konsumen disebut", "Distribusi", "Produksi", "Promosi", "Konsumsi"], ["Evaluasi usaha dilakukan untuk", "Mengukur keberhasilan dan memperbaiki kekurangan", "Menutup usaha", "Menambah utang", "Menghindari pajak"], ["Produk kerajinan ekspor perlu memperhatikan standar", "Kualitas dan mutu internasional", "Harga termurah saja", "Bahan seadanya", "Desain asal jadi"], ["Wirausaha sosial adalah usaha yang berorientasi pada", "Keuntungan sekaligus dampak sosial", "Keuntungan semata", "Kerugian terus-menerus", "Tanpa tujuan jelas"], ["Pengemasan ramah lingkungan mendukung konsep", "Bisnis berkelanjutan", "Produksi massal murah", "Distribusi cepat saja", "Promosi agresif"], ["Studi kelayakan usaha dilakukan sebelum", "Memulai suatu usaha", "Menutup usaha", "Membayar pajak", "Melakukan promosi"], ["Sumber daya utama dalam produksi meliputi manusia, modal, bahan baku, dan", "Teknologi", "Iklan saja", "Pajak saja", "Regulasi saja"], ["Diversifikasi produk bertujuan untuk", "Memperluas variasi produk dan pasar", "Mengurangi variasi produk", "Menutup usaha", "Menghentikan inovasi"], ["Analisis biaya produksi digunakan untuk menentukan", "Harga jual produk", "Warna kemasan", "Nama merek saja", "Logo usaha saja"], ["Digital marketing memanfaatkan media", "Internet dan media sosial", "Surat kabar cetak saja", "Radio saja", "Papan reklame saja"]],
                        },
                        "Koding dan Kecerdasan Artifisial": {
                            "SD": [["Kumpulan langkah-langkah untuk menyelesaikan suatu masalah secara berurutan disebut", "Algoritma", "Aplikasi", "Data", "Jaringan"], ["Aplikasi pemrograman berbasis blok yang cocok untuk pemula misalnya", "Scratch", "Python", "Java", "C++"], ["Perintah pada program yang dijalankan secara berurutan disebut struktur", "Sekuensial", "Perulangan", "Percabangan", "Paralel"], ["Perintah yang mengulang suatu langkah beberapa kali disebut", "Perulangan (loop)", "Percabangan", "Sekuensial", "Variabel"], ["Perintah yang memilih salah satu langkah berdasarkan syarat disebut", "Percabangan (if)", "Perulangan", "Sekuensial", "Fungsi"], ["Robot yang dapat mengikuti perintah manusia untuk membantu pekerjaan disebut robot", "Pembantu/asisten", "Berpikir sendiri", "Tanpa program", "Alami"], ["Mesin atau program yang dapat meniru cara berpikir manusia disebut", "Kecerdasan buatan", "Robot mekanik saja", "Komputer biasa", "Internet"], ["Aplikasi yang dapat menjawab pertanyaan seperti manusia disebut", "Chatbot", "Kalkulator", "Kamera", "Speaker"], ["Kesalahan pada program yang membuatnya tidak berjalan dengan benar disebut", "Bug", "Fitur", "Update", "Ikon"], ["Kegiatan mencari dan memperbaiki kesalahan program disebut", "Debugging", "Coding", "Browsing", "Uploading"], ["Bagian dari program yang digunakan untuk menyimpan nilai sementara disebut", "Variabel", "Fungsi", "Loop", "Array"], ["Gambar-gambar yang digerakkan dalam pemrograman blok disebut", "Sprite", "Icon", "Widget", "Banner"], ["Permainan yang dibuat menggunakan pemrograman disebut", "Game", "Poster", "Lagu", "Puisi"], ["Robot penyapu lantai otomatis di rumah menggunakan teknologi", "Kecerdasan buatan sederhana", "Mesin manual", "Alat listrik biasa", "Mainan biasa"], ["Asisten virtual di ponsel yang dapat menjawab perintah suara disebut", "Asisten AI (misal Siri/Google Assistant)", "Kamera", "Baterai", "Layar sentuh"], ["Langkah pertama sebelum membuat program adalah", "Merencanakan alur/algoritma", "Langsung menekan tombol run", "Menghapus semua kode", "Mematikan komputer"], ["Kode program yang ditulis oleh manusia disebut", "Kode sumber (source code)", "Kode mesin", "Bug", "Data mentah"], ["Alat yang digunakan untuk menjalankan program blok pada layar adalah", "Komputer atau tablet", "Kalkulator saja", "Radio", "Televisi analog"], ["Mengurutkan langkah cara membuat mi instan adalah contoh dari", "Algoritma sehari-hari", "Kecerdasan buatan", "Jaringan internet", "Basis data"], ["Ikon berbentuk bendera hijau pada Scratch digunakan untuk", "Memulai program", "Menghentikan program", "Menghapus program", "Menyimpan program"], ["Ikon tanda stop pada Scratch digunakan untuk", "Menghentikan program", "Memulai program", "Mengunduh program", "Membagikan program"], ["Foto yang dapat dikenali wajahnya secara otomatis oleh aplikasi menggunakan teknologi", "Pengenalan wajah (face recognition)", "Pengenalan suara", "Pengenalan sidik jari", "Pengenalan warna"], ["Perintah suara yang dipahami komputer untuk melakukan tindakan disebut teknologi", "Pengenalan suara", "Pengenalan wajah", "Pengenalan gambar", "Pengenalan tulisan"], ["Sikap bijak menggunakan teknologi digital sejak dini disebut", "Etika digital", "Kecanduan digital", "Plagiarisme", "Penyalahgunaan data"], ["Data pribadi yang perlu dijaga kerahasiaannya saat menggunakan aplikasi contohnya", "Nama dan alamat rumah", "Warna favorit", "Nama hewan peliharaan", "Judul film favorit"], ["Permainan edukatif berbasis komputer dapat membantu belajar sambil", "Bermain", "Tidur", "Mengantuk", "Melamun"], ["Bentuk paling sederhana dari perintah komputer disebut", "Instruksi", "Ilustrasi", "Investasi", "Interaksi"], ["Kumpulan blok kode yang disusun untuk membuat animasi bergerak disebut", "Skrip (script)", "Sensor", "Server", "Domain"], ["Mobil yang dapat berjalan sendiri tanpa dikendalikan manusia menggunakan teknologi", "Kecerdasan buatan (mobil otonom)", "Mesin uap", "Roda manual", "Rem tangan"], ["Kegiatan menyusun urutan gambar untuk membuat cerita animasi disebut", "Storyboard", "Storyline saja", "Story mode saja", "Storage"]],
                            "SMP": [["Bahasa pemrograman berbasis teks yang mudah dipelajari pemula adalah", "Python", "HTML saja", "CSS saja", "SQL saja"], ["Variabel dalam pemrograman digunakan untuk", "Menyimpan nilai data", "Menampilkan gambar saja", "Menghapus program", "Memutar musik"], ["Struktur kontrol yang mengulang blok kode disebut", "Perulangan (for/while)", "Percabangan", "Fungsi", "Array"], ["Struktur kontrol yang memilih jalur berdasarkan kondisi disebut", "Percabangan (if-else)", "Perulangan", "Variabel", "Konstanta"], ["Kumpulan instruksi yang diberi nama dan dapat dipanggil berulang disebut", "Fungsi", "Variabel", "Array", "Kelas"], ["Kumpulan data sejenis yang tersusun berurutan disebut", "Array/list", "Variabel tunggal", "Fungsi", "Objek"], ["Kecerdasan buatan yang dapat belajar dari data disebut", "Machine learning", "Basis data biasa", "Jaringan LAN", "Sistem operasi"], ["Data yang digunakan untuk melatih model kecerdasan buatan disebut", "Data latih (training data)", "Data sampah", "Data cadangan", "Data kosong"], ["Program komputer yang dapat mengenali pola gambar disebut sistem", "Pengenalan gambar (image recognition)", "Pengolah kata", "Pengolah angka", "Peramban web"], ["Chatbot berbasis AI dapat menjawab pertanyaan pengguna menggunakan", "Pemrosesan bahasa alami (NLP)", "Pengolah angka", "Kompresi data", "Enkripsi data"], ["Kesalahan logika pada program yang tidak menghasilkan output yang diharapkan disebut", "Bug logika", "Fitur baru", "Update sistem", "Backup data"], ["Kegiatan menguji program untuk menemukan kesalahan disebut", "Testing", "Deploying", "Hosting", "Uploading"], ["Diagram yang menggambarkan alur logika program disebut", "Flowchart", "Mind map", "Infografis", "Peta konsep"], ["Simbol flowchart berbentuk belah ketupat menyatakan", "Keputusan/percabangan", "Proses", "Mulai/selesai", "Input/output"], ["Kode program yang sudah diterjemahkan ke bahasa mesin disebut", "Kode objek (object code)", "Kode sumber", "Pseudocode", "Algoritma"], ["Etika dalam menggunakan kecerdasan buatan penting untuk mencegah", "Penyalahgunaan data dan bias", "Peningkatan efisiensi", "Kemudahan akses", "Otomatisasi tugas"], ["Bias dalam sistem AI dapat terjadi akibat", "Data latih yang tidak seimbang", "Kode terlalu pendek", "Komputer terlalu cepat", "Internet terlalu lambat"], ["Robot yang dapat bergerak dan mengambil keputusan sendiri berdasarkan sensor disebut robot", "Otonom", "Manual", "Statis", "Analog"], ["Sensor yang mendeteksi jarak benda pada robot disebut sensor", "Ultrasonik", "Warna", "Suara", "Cahaya saja"], ["Pemrograman berorientasi objek mengelompokkan data dan fungsi dalam bentuk", "Kelas dan objek", "Array saja", "Variabel saja", "Loop saja"], ["Internet of Things (IoT) menghubungkan berbagai perangkat melalui", "Internet", "Kabel telepon saja", "Radio AM saja", "Surat pos"], ["Asisten virtual yang menjawab perintah suara menggunakan teknologi", "Pengenalan suara dan AI", "Pengenalan wajah saja", "Pengenalan sidik jari saja", "Pengenalan warna saja"], ["Data besar yang kompleks dan sulit diolah dengan cara biasa disebut", "Big data", "Small data", "Metadata saja", "Cache"], ["Keamanan data pribadi saat menggunakan aplikasi AI penting untuk menjaga", "Privasi pengguna", "Kecepatan internet", "Ukuran layar", "Warna aplikasi"], ["Algoritma pencarian yang membagi data menjadi dua bagian secara berulang disebut", "Binary search", "Bubble sort", "Linear search", "Selection sort"], ["Pseudocode digunakan untuk", "Menuliskan algoritma dengan bahasa sederhana sebelum coding", "Menjalankan program langsung", "Mengganti bahasa pemrograman", "Mengunggah program ke internet"], ["Contoh penerapan AI dalam bidang kesehatan adalah", "Deteksi penyakit dari gambar medis", "Menyapu lantai", "Menyalakan lampu", "Memasak nasi"], ["Contoh penerapan AI dalam transportasi adalah", "Mobil otonom dan navigasi cerdas", "Sepeda ontel", "Delman", "Gerobak dorong"], ["Prinsip AI yang bertanggung jawab menekankan pentingnya", "Transparansi dan keadilan", "Kecepatan semata", "Keuntungan semata", "Kerahasiaan penuh tanpa aturan"], ["Model AI yang salah memberikan hasil karena data tidak lengkap disebut mengalami", "Bias data", "Optimasi", "Kompresi", "Enkripsi"]],
                            "SMA": [["Cabang kecerdasan buatan yang meniru cara kerja jaringan saraf otak disebut", "Jaringan saraf tiruan (neural network)", "Basis data relasional", "Sistem operasi", "Jaringan komputer"], ["Proses melatih model AI menggunakan data berlabel disebut pembelajaran", "Terawasi (supervised learning)", "Tanpa pengawasan", "Penguatan saja", "Acak"], ["Proses melatih model AI tanpa data berlabel disebut pembelajaran", "Tanpa pengawasan (unsupervised learning)", "Terawasi", "Penguatan", "Manual"], ["Pembelajaran mesin di mana model belajar melalui coba-coba dan hadiah disebut", "Pembelajaran penguatan (reinforcement learning)", "Pembelajaran terawasi", "Pembelajaran tanpa pengawasan", "Pembelajaran statis"], ["Cabang AI yang memungkinkan komputer memahami bahasa manusia disebut", "Pemrosesan bahasa alami (NLP)", "Visi komputer", "Robotika", "Basis data"], ["Cabang AI yang memungkinkan komputer mengenali objek pada gambar disebut", "Visi komputer (computer vision)", "Pemrosesan bahasa alami", "Robotika", "Kriptografi"], ["Lapisan pada jaringan saraf tiruan yang menerima data awal disebut lapisan", "Input", "Tersembunyi (hidden)", "Output", "Aktivasi"], ["Lapisan pada jaringan saraf tiruan yang menghasilkan hasil akhir disebut lapisan", "Output", "Input", "Tersembunyi", "Konvolusi"], ["Model AI yang dilatih secara berlebihan sehingga akurat pada data latih tetapi buruk pada data baru mengalami", "Overfitting", "Underfitting", "Normalisasi", "Regularisasi berhasil"], ["Model AI yang terlalu sederhana sehingga tidak mampu mempelajari pola data disebut mengalami", "Underfitting", "Overfitting", "Konvergensi", "Optimasi sempurna"], ["Data yang digunakan untuk menguji performa model setelah pelatihan disebut data", "Uji (testing data)", "Latih", "Validasi silang saja", "Cadangan"], ["Bahasa pemrograman yang populer untuk pengembangan AI dan data science adalah", "Python", "HTML", "CSS", "Assembly"], ["Struktur data pohon biner banyak digunakan dalam algoritma", "Pencarian dan pengurutan data", "Enkripsi email", "Kompresi audio saja", "Rendering grafis saja"], ["Kompleksitas algoritma yang menyatakan efisiensi waktu eksekusi disebut notasi", "Big O", "Big Data", "Big Bang saja", "Big Query"], ["Etika AI menekankan pentingnya transparansi, keadilan, dan", "Akuntabilitas", "Kecepatan semata", "Kerahasiaan mutlak", "Biaya rendah semata"], ["Bias algoritma dapat menyebabkan diskriminasi terhadap kelompok tertentu akibat", "Data latih yang tidak representatif", "Kode program terlalu pendek", "Server terlalu cepat", "Jaringan terlalu stabil"], ["Deepfake adalah teknologi AI yang digunakan untuk", "Memanipulasi gambar atau video secara realistis", "Mengenkripsi data", "Mengompresi file", "Menyimpan cadangan data"], ["Perlindungan data pribadi dalam pengembangan AI diatur melalui regulasi", "Perlindungan data pribadi", "Hak cipta saja", "Hak paten saja", "Merek dagang saja"], ["Model bahasa besar yang dapat menghasilkan teks seperti manusia disebut", "Large Language Model (LLM)", "Basis data relasional", "Sistem pakar sederhana", "Jaringan LAN"], ["Sistem yang meniru pengambilan keputusan pakar manusia di bidang tertentu disebut", "Sistem pakar (expert system)", "Sistem operasi", "Basis data", "Jaringan komputer"], ["Proses mengubah data mentah menjadi bentuk yang siap dianalisis disebut", "Pra-pemrosesan data (data preprocessing)", "Enkripsi data", "Kompresi data", "Distribusi data"], ["Visualisasi data bertujuan untuk", "Mempermudah pemahaman pola dan tren data", "Menyembunyikan data", "Memperbesar ukuran file", "Memperlambat analisis"], ["Algoritma pengurutan yang efisien untuk data besar misalnya", "Merge sort atau quick sort", "Bubble sort saja", "Selection sort saja", "Insertion sort saja"], ["Komputasi awan (cloud computing) memungkinkan pelatihan model AI dengan", "Sumber daya komputasi yang dapat diskalakan", "Komputer tunggal terbatas", "Tanpa koneksi internet", "Kertas dan pena"], ["Robot yang menggunakan AI untuk bernavigasi secara mandiri disebut robot", "Otonom berbasis AI", "Manual", "Terprogram statis", "Analog"], ["Pengujian model AI dengan data yang belum pernah dilihat sebelumnya bertujuan mengukur", "Kemampuan generalisasi model", "Kecepatan komputer", "Ukuran penyimpanan", "Warna antarmuka"], ["Isu keamanan siber terkait AI meliputi risiko", "Serangan adversarial pada model AI", "Peningkatan kecepatan internet", "Penurunan harga perangkat", "Penambahan RAM"], ["Konsep AI yang dapat menjelaskan alasan di balik keputusannya disebut", "AI yang dapat dijelaskan (explainable AI)", "AI tertutup", "AI acak", "AI statis"], ["Penerapan AI dalam bidang pertanian dapat membantu", "Memprediksi hasil panen dan mendeteksi hama", "Menggantikan seluruh petani", "Menghapus kebutuhan lahan", "Menghentikan produksi pangan"], ["Kolaborasi manusia dan AI di dunia kerja menekankan pentingnya", "Keterampilan berpikir kritis dan adaptasi", "Menghindari teknologi sepenuhnya", "Ketergantungan penuh tanpa pengawasan", "Penghapusan seluruh pekerjaan manual"]],
                        },
                        "Pendidikan Agama Islam": {
                            "SD": [["Rukun Islam yang pertama adalah", "Syahadat", "Salat", "Zakat", "Puasa"], ["Rukun Islam yang kedua adalah", "Salat", "Syahadat", "Zakat", "Haji"], ["Rukun Islam yang ketiga adalah", "Zakat", "Salat", "Puasa", "Haji"], ["Rukun Islam yang keempat adalah", "Puasa Ramadan", "Zakat", "Salat", "Syahadat"], ["Rukun Islam yang kelima adalah", "Haji bagi yang mampu", "Puasa", "Zakat", "Salat"], ["Jumlah rukun Islam ada", "Lima", "Empat", "Enam", "Tiga"], ["Jumlah rukun Iman ada", "Enam", "Lima", "Empat", "Tujuh"], ["Kitab suci umat Islam adalah", "Al-Qur'an", "Taurat", "Zabur", "Injil"], ["Nabi terakhir dan penutup para nabi adalah", "Nabi Muhammad SAW", "Nabi Musa AS", "Nabi Isa AS", "Nabi Ibrahim AS"], ["Salat wajib dilaksanakan sebanyak", "Lima waktu sehari", "Tiga waktu sehari", "Dua waktu sehari", "Tujuh waktu sehari"], ["Salat yang dikerjakan saat matahari terbenam disebut salat", "Magrib", "Subuh", "Zuhur", "Asar"], ["Salat yang dikerjakan pada waktu fajar disebut salat", "Subuh", "Magrib", "Isya", "Zuhur"], ["Bulan wajib berpuasa bagi umat Islam adalah bulan", "Ramadan", "Syawal", "Muharam", "Rajab"], ["Tempat ibadah umat Islam disebut", "Masjid", "Gereja", "Pura", "Wihara"], ["Kegiatan membaca Al-Qur'an dengan tartil disebut", "Tilawah", "Ceramah", "Khotbah", "Dakwah"], ["Zakat yang wajib dikeluarkan menjelang Idulfitri disebut zakat", "Fitrah", "Mal", "Profesi", "Emas"], ["Ibadah puasa dimulai sejak terbit fajar hingga", "Terbenam matahari", "Tengah malam", "Terbit matahari", "Siang hari"], ["Kalimat syahadat berisi pengakuan tentang", "Keesaan Allah dan kerasulan Nabi Muhammad", "Nama-nama malaikat", "Nama kitab suci", "Nama nabi terdahulu"], ["Malaikat yang bertugas menyampaikan wahyu kepada para nabi adalah", "Jibril", "Mikail", "Israfil", "Izrail"], ["Malaikat yang bertugas mencabut nyawa adalah", "Izrail", "Jibril", "Mikail", "Munkar"], ["Sikap jujur dalam ajaran Islam disebut", "Sidik", "Amanah", "Tablig", "Fatanah"], ["Sikap dapat dipercaya dalam ajaran Islam disebut", "Amanah", "Sidik", "Tablig", "Fatanah"], ["Perbuatan baik kepada kedua orang tua disebut", "Birrul walidain", "Silaturahmi saja", "Sedekah saja", "Tawaduk saja"], ["Kegiatan saling mengunjungi dan menyambung tali persaudaraan disebut", "Silaturahmi", "Ghibah", "Fitnah", "Riya"], ["Sikap rendah hati dan tidak sombong dalam Islam disebut", "Tawaduk", "Takabur", "Riya", "Hasad"], ["Hari besar umat Islam setelah bulan Ramadan disebut", "Idulfitri", "Idul Adha", "Isra Mikraj", "Maulid Nabi"], ["Hari raya kurban dalam Islam disebut", "Idul Adha", "Idulfitri", "Nuzulul Qur'an", "Tahun baru Hijriah"], ["Peristiwa perjalanan malam Nabi Muhammad dari Mekah ke Yerusalem lalu ke langit disebut", "Isra Mikraj", "Hijrah", "Fathu Makkah", "Nuzulul Qur'an"], ["Kalender yang digunakan umat Islam disebut kalender", "Hijriah", "Masehi", "Saka", "Julian"], ["Wudu dilakukan sebelum melaksanakan ibadah", "Salat", "Puasa", "Zakat", "Sedekah"]],
                            "SMP": [["Ilmu yang mempelajari tata cara ibadah dalam Islam disebut ilmu", "Fikih", "Tauhid", "Akhlak", "Tarikh"], ["Ilmu yang mempelajari keesaan Allah disebut ilmu", "Tauhid", "Fikih", "Akhlak", "Tarikh"], ["Ilmu yang mempelajari sejarah Islam disebut ilmu", "Tarikh/Sejarah Islam", "Tauhid", "Fikih", "Tajwid"], ["Ilmu yang mempelajari tata cara membaca Al-Qur'an dengan benar disebut ilmu", "Tajwid", "Fikih", "Tauhid", "Nahwu"], ["Hukum mengerjakan salat lima waktu bagi muslim baligh adalah", "Fardu ain (wajib)", "Sunah", "Mubah", "Makruh"], ["Hukum salat sunah rawatib adalah", "Sunah", "Wajib", "Haram", "Makruh"], ["Rukun salat yang pertama adalah", "Niat", "Rukuk", "Sujud", "Salam"], ["Gerakan salat membungkukkan badan disebut", "Rukuk", "Sujud", "Iktidal", "Tasyahud"], ["Gerakan salat meletakkan dahi ke lantai disebut", "Sujud", "Rukuk", "Iktidal", "Duduk di antara dua sujud"], ["Syarat sah salat di antaranya suci dari hadas dan menutup", "Aurat", "Rambut saja", "Wajah saja", "Tangan saja"], ["Zakat yang dikenakan pada harta simpanan disebut zakat", "Mal", "Fitrah", "Profesi saja", "Pertanian saja"], ["Nisab adalah batas minimal harta yang wajib", "Dizakati", "Dihibahkan", "Dijual", "Diwariskan"], ["Puasa yang dilakukan setiap Senin dan Kamis termasuk puasa", "Sunah", "Wajib", "Haram", "Makruh"], ["Hal yang membatalkan puasa antara lain", "Makan dan minum dengan sengaja", "Tidur siang", "Membaca Al-Qur'an", "Berzikir"], ["Nabi Muhammad SAW lahir di kota", "Mekah", "Madinah", "Yerusalem", "Baghdad"], ["Nabi Muhammad SAW hijrah dari Mekah menuju", "Madinah", "Yerusalem", "Baghdad", "Damaskus"], ["Peristiwa turunnya Al-Qur'an pertama kali disebut", "Nuzulul Qur'an", "Isra Mikraj", "Hijrah", "Fathu Makkah"], ["Khalifah pertama setelah Nabi Muhammad wafat adalah", "Abu Bakar As-Siddiq", "Umar bin Khattab", "Usman bin Affan", "Ali bin Abi Thalib"], ["Sifat wajib bagi Allah yang berarti Maha Esa adalah", "Wahdaniyah", "Qidam", "Baqa", "Wujud"], ["Sifat mustahil bagi Allah yang berarti sombong disebut", "Takabbur", "Wahdaniyah", "Iradah", "Ilmu"], ["Akhlak terpuji terhadap sesama manusia disebut akhlak", "Mahmudah", "Mazmumah", "Fasad", "Munkar"], ["Akhlak tercela yang harus dihindari disebut akhlak", "Mazmumah", "Mahmudah", "Karimah saja", "Sholihah saja"], ["Sikap menahan diri dari sifat marah berlebihan disebut", "Sabar", "Riya", "Hasad", "Takabur"], ["Sikap iri hati terhadap nikmat orang lain disebut", "Hasad", "Sabar", "Tawaduk", "Amanah"], ["Sikap pamer dalam beribadah agar dipuji orang disebut", "Riya", "Ikhlas", "Tawaduk", "Sabar"], ["Ibadah kurban dilaksanakan pada bulan", "Zulhijah", "Ramadan", "Syawal", "Muharam"], ["Ibadah haji dilaksanakan di kota", "Mekah", "Madinah", "Yerusalem", "Kairo"], ["Tawaf adalah kegiatan mengelilingi", "Ka'bah", "Masjid Nabawi", "Bukit Safa", "Padang Arafah"], ["Sai adalah kegiatan berlari kecil antara bukit", "Safa dan Marwah", "Uhud dan Safa", "Marwah dan Sinai", "Tursina dan Safa"], ["Salah satu adab bergaul dengan teman dalam Islam adalah", "Saling menghormati dan tolong-menolong", "Saling mencela", "Bersikap acuh", "Mengabaikan hak teman"]],
                            "SMA": [["Ilmu yang membahas hukum-hukum muamalah dalam Islam disebut fikih", "Muamalah", "Ibadah saja", "Munakahat saja", "Jinayah saja"], ["Hukum pernikahan dalam Islam dibahas dalam fikih", "Munakahat", "Muamalah", "Jinayah", "Mawaris"], ["Hukum waris dalam Islam dibahas dalam ilmu", "Mawaris (faraid)", "Munakahat", "Muamalah", "Jinayah"], ["Hukum pidana Islam dibahas dalam fikih", "Jinayah", "Munakahat", "Muamalah", "Mawaris"], ["Prinsip ekonomi Islam melarang praktik", "Riba", "Jual beli", "Sewa-menyewa", "Bagi hasil"], ["Sistem bagi hasil dalam ekonomi syariah disebut", "Mudarabah", "Riba", "Gharar", "Maisir"], ["Kerja sama usaha dengan modal bersama dalam ekonomi syariah disebut", "Musyarakah", "Riba", "Gharar", "Maisir"], ["Ketidakpastian yang dilarang dalam transaksi syariah disebut", "Gharar", "Mudarabah", "Musyarakah", "Wadiah"], ["Perjudian yang dilarang dalam Islam disebut", "Maisir", "Mudarabah", "Musyarakah", "Wadiah"], ["Ilmu kalam membahas tentang", "Akidah dan keyakinan Islam", "Tata cara ibadah", "Sejarah Islam", "Bacaan Al-Qur'an"], ["Aliran teologi dalam Islam yang menekankan akal dan wahyu bersama antara lain", "Asy'ariyah dan Mu'tazilah", "Hanafiyah saja", "Malikiyah saja", "Syafi'iyah saja"], ["Empat mazhab besar fikih dalam Islam Sunni adalah Hanafi, Maliki, Syafi'i, dan", "Hanbali", "Ja'fari", "Zahiri saja", "Ibadi saja"], ["Ijtihad adalah usaha sungguh-sungguh ulama untuk", "Menetapkan hukum yang belum diatur secara jelas", "Membatalkan hukum yang ada", "Menghapus Al-Qur'an", "Mengubah rukun Islam"], ["Sumber hukum Islam yang pertama adalah", "Al-Qur'an", "Ijma", "Kias", "Ijtihad"], ["Sumber hukum Islam kedua setelah Al-Qur'an adalah", "Hadis", "Ijma", "Kias", "Ijtihad"], ["Kesepakatan para ulama dalam menetapkan hukum disebut", "Ijma", "Kias", "Hadis", "Ijtihad"], ["Penetapan hukum baru berdasarkan analogi dengan hukum yang sudah ada disebut", "Kias (qiyas)", "Ijma", "Ijtihad saja", "Hadis"], ["Peradaban Islam mengalami masa keemasan pada masa Dinasti", "Abbasiyah", "Umayyah saja", "Fatimiyah saja", "Mamluk saja"], ["Ilmuwan muslim yang dikenal sebagai bapak aljabar adalah", "Al-Khawarizmi", "Ibnu Sina", "Al-Farabi", "Ibnu Rusyd"], ["Ilmuwan muslim yang dikenal dalam bidang kedokteran adalah", "Ibnu Sina (Avicenna)", "Al-Khawarizmi", "Al-Battani", "Al-Kindi"], ["Masuknya Islam ke Nusantara diperkirakan dibawa melalui jalur", "Perdagangan", "Peperangan saja", "Penjajahan saja", "Perbudakan saja"], ["Kerajaan Islam pertama di Nusantara adalah", "Samudra Pasai", "Demak", "Mataram Islam", "Banten"], ["Konsep toleransi dalam Islam mengajarkan sikap", "Menghormati perbedaan keyakinan", "Memaksakan keyakinan", "Mengabaikan perbedaan", "Menolak interaksi sosial"], ["Konsep ukhuwah Islamiyah menekankan pentingnya", "Persaudaraan sesama muslim", "Persaingan antarumat", "Perpecahan umat", "Individualisme"], ["Dakwah dalam Islam sebaiknya dilakukan dengan cara", "Hikmah dan cara yang baik", "Paksaan", "Kekerasan", "Ancaman"], ["Konsep jihad dalam Islam secara luas mencakup", "Sungguh-sungguh berjuang di jalan kebaikan", "Hanya peperangan semata", "Balas dendam", "Permusuhan"], ["Etika berbisnis dalam Islam menekankan pentingnya", "Kejujuran dan keadilan", "Keuntungan sebesar-besarnya tanpa aturan", "Penipuan yang tersembunyi", "Monopoli pasar"], ["Konsep khalifah dalam Islam mengandung makna manusia sebagai", "Pemimpin dan pengelola bumi", "Penguasa mutlak tanpa tanggung jawab", "Makhluk pasif", "Perusak alam"], ["Filsafat Islam banyak dipengaruhi oleh pemikiran", "Yunani yang diadaptasi ulama muslim", "Hanya budaya Arab", "Hanya budaya Persia", "Tidak dipengaruhi budaya lain"], ["Tasawuf dalam Islam menekankan aspek", "Penyucian hati dan kedekatan spiritual dengan Allah", "Hukum pidana", "Ekonomi semata", "Politik semata"]],
                        },
                        "Pendidikan Agama Kristen": {
                            "SD": [["Kitab suci umat Kristen disebut", "Alkitab", "Al-Qur'an", "Weda", "Tripitaka"], ["Alkitab terdiri dari dua bagian besar yaitu Perjanjian Lama dan", "Perjanjian Baru", "Perjanjian Tengah", "Perjanjian Akhir", "Perjanjian Awal"], ["Tempat ibadah umat Kristen disebut", "Gereja", "Masjid", "Pura", "Wihara"], ["Tokoh utama dalam iman Kristen yang diyakini sebagai Juru Selamat adalah", "Yesus Kristus", "Musa", "Abraham", "Daud"], ["Hari raya yang memperingati kelahiran Yesus Kristus disebut", "Natal", "Paskah", "Pentakosta", "Kenaikan"], ["Hari raya yang memperingati kebangkitan Yesus Kristus disebut", "Paskah", "Natal", "Pentakosta", "Advent"], ["Hari ibadah utama umat Kristen umumnya jatuh pada hari", "Minggu", "Jumat", "Sabtu", "Senin"], ["Doa yang diajarkan langsung oleh Yesus kepada para murid disebut", "Doa Bapa Kami", "Doa Salam Maria", "Doa Rosario", "Doa Malaikat Tuhan"], ["Sepuluh perintah Allah disebut juga", "Dasa Titah", "Tri Hita Karana", "Rukun Iman", "Pancasila"], ["Kasih kepada Tuhan dan kasih kepada sesama merupakan inti ajaran", "Kristen", "Tanpa nama khusus", "Filsafat umum", "Tradisi lokal"], ["Kisah tentang penciptaan dunia dalam Alkitab terdapat pada kitab", "Kejadian", "Keluaran", "Mazmur", "Wahyu"], ["Nabi yang memimpin bangsa Israel keluar dari Mesir adalah", "Musa", "Abraham", "Daud", "Yusuf"], ["Raja Israel yang terkenal karena mengalahkan Goliat adalah", "Daud", "Musa", "Saul", "Salomo"], ["Kedua belas pengikut utama Yesus disebut", "Rasul/murid", "Nabi", "Imam", "Malaikat"], ["Kitab dalam Alkitab yang berisi nyanyian pujian disebut kitab", "Mazmur", "Kejadian", "Wahyu", "Amsal"], ["Sakramen yang menandai seseorang resmi menjadi anggota gereja disebut", "Baptisan", "Perjamuan kudus saja", "Pengakuan dosa saja", "Pernikahan saja"], ["Perayaan mengenang perjamuan terakhir Yesus dengan para murid disebut", "Perjamuan kudus", "Baptisan", "Pengakuan iman", "Pemberkatan"], ["Tempat kelahiran Yesus Kristus menurut Alkitab adalah", "Betlehem", "Nazaret", "Yerusalem", "Galilea"], ["Ibu Yesus Kristus dalam ajaran Kristen adalah", "Maria", "Marta", "Elisabet", "Sara"], ["Sikap saling mengasihi sesama manusia diajarkan melalui perumpamaan", "Orang Samaria yang baik hati", "Anak yang hilang saja", "Talenta saja", "Domba yang hilang saja"], ["Sikap bersyukur kepada Tuhan dapat diwujudkan melalui", "Doa dan ibadah", "Mengabaikan Tuhan", "Bersikap sombong", "Melupakan sesama"], ["Kegiatan membaca dan merenungkan firman Tuhan disebut", "Saat teduh", "Ziarah", "Puasa saja", "Perayaan saja"], ["Pemimpin ibadah di gereja umumnya disebut", "Pendeta", "Imam", "Biksu", "Pandita"], ["Kasih yang tulus tanpa mengharapkan balasan dalam ajaran Kristen disebut kasih", "Agape", "Filia saja", "Eros saja", "Storge saja"], ["Sikap jujur dan tidak berbohong merupakan salah satu nilai dalam", "Dasa Titah", "Tradisi lokal saja", "Aturan sekolah saja", "Kebiasaan masyarakat saja"], ["Kegiatan menolong sesama yang membutuhkan disebut perbuatan", "Kasih", "Sombong", "Iri hati", "Serakah"], ["Minggu yang mempersiapkan umat Kristen menyambut Natal disebut masa", "Adven", "Paskah saja", "Pentakosta saja", "Prapaskah saja"], ["Masa 40 hari sebelum Paskah yang diisi dengan refleksi dan pertobatan disebut", "Prapaskah", "Adven", "Pentakosta", "Natal"], ["Hari turunnya Roh Kudus kepada para rasul disebut", "Pentakosta", "Paskah", "Natal", "Adven"], ["Sikap rendah hati dan mau melayani sesama diteladankan oleh", "Yesus Kristus", "Tokoh dongeng", "Pahlawan super", "Tokoh kartun"]],
                            "SMP": [["Perjanjian Lama dalam Alkitab sebagian besar ditulis dalam bahasa", "Ibrani", "Yunani", "Latin", "Arab"], ["Perjanjian Baru dalam Alkitab sebagian besar ditulis dalam bahasa", "Yunani", "Ibrani", "Latin", "Aram saja"], ["Empat kitab Injil dalam Perjanjian Baru adalah Matius, Markus, Lukas, dan", "Yohanes", "Kisah Para Rasul", "Wahyu", "Roma"], ["Kitab yang menceritakan perjalanan pelayanan para rasul setelah kenaikan Yesus adalah", "Kisah Para Rasul", "Injil Yohanes", "Wahyu", "Mazmur"], ["Rasul yang menulis banyak surat kepada jemaat mula-mula adalah", "Paulus", "Yohanes saja", "Petrus saja", "Matius saja"], ["Konsep Tritunggal dalam iman Kristen mengacu pada Allah Bapa, Anak, dan", "Roh Kudus", "Malaikat", "Nabi", "Rasul"], ["Peristiwa Yesus disalibkan diperingati pada hari", "Jumat Agung", "Minggu Palma", "Kamis Putih", "Sabtu Suci"], ["Hari Minggu sebelum Paskah yang memperingati Yesus memasuki Yerusalem disebut", "Minggu Palma", "Jumat Agung", "Kamis Putih", "Sabtu Suci"], ["Malam sebelum Jumat Agung yang memperingati perjamuan terakhir disebut", "Kamis Putih", "Jumat Agung", "Minggu Palma", "Sabtu Suci"], ["Sakramen dalam gereja yang menandai pengampunan dosa disebut", "Pengakuan dosa/pertobatan", "Baptisan saja", "Perjamuan kudus saja", "Pemberkatan saja"], ["Nilai kasih dalam ajaran Kristen tercermin dalam hukum kasih yaitu mengasihi Tuhan dan", "Mengasihi sesama manusia", "Mengasihi diri sendiri saja", "Mengasihi harta", "Mengasihi kekuasaan"], ["Konsep keselamatan dalam iman Kristen diperoleh melalui", "Iman kepada Yesus Kristus", "Perbuatan baik semata", "Kekayaan", "Kedudukan sosial"], ["Gereja sebagai persekutuan orang percaya memiliki peran penting dalam", "Membangun iman dan pelayanan", "Mencari keuntungan", "Persaingan politik", "Kekuasaan duniawi"], ["Sikap toleransi dalam kehidupan beragama penting untuk menjaga", "Kerukunan antarumat", "Perpecahan", "Konflik", "Permusuhan"], ["Keluarga dalam ajaran Kristen dipandang sebagai", "Gereja kecil/tempat pendidikan iman", "Tempat persaingan", "Institusi ekonomi semata", "Tempat tanpa nilai spiritual"], ["Etika Kristen mengajarkan pentingnya bersikap jujur dalam", "Perkataan dan perbuatan", "Hanya perkataan saja", "Hanya perbuatan saja", "Tidak keduanya"], ["Perumpamaan tentang anak yang hilang mengajarkan tentang", "Pengampunan dan kasih Bapa", "Balas dendam", "Kesombongan", "Keserakahan"], ["Perumpamaan tentang talenta mengajarkan pentingnya", "Bertanggung jawab menggunakan karunia yang diberikan", "Menyembunyikan kemampuan", "Iri hati", "Malas berusaha"], ["Konsep pelayanan (diakonia) dalam gereja berarti", "Melayani sesama dengan kasih", "Mencari popularitas", "Berkuasa atas orang lain", "Mengabaikan kebutuhan sesama"], ["Persekutuan (koinonia) dalam gereja menekankan pentingnya", "Kebersamaan umat percaya", "Individualisme", "Persaingan", "Perpecahan"], ["Kesaksian (marturia) dalam iman Kristen berarti", "Menyampaikan kabar baik kepada orang lain", "Menyembunyikan iman", "Memaksakan keyakinan", "Mengabaikan sesama"], ["Pujian dan penyembahan (liturgi) dalam ibadah bertujuan untuk", "Memuliakan Tuhan", "Hiburan semata", "Kompetisi paduan suara", "Menunjukkan kekayaan"], ["Roh Kudus dalam ajaran Kristen berperan sebagai", "Penolong dan penuntun umat percaya", "Malaikat pelindung saja", "Nabi terakhir", "Rasul utama"], ["Sikap mengampuni orang yang bersalah diajarkan Yesus melalui doa", "Bapa Kami", "Salam Maria", "Rosario", "Malaikat Tuhan"], ["Nilai kejujuran dan integritas penting diterapkan dalam kehidupan", "Sehari-hari termasuk sekolah dan masyarakat", "Hanya di gereja saja", "Hanya saat berdoa saja", "Tidak perlu diterapkan"], ["Sikap peduli terhadap lingkungan sebagai wujud tanggung jawab manusia disebut", "Kepedulian terhadap ciptaan Tuhan", "Eksploitasi alam", "Pengabaian lingkungan", "Perusakan alam"], ["Konsep damai sejahtera dalam iman Kristen mengajak umat untuk", "Hidup rukun dan menjadi pembawa damai", "Mencari konflik", "Bersikap individualis", "Mengabaikan sesama"], ["Pelayanan sosial gereja seperti membantu kaum miskin mencerminkan nilai", "Kasih dan kepedulian sosial", "Kompetisi ekonomi", "Individualisme", "Ketidakpedulian"], ["Sikap rendah hati dalam kepemimpinan Kristen diteladankan melalui tindakan Yesus", "Membasuh kaki para murid", "Menghukum musuh", "Mencari kekuasaan", "Mengabaikan pengikut"], ["Pendidikan agama Kristen mengajarkan pentingnya membangun karakter yang", "Berlandaskan iman dan kasih", "Individualis semata", "Materialistis", "Egois"]],
                            "SMA": [["Ilmu yang mempelajari ajaran iman Kristen secara sistematis disebut", "Teologi", "Liturgi", "Homiletika", "Eklesiologi"], ["Cabang teologi yang mempelajari tentang gereja disebut", "Eklesiologi", "Kristologi", "Soteriologi", "Pneumatologi"], ["Cabang teologi yang mempelajari tentang pribadi dan karya Yesus Kristus disebut", "Kristologi", "Eklesiologi", "Soteriologi", "Antropologi teologis"], ["Cabang teologi yang mempelajari tentang keselamatan disebut", "Soteriologi", "Kristologi", "Eklesiologi", "Eskatologi"], ["Cabang teologi yang mempelajari tentang akhir zaman disebut", "Eskatologi", "Soteriologi", "Kristologi", "Eklesiologi"], ["Reformasi gereja pada abad ke-16 dipelopori oleh", "Martin Luther", "Yohanes Calvin saja", "Paus Leo X saja", "Konstantinus saja"], ["Gerakan reformasi gereja melahirkan aliran Kristen Protestan dan tetap adanya", "Gereja Katolik Roma", "Gereja Ortodoks saja", "Gereja Anglikan saja", "Tidak ada gereja lain"], ["Konsep sola scriptura dalam teologi reformasi menekankan", "Alkitab sebagai satu-satunya sumber otoritas iman", "Tradisi gereja sebagai sumber utama", "Perkataan pemimpin gereja", "Adat istiadat setempat"], ["Konsep sola fide menekankan bahwa keselamatan diperoleh melalui", "Iman semata", "Perbuatan baik semata", "Kekayaan", "Status sosial"], ["Konsep sola gratia menekankan bahwa keselamatan adalah", "Anugerah Allah semata", "Hasil usaha manusia", "Warisan keluarga", "Pencapaian pribadi"], ["Etika Kristen dalam menghadapi isu sosial menekankan pentingnya", "Keadilan dan kasih terhadap sesama", "Individualisme", "Ketidakpedulian sosial", "Kompetisi tanpa batas"], ["Pandangan Kristen tentang martabat manusia menekankan bahwa manusia diciptakan", "Segambar dan serupa dengan Allah", "Tanpa nilai khusus", "Sama seperti benda mati", "Untuk dieksploitasi"], ["Konsep panggilan (vokasi) dalam iman Kristen berarti", "Setiap pekerjaan dapat menjadi sarana melayani Tuhan", "Hanya pelayanan gerejawi yang bernilai", "Pekerjaan duniawi tidak penting", "Hanya biarawan yang memiliki panggilan"], ["Tanggung jawab Kristen terhadap lingkungan hidup disebut", "Pengelolaan ciptaan (stewardship)", "Eksploitasi ciptaan", "Pengabaian ciptaan", "Perusakan ciptaan"], ["Dialog antaragama dalam konteks Kristen bertujuan untuk", "Membangun toleransi dan saling pengertian", "Memaksakan keyakinan", "Menghindari interaksi", "Menimbulkan konflik"], ["Konsep gereja yang am (universal) menekankan bahwa gereja", "Mencakup seluruh umat percaya di segala tempat dan waktu", "Hanya terbatas pada satu daerah", "Hanya untuk kalangan tertentu", "Tidak memiliki kesatuan"], ["Sakramen dalam tradisi Protestan umumnya diakui ada dua yaitu Baptisan dan", "Perjamuan Kudus", "Pengakuan dosa", "Pengurapan orang sakit", "Imamat"], ["Konsep pemuridan (discipleship) dalam iman Kristen menekankan proses", "Bertumbuh dalam iman dan mengikuti teladan Kristus", "Hanya menghadiri ibadah rutin", "Mencari status sosial", "Menghindari komunitas gereja"], ["Etika Kristen memandang pekerjaan sebagai bagian dari", "Tanggung jawab dan ibadah kepada Tuhan", "Beban semata", "Hukuman", "Kegiatan tanpa makna"], ["Isu bioetika dalam pandangan Kristen menekankan pentingnya", "Menghormati kehidupan manusia", "Mengabaikan nilai kehidupan", "Mengutamakan kepentingan pribadi", "Mengabaikan etika medis"], ["Konsep kerajaan Allah dalam pengajaran Yesus menekankan", "Pemerintahan Allah yang penuh kasih dan keadilan", "Kerajaan duniawi semata", "Kekuasaan politik tertentu", "Sistem ekonomi tertentu"], ["Peran orang Kristen sebagai garam dan terang dunia berarti", "Memberi pengaruh positif bagi masyarakat", "Mengasingkan diri dari masyarakat", "Mendominasi masyarakat", "Mengabaikan tanggung jawab sosial"], ["Konsep pengampunan dalam iman Kristen mengajarkan untuk", "Mengampuni sesama seperti Allah mengampuni", "Membalas kejahatan dengan kejahatan", "Menyimpan dendam", "Menghindari rekonsiliasi"], ["Peran keluarga Kristen dalam pendidikan iman anak sangat penting sebagai", "Gereja rumah tangga (gereja kecil)", "Institusi ekonomi semata", "Tempat tanpa nilai spiritual", "Pilihan yang tidak wajib"], ["Nilai kejujuran dan integritas dalam kepemimpinan Kristen tercermin dalam konsep", "Kepemimpinan yang melayani (servant leadership)", "Kepemimpinan otoriter", "Kepemimpinan tanpa tanggung jawab", "Kepemimpinan berbasis kekuasaan semata"], ["Dampak positif iman Kristen terhadap kehidupan sosial dapat berupa", "Pelayanan pendidikan dan kesehatan bagi masyarakat", "Eksklusivitas sosial", "Diskriminasi", "Isolasi komunitas"], ["Sikap kritis namun santun terhadap perkembangan zaman diajarkan Kristen melalui prinsip", "Hidup di dunia namun berpegang pada nilai iman", "Menolak seluruh perkembangan zaman", "Mengikuti tren tanpa filter", "Mengabaikan nilai moral"], ["Konsep kasih tanpa syarat (agape) dalam etika Kristen mendorong sikap", "Mengasihi bahkan kepada musuh", "Mengasihi hanya kepada keluarga", "Mengasihi dengan pamrih", "Mengasihi berdasarkan keuntungan"], ["Peran gereja dalam masyarakat modern mencakup pelayanan spiritual dan", "Tanggung jawab sosial kemanusiaan", "Kegiatan politik praktis semata", "Kegiatan bisnis semata", "Isolasi dari masyarakat"], ["Pendidikan Agama Kristen di sekolah bertujuan membentuk siswa yang beriman dan", "Berakhlak mulia dalam kehidupan bermasyarakat", "Eksklusif terhadap agama lain", "Mengabaikan nilai sosial", "Tidak peduli terhadap sesama"]],
                        },
                        "Pendidikan Agama Hindu": {
                            "SD": [["Kitab suci umat Hindu disebut", "Weda", "Al-Qur'an", "Alkitab", "Tripitaka"], ["Tempat ibadah umat Hindu disebut", "Pura", "Masjid", "Gereja", "Wihara"], ["Konsep keyakinan dasar umat Hindu disebut", "Panca Sradha", "Rukun Iman", "Dasa Titah", "Tri Ratna"], ["Jumlah keyakinan dasar dalam Panca Sradha ada", "Lima", "Empat", "Enam", "Tiga"], ["Keyakinan pertama dalam Panca Sradha adalah percaya kepada", "Brahman (Tuhan Yang Maha Esa)", "Roh leluhur saja", "Alam semesta saja", "Diri sendiri saja"], ["Konsep Tuhan Yang Maha Esa dalam ajaran Hindu disebut", "Brahman", "Atman", "Karma", "Dharma"], ["Percikan Tuhan yang ada dalam setiap makhluk hidup disebut", "Atman", "Brahman", "Karma", "Moksa"], ["Hukum sebab akibat perbuatan dalam ajaran Hindu disebut", "Karma phala", "Dharma", "Moksa", "Punarbhawa"], ["Kelahiran kembali (reinkarnasi) dalam ajaran Hindu disebut", "Punarbhawa", "Karma", "Dharma", "Moksa"], ["Kebebasan tertinggi dari siklus kelahiran dan kematian disebut", "Moksa", "Karma", "Dharma", "Punarbhawa"], ["Kewajiban dan kebenaran yang harus dijalankan manusia disebut", "Dharma", "Karma", "Moksa", "Punarbhawa"], ["Perayaan hari suci untuk memperingati kemenangan kebaikan atas kejahatan disebut", "Hari Raya Galungan", "Hari Raya Nyepi", "Hari Raya Saraswati", "Hari Raya Kuningan"], ["Hari raya umat Hindu yang dirayakan dengan sehari penuh tanpa aktivitas disebut", "Hari Raya Nyepi", "Hari Raya Galungan", "Hari Raya Kuningan", "Hari Raya Saraswati"], ["Hari raya untuk memuliakan ilmu pengetahuan dalam ajaran Hindu disebut", "Hari Raya Saraswati", "Hari Raya Nyepi", "Hari Raya Galungan", "Hari Raya Pagerwesi"], ["Sesajen yang dipersembahkan umat Hindu sehari-hari disebut", "Canang sari", "Tumpeng", "Ogoh-ogoh saja", "Wayang"], ["Patung besar yang diarak menjelang Hari Raya Nyepi disebut", "Ogoh-ogoh", "Canang sari", "Sesaji", "Wayang"], ["Konsep keseimbangan hubungan manusia dengan Tuhan, sesama, dan alam disebut", "Tri Hita Karana", "Panca Sradha", "Catur Marga", "Dasa Titah"], ["Tiga kerangka dasar ajaran Hindu adalah Tattwa, Susila, dan", "Upacara", "Weda saja", "Karma saja", "Dharma saja"], ["Bagian ajaran Hindu tentang filsafat dan keyakinan disebut", "Tattwa", "Susila", "Upacara", "Yadnya"], ["Bagian ajaran Hindu tentang etika dan perilaku disebut", "Susila", "Tattwa", "Upacara", "Karma"], ["Bagian ajaran Hindu tentang ritual dan persembahan disebut", "Upacara/Yadnya", "Tattwa", "Susila", "Dharma"], ["Persembahan suci yang tulus ikhlas dalam ajaran Hindu disebut", "Yadnya", "Karma saja", "Dharma saja", "Moksa saja"], ["Tempat pemujaan keluarga di rumah umat Hindu di Bali disebut", "Sanggah/merajan", "Pura besar saja", "Wihara", "Gereja"], ["Doa yang biasa diucapkan umat Hindu sebelum kegiatan disebut", "Puja Tri Sandya", "Doa Bapa Kami", "Doa Rosario", "Doa syahadat"], ["Tarian sakral yang biasa dipentaskan dalam upacara keagamaan Hindu di Bali misalnya", "Tari Rejang", "Tari Saman", "Tari Piring", "Tari Jaipong"], ["Sikap menghormati orang tua dan guru dalam ajaran Hindu termasuk bagian dari", "Susila (etika)", "Upacara", "Tattwa", "Karma buruk"], ["Kitab yang berisi kisah kepahlawanan dan nilai moral dalam tradisi Hindu misalnya", "Ramayana dan Mahabharata", "Kejadian", "Kisah Para Rasul", "Wahyu"], ["Tokoh dalam kisah Ramayana yang dikenal sebagai raja yang setia dan bijaksana adalah", "Rama", "Rahwana", "Kresna", "Arjuna"], ["Tokoh dalam kisah Mahabharata yang dikenal sebagai penasihat bijaksana adalah", "Kresna", "Rahwana", "Hanoman", "Sinta"], ["Sikap berbuat baik tanpa mengharap imbalan dalam ajaran Hindu disebut", "Sevanam/pengabdian tulus", "Keserakahan", "Kesombongan", "Kebencian"]],
                            "SMP": [["Kitab suci Weda terdiri dari empat bagian utama yaitu Reg, Yajur, Sama, dan", "Atharwa Weda", "Upanisad saja", "Purana saja", "Itihasa saja"], ["Kitab Weda yang berisi kumpulan syair pujian disebut", "Reg Weda", "Yajur Weda", "Sama Weda", "Atharwa Weda"], ["Kitab Weda yang berisi mantra pengorbanan disebut", "Yajur Weda", "Reg Weda", "Sama Weda", "Atharwa Weda"], ["Kitab Weda yang berisi kumpulan nyanyian pujian disebut", "Sama Weda", "Reg Weda", "Yajur Weda", "Atharwa Weda"], ["Kitab suci tambahan yang berisi filsafat mendalam tentang Weda disebut", "Upanisad", "Purana", "Itihasa", "Dharmasastra"], ["Kitab yang berisi kisah kepahlawanan seperti Ramayana dan Mahabharata disebut", "Itihasa", "Purana", "Upanisad", "Dharmasastra"], ["Kitab yang berisi hukum dan tata cara kehidupan umat Hindu disebut", "Dharmasastra", "Itihasa", "Purana", "Upanisad"], ["Empat jalan untuk mencapai tujuan hidup (Catur Marga) meliputi Bhakti, Karma, Jnana, dan", "Yoga", "Dharma saja", "Moksa saja", "Tattwa saja"], ["Jalan pengabdian dan cinta kasih kepada Tuhan disebut", "Bhakti marga", "Karma marga", "Jnana marga", "Yoga marga"], ["Jalan mencapai Tuhan melalui perbuatan tanpa pamrih disebut", "Karma marga", "Bhakti marga", "Jnana marga", "Yoga marga"], ["Jalan mencapai Tuhan melalui pengetahuan dan kebijaksanaan disebut", "Jnana marga", "Bhakti marga", "Karma marga", "Yoga marga"], ["Jalan mencapai Tuhan melalui pengendalian diri dan meditasi disebut", "Yoga marga", "Bhakti marga", "Karma marga", "Jnana marga"], ["Tujuan akhir hidup manusia dalam ajaran Hindu disebut Catur Purusartha yang meliputi Dharma, Artha, Kama, dan", "Moksa", "Karma saja", "Yadnya saja", "Susila saja"], ["Tujuan hidup untuk memenuhi kebutuhan materi disebut", "Artha", "Dharma", "Kama", "Moksa"], ["Tujuan hidup untuk memenuhi keinginan dan kesenangan disebut", "Kama", "Dharma", "Artha", "Moksa"], ["Lima jenis persembahan suci (Panca Yadnya) meliputi Dewa Yadnya, Pitra Yadnya, Rsi Yadnya, Manusa Yadnya, dan", "Bhuta Yadnya", "Homa Yadnya saja", "Yoga Yadnya saja", "Tapa Yadnya saja"], ["Persembahan kepada Tuhan disebut", "Dewa Yadnya", "Pitra Yadnya", "Rsi Yadnya", "Bhuta Yadnya"], ["Persembahan kepada leluhur disebut", "Pitra Yadnya", "Dewa Yadnya", "Rsi Yadnya", "Manusa Yadnya"], ["Persembahan kepada para guru suci dan orang bijaksana disebut", "Rsi Yadnya", "Dewa Yadnya", "Pitra Yadnya", "Bhuta Yadnya"], ["Upacara potong gigi dalam tradisi Hindu Bali disebut", "Mepandes/metatah", "Ngaben", "Otonan", "Melasti"], ["Upacara pembakaran jenazah dalam tradisi Hindu Bali disebut", "Ngaben", "Mepandes", "Otonan", "Melasti"], ["Upacara penyucian diri dan sarana upacara menjelang Nyepi disebut", "Melasti", "Ngaben", "Mepandes", "Otonan"], ["Perayaan hari kelahiran menurut wuku dalam tradisi Bali disebut", "Otonan", "Ngaben", "Melasti", "Mepandes"], ["Sistem pembagian tugas dalam masyarakat menurut ajaran Hindu klasik disebut", "Catur Warna", "Catur Marga", "Catur Purusartha", "Catur Asrama"], ["Empat tahapan kehidupan manusia (Catur Asrama) meliputi Brahmacari, Grahasta, Wanaprasta, dan", "Bhiksuka/Sanyasin", "Yadnya saja", "Dharma saja", "Moksa saja"], ["Tahap kehidupan menuntut ilmu dalam Catur Asrama disebut", "Brahmacari", "Grahasta", "Wanaprasta", "Bhiksuka"], ["Tahap kehidupan berumah tangga dalam Catur Asrama disebut", "Grahasta", "Brahmacari", "Wanaprasta", "Bhiksuka"], ["Konsep Tri Kaya Parisudha mengajarkan tiga hal yang harus disucikan yaitu pikiran, perkataan, dan", "Perbuatan", "Perasaan saja", "Keinginan saja", "Ambisi saja"], ["Sikap ahimsa dalam ajaran Hindu berarti", "Tanpa kekerasan", "Kebencian", "Balas dendam", "Kesombongan"], ["Konsep satya dalam ajaran Hindu menekankan pentingnya", "Kejujuran dan kebenaran", "Kebohongan", "Keserakahan", "Kemalasan"]],
                            "SMA": [["Filsafat Hindu yang mengkaji hakikat realitas disebut filsafat", "Tattwa/Darsana", "Susila saja", "Upacara saja", "Yadnya saja"], ["Enam sistem filsafat Hindu klasik disebut", "Sad Darsana", "Panca Sradha", "Catur Marga", "Tri Hita Karana"], ["Konsep penyatuan Atman dengan Brahman merupakan tujuan tertinggi berupa", "Moksa", "Karma saja", "Dharma saja", "Yadnya saja"], ["Hukum kekekalan energi dan sebab akibat perbuatan yang menentukan kelahiran kembali disebut", "Hukum Karma", "Hukum Dharma saja", "Hukum Yadnya saja", "Hukum Tattwa saja"], ["Konsep siklus kelahiran, kehidupan, dan kematian yang berulang disebut", "Samsara", "Moksa", "Dharma", "Yadnya"], ["Konsep Tri Hita Karana menekankan keharmonisan antara manusia dengan Tuhan, manusia dengan manusia, dan manusia dengan", "Alam lingkungan", "Diri sendiri saja", "Harta benda saja", "Kekuasaan saja"], ["Konsep Tri Murti dalam ajaran Hindu terdiri dari Brahma, Wisnu, dan", "Siwa", "Ganesha saja", "Indra saja", "Surya saja"], ["Dewa pencipta dalam konsep Tri Murti adalah", "Brahma", "Wisnu", "Siwa", "Indra"], ["Dewa pemelihara dalam konsep Tri Murti adalah", "Wisnu", "Brahma", "Siwa", "Ganesha"], ["Dewa pelebur/pemralina dalam konsep Tri Murti adalah", "Siwa", "Brahma", "Wisnu", "Indra"], ["Konsep etika Hindu yang mengajarkan pengendalian diri melalui yoga terangkum dalam kitab", "Yoga Sutra Patanjali", "Weda Reg saja", "Dharmasastra saja", "Purana saja"], ["Delapan tahapan yoga (Astangga Yoga) diawali dengan Yama dan", "Niyama", "Asana saja", "Dhyana saja", "Samadhi saja"], ["Tahap akhir dalam Astangga Yoga yang merupakan penyatuan sempurna disebut", "Samadhi", "Yama", "Niyama", "Pratyahara"], ["Konsep kepemimpinan ideal dalam ajaran Hindu disebut", "Asta Brata", "Catur Warna", "Catur Marga", "Tri Hita Karana"], ["Asta Brata mengajarkan pemimpin meneladani sifat delapan unsur alam seperti matahari dan", "Bulan, bumi, angin, dan lainnya", "Hanya api saja", "Hanya air saja", "Hanya angin saja"], ["Etika sosial dalam ajaran Hindu menekankan konsep Wasudewa Kutumbakam yang berarti", "Semua makhluk bersaudara", "Persaingan antarmanusia", "Individualisme", "Eksklusivitas kelompok"], ["Ajaran Hindu tentang pelestarian lingkungan tercermin dalam konsep", "Tri Hita Karana", "Catur Warna saja", "Catur Asrama saja", "Panca Sradha saja"], ["Konsep karma dibedakan menjadi tiga yaitu Sancita, Prarabda, dan", "Kriyamana", "Wasana saja", "Samsara saja", "Dharma saja"], ["Karma yang sedang dijalani pada kehidupan sekarang disebut", "Prarabda karma", "Sancita karma", "Kriyamana karma", "Wasana karma"], ["Karma yang sedang dilakukan dan akan berbuah di kemudian hari disebut", "Kriyamana karma", "Prarabda karma", "Sancita karma", "Wasana karma"], ["Peran pura sebagai pusat kegiatan keagamaan dan sosial masyarakat Hindu mencerminkan konsep", "Desa Kala Patra (kontekstualisasi ajaran)", "Isolasi keagamaan", "Eksklusivitas ritual", "Individualisme spiritual"], ["Konsep Desa Kala Patra dalam pelaksanaan ajaran Hindu menekankan penyesuaian dengan", "Tempat, waktu, dan keadaan", "Aturan yang kaku tanpa perubahan", "Tradisi luar negeri", "Kepentingan pribadi semata"], ["Sistem pendidikan tradisional Hindu yang menekankan hubungan guru dan murid disebut", "Guru Kula", "Grahasta saja", "Wanaprasta saja", "Bhiksuka saja"], ["Tri Rna dalam ajaran Hindu mengajarkan tiga hutang manusia yaitu kepada Tuhan, leluhur, dan", "Guru/orang bijaksana", "Diri sendiri saja", "Harta benda saja", "Kekuasaan saja"], ["Toleransi antarumat beragama dalam perspektif Hindu tercermin dalam semboyan", "Tat Twam Asi (aku adalah engkau)", "Persaingan keyakinan", "Eksklusivitas kelompok", "Penolakan perbedaan"], ["Konsep kebahagiaan sejati dalam filsafat Hindu dicapai melalui", "Keseimbangan lahir dan batin", "Kekayaan materi semata", "Kekuasaan semata", "Popularitas semata"], ["Peran umat Hindu dalam menjaga kerukunan bangsa tercermin dalam sikap", "Toleransi dan gotong royong", "Eksklusivitas sosial", "Fanatisme sempit", "Individualisme"], ["Perkembangan ajaran Hindu di Indonesia banyak dipengaruhi oleh kebudayaan", "Lokal Nusantara yang berakulturasi", "Tanpa akulturasi budaya lokal", "Budaya Barat modern", "Budaya Timur Tengah"], ["Kerajaan Hindu tertua di Nusantara adalah", "Kutai", "Majapahit", "Mataram Kuno", "Sriwijaya"], ["Nilai-nilai kearifan lokal Hindu di Bali turut mendukung pelestarian", "Budaya dan lingkungan", "Konflik sosial", "Individualisme", "Eksploitasi alam"]],
                        },
                        "Pendidikan Pancasila": {
                            "SD": [["Pancasila terdiri dari berapa sila","5 sila","4 sila","6 sila","3 sila"],["Lambang sila pertama Pancasila adalah","Bintang","Rantai","Pohon beringin","Kepala banteng"],["Lambang sila kedua Pancasila adalah","Rantai","Bintang","Pohon beringin","Padi dan kapas"],["Lambang sila ketiga Pancasila adalah","Pohon beringin","Bintang","Rantai","Kepala banteng"],["Lambang sila keempat Pancasila adalah","Kepala banteng","Bintang","Rantai","Padi dan kapas"],["Lambang sila kelima Pancasila adalah","Padi dan kapas","Bintang","Rantai","Pohon beringin"],["Bunyi sila pertama Pancasila adalah","Ketuhanan Yang Maha Esa","Kemanusiaan yang adil dan beradab","Persatuan Indonesia","Keadilan sosial"],["Bunyi sila kedua Pancasila adalah","Kemanusiaan yang adil dan beradab","Ketuhanan Yang Maha Esa","Persatuan Indonesia","Kerakyatan"],["Bunyi sila ketiga Pancasila adalah","Persatuan Indonesia","Ketuhanan Yang Maha Esa","Kemanusiaan yang adil dan beradab","Keadilan sosial"],["Bunyi sila kelima Pancasila adalah","Keadilan sosial bagi seluruh rakyat Indonesia","Ketuhanan Yang Maha Esa","Persatuan Indonesia","Kerakyatan"],["Pancasila disahkan sebagai dasar negara pada tanggal","18 Agustus 1945","17 Agustus 1945","1 Juni 1945","28 Oktober 1928"],["Hari Lahir Pancasila diperingati setiap tanggal","1 Juni","18 Agustus","17 Agustus","28 Oktober"],["Tokoh yang mengusulkan istilah Pancasila adalah","Ir. Soekarno","Moh. Hatta","Moh. Yamin","Soepomo"],["Semboyan bangsa Indonesia yang berarti berbeda-beda tetapi tetap satu adalah","Bhinneka Tunggal Ika","Garuda Pancasila","Merdeka atau mati","Bersatu kita teguh"],["Burung yang menjadi lambang negara Indonesia adalah","Garuda","Elang","Merak","Cendrawasih"],["Sikap saling menghormati antarumat beragama merupakan pengamalan sila ke","1","2","3","4"],["Sikap gotong royong membantu tetangga merupakan pengamalan sila ke","3","1","2","5"],["Sikap bermusyawarah untuk mencapai mufakat merupakan pengamalan sila ke","4","1","2","3"],["Sikap tidak membeda-bedakan teman merupakan pengamalan sila ke","2","1","3","4"],["Sikap menghargai hasil kerja keras orang lain merupakan pengamalan sila ke","5","1","2","3"],["Pancasila berfungsi sebagai dasar negara dan","Pandangan hidup bangsa","Lagu kebangsaan","Bahasa nasional","Bendera negara"],["Nilai yang terkandung dalam sila ketiga Pancasila adalah","Persatuan dan kesatuan","Keadilan sosial","Musyawarah mufakat","Ketuhanan"],["Perilaku rukun dengan teman yang berbeda agama mencerminkan sila","Pertama","Kedua","Ketiga","Kelima"],["Simbol rantai pada Pancasila melambangkan","Hubungan manusia yang saling membutuhkan","Persatuan bangsa","Kedaulatan rakyat","Keadilan sosial"],["Nilai kekeluargaan dalam mengambil keputusan bersama termasuk pengamalan sila","Keempat","Pertama","Kedua","Ketiga"],["Menjaga kebersihan lingkungan bersama tetangga adalah contoh sila","Ketiga","Kedua","Keempat","Kelima"],["Membantu teman yang kesusahan tanpa membeda-bedakan adalah pengamalan sila","Kedua","Pertama","Ketiga","Kelima"],["Pancasila sebagai dasar negara tercantum dalam pembukaan","UUD 1945","Piagam Jakarta saja","Sumpah Pemuda","Proklamasi"],["Sikap tenggang rasa dan tepa selira mencerminkan pengamalan sila","Kedua","Pertama","Ketiga","Keempat"],["Menghormati keputusan hasil musyawarah kelas adalah pengamalan sila","Keempat","Pertama","Kedua","Kelima"],["Rajin menabung dan tidak boros mencerminkan sikap adil yang termasuk sila","Kelima","Pertama","Kedua","Ketiga"]],
                            "SMP": [["Pancasila digali dari nilai-nilai luhur","Budaya bangsa Indonesia","Budaya asing","Ideologi lain","Adat negara lain"],["Piagam Jakarta dirumuskan oleh","Panitia Sembilan","BPUPKI seluruhnya","PPKI seluruhnya","KNIP"],["Sidang pertama BPUPKI membahas","Dasar negara","Bentuk pemerintahan","Wilayah negara","Undang-undang"],["Ketua BPUPKI adalah","Radjiman Wedyodiningrat","Ir. Soekarno","Moh. Hatta","Soepomo"],["PPKI mengesahkan Pancasila dan UUD 1945 pada tanggal","18 Agustus 1945","17 Agustus 1945","1 Juni 1945","22 Juni 1945"],["Pancasila berkedudukan sebagai sumber dari segala sumber","Hukum negara","Ekonomi negara","Budaya negara","Pendidikan negara"],["Pancasila bersifat terbuka artinya","Dapat menyesuaikan perkembangan zaman tanpa mengubah nilai dasarnya","Dapat diganti sewaktu-waktu","Tertutup dari pengaruh luar","Tidak dapat diamalkan"],["Nilai dasar Pancasila bersifat","Tetap dan tidak berubah","Berubah sesuai keinginan","Fleksibel sepenuhnya","Ditentukan pemerintah saja"],["Ideologi Pancasila berbeda dengan liberalisme karena Pancasila menekankan","Keseimbangan hak dan kewajiban","Kebebasan individu mutlak","Dominasi negara penuh","Kepemilikan bersama total"],["Ideologi Pancasila berbeda dengan komunisme karena Pancasila mengakui","Keberadaan Tuhan dan agama","Sistem satu partai","Penghapusan hak milik pribadi","Ateisme negara"],["Contoh penerapan nilai Pancasila dalam kehidupan berbangsa adalah","Menjaga persatuan antarsuku dan agama","Memaksakan kehendak","Bersikap individualis","Mengabaikan musyawarah"],["Norma yang bersumber dari Pancasila dan mengatur kehidupan bernegara disebut norma","Hukum","Agama saja","Kesopanan saja","Kesusilaan saja"],["Pancasila sebagai ideologi terbuka mampu beradaptasi dengan","Perkembangan zaman","Ideologi lain yang bertentangan","Budaya asing tanpa filter","Kepentingan kelompok tertentu"],["Sila keempat Pancasila menekankan sistem demokrasi yang berlandaskan","Musyawarah mufakat","Suara terbanyak mutlak","Keputusan sepihak","Kekuasaan mutlak"],["Semangat persatuan dalam keberagaman suku, agama, dan budaya sesuai dengan sila","Ketiga","Pertama","Kedua","Kelima"],["Sikap menghargai perbedaan pendapat dalam musyawarah mencerminkan sila","Keempat","Pertama","Kedua","Ketiga"],["Keadilan sosial dalam Pancasila bertujuan mewujudkan","Kesejahteraan seluruh rakyat","Kekayaan kelompok tertentu","Kesenjangan sosial","Persaingan bebas tanpa batas"],["Fungsi Pancasila sebagai pandangan hidup bangsa berarti Pancasila menjadi","Pedoman dalam bersikap dan bertingkah laku","Sekadar simbol negara","Materi pelajaran saja","Slogan semata"],["Sikap cinta tanah air dan rela berkorban untuk bangsa mencerminkan nilai","Nasionalisme Pancasila","Individualisme","Liberalisme","Sekularisme"],["Toleransi antarumat beragama merupakan wujud pengamalan sila","Pertama","Kedua","Ketiga","Keempat"],["Upaya menjaga keutuhan Negara Kesatuan Republik Indonesia adalah wujud pengamalan sila","Ketiga","Pertama","Kedua","Kelima"],["Sikap mengutamakan kepentingan bangsa di atas kepentingan pribadi mencerminkan sila","Ketiga","Pertama","Kedua","Keempat"],["Penerapan keadilan dalam pembagian hasil kerja kelompok mencerminkan sila","Kelima","Pertama","Kedua","Ketiga"],["Nilai gotong royong yang menjadi ciri khas budaya Indonesia sesuai dengan sila","Ketiga","Pertama","Kedua","Kelima"],["Menghormati hak asasi manusia setiap warga negara mencerminkan sila","Kedua","Pertama","Ketiga","Kelima"],["Pancasila sebagai dasar negara berfungsi untuk","Mengatur penyelenggaraan negara","Mengatur ibadah pribadi","Menentukan mata pencaharian","Mengatur pertemanan"],["Contoh pelanggaran nilai Pancasila adalah","Melakukan diskriminasi terhadap kelompok tertentu","Bermusyawarah untuk mufakat","Membantu korban bencana","Membayar pajak tepat waktu"],["Sikap adil terhadap sesama tanpa memandang status sosial mencerminkan sila","Kelima","Pertama","Kedua","Ketiga"],["Wujud nyata persatuan dalam keberagaman budaya Indonesia disebut","Bhinneka Tunggal Ika","Trisila","Ekasila","Panca Dharma"],["Kewajiban warga negara dalam menjaga keamanan lingkungan termasuk pengamalan sila","Ketiga","Pertama","Kedua","Kelima"]],
                            "SMA": [["Pancasila sebagai ideologi negara berfungsi sebagai","Cita-cita dan pedoman bernegara","Sekadar teori politik","Ajaran agama tertentu","Peraturan daerah"],["Rumusan Pancasila yang sah dan resmi termuat dalam","Pembukaan UUD 1945","Piagam Jakarta","Pidato 1 Juni 1945","Dekrit Presiden 1959"],["Trias Politika bukan bagian dari sistem Pancasila, melainkan konsep pemisahan kekuasaan dari","Montesquieu","Soekarno","Soepomo","Moh. Hatta"],["Pancasila sebagai ideologi terbuka memiliki tiga dimensi yaitu realita, idealisme, dan","Fleksibilitas","Absolutisme","Radikalisme","Otoritarianisme"],["Implementasi Pancasila dalam sistem ekonomi Indonesia tercermin dalam konsep","Ekonomi kerakyatan","Ekonomi liberal murni","Ekonomi komunis","Ekonomi feodal"],["Pasal dalam UUD 1945 yang mengatur tentang hak asasi manusia mencerminkan pengamalan sila","Kedua","Pertama","Ketiga","Keempat"],["Konsep negara hukum yang dianut Indonesia sesuai dengan nilai Pancasila tercantum pada","Pasal 1 ayat (3) UUD 1945","Pasal 27 UUD 1945","Pasal 33 UUD 1945","Pasal 29 UUD 1945"],["Sila keempat Pancasila menjadi dasar sistem pemerintahan yang bersifat","Demokratis","Otoriter","Monarki","Oligarki"],["Dekrit Presiden 5 Juli 1959 berkaitan dengan","Kembali ke UUD 1945","Perubahan dasar negara","Penghapusan Pancasila","Pembentukan konstitusi baru"],["Tantangan penerapan Pancasila di era globalisasi antara lain","Masuknya budaya asing yang tidak sesuai nilai luhur bangsa","Meningkatnya rasa nasionalisme","Menguatnya gotong royong","Bertambahnya toleransi"],["Radikalisme dan intoleransi merupakan ancaman terhadap pengamalan sila","Pertama","Kedua","Ketiga","Kelima"],["Korupsi merupakan pelanggaran terhadap nilai Pancasila terutama sila","Kelima","Pertama","Kedua","Ketiga"],["Pancasila sebagai sumber hukum tertinggi berarti seluruh peraturan perundang-undangan harus","Sesuai dan tidak bertentangan dengan Pancasila","Dibuat oleh presiden saja","Mengikuti hukum internasional saja","Ditentukan oleh partai politik"],["Konsep hak dan kewajiban warga negara seimbang sesuai dengan sila","Kedua","Pertama","Ketiga","Kelima"],["Sistem multipartai di Indonesia merupakan wujud demokrasi sesuai sila","Keempat","Pertama","Kedua","Ketiga"],["Upaya menjaga integrasi nasional di tengah keberagaman disebut","Persatuan dalam kebinekaan","Disintegrasi","Sekularisasi","Separatisme"],["Nilai instrumental Pancasila diwujudkan dalam bentuk","Peraturan perundang-undangan","Nilai dasar yang abadi","Perasaan pribadi","Adat istiadat semata"],["Nilai praksis Pancasila tercermin dalam","Pengamalan nyata dalam kehidupan sehari-hari","Teori semata","Rumusan tertulis saja","Simbol negara saja"],["Ancaman disintegrasi bangsa dapat diatasi dengan penguatan nilai","Persatuan Indonesia","Individualisme","Sektarianisme","Liberalisme ekonomi"],["Prinsip keadilan sosial dalam Pancasila menghendaki pemerataan","Kesejahteraan bagi seluruh rakyat","Kekayaan bagi kelompok elite","Kekuasaan bagi partai tertentu","Pendidikan bagi kota besar saja"],["Konsep negara kesatuan berbentuk republik sesuai dengan nilai Pancasila diatur dalam","Pasal 1 ayat (1) UUD 1945","Pasal 27 UUD 1945","Pasal 31 UUD 1945","Pasal 34 UUD 1945"],["Wawasan Nusantara sebagai cara pandang bangsa Indonesia bersumber dari nilai","Persatuan dan kesatuan","Kepentingan pribadi","Kepentingan golongan","Kepentingan asing"],["Ketahanan nasional Indonesia dibangun berdasarkan nilai-nilai","Pancasila","Ideologi asing","Kepentingan ekonomi semata","Kekuatan militer semata"],["Sikap kritis terhadap kebijakan pemerintah yang tetap menghormati proses demokrasi mencerminkan sila","Keempat","Pertama","Kedua","Ketiga"],["Upaya bela negara oleh setiap warga negara merupakan wujud pengamalan sila","Ketiga","Pertama","Kedua","Kelima"],["Prinsip musyawarah mufakat dalam pengambilan keputusan publik mencerminkan nilai demokrasi","Pancasila","Liberal","Komunis","Otoriter"],["Isu intoleransi dan ujaran kebencian di media sosial menjadi tantangan pengamalan sila","Pertama dan kedua","Ketiga dan keempat","Kelima saja","Tidak ada kaitannya"],["Konsep negara kesejahteraan yang dianut Indonesia bertujuan mewujudkan","Keadilan sosial bagi seluruh rakyat","Kekayaan negara semata","Kekuasaan pemerintah pusat","Persaingan bebas tanpa batas"],["Peran generasi muda dalam menjaga keutuhan NKRI dapat diwujudkan melalui","Penguatan wawasan kebangsaan dan cinta tanah air","Sikap apatis politik","Individualisme digital","Ketergantungan pada budaya asing"],["Reformasi 1998 menuntut penguatan nilai demokrasi dan penegakan","Hukum dan HAM sesuai Pancasila","Kekuasaan militer","Sistem satu partai","Ekonomi tertutup"]]
                        },
                        "Bahasa Arab": {
                            "1": {
                                "Mudah": [["Huruf pertama dalam hijaiyah adalah", "Alif", "Ba", "Ta", "Jim"], ["Huruf kedua dalam hijaiyah adalah", "Ba", "Alif", "Tsa", "Dal"], ["Huruf ketiga dalam hijaiyah adalah", "Ta", "Ba", "Jim", "Kha"], ["Angka satu dalam bahasa Arab adalah", "Wahid", "Itsnan", "Tsalatsah", "Arba'ah"], ["Angka dua dalam bahasa Arab adalah", "Itsnan", "Wahid", "Khamsah", "Sittah"], ["Warna Ahmar berarti", "Merah", "Biru", "Hijau", "Kuning"]],
                                "Sedang": [["Huruf keempat dalam hijaiyah adalah", "Tsa", "Jim", "Kha", "Dal"], ["Huruf kelima dalam hijaiyah adalah", "Jim", "Tsa", "Ha", "Kha"], ["Angka tiga dalam bahasa Arab adalah", "Tsalatsah", "Arba'ah", "Khamsah", "Itsnan"], ["Angka empat dalam bahasa Arab adalah", "Arba'ah", "Tsalatsah", "Khamsah", "Wahid"], ["Warna Azraq berarti", "Biru", "Merah", "Hitam", "Putih"], ["Arti kata Bait adalah", "Rumah", "Sekolah", "Pasar", "Masjid"]],
                                "Sulit": [["Angka lima dalam bahasa Arab adalah", "Khamsah", "Sittah", "Arba'ah", "Wahid"], ["Arti kata Kitab adalah", "Buku", "Pena", "Meja", "Tas"], ["Arti kata Qalam adalah", "Pena", "Buku", "Papan tulis", "Penghapus"], ["Warna Akhdar berarti", "Hijau", "Kuning", "Biru", "Merah"], ["Warna Aswad berarti", "Hitam", "Putih", "Hijau", "Biru"], ["Ucapan salam dalam bahasa Arab adalah", "Assalamu'alaikum", "Marhaban", "Syukron", "Afwan"]]
                            },
                            "2": {
                                "Mudah": [["Balasan salam yang benar adalah", "Wa'alaikumussalam", "Ahlan wa sahlan", "Ma'as salamah", "Jazakallah"], ["Angka enam dalam bahasa Arab adalah", "Sittah", "Sab'ah", "Tsamaniyah", "Tis'ah"], ["Angka tujuh dalam bahasa Arab adalah", "Sab'ah", "Sittah", "Tsamaniyah", "Asyarah"], ["Arti kata Baab adalah", "Pintu", "Jendela", "Atap", "Lantai"], ["Arti kata Syams adalah", "Matahari", "Bulan", "Bintang", "Awan"], ["Warna Abyad berarti", "Putih", "Hitam", "Merah", "Kuning"]],
                                "Sedang": [["Angka delapan dalam bahasa Arab adalah", "Tsamaniyah", "Sab'ah", "Tis'ah", "Asyarah"], ["Angka sembilan dalam bahasa Arab adalah", "Tis'ah", "Tsamaniyah", "Asyarah", "Sittah"], ["Angka sepuluh dalam bahasa Arab adalah", "Asyarah", "Tis'ah", "Tsamaniyah", "Sab'ah"], ["Arti kata Qamar adalah", "Bulan", "Matahari", "Bintang", "Langit"], ["Arti kata Maa' adalah", "Air", "Api", "Tanah", "Udara"], ["Arti kata Nar adalah", "Api", "Air", "Angin", "Tanah"]],
                                "Sulit": [["Arti kata Walad adalah", "Anak laki-laki", "Anak perempuan", "Ayah", "Ibu"], ["Arti kata Bintun adalah", "Anak perempuan", "Anak laki-laki", "Kakak", "Adik laki-laki"], ["Arti kata Sayyarah adalah", "Mobil", "Sepeda", "Kapal", "Pesawat"], ["Arti kata Madrasah adalah", "Sekolah", "Rumah", "Pasar", "Masjid"], ["Arti kata Kursi adalah", "Kursi", "Meja", "Lemari", "Pintu"], ["Arti kata Masjid adalah", "Tempat sujud/ibadah", "Sekolah", "Pasar", "Rumah"]]
                            },
                            "3": {
                                "Mudah": [["Arti kata Ukhti adalah", "Saudari perempuan", "Saudara laki-laki", "Ibu", "Ayah"], ["Arti kata Akhi adalah", "Saudara laki-laki", "Saudari perempuan", "Paman", "Bibi"], ["Arti kata Ummi adalah", "Ibu saya", "Ayah saya", "Kakak saya", "Adik saya"], ["Arti kata Abi adalah", "Ayah saya", "Ibu saya", "Paman saya", "Kakek saya"], ["Arti kata Jadd adalah", "Kakek", "Nenek", "Paman", "Bibi"], ["Arti kata Jaddah adalah", "Nenek", "Kakek", "Ibu", "Bibi"]],
                                "Sedang": [["Arti kata Ustadz adalah", "Guru laki-laki", "Guru perempuan", "Murid", "Kepala sekolah"], ["Arti kata Ustadzah adalah", "Guru perempuan", "Guru laki-laki", "Murid", "Penjaga sekolah"], ["Arti kata Thalib adalah", "Murid laki-laki", "Murid perempuan", "Guru", "Kepala sekolah"], ["Arti kata Thalibah adalah", "Murid perempuan", "Murid laki-laki", "Guru", "Penjaga sekolah"], ["Arti kata Fasl adalah", "Kelas", "Sekolah", "Rumah", "Kantor"], ["Arti kata Sabburah adalah", "Papan tulis", "Meja", "Kursi", "Jendela"]],
                                "Sulit": [["Arti kata Mistarah adalah", "Penggaris", "Pensil", "Buku", "Pena"], ["Arti kata Miqlamah adalah", "Tempat pensil", "Tas", "Buku", "Papan tulis"], ["Arti kata Haqibah adalah", "Tas", "Penggaris", "Buku", "Pensil"], ["Arti kata Miqash adalah", "Gunting", "Pensil", "Penggaris", "Lem"], ["Arti kata Maktab adalah", "Meja tulis/kantor", "Kursi", "Lemari", "Rak buku"], ["Arti kata Naafidzah adalah", "Jendela", "Pintu", "Atap", "Dinding"]]
                            },
                            "4": {
                                "Mudah": [["Arti kata Ghurfah adalah", "Kamar", "Dapur", "Kamar mandi", "Ruang tamu"], ["Arti kata Mathbakh adalah", "Dapur", "Kamar", "Ruang tamu", "Kamar mandi"], ["Arti kata Hadiqah adalah", "Taman", "Kebun binatang", "Kolam", "Halaman"], ["Arti kata Kabir adalah", "Besar", "Kecil", "Panjang", "Pendek"], ["Arti kata Shaghir adalah", "Kecil", "Besar", "Tinggi", "Rendah"], ["Arti kata Sath adalah", "Atap", "Lantai", "Dinding", "Pintu"]],
                                "Sedang": [["Arti kata Thawil adalah", "Panjang/tinggi", "Pendek", "Lebar", "Sempit"], ["Arti kata Qashir adalah", "Pendek", "Panjang", "Lebar", "Luas"], ["Arti kata Jamil adalah", "Indah/cantik", "Buruk", "Kotor", "Bersih"], ["Arti kata Nazhif adalah", "Bersih", "Kotor", "Indah", "Jelek"], ["Arti kata Bab (jamaknya Abwab) artinya", "Pintu (pintu-pintu)", "Jendela", "Atap", "Dinding"], ["Arti kata Jadid adalah", "Baru", "Lama", "Rusak", "Kotor"]],
                                "Sulit": [["Arti kata Qadim adalah", "Lama", "Baru", "Bersih", "Indah"], ["Arti kata Wasi' adalah", "Luas", "Sempit", "Panjang", "Pendek"], ["Arti kata Dhayyiq adalah", "Sempit", "Luas", "Panjang", "Tinggi"], ["Arti kata Ba'id adalah", "Jauh", "Dekat", "Tinggi", "Rendah"], ["Arti kata Qarib adalah", "Dekat", "Jauh", "Luas", "Sempit"], ["Arti kata Fauq adalah", "Atas", "Bawah", "Depan", "Belakang"]]
                            },
                            "5": {
                                "Mudah": [["Yaumul Ahad artinya", "Hari Minggu", "Hari Senin", "Hari Selasa", "Hari Jumat"], ["Yaumul Itsnain artinya", "Hari Senin", "Hari Minggu", "Hari Rabu", "Hari Kamis"], ["Yaumul Tsulatsa artinya", "Hari Selasa", "Hari Senin", "Hari Rabu", "Hari Kamis"], ["Yaumul Arbi'a artinya", "Hari Rabu", "Hari Selasa", "Hari Kamis", "Hari Jumat"], ["Yaumul Khamis artinya", "Hari Kamis", "Hari Rabu", "Hari Jumat", "Hari Sabtu"], ["Yaumul Jumu'ah artinya", "Hari Jumat", "Hari Kamis", "Hari Sabtu", "Hari Minggu"]],
                                "Sedang": [["Yaumul Sabt artinya", "Hari Sabtu", "Hari Jumat", "Hari Minggu", "Hari Senin"], ["Angka sebelas dalam bahasa Arab adalah", "Ahada asyar", "Itsna asyar", "Asyarah", "Tis'ah asyar"], ["Angka dua belas dalam bahasa Arab adalah", "Itsna asyar", "Ahada asyar", "Tsalatsata asyar", "Asyarah"], ["Arti kata Shabah adalah", "Pagi", "Siang", "Sore", "Malam"], ["Arti kata Masaa' adalah", "Sore/malam", "Pagi", "Siang", "Tengah hari"], ["Arti kata Lailah adalah", "Malam", "Pagi", "Siang", "Sore"]],
                                "Sulit": [["Arti kata Usbu' adalah", "Minggu (satuan waktu)", "Hari", "Bulan", "Tahun"], ["Arti kata Syahr adalah", "Bulan (satuan waktu)", "Hari", "Minggu", "Tahun"], ["Arti kata Sanah adalah", "Tahun", "Bulan", "Hari", "Minggu"], ["Arti kata Sa'ah adalah", "Jam", "Menit", "Detik", "Hari"], ["Kata tanya Kam berarti", "Berapa", "Bagaimana", "Apa", "Siapa"], ["Kata tanya Mataa berarti", "Kapan", "Di mana", "Bagaimana", "Siapa"]]
                            },
                            "6": {
                                "Mudah": [["Arti kata Kaifa haluk adalah", "Bagaimana kabarmu", "Siapa namamu", "Di mana rumahmu", "Apa pekerjaanmu"], ["Arti kata Ismi adalah", "Nama saya", "Rumah saya", "Sekolah saya", "Buku saya"], ["Arti kata Man adalah", "Siapa", "Apa", "Di mana", "Kapan"], ["Arti kata Maa adalah", "Apa", "Siapa", "Bagaimana", "Berapa"], ["Arti kata Aina adalah", "Di mana", "Kapan", "Siapa", "Apa"], ["Arti kata Na'am adalah", "Ya", "Tidak", "Mungkin", "Belum"]],
                                "Sedang": [["Arti kata Laa adalah", "Tidak", "Ya", "Mungkin", "Sudah"], ["Arti kata Syukron adalah", "Terima kasih", "Maaf", "Tolong", "Permisi"], ["Arti kata Afwan adalah", "Sama-sama/maaf", "Terima kasih", "Selamat", "Salam"], ["Arti kata Min fadhlik adalah", "Tolong (untuk perempuan)", "Terima kasih", "Maaf", "Permisi"], ["Arti kata Ma'as salamah adalah", "Selamat tinggal", "Selamat datang", "Selamat pagi", "Selamat malam"], ["Arti kata Ahlan wa sahlan adalah", "Selamat datang", "Selamat tinggal", "Sampai jumpa", "Terima kasih"]],
                                "Sulit": [["Arti kata Marhaban adalah", "Halo/selamat datang", "Selamat tinggal", "Maaf", "Tolong"], ["Isim adalah kata yang menunjukkan", "Nama/benda", "Perbuatan", "Keterangan waktu", "Kata sambung"], ["Fi'il adalah kata yang menunjukkan", "Perbuatan/kata kerja", "Nama benda", "Kata sifat", "Kata sambung"], ["Huruf dalam ilmu nahwu berfungsi sebagai", "Kata sambung/penghubung", "Kata benda", "Kata kerja", "Kata sifat"], ["Contoh huruf jar adalah", "Fi, ila, min", "Wa, tsumma", "Hal, ma", "Qad, sa"], ["Kata tanya Limadza berarti", "Mengapa", "Kapan", "Di mana", "Berapa"]]
                            },
                            "7": {
                                "Mudah": [["Arti kata Ana adalah", "Saya", "Kamu", "Dia laki-laki", "Kami"], ["Arti kata Anta adalah", "Kamu (laki-laki)", "Kamu (perempuan)", "Saya", "Dia"], ["Arti kata Anti adalah", "Kamu (perempuan)", "Kamu (laki-laki)", "Kami", "Mereka"], ["Arti kata Huwa adalah", "Dia (laki-laki)", "Dia (perempuan)", "Saya", "Kamu"], ["Arti kata Hiya adalah", "Dia (perempuan)", "Dia (laki-laki)", "Kami", "Kalian"], ["Arti kata Nahnu adalah", "Kami/Kita", "Saya", "Kamu", "Mereka"]],
                                "Sedang": [["Kata benda yang menunjukkan jumlah satu disebut", "Mufrad", "Mutsanna", "Jamak", "Ma'rifat"], ["Kata benda yang menunjukkan jumlah dua disebut", "Mutsanna", "Mufrad", "Jamak", "Nakirah"], ["Kata benda yang menunjukkan jumlah lebih dari dua disebut", "Jamak", "Mufrad", "Mutsanna", "Idhafah"], ["Bentuk mutsanna dari kata Muslimun adalah", "Muslimani", "Muslimun", "Muslimuna", "Muslimatun"], ["Kata ganti yang menunjukkan perempuan disebut", "Muannats", "Mudzakkar", "Mufrad", "Jamak"], ["Kata ganti yang menunjukkan laki-laki disebut", "Mudzakkar", "Muannats", "Mutsanna", "Nakirah"]],
                                "Sulit": [["Arti kata Hum adalah", "Mereka (laki-laki)", "Mereka (perempuan)", "Kalian", "Kami"], ["Arti kata Hunna adalah", "Mereka (perempuan)", "Mereka (laki-laki)", "Kalian", "Kami"], ["Arti kata Antum adalah", "Kalian (laki-laki)", "Kalian (perempuan)", "Kami", "Mereka"], ["Arti kata Antunna adalah", "Kalian (perempuan)", "Kalian (laki-laki)", "Kami", "Mereka"], ["Bentuk jamak dari kata Muslimun adalah", "Muslimuna", "Muslimani", "Muslimatun", "Muslimataani"], ["Isim yang menunjuk pada sesuatu yang sudah dikenal disebut", "Ma'rifat", "Nakirah", "Mufrad", "Jamak"]]
                            },
                            "8": {
                                "Mudah": [["Arti kata Madrasatun adalah", "Sekolah", "Perpustakaan", "Rumah sakit", "Pasar"], ["Arti kata Maktabun adalah", "Perpustakaan", "Sekolah", "Rumah sakit", "Kantor"], ["Arti kata Mustasyfa adalah", "Rumah sakit", "Sekolah", "Pasar", "Masjid"], ["Arti kata Suuq adalah", "Pasar", "Sekolah", "Rumah sakit", "Kantor"], ["Arti kata Masjid adalah", "Tempat sujud/ibadah", "Sekolah", "Pasar", "Rumah"], ["Arti kata Maktabah adalah", "Perpustakaan/toko buku", "Rumah sakit", "Pasar", "Kantor pos"]],
                                "Sedang": [["Kata tanya Maa berarti", "Apa", "Siapa", "Di mana", "Kapan"], ["Kata tanya Man berarti", "Siapa", "Apa", "Bagaimana", "Berapa"], ["Kata tanya Aina berarti", "Di mana", "Kapan", "Siapa", "Apa"], ["Kata tanya Mataa berarti", "Kapan", "Di mana", "Bagaimana", "Siapa"], ["Kata tanya Kaifa berarti", "Bagaimana", "Berapa", "Di mana", "Kapan"], ["Kata tanya Kam berarti", "Berapa", "Bagaimana", "Apa", "Siapa"]],
                                "Sulit": [["Kata tanya Limadza berarti", "Mengapa", "Kapan", "Di mana", "Berapa"], ["Kata tanya Ayyu berarti", "Yang mana", "Siapa", "Apa", "Kapan"], ["Yaumul Ahad artinya", "Hari Minggu", "Hari Senin", "Hari Selasa", "Hari Jumat"], ["Yaumul Itsnain artinya", "Hari Senin", "Hari Minggu", "Hari Rabu", "Hari Kamis"], ["Arti Kaifa haluk adalah", "Bagaimana kabarmu", "Siapa namamu", "Di mana rumahmu", "Apa pekerjaanmu"], ["Arti kata Bikam hadza adalah", "Berapa harga ini", "Apa nama ini", "Kapan ini terjadi", "Di mana tempat ini"]]
                            },
                            "9": {
                                "Mudah": [["Fi'il Madhi menunjukkan perbuatan yang terjadi pada waktu", "Lampau", "Sekarang", "Akan datang", "Terus-menerus"], ["Fi'il Mudhari menunjukkan perbuatan pada waktu", "Sekarang/akan datang", "Lampau", "Sudah selesai", "Masa lalu jauh"], ["Isim adalah kata yang menunjukkan", "Nama/benda", "Perbuatan", "Keterangan waktu", "Kata sambung"], ["Fi'il adalah kata yang menunjukkan", "Perbuatan/kata kerja", "Nama benda", "Kata sifat", "Kata sambung"], ["Huruf dalam ilmu nahwu berfungsi sebagai", "Kata sambung/penghubung", "Kata benda", "Kata kerja", "Kata sifat"], ["Contoh huruf jar adalah", "Fi, ila, min", "Wa, tsumma", "Hal, ma", "Qad, sa"]],
                                "Sedang": [["Fi'il Madhi dari kata Kataba artinya", "Telah menulis", "Sedang menulis", "Akan menulis", "Menulislah"], ["Fi'il Mudhari dari kata Yaktubu artinya", "Sedang/akan menulis", "Telah menulis", "Menulislah", "Jangan menulis"], ["Contoh huruf athaf adalah", "Wa, tsumma, aw", "Fi, ila, min", "Hal, ma", "Qad, sa"], ["Kalimat yang diawali dengan kata benda disebut", "Jumlah Ismiyah", "Jumlah Fi'liyah", "Jumlah Syarthiyah", "Jumlah Nida'"], ["Kalimat yang diawali dengan kata kerja disebut", "Jumlah Fi'liyah", "Jumlah Ismiyah", "Jumlah Istifham", "Jumlah Ta'ajjub"], ["Subjek dalam kalimat Jumlah Ismiyah disebut", "Mubtada", "Khabar", "Fa'il", "Maf'ul bih"]],
                                "Sulit": [["Predikat dalam kalimat Jumlah Ismiyah disebut", "Khabar", "Mubtada", "Na'at", "Idhafah"], ["Pelaku perbuatan dalam Jumlah Fi'liyah disebut", "Fa'il", "Maf'ul bih", "Mubtada", "Khabar"], ["Objek yang dikenai perbuatan disebut", "Maf'ul bih", "Fa'il", "Mubtada", "Na'at"], ["Kata yang menerangkan sifat suatu benda disebut", "Na'at", "Idhafah", "Athaf", "Badal"], ["Idhafah adalah gabungan dua kata benda yang menunjukkan", "Kepemilikan/keterangan", "Perlawanan", "Pertanyaan", "Perintah"], ["Kalimat Kitabul mudarris menggunakan struktur", "Idhafah", "Na'at man'ut", "Athaf", "Badal"]]
                            },
                            "10": {
                                "Mudah": [["Ilmu yang mempelajari perubahan bentuk kata dalam bahasa Arab disebut", "Sharaf", "Nahwu", "Balaghah", "Arudh"], ["Ilmu yang mempelajari kedudukan kata dalam kalimat disebut", "Nahwu", "Sharaf", "Balaghah", "Mantiq"], ["Kalimat yang diawali dengan kata benda disebut", "Jumlah Ismiyah", "Jumlah Fi'liyah", "Jumlah Syarthiyah", "Jumlah Nida'"], ["Kalimat yang diawali dengan kata kerja disebut", "Jumlah Fi'liyah", "Jumlah Ismiyah", "Jumlah Istifham", "Jumlah Ta'ajjub"], ["Subjek dalam kalimat Jumlah Ismiyah disebut", "Mubtada", "Khabar", "Fa'il", "Maf'ul bih"], ["Predikat dalam kalimat Jumlah Ismiyah disebut", "Khabar", "Mubtada", "Na'at", "Idhafah"]],
                                "Sedang": [["Pelaku perbuatan dalam Jumlah Fi'liyah disebut", "Fa'il", "Maf'ul bih", "Mubtada", "Khabar"], ["Objek yang dikenai perbuatan disebut", "Maf'ul bih", "Fa'il", "Mubtada", "Na'at"], ["Kata yang menerangkan sifat suatu benda disebut", "Na'at", "Idhafah", "Athaf", "Badal"], ["Harakat akhir kata yang menunjukkan posisi subjek disebut", "Rafa'", "Nashab", "Jar", "Jazm"], ["Harakat akhir kata yang menunjukkan posisi objek disebut", "Nashab", "Rafa'", "Jar", "Jazm"], ["Idhafah adalah gabungan dua kata benda yang menunjukkan", "Kepemilikan/keterangan", "Perlawanan", "Pertanyaan", "Perintah"]],
                                "Sulit": [["Kalimat Kitabul mudarris menggunakan struktur", "Idhafah", "Na'at man'ut", "Athaf", "Badal"], ["Contoh huruf athaf adalah", "Wa, tsumma, aw", "Fi, ila, min", "Hal, ma", "Qad, sa"], ["Fi'il Amr digunakan untuk menyatakan", "Perintah", "Larangan", "Berita", "Pertanyaan"], ["Fi'il Nahi digunakan untuk menyatakan", "Larangan", "Perintah", "Berita", "Harapan"], ["Contoh dhamir muttashil adalah", "Ha, Hu, Ki", "Ana, Anta, Huwa", "Hadza, Tilka", "Man, Maa"], ["Isim yang tidak menerima tanwin disebut", "Isim ghairu munsharif", "Isim munsharif", "Isim ma'rifat", "Isim nakirah"]]
                            },
                            "11": {
                                "Mudah": [["Fi'il Amr digunakan untuk menyatakan", "Perintah", "Larangan", "Berita", "Pertanyaan"], ["Fi'il Nahi digunakan untuk menyatakan", "Larangan", "Perintah", "Berita", "Harapan"], ["Contoh dhamir muttashil adalah", "Ha, Hu, Ki", "Ana, Anta, Huwa", "Hadza, Tilka", "Man, Maa"], ["Isim yang tidak menerima tanwin disebut", "Isim ghairu munsharif", "Isim munsharif", "Isim ma'rifat", "Isim nakirah"], ["Wazan tsulasi mujarrad yang paling dasar contohnya", "Fa'ala", "Yaf'alu", "Muf'alun", "Fa'il"], ["Isim fa'il menunjukkan makna", "Pelaku", "Objek yang dikenai", "Tempat", "Alat"]],
                                "Sedang": [["Isim maf'ul menunjukkan makna", "Objek yang dikenai perbuatan", "Pelaku", "Waktu", "Sifat"], ["Mashdar adalah kata benda yang berasal dari", "Kata kerja", "Kata benda lain", "Kata sifat", "Huruf jar"], ["Fi'il yang huruf akhirnya alif, wawu, atau ya' disebut", "Fi'il mu'tal", "Fi'il shahih", "Fi'il mudhaaf", "Fi'il jamid"], ["Fi'il Mudhari yang didahului huruf Lam Amr berfungsi untuk", "Perintah tidak langsung", "Larangan", "Berita", "Pertanyaan"], ["Kalimat tanya dalam bahasa Arab menggunakan huruf istifham seperti", "Hal dan Maa", "Wa dan Tsumma", "Fi dan Ila", "Qad dan Sa"], ["Dhamir munfashil contohnya", "Ana, Anta, Huwa", "Ha, Hu, Ki", "Hadza, Tilka", "Man, Maa"]],
                                "Sulit": [["Arti kata Muhadatsah adalah", "Percakapan", "Karangan", "Terjemahan", "Tata bahasa"], ["Arti kata Insya adalah", "Karangan/mengarang", "Percakapan", "Ujian", "Terjemahan"], ["Arti kata Muthala'ah adalah", "Membaca pemahaman", "Menulis", "Berbicara", "Mendengar"], ["Arti kata Tarjamah adalah", "Terjemahan", "Karangan", "Ujian", "Kaidah"], ["Arti kata Qawa'id adalah", "Tata bahasa/kaidah", "Percakapan", "Kosakata", "Ujian"], ["Percakapan formal untuk perkenalan diri disebut", "Ta'aruf", "Muhadatsah bebas", "Khitobah", "Munazharah"]]
                            },
                            "12": {
                                "Mudah": [["Arti kata Imtihan adalah", "Ujian", "Liburan", "Pelajaran", "Perpustakaan"], ["Ilmu yang mempelajari keindahan bahasa dan sastra Arab disebut", "Balaghah", "Nahwu", "Sharaf", "Arudh"], ["Arti kata Muhadatsah adalah", "Percakapan", "Karangan", "Terjemahan", "Tata bahasa"], ["Arti kata Insya adalah", "Karangan/mengarang", "Percakapan", "Ujian", "Terjemahan"], ["Arti kata Tarjamah adalah", "Terjemahan", "Karangan", "Ujian", "Kaidah"], ["Arti kata Qawa'id adalah", "Tata bahasa/kaidah", "Percakapan", "Kosakata", "Ujian"]],
                                "Sedang": [["Wazan tsulasi mujarrad yang paling dasar contohnya", "Fa'ala", "Yaf'alu", "Muf'alun", "Fa'il"], ["Isim fa'il menunjukkan makna", "Pelaku", "Objek yang dikenai", "Tempat", "Alat"], ["Isim maf'ul menunjukkan makna", "Objek yang dikenai perbuatan", "Pelaku", "Waktu", "Sifat"], ["Mashdar adalah kata benda yang berasal dari", "Kata kerja", "Kata benda lain", "Kata sifat", "Huruf jar"], ["Idhafah adalah gabungan dua kata benda yang menunjukkan", "Kepemilikan/keterangan", "Perlawanan", "Pertanyaan", "Perintah"], ["Kalimat Kitabul mudarris menggunakan struktur", "Idhafah", "Na'at man'ut", "Athaf", "Badal"]],
                                "Sulit": [["Contoh huruf athaf adalah", "Wa, tsumma, aw", "Fi, ila, min", "Hal, ma", "Qad, sa"], ["Fi'il yang huruf akhirnya alif, wawu, atau ya' disebut", "Fi'il mu'tal", "Fi'il shahih", "Fi'il mudhaaf", "Fi'il jamid"], ["Percakapan formal untuk perkenalan diri disebut", "Ta'aruf", "Muhadatsah bebas", "Khitobah", "Munazharah"], ["Arti kata Muthala'ah adalah", "Membaca pemahaman", "Menulis", "Berbicara", "Mendengar"], ["Isim yang tidak menerima tanwin disebut", "Isim ghairu munsharif", "Isim munsharif", "Isim ma'rifat", "Isim nakirah"], ["Ilmu yang mempelajari struktur bait syair Arab disebut", "Arudh", "Balaghah", "Nahwu", "Sharaf"]]
                            }
                        },
                    };
                    
                    // Fallback mapel spesifik atau default text generator agar tembus 30
                    // Prioritas: data per Kelas spesifik (jika tersedia) -> data per Jenjang (perilaku lama, tetap sama untuk mapel lain)
                    let bankRaw = (factBanks[subject] && factBanks[subject][kelas]) ? factBanks[subject][kelas]
                                : (factBanks[subject] && factBanks[subject][jenjang]) ? factBanks[subject][jenjang]
                                : null;
                    let bank = null;
                    if (Array.isArray(bankRaw)) {
                        // Struktur lama: array soal langsung (tanpa pembagian tingkat kesulitan)
                        bank = bankRaw;
                    } else if (bankRaw && typeof bankRaw === 'object') {
                        // Struktur baru: dibagi per tingkat kesulitan (Mudah/Sedang/Sulit)
                        bank = bankRaw[tingkat] || bankRaw['Sedang'] || Object.values(bankRaw)[0];
                    }
                    if(bank && bank.length) {
                        let b = bank[getRandomInt(0, bank.length-1)];
                        qText = `${b[0]}?`; [ans, w1, w2, w3] = [b[1], b[2], b[3], b[4]];
                    } else {
                        // Generator generik jika data base habis (mencegah loop tak terhingga)
                        qText = `Pertanyaan ${subject} (${jenjang}) Bab ${getRandomInt(1,9)} No.${getRandomInt(10,99)}?`;
                        ans = `Jawaban Benar`; w1 = `Pilihan Salah A`; w2 = `Pilihan Salah B`; w3 = `Pilihan Salah C`;
                    }
                }

                // Append unique id to string to ensure Set works, but display only text
                let qStr = qText + "|" + ans;
                if (!generatedSet.has(qStr)) {
                    generatedSet.add(qStr);
                    let options = [ans, w1, w2, w3];
                    
                    // Pastikan tidak ada opsi kembar
                    options = [...new Set(options)];
                    while(options.length < 4) options.push(`Opsi Lain ${Math.random().toString(36).substring(7,10)}`);
                    
                    options.sort(() => Math.random() - 0.5); // Acak
                    questions.push({ text: qText, options: options, answer: ans, image: null });
                }
            }
            return questions;
        }

        // --- Canvas & Physics State ---
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        let cw = window.innerWidth;
        let ch = window.innerHeight;
        canvas.width = cw;
        canvas.height = ch;

        window.addEventListener('resize', () => {
            cw = window.innerWidth; ch = window.innerHeight;
            canvas.width = cw; canvas.height = ch;
        });

        let gameState = 'SETUP'; // SETUP, PLAYING, GAMEOVER
        let config = {};
        let questionList = [];
        let currentQIndex = 0;
        let isTransitioningQuestion = false;
        
        let p1Score = 0; let p2Score = 0;
        let p1WrongStreak = 0; let p2WrongStreak = 0; // Menghitung jawaban salah beruntun untuk sistem poin minus progresif
        let p1Hands = []; let p2Hands = [];
        let fallingItems = []; let particles = [];
        let speedMultiplier = 1; // Diatur lewat tombol Kecepatan di layar setup

        // Diperbesar untuk menampung teks panjang
        const getBaseRadius = () => Math.min(cw, ch) * 0.085; 
        const FALL_SPEED = ch * 0.0035;

        // Utility: Word Wrap for Canvas
        function wrapText(context, text, x, y, maxWidth, lineHeight) {
            let words = text.toString().split(' ');
            let line = '';
            let lines = [];

            for(let n = 0; n < words.length; n++) {
                let testLine = line + words[n] + ' ';
                let metrics = context.measureText(testLine);
                let testWidth = metrics.width;
                if (testWidth > maxWidth && n > 0) {
                    lines.push(line);
                    line = words[n] + ' ';
                } else {
                    line = testLine;
                }
            }
            lines.push(line);
            
            let startY = y - ((lines.length - 1) * lineHeight) / 2;
            for(let k=0; k<lines.length; k++) {
                context.fillText(lines[k].trim(), x, startY + (k * lineHeight));
            }
        }

        class FallingItem {
            constructor(text, isCorrect, colIndex, totalCols, side) {
                this.text = text;
                this.isCorrect = isCorrect;
                this.side = side; 
                this.active = true;
                
                this.radius = getBaseRadius();
                const sectionWidth = cw / 2;
                const offset = side === 'left' ? 0 : sectionWidth;
                const colWidth = sectionWidth / totalCols;
                
                this.x = offset + (colWidth * colIndex) + (colWidth / 2);
                this.x += (Math.random() - 0.5) * colWidth * 0.2; 
                
                this.y = -this.radius * 2 - (Math.random() * ch * 0.25);
                this.speed = FALL_SPEED * speedMultiplier * (0.8 + Math.random() * 0.4);
                
                this.color = side === 'left' ? '#facc15' : '#60a5fa';
                this.swingAngle = Math.random() * Math.PI * 2;
                this.baseX = this.x;
            }

            update() {
                if (!this.active) return;
                this.y += this.speed;
                this.swingAngle += 0.02;
                this.x = this.baseX + Math.sin(this.swingAngle) * (cw * 0.015);
                if (this.y > ch + this.radius * 2) this.active = false;
            }

            draw(ctx) {
                if (!this.active) return;

                // Tali gantung
                ctx.beginPath();
                ctx.moveTo(this.baseX, 0);
                ctx.lineTo(this.x, this.y);
                ctx.strokeStyle = 'rgba(255,255,255,0.25)';
                ctx.lineWidth = 2;
                ctx.stroke();

                // Balon
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = '#1e293b';
                ctx.fill();
                ctx.lineWidth = 4;
                ctx.strokeStyle = this.color;
                ctx.stroke();

                // Teks (dengan auto-wrap)
                ctx.fillStyle = '#ffffff';
                let fontSize = this.radius * 0.35;
                if (this.text.toString().length > 15) fontSize = this.radius * 0.25;
                ctx.font = `bold ${fontSize}px 'Nunito'`;
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                wrapText(ctx, this.text, this.x, this.y, this.radius * 1.7, fontSize * 1.2);
            }
            
            checkHit(hx, hy) {
                if (!this.active) return false;
                const dist = Math.hypot(this.x - hx, this.y - hy);
                return dist < this.radius * 1.5; // Hitbox sedikit diperbesar untuk toleransi kamera lemah
            }
        }

        class Particle {
            constructor(x, y, color) {
                this.x = x; this.y = y;
                this.vx = (Math.random() - 0.5) * 18;
                this.vy = (Math.random() - 0.5) * 18;
                this.life = 1.0; this.color = color;
                this.size = Math.random() * 8 + 4;
            }
            update() {
                this.x += this.vx; this.y += this.vy;
                this.life -= 0.035;
            }
            draw(ctx) {
                if (this.life <= 0) return;
                ctx.globalAlpha = this.life;
                ctx.fillStyle = this.color;
                ctx.beginPath(); ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2); ctx.fill();
                ctx.globalAlpha = 1.0;
            }
        }

        function createExplosion(x, y, color) {
            for (let i = 0; i < 22; i++) particles.push(new Particle(x, y, color));
        }

        function startNewQuestion() {
            if (currentQIndex >= questionList.length) {
                endGame();
                return;
            }

            isTransitioningQuestion = false;
            const q = questionList[currentQIndex];
            document.getElementById('questionDisplay').innerText = q.text;
            document.getElementById('progressDisplay').innerText = `Soal: ${currentQIndex + 1} / ${config.jumlah}`;
            
            const qImgEl = document.getElementById('questionImage');
            if (q.image) {
                qImgEl.src = q.image;
                qImgEl.classList.remove('hidden');
            } else {
                qImgEl.src = '';
                qImgEl.classList.add('hidden');
            }

            const qc = document.getElementById('questionContainer');
            qc.classList.remove('scale-100'); qc.classList.add('scale-0');
            setTimeout(() => {
                qc.classList.remove('scale-0'); qc.classList.add('scale-100');
            }, 60);

            fallingItems = [];
            q.options.forEach((opt, idx) => {
                fallingItems.push(new FallingItem(opt, opt === q.answer, idx, 4, 'left'));
                fallingItems.push(new FallingItem(opt, opt === q.answer, idx, 4, 'right'));
            });
        }

        function triggerNextQuestion() {
            if (isTransitioningQuestion) return;
            isTransitioningQuestion = true;
            fallingItems.forEach(item => item.active = false);
            currentQIndex++;
            setTimeout(() => { fallingItems = []; startNewQuestion(); }, 850);
        }

        function updateScores() {
            document.getElementById('scoreP1').innerText = p1Score;
            document.getElementById('scoreP2').innerText = p2Score;
        }

        // --- EXPORT & IMPORT JSON LOGIC (Mode Guru) ---
        const customQuestionsContainer = document.getElementById('customQuestionsContainer');
        const btnExport = document.getElementById('btnExport');
        const inpImport = document.getElementById('inpImport');
        
        btnExport.addEventListener('click', () => {
            let data = [];
            document.querySelectorAll('.custom-q-block').forEach(block => {
                let text = block.querySelector('.cq-text').value.trim();
                let ans = block.querySelector('.cq-ans').value.trim();
                let w1 = block.querySelector('.cq-w1').value.trim();
                let w2 = block.querySelector('.cq-w2').value.trim();
                let w3 = block.querySelector('.cq-w3').value.trim();
                let imgEl = block.querySelector('.cq-img-preview');
                let img = (!imgEl.classList.contains('hidden') && imgEl.src) ? imgEl.src : null;
                
                if(text && ans && w1) {
                    data.push({ q: text, a: ans, w: [w1, w2, w3], img: img });
                }
            });
            
            if(data.length === 0) {
                alert("Tidak ada soal lengkap untuk diekspor!"); return;
            }
            
            const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(data));
            const dlAnchor = document.createElement('a');
            dlAnchor.setAttribute("href", dataStr);
            dlAnchor.setAttribute("download", "Bank_Soal_Gesture_Edu.json");
            document.body.appendChild(dlAnchor);
            dlAnchor.click();
            dlAnchor.remove();
        });

        inpImport.addEventListener('change', (e) => {
            const file = e.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (evt) => {
                try {
                    const parsed = JSON.parse(evt.target.result);
                    customQuestionsContainer.innerHTML = '';
                    parsed.forEach(item => {
                        addCustomQuestionUI(item);
                    });
                    alert(`Berhasil mengimpor ${parsed.length} soal!`);
                } catch (err) {
                    alert("Format file JSON tidak valid!");
                }
            };
            reader.readAsText(file);
            e.target.value = ""; // Reset
        });

        function addCustomQuestionUI(prefill = null) {
            const index = customQuestionsContainer.children.length + 1;
            const div = document.createElement('div');
            div.className = 'custom-q-block bg-slate-800 p-4 rounded-xl border border-slate-600 relative shadow-inner';
            
            let html = `
                <div class="flex justify-between items-center mb-3">
                    <span class="text-xs font-black text-slate-400 uppercase tracking-wider q-label">Soal #${index}</span>
                    <button class="text-red-400 hover:text-red-200 font-bold text-xs bg-red-900/30 px-3 py-1 rounded-md" onclick="this.parentElement.parentElement.remove(); updateCustomQuestionLabels();">Hapus</button>
                </div>
                <textarea class="cq-text form-input mb-3 text-sm py-2 h-16 resize-none" placeholder="Ketik Pertanyaan...">${prefill ? prefill.q : ''}</textarea>
                
                <div class="mb-3 bg-slate-900/50 p-2.5 rounded-xl border border-slate-700">
                    <label class="text-xs font-bold text-indigo-300 block mb-1">Gambar Soal (Opsional)</label>
                    <div class="flex items-center gap-3">
                        <input type="file" accept="image/*" class="cq-img-file text-xs text-slate-300 file:mr-2 file:py-1.5 file:px-3 file:rounded-lg file:border-0 file:text-xs file:font-bold file:bg-indigo-600 file:text-white hover:file:bg-indigo-500 cursor-pointer">
                        <img class="cq-img-preview ${(prefill && prefill.img) ? '' : 'hidden'} w-12 h-12 object-cover rounded-lg border-2 border-indigo-400" src="${(prefill && prefill.img) ? prefill.img : ''}">
                    </div>
                </div>

                <label class="text-xs font-bold text-emerald-400 block mb-1">Jawaban Benar</label>
                <input type="text" class="cq-ans form-input border-emerald-500/50 mb-3 text-sm py-1.5 text-emerald-300" placeholder="Jawaban Tepat" value="${prefill ? prefill.a : ''}">
                <label class="text-xs font-bold text-red-400 block mb-1">3 Jawaban Pengecoh</label>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-2">
                    <input type="text" class="cq-w1 form-input border-red-400/50 text-sm py-1.5 text-red-300" placeholder="Pengecoh 1" value="${prefill ? prefill.w[0] : ''}">
                    <input type="text" class="cq-w2 form-input border-red-400/50 text-sm py-1.5 text-red-300" placeholder="Pengecoh 2" value="${prefill ? prefill.w[1] : ''}">
                    <input type="text" class="cq-w3 form-input border-red-400/50 text-sm py-1.5 text-red-300" placeholder="Pengecoh 3" value="${prefill ? (prefill.w[2]||'') : ''}">
                </div>
            `;
            div.innerHTML = html;
            
            const fileInput = div.querySelector('.cq-img-file');
            const imgPreview = div.querySelector('.cq-img-preview');
            fileInput.addEventListener('change', (e) => {
                const file = e.target.files[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onload = (evt) => { imgPreview.src = evt.target.result; imgPreview.classList.remove('hidden'); };
                    reader.readAsDataURL(file);
                } else { imgPreview.src = ''; imgPreview.classList.add('hidden'); }
            });

            customQuestionsContainer.appendChild(div);
            updateCustomQuestionLabels();
            customQuestionsContainer.scrollTop = customQuestionsContainer.scrollHeight;
        }

        function updateCustomQuestionLabels() {
            customQuestionsContainer.querySelectorAll('.custom-q-block').forEach((b, idx) => {
                b.querySelector('.q-label').innerText = `Soal #${idx + 1}`;
            });
        }
        document.getElementById('btnAddCustom').addEventListener('click', () => addCustomQuestionUI());

        // Mode Toggles
        const btnModeAuto = document.getElementById('btnModeAuto');
        const btnModeCustom = document.getElementById('btnModeCustom');
        const autoConfigMode = document.getElementById('autoConfigMode');
        const customConfigMode = document.getElementById('customConfigMode');
        let currentMode = 'AUTO'; 

        btnModeAuto.addEventListener('click', () => {
            currentMode = 'AUTO';
            btnModeAuto.className = 'flex-1 py-2 px-4 rounded-lg bg-indigo-600 text-white font-bold text-sm transition-all shadow-md';
            btnModeCustom.className = 'flex-1 py-2 px-4 rounded-lg text-slate-400 hover:text-white font-bold text-sm transition-all';
            autoConfigMode.classList.remove('hidden'); customConfigMode.classList.add('hidden');
        });

        btnModeCustom.addEventListener('click', () => {
            currentMode = 'CUSTOM';
            btnModeCustom.className = 'flex-1 py-2 px-4 rounded-lg bg-indigo-600 text-white font-bold text-sm transition-all shadow-md';
            btnModeAuto.className = 'flex-1 py-2 px-4 rounded-lg text-slate-400 hover:text-white font-bold text-sm transition-all';
            autoConfigMode.classList.add('hidden'); customConfigMode.classList.remove('hidden');
            if(customQuestionsContainer.children.length === 0) addCustomQuestionUI();
        });

        // Speed Selector (mengatur kecepatan jatuhnya bola jawaban)
        const sliderSpeed = document.getElementById('sliderSpeed');
        const speedValueLabel = document.getElementById('speedValueLabel');
        function updateSpeedLabel(val) {
            let label = 'Normal';
            if (val <= 0.7) label = 'Lambat';
            else if (val < 0.95) label = 'Agak Lambat';
            else if (val <= 1.05) label = 'Normal';
            else if (val <= 1.6) label = 'Cepat';
            else label = 'Sangat Cepat';
            speedValueLabel.innerText = label;
        }
        sliderSpeed.addEventListener('input', () => {
            speedMultiplier = parseFloat(sliderSpeed.value);
            updateSpeedLabel(speedMultiplier);
        });

        // Start Game
        document.getElementById('btnStart').addEventListener('click', async () => {
            document.getElementById('setupError').classList.add('hidden');
            
            config = {
                p1Name: document.getElementById('inpP1Name').value.trim() || "Siswa Kiri",
                p2Name: document.getElementById('inpP2Name').value.trim() || "Siswa Kanan"
            };

            if (currentMode === 'AUTO') {
                config.jenjang = document.getElementById('selJenjang').value;
                config.kelas = document.getElementById('selKelas').value;
                config.mapel = document.getElementById('selMapel').value;
                config.tingkat = document.getElementById('selTingkat').value;
                config.jumlah = parseInt(document.getElementById('inpJumlah').value) || 30;
                
                if (config.jumlah > 30) config.jumlah = 30;
                if (config.jumlah < 1) config.jumlah = 1;

                document.getElementById('questionSubject').innerText = `${config.mapel} - ${config.jenjang}`;
                questionList = generateQuestions(config.mapel, config.jenjang, config.tingkat, config.jumlah, config.kelas);
            } else {
                const blocks = customQuestionsContainer.querySelectorAll('.custom-q-block');
                if (blocks.length === 0) {
                    const err = document.getElementById('setupError');
                    err.innerText = "Tidak ada soal! Tambahkan soal atau impor dari JSON.";
                    err.classList.remove('hidden'); return;
                }

                questionList = [];
                let hasError = false;

                blocks.forEach(block => {
                    const qText = block.querySelector('.cq-text').value.trim();
                    const qAns = block.querySelector('.cq-ans').value.trim();
                    const qW1 = block.querySelector('.cq-w1').value.trim();
                    const qW2 = block.querySelector('.cq-w2').value.trim();
                    const qW3 = block.querySelector('.cq-w3').value.trim();
                    const imgPreview = block.querySelector('.cq-img-preview');
                    const qImg = (!imgPreview.classList.contains('hidden')) ? imgPreview.src : null;

                    if (!qText || !qAns || !qW1) hasError = true;
                    else {
                        let options = [qAns, qW1];
                        if(qW2) options.push(qW2); if(qW3) options.push(qW3);
                        while(options.length < 4) options.push(`Pengecoh ${options.length}`);
                        options.sort(() => Math.random() - 0.5);
                        questionList.push({ text: qText, image: qImg, options: options, answer: qAns });
                    }
                });

                if (hasError) {
                    const err = document.getElementById('setupError');
                    err.innerText = "Lengkapi Pertanyaan, Jawaban Benar, dan minimal 1 Pengecoh di semua soal!";
                    err.classList.remove('hidden'); return;
                }
                config.jumlah = questionList.length;
                document.getElementById('questionSubject').innerText = "Soal Kustom Guru";
            }

            await initAudio();
            playStartSound();

            document.getElementById('nameP1HUD').innerText = config.p1Name; document.getElementById('nameP2HUD').innerText = config.p2Name;
            document.getElementById('nameP1GO').innerText = config.p1Name; document.getElementById('nameP2GO').innerText = config.p2Name;
            
            p1Score = 0; p2Score = 0; p1WrongStreak = 0; p2WrongStreak = 0; currentQIndex = 0;
            isTransitioningQuestion = false; particles = []; fallingItems = [];
            updateScores();

            document.getElementById('setupScreen').classList.add('hidden');
            document.getElementById('gameOverScreen').classList.add('hidden');
            document.getElementById('hudLayer').classList.remove('hidden');
            document.getElementById('btnHome').classList.remove('hidden'); // Show Home btn
            
            gameState = 'PLAYING';
            startNewQuestion();
        });

        document.getElementById('btnRestart').addEventListener('click', () => {
            document.getElementById('gameOverScreen').classList.add('hidden');
            document.getElementById('hudLayer').classList.add('hidden');
            document.getElementById('btnHome').classList.add('hidden');
            document.getElementById('setupScreen').classList.remove('hidden');
            gameState = 'SETUP';
        });

        function endGame() {
            gameState = 'GAMEOVER';
            document.getElementById('hudLayer').classList.add('hidden');
            document.getElementById('btnHome').classList.add('hidden'); // Hide Home btn on game over
            const goScreen = document.getElementById('gameOverScreen');
            goScreen.classList.remove('hidden');
            
            document.getElementById('finalScoreP1').innerText = p1Score;
            document.getElementById('finalScoreP2').innerText = p2Score;
            
            const badge = document.getElementById('winnerBadge');
            const txt = document.getElementById('winnerText');
            
            if (p1Score > p2Score) {
                badge.className = 'bg-yellow-500 px-8 py-3 rounded-full mb-8 transform scale-105 shadow-[0_0_30px_#eab308] border-2 border-white';
                txt.innerText = `${config.p1Name.toUpperCase()}\nMENANG!`;
            } else if (p2Score > p1Score) {
                badge.className = 'bg-blue-500 px-8 py-3 rounded-full mb-8 transform scale-105 shadow-[0_0_30px_#3b82f6] border-2 border-white';
                txt.innerText = `${config.p2Name.toUpperCase()}\nMENANG!`;
            } else {
                badge.className = 'bg-slate-600 px-8 py-3 rounded-full mb-8 transform scale-105 border-2 border-white';
                txt.innerText = 'HASIL SERI!';
            }
        }

        // --- MEDIAPIPE AI TRACKING (OPTIMIZED FOR IFP) ---
        const videoElement = document.getElementById('input_video');
        const hands = new Hands({locateFile: (file) => `https://cdn.jsdelivr.net/npm/@mediapipe/hands/${file}`});

        hands.setOptions({
            maxNumHands: 4, // Allow up to 4 hands (2 per student)
            modelComplexity: 0, // 0 = FASTEST (Best for IFP/Weak Processors)
            minDetectionConfidence: 0.4, // Diturunkan ke 0.4 agar tangan benar-benar terdeteksi di IFP/kamera sekolah
            minTrackingConfidence: 0.4 // Diturunkan ke 0.4 agar pelacakan tidak mudah putus
        });

        hands.onResults((results) => {
            ctx.clearRect(0, 0, cw, ch);

            if (results.image) {
                ctx.save();
                ctx.scale(-1, 1);
                ctx.imageSmoothingEnabled = true;
                ctx.drawImage(results.image, -cw, 0, cw, ch);
                
                const bgGradient = ctx.createRadialGradient(-cw/2, ch/2, Math.min(cw, ch)*0.3, -cw/2, ch/2, Math.max(cw, ch)*0.85);
                bgGradient.addColorStop(0, 'rgba(15, 23, 42, 0.2)');
                bgGradient.addColorStop(1, 'rgba(15, 23, 42, 0.6)');
                ctx.fillStyle = bgGradient; ctx.fillRect(-cw, 0, cw, ch);
                ctx.restore();
            }

            aiResultCount++;
            p1Hands = []; p2Hands = [];

            if (results.multiHandLandmarks) {
                for (const landmarks of results.multiHandLandmarks) {
                    const indexTip = landmarks[8];
                    const hx = (1 - indexTip.x) * cw; 
                    const hy = indexTip.y * ch;

                    // Tidak peduli label kiri/kanan dari MediaPipe, cukup deteksi posisi fisik di layar
                    if (hx < cw / 2) p1Hands.push({ x: hx, y: hy });
                    else p2Hands.push({ x: hx, y: hy });
                }
            }

            updateHandStatus(results.multiHandLandmarks ? results.multiHandLandmarks.length : 0);

            if (gameState === 'PLAYING') updateAndDrawGame();
        });

        function updateAndDrawGame() {
            // Split Line
            ctx.beginPath(); ctx.setLineDash([12, 16]);
            ctx.moveTo(cw/2, 0); ctx.lineTo(cw/2, ch);
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.3)'; ctx.lineWidth = 4; ctx.stroke(); ctx.setLineDash([]);

            // Particles
            for (let i = particles.length - 1; i >= 0; i--) {
                particles[i].update(); particles[i].draw(ctx);
                if (particles[i].life <= 0) particles.splice(i, 1);
            }

            // Hit Detection & Drawing Items
            let itemsActive = false;
            for (let i = fallingItems.length - 1; i >= 0; i--) {
                let item = fallingItems[i];
                item.update(); item.draw(ctx);
                if (item.active) itemsActive = true;

                if (item.active) {
                    let hitBy = null;
                    if (item.side === 'left') {
                        for (let hp of p1Hands) if (item.checkHit(hp.x, hp.y)) { hitBy = 'P1'; break; }
                    } else if (item.side === 'right') {
                        for (let hp of p2Hands) if (item.checkHit(hp.x, hp.y)) { hitBy = 'P2'; break; }
                    }

                    if (hitBy) {
                        item.active = false;
                        if (item.isCorrect) {
                            playCorrectSound();
                            if (hitBy === 'P1') { p1Score += 5; p1WrongStreak = 0; createExplosion(item.x, item.y, '#facc15'); } 
                            else { p2Score += 5; p2WrongStreak = 0; createExplosion(item.x, item.y, '#60a5fa'); }
                            updateScores(); triggerNextQuestion(); break;
                        } else {
                            playWrongSound();
                            // Sistem poin minus progresif: salah ke-1 -2, salah ke-2 -4, salah ke-3 -6, dst (bisa minus jika skor 0)
                            if (hitBy === 'P1') { p1WrongStreak++; p1Score -= p1WrongStreak * 2; createExplosion(item.x, item.y, '#ef4444'); } 
                            else { p2WrongStreak++; p2Score -= p2WrongStreak * 2; createExplosion(item.x, item.y, '#ef4444'); }
                            updateScores();
                        }
                    }
                }
            }

            if (!itemsActive && fallingItems.length > 0 && !isTransitioningQuestion) triggerNextQuestion();

            // P1 Pointer
            p1Hands.forEach(hp => {
                ctx.beginPath(); ctx.arc(hp.x, hp.y, 25, 0, Math.PI*2);
                ctx.fillStyle = 'rgba(250, 204, 21, 0.4)'; ctx.fill();
                ctx.lineWidth = 4; ctx.strokeStyle = '#facc15'; ctx.stroke();
                ctx.beginPath(); ctx.arc(hp.x, hp.y, 6, 0, Math.PI*2); ctx.fillStyle = '#ffffff'; ctx.fill();
            });

            // P2 Pointer
            p2Hands.forEach(hp => {
                ctx.beginPath(); ctx.arc(hp.x, hp.y, 25, 0, Math.PI*2);
                ctx.fillStyle = 'rgba(96, 165, 250, 0.4)'; ctx.fill();
                ctx.lineWidth = 4; ctx.strokeStyle = '#60a5fa'; ctx.stroke();
                ctx.beginPath(); ctx.arc(hp.x, hp.y, 6, 0, Math.PI*2); ctx.fillStyle = '#ffffff'; ctx.fill();
            });
        }

        const camera = new Camera(videoElement, {
            onFrame: async () => { try { await hands.send({ image: videoElement }); } catch (e) { console.error('Deteksi tangan error:', e); } },
            width: 640, height: 480
        });

        // Fungsi ini HARUS dipanggil langsung dari dalam event klik pengguna
        // (bukan otomatis saat halaman dimuat), karena browser (terutama Safari
        // di iPhone/iPad dan banyak browser IFP) hanya akan menampilkan dialog
        // izin kamera / menyalakan kamera jika permintaannya berasal dari
        // gesture pengguna secara langsung (klik/tap).
        let cameraStartRequested = false;
        let cameraStream = null;
        let aiResultCount = 0;
        let lastHandStatus = '';

        // Menampilkan status deteksi tangan di kotak status (layar awal) agar terlihat apakah AI bekerja
        function updateHandStatus(n) {
            const el = document.getElementById('handDetectStatus');
            if (!el) return;
            const txt = n > 0 ? ('Tangan terdeteksi ✓ (' + n + ' tangan)') : 'AI aktif. Angkat tangan di depan kamera...';
            if (txt === lastHandStatus) return;
            lastHandStatus = txt;
            el.textContent = txt;
            el.className = (n > 0 ? 'text-emerald-300' : 'text-yellow-300') + ' font-bold text-xs mt-1 text-center';
        }

        // Meminta izin kamera SECARA EKSPLISIT lewat getUserMedia agar dialog izin
        // muncul di browser/IFP. Setelah izin diberikan, stream langsung dilepas
        // dan MediaPipe Camera dijalankan seperti semula (tanpa prompt ulang).
        async function askCameraPermission() {
            const md = navigator.mediaDevices;
            if (!md || !md.getUserMedia) {
                const err = new Error('Insecure context / API kamera tidak tersedia');
                err.name = 'NoMediaDevicesError';
                throw err;
            }
            let stream;
            try {
                stream = await md.getUserMedia({
                    video: { facingMode: 'user', width: { ideal: 640 }, height: { ideal: 480 } },
                    audio: false
                });
            } catch (e) {
                // Jika hanya masalah resolusi/kamera depan, coba lagi dengan setelan paling sederhana
                if (e && (e.name === 'OverconstrainedError' || e.name === 'ConstraintNotSatisfiedError')) {
                    stream = await md.getUserMedia({ video: true, audio: false });
                } else {
                    throw e;
                }
            }
            return stream; // stream DIPAKAI ULANG agar izin tidak diminta dua kali
        }

        function cameraErrorMessage(err) {
            const n = err && err.name;
            if (n === 'ModelLoadError' || (err && /wasm|tflite|binarypb|fetch|network|load/i.test(err.message || ''))) return 'Model AI deteksi tangan gagal dimuat. Pastikan IFP terhubung internet dan jaringan sekolah tidak memblokir cdn.jsdelivr.net, lalu klik Coba Lagi.';
            if (n === 'NoMediaDevicesError') return 'Browser tidak mengizinkan akses kamera di halaman ini. Buka aplikasi lewat alamat HTTPS (https://...) atau localhost, bukan file lokal.';
            if (n === 'NotAllowedError' || n === 'PermissionDeniedError' || n === 'SecurityError') return 'Izin kamera ditolak/diblokir. Ketuk ikon gembok/kamera di address bar (atau pengaturan aplikasi IFP), ubah Kamera menjadi "Izinkan", lalu klik Coba Lagi.';
            if (n === 'NotFoundError' || n === 'DevicesNotFoundError') return 'Kamera tidak ditemukan pada perangkat ini. Pastikan kamera IFP/webcam terpasang.';
            if (n === 'NotReadableError' || n === 'TrackStartError') return 'Kamera sedang dipakai aplikasi/tab lain. Tutup aplikasi tersebut lalu klik Coba Lagi.';
            return 'Gagal mengakses kamera. Pastikan Anda menekan "Izinkan" saat browser meminta akses kamera.';
        }

        async function requestCameraAccess() {
            if (cameraStartRequested) return;
            cameraStartRequested = true;

            const statusDiv = document.getElementById('cameraStatus');
            statusDiv.innerHTML = '<div class="loader mb-2 w-8 h-8 border-4 border-t-indigo-500"></div><p class="text-yellow-400 font-bold text-sm">Meminta izin kamera...</p>';

            try {
                cameraStream = await askCameraPermission();   // memunculkan dialog izin kamera (hanya 1x)

                // Muat model AI tangan lebih dulu (butuh internet ke cdn.jsdelivr.net)
                statusDiv.innerHTML = '<div class="loader mb-2 w-8 h-8 border-4 border-t-indigo-500"></div><p class="text-yellow-400 font-bold text-sm text-center">Memuat model AI deteksi tangan... (mohon tunggu, butuh internet)</p>';
                await Promise.race([
                    hands.initialize(),
                    new Promise((_, rej) => setTimeout(() => { const e = new Error('Timeout model AI'); e.name = 'ModelLoadError'; rej(e); }, 60000))
                ]);

                // MediaPipe Camera akan memanggil getUserMedia lagi. Agar tidak muncul
                // dialog izin kedua, kirimkan stream yang sudah diizinkan tadi (sekali pakai).
                navigator.mediaDevices.getUserMedia = () => {
                    delete navigator.mediaDevices.getUserMedia; // kembalikan fungsi asli
                    return Promise.resolve(cameraStream);
                };
                try {
                    await camera.start();      // menjalankan kamera + AI seperti semula
                } finally {
                    delete navigator.mediaDevices.getUserMedia; // pastikan selalu kembali normal
                }
                statusDiv.classList.replace('bg-slate-800/80', 'bg-emerald-900/60');
                statusDiv.classList.replace('border-slate-700', 'border-emerald-500');
                statusDiv.innerHTML = '<p class="text-emerald-400 font-extrabold text-base">Kamera & AI Siap Digunakan! ✓</p><p id="handDetectStatus" class="text-yellow-300 font-bold text-xs mt-1 text-center">Menunggu AI... coba lambaikan tangan di depan kamera</p>';
                // Jika AI tidak pernah memberi hasil, tampilkan peringatan penyebab umum
                setTimeout(() => {
                    if (aiResultCount === 0) {
                        const el = document.getElementById('handDetectStatus');
                        if (el) { el.textContent = 'AI belum memberi hasil. Cek internet (cdn.jsdelivr.net tidak boleh diblokir) & coba muat ulang halaman.'; el.className = 'text-red-400 font-bold text-xs mt-1 text-center'; }
                    }
                }, 15000);
                document.getElementById('btnStart').disabled = false;
            } catch (err) {
                console.error('Kamera gagal:', err);
                cameraStartRequested = false;
                if (cameraStream) { cameraStream.getTracks().forEach(t => t.stop()); cameraStream = null; }
                statusDiv.innerHTML = '<p class="text-red-400 font-bold text-sm mb-2 text-center"></p><button id="btnEnableCamera" type="button" class="bg-red-600 hover:bg-red-500 text-white font-bold py-2 px-4 rounded-xl text-sm transition-all shadow-md">Coba Lagi</button>';
                statusDiv.querySelector('p').textContent = cameraErrorMessage(err);
                // Diagnosis tambahan: tampilkan status izin kamera yang tercatat di browser
                try {
                    if (navigator.permissions && navigator.permissions.query) {
                        navigator.permissions.query({ name: 'camera' }).then((r) => {
                            const info = document.createElement('p');
                            info.className = 'text-slate-400 font-bold text-xs mb-2 text-center';
                            info.textContent = 'Status izin kamera di browser: ' + r.state + ' (' + (err && err.name ? err.name : 'error') + ')';
                            statusDiv.insertBefore(info, statusDiv.querySelector('button'));
                        }).catch(() => {});
                    }
                } catch (e) {}
                document.getElementById('btnEnableCamera').addEventListener('click', requestCameraAccess);
            }
        }

        document.getElementById('btnEnableCamera').addEventListener('click', requestCameraAccess);

    </script>
</body>
</html>
