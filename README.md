[Uploading index_22_halte_bus(4).html…]()
<!DOCTYPE html><html lang="id" data-aes="AESC1-2026-10C8CD16"><head> <meta charset="UTF-8" /><meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" /><title>AES CLASS (PREVIEW tanpa login)</title><meta name="copyright" content="© 2026 AES CLASS. Seluruh hak cipta dilindungi. Dilarang menyalin, memodifikasi, merapikan ulang, atau mendistribusikan kode ini tanpa izin tertulis, termasuk dengan bantuan alat AI." /><meta name="author" content="AES CLASS" /><meta name="aes-build" content="AESC1-2026-10C8CD16" /> <script>window.__aesOk=function(){return!0};</script> <script src="https://cdn.tailwindcss.com"></script> <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script> <script src="https://unpkg.com/mqtt/dist/mqtt.min.js"></script> <script src="https://cdnjs.cloudflare.com/ajax/libs/lz-string/1.4.4/lz-string.min.js"></script> <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script> <script>window.MathJax={tex:{inlineMath:[["$","$"],["\\(","\\)"]],displayMath:[["$$","$$"],["\\[","\\]"]]},svg:{fontCache:"global"}};</script> <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js"></script> <style>@import"https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;700;800&display=swap";body{font-family:Plus Jakarta Sans,"Noto Sans","Segoe UI","Noto Sans Arabic","Noto Sans Hebrew","Noto Sans JP","Hiragino Sans","Yu Gothic","Noto Sans KR","Malgun Gothic","Noto Sans SC","Microsoft YaHei","PingFang SC","Noto Sans TC","Noto Sans Devanagari","Nirmala UI","Noto Sans Thai","Arial Unicode MS",sans-serif;overflow:hidden;user-select:none;background-color:#0f172a;margin:0;padding:0;touch-action:none}#canvas-container{position:fixed;top:0;left:0;width:100vw;height:100vh;z-index:1}.ui-layer{position:relative;z-index:10}.glass{background:#0f172aeb;border:1px solid rgba(255,255,255,.25)}.glass-light{background:#0f172acc;border:1px solid rgba(56,189,248,.45)}.custom-scroll::-webkit-scrollbar{width:6px;height:6px}.custom-scroll::-webkit-scrollbar-track{background:#0f172a59;border-radius:9999px}.custom-scroll::-webkit-scrollbar-thumb{background:#38bdf8bf;border-radius:9999px}@keyframes pulse-glow{0%,to{transform:scale(.96);box-shadow:0 0 15px #facc1599}50%{transform:scale(1.04);box-shadow:0 0 30px #facc15}}.animate-pulse-glow{animation:pulse-glow 1.8s infinite ease-in-out}.fs-start-btn{position:absolute;top:10px;right:10px;z-index:5;width:34px;height:34px;border-radius:10px;background:#0f172ab8;color:#bae6fd;border:1px solid rgba(255,255,255,.28);font-size:17px;line-height:1;font-weight:800;cursor:pointer;display:flex;align-items:center;justify-content:center;transition:background .15s}.fs-start-btn:hover{background:#0ea5e9d9;color:#fff}.fs-start-btn.hidden{display:none}#hud-left-card.teacher-hud #hud-left-header{flex-wrap:wrap;row-gap:6px}#hud-left-card.teacher-hud #hud-title-block{flex:1 1 100%;overflow:visible;white-space:normal}#hud-left-card.teacher-hud #hud-player-name{white-space:normal;overflow:visible;text-overflow:clip}#hud-left-card.teacher-hud #hud-btn-row{flex:1 1 100%;justify-content:space-between}#hud-left-card.teacher-hud #hud-btn-row>button{flex:1 1 0;min-width:0;padding-left:4px;padding-right:4px}.wrap-anywhere{overflow-wrap:anywhere;word-break:break-word;white-space:normal}
.aes-video{position:relative;width:100%;aspect-ratio:16/9;margin:10px 0 4px;border-radius:12px;overflow:hidden;background:#000;border:1px solid rgba(56,189,248,.35)}
.aes-video iframe{position:absolute;inset:0;width:100%;height:100%;border:0}
.aes-vid{display:block;width:100%;max-height:60vh;border-radius:12px;margin:8px 0;background:#000}
.aes-link{color:#7dd3fc;text-decoration:underline;word-break:break-all}
#quiz-options-grid img,#building-quiz-options img,.rn-opt img{max-height:90px;max-width:100%;object-fit:contain;margin:2px 0;border-radius:8px}
#quiz-options-grid .my-3,#building-quiz-options .my-3,.rn-opt .my-3{margin:2px 0}
#quiz-options-grid a,#building-quiz-options a,.rn-opt a{pointer-events:none;color:inherit;text-decoration:none}
#quiz-options-grid .aes-video,#building-quiz-options .aes-video,.rn-opt .aes-video,#quiz-options-grid video,#building-quiz-options video,.rn-opt video{display:none}
#modal-building-content,#quiz-question-text,#building-quiz-question,#quiz-options-grid span,#building-quiz-options button,#rn-qtext,.rn-opt span,#questions-editor-list textarea,#questions-editor-list input[type=text],#buildings-editor-list textarea,#buildings-editor-list input[type=text]{unicode-bidi:plaintext}
.aes-ins-bar{position:sticky;top:0;z-index:25;display:flex;flex-wrap:wrap;gap:6px;align-items:center;padding:8px 10px;margin-bottom:10px;background:rgba(15,23,42,.97);border:1px solid rgba(56,189,248,.4);border-radius:12px;font-size:11px;font-weight:700;color:#bae6fd}
.aes-ins-bar button,.aes-sym button{padding:5px 10px;border-radius:9px;border:1px solid rgba(255,255,255,.25);background:rgba(255,255,255,.08);color:#fff;font-size:11px;font-weight:800;cursor:pointer}
.aes-ins-bar button:hover,.aes-sym button:hover{background:rgba(56,189,248,.3)}
.aes-sym{flex-basis:100%;max-height:34vh;overflow-y:auto;padding:6px 2px 2px}
.aes-sym .g{margin-bottom:6px}.aes-sym .gl{font-size:10px;color:#94a3b8;margin-bottom:3px}
.aes-sym button{min-width:30px;padding:4px 7px;font-size:13px;font-weight:600}
#aes-prev{position:fixed;inset:0;z-index:99999;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.75)}
#aes-prev .bx{max-width:min(92vw,720px);max-height:85vh;overflow:auto;background:#0f172a;color:#e2e8f0;padding:16px;border-radius:16px;border:1px solid rgba(56,189,248,.5);white-space:pre-line;line-height:1.6;font-size:14px;unicode-bidi:plaintext}
</style> <style>@media(max-height:570px){html{font-size:clamp(9px,2.8vh,16px)!important}#hud-top-bar{padding:6px!important;gap:6px!important}#hud-left-card,#hud-right-card{padding:.5rem!important}#hud-right-card{width:15rem!important}#hud-online-list{max-height:4.5rem!important}#aes-hud-ctl{display:flex}}#aes-hud-ctl{display:none;position:fixed;top:4px;left:50%;transform:translate(-50%);z-index:9500;gap:6px;align-items:center}#aes-hud-ctl button{width:30px;height:30px;border-radius:9px;background:#0f172acc;color:#bae6fd;border:1px solid rgba(255,255,255,.3);font-size:15px;line-height:1;padding:0;cursor:pointer;touch-action:manipulation}#aes-hud-ctl button.off{opacity:.45}html.aes-hide-left #hud-left-card,html.aes-hide-map #hud-right-card{display:none!important}#hud-top-bar.teacher-monitor-offset{align-items:flex-start}#hud-top-bar.teacher-monitor-offset #hud-center-card{margin-top:2.6rem;flex:1 1 0;min-width:0;max-width:38rem}#hud-top-bar.teacher-monitor-offset #hud-location-indicator{display:none}#hud-top-bar.teacher-monitor-offset #hud-left-card,#hud-top-bar.teacher-monitor-offset #hud-right-card{width:19rem;flex:0 0 19rem}@media(max-width:1100px){#hud-top-bar.teacher-monitor-offset #hud-left-card,#hud-top-bar.teacher-monitor-offset #hud-right-card{width:17.5rem;flex-basis:17.5rem}}#camera-control-box{position:fixed;right:.6rem;top:60%;z-index:15;display:flex;flex-direction:row-reverse;align-items:center;gap:.4rem}#cam-toggle{width:2.4rem;height:2.4rem;border-radius:9999px;font-size:1.05rem;display:flex;align-items:center;justify-content:center;cursor:pointer;flex:0 0 auto}#cam-panel{width:9.5rem;padding:.4rem .5rem;gap:.25rem;border-radius:.75rem;display:none;flex-direction:column}#camera-control-box.open #cam-panel{display:flex}#cam-panel .cam-title{font-size:9px}#cam-panel .cam-btns button{padding:1px 0;font-size:11px;line-height:1.3}</style></head><body class="text-slate-100" onclick="unlockAudioOnFirstInteraction()"><div id="conn-warning" class="hidden fixed top-2 left-1/2 -translate-x-1/2 px-4 py-2 rounded-full bg-amber-400 text-slate-950 text-xs font-extrabold shadow-lg text-center" style="z-index:9000;pointer-events:none;max-width:92vw">⚠️ Belum tersambung ke server kelas… sedang mencoba lagi. Cek internet / jaringan sekolah.</div><div id="access-gate" class="fixed inset-0 overflow-y-auto bg-slate-950" style="z-index:9999;display:none"><div class="min-h-full flex items-center justify-center p-4"><div class="relative max-w-md w-full glass rounded-3xl p-6 md:p-8 border border-sky-300/40 shadow-2xl space-y-4 text-center"><div class="w-16 h-16 rounded-2xl bg-sky-400/20 border border-sky-300/40 flex items-center justify-center mx-auto text-3xl">🔐</div><div><span class="px-3 py-1 bg-amber-400 text-slate-950 text-xs font-extrabold rounded-full">AES CLASS</span><h1 class="text-2xl font-extrabold text-white mt-2">Masuk AES CLASS</h1><p class="text-xs text-sky-200 mt-1">Masukkan email aktifmu dan password dari admin.</p></div><div id="gate-tabs" style="display:none" class="grid grid-cols-2 gap-2 bg-slate-950/60 p-1 rounded-2xl"><button id="gate-tab-login" onclick="gateSetMode('login')" class="py-2 rounded-xl text-sm font-extrabold">Masuk</button><button id="gate-tab-register" onclick="gateSetMode('register')" class="py-2 rounded-xl text-sm font-extrabold">Daftar</button></div><div class="text-left space-y-2"><input id="gate-nama" type="text" placeholder="Nama lengkap" class="hidden w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white font-semibold focus:border-sky-400 focus:outline-none" style="user-select:text" /><input id="gate-email" type="email" placeholder="Email" autocomplete="username" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white font-semibold focus:border-sky-400 focus:outline-none" style="user-select:text" /><input id="gate-pass" type="password" placeholder="Password" autocomplete="current-password" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white font-semibold focus:border-sky-400 focus:outline-none" style="user-select:text" /><input id="gate-key" type="password" placeholder="Kunci Admin" class="hidden w-full bg-slate-900 border border-amber-400 rounded-xl px-4 py-3 text-white font-semibold focus:outline-none" style="user-select:text" /></div><div id="gate-wait" class="hidden bg-amber-400/15 border border-amber-300/50 rounded-2xl p-3 text-left"><p class="text-sm font-extrabold text-amber-300">⏳ Menunggu persetujuan admin</p><p class="text-xs text-amber-100 mt-1">Akunmu sudah terdaftar. Hubungi admin lewat kontak di bawah, lalu klik tombol untuk mengecek status.</p></div><p id="gate-msg" class="text-sm font-bold text-amber-300 min-h-[1.25rem]"></p><button id="gate-btn" onclick="gateSubmit()" class="w-full py-3.5 bg-gradient-to-r from-sky-400 to-blue-500 hover:from-sky-300 hover:to-blue-400 text-slate-950 font-extrabold rounded-xl shadow-lg transition">Masuk</button><button id="gate-admin-toggle" style="display:none" onclick="gateAdminToggle()" class="text-xs text-sky-300 hover:text-white transition">🛡️ Masuk sebagai Admin</button><div class="border-t border-slate-700 pt-4 space-y-3"><p class="text-xs font-bold text-sky-100">Belum punya password? Hubungi admin</p><div class="flex items-center justify-center gap-4"><a href="https://wa.me/6285397772345" target="_blank" rel="noopener" title="WhatsApp 0853-9777-2345" class="w-12 h-12 rounded-full bg-emerald-500 hover:bg-emerald-400 flex items-center justify-center shadow-lg transition"><svg viewBox="0 0 24 24" width="26" height="26" fill="#fff"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/></svg></a><a href="https://www.instagram.com/aes_435" target="_blank" rel="noopener" title="Instagram @aes_435" class="w-12 h-12 rounded-full flex items-center justify-center shadow-lg transition hover:opacity-90" style="background:linear-gradient(45deg,#f9a825,#e1306c,#833ab4)"><svg viewBox="0 0 24 24" width="26" height="26" fill="none" stroke="#fff" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.3" cy="6.7" r="1" fill="#fff" stroke="none"/></svg></a><a href="https://www.tiktok.com/@aes_435" target="_blank" rel="noopener" title="TikTok @aes_435" class="w-12 h-12 rounded-full bg-black hover:bg-slate-800 border border-slate-600 flex items-center justify-center shadow-lg transition"><svg viewBox="0 0 24 24" width="24" height="24" fill="#fff"><path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/></svg></a></div><p class="text-[11px] text-slate-400">Aplikasi ini dibuat oleh AES</p></div><button type="button" onclick="toggleFullScreen()" title="Layar penuh" aria-label="Layar penuh" class="fs-start-btn hidden" style="margin:0!important">⛶</button></div></div></div><button id="admin-fab" onclick="adminOpen()" style="display:none;position:fixed;left:12px;bottom:12px;z-index:9000" class="px-4 py-2.5 bg-rose-500 hover:bg-rose-400 text-white rounded-2xl text-xs font-extrabold shadow-xl border-2 border-white">🛡️ Panel Admin</button><div id="admin-panel" class="fixed inset-0 p-3 md:p-6 bg-slate-950/95" style="z-index:10000;display:none"><div class="max-w-4xl mx-auto h-full flex flex-col glass rounded-3xl p-4 md:p-6 border border-rose-300/40 shadow-2xl"><div class="flex items-center justify-between gap-2 pb-3 border-b border-slate-700"><h2 class="text-lg md:text-xl font-extrabold text-white">🛡️ Panel Admin — Pengguna Masuk</h2><div class="flex gap-2"><button onclick="adminRefresh()" class="px-3 py-2 bg-sky-500 hover:bg-sky-400 text-slate-950 rounded-xl text-xs font-extrabold">↻ Muat Ulang</button><button onclick="adminClose()" class="px-3 py-2 bg-slate-700 hover:bg-slate-600 text-white rounded-xl text-xs font-extrabold">✕ Tutup</button></div></div><div id="admin-filters" class="grid grid-cols-2 md:grid-cols-4 gap-2 py-3"></div><input id="admin-search" type="text" oninput="adminRender()" placeholder="🔍 Cari email pengguna..." class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-2.5 text-white text-sm font-semibold focus:border-sky-400 focus:outline-none mb-2" style="user-select:text" /><p id="admin-info" class="text-xs text-amber-300 pb-2"></p><div id="admin-list" class="flex-1 overflow-y-auto custom-scroll space-y-2 pr-1" style="user-select:text"></div></div></div><div id="canvas-container"></div><div id="teacher-screen" class="ui-layer fixed inset-0 overflow-y-auto custom-scroll bg-slate-900/90 backdrop-blur-md p-4 md:p-8 hidden"><div class="max-w-7xl mx-auto space-y-6 pb-28"><div class="relative flex flex-col lg:flex-row lg:items-center justify-between gap-4 bg-gradient-to-r from-sky-600 via-blue-700 to-indigo-900 p-6 rounded-3xl border border-sky-300/40 shadow-2xl"><button type="button" onclick="toggleFullScreen()" title="Layar penuh" aria-label="Layar penuh" class="fs-start-btn hidden" style="margin:0!important">⛶</button><div><span class="px-3.5 py-1 text-xs font-extrabold uppercase tracking-widest bg-amber-400 text-slate-950 rounded-full shadow">MEDIA PEMBELAJARAN INTERAKTIF 3D</span><h1 class="text-3xl md:text-4xl font-extrabold mt-2 text-white tracking-tight">AES CLASS</h1><p class="text-sky-100 text-sm mt-1">Kelola materi gedung (G1 s.d. G20), unduh prompt simpel, impor/paste JSON, pantau jawaban kuis secara real-time, dan unduh refleksi siswa.</p></div><div class="flex flex-wrap items-center gap-2"><button onclick="toggleBGM()" id="btn-teacher-bgm" class="px-3 py-2.5 bg-slate-900/70 hover:bg-slate-900 text-emerald-300 rounded-2xl text-xs font-extrabold border border-emerald-400/40 transition shadow-lg">🎵 Musik: ON</button><button onclick="toggleSFX()" id="btn-teacher-sfx" class="px-3 py-2.5 bg-slate-900/70 hover:bg-slate-900 text-sky-200 rounded-2xl text-xs font-extrabold border border-sky-400/40 transition shadow-lg">🔊 SFX: ON</button><button onclick="aesGfxOpen()" id="btn-teacher-gfx" class="px-3 py-2.5 bg-slate-900/70 hover:bg-slate-900 text-amber-300 rounded-2xl text-xs font-extrabold border border-amber-400/40 transition shadow-lg">🖥️ Grafik: Otomatis</button><button onclick="downloadDocxPromptTemplate()" class="px-4 py-2.5 bg-yellow-300 hover:bg-yellow-200 text-slate-950 rounded-2xl text-xs md:text-sm font-extrabold transition flex items-center gap-2 shadow-xl border-2 border-white"><span>📄 Unduh Prompt Simpel (.docx)</span></button><label class="px-4 py-2.5 bg-sky-400 hover:bg-sky-300 text-slate-950 rounded-2xl text-xs md:text-sm font-extrabold cursor-pointer transition flex items-center gap-2 shadow-lg"><span>📂 Impor File JSON</span><input type="file" id="json-upload" accept=".json" class="hidden" onchange="importJSON(event)" /></label><button onclick="openPasteJsonModal()" class="px-4 py-2.5 bg-amber-400 hover:bg-amber-300 text-slate-950 rounded-2xl text-xs md:text-sm font-extrabold transition shadow-lg">📋 Paste Kode JSON</button><button onclick="exportCurrentConfigJSON()" class="px-3.5 py-2.5 bg-indigo-500 hover:bg-indigo-400 text-white rounded-2xl text-xs font-extrabold transition shadow-lg">💾 Simpan .JSON</button><button onclick="shuffleAnswerKeysNow()" class="px-3.5 py-2.5 bg-fuchsia-500 hover:bg-fuchsia-400 text-white rounded-2xl text-xs font-extrabold transition shadow-lg">🔀 Acak Kunci Jawaban</button><button onclick="enterTeacher3DMonitor()" class="px-4 py-2.5 bg-emerald-400 hover:bg-emerald-300 text-slate-950 rounded-2xl text-xs md:text-sm font-extrabold transition shadow-lg">🏙️ Lihat Dunia 3D</button></div></div><div id="session-live-box" class="hidden bg-slate-900/95 border-2 border-sky-400 rounded-3xl p-6 shadow-2xl space-y-5"><div id="session-restored-note" class="hidden flex flex-col sm:flex-row sm:items-center justify-between gap-3 bg-emerald-500/15 border border-emerald-400/50 rounded-2xl px-4 py-3"><span id="session-restored-text" class="text-sm font-bold text-emerald-200"></span><button onclick="tsClearAndRestart()" class="shrink-0 px-3 py-1.5 bg-slate-800 hover:bg-slate-700 text-rose-300 border border-rose-400/40 rounded-lg text-xs font-extrabold">Mulai dari awal</button></div><div class="flex flex-col lg:flex-row lg:items-center justify-between gap-4 border-b border-slate-800 pb-4"><div><div class="flex items-center gap-2.5"><span class="w-3.5 h-3.5 rounded-full bg-emerald-400 animate-ping"></span><h2 class="text-xl font-extrabold text-sky-300">Panel Kendali, Statistik Kuis Real-Time & Refleksi — AES CLASS</h2></div><p class="text-xs md:text-sm text-slate-300 mt-1">Biarkan tab Guru ini tetap terbuka agar materi tersinkronisasi otomatis ke siswa.</p></div><div class="flex items-center gap-3 bg-slate-950 px-4 py-2.5 rounded-2xl border border-slate-700"><div class="text-right"><div class="text-[10px] font-bold uppercase text-slate-400">Status Kelas</div><div id="teacher-phase-status" class="text-sm font-extrabold text-amber-400">MENUNGGU GURU MEMULAI</div></div><div class="h-8 w-px bg-slate-800"></div><div><div class="text-[10px] font-bold uppercase text-slate-400">Sisa Waktu</div><div id="teacher-live-timer" class="text-xl font-mono font-extrabold text-white">30:00</div></div></div></div><div id="local-file-warning" class="hidden bg-amber-500/20 border border-amber-400 text-amber-200 px-4 py-3 rounded-2xl text-xs leading-relaxed"> ⚠️ <b>Perhatian:</b> Anda membuka file ini dari komputer lokal (<code class="text-white">file:///</code>). Unggah ke hosting gratis (GitHub Pages / Netlify / Vercel) agar link bisa dibuka dari perangkat siswa lain. </div><div class="flex flex-wrap items-center gap-2 text-xs"><span id="aes-conn-chip" class="px-3 py-1.5 rounded-full bg-slate-800 border border-slate-600 font-bold" style="color:#fcd34d">⏳ Menyambung ke server…</span><label class="text-slate-300 font-bold" for="aes-broker-select">Server:</label><select id="aes-broker-select" onchange="aesSwitchBroker(this.value,false)" class="bg-slate-950 border border-slate-700 rounded-lg px-2 py-1 text-slate-200"></select><span class="text-slate-400">Jika siswa tidak bisa mulai/nama salah, ganti server lalu salin ulang Link Siswa.</span></div><div id="aes-share-panel" class="space-y-3"><div class="space-y-1.5"><div class="text-[11px] font-extrabold uppercase tracking-wider text-sky-400">🔗 Link Panjang <span class="normal-case font-bold text-slate-400">(memuat semua soal)</span></div><div class="flex flex-col sm:flex-row gap-2.5"><input id="generated-link" type="text" readonly class="flex-1 min-w-0 bg-slate-950 border border-sky-500/40 rounded-xl px-4 py-3 text-xs md:text-sm text-sky-200 font-mono focus:outline-none" /><button onclick="copyStudentLink()" class="px-5 py-3 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold rounded-xl text-xs md:text-sm transition shrink-0">📋 Salin Link Panjang</button></div></div><div class="space-y-1.5"><div class="text-[11px] font-extrabold uppercase tracking-wider text-sky-400">⚡ Link Pendek <span class="normal-case font-bold text-slate-400">(soal diambil dari server)</span></div><div class="flex flex-col sm:flex-row gap-2.5"><input id="generated-link-short" type="text" readonly class="flex-1 min-w-0 bg-slate-950 border border-sky-500/40 rounded-xl px-4 py-3 text-xs md:text-sm text-sky-200 font-mono focus:outline-none" /><button onclick="aesCopyShortLink()" class="px-5 py-3 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold rounded-xl text-xs md:text-sm transition shrink-0">📋 Salin Link Pendek</button></div></div><div class="flex flex-wrap items-center gap-3 bg-slate-950/90 p-3 rounded-2xl border border-slate-800"><div class="bg-white p-1.5 rounded-xl shrink-0"><canvas id="aes-qr-canvas" width="150" height="150" style="width:132px;height:132px;image-rendering:pixelated;display:block"></canvas></div><div class="space-y-2"><div class="text-[11px] font-extrabold uppercase tracking-wider text-sky-400">▦ Barcode Siswa <span class="normal-case font-bold text-slate-400">(isinya link pendek)</span></div><div class="flex flex-wrap gap-2"><button onclick="aesShowQrBig()" class="px-4 py-2.5 bg-slate-800 hover:bg-slate-700 border border-slate-600 text-slate-100 font-extrabold rounded-xl text-xs transition">🔍 Tampilkan Besar</button><button onclick="aesDownloadQr()" class="px-4 py-2.5 bg-slate-800 hover:bg-slate-700 border border-slate-600 text-slate-100 font-extrabold rounded-xl text-xs transition">⬇️ Unduh Barcode</button></div></div></div><div class="flex flex-wrap gap-2.5 items-center"><button onclick="aesResetLink()" class="px-4 py-3 bg-rose-500 hover:bg-rose-400 text-white font-extrabold rounded-xl text-xs md:text-sm transition shrink-0">🔄 Reset Link (buat link baru)</button><button onclick="switchToStudentModeDirectly()" class="px-4 py-3 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold rounded-xl text-xs md:text-sm transition shrink-0">🤖 Uji Coba Jadi Siswa</button></div><div id="aes-reset-note" class="rounded-xl px-3 py-2 text-xs font-bold leading-relaxed" style="display:none"></div></div><div class="grid grid-cols-1 md:grid-cols-2 gap-4 pt-1"><div class="bg-slate-950/90 p-4 rounded-2xl border border-slate-800 space-y-2.5"><div class="text-xs font-extrabold uppercase tracking-wider text-sky-400">🎛️ 1. Kendali Tahapan Kelas & Refleksi</div><div class="grid grid-cols-2 sm:grid-cols-4 gap-2"><button onclick="teacherStartLearningPhase()" class="px-3 py-2.5 bg-emerald-500 hover:bg-emerald-400 text-slate-950 font-extrabold rounded-xl text-xs transition shadow-md">▶️ Mulai Belajar</button><button onclick="teacherCallToDockPhase()" class="px-3 py-2.5 bg-amber-500 hover:bg-amber-400 text-slate-950 font-extrabold rounded-xl text-xs transition shadow-md">🧭 Ke Dermaga</button><button onclick="teacherStartBoatRace()" class="px-3 py-2.5 bg-rose-500 hover:bg-rose-400 text-white font-extrabold rounded-xl text-xs transition shadow-md">🏁 Mulai Lomba!</button><button onclick="teacherStartReflectionPhase()" class="px-3 py-2.5 bg-purple-500 hover:bg-purple-400 text-white font-extrabold rounded-xl text-xs transition shadow-md border border-purple-300">📝 Klik Refleksi</button></div></div><div class="bg-slate-950/90 p-4 rounded-2xl border border-slate-800 space-y-2.5"><div class="text-xs font-extrabold uppercase tracking-wider text-amber-400">⏱️ 2. Tambah / Kurangi Waktu Belajar</div><div class="flex flex-wrap items-center gap-2"><button onclick="teacherAdjustTime(300)" class="px-3.5 py-2 bg-emerald-500/20 hover:bg-emerald-500/30 text-emerald-300 border border-emerald-500/40 rounded-xl text-xs font-extrabold transition">+5 Menit</button><button onclick="teacherAdjustTime(60)" class="px-3.5 py-2 bg-emerald-500/20 hover:bg-emerald-500/30 text-emerald-300 border border-emerald-500/40 rounded-xl text-xs font-extrabold transition">+1 Menit</button><button onclick="teacherAdjustTime(-60)" class="px-3.5 py-2 bg-rose-500/20 hover:bg-rose-500/30 text-rose-300 border border-rose-500/40 rounded-xl text-xs font-extrabold transition">-1 Menit</button><button onclick="teacherAdjustTime(-300)" class="px-3.5 py-2 bg-rose-500/20 hover:bg-rose-500/30 text-rose-300 border border-rose-500/40 rounded-xl text-xs font-extrabold transition">-5 Menit</button><button onclick="enterTeacher3DMonitor()" class="ml-auto px-3.5 py-2 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold rounded-xl text-xs transition">🎥 Pantau Lomba 3D</button></div></div></div><div class="bg-slate-950/90 rounded-2xl p-4 border border-slate-800 space-y-3"><div class="flex flex-wrap items-center justify-between gap-2"><div><h3 class="font-bold text-sky-300 text-xs md:text-sm uppercase tracking-wider">📊 Laporan Real-Time: Jawaban Benar/Salah, Nilai & Isi Refleksi Siswa</h3><p class="text-[11px] text-slate-400">Data Benar/Salah terupdate secara langsung (real-time) setiap kali siswa menjawab soal tanpa menunggu sampai finish.</p></div><div class="flex flex-wrap gap-2"><button onclick="exportStudentReportDOCX()" class="px-4 py-2.5 bg-emerald-500 hover:bg-emerald-400 text-slate-950 rounded-xl text-xs font-extrabold transition shadow-lg">📄 Download Laporan Nilai (.docx)</button><button onclick="exportStudentReflectionDOCX()" class="px-4 py-2.5 bg-purple-500 hover:bg-purple-400 text-white rounded-xl text-xs font-extrabold transition shadow-lg border border-purple-300">📄 Download Laporan Refleksi (.docx)</button><button onclick="exportStudentNotesDOCX()" class="px-4 py-2.5 bg-sky-500 hover:bg-sky-400 text-slate-950 rounded-xl text-xs font-extrabold transition shadow-lg border border-sky-300">📄 Download Catatan Gedung (.docx)</button><button onclick="exportStudentFullRecapDOCX()" class="px-4 py-2.5 bg-amber-400 hover:bg-amber-300 text-slate-950 rounded-xl text-xs font-extrabold transition shadow-lg border-2 border-white">📦 Download REKAP LENGKAP (.docx)</button></div></div><div class="overflow-x-auto custom-scroll"><table class="w-full text-left border-collapse text-xs md:text-sm"><thead><tr class="border-b border-slate-800 text-slate-300 text-xs uppercase bg-slate-900/60"><th class="py-3 px-3">Nama Siswa</th><th class="py-3 px-3">Status & Lokasi</th><th class="py-3 px-3">Gedung & Catatan</th><th class="py-3 px-3">Progres Soal</th><th class="py-3 px-3 text-emerald-300">Putaran 1 (Dihitung Nilai)</th><th class="py-3 px-3 text-amber-300">Diulangi (Tanpa Poin)</th><th class="py-3 px-3 text-center">Nilai Real-Time</th><th class="py-3 px-3 text-purple-300">Status & Isi Refleksi</th><th class="py-3 px-3 text-right">Kamera</th></tr></thead><tbody id="teacher-student-table-body" class="divide-y divide-slate-800/80 text-slate-100"><tr><td colspan="9" class="py-4 text-center text-slate-500 italic">Menunggu siswa bergabung melalui link...</td></tr></tbody></table></div></div></div><div class="grid grid-cols-1 lg:grid-cols-3 gap-6"><div class="bg-slate-900/95 border border-slate-800 rounded-2xl p-5 space-y-4"><h2 class="text-base font-extrabold text-sky-400">⏱️ 1. Waktu & Jumlah Gedung Materi</h2><div><label class="block text-xs font-semibold text-slate-400 uppercase mb-1">Durasi Awal Belajar (Menit)</label><input id="input-timer" type="number" min="1" max="240" value="30" class="w-full bg-slate-950 border border-slate-700 rounded-xl px-4 py-2.5 text-white font-bold focus:border-sky-400 focus:outline-none" /></div><div><label class="block text-xs font-semibold text-slate-400 uppercase mb-1">Jumlah Sub-Materi / Gedung Aktif (G1 s.d. G20)</label><div class="flex gap-2"><input id="input-building-count" type="number" min="1" max="20" value="5" onchange="adjustBuildingsCount(this.value)" class="w-full bg-slate-950 border border-slate-700 rounded-xl px-4 py-2.5 text-white font-bold focus:border-sky-400 focus:outline-none" /><button onclick="addBuildingItem()" class="px-4 py-2 bg-sky-500 hover:bg-sky-400 text-slate-950 font-extrabold rounded-xl text-xs shrink-0">+ Tambah</button></div></div></div><div class="lg:col-span-2 bg-slate-900/95 border border-slate-800 rounded-2xl p-5 space-y-3"><div class="flex items-center justify-between"><h2 class="text-base font-extrabold text-sky-400">👩‍🎓 2. Daftar Nama Siswa (Satu Baris Satu Nama, boleh kosong)</h2><span class="text-xs text-slate-400">Boleh dikosongkan — siswa mengetik namanya sendiri saat membuka link</span></div> <textarea id="input-students" rows="5" class="w-full bg-slate-950 border border-slate-700 rounded-xl p-3.5 text-sm text-slate-100 focus:border-sky-400 focus:outline-none custom-scroll"></textarea> </div></div><div class="bg-slate-900/95 border border-slate-800 rounded-2xl p-5 space-y-4"><div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2"><div><h2 class="text-base font-extrabold text-sky-400">🏢 3. Daftar Gedung Materi Berurutan (G1, G2, G3...)</h2><p class="text-xs text-slate-400">Pilih jenis arsitektur gedung 3D yang diinginkan untuk masing-masing sub-materi.</p></div><button onclick="addBuildingItem()" class="px-4 py-2 bg-sky-500/20 hover:bg-sky-500/30 text-sky-300 border border-sky-400/30 rounded-xl text-xs font-bold transition">+ Tambah Gedung Materi</button></div><div id="buildings-editor-list" class="grid grid-cols-1 md:grid-cols-2 gap-4"></div></div><div class="bg-slate-900/95 border border-slate-800 rounded-2xl p-5 space-y-4"><div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2"><div><h2 class="text-base font-extrabold text-amber-400">🚤 4. Daftar Soal Lomba Perahu Menuju Pulau Victory</h2><p class="text-xs text-slate-400">Mendukung soal pilihan ganda beserta rumus matematika.</p></div><button onclick="addQuestionItem()" class="px-4 py-2 bg-amber-500/20 hover:bg-amber-500/30 text-amber-300 border border-amber-400/30 rounded-xl text-xs font-bold transition">+ Tambah Soal Pilihan Ganda</button></div><div id="questions-editor-list" class="space-y-4"></div></div><div class="sticky bottom-4 z-20 flex flex-wrap justify-end gap-3"><button onclick="switchToStudentModeDirectly()" class="px-6 py-4 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold text-sm rounded-2xl shadow-2xl transition">🤖 Simulasi Main Sebagai Siswa</button><button onclick="generateSessionAndLink()" class="px-8 py-4 bg-gradient-to-r from-sky-400 to-blue-600 hover:from-sky-300 hover:to-blue-500 text-white font-extrabold text-sm md:text-base rounded-2xl shadow-2xl transition">🚀 Simpan & Buat Link Kelas Multiplayer</button></div></div></div><div id="paste-json-modal" class="ui-layer fixed inset-0 bg-slate-950/85 backdrop-blur-md flex items-center justify-center p-4 hidden z-50"><div class="max-w-2xl w-full bg-slate-900 border-2 border-amber-400 rounded-3xl p-6 space-y-4 shadow-2xl"><div class="flex items-center justify-between border-b border-slate-800 pb-3"><div><span class="px-2.5 py-0.5 bg-amber-400 text-slate-950 font-extrabold text-[11px] rounded-full">TANPA RIBET BUAT FILE</span><h3 class="text-lg font-extrabold text-white mt-1">📋 Tempel (Paste) Kode JSON dari ChatGPT / Gemini</h3></div><button onclick="closePasteJsonModal()" class="px-3 py-1 bg-rose-500/20 text-rose-300 rounded-xl text-xs font-bold">✕ Tutup</button></div> <textarea id="paste-json-textarea" rows="10" class="w-full bg-slate-950 border border-slate-700 rounded-2xl p-3.5 text-xs font-mono text-emerald-300 focus:border-amber-400 focus:outline-none custom-scroll" placeholder='Paste kode JSON di sini...'></textarea> <div class="flex flex-wrap justify-between items-center gap-2 pt-1"><button onclick="applyPastedJSONAndDownload()" class="px-4 py-2.5 bg-indigo-500 hover:bg-indigo-400 text-white font-extrabold rounded-xl text-xs transition">💾 Terapkan & Download File .JSON</button><div class="flex gap-2"><button onclick="closePasteJsonModal()" class="px-4 py-2.5 bg-slate-800 text-slate-300 font-bold rounded-xl text-xs">Batal</button><button onclick="applyPastedJSON(false)" class="px-6 py-2.5 bg-emerald-400 hover:bg-emerald-300 text-slate-950 font-extrabold rounded-xl text-xs shadow-lg transition">✅ Terapkan Sekarang</button></div></div></div></div><div id="student-login-screen" class="ui-layer fixed inset-0 flex items-center justify-center p-4 bg-sky-950/60 backdrop-blur-md hidden"><div class="relative max-w-md w-full glass rounded-3xl p-6 md:p-8 border border-sky-300/40 shadow-2xl space-y-6 text-center"><div class="w-16 h-16 rounded-2xl bg-sky-400/20 border border-sky-300/40 flex items-center justify-center mx-auto text-3xl shadow-inner">🤖</div><div><span class="px-3 py-1 bg-amber-400 text-slate-950 text-xs font-extrabold rounded-full">AES CLASS</span><h1 class="text-2xl font-extrabold text-white mt-2">Pilih Robot & Namamu</h1><p id="student-sync-notice" class="text-xs text-emerald-300 mt-1 font-semibold">Terhubung ke Kelas! Pilih namamu untuk mulai menjelajah gedung G1, G2, G3...</p></div><div class="text-center"><button type="button" onclick="aesGfxOpen()" id="btn-login-gfx" class="px-3 py-1.5 bg-slate-900/70 hover:bg-slate-900 text-amber-300 rounded-full text-[11px] font-extrabold border border-amber-400/40 transition">🖥️ Grafik: Otomatis</button></div><div class="text-left space-y-2"><label class="text-xs font-bold uppercase tracking-wider text-sky-300">Pilih Nama Siswa:</label><select id="student-name-select" onchange="toggleCustomStudentNameInput()" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white font-semibold focus:border-sky-400 focus:outline-none"></select><input id="student-custom-name" type="text" oninput="updateResumeNotice()" placeholder="Ketik nama lengkapmu di sini..." class="hidden w-full bg-slate-950 border border-sky-400 rounded-xl px-4 py-2.5 text-white text-sm font-bold mt-2 focus:outline-none" /><div id="student-resume-notice" class="hidden mt-2 text-[11px] font-bold text-emerald-200 bg-emerald-500/15 border border-emerald-400/40 rounded-xl px-3 py-2 text-left"></div></div><div class="text-left space-y-2"><label class="text-xs font-bold uppercase tracking-wider text-sky-300">Pilih Warna Robotmu:</label><div id="avatar-color-picker" class="flex items-center justify-center gap-3 pt-1"><button onclick="selectAvatarColor('#0ea5e9', this)" class="w-9 h-9 rounded-full bg-sky-500 ring-4 ring-white transition"></button><button onclick="selectAvatarColor('#f43f5e', this)" class="w-9 h-9 rounded-full bg-rose-500 opacity-75 hover:opacity-100 transition"></button><button onclick="selectAvatarColor('#10b981', this)" class="w-9 h-9 rounded-full bg-emerald-500 opacity-75 hover:opacity-100 transition"></button><button onclick="selectAvatarColor('#f59e0b', this)" class="w-9 h-9 rounded-full bg-amber-500 opacity-75 hover:opacity-100 transition"></button><button onclick="selectAvatarColor('#a855f7', this)" class="w-9 h-9 rounded-full bg-purple-500 opacity-75 hover:opacity-100 transition"></button></div></div><div class="space-y-2"><button onclick="startStudentGame()" class="w-full py-3.5 bg-gradient-to-r from-sky-400 to-blue-500 hover:from-sky-300 hover:to-blue-400 text-slate-950 font-extrabold rounded-xl shadow-lg transition">🚀 Masuk ke AES CLASS 3D</button><button id="btn-login-back-teacher" onclick="backToTeacherFromLogin()" class="w-full py-2 text-xs text-sky-200 hover:text-white transition">← Kembali ke Dashboard Guru</button></div><button type="button" onclick="toggleFullScreen()" title="Layar penuh" aria-label="Layar penuh" class="fs-start-btn hidden" style="margin:0!important">⛶</button></div></div><div id="game-hud" class="ui-layer fixed inset-0 pointer-events-none hidden"><div id="teacher-clean-toggle-wrap" class="fixed top-2 left-1/2 -translate-x-1/2 z-30 pointer-events-auto hidden"><div class="glass-light px-1.5 py-1 rounded-full flex items-center gap-1.5 shadow-lg"><button onclick="toggleTeacherCleanUI()" id="btn-clean-ui" class="px-3 py-1 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold text-[11px] leading-tight rounded-full transition whitespace-nowrap">👁️ Sembunyikan Panel</button><button onclick="exitTeacher3DMonitor()" class="px-3 py-1 bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-[11px] leading-tight rounded-full transition whitespace-nowrap">📊 Tabel Nilai & Refleksi</button></div></div><div id="hud-top-bar" class="p-3 md:p-4 flex flex-wrap items-start justify-between gap-2 transition-opacity duration-300"><div id="hud-left-card" class="glass rounded-2xl p-3.5 pointer-events-auto w-72 space-y-2 shadow-xl"><div id="hud-left-header" class="flex items-center justify-between gap-1"><div id="hud-title-block" class="truncate"><span id="hud-role-badge" class="text-[11px] font-extrabold uppercase tracking-wider px-2.5 py-0.5 bg-amber-400 text-slate-950 rounded-md">AES CLASS</span><h2 id="hud-player-name" class="font-extrabold text-white text-base truncate mt-1">Nama Siswa</h2></div><div id="hud-btn-row" class="flex items-center gap-1 shrink-0"><button onclick="toggleTeacherMic()" id="btn-hud-mic" title="Pengumuman suara ke siswa (Alt+M)" style="display:none" class="btn-teacher-mic px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-rose-300 rounded-lg text-xs font-bold border border-white/15">🎤</button><button onclick="toggleBGM()" id="btn-hud-bgm" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-emerald-300 rounded-lg text-xs font-bold border border-white/15">🎵</button><button onclick="toggleSFX()" id="btn-hud-sfx" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-sky-200 rounded-lg text-xs font-bold border border-white/15">🔊</button><button onclick="aesGfxOpen()" id="btn-hud-gfx" title="Pengaturan grafik" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-amber-300 rounded-lg text-xs font-bold border border-white/15">🖥️</button><button onclick="toggleFullScreen()" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-sky-200 rounded-lg text-xs font-bold border border-white/15">⛶</button><button id="btn-back-teacher" onclick="exitTeacher3DMonitor()" class="px-2.5 py-1.5 bg-indigo-600 hover:bg-indigo-500 text-white rounded-lg text-xs font-bold">⚙️</button></div></div><div class="text-xs text-slate-200"><div class="flex items-center justify-between mb-1"><span>Urutan Belajar (Mulai G1):</span><span id="hud-building-progress" class="font-bold text-emerald-300">0 / 5</span></div><div class="flex items-center justify-between mb-1"><span>Koin Gedung:</span><span class="font-extrabold text-amber-300">🪙 <span id="hud-coins">0</span></span></div><div id="hud-building-badges" class="flex flex-wrap gap-1 mt-1 max-h-16 overflow-y-auto custom-scroll"></div><div id="shop-lock-hint" class="hidden text-[11px] font-bold text-slate-300 mt-1.5 bg-slate-900/70 px-2.5 py-1.5 rounded-lg border border-slate-600/50">🔒 Toko, mobil & bus terbuka setelah semua gedung selesai dipelajari</div><div id="shop-hud-row" class="hidden flex flex-wrap gap-1.5 mt-1.5"><button onclick="openShopModal()" class="flex-1 px-2 py-1.5 bg-amber-400 hover:bg-amber-300 text-slate-950 rounded-lg text-xs font-extrabold shadow">🛍️ Toko</button><button id="btn-car-toggle" onclick="toggleCar()" class="hidden flex-1 px-2 py-1.5 bg-sky-400 hover:bg-sky-300 text-slate-950 rounded-lg text-xs font-extrabold shadow">🚗 Naik Mobil</button><button id="btn-bus-toggle" onclick="toggleBus()" class="hidden flex-1 px-2 py-1.5 bg-indigo-400 hover:bg-indigo-300 text-slate-950 rounded-lg text-xs font-extrabold shadow">🚌 Naik Bus</button></div><div id="hud-next-target-hint" class="text-xs font-bold text-amber-300 mt-1.5 bg-slate-900/80 px-2.5 py-1.5 rounded-lg border border-amber-400/30">🎯 Tujuan Berikutnya: Gedung G1</div></div><div id="teacher-follow-indicator" class="hidden text-xs bg-amber-500/25 border border-amber-400 text-amber-200 px-3 py-1.5 rounded-lg flex items-center justify-between"><span id="teacher-follow-name" class="truncate font-extrabold">Memantau: Siswa</span><button onclick="stopFollowingStudent()" class="text-xs font-extrabold text-white ml-2 hover:underline">Lepas ✕</button></div></div><div id="hud-center-card" class="glass rounded-2xl px-5 py-3 pointer-events-auto text-center shadow-xl border border-sky-300/40"><div id="hud-phase-label" class="text-xs font-extrabold uppercase tracking-widest text-sky-200">MENUNGGU INSTRUKSI GURU</div><div id="hud-timer" class="text-2xl md:text-3xl font-extrabold text-white font-mono">30:00</div><div id="hud-location-indicator" class="text-xs text-amber-300 font-bold">📍 Lokasi: Plaza Metropolis</div><div id="hud-teacher-quick-bar" class="mt-2 pt-2 border-t border-white/15 flex flex-wrap items-center justify-center gap-1.5"><button onclick="teacherStartLearningPhase()" class="px-2.5 py-1 bg-emerald-400 hover:bg-emerald-300 text-slate-950 font-extrabold text-xs rounded-md">▶️ Mulai Belajar</button><button onclick="teacherAdjustTime(60)" class="px-2.5 py-1 bg-slate-800 hover:bg-slate-700 text-emerald-300 font-bold text-xs rounded-md border border-emerald-400/40">+1m</button><button onclick="teacherAdjustTime(-60)" class="px-2.5 py-1 bg-slate-800 hover:bg-slate-700 text-rose-300 font-bold text-xs rounded-md border border-rose-400/40">-1m</button><button onclick="teacherCallToDockPhase()" class="px-2.5 py-1 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold text-xs rounded-md">🧭 Ke Dermaga</button><button onclick="teacherStartBoatRace()" class="px-2.5 py-1 bg-rose-500 hover:bg-rose-400 text-white font-extrabold text-xs rounded-md">🏁 Mulai Lomba</button><button onclick="teacherStartReflectionPhase()" title="Panggil siswa ke pulau untuk mengisi refleksi" class="px-2.5 py-1 bg-purple-500 hover:bg-purple-400 text-white font-extrabold text-xs rounded-md border border-purple-300">📝 Refleksi</button></div></div><div id="hud-right-card" class="glass rounded-2xl p-3 pointer-events-auto w-80 space-y-2 shadow-xl"><div class="flex items-center justify-between"><span id="hud-map-title" class="text-xs font-extrabold uppercase tracking-wider text-sky-200">🗺️ Peta & Pantauan Siswa</span><span id="hud-online-count" class="text-xs font-extrabold bg-emerald-500/30 text-emerald-200 px-2.5 py-0.5 rounded-full">0 Siswa</span></div><canvas id="minimap-canvas" width="260" height="145" class="w-full rounded-xl border border-white/20 bg-emerald-950"></canvas><div id="hud-map-pick" class="hidden max-h-44 overflow-y-auto custom-scroll rounded-xl bg-slate-900/95 border border-amber-300/60 p-2 text-xs space-y-1.5"></div><div id="hud-map-legend" class="flex items-center justify-between text-[10px] font-semibold text-slate-200 px-1"><span>🟡 G1..GN</span><span>🟢 Selesai</span><span>✓ Benar | ✗ Salah</span><span>🏝️ Pulau | 🟣 Di dalam</span></div><div id="hud-online-list" class="max-h-48 overflow-y-auto custom-scroll space-y-1.5 text-xs pt-1.5 border-t border-white/15"></div></div></div><div id="waiting-teacher-banner" class="fixed top-36 left-1/2 -translate-x-1/2 pointer-events-auto hidden"><div class="glass border-2 border-amber-300 rounded-3xl px-6 py-4 text-center shadow-2xl max-w-md space-y-2"><div class="text-2xl">⏳</div><h3 class="text-base md:text-lg font-extrabold text-amber-300">Menunggu Guru Memulai Waktu Belajar...</h3><p class="text-xs text-slate-100">Lihat Peta di kanan atas: terdapat gedung <b>G1, G2, G3...</b>. Saat Bapak/Ibu Guru menekan tombol <b>Mulai Waktu Belajar</b>, kamu baru bisa berjalan menuju gedung <b>G1</b>!</p></div></div><div id="walk-to-dock-banner" class="fixed top-36 left-1/2 -translate-x-1/2 pointer-events-auto hidden"><div class="bg-gradient-to-r from-amber-400 to-orange-500 text-slate-950 font-extrabold px-6 py-3 rounded-2xl shadow-2xl border-2 border-white text-center animate-bounce"><div class="text-xs md:text-sm">🧭 WAKTU BELAJAR SELESAI! IKUTI PANAH KUNING MENUJU DERMAGA!</div><div id="dock-distance-text" class="text-xs font-bold mt-0.5">Jarak ke Dermaga: 50 meter</div></div></div><div id="ready-on-boat-banner" class="fixed top-36 left-1/2 -translate-x-1/2 pointer-events-auto hidden"><div class="glass border-2 border-emerald-400 px-6 py-3.5 rounded-2xl text-center shadow-2xl space-y-2"><div class="text-sm md:text-base font-extrabold text-emerald-300">🚤 Kamu Sudah Naik Speedboat di Dermaga!</div><div class="text-xs text-slate-100">Pulau Victory berada jauh di seberang lautan! Menunggu teman lain tiba & Guru menekan tombol <b>Mulai Lomba ke Pulau</b>...</div></div></div><div id="island-explore-banner" class="fixed top-28 left-1/2 -translate-x-1/2 pointer-events-auto hidden"><div class="glass border-2 border-emerald-400 px-5 py-2.5 rounded-2xl text-center shadow-2xl flex items-center gap-3"><span class="text-2xl">🏝️</span><div class="text-left"><div class="text-xs md:text-sm font-extrabold text-emerald-300">Selamat Datang di Pulau Tropis Victory!</div><div class="text-[11px] text-slate-200">Jelajahi pulau: gazebo, taman bermain, layangan, api unggun, kolam & pantai (boleh main air di pinggir pantai).</div></div><button onclick="openReflectionModal()" class="px-3 py-1.5 bg-purple-500 hover:bg-purple-400 text-white font-extrabold text-xs rounded-xl shrink-0">📝 Isi Refleksi</button><button onclick="document.getElementById('winner-modal').classList.remove('hidden')" class="px-3 py-1.5 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold text-xs rounded-xl shrink-0">🏆 Lihat Nilai</button></div></div><div id="building-prompt" class="fixed bottom-32 left-1/2 -translate-x-1/2 pointer-events-auto hidden"><button onclick="openCurrentBuildingModal()" class="animate-pulse-glow px-6 py-3.5 bg-gradient-to-r from-amber-300 to-yellow-400 text-slate-950 font-extrabold rounded-2xl shadow-2xl border-2 border-white flex items-center gap-3 text-sm md:text-base"><span class="text-xl">📖</span><span id="building-prompt-text">KLIK BELAJAR MATERI GEDUNG</span></button></div><div id="bus-board-wrap" class="fixed bottom-48 left-1/2 -translate-x-1/2 pointer-events-auto hidden z-20 text-center"><button id="btn-bus-board" onclick="onBusBoardClick()" class="animate-pulse-glow px-6 py-3 bg-gradient-to-r from-indigo-300 to-sky-400 text-slate-950 font-extrabold rounded-2xl shadow-2xl border-2 border-white text-sm md:text-base">🚌 Naik Bus (Gratis!)</button><div id="bus-driver-hint" class="hidden glass-light px-4 py-2 rounded-2xl text-xs font-bold text-sky-100 max-w-xs"></div></div><div id="joystick-zone" class="fixed bottom-6 left-6 pointer-events-auto flex flex-col items-center gap-1.5"><div id="joystick-base" class="w-28 h-28 md:w-32 md:h-32 rounded-full bg-slate-900/70 border-2 border-white/60 shadow-[0_0_25px_rgba(56,189,248,0.4)] relative flex items-center justify-center backdrop-blur-md"><div class="w-16 h-16 rounded-full border border-white/25 pointer-events-none"></div><div id="joystick-knob" class="w-12 h-12 rounded-full bg-gradient-to-br from-sky-300 to-blue-600 shadow-[0_0_18px_rgba(56,189,248,1)] border-2 border-white absolute pointer-events-none transition-transform duration-75"></div></div><span class="text-[10px] font-bold text-white bg-slate-900/80 px-2.5 py-0.5 rounded-full border border-white/20">Geser Bulatan / Panah Keyboard</span></div><div id="camera-control-box" class="pointer-events-auto"><button id="cam-toggle" onclick="document.getElementById('camera-control-box').classList.toggle('open')" title="Zoom kamera" class="glass border border-white/30 shadow-2xl text-white">🔍</button><div id="cam-panel" class="glass border border-white/30 shadow-2xl"><div class="flex items-center justify-between"><span class="cam-title font-extrabold text-sky-200 uppercase tracking-wider">Zoom</span><span id="cam-dist-label" class="font-bold text-amber-300" style="font-size:9px">Dekat</span></div><input id="camera-dist-slider" type="range" min="3.5" max="45" step="0.4" value="6.5" oninput="setCameraDistanceFromSlider(this.value)" class="w-full accent-sky-400 cursor-pointer h-1 bg-slate-700 rounded-lg" /><div class="cam-btns grid grid-cols-3 gap-1 font-bold"><button onclick="setQuickCameraView(4.0, 0.18)" title="Dekat" class="bg-sky-500/30 hover:bg-sky-500/50 text-white rounded-md border border-sky-300/40">👁️</button><button onclick="setQuickCameraView(8.0, 0.28)" title="Sedang" class="bg-slate-800/80 hover:bg-slate-700 text-slate-200 rounded-md border border-white/15">🚶</button><button onclick="setQuickCameraView(24, 0.52)" title="Jauh" class="bg-slate-800/80 hover:bg-slate-700 text-slate-200 rounded-md border border-white/15">🏙️</button></div></div></div><div id="race-quiz-panel" class="fixed bottom-1.5 inset-x-0 px-2 md:px-4 pointer-events-auto hidden z-20"><div class="max-w-3xl mx-auto glass-light rounded-2xl p-2.5 md:p-3 border border-sky-300/50 shadow-xl relative"><div id="wrong-penalty-overlay" class="absolute inset-0 bg-rose-950/90 backdrop-blur-sm z-30 rounded-2xl flex flex-col items-center justify-center text-center p-2 hidden"><h3 class="text-xs md:text-sm font-extrabold text-rose-200">⚠️ Jawaban Kurang Tepat! Soal Akan Diulang Nanti</h3><p class="text-[11px] text-rose-300 mt-0.5">Tunggu jeda <span id="penalty-countdown" class="font-extrabold text-white underline">2.0</span> detik...</p></div><div class="flex flex-wrap items-center justify-between gap-2 mb-1.5 border-b border-white/15 pb-1"><div class="flex items-center gap-2"><span id="quiz-mode-badge" class="px-2 py-0.5 bg-amber-400 text-slate-950 font-extrabold text-[9px] rounded-md">🚤 PUTARAN UTAMA</span><span id="quiz-question-counter" class="text-[10px] font-bold text-sky-200">Soal #1</span></div><div class="flex items-center gap-2.5 text-[10px] font-bold"><span class="text-emerald-300">Progres: <b id="quiz-my-strokes" class="text-white">0</b>/<b id="quiz-target-strokes">10</b></span><span class="text-sky-200">| Skor Putaran 1: <b id="quiz-live-correct" class="text-emerald-400">✓0</b><b id="quiz-live-wrong" class="text-rose-400">✗0</b></span><button onclick="toggleMinimizeQuizBody()" class="px-2 py-0.5 bg-slate-800/80 hover:bg-slate-700 text-sky-200 rounded text-[9px] border border-white/20" id="btn-min-quiz">🔽 Kecilkan</button></div></div><div id="quiz-body-content" class="max-h-[24vh] overflow-y-auto custom-scroll pr-1 space-y-1.5"><div id="quiz-question-image-box" class="hidden"><img id="quiz-question-image" src="" alt="Gambar Soal" class="max-h-24 rounded-xl border border-white/20 mx-auto object-contain bg-slate-950/60 p-1" /></div><div id="quiz-question-text" class="text-xs font-bold text-white leading-snug wrap-anywhere">Memuat soal lomba...</div><div id="quiz-options-grid" class="grid grid-cols-1 sm:grid-cols-2 gap-1.5"></div></div></div></div></div><div id="building-material-modal" class="ui-layer fixed inset-0 bg-slate-950/80 backdrop-blur-md flex items-center justify-center p-3 md:p-6 hidden"><div class="max-w-4xl w-full bg-slate-900 border-2 border-sky-400 rounded-3xl p-5 md:p-8 shadow-2xl space-y-4 h-[90vh] flex flex-col"><div class="flex flex-wrap items-start justify-between gap-4 border-b border-slate-800 pb-3 shrink-0"><div><span id="modal-building-type" class="px-3 py-1 bg-amber-400 text-slate-950 text-xs font-extrabold rounded-full">GEDUNG G1</span><h2 id="modal-building-title" class="text-lg md:text-2xl font-extrabold text-white mt-1.5">Judul Materi Gedung</h2></div><div class="flex items-center gap-2"><button onclick="adjustMaterialFontSize(-2)" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-slate-200 rounded-lg text-xs font-bold border border-slate-700">A-</button><button onclick="adjustMaterialFontSize(2)" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 text-slate-200 rounded-lg text-xs font-bold border border-slate-700">A+</button><button onclick="closeBuildingModal()" class="p-2 bg-rose-500/20 hover:bg-rose-500/40 text-rose-300 rounded-xl text-sm font-bold">✕ Tutup</button></div></div><div id="modal-building-scroll-area" class="flex-1 overflow-y-auto custom-scroll bg-slate-950/70 border border-slate-800/90 rounded-2xl p-4 md:p-6 space-y-4 select-text"><div id="modal-building-image-box" class="hidden"><img id="modal-building-image" src="" alt="Ilustrasi Materi" class="max-h-72 rounded-2xl border border-sky-400/30 mx-auto object-contain bg-slate-900 p-2 shadow-lg" /></div><div id="modal-building-content" style="font-size: 15px;" class="text-slate-100 leading-relaxed whitespace-pre-line wrap-anywhere"></div><div id="building-quiz-box" class="hidden bg-amber-400/10 border-2 border-amber-400/60 rounded-2xl p-4 space-y-3 whitespace-normal"><div class="flex items-center justify-between gap-2"><span class="px-2.5 py-0.5 bg-amber-400 text-slate-950 text-[11px] font-extrabold rounded-full">🪙 SOAL KOIN</span><span class="text-[11px] text-amber-200 font-bold">Hanya 1x kesempatan • benar = 1 koin</span></div><div id="building-quiz-question" class="text-sm font-bold text-white wrap-anywhere"></div><div id="building-quiz-options" class="grid grid-cols-1 gap-2"></div><div id="building-quiz-feedback" class="text-sm font-extrabold min-h-[1.25rem]"></div></div></div><div class="bg-slate-950 p-3.5 rounded-2xl border border-sky-500/40 space-y-1.5 shrink-0"><div class="flex items-center justify-between"><label class="text-xs font-bold text-sky-400 uppercase">📝 Catatan Belajar Wajib di Gedung Ini (Dipantau Guru Real-Time):</label><span id="student-note-char-status" class="text-[11px] font-extrabold text-amber-400">Minimal 15 karakter</span></div> <textarea id="student-personal-note" rows="2" class="w-full bg-slate-900/90 border border-slate-700 rounded-xl p-2.5 text-xs md:text-sm text-slate-100 focus:border-sky-400 focus:outline-none custom-scroll" placeholder="Tuliskan rangkuman atau poin penting yang kamu pelajari dari gedung ini (minimal 15 karakter agar gedung berstatus selesai)..."></textarea> </div><div class="flex justify-end gap-3 shrink-0"><button id="btn-finish-building" onclick="markBuildingCompletedAndClose()" class="w-full md:w-auto px-6 py-3 bg-gradient-to-r from-emerald-400 to-sky-400 hover:from-emerald-300 hover:to-sky-300 text-slate-950 font-extrabold rounded-xl text-sm shadow-lg transition">✅ Simpan Catatan & Selesai Mempelajari Gedung Ini</button></div></div></div><div id="teacher-notes-modal" class="ui-layer fixed inset-0 bg-slate-950/85 backdrop-blur-md flex items-center justify-center p-4 hidden z-50"><div class="max-w-3xl w-full bg-slate-900 border-2 border-sky-400 rounded-3xl p-6 space-y-4 shadow-2xl max-h-[88vh] flex flex-col"><div class="flex items-center justify-between border-b border-slate-800 pb-3 shrink-0"><div><span class="px-2.5 py-0.5 bg-sky-400 text-slate-950 font-extrabold text-[11px] rounded-full">PANTAUAN REAL-TIME GURU</span><h3 id="teacher-notes-modal-title" class="text-lg md:text-xl font-extrabold text-white mt-1">📖 Catatan Belajar Siswa di Tiap Gedung</h3></div><button onclick="closeTeacherNotesModal()" class="px-3 py-1.5 bg-rose-500/20 hover:bg-rose-500/40 text-rose-300 rounded-xl text-xs font-bold">✕ Tutup</button></div><div id="teacher-notes-modal-body" class="flex-1 overflow-y-auto custom-scroll space-y-3 pr-1"></div><div class="flex justify-between items-center pt-2 border-t border-slate-800 shrink-0"><span class="text-xs text-slate-400">Catatan diperbarui otomatis saat siswa mengetik di dalam gedung.</span><button onclick="exportStudentNotesDOCX()" class="px-4 py-2 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold rounded-xl text-xs shadow">📄 Unduh Semua Catatan (.docx)</button></div></div></div><div id="shop-modal" class="ui-layer fixed inset-0 bg-slate-950/85 backdrop-blur-md flex items-center justify-center p-4 hidden z-50"><div class="max-w-2xl w-full bg-slate-900 border-2 border-amber-400 rounded-3xl p-5 md:p-6 space-y-4 shadow-2xl max-h-[90vh] flex flex-col"><div class="flex items-center justify-between border-b border-slate-800 pb-3 shrink-0"><div><span class="px-2.5 py-0.5 bg-amber-400 text-slate-950 font-extrabold text-[11px] rounded-full">🛍️ TOKO KOTA</span><h3 class="text-lg md:text-xl font-extrabold text-white mt-1">Tukar Koinmu! <span class="text-amber-300">(harga tertera di tiap barang)</span></h3></div><div class="flex items-center gap-2"><span class="px-3 py-1.5 bg-slate-800 border border-amber-400/50 rounded-xl text-sm font-extrabold text-amber-300">🪙 <span id="shop-coin-balance">0</span></span><button onclick="closeShopModal()" class="px-3 py-1.5 bg-rose-500/20 hover:bg-rose-500/40 text-rose-300 rounded-xl text-xs font-bold">✕ Tutup</button></div></div><div id="shop-items-grid" class="flex-1 overflow-y-auto custom-scroll grid grid-cols-1 sm:grid-cols-2 gap-3 pr-1"></div><p class="text-[11px] text-slate-400 shrink-0">Mobil &amp; bus hanya bisa dipakai di kota. Teman sekelas boleh naik busmu gratis tanpa koin. Aksesoris terlihat oleh teman sekelas.</p></div></div><div id="reflection-modal" class="ui-layer fixed inset-0 bg-slate-950/85 backdrop-blur-md flex items-center justify-center p-4 hidden z-40"><div class="max-w-lg w-full glass border-2 border-purple-400 rounded-3xl p-6 md:p-7 space-y-4 shadow-2xl"><div class="flex items-center justify-between border-b border-slate-800 pb-3"><div><span class="px-3 py-1 bg-purple-500/30 text-purple-200 text-[11px] font-extrabold uppercase rounded-full border border-purple-400/40">🏝️ Refleksi di Pulau Victory</span><h2 class="text-xl font-extrabold text-white mt-1.5">📝 Lembar Refleksi Pembelajaran</h2></div><button id="reflection-sim-close" onclick="document.getElementById('reflection-modal').classList.add('hidden')" class="hidden px-3 py-1.5 bg-slate-700 hover:bg-slate-600 text-white font-bold text-xs rounded-lg shrink-0">✖ Tutup (simulasi guru)</button></div><p class="text-xs text-slate-300">Silakan isi refleksi pengalaman belajarmu hari ini dengan jujur. Hasil refleksi ini akan langsung terkirim ke Dashboard Guru.</p><div class="space-y-3 text-left text-xs"><div><label class="block font-bold text-sky-300 mb-1">1. Bagaimana perasaanmu mengikuti pembelajaran 3D hari ini? *</label><select id="ref-feeling" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-3.5 py-2.5 text-white font-semibold focus:border-purple-400 focus:outline-none"><option value="🤩 Sangat Senang & Bersemangat">🤩 Sangat Senang & Bersemangat</option><option value="😊 Senang & Mudah Paham">😊 Senang & Mudah Paham</option><option value="😐 Biasa Saja">😐 Biasa Saja</option><option value="😥 Agak Bingung / Butuh Bantuan">😥 Agak Bingung / Butuh Bantuan</option></select></div><div><label class="block font-bold text-emerald-300 mb-1">2. Hal penting / materi apa yang paling kamu pahami hari ini? *</label> <textarea id="ref-understood" rows="2" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-3 text-slate-100 focus:border-purple-400 focus:outline-none custom-scroll" placeholder="Tuliskan materi yang sudah kamu kuasai..."></textarea> </div><div><label class="block font-bold text-amber-300 mb-1">3. Bagian mana yang menurutmu masih sulit atau belum dipahami? *</label> <textarea id="ref-difficulty" rows="2" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-3 text-slate-100 focus:border-purple-400 focus:outline-none custom-scroll" placeholder="Tuliskan kesulitanmu (atau ketik 'Tidak ada' jika sudah paham semua)..."></textarea> </div><div><label class="block font-bold text-purple-300 mb-1">4. Pesan atau harapanmu untuk pembelajaran berikutnya:</label> <textarea id="ref-suggestion" rows="2" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-3 text-slate-100 focus:border-purple-400 focus:outline-none custom-scroll" placeholder="Tuliskan kesan atau saranmu..."></textarea> </div></div><button onclick="submitStudentReflection()" class="w-full py-3.5 bg-gradient-to-r from-purple-500 to-indigo-500 hover:from-purple-400 hover:to-indigo-400 text-white font-extrabold rounded-xl text-sm shadow-lg transition"> 🚀 Kirim Refleksi ke Guru & Jalan-Jalan di Pulau </button></div></div><div id="winner-modal" class="ui-layer fixed inset-0 bg-slate-950/80 backdrop-blur-md flex items-center justify-center p-4 hidden"><div class="max-w-lg w-full glass border-2 border-emerald-400 rounded-3xl p-6 md:p-8 text-center space-y-4 shadow-2xl"><div class="text-5xl">🏝️🏆</div><div><span class="px-3 py-1 bg-emerald-500/20 text-emerald-300 text-xs font-bold uppercase rounded-full">Mendarat di Pulau Victory!</span><h2 class="text-2xl font-extrabold text-white mt-2">Selamat! Kamu Sampai di Pulau Impian!</h2></div><div id="my-finish-summary" class="bg-slate-900/90 border border-sky-400/40 rounded-2xl p-4 text-left space-y-2 text-xs"></div><div class="text-left"><div class="text-xs font-extrabold uppercase text-amber-300 mb-2">📊 Peringkat Kelas Saat Ini:</div><div id="leaderboard-list" class="space-y-1.5 max-h-44 overflow-y-auto custom-scroll"></div></div><div class="flex flex-col sm:flex-row gap-2"><button onclick="document.getElementById('winner-modal').classList.add('hidden'); openReflectionModal();" class="flex-1 py-3 bg-purple-500 hover:bg-purple-400 text-white font-extrabold rounded-xl text-xs shadow-lg">📝 Isi Refleksi Dulu</button><button onclick="document.getElementById('winner-modal').classList.add('hidden')" class="flex-1 py-3 bg-gradient-to-r from-emerald-400 to-sky-400 text-slate-950 font-extrabold rounded-xl text-xs shadow-lg">🏝️ Jalan-Jalan di Pantai</button></div></div></div> <script>(function(){window.__aesBuild="AESC1-2026-10C8CD16";try{console.info("%c© 2026 AES CLASS. Seluruh hak cipta dilindungi. Dilarang menyalin, memodifikasi, merapikan ulang, atau mendistribusikan kode ini tanpa izin tertulis, termasuk dengan bantuan alat AI. [AESC1-2026-10C8CD16]","color:#0284c7;font-weight:bold")}catch{}})();let audioCtx=null,isBgmEnabled=!0,isSfxEnabled=!0,bgmInterval=null,bgmStep=0,lastFootstepTime=0;function initAudioEngine(){try{if(!audioCtx){const e=window.AudioContext||window.webkitAudioContext;e&&(audioCtx=new e)}audioCtx&&audioCtx.state==="suspended"&&audioCtx.resume(),isBgmEnabled&&!bgmInterval&&startBackgroundMusicLoop()}catch{}}function unlockAudioOnFirstInteraction(){initAudioEngine()}function toggleBGM(){initAudioEngine(),isBgmEnabled=!isBgmEnabled,updateAudioButtonsUI(),isBgmEnabled?startBackgroundMusicLoop():bgmInterval&&(clearInterval(bgmInterval),bgmInterval=null)}function toggleSFX(){initAudioEngine(),isSfxEnabled=!isSfxEnabled,updateAudioButtonsUI(),isSfxEnabled&&playSoundEffect("click")}function updateAudioButtonsUI(){const e=document.getElementById("btn-teacher-bgm"),t=document.getElementById("btn-teacher-sfx"),n=document.getElementById("btn-hud-bgm"),o=document.getElementById("btn-hud-sfx");e&&(e.textContent=isBgmEnabled?"🎵 Musik: ON":"🔇 Musik: OFF"),t&&(t.textContent=isSfxEnabled?"🔊 SFX: ON":"🔇 SFX: OFF"),n&&(n.textContent=isBgmEnabled?"🎵":"🔇"),o&&(o.textContent=isSfxEnabled?"🔊":"🔈")}function playTone(e,t,n,o=.08,a=0){if(audioCtx)try{const r=audioCtx.createOscillator(),s=audioCtx.createGain();r.type=t,r.frequency.setValueAtTime(e,audioCtx.currentTime+a),s.gain.setValueAtTime(.001,audioCtx.currentTime+a),s.gain.linearRampToValueAtTime(o,audioCtx.currentTime+a+.02),s.gain.exponentialRampToValueAtTime(1e-4,audioCtx.currentTime+a+n),r.connect(s),s.connect(audioCtx.destination),r.start(audioCtx.currentTime+a),r.stop(audioCtx.currentTime+a+n+.02)}catch{}}function startBackgroundMusicLoop(){bgmInterval&&clearInterval(bgmInterval);const e=[261.63,329.63,392,523.25,392,329.63,293.66,392],t=[329.63,392,440,523.25,440,523.25,587.33,659.25];bgmInterval=setInterval(()=>{!isBgmEnabled||!audioCtx||audioCtx.state!=="running"||(bgmStep=(bgmStep+1)%8,gamePhase==="race"&&!myPlayer.finishedRace?playTone(t[bgmStep],"triangle",.22,.035):bgmStep%2===0&&playTone(e[bgmStep],"sine",.38,.03))},320)}function playSoundEffect(e){if(isSfxEnabled&&(initAudioEngine(),!!audioCtx))if(e==="step"){const t=Date.now();if(t-lastFootstepTime<260)return;lastFootstepTime=t,playTone(130+Math.random()*25,"triangle",.06,.035)}else e==="click"||e==="open_building"?(playTone(523.25,"sine",.12,.08,0),playTone(659.25,"sine",.16,.08,.07)):e==="complete_building"||e==="finish_island"?(playTone(523.25,"triangle",.14,.09,0),playTone(659.25,"triangle",.14,.09,.1),playTone(783.99,"triangle",.14,.09,.2),playTone(1046.5,"triangle",.35,.11,.3)):e==="correct_row"?(playTone(587.33,"sine",.12,.1,0),playTone(880,"sine",.24,.1,.09)):e==="wrong_answer"?(playTone(190,"sawtooth",.22,.08,0),playTone(145,"sawtooth",.35,.08,.16)):e==="whistle_dock"&&(playTone(783.99,"square",.18,.06,0),playTone(783.99,"square",.35,.06,.22))}function aesEscTA(e){return String(e==null?"":e).replace(/&/g,"&amp;").replace(/</g,"&lt;")}function formatRichEducationalText(e,rich){if(!e)return"";let t=String(e).replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;");const keep=[],K=h=>"\u0001"+(keep.push(h)-1)+"\u0002",Qt=u=>String(u).trim().replace(/"/g,"%22").replace(/'/g,"%27").replace(/</g,"%3C").replace(/>/g,"%3E"),un=u=>String(u).replace(/&amp;/g,"&"),isH=u=>/^https?:\/\//i.test(u),img=(u,alt)=>`<div class="my-3"><img src="${Qt(u)}" alt="${String(alt||"gambar").replace(/"/g,"&quot;")}" loading="lazy" referrerpolicy="no-referrer" class="max-h-60 rounded-xl border border-sky-400/30 mx-auto object-contain bg-slate-900 p-1.5 shadow-md" /></div>`,lnk=(u,x)=>isH(u)?`<a href="${Qt(u)}" target="_blank" rel="noopener noreferrer" class="aes-link">${x||u}</a>`:(x||u),vid=u0=>{const u=un(u0);let m;if(m=u.match(/(?:youtu\.be\/|youtube(?:-nocookie)?\.com\/(?:watch\?(?:[^#]*&)?v=|embed\/|shorts\/|live\/|v\/))([\w-]{11})/i)){const st=(u.match(/[?&](?:t|start)=(\d+)/)||[])[1];return`<div class="aes-video"><iframe src="https://www.youtube-nocookie.com/embed/${m[1]}${st?"?start="+st:""}" title="Video" loading="lazy" allowfullscreen allow="accelerometer; encrypted-media; picture-in-picture; fullscreen" referrerpolicy="strict-origin-when-cross-origin"></iframe></div>`+lnk(u0,"▶ Buka video di tab baru")}if(m=u.match(/vimeo\.com\/(?:video\/)?(\d+)/i))return`<div class="aes-video"><iframe src="https://player.vimeo.com/video/${m[1]}" title="Video" loading="lazy" allowfullscreen allow="fullscreen; picture-in-picture"></iframe></div>`+lnk(u0,"▶ Buka video di tab baru");if(m=u.match(/drive\.google\.com\/file\/d\/([\w-]+)/i))return`<div class="aes-video"><iframe src="https://drive.google.com/file/d/${m[1]}/preview" title="Video" loading="lazy" allowfullscreen></iframe></div>`+lnk(u0,"▶ Buka video di tab baru");return/\.(mp4|webm|ogg|mov|m4v)(\?|#|$)/i.test(u)&&isH(u)?`<video class="aes-vid" controls playsinline preload="metadata" src="${Qt(u0)}"></video>`:lnk(u0,"▶ Buka video")};t=t.replace(/\[img:(https?:\/\/[^\]]+|data:image\/[^\]]+)\]/gi,(n,o)=>K(img(o))),t=t.replace(/!\[([^\]]*)\]\((https?:\/\/[^\s)]+)\)/g,(n,o,a)=>K(img(a,o)));if(rich){t=t.replace(/\[(?:video|vid):\s*(https?:\/\/[^\]\s]+)\s*\]/gi,(n,o)=>K(vid(o))),t=t.replace(/\[link:\s*(https?:\/\/[^\]|\s]+)\s*(?:\|([^\]]*))?\]/gi,(n,o,a)=>K(lnk(o,(a||"").trim()||o))),t=t.replace(/\[([^\]\n]+)\]\((https?:\/\/[^\s)]+)\)/g,(n,o,a)=>K(lnk(a,o))),t=t.replace(/(^|[\s(>])(https?:\/\/[^\s<>"')\]\u0001]+)/g,(n,o,a)=>{let u=a,tr="";const tm=u.match(/[.,;:!?]+$/);tm&&(tr=tm[0],u=u.slice(0,-tr.length));if(!isH(u))return n;const uu=un(u);let h;return/\.(png|jpe?g|gif|webp|svg|avif|bmp)(\?|#|$)/i.test(uu)?h=img(u):/(youtu\.be\/|youtube(?:-nocookie)?\.com\/(watch|embed|shorts|live)|vimeo\.com\/\d|drive\.google\.com\/file\/d\/|\.(mp4|webm|mov|m4v)(\?|#|$))/i.test(uu)?h=vid(u):h=lnk(u,u.length>52?u.slice(0,50)+"…":u),o+K(h)+tr})}return t=t.replace(/\u0001(\d+)\u0002/g,(n,o)=>keep[+o]||""),t}function triggerMathJaxRender(e){window.MathJax&&typeof window.MathJax.typesetPromise=="function"&&window.MathJax.typesetPromise(e).catch(()=>{})}function toggleFullScreen(){try{playSoundEffect("click")}catch{}const e=document.documentElement,t=!!(document.fullscreenElement||document.webkitFullscreenElement);try{if(t){const n=document.exitFullscreen||document.webkitExitFullscreen;if(n){const o=n.call(document);o&&o.catch&&o.catch(()=>{})}}else{const n=e.requestFullscreen||e.webkitRequestFullscreen;if(n){const o=n.call(e);o&&o.catch&&o.catch(()=>{})}}}catch{}}function syncFullScreenButtons(){const e=!!(document.documentElement.requestFullscreen||document.documentElement.webkitRequestFullscreen),t=!!(document.fullscreenElement||document.webkitFullscreenElement);document.querySelectorAll(".fs-start-btn").forEach(n=>{n.classList.toggle("hidden",!e),n.textContent=t?"✕":"⛶",n.title=t?"Keluar layar penuh":"Layar penuh"})}document.addEventListener("fullscreenchange",syncFullScreenButtons),document.addEventListener("webkitfullscreenchange",syncFullScreenButtons),window.addEventListener("DOMContentLoaded",syncFullScreenButtons);let currentMaterialFontSize=15;function adjustMaterialFontSize(e){playSoundEffect("click"),currentMaterialFontSize=Math.max(12,Math.min(26,currentMaterialFontSize+e));const t=document.getElementById("modal-building-content");t&&(t.style.fontSize=currentMaterialFontSize+"px")}const BUILDING_ARCHETYPES=[{code:"G1",type:"Perpustakaan Pusat",style:"library",color:"#0284c7",icon:"📚"},{code:"G2",type:"Grand Cafe & Resto",style:"cafe",color:"#ea580c",icon:"☕"},{code:"G3",type:"Rumah Sakit Medika",style:"hospital",color:"#e11d48",icon:"🏥"},{code:"G4",type:"Mega Mall & Plaza",style:"mall",color:"#9333ea",icon:"🛍️"},{code:"G5",type:"Menara Kantor Tech",style:"office",color:"#059669",icon:"🏢"},{code:"G6",type:"Bioskop Cinema XXI",style:"cinema",color:"#db2777",icon:"🎬"},{code:"G7",type:"Supermarket FreshMart",style:"supermarket",color:"#ca8a04",icon:"🛒"},{code:"G8",type:"Museum Sains & Robotika",style:"museum",color:"#4f46e5",icon:"🔬"},{code:"G9",type:"Stasiun TV & Media",style:"tvstation",color:"#0d9488",icon:"📡"},{code:"G10",type:"Stadion Olahraga Kota",style:"stadium",color:"#16a34a",icon:"🏟️"},{code:"G11",type:"Balai Kota Metropolis",style:"cityhall",color:"#2563eb",icon:"🏛️"},{code:"G12",type:"Hotel Grand Surya",style:"hotel",color:"#d97706",icon:"🏨"},{code:"G13",type:"Bank Sentral Finansial",style:"bank",color:"#0891b2",icon:"🏦"},{code:"G14",type:"Kampus Universitas Raya",style:"university",color:"#7c3aed",icon:"🎓"},{code:"G15",type:"Gedung Opera & Konser",style:"opera",color:"#e11d48",icon:"🎭"},{code:"G16",type:"Pusat Riset Antariksa",style:"spacelab",color:"#0284c7",icon:"🚀"},{code:"G17",type:"Markas Pemadam Kebakaran",style:"firestation",color:"#dc2626",icon:"🚒"},{code:"G18",type:"Markas Kepolisian Kota",style:"police",color:"#1d4ed8",icon:"🚓"},{code:"G19",type:"Terminal Skyport Helipad",style:"skyport",color:"#059669",icon:"🚁"},{code:"G20",type:"Menara Kembar Petronas",style:"twintower",color:"#0ea5e9",icon:"🏙️"}];function getBuildingSlotCoordinate(e){const t=[{x:-42,z:6},{x:42,z:6},{x:-42,z:-54},{x:42,z:-54},{x:-42,z:-114},{x:42,z:-114},{x:-126,z:6},{x:126,z:6},{x:-126,z:-54},{x:126,z:-54},{x:-126,z:-114},{x:126,z:-114},{x:-42,z:-174},{x:42,z:-174},{x:-126,z:-174},{x:126,z:-174},{x:-42,z:-234},{x:42,z:-234},{x:-126,z:-234},{x:126,z:-234}];if(e<t.length)return t[e];const n=Math.floor((e-t.length)/4),o=(e-t.length)%4;return{x:[-126,-42,42,126][o],z:-294-n*60}}const DEFAULT_GAME_DATA={subjectName:"Informatika - Berpikir Komputasional",gradeLevel:"SMP / SMA",timerMinutes:30,students:["Ahmad Fauzi","Budi Santoso","Citra Lestari","Dewi Anggraini","Eko Prasetyo"],buildings:[{id:"b1",quiz:{q:"Berikut ini yang BUKAN termasuk 4 pilar berpikir komputasional adalah...",options:["Dekomposisi","Pengenalan Pola","Hafalan","Algoritma"],correct:2},type:"Perpustakaan Pusat",style:"library",name:"Perpustakaan Pusat (Pengantar)",color:"#0284c7",image:"",content:`Selamat datang di Gedung G1: Perpustakaan Pusat!\n\nBerpikir Komputasional adalah metode menyelesaikan masalah secara sistematis, logis, dan terstruktur.\n\n4 Pilar Utama:\n1. Dekomposisi (G2)\n2. Pengenalan Pola (G3)\n3. Abstraksi (G4)\n4. Algoritma (G5)`},{id:"b2",quiz:{q:"Memecah masalah besar menjadi bagian-bagian yang lebih kecil disebut...",options:["Abstraksi","Dekomposisi","Algoritma","Pengenalan Pola"],correct:1},type:"Grand Cafe & Resto",style:"cafe",name:"Grand Cafe & Resto (Dekomposisi)",color:"#ea580c",image:"",content:`Selamat datang di Gedung G2: Grand Cafe!\n\nDekomposisi adalah kemampuan memecah masalah besar menjadi bagian-bagian yang lebih kecil dan mudah dikelola.`},{id:"b3",quiz:{q:"Mencari kesamaan atau keteraturan di antara berbagai masalah disebut...",options:["Pengenalan Pola","Dekomposisi","Abstraksi","Algoritma"],correct:0},type:"Rumah Sakit Medika",style:"hospital",name:"RS Medika Utama (Pengenalan Pola)",color:"#e11d48",image:"",content:`Selamat datang di Gedung G3: Rumah Sakit Medika!\n\nPengenalan Pola adalah mencari kesamaan atau keteraturan di antara berbagai masalah.`},{id:"b4",quiz:{q:"Fokus pada hal penting dan mengabaikan detail yang tidak relevan disebut...",options:["Algoritma","Pengenalan Pola","Dekomposisi","Abstraksi"],correct:3},type:"Mega Mall & Plaza",style:"mall",name:"Mega Mall & Plaza (Abstraksi)",color:"#9333ea",image:"",content:`Selamat datang di Gedung G4: Mega Mall!\n\nAbstraksi adalah menyaring informasi dengan fokus hanya pada hal penting dan mengabaikan detail yang tidak relevan.`},{id:"b5",quiz:{q:"Menyusun langkah-langkah penyelesaian masalah secara berurutan dan logis disebut...",options:["Dekomposisi","Abstraksi","Pengenalan Pola","Algoritma"],correct:3},type:"Menara Kantor Tech",style:"office",name:"Menara Kantor Tech (Algoritma)",color:"#059669",image:"",content:`Selamat datang di Gedung G5: Menara Kantor Tech!\n\nBerpikir Algoritmik adalah menyusun langkah-langkah penyelesaian masalah secara berurutan dan logis.`}],questions:[{q:"Kemampuan memecah masalah besar menjadi bagian-bagian yang lebih kecil disebut...",image:"",options:["Dekomposisi","Abstraksi","Pengenalan Pola","Algoritma"],correct:0},{q:"Dokter mendiagnosis penyakit pasien dengan melihat kemiripan gejala pasien sebelumnya. Ini adalah...",image:"",options:["Dekomposisi","Pengenalan Pola","Abstraksi","Pemrograman"],correct:1},{q:"Fokus pada informasi penting dan mengabaikan detail yang tidak relevan disebut...",image:"",options:["Algoritma","Dekomposisi","Abstraksi","Kompilasi"],correct:2},{q:"Urutan langkah-langkah logis untuk menyelesaikan tugas dari awal sampai akhir disebut...",image:"",options:["Abstraksi","Dekomposisi","Pengenalan Pola","Algoritma"],correct:3},{q:"Perhatikan barisan: $3, 6, 12, 24, 48, \\dots$ Suku berikutnya adalah...",image:"",options:["$72$","$84$","$96$","$108$"],correct:2}]};let gameConfig=JSON.parse(JSON.stringify(DEFAULT_GAME_DATA)),roomId="aesclass-default",isTeacherMode=!0,isTeacher3DMonitor=!1,isTeacherCleanUI=!1,teacherFollowPlayerId=null;const SHOP_ITEMS=[{id:"car",icon:"🚗",name:"Mobil Keliling Kota",desc:"Naik mobil dan keliling kota lebih cepat!",slot:"car",price:1},{id:"bus",icon:"🚌",name:"Bus Wisata Kota",desc:"Bus terbuka untuk 6 penumpang. Ajak teman naik GRATIS, mereka tidak perlu koin!",slot:"car",price:3},{id:"hat_cap",icon:"🧢",name:"Topi Baseball",desc:"Topi santai untuk robotmu.",slot:"head"},{id:"hat_magic",icon:"🎩",name:"Topi Pesulap",desc:"Siapa tahu ada kelinci di dalamnya.",slot:"head"},{id:"crown",icon:"👑",name:"Mahkota Emas",desc:"Untuk sang juara kota!",slot:"head"},{id:"glasses",icon:"🕶️",name:"Kacamata Keren",desc:"Gaya paling kece di kota.",slot:"face"},{id:"bowtie",icon:"🎀",name:"Dasi Kupu-kupu",desc:"Tampil rapi dan elegan.",slot:"neck"},{id:"cape",icon:"🦸",name:"Jubah Pahlawan",desc:"Berkibar di punggungmu.",slot:"back"},{id:"backpack",icon:"🎒",name:"Ransel Petualang",desc:"Ransel oranye untuk bekal belajarmu.",slot:"pack"},{id:"watch",icon:"⌚",name:"Jam Tangan Digital",desc:"Layar biru menyala di pergelangan tangan.",slot:"wrist"},{id:"jacket",icon:"🧥",name:"Jaket Keren",desc:"Jaket biru dengan garis putih.",slot:"body"}];function shopItemById(e){return SHOP_ITEMS.find(t=>t.id===e)}function shopPrice(e){return e&&e.price?e.price:1}let gamePhase="waiting",remainingSeconds=1800,timerInterval=null,mqttBroadcastLoop=null,racePassiveDrift=0,raceInited=!1,myPlayer={id:"p_"+Math.random().toString(36).substring(2,9),name:"",role:"spectator",hasJoinedGame:!1,color:"#0ea5e9",x:0,z:50,rotY:Math.PI,currentBuilding:"Plaza Metropolis",completedBuildings:[],atDock:!1,boatStrokes:0,initialCorrect:0,initialWrong:0,retryCorrect:0,retryWrong:0,finishedRace:!1,finalScore:0,lastRowTime:0,phase:"waiting",reflectionSubmitted:!1,reflectionFeeling:"",reflectionUnderstood:"",reflectionDifficulty:"",reflectionSuggestion:"",buildingNotes:{},coins:0,coinBuildings:[],buildingQuizResult:{},buildingQuizPick:{},ownedItems:[],equip:{},inCar:!1,rideDriverId:null,insideBuilding:null},questionQueue=[],firstAttemptTracker={},otherPlayers={},mqttClient=null,isPenaltyLocked=!1,activeNearBuilding=null,studentNotes={};const DOCK_TARGET={x:0,z:64},BOAT_START_POS={x:-35,z:92},VICTORY_ISLAND={finishLineX:90,finishLineZ:155,centerX:135,centerZ:165,radius:40},ISLAND_SHORE_R=40,ISLAND_WADE_R=46,ISLAND_POND={x:17,z:11,r:4.6,y:1.3},ISLAND_MOUNDS=[[-19,-15,4.5,.7],[-22,17,4,.5]],ISLAND_PIER={minX:-44,maxX:-24,minZ:-12,maxZ:4,y:1.12};function _sstep(e,t,n){const o=Math.max(0,Math.min(1,(n-e)/(t-e)));return o*o*(3-2*o)}function islandHeight(e,t){const n=Math.hypot(e,t);let o;n<=24?o=1.55:n<=29?o=1.55-.5*_sstep(24,29,n):n<=36?o=1.05:n<=40?o=1.05-.73*((n-36)/4):n<=47?o=.32*(1-_sstep(40,47,n)):o=-.4*_sstep(47,54,n);for(let r=0;r<ISLAND_MOUNDS.length;r++){const s=ISLAND_MOUNDS[r],i=Math.hypot(e-s[0],t-s[1])/s[2];i<2.4&&(o+=s[3]*Math.exp(-i*i))}const a=Math.hypot(e-ISLAND_POND.x,t-ISLAND_POND.z);return a<10&&(o-=.55*Math.exp(-Math.pow(a/4.2,2))),o}function islandGroundY(e,t){const n=e-VICTORY_ISLAND.centerX,o=t-VICTORY_ISLAND.centerZ;let a=islandHeight(n,o);return n>ISLAND_PIER.minX&&n<ISLAND_PIER.maxX&&o>ISLAND_PIER.minZ&&o<ISLAND_PIER.maxZ&&(a=Math.max(a,ISLAND_PIER.y)),a}let ISL={swings:[],seesaw:null,flames:[],beam:null,kites:[],koi:[],butterflies:[],ripples:[],foam:[],buoys:[],group:null,rippleT:0,lx:0,lz:0},AES_LITE=(function(){try{const e=new URLSearchParams(location.search),t=new URLSearchParams(location.hash.replace(/^#/,""));return!!(e.get("room")||t.get("room"))}catch{return!1}})(),AES_LOWEND=(function(){try{return!!(navigator.deviceMemory&&navigator.deviceMemory<=4||navigator.hardwareConcurrency&&navigator.hardwareConcurrency<=4||/CrOS/.test(navigator.userAgent))}catch{return!1}})();
/* ===== PENGATURAN GRAFIK: Otomatis / Rendah / Normal / Tinggi (tersimpan per perangkat) ===== */
const AES_GFX_DEVLOW=AES_LOWEND;
let AES_GFX_MODE="auto";
try{const _gm=localStorage.getItem("aes_gfx");if(_gm==="auto"||_gm==="low"||_gm==="normal"||_gm==="high")AES_GFX_MODE=_gm}catch{}
const AES_GFX_INFO={auto:{n:"Otomatis",i:"✨",d:"Menyesuaikan perangkat dan kelancaran. Disarankan."},low:{n:"Rendah",i:"🐢",d:"Paling ringan, untuk Chromebook atau HP lama. Gambar lebih sederhana."},normal:{n:"Normal",i:"⚖️",d:"Seimbang antara tajam dan lancar."},high:{n:"Tinggi",i:"💎",d:"Paling tajam dan detail. Butuh perangkat kuat, bisa terasa berat."}};
function aesGfxLow(){return AES_GFX_MODE==="low"||(AES_GFX_MODE==="auto"&&AES_GFX_DEVLOW)}
function aesGfxAdaptive(){return AES_GFX_MODE==="auto"||AES_GFX_MODE==="normal"}
function aesGfxBaseDpr(){const d=window.devicePixelRatio||1;return AES_GFX_MODE==="low"?1:AES_GFX_MODE==="normal"?Math.min(Math.max(d,1),1.5):AES_GFX_MODE==="high"?2:(AES_GFX_DEVLOW?1:Math.min(Math.max(d,1.75),2))}
function aesGfxRaceDpr(cap){const d=window.devicePixelRatio||1;return AES_GFX_MODE==="low"?1:AES_GFX_MODE==="normal"?Math.min(d,1.5):AES_GFX_MODE==="high"?Math.min(Math.max(d,1.75),2):Math.min(d,AES_GFX_DEVLOW?1:cap)}
function aesGfxMaxMesh(){return AES_GFX_MODE==="low"?10:AES_GFX_MODE==="high"?24:AES_GFX_MODE==="normal"?16:(AES_GFX_DEVLOW?10:16)}
function aesGfxMaxVis(){return AES_GFX_MODE==="low"?10:AES_GFX_MODE==="high"?30:AES_GFX_MODE==="normal"?18:(AES_GFX_DEVLOW?10:18)}
AES_LOWEND=aesGfxLow();
function aesGfxLabel(){const t=AES_GFX_INFO[AES_GFX_MODE];return t.i+" Grafik: "+t.n}
function aesGfxRefreshUI(){
  ["btn-teacher-gfx","btn-login-gfx"].forEach(id=>{const b=document.getElementById(id);if(b)b.textContent=aesGfxLabel()});
  const h=document.getElementById("btn-hud-gfx");if(h){h.textContent="🖥️";h.title=aesGfxLabel()}
  const m=document.getElementById("aes-gfx-modal");
  if(m)m.querySelectorAll("[data-gfx]").forEach(b=>{const on=b.dataset.gfx===AES_GFX_MODE;b.style.borderColor=on?"#fbbf24":"rgba(148,163,184,.35)";b.style.background=on?"rgba(251,191,36,.18)":"rgba(30,41,59,.9)";const ck=b.querySelector(".gfx-ck");if(ck)ck.textContent=on?"✓ Dipakai":""});
}
function aesGfxSet(m){
  if(!AES_GFX_INFO[m])return;
  AES_GFX_MODE=m;try{localStorage.setItem("aes_gfx",m)}catch{}
  AES_LOWEND=aesGfxLow();
  try{if(typeof renderer!=="undefined"&&renderer){baseDpr=aesGfxBaseDpr();curDpr=baseDpr;renderer.setPixelRatio(curDpr);renderer.setSize(window.innerWidth,window.innerHeight)}}catch{}
  aesGfxRefreshUI();
}
function aesGfxOpen(){
  try{playSoundEffect("click")}catch{}
  let m=document.getElementById("aes-gfx-modal");
  if(!m){
    m=document.createElement("div");m.id="aes-gfx-modal";
    m.style.cssText="position:fixed;inset:0;z-index:99990;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.72)";
    m.innerHTML='<div style="width:100%;max-width:380px;max-height:92vh;overflow-y:auto;background:#0f172a;border:1px solid rgba(148,163,184,.4);border-radius:20px;padding:18px;color:#fff;font-family:inherit"><div style="font-weight:800;font-size:17px">🖥️ Pengaturan Grafik</div><div style="font-size:12px;color:#94a3b8;margin:3px 0 12px">Pilih sesuai kemampuan perangkatmu. Pengaturan ini hanya berlaku di perangkat ini.</div><div id="aes-gfx-list" style="display:flex;flex-direction:column;gap:8px"></div><div style="font-size:11px;color:#94a3b8;margin-top:10px;line-height:1.45">Ketajaman layar dan detail balapan berubah langsung. Tepi halus (anti-alias) berlaku penuh setelah halaman dimuat ulang.</div><button id="aes-gfx-close" type="button" style="width:100%;margin-top:12px;padding:10px;border:0;border-radius:12px;background:#334155;color:#fff;font-weight:800;font-size:13px;cursor:pointer">Tutup</button></div>';
    document.body.appendChild(m);
    const L=m.querySelector("#aes-gfx-list");
    ["auto","low","normal","high"].forEach(k=>{const t=AES_GFX_INFO[k],b=document.createElement("button");b.type="button";b.dataset.gfx=k;b.style.cssText="text-align:left;padding:10px 12px;border-radius:14px;border:2px solid rgba(148,163,184,.35);color:#fff;cursor:pointer;font-family:inherit";b.innerHTML='<div style="display:flex;justify-content:space-between;gap:8px;font-weight:800;font-size:14px"><span>'+t.i+" "+t.n+'</span><span class="gfx-ck" style="color:#fbbf24;font-size:12px"></span></div><div style="font-size:11px;color:#cbd5e1;margin-top:2px;font-weight:500">'+t.d+"</div>";b.onclick=()=>aesGfxSet(k);L.appendChild(b)});
    m.querySelector("#aes-gfx-close").onclick=()=>{m.style.display="none"};
    m.addEventListener("click",e=>{if(e.target===m)m.style.display="none"});
    document.addEventListener("keydown",e=>{if(e.key==="Escape"&&m.style.display!=="none")m.style.display="none"});
  }
  m.style.display="flex";aesGfxRefreshUI();
}
if(document.readyState==="loading")document.addEventListener("DOMContentLoaded",aesGfxRefreshUI);else aesGfxRefreshUI();
let _aesLastFrame=0,_aesLastCfgRaw=null,_aesCullT=0,_teacherCmdSeen=!1;function aesMergeGeos(e,t){const n=[];let o=[],a=0,r=0;const s=()=>{if(!o.length)return;const i=new Float32Array(a*3),l=new Float32Array(a*3),m=new Uint16Array(r);let d=0,w=0;o.forEach(u=>{const H=u.attributes.position,M=u.attributes.normal,E=H.count;for(let g=0;g<E;g++)i[(d+g)*3]=H.getX(g),i[(d+g)*3+1]=H.getY(g),i[(d+g)*3+2]=H.getZ(g),l[(d+g)*3]=M.getX(g),l[(d+g)*3+1]=M.getY(g),l[(d+g)*3+2]=M.getZ(g);if(u.index)for(let g=0;g<u.index.count;g++)m[w++]=u.index.getX(g)+d;else for(let g=0;g<E;g++)m[w++]=d+g;d+=E});const p=new THREE.BufferGeometry;p.setAttribute("position",new THREE.BufferAttribute(i,3)),p.setAttribute("normal",new THREE.BufferAttribute(l,3)),p.setIndex(new THREE.BufferAttribute(m,1)),n.push(new THREE.Mesh(p,t)),o=[],a=0,r=0};return e.forEach(i=>{const l=i.attributes.position.count,m=i.index?i.index.count:l;a+l>6e4&&s(),o.push(i),a+=l,r+=m}),s(),n}function aesMeshMergeable(e){return e.isMesh&&!Array.isArray(e.material)&&e.material&&!e.material.map&&e.geometry&&e.geometry.attributes&&e.geometry.attributes.position&&!Object.prototype.hasOwnProperty.call(e,"onBeforeRender")&&!e.isInstancedMesh&&!e.isSkinnedMesh}function aesBakeDirect(e){try{const t=new Map,n=new Set;Object.values(e.userData||{}).forEach(o=>{o&&o.isObject3D?n.add(o):Array.isArray(o)&&o.forEach(a=>{a&&a.isObject3D&&n.add(a)})}),e.children.slice().forEach(o=>{if(!aesMeshMergeable(o)||n.has(o))return;o.updateMatrix();const a=o.geometry.clone();a.attributes.normal||a.computeVertexNormals(),a.applyMatrix4(o.matrix);let r=t.get(o.material.uuid);r||(r={mat:o.material,list:[]},t.set(o.material.uuid,r)),r.list.push(a),e.remove(o)}),t.forEach(o=>aesMergeGeos(o.list,o.mat).forEach(a=>e.add(a)))}catch(t){console.warn("aesBakeDirect",t)}}function aesMergeStaticRange(e){try{const t=scene.children.slice(e);scene.updateMatrixWorld(!0);const n=[];t.forEach(s=>s.traverse(i=>{aesMeshMergeable(i)&&n.push(i)}));const o=s=>[s.type,s.color?s.color.getHex():0,s.opacity,s.transparent?1:0,s.side,s.depthWrite?1:0,s.polygonOffset?1:0,s.polygonOffsetFactor||0,s.polygonOffsetUnits||0,s.shininess||0,s.flatShading?1:0].join("|"),a=new Map;n.forEach(s=>{const i=s.geometry.clone();i.attributes.normal||i.computeVertexNormals(),i.applyMatrix4(s.matrixWorld);const l=o(s.material);let m=a.get(l);m||(m={mat:s.material,list:[]},a.set(l,m)),m.list.push(i)}),n.forEach(s=>{s.parent&&s.parent.remove(s)});const r=s=>{s.children.slice().forEach(r),s.isGroup&&s.children.length===0&&s.parent&&s.parent.remove(s)};t.forEach(r),a.forEach(s=>aesMergeGeos(s.list,s.mat).forEach(i=>{i.matrixAutoUpdate=!1,i.updateMatrix(),scene.add(i)}))}catch(t){console.warn("aesMergeStaticRange",t)}}function aesMergeStaticTree(e,t){try{if(!e)return;const n=new Set((t||[]).filter(Boolean));e.updateMatrixWorld(!0);const o=d=>{for(let w=d;w&&w!==e;w=w.parent)if(n.has(w)||w.visible===!1)return!0;return!1},a=[];e.traverse(d=>{aesMeshMergeable(d)&&d.visible&&!o(d)&&a.push(d)});const r=new THREE.Matrix4().copy(e.matrixWorld).invert(),s=new THREE.Matrix4,i=(d,w)=>[d.type,d.color?d.color.getHex():0,d.opacity,d.transparent?1:0,d.side,d.depthWrite?1:0,d.depthTest===!1?0:1,d.polygonOffset?1:0,d.polygonOffsetFactor||0,d.polygonOffsetUnits||0,d.shininess||0,d.flatShading?1:0,d.fog===!1?0:1,d.emissive?d.emissive.getHex():0,w.renderOrder||0].join("|"),l=new Map;a.forEach(d=>{const w=d.geometry.clone();w.attributes.normal||w.computeVertexNormals(),w.applyMatrix4(s.multiplyMatrices(r,d.matrixWorld));const p=i(d.material,d);let u=l.get(p);u||(u={mat:d.material,ro:d.renderOrder||0,list:[]},l.set(p,u)),u.list.push(w)}),a.forEach(d=>{d.parent&&d.parent.remove(d)});const m=d=>{d.children.slice().forEach(m),d.isGroup&&d!==e&&d.children.length===0&&!n.has(d)&&d.parent&&d.parent.remove(d)};m(e),l.forEach(d=>aesMergeGeos(d.list,d.mat).forEach(w=>{w.renderOrder=d.ro,w.matrixAutoUpdate=!1,w.updateMatrix(),e.add(w)}))}catch(n){console.warn("aesMergeStaticTree",n)}}function aesDisposeDeep(e){try{e.traverse(t=>{t.geometry&&t.geometry.dispose(),t.material&&(Array.isArray(t.material)?t.material:[t.material]).forEach(n=>{n.map&&n.map.dispose(),n.dispose()})})}catch{}}function aesLiteCull(e){if(e-_aesCullT<250||!scene||!camera)return;_aesCullT=e;const t=camera.position.x,n=camera.position.z,o=gamePhase==="race"||gamePhase==="reflection",a=(l,m,d)=>{l.sort((w,p)=>w.d-p.d),l.forEach((w,p)=>{const u=p<m&&w.d<d;u&&!w.o.parent?scene.add(w.o):!u&&w.o.parent===scene&&scene.remove(w.o)})},r=[],s=[],i=[];Object.values(otherPlayers).forEach(l=>{l.offline||(l.mesh&&r.push({o:l.mesh,d:l.mesh.visible?Math.hypot((l.targetX||0)-t,(l.targetZ||0)-n):1/0}),l.boatMesh&&s.push({o:l.boatMesh,d:l.boatMesh.visible?Math.hypot(l.boatMesh.position.x-t,l.boatMesh.position.z-n):1/0}))}),Object.keys(parkedBoats).forEach(l=>{const m=parkedBoats[l].mesh;m&&i.push({o:m,d:m.visible?Math.hypot(m.position.x-t,m.position.z-n):1/0})}),a(r,1e9,1e9),a(s,1e9,1e9),a(i,1e9,1e9)}const TS_CFG_KEY="aes_teacher_cfg_v1",TS_LIVE_KEY="aes_teacher_live_v1";let _tsLastCfgStr="",_tsLive=!1,_tsTimer=null,_tsRestoredInfo=null;function tsSaveConfig(){try{const e=JSON.stringify(gameConfig);if(e===_tsLastCfgStr)return;try{localStorage.setItem(TS_CFG_KEY,JSON.stringify({v:1,savedAt:Date.now(),cfg:gameConfig})),_tsLastCfgStr=e}catch{const n=JSON.parse(e),o=a=>{a&&typeof a=="object"&&Object.keys(a).forEach(r=>{typeof a[r]=="string"&&a[r].length>6e4&&/^data:/.test(a[r])?a[r]="":o(a[r])})};o(n);try{localStorage.setItem(TS_CFG_KEY,JSON.stringify({v:1,savedAt:Date.now(),cfg:n,slim:!0})),_tsLastCfgStr=e}catch{}}}catch{}}function tsSaveLive(){try{if(!isTeacherMode||new URLSearchParams(location.search).get("room"))return;localStorage.setItem(TS_LIVE_KEY,JSON.stringify({v:1,savedAt:Date.now(),live:_tsLive,roomId,bk:AES_BROKER_IDX,phase:gamePhase,remaining:remainingSeconds,monitor:!!isTeacher3DMonitor}))}catch{}}function tsSaveAll(){tsSaveConfig(),tsSaveLive()}function tsStartAutosave(){_tsTimer||(_tsTimer=setInterval(()=>{tsSaveLive(),document.hidden||tsSaveConfig()},2e3),window.addEventListener("pagehide",tsSaveAll),window.addEventListener("beforeunload",tsSaveAll),document.addEventListener("visibilitychange",()=>{document.hidden&&tsSaveAll()}))}function tsWhenSceneReady(e,t){if(t=t||0,typeof scene<"u"&&scene&&camera&&renderer)try{e()}catch(n){console.error(n)}else t<60&&setTimeout(()=>tsWhenSceneReady(e,t+1),200)}function tsRestoreTeacherSession(){let e=null,t=null;try{e=JSON.parse(localStorage.getItem(TS_CFG_KEY)||"null")}catch{}try{t=JSON.parse(localStorage.getItem(TS_LIVE_KEY)||"null")}catch{}if(e&&e.cfg&&Array.isArray(e.cfg.buildings)&&Array.isArray(e.cfg.questions)&&e.cfg.buildings.length&&(gameConfig=Object.assign(JSON.parse(JSON.stringify(DEFAULT_GAME_DATA)),e.cfg),_tsLastCfgStr=JSON.stringify(gameConfig),remainingSeconds=(gameConfig.timerMinutes||30)*60,renderTeacherForm()),t&&t.live&&t.roomId&&Date.now()-t.savedAt<24*3600*1e3){const n=Math.max(0,(Date.now()-t.savedAt)/1e3);roomId=t.roomId,_tsLive=!0,_aesLinkShared=!0,typeof t.bk=="number"&&t.bk>=0&&t.bk<AES_BROKERS.length&&(AES_BROKER_IDX=t.bk);let o=t.phase||"waiting",a=typeof t.remaining=="number"?t.remaining:remainingSeconds;o==="explore"&&(a=Math.max(0,Math.round(a-n)),a<=0&&(o="walk_to_dock",a=0)),_tsRestoredInfo={ageSec:n,phase:o,monitor:!!t.monitor},document.getElementById("generated-link").value=aesBuildStudentLink(),document.getElementById("session-live-box").classList.remove("hidden"),document.getElementById("local-file-warning").classList.toggle("hidden",window.location.protocol!=="file:"),gamePhase="waiting",remainingSeconds=a,updateTimerDisplayUI();const r=document.getElementById("session-restored-note");if(r){r.classList.remove("hidden");const s=Math.max(1,Math.round(n/60));document.getElementById("session-restored-text").textContent=`♻️ Sesi sebelumnya dipulihkan otomatis (terakhir tersimpan ±${s} menit lalu): soal, link siswa, timer, dan pantauan siswa dilanjutkan.`}tsWhenSceneReady(()=>{o!=="waiting"&&applyPhaseChange(o),remainingSeconds=a,updateTimerDisplayUI(),startMasterClockLoop(),connectMultiplayerMQTT(),refreshOnlinePlayersUI(),o==="explore"&&setTimeout(()=>publishTeacherCommand({action:"SYNC_TIME",phase:"explore",remainingSeconds}),1500),t.monitor&&enterTeacher3DMonitor()})}}function tsClearAndRestart(){if(confirm("Mulai dari awal? Soal tersimpan dan sesi sebelumnya akan dihapus dari browser ini. Siswa yang masih memakai link lama tidak akan terhubung lagi.")){try{localStorage.removeItem(TS_CFG_KEY),localStorage.removeItem(TS_LIVE_KEY)}catch{}_tsLive=!1,_tsLastCfgStr="",window.removeEventListener("pagehide",tsSaveAll),window.removeEventListener("beforeunload",tsSaveAll),location.reload()}}const AES_BROKERS=[{name:"EMQX",url:"wss://broker.emqx.io:8084/mqtt"},{name:"HiveMQ",url:"wss://broker.hivemq.com:8884/mqtt"},{name:"Mosquitto",url:"wss://test.mosquitto.org:8081"}];let _aesCfgGot=!1,_aesLinkShared=!1,aesPubCfgNow=function(){},AES_BROKER_IDX=(function(){try{const e=new URLSearchParams(location.search),t=new URLSearchParams(location.hash.replace(/^#/,"")),n=parseInt(e.get("bk")||t.get("bk"));if(n>=0&&n<AES_BROKERS.length)return n;if(!(e.get("room")||t.get("room"))){const o=parseInt(localStorage.getItem("aes_bk"));if(o>=0&&o<AES_BROKERS.length)return o}}catch{}return 0})();function aesHasCustomBroker(){try{const e=new URLSearchParams(location.search).get("broker");return!!(e&&/^wss?:\/\//i.test(e))}catch{return!1}}function aesBrokerUrl(){try{const e=new URLSearchParams(location.search).get("broker");if(e&&/^wss?:\/\//i.test(e))return e}catch{}return AES_BROKERS[AES_BROKER_IDX].url}function aesUpdateConnChip(e){const t=document.getElementById("aes-conn-chip"),n=document.getElementById("aes-broker-select");if(n&&(n.options.length||AES_BROKERS.forEach((o,a)=>{const r=document.createElement("option");r.value=a,r.textContent=o.name,n.appendChild(r)}),n.value=String(AES_BROKER_IDX)),t){const o=AES_BROKERS[AES_BROKER_IDX].name;t.textContent=e?"🟢 Terhubung ke server "+o:"🔴 Belum tersambung ke server "+o+" (mencoba…)",t.style.color=e?"#6ee7b7":"#fcd34d"}}function aesSwitchBroker(e,t){if(e=parseInt(e),!(e>=0&&e<AES_BROKERS.length))return;if(AES_BROKER_IDX=e,mqttClient){try{mqttClient.end(!0)}catch{}mqttClient=null}connectMultiplayerMQTT();const n=document.getElementById("generated-link");n&&isTeacherMode&&(n.value=aesBuildStudentLink()),aesUpdateConnChip(!1),!t&&_aesLinkShared&&alert("Server diganti ke "+AES_BROKERS[e].name+". Salin ulang Link Siswa dan bagikan lagi ke siswa.")}function aesLoadMqttLib(e){if(window._aesLibBusy)return;window._aesLibBusy=!0,aesConnWarn(!0,0,"⏳ Memuat komponen koneksi…");const t=["https://cdn.jsdelivr.net/npm/mqtt@5.10.1/dist/mqtt.min.js","https://cdnjs.cloudflare.com/ajax/libs/mqtt/5.10.1/mqtt.min.js","https://unpkg.com/mqtt@5.10.1/dist/mqtt.min.js"],n=o=>{if(typeof mqtt<"u"){window._aesLibBusy=!1,aesConnWarn(!1),e();return}if(o>=t.length){window._aesLibBusy=!1,aesConnWarn(!0,0,"⚠️ Komponen koneksi gagal dimuat. Muat ulang halaman atau coba jaringan lain."),setTimeout(()=>aesLoadMqttLib(e),8e3);return}let a=!1;const r=()=>{a||(a=!0,n(o+1))},s=document.createElement("script");s.src=t[o],s.onload=r,s.onerror=r,document.head.appendChild(s),setTimeout(r,9e3)};n(0)}function aesCfgPayload(){let e=JSON.stringify(gameConfig);if(e.length<=18e4)return e;try{const t=JSON.parse(e),n=o=>{o&&typeof o=="object"&&Object.keys(o).forEach(a=>{const r=o[a];typeof r=="string"&&/^data:/.test(r)&&r.length>300?o[a]="":n(r)})};n(t),e=JSON.stringify(t)}catch{}return e}function aesUpdateWaitNote(){if(isTeacherMode)return;const e=document.getElementById("student-name-select");if(!e||!e.parentNode)return;let t=document.getElementById("aes-cfg-wait");t||(t=document.createElement("div"),t.id="aes-cfg-wait",t.style.cssText="font-size:11px;font-weight:800;color:#fcd34d;margin:6px 0",t.textContent="⏳ Menunggu daftar nama & soal dari guru… Jika lama, pastikan guru masih membuka halamannya.",e.parentNode.insertBefore(t,e)),t.style.display=_aesCfgGot?"none":"block"}let _aesNCache=1,_aesNT=0;function aesOnlineN(){const e=Date.now();if(e-_aesNT>1500){_aesNT=e;let t=1;Object.values(otherPlayers).forEach(n=>{!n.offline&&n.role==="student"&&t++}),_aesNCache=t}return _aesNCache}function aesPosMinMove(){const e=aesOnlineN();return e<=12?0:e<=30?200:e<=60?350:600}function aesPosIdle(){const e=aesOnlineN();return e<=30?1e3:e<=60?2500:4e3}function aesStateEvery(){const e=aesOnlineN();return e<=20?2e3:e<=50?4e3:6e3}function aesBuildStudentLink(aesShort){let t=`${window.location.href.split("?")[0].split("#")[0]}?room=${roomId}&bk=${AES_BROKER_IDX}`;try{const n=new URLSearchParams(location.search).get("broker");if(n&&/^wss?:\/\//i.test(n)&&(t+=`&broker=${encodeURIComponent(n)}`),aesShort)return t;if(typeof LZString<"u"&&LZString.compressToEncodedURIComponent){const a=JSON.parse(JSON.stringify(gameConfig)),r=l=>{l&&typeof l=="object"&&Object.keys(l).forEach(m=>{const d=l[m];typeof d=="string"&&(/^data:/.test(d)||/^(image|img|photo|gambar)/i.test(m)&&d.length>300)?l[m]="":r(d)})};r(a);const s=()=>LZString.compressToEncodedURIComponent(JSON.stringify(a));let i=s();t+=`&session=${i}`}}catch{}try{aesShareRefreshSoon()}catch{}return t}let _connWarnT=null;function aesConnWarn(e,t,n){const o=document.getElementById("conn-warning");if(o){if(o.dataset.def===void 0&&(o.dataset.def=o.textContent),_connWarnT&&(clearTimeout(_connWarnT),_connWarnT=null),!e){o.classList.add("hidden");return}_connWarnT=setTimeout(()=>{o.textContent=n||o.dataset.def,o.classList.remove("hidden")},t||0)}}window.addEventListener("DOMContentLoaded",()=>{(function(){const e=new URLSearchParams(location.search),t=new URLSearchParams(location.hash.replace(/^#/,""));!!(e.get("room")||t.get("room"))&&!ACCESS_GATE.GATE_STUDENTS?checkURLParameters():gateStart(checkURLParameters)})();try{initThreeJSWorld(),rebuildCityBuildings3D()}catch(e){console.error(e)}try{initAnalogJoystick(),initCameraOrbitControls()}catch(e){console.error(e)}}),document.addEventListener("visibilitychange",()=>{document.hidden?saveMyProgress():(lastPosKey="",broadcastMyPos(),broadcastMyState())}),window.addEventListener("pagehide",()=>{saveMyProgress()}),window.addEventListener("beforeunload",()=>{saveMyProgress(),mqttClient&&mqttClient.connected&&myPlayer.hasJoinedGame&&mqttClient.publish(`aes_class_3d/${roomId}/player_leave`,JSON.stringify({id:myPlayer.id}))});function checkURLParameters(){const e=new URLSearchParams(window.location.search),t=new URLSearchParams(window.location.hash.replace(/^#/,"")),n=e.get("room")||t.get("room"),o=e.get("session")||t.get("session");if(n){if(roomId=n,isTeacherMode=!1,myPlayer.role="spectator",myPlayer.hasJoinedGame=!1,o&&typeof LZString<"u")try{const a=LZString.decompressFromEncodedURIComponent(o);if(a){const r=JSON.parse(a);r&&r.buildings&&(gameConfig=r,_aesCfgGot=!0)}}catch{}if(!_aesCfgGot){const a=e.get("names")||t.get("names");if(a&&typeof LZString<"u")try{const r=JSON.parse(LZString.decompressFromEncodedURIComponent(a));Array.isArray(r)&&(gameConfig.students=r.map(s=>String(s||"").trim()).filter(Boolean),_aesCfgGot=!0)}catch{}}gamePhase="waiting",remainingSeconds=(gameConfig.timerMinutes||30)*60,document.getElementById("btn-login-back-teacher").classList.add("hidden"),document.getElementById("hud-teacher-quick-bar").classList.add("hidden"),document.getElementById("btn-back-teacher").classList.add("hidden"),showStudentLoginModal(),connectMultiplayerMQTT()}else{isTeacherMode=!0,myPlayer.role="teacher",myPlayer.hasJoinedGame=!1,gamePhase="waiting",remainingSeconds=(gameConfig.timerMinutes||30)*60,renderTeacherForm(),document.getElementById("teacher-screen").classList.remove("hidden");try{tsRestoreTeacherSession()}catch(a){console.error(a)}tsStartAutosave()}}function escapeXml(e){return String(e).replace(/[\u0000-\u0008\u000B\u000C\u000E-\u001F\uFFFE\uFFFF]/g,"").replace(/[\uD800-\uDBFF](?![\uDC00-\uDFFF])|(?<![\uD800-\uDBFF])[\uDC00-\uDFFF]/g,"").replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;").replace(/"/g,"&quot;").replace(/'/g,"&apos;")}function createWordParagraphXml(e,t=100){const n=e.map(o=>{const a=o.mono?"Consolas":"Calibri";return`<w:r><w:rPr><w:rFonts w:ascii="${a}" w:hAnsi="${a}"/>${o.bold||o.highlight?"<w:b/>":""}${o.color?`<w:color w:val="${o.color}"/>`:o.highlight?'<w:color w:val="000000"/>':""}${o.highlight?'<w:highlight w:val="yellow"/>':""}<w:sz w:val="${o.size||22}"/></w:rPr><w:t xml:space="preserve">${escapeXml(o.text)}</w:t></w:r>`}).join("");return`<w:p><w:pPr><w:spacing w:after="${t}"/></w:pPr>${n}</w:p>`}function triggerFileDownload(e,t){const n=URL.createObjectURL(e),o=document.createElement("a");o.href=n,o.download=t,o.style.display="none",document.body.appendChild(o),o.click(),setTimeout(()=>{try{document.body.removeChild(o),URL.revokeObjectURL(n)}catch{}},4e3)}function ensureJSZip(){return typeof JSZip>"u"?(alert("Pustaka pembuat file Word (JSZip) belum termuat. Periksa koneksi internet lalu muat ulang halaman."),!1):!0}async function downloadDocxPromptTemplate(){playSoundEffect("click"),syncFormToConfig();const e=[];e.push(createWordParagraphXml([{text:"PROMPT GENERATOR SIMPEL — AES CLASS (SIAP DOWNLOAD JSON)",bold:!0,size:30,color:"0284C7"}],120)),e.push(createWordParagraphXml([{text:"1. Isi bagian STABILO KUNING dengan kata kunci singkat saja. AI akan menuliskan penjelasan lengkapnya.",size:21}],50)),e.push(createWordParagraphXml([{text:"2. HAPUS baris gedung (G1-G20) di bawah yang tidak ingin digunakan.",highlight:!0,size:21}],50)),e.push(createWordParagraphXml([{text:"3. Daftar Nama Siswa BOLEH DIKOSONGKAN: siswa akan mengetik namanya sendiri saat membuka game.",size:21}],120)),e.push(createWordParagraphXml([{text:"================ MULAI SALIN DARI SINI ================",bold:!0,size:22,color:"0284C7"}],90)),e.push(createWordParagraphXml([{text:`INSTRUKSI AI: Ubah kata kunci setiap gedung di bawah menjadi URAIAN MATERI LENGKAP (minimal 2-3 paragraf + contoh nyata). WAJIB gunakan fitur Code Interpreter / File Generator untuk menghasilkan file 'materi_aes_class.json' yang siap saya download, serta tampilkan juga blok kode JSON murninya. Format JSON WAJIB PERSIS sesuai skema dan aturan di bagian bawah (nama properti, struktur, dan tipe data tidak boleh diubah atau ditambah) karena akan langsung diimpor ke game. PENTING: untuk SETIAP gedung kamu juga WAJIB membuat sendiri 1 soal pilihan ganda (properti "quiz") berdasarkan isi "content" gedung itu, tanpa menunggu saya menuliskannya. JSON yang tidak punya "quiz" di salah satu gedung dianggap SALAH dan harus kamu perbaiki sebelum dikirim.`,bold:!0,size:21,color:"DC2626"}],100)),e.push(createWordParagraphXml([{text:"• Mata Pelajaran & Topik: ",bold:!0},{text:`[${gameConfig.subjectName||"Tulis mata pelajaran & topik"}]`,highlight:!0}],55)),e.push(createWordParagraphXml([{text:"• Kelas: ",bold:!0},{text:`[${gameConfig.gradeLevel||"Tulis kelas"}]`,highlight:!0}],55)),e.push(createWordParagraphXml([{text:"• Waktu Belajar (Menit): ",bold:!0},{text:`[${gameConfig.timerMinutes||30}]`,highlight:!0}],55)),e.push(createWordParagraphXml([{text:"• Jumlah Soal Pilihan Ganda: ",bold:!0},{text:`[${gameConfig.questions.length||10}]`,highlight:!0}],55)),e.push(createWordParagraphXml([{text:"• Daftar Nama Siswa: ",bold:!0},{text:(gameConfig.students||[]).length?`[${gameConfig.students.join(", ")}]`:"[KOSONGKAN jika siswa mengetik nama sendiri]",highlight:!0}],55)),e.push(createWordParagraphXml([{text:"• Soal Koin per Gedung: ",bold:!0},{text:'kamu (AI) yang membuatnya otomatis, saya tidak perlu menulis soalnya. Setiap gedung WAJIB punya 1 soal pilihan ganda (properti "quiz" di dalam objek gedung, sejajar dengan "content") yang dijawab siswa SETELAH selesai membaca materi gedung itu. Soal harus bisa dijawab hanya dari isi "content" gedung tersebut dan tidak boleh sama dengan soal lomba perahu.',size:20,bold:!0}],100)),e.push(createWordParagraphXml([{text:"DAFTAR GEDUNG (HAPUS BARIS GEDUNG YANG TIDAK DIPAKAI):",bold:!0,size:22}],65));for(let m=0;m<20;m++){const d=BUILDING_ARCHETYPES[m],w=gameConfig.buildings[m];e.push(createWordParagraphXml([{text:`G${m+1} | Gedung: "${d.type}" (style: "${d.style}", color: "${d.color}") | Sub-Materi: `,bold:!0,size:20},{text:`[${w?w.name:"Tulis sub-materi G"+(m+1)+" atau HAPUS baris ini"}]`,highlight:!0,size:20},{text:" → buat: content + quiz",bold:!0,size:20,color:"B45309"}],45))}e.push(createWordParagraphXml([{text:"ATURAN FORMAT JSON (WAJIB DIPATUHI):",bold:!0,size:22,color:"DC2626"}],55)),['1. "students": isi sesuai Daftar Nama Siswa di atas. Jika daftar itu kosong atau masih tertulis KOSONGKAN, tulis "students": [] (array kosong).','2. "id" gedung berurutan sesuai gedung yang dipakai: "b1", "b2", "b3", dst. "type", "style", dan "color" harus persis seperti pada baris gedung di atas.','3. "image" selalu string kosong "".','4. WAJIB: SETIAP objek di "buildings" harus punya properti "quiz" yang kamu buat sendiri: { "q": pertanyaan, "options": TEPAT 4 pilihan, "correct": angka 0-3 }. 0 = A, 1 = B, 2 = C, 3 = D. Soal harus sesuai isi "content" gedung yang sama. Jumlah "quiz" HARUS sama dengan jumlah gedung.','5. "questions" (soal lomba perahu) berjumlah sesuai Jumlah Soal di atas; tiap soal punya "q", "image" (""), "options" (TEPAT 4), dan "correct" (angka 0-3). Soal lomba tidak boleh sama dengan soal koin gedung.','6. "timerMinutes" berupa angka. "subjectName" dan "gradeLevel" berupa teks sesuai data di atas.','7. Di dalam "content", gunakan \\n untuk pergantian baris/paragraf. Jangan gunakan tanda kutip ganda di dalam teks (pakai tanda kutip tunggal). Rumus ditulis di antara $...$ dan setiap backslash ditulis ganda.',"8. Keluarkan JSON yang valid: tanpa komentar, tanpa koma berlebih di akhir, tanpa properti tambahan.",`9. Sebarkan posisi jawaban benar ("correct") secara merata dan acak antara 0, 1, 2, dan 3 di seluruh soal (soal gedung maupun soal lomba). Jangan biarkan satu posisi mendominasi atau membentuk pola. Hindari opsi seperti 'Semua jawaban benar' atau 'A dan B benar'.`,`10. CEK SEBELUM MENGIRIM: hitung jumlah gedung dan jumlah "quiz". Jika ada gedung tanpa "quiz", tambahkan dulu. Setelah JSON, tulis satu baris: 'Cek: N gedung, N quiz gedung, M soal lomba.'`].forEach(m=>e.push(createWordParagraphXml([{text:m,size:20}],40))),e.push(createWordParagraphXml([{text:"SKEMA JSON:",bold:!0,size:22,color:"0284C7"}],55)),`{\n  "subjectName": "Nama Mapel",\n  "gradeLevel": "Kelas",\n  "timerMinutes": 30,\n  "students": ["Siswa 1", "Siswa 2"],\n  "buildings": [\n    {\n      "id": "b1",\n      "type": "Perpustakaan Pusat",\n      "style": "library",\n      "name": "Perpustakaan Pusat (Judul Sub-Materi G1)",\n      "color": "#0284c7",\n      "image": "",\n      "content": "Penjelasan lengkap beberapa paragraf...",\n      "quiz": { "q": "Pertanyaan gedung G1 dari isi content G1...", "options": ["A","B","C","D"], "correct": 0 }\n    },\n    {\n      "id": "b2",\n      "type": "Grand Cafe & Resto",\n      "style": "cafe",\n      "name": "Grand Cafe & Resto (Judul Sub-Materi G2)",\n      "color": "#ea580c",\n      "image": "",\n      "content": "Penjelasan lengkap beberapa paragraf...",\n      "quiz": { "q": "Pertanyaan gedung G2 dari isi content G2...", "options": ["A","B","C","D"], "correct": 2 }\n    }\n  ],\n  "questions": [\n    {\n      "q": "Pertanyaan...",\n      "image": "",\n      "options": ["Opsi A", "Opsi B", "Opsi C", "Opsi D"],\n      "correct": 0\n    }\n  ]\n}`.split(`\n`).forEach(m=>e.push(createWordParagraphXml([{text:m,mono:!0,size:19}],28)));const n=`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><w:document xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"><w:body>${e.join("")}<w:sectPr><w:pgSz w:w="11906" w:h="16838"/><w:pgMar w:top="1134" w:right="1134" w:bottom="1134" w:left="1134"/></w:sectPr></w:body></w:document>`,o='<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Types xmlns="http://schemas.openxmlformats.org/package/2006/content-types"><Default Extension="rels" ContentType="application/vnd.openxmlformats-package.relationships+xml"/><Default Extension="xml" ContentType="application/xml"/><Override PartName="/word/document.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/></Types>',a='<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships"><Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target="word/document.xml"/></Relationships>',r='<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships"></Relationships>';if(!ensureJSZip())return;const s=new JSZip;s.file("[Content_Types].xml",o),s.folder("_rels").file(".rels",a);const i=s.folder("word");i.file("document.xml",n),i.folder("_rels").file("document.xml.rels",r);const l=await s.generateAsync({type:"blob",mimeType:"application/vnd.openxmlformats-officedocument.wordprocessingml.document"});triggerFileDownload(l,"Prompt_Simpel_AES_CLASS.docx")}function openPasteJsonModal(){playSoundEffect("click"),document.getElementById("paste-json-modal").classList.remove("hidden")}function closePasteJsonModal(){document.getElementById("paste-json-modal").classList.add("hidden")}function sanitizeAndParseJSON(e){let t=String(e).trim();const n=t.indexOf("{"),o=t.lastIndexOf("}");n!==-1&&o!==-1&&o>n&&(t=t.substring(n,o+1));const a=JSON.parse(t);if(!a.buildings||!a.questions)throw new Error("Properti 'buildings' atau 'questions' tidak ditemukan.");return a.buildings.forEach((r,s)=>{const i=BUILDING_ARCHETYPES[s%BUILDING_ARCHETYPES.length];r.color||(r.color=i.color),r.type||(r.type=i.type),r.style||(r.style=i.style),r.id||(r.id="b"+(s+1)),typeof r.image!="string"&&(r.image=""),(!r.quiz||typeof r.quiz!="object")&&(r.quiz={q:"",options:["","","",""],correct:0}),Array.isArray(r.quiz.options)||(r.quiz.options=["","","",""]),r.quiz.q=String(r.quiz.q||""),r.quiz.correct=parseInt(r.quiz.correct)||0}),a.questions.forEach(r=>{typeof r.image!="string"&&(r.image=""),typeof r.correct!="number"&&(r.correct=parseInt(r.correct)||0)}),a.students=Array.isArray(a.students)?a.students.map(r=>String(r||"").trim()).filter(Boolean):[],balanceAnswerKeys(a),a}function balanceAnswerKeys(e){const t=[];(e.buildings||[]).forEach(i=>{i&&i.quiz&&t.push(i.quiz)}),(e.questions||[]).forEach(i=>t.push(i));const n=t.filter(i=>Array.isArray(i.options)&&i.options.length===4&&i.options.every(l=>String(l||"").trim())&&i.correct>=0&&i.correct<=3&&!optionsDependOnOrder(i.options)),o=n.length,a=[0,0,0,0];if(!o)return{total:0,dist:a};const r=i=>{for(let l=i.length-1;l>0;l--){const m=Math.floor(Math.random()*(l+1));[i[l],i[m]]=[i[m],i[l]]}return i};let s=[];for(let i=0;i<60;i++){const l=[];for(let d=0;d<o;d++)l.push(d%4);s=r(l);let m=!1;for(let d=2;d<o;d++)if(s[d]===s[d-1]&&s[d]===s[d-2]){m=!0;break}if(!m)break}return n.forEach((i,l)=>{const m=i.options[i.correct],d=r(i.options.filter((u,H)=>H!==i.correct)),w=[];let p=0;for(let u=0;u<4;u++)w.push(u===s[l]?m:d[p++]);i.options=w,i.correct=s[l],a[s[l]]++}),{total:o,dist:a}}function shuffleAnswerKeysNow(){playSoundEffect("click"),syncFormToConfig();const e=balanceAnswerKeys(gameConfig);if(renderTeacherForm(),!e.total){alert("Belum ada soal yang bisa diacak (butuh 4 opsi terisi dan kunci jawaban terpilih).");return}alert(`Kunci jawaban diacak untuk ${e.total} soal (gedung + lomba perahu).\nSebaran: A=${e.dist[0]}, B=${e.dist[1]}, C=${e.dist[2]}, D=${e.dist[3]}`)}function collectQuizWarnings(e){const t=[],n=(o,a)=>{const r=Array.isArray(a.options)?a.options:[];if(!String(a.q||"").trim()){t.push(`${o}: pertanyaan kosong`);return}r.length!==4||r.some(s=>!String(s||"").trim())?t.push(`${o}: opsi harus tepat 4 dan tidak kosong (terbaca ${r.length})`):a.correct>=0&&a.correct<=3||t.push(`${o}: nilai "correct" harus 0-3`)};return(e.buildings||[]).forEach((o,a)=>{String(o.content||"").trim()||t.push(`Gedung G${a+1}: materi (content) kosong`),!o.quiz||!String(o.quiz.q||"").trim()?t.push(`Gedung G${a+1}: belum punya soal`):n(`Soal gedung G${a+1}`,o.quiz)}),(e.questions||[]).forEach((o,a)=>n(`Soal lomba #${a+1}`,o)),t}function formatImportWarnings(){const e=collectQuizWarnings(gameConfig);if(!e.length)return"";const t=e.some(n=>/belum punya soal|pertanyaan kosong/.test(n));return`\n\n⚠️ Perlu dicek (${e.length}):\n- `+e.slice(0,8).join(`\n- `)+(e.length>8?`\n- ...dan ${e.length-8} lainnya`:"")+(t?`\n\n💡 Ada gedung tanpa soal. Kirim ke AI: 'Tambahkan properti quiz {q, options (4), correct 0-3} ke SETIAP gedung di JSON ini berdasarkan isi content-nya, lalu kirim ulang JSON lengkap.' Atau isi manual di kolom Soal Koin tiap gedung.`:"")}function applyPastedJSON(e=!1){const t=document.getElementById("paste-json-textarea").value;if(!t.trim()){alert("Silakan Paste kode JSON terlebih dahulu.");return}try{gameConfig=sanitizeAndParseJSON(t),renderTeacherForm(),rebuildCityBuildings3D(),closePasteJsonModal(),playSoundEffect("complete_building"),e&&exportCurrentConfigJSON(),alert(`Berhasil menerapkan ${gameConfig.buildings.length} Gedung Materi dan ${gameConfig.questions.length} Soal!`+formatImportWarnings())}catch(n){alert("Format JSON belum valid: "+n.message)}}function applyPastedJSONAndDownload(){applyPastedJSON(!0)}function exportCurrentConfigJSON(){playSoundEffect("click"),syncFormToConfig();const e=new Blob([JSON.stringify(gameConfig,null,2)],{type:"application/json"}),t=document.createElement("a");t.href=URL.createObjectURL(e),t.download="materi_aes_class.json",t.click()}function importJSON(e){const t=e.target.files[0];if(!t)return;const n=new FileReader;n.onload=o=>{try{gameConfig=sanitizeAndParseJSON(o.target.result),renderTeacherForm(),rebuildCityBuildings3D(),playSoundEffect("complete_building"),alert(`Berhasil mengimpor ${gameConfig.buildings.length} Gedung dan ${gameConfig.questions.length} Soal!`+formatImportWarnings())}catch(a){alert("Gagal membaca file JSON: "+a.message)}},n.readAsText(t)}function createWordTableCellXml(e,t={}){const n=t.fill?`<w:shd w:val="clear" w:color="auto" w:fill="${t.fill}"/>`:"",o=t.align?`<w:jc w:val="${t.align}"/>`:"",a=t.color?`<w:color w:val="${t.color}"/>`:'<w:color w:val="1E293B"/>',r=t.bold?"<w:b/>":"",s=t.size||20,l=String(e??"-").split(`\n`).map(m=>`<w:p><w:pPr>${o}<w:spacing w:before="40" w:after="40"/></w:pPr><w:r><w:rPr><w:rFonts w:ascii="Calibri" w:hAnsi="Calibri"/>${r}${a}<w:sz w:val="${s}"/></w:rPr><w:t xml:space="preserve">${escapeXml(m)}</w:t></w:r></w:p>`).join("");return`<w:tc><w:tcPr>${n}<w:vAlign w:val="center"/></w:tcPr>${l}</w:tc>`}function createWordTableXml(e,t,n="0284C7"){const o='<w:tblBorders><w:top w:val="single" w:sz="6" w:space="0" w:color="CBD5E1"/><w:left w:val="single" w:sz="6" w:space="0" w:color="CBD5E1"/><w:bottom w:val="single" w:sz="6" w:space="0" w:color="CBD5E1"/><w:right w:val="single" w:sz="6" w:space="0" w:color="CBD5E1"/><w:insideH w:val="single" w:sz="4" w:space="0" w:color="E2E8F0"/><w:insideV w:val="single" w:sz="4" w:space="0" w:color="E2E8F0"/></w:tblBorders>',a='<w:tblCellMar><w:top w:w="100" w:type="dxa"/><w:left w:w="120" w:type="dxa"/><w:bottom w:w="100" w:type="dxa"/><w:right w:w="120" w:type="dxa"/></w:tblCellMar>',r=`<w:tr><w:trPr><w:tblHeader/></w:trPr>${e.map(l=>createWordTableCellXml(l,{fill:n,color:"FFFFFF",bold:!0,align:"center",size:20})).join("")}</w:tr>`,s=t.map((l,m)=>{const d=m%2===1?"F8FAFC":"FFFFFF";return`<w:tr>${l.map(w=>typeof w=="object"&&w!==null?createWordTableCellXml(w.text,{fill:w.fill||d,color:w.color,bold:w.bold,align:w.align,size:w.size||19}):createWordTableCellXml(w,{fill:d,size:19})).join("")}</w:tr>`}).join(""),i=`<w:tblGrid>${e.map(()=>`<w:gridCol w:w="${Math.floor(14800/e.length)}"/>`).join("")}</w:tblGrid>`;return`<w:tbl><w:tblPr><w:tblW w:w="5000" w:type="pct"/>${o}${a}</w:tblPr>${i}${r}${s}</w:tbl>`}async function buildAndDownloadDocxFile(e,t,n=!0){const o=n?'<w:pgSz w:w="16838" w:h="11906" w:orient="landscape"/>':'<w:pgSz w:w="11906" w:h="16838"/>',a=`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><w:document xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"><w:body>${e.join("")}<w:sectPr>${o}<w:pgMar w:top="1000" w:right="1000" w:bottom="1000" w:left="1000"/></w:sectPr></w:body></w:document>`,r='<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Types xmlns="http://schemas.openxmlformats.org/package/2006/content-types"><Default Extension="rels" ContentType="application/vnd.openxmlformats-package.relationships+xml"/><Default Extension="xml" ContentType="application/xml"/><Override PartName="/word/document.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/></Types>',s='<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships"><Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target="word/document.xml"/></Relationships>',i='<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships"></Relationships>';if(!ensureJSZip())return;const l=new JSZip;l.file("[Content_Types].xml",r),l.folder("_rels").file(".rels",s);const m=l.folder("word");m.file("document.xml",a),m.folder("_rels").file("document.xml.rels",i);const d=await l.generateAsync({type:"blob",mimeType:"application/vnd.openxmlformats-officedocument.wordprocessingml.document"});triggerFileDownload(d,t)}async function exportStudentReportDOCX(){playSoundEffect("click");const e=getAllStudentsListForReport(),t=gameConfig.questions.length,n=gameConfig.buildings.length,o=new Date().toLocaleString("id-ID"),a=[];a.push(createWordParagraphXml([{text:"LAPORAN NILAI, PROGRES KUIS & CATATAN BELAJAR SISWA — AES CLASS",bold:!0,size:28,color:"0284C7"}],80)),a.push(createWordParagraphXml([{text:`Mata Pelajaran / Topik: ${gameConfig.subjectName||"-"} | Kelas: ${gameConfig.gradeLevel||"-"} | Tanggal Unduh: ${o}`,bold:!0,size:20,color:"475569"}],160));const r=["No","Nama Siswa","Status Akhir","Lokasi Terakhir","Gedung Dipelajari","Catatan Gedung Terisi","Progres Soal","Putaran 1 (Benar / Salah)","Diulangi (Benar / Salah)","Soal Gedung (Benar / Salah)","Nilai Akhir (0-100)"],s=e.length>0?e.map((i,l)=>{const m=i.finishedRace?"DI PULAU VICTORY":i.atDock?"Sedang Mendayung":"Di Kota",d=i.buildingNotes||{},w=Object.values(d).filter(p=>String(p||"").trim().length>0).length;return[{text:String(l+1),align:"center"},{text:i.name||"-",bold:!0},{text:m,align:"center"},{text:i.currentBuilding||"-"},{text:`${i.completedCount||0} / ${n}`,align:"center"},{text:`${w} / ${n} Gedung`,align:"center"},{text:`${i.boatStrokes||0} / ${t}`,align:"center"},{text:`Benar: ${i.initialCorrect||0} | Salah: ${i.initialWrong||0}`,align:"center"},{text:`Benar: ${i.retryCorrect||0} | Salah: ${i.retryWrong||0}`,align:"center"},{text:(()=>{const p=Object.values(i.buildingQuizResult||{});return`Benar: ${p.filter(u=>u==="correct").length} | Salah: ${p.filter(u=>u==="wrong").length} (dari ${gameConfig.buildings.filter(u=>buildingHasQuiz(u)).length})`})(),align:"center"},{text:String(i.finalScore||0),bold:!0,align:"center",color:"047857"}]}):[[{text:"-",align:"center"},{text:"Belum ada data siswa",align:"center"},"-","-","-","-","-","-","-","-","-"]];a.push(createWordTableXml(r,s,"059669")),a.push(createWordParagraphXml([{text:"",size:20}],120)),await buildAndDownloadDocxFile(a,"Laporan_Nilai_Siswa_AES_CLASS.docx",!0)}async function exportStudentReflectionDOCX(){playSoundEffect("click");const e=getAllStudentsListForReport(),t=new Date().toLocaleString("id-ID"),n=[];n.push(createWordParagraphXml([{text:"LAPORAN REFLEKSI PEMBELAJARAN SISWA — AES CLASS",bold:!0,size:28,color:"7C3AED"}],80)),n.push(createWordParagraphXml([{text:`Mata Pelajaran / Topik: ${gameConfig.subjectName||"-"} | Kelas: ${gameConfig.gradeLevel||"-"} | Tanggal Unduh: ${t}`,bold:!0,size:20,color:"475569"}],160));const o=["No","Nama Siswa","Nilai Kuis","Status Refleksi","Perasaan Mengikuti Kelas","Materi yang Paling Dipahami","Bagian yang Masih Sulit / Kendala","Pesan & Harapan Siswa"],a=e.length>0?e.map((r,s)=>{const i=r.reflectionSubmitted?"SUDAH MENGISI":"BELUM MENGISI";return[{text:String(s+1),align:"center"},{text:r.name||"-",bold:!0},{text:String(r.finalScore||0),bold:!0,align:"center"},{text:i,align:"center",bold:!0,color:r.reflectionSubmitted?"047857":"B91C1C"},{text:r.reflectionFeeling||"-"},{text:r.reflectionUnderstood||"-"},{text:r.reflectionDifficulty||"-"},{text:r.reflectionSuggestion||"-"}]}):[[{text:"-",align:"center"},{text:"Belum ada data refleksi siswa",align:"center"},"-","-","-","-","-","-"]];n.push(createWordTableXml(o,a,"7C3AED")),n.push(createWordParagraphXml([{text:"",size:20}],120)),await buildAndDownloadDocxFile(n,"Laporan_Refleksi_Siswa_AES_CLASS.docx",!0)}async function exportStudentNotesDOCX(){playSoundEffect("click");const e=getAllStudentsListForReport(),t=new Date().toLocaleString("id-ID"),n=[];n.push(createWordParagraphXml([{text:"LAPORAN CATATAN BELAJAR SISWA DI TIAP GEDUNG — AES CLASS",bold:!0,size:28,color:"0284C7"}],80)),n.push(createWordParagraphXml([{text:`Mata Pelajaran / Topik: ${gameConfig.subjectName||"-"} | Kelas: ${gameConfig.gradeLevel||"-"} | Tanggal Unduh: ${t}`,bold:!0,size:20,color:"475569"}],160));const o=["No","Nama Siswa","Gedung Dipelajari","Rincian Catatan Siswa di Setiap Gedung (G1 s.d. GN)"],a=e.length>0?e.map((r,s)=>{const i=r.buildingNotes||{},l=gameConfig.buildings.map((m,d)=>{const w=(i[m.id]||"").trim();return`[G${d+1} - ${m.name}]: ${w||"(Belum mencatat)"}`}).join(`\n`);return[{text:String(s+1),align:"center"},{text:r.name||"-",bold:!0},{text:`${r.completedCount||0} / ${gameConfig.buildings.length}`,align:"center"},{text:l}]}):[[{text:"-",align:"center"},{text:"Belum ada data catatan siswa",align:"center"},"-","-"]];n.push(createWordTableXml(o,a,"0284C7")),n.push(createWordParagraphXml([{text:"",size:20}],120)),await buildAndDownloadDocxFile(n,"Laporan_Catatan_Gedung_Siswa_AES_CLASS.docx",!0)}async function exportStudentFullRecapDOCX(){
  playSoundEffect("click");
  const list=getAllStudentsListForReport(),totalQ=gameConfig.questions.length,blds=gameConfig.buildings,
    quizBlds=blds.filter(b=>buildingHasQuiz(b)),when=new Date().toLocaleString("id-ID"),out=[];
  const P=(runs,after)=>createWordParagraphXml(runs,after==null?80:after);
  const GAP=()=>P([{text:"",size:16}],60);
  const PAGE='<w:p><w:r><w:br w:type="page"/></w:r></w:p>';
  const calc=r=>{
    const notes=r.buildingNotes||{},res=r.buildingQuizResult||{};
    const noteCnt=blds.filter(b=>String(notes[b.id]||"").trim().length>0).length;
    const bOk=quizBlds.filter(b=>res[b.id]==="correct").length,bBad=quizBlds.filter(b=>res[b.id]==="wrong").length;
    return{notes,res,noteCnt,bOk,bBad,bPct:quizBlds.length?Math.round(bOk/quizBlds.length*100):0};
  };
  out.push(P([{text:"REKAP LENGKAP SISWA — AES CLASS",bold:!0,size:30,color:"0284C7"}],80));
  out.push(P([{text:`Mata Pelajaran / Topik: ${gameConfig.subjectName||"-"} | Kelas: ${gameConfig.gradeLevel||"-"} | Tanggal Unduh: ${when}`,bold:!0,size:20,color:"475569"}],100));
  out.push(P([{text:"Isi: (1) ringkasan semua siswa, lalu (2) rincian tiap siswa: catatan di tiap gedung, hasil soal koin tiap gedung, skor soal lomba perahu, dan refleksi.",size:19,color:"64748B"}],140));
  out.push(P([{text:"A. RINGKASAN SEMUA SISWA",bold:!0,size:24,color:"0F172A"}],80));
  const head=["No","Nama Siswa","Gedung Dipelajari","Catatan Terisi","Soal Koin Gedung (Benar / Salah)","Skor Gedung (0-100)","Koin","Lomba Perahu Putaran 1 (Benar / Salah)","Nilai Lomba (0-100)","Refleksi"];
  const rows=list.length?list.map((r,i)=>{
    const c=calc(r);
    return[{text:String(i+1),align:"center"},{text:r.name||"-",bold:!0},
      {text:`${r.completedCount||0} / ${blds.length}`,align:"center"},
      {text:`${c.noteCnt} / ${blds.length}`,align:"center"},
      {text:`Benar: ${c.bOk} | Salah: ${c.bBad} (dari ${quizBlds.length})`,align:"center"},
      {text:String(c.bPct),bold:!0,align:"center",color:"047857"},
      {text:String(r.coins||0),align:"center"},
      {text:`Benar: ${r.initialCorrect||0} | Salah: ${r.initialWrong||0} (dari ${totalQ})`,align:"center"},
      {text:String(r.finalScore||0),bold:!0,align:"center",color:"047857"},
      {text:r.reflectionSubmitted?"SUDAH":"BELUM",bold:!0,align:"center",color:r.reflectionSubmitted?"047857":"B91C1C"}];
  }):[[{text:"-",align:"center"},{text:"Belum ada data siswa",align:"center"},"-","-","-","-","-","-","-","-"]];
  out.push(createWordTableXml(head,rows,"0284C7"));
  out.push(GAP());
  list.forEach((r,idx)=>{
    const c=calc(r);
    out.push(PAGE);
    out.push(P([{text:`B.${idx+1}  ${r.name||"-"}`,bold:!0,size:28,color:"0284C7"}],60));
    out.push(P([{text:`Status: ${r.finishedRace?"Sudah di Pulau Victory":r.atDock?"Sedang di dermaga / mendayung":"Masih di kota"} | Gedung dipelajari: ${r.completedCount||0} / ${blds.length} | Koin: ${r.coins||0}`,size:20,color:"475569"}],120));
    out.push(P([{text:"1. Catatan Belajar & Hasil Soal Koin per Gedung",bold:!0,size:22}],60));
    const bh=["Gedung","Soal Koin","Catatan Belajar Siswa"];
    const br=blds.length?blds.map((b,i)=>{
      const st=c.res[b.id],note=String(c.notes[b.id]||"").trim();
      const koin=st==="correct"?{text:"✓ Benar",bold:!0,color:"047857",align:"center"}:st==="wrong"?{text:"✗ Salah",bold:!0,color:"B91C1C",align:"center"}:buildingHasQuiz(b)?{text:"Belum dijawab",color:"64748B",align:"center"}:{text:"Tidak ada soal",color:"64748B",align:"center"};
      return[{text:`G${i+1} - ${b.name||b.type||""}`,bold:!0},koin,{text:note||"(Belum mencatat)",color:note?"1E293B":"94A3B8"}];
    }):[["-","-","-"]];
    out.push(createWordTableXml(bh,br,"0284C7"));
    out.push(P([{text:`Skor soal koin gedung: Benar ${c.bOk}, Salah ${c.bBad}, dari ${quizBlds.length} soal gedung | Skor ${c.bPct} / 100`,bold:!0,size:20,color:"047857"}],120));
    out.push(P([{text:"2. Skor Soal Kuis Lomba Perahu",bold:!0,size:22}],60));
    out.push(createWordTableXml(["Progres Soal","Putaran 1: Benar","Putaran 1: Salah","Pengulangan: Benar","Pengulangan: Salah","Nilai Akhir (0-100)"],
      [[{text:`${r.boatStrokes||0} / ${totalQ}`,align:"center"},{text:String(r.initialCorrect||0),align:"center",color:"047857",bold:!0},{text:String(r.initialWrong||0),align:"center",color:"B91C1C",bold:!0},{text:String(r.retryCorrect||0),align:"center"},{text:String(r.retryWrong||0),align:"center"},{text:String(r.finalScore||0),align:"center",bold:!0,color:"047857"}]],"059669"));
    out.push(GAP());
    out.push(P([{text:"3. Refleksi Pembelajaran",bold:!0,size:22}],60));
    if(r.reflectionSubmitted){
      out.push(createWordTableXml(["Pertanyaan","Jawaban Siswa"],[
        [{text:"Perasaan mengikuti pembelajaran",bold:!0},{text:r.reflectionFeeling||"-"}],
        [{text:"Materi yang paling dipahami",bold:!0},{text:r.reflectionUnderstood||"-"}],
        [{text:"Bagian yang masih sulit",bold:!0},{text:r.reflectionDifficulty||"-"}],
        [{text:"Pesan & harapan",bold:!0},{text:r.reflectionSuggestion||"-"}]],"7C3AED"));
    }else out.push(P([{text:"Siswa belum mengisi refleksi.",size:20,color:"B91C1C",bold:!0}],80));
  });
  await buildAndDownloadDocxFile(out,"Rekap_Lengkap_Siswa_AES_CLASS.docx",!0);
}
function exportStudentReportCSV(){exportStudentReportDOCX()}function exportStudentReflectionCSV(){exportStudentReflectionDOCX()}function renderTeacherForm(){document.getElementById("input-timer").value=gameConfig.timerMinutes||30,document.getElementById("input-building-count").value=gameConfig.buildings.length,document.getElementById("input-students").value=(gameConfig.students||[]).join(`\n`),renderBuildingsEditor(),renderQuestionsEditor()}function renderBuildingsEditor(){const e=document.getElementById("buildings-editor-list");e.innerHTML="",gameConfig.buildings.forEach((t,n)=>{const o=document.createElement("div");o.className="bg-slate-950 border border-slate-800 rounded-xl p-4 space-y-2.5";const a=BUILDING_ARCHETYPES.map(r=>{const s=gameConfig.buildings.findIndex((i,l)=>l!==n&&i.style===r.style);return`<option value="${r.style}" ${t.style===r.style?"selected":""} ${s>=0?"disabled":""}>${r.icon} ${r.type} (lokasi tetap ${r.code})${s>=0?" - dipakai G"+(s+1):""}</option>`}).join("");o.innerHTML=`\n          <div class="flex items-center justify-between gap-2">\n            <span class="text-xs font-extrabold px-2.5 py-1 rounded-md text-slate-950 bg-amber-400">GEDUNG G${n+1}</span>\n            <select onchange="changeBuildingArchetype(${n}, this.value)" class="bg-slate-900 border border-slate-700 text-xs text-sky-300 font-bold rounded-lg px-2.5 py-1">${a}</select>\n            ${gameConfig.buildings.length>1?`<button onclick="removeBuildingItem(${n})" class="text-xs text-rose-400 hover:underline ml-auto">Hapus</button>`:""}\n          </div>\n          <input type="text" value="${(t.name||"").replace(/"/g,"&quot;")}" oninput="updateBuildingName(${n}, this.value)" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-3 py-1.5 text-xs text-white font-bold" />\n          <textarea rows="3" oninput="gameConfig.buildings[${n}].content = this.value" class="w-full bg-slate-900 border border-slate-700 rounded-lg p-2.5 text-xs text-slate-200 custom-scroll">${aesEscTA(t.content)}</textarea>\n          ${(()=>{t.quiz||(t.quiz={q:"",options:["","","",""],correct:0});const r=t.quiz;for(;r.options.length<4;)r.options.push("");return`\n          <div class="border-t border-slate-800 pt-2.5 space-y-2">\n            <div class="text-[11px] font-extrabold text-amber-300">🪙 Soal Koin Gedung G${n+1} (benar di percobaan pertama = 1 koin; kosongkan soal jika tidak dipakai)</div>\n            <textarea rows="2" placeholder="Tulis pertanyaan gedung ini..." oninput="gameConfig.buildings[${n}].quiz.q = this.value" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-3 py-2 text-xs text-white font-semibold">${aesEscTA(r.q||"")}</textarea>\n            <div class="grid grid-cols-1 sm:grid-cols-2 gap-2">\n              ${r.options.map((s,i)=>`\n                <div class="flex items-center gap-2 bg-slate-900 border border-slate-800 rounded-lg px-2.5 py-2">\n                  <input type="radio" name="bquiz_correct_${n}" ${r.correct===i?"checked":""} onchange="gameConfig.buildings[${n}].quiz.correct = ${i}" />\n                  <span class="text-xs font-extrabold text-sky-400">${String.fromCharCode(65+i)}.</span>\n                  <input type="text" value="${String(s||"").replace(/&/g,"&amp;").replace(/"/g,"&quot;")}" oninput="gameConfig.buildings[${n}].quiz.options[${i}] = this.value" class="w-full bg-transparent text-xs text-slate-200 focus:outline-none" />\n                </div>\n              `).join("")}\n            </div>\n          </div>`})()}\n        `,e.appendChild(o)})}function changeBuildingArchetype(e,t){const n=BUILDING_ARCHETYPES.find(o=>o.style===t)||BUILDING_ARCHETYPES[0];if(gameConfig.buildings.some((o,a)=>a!==e&&o.style===n.style)){renderBuildingsEditor();return}gameConfig.buildings[e].style=n.style,gameConfig.buildings[e].type=n.type,gameConfig.buildings[e].color=n.color,renderBuildingsEditor(),rebuildCityBuildings3D()}function updateBuildingName(e,t){gameConfig.buildings[e].name=t,rebuildCityBuildings3D()}function adjustBuildingsCount(e){const t=Math.max(1,Math.min(20,parseInt(e)||5));for(;gameConfig.buildings.length<t;){const n=gameConfig.buildings.length,o=new Set;gameConfig.buildings.forEach(s=>{const i=BUILDING_ARCHETYPES.findIndex(l=>l.style===s.style);i>=0&&o.add(i)});const a=aesFirstFreeArchetype(o),r=BUILDING_ARCHETYPES[a>=0?a:n%BUILDING_ARCHETYPES.length];gameConfig.buildings.push({id:"b"+(n+1),type:r.type,style:r.style,name:`${r.type} (Materi G${n+1})`,color:r.color,image:"",quiz:{q:"",options:["","","",""],correct:0},content:`Materi Gedung G${n+1}...`})}gameConfig.buildings.length>t&&(gameConfig.buildings=gameConfig.buildings.slice(0,t)),renderBuildingsEditor(),rebuildCityBuildings3D()}function addBuildingItem(){playSoundEffect("click"),adjustBuildingsCount(gameConfig.buildings.length+1),document.getElementById("input-building-count").value=gameConfig.buildings.length}function removeBuildingItem(e){playSoundEffect("click"),gameConfig.buildings.splice(e,1),document.getElementById("input-building-count").value=gameConfig.buildings.length,renderBuildingsEditor(),rebuildCityBuildings3D()}function renderQuestionsEditor(){const e=document.getElementById("questions-editor-list");e.innerHTML="",gameConfig.questions.forEach((t,n)=>{const o=document.createElement("div");o.className="bg-slate-950 border border-slate-800 rounded-xl p-4 space-y-2.5",o.innerHTML=`\n          <div class="flex items-center justify-between">\n            <span class="text-xs font-bold text-amber-400">Soal #${n+1}</span>\n            ${gameConfig.questions.length>1?`<button onclick="removeQuestionItem(${n})" class="text-xs text-rose-400 hover:underline">Hapus Soal</button>`:""}\n          </div>\n          <textarea rows="2" oninput="gameConfig.questions[${n}].q = this.value" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-3 py-2 text-xs text-white font-semibold">${aesEscTA(t.q)}</textarea>\n          <div class="grid grid-cols-1 sm:grid-cols-2 gap-2">\n            ${t.options.map((a,r)=>`\n              <div class="flex items-center gap-2 bg-slate-900 border border-slate-800 rounded-lg px-2.5 py-2">\n                <input type="radio" name="correct_${n}" ${t.correct===r?"checked":""} onchange="gameConfig.questions[${n}].correct = ${r}" />\n                <span class="text-xs font-extrabold text-sky-400">${String.fromCharCode(65+r)}.</span>\n                <input type="text" value="${a.replace(/&/g,"&amp;").replace(/"/g,"&quot;")}" oninput="gameConfig.questions[${n}].options[${r}] = this.value" class="w-full bg-transparent text-xs text-slate-200 focus:outline-none" />\n              </div>\n            `).join("")}\n          </div>\n        `,e.appendChild(o)})}function addQuestionItem(){playSoundEffect("click"),gameConfig.questions.push({q:"Pertanyaan baru...",image:"",options:["Opsi A","Opsi B","Opsi C","Opsi D"],correct:0}),renderQuestionsEditor()}function removeQuestionItem(e){playSoundEffect("click"),gameConfig.questions.splice(e,1),renderQuestionsEditor()}function syncFormToConfig(){gameConfig.timerMinutes=parseInt(document.getElementById("input-timer").value)||30;const e=document.getElementById("input-students").value.split(`\n`).map(t=>t.trim()).filter(Boolean);gameConfig.students=e}function generateSessionAndLink(){try{aesRevokeIfLive()}catch{}if(playSoundEffect("complete_building"),syncFormToConfig(),rebuildCityBuildings3D(),myPlayer.role="teacher",myPlayer.hasJoinedGame=!1,removeMyAvatarFromScene(),clearAllOtherPlayersFromScene(),mqttClient){try{mqttClient.end(!0)}catch{}mqttClient=null}roomId=aesNewRoomId(),_aesLinkShared=!1,document.getElementById("generated-link").value=aesBuildStudentLink(),document.getElementById("session-live-box").classList.remove("hidden"),document.getElementById("local-file-warning").classList.toggle("hidden",window.location.protocol!=="file:"),document.getElementById("session-live-box").scrollIntoView({behavior:"smooth"}),gamePhase="waiting",remainingSeconds=gameConfig.timerMinutes*60,updateTimerDisplayUI(),startMasterClockLoop(),connectMultiplayerMQTT(),refreshOnlinePlayersUI(),_tsLive=!0,document.getElementById("session-restored-note")&&document.getElementById("session-restored-note").classList.add("hidden"),tsSaveAll()}function copyStudentLink(){playSoundEffect("click");const e=document.getElementById("generated-link");try{syncFormToConfig()}catch{}e.value=aesBuildStudentLink(),_aesLinkShared=!0;try{aesPubCfgNow()}catch{}e.select(),navigator.clipboard.writeText(e.value),alert("Link siswa berhasil disalin!")}function toggleTeacherCleanUI(){playSoundEffect("click"),isTeacherCleanUI=!isTeacherCleanUI,document.getElementById("hud-top-bar").classList.toggle("opacity-0",isTeacherCleanUI),document.getElementById("hud-top-bar").classList.toggle("pointer-events-none",isTeacherCleanUI),document.getElementById("camera-control-box").classList.toggle("hidden",isTeacherCleanUI),document.getElementById("btn-clean-ui").textContent=isTeacherCleanUI?"👁️ Tampilkan Panel":"👁️ Sembunyikan Panel"}function toggleMinimizeQuizBody(){playSoundEffect("click");const e=document.getElementById("quiz-body-content");e.classList.toggle("hidden"),document.getElementById("btn-min-quiz").textContent=e.classList.contains("hidden")?"🔼 Buka Soal":"🔽 Kecilkan"}function teacherStartLearningPhase(){playSoundEffect("complete_building"),remainingSeconds<=0&&(remainingSeconds=(gameConfig.timerMinutes||30)*60),applyPhaseChange("explore"),publishTeacherCommand({action:"SET_PHASE",phase:"explore",remainingSeconds})}function teacherAdjustTime(e){playSoundEffect("click"),remainingSeconds=Math.max(0,remainingSeconds+e),remainingSeconds>0&&gamePhase==="walk_to_dock"?applyPhaseChange("explore"):remainingSeconds===0&&gamePhase==="explore"&&applyPhaseChange("walk_to_dock"),updateTimerDisplayUI(),publishTeacherCommand({action:"SYNC_TIME",phase:gamePhase,remainingSeconds})}function teacherCallToDockPhase(){playSoundEffect("whistle_dock"),remainingSeconds=0,applyPhaseChange("walk_to_dock"),publishTeacherCommand({action:"SET_PHASE",phase:"walk_to_dock",remainingSeconds:0})}function teacherStartBoatRace(){playSoundEffect("complete_building"),applyPhaseChange("race"),publishTeacherCommand({action:"SET_PHASE",phase:"race",remainingSeconds:0}),isTeacherMode&&!isTeacher3DMonitor&&enterTeacher3DMonitor()}function teacherStartReflectionPhase(){playSoundEffect("finish_island"),applyPhaseChange("reflection"),publishTeacherCommand({action:"SET_PHASE",phase:"reflection",remainingSeconds:0})}let micRecorder=null,micStream=null,micChunks=[],micTimer=null,lastAnnId=null,annAudio=null,annBannerTimer=null;const MIC_MAX_SECONDS=20;function showAnnBanner(e,t,n){let o=document.getElementById("aes-ann-banner");o||(o=document.createElement("div"),o.id="aes-ann-banner",o.style.cssText="position:fixed;top:12px;left:50%;transform:translateX(-50%);z-index:99999;background:#f59e0b;color:#0f172a;font-weight:800;font-size:13px;padding:10px 18px;border-radius:999px;box-shadow:0 8px 24px rgba(0,0,0,.4);max-width:92vw;text-align:center;cursor:default",document.body.appendChild(o)),o.textContent=e,o.style.display="block",o.style.cursor=t?"pointer":"default",o.onclick=t||null,clearTimeout(annBannerTimer),n&&(annBannerTimer=setTimeout(hideAnnBanner,n))}document.addEventListener("keydown",function(e){if(!e.altKey||e.ctrlKey||e.metaKey||String(e.key).toLowerCase()!=="m")return;const t=e.target,n=t&&t.tagName?t.tagName.toUpperCase():"";n==="INPUT"||n==="TEXTAREA"||t&&t.isContentEditable||(e.preventDefault(),typeof toggleTeacherMic=="function"&&toggleTeacherMic())});function hideAnnBanner(){const e=document.getElementById("aes-ann-banner");e&&(e.style.display="none")}function setMicButtons(e){document.querySelectorAll(".btn-teacher-mic").forEach(t=>{t.textContent=e?"⏹":"🎤",t.title=e?"Klik untuk mengirim pengumuman":"Pengumuman suara ke siswa (Alt+M)",t.style.background=e?"#e11d48":"",t.style.color=e?"#fff":""})}(function(){function e(){const t=!!(isTeacherMode&&isTeacher3DMonitor),n=document.getElementById("hud-left-card"),o=document.getElementById("btn-hud-mic");n&&n.classList.toggle("teacher-hud",t),o&&(o.style.display=t?"":"none")}setInterval(e,300)})(),(function(){let e=null,t=null;function n(){const o=!isTeacherMode;if(o===e)return;e=o;const a=document.getElementById("hud-online-count"),r=document.getElementById("hud-online-list"),s=document.getElementById("hud-map-title"),i=document.getElementById("hud-map-legend");t===null&&i&&(t=i.innerHTML),a&&(a.style.display=o?"none":""),r&&(r.style.display=o?"none":""),s&&(s.textContent=o?"🗺️ Peta Kota":"🗺️ Peta & Pantauan Siswa"),i&&(i.innerHTML=o?"<span>🟡 G1..GN</span><span>🟢 Selesai</span><span>🏝️ Pulau</span><span>🟩 Kamu</span>":t)}setInterval(n,300)})();async function toggleTeacherMic(){if(!isTeacherMode)return;if(micRecorder&&micRecorder.state==="recording"){micRecorder.stop();return}if(pendingAnn&&cancelPendingAnnouncement(!0),!mqttClient||!mqttClient.connected){alert("Belum tersambung ke ruang kelas. Tunggu beberapa detik lalu coba lagi.");return}if(!navigator.mediaDevices||!window.MediaRecorder){alert("Browser ini tidak mendukung rekam suara. Gunakan Chrome atau Edge terbaru.");return}try{micStream=await navigator.mediaDevices.getUserMedia({audio:!0})}catch{alert("Izin mikrofon ditolak. Izinkan akses mikrofon untuk halaman ini di pengaturan browser.");return}micChunks=[];const e=["audio/webm;codecs=opus","audio/mp4","audio/webm"].find(t=>MediaRecorder.isTypeSupported(t))||"";try{micRecorder=new MediaRecorder(micStream,e?{mimeType:e,audioBitsPerSecond:24e3}:{audioBitsPerSecond:24e3})}catch{micStream.getTracks().forEach(n=>n.stop()),alert("Gagal memulai perekaman suara.");return}micRecorder.ondataavailable=t=>{t.data&&t.data.size&&micChunks.push(t.data)},micRecorder.onstop=()=>{clearTimeout(micTimer),micStream&&micStream.getTracks().forEach(o=>o.stop()),setMicButtons(!1);const t=micRecorder&&micRecorder.mimeType||"audio/webm",n=new Blob(micChunks,{type:t});if(annCancelled){annCancelled=!1,showAnnBanner("Rekaman dibatalkan, tidak ada yang terkirim.",null,2500);return}n.size>0&&queueAnnouncement(n,t)},micRecorder.start(),setMicButtons(!0),annCancelled=!1,showAnnActionBanner(`🎤 Merekam... klik ⏹ untuk kirim (maks. ${MIC_MAX_SECONDS} dtk)`,"✕ Batal",cancelRecording),micTimer=setTimeout(()=>{micRecorder&&micRecorder.state==="recording"&&micRecorder.stop()},MIC_MAX_SECONDS*1e3)}let annCancelled=!1,pendingAnn=null;const ANN_UNDO_SECONDS=4;function showAnnActionBanner(e,t,n){showAnnBanner("",null,0);const o=document.getElementById("aes-ann-banner");o.textContent="";const a=document.createElement("span");a.textContent=e;const r=document.createElement("button");return r.type="button",r.textContent=t,r.style.cssText="margin-left:10px;background:#0f172a;color:#fff;border:0;border-radius:999px;padding:4px 12px;font-weight:800;font-size:12px;cursor:pointer",r.onclick=function(s){s.stopPropagation(),n()},o.appendChild(a),o.appendChild(r),a}function cancelRecording(){micRecorder&&micRecorder.state==="recording"&&(annCancelled=!0,micRecorder.stop())}function queueAnnouncement(e,t){pendingAnn&&cancelPendingAnnouncement(!0);const n={left:ANN_UNDO_SECONDS,timer:null};pendingAnn=n;const o=()=>`📤 Terkirim ke siswa dalam ${n.left} dtk...`,a=showAnnActionBanner(o(),"↩ Batalkan",()=>cancelPendingAnnouncement(!1));n.timer=setInterval(()=>{n.left--,n.left<=0?(clearInterval(n.timer),pendingAnn=null,sendAnnouncementBlob(e,t)):a.textContent=o()},1e3)}function cancelPendingAnnouncement(e){pendingAnn&&(clearInterval(pendingAnn.timer),pendingAnn=null,e||showAnnBanner("Pengumuman dibatalkan, tidak ada yang terkirim.",null,2500))}document.addEventListener("keydown",function(e){e.key==="Escape"&&(micRecorder&&micRecorder.state==="recording"?cancelRecording():pendingAnn&&cancelPendingAnnouncement(!1))});function sendAnnouncementBlob(e,t){const n=new FileReader;n.onloadend=()=>{const o=String(n.result||"").split(",")[1]||"";if(!o){showAnnBanner("Gagal memproses rekaman.",null,3e3);return}mqttClient&&mqttClient.connected?(mqttClient.publish(`aes_class_3d/${roomId}/announce`,JSON.stringify({aid:Date.now()+"_"+Math.floor(Math.random()*9999),mime:t,data:o}),{qos:0,retain:!1}),showAnnBanner("✅ Pengumuman terkirim ke siswa yang sedang online",null,3e3)):showAnnBanner("Koneksi terputus, pengumuman tidak terkirim.",null,4e3)},n.readAsDataURL(e)}function playTeacherAnnouncement(e){if(!e||!e.data||e.aid===lastAnnId)return;lastAnnId=e.aid;try{annAudio&&annAudio.pause()}catch{}annAudio=new Audio(`data:${e.mime||"audio/webm"};base64,${e.data}`),showAnnBanner("📢 Pengumuman dari Guru...",null,0),annAudio.onended=()=>hideAnnBanner(),annAudio.onerror=()=>showAnnBanner("Pengumuman suara tidak bisa diputar di perangkat ini",null,4e3);const t=annAudio.play();t&&t.catch&&t.catch(()=>showAnnBanner("📢 Ada pengumuman dari guru — ketuk di sini untuk mendengarkan",()=>{annAudio.play().catch(()=>{}),showAnnBanner("📢 Pengumuman dari Guru...",null,0)},0))}function publishTeacherCommand(e){e=Object.assign({sentAt:Date.now()},e),mqttClient&&!mqttClient.connected&&aesConnWarn(!0,0),mqttClient&&mqttClient.publish(`aes_class_3d/${roomId}/teacher_cmd`,JSON.stringify(e),{retain:!0,qos:1})}function focusCameraOnStudent(e){playSoundEffect("click"),teacherFollowPlayerId=e,enterTeacher3DMonitor(),otherPlayers[e]&&(document.getElementById("teacher-follow-indicator").classList.remove("hidden"),document.getElementById("teacher-follow-name").textContent=`Memantau: ${otherPlayers[e].name}`)}function stopFollowingStudent(){playSoundEffect("click"),teacherFollowPlayerId=null,document.getElementById("teacher-follow-indicator").classList.add("hidden")}function applyPhaseChange(e){const t=gamePhase;gamePhase=e,myPlayer.phase=e,(e!=="race"&&e!=="reflection"||e==="race"&&t==="reflection")&&(raceInited=!1),["waiting-teacher-banner","walk-to-dock-banner","ready-on-boat-banner","island-explore-banner","race-quiz-panel"].forEach(a=>document.getElementById(a).classList.add("hidden"));const n=document.getElementById("hud-phase-label"),o=document.getElementById("teacher-phase-status");if(e==="waiting")myPlayer.finishedRace=!1,myPlayer.atDock=!1,racePassiveDrift=0,n.textContent="⏳ MENUNGGU GURU MEMULAI WAKTU BELAJAR",o&&(o.textContent="MENUNGGU GURU MEMULAI"),!isTeacher3DMonitor&&myPlayer.role==="student"&&myPlayer.hasJoinedGame&&document.getElementById("waiting-teacher-banner").classList.remove("hidden"),setArrowGuideVisibility(!1),setBoatsVisibility(!1);else if(e==="explore")myPlayer.finishedRace=!1,myPlayer.atDock=!1,racePassiveDrift=0,myPlayer.z>64&&(myPlayer.x=0,myPlayer.z=59),n.textContent="🏙️ FASE 1: PELAJARI GEDUNG BERURUTAN MULAI DARI G1",o&&(o.textContent="BELAJAR AKTIF BERJALAN"),!isTeacher3DMonitor&&myPlayer.hasJoinedGame&&document.getElementById("joystick-zone").classList.remove("hidden"),setArrowGuideVisibility(!1),setBoatsVisibility(!1);else if(e==="walk_to_dock")closeBuildingModal(),document.getElementById("building-prompt").classList.add("hidden"),n.textContent="🧭 IKUTI PANAH KUNING MENUJU DERMAGA LAUT!",o&&(o.textContent="SISWA MENUJU DERMAGA"),!myPlayer.atDock&&!isTeacher3DMonitor&&myPlayer.hasJoinedGame?(document.getElementById("walk-to-dock-banner").classList.remove("hidden"),setArrowGuideVisibility(!0)):myPlayer.atDock&&!isTeacher3DMonitor&&myPlayer.role==="student"&&myPlayer.hasJoinedGame&&(document.getElementById("ready-on-boat-banner").classList.remove("hidden"),setBoatsVisibility(!1));else if(e==="race"){if(closeBuildingModal(),document.getElementById("building-prompt").classList.add("hidden"),setArrowGuideVisibility(!1),racePassiveDrift=0,n.textContent="🏁 FASE 2: LOMBA SPEEDBOAT MENYEBERANGI LAUT KE PULAU VICTORY!",o&&(o.textContent="LOMBA MENUJU PULAU VICTORY"),myPlayer.role==="student"&&myPlayer.hasJoinedGame)if(raceInited)myPlayer.finishedRace||(myPlayer.atDock=!0);else{myPlayer.atDock=!0,myPlayer.boatStrokes=0,myPlayer.initialCorrect=0,myPlayer.initialWrong=0,myPlayer.retryCorrect=0,myPlayer.retryWrong=0,myPlayer.finishedRace=!1,myPlayer.finalScore=0,firstAttemptTracker={},questionQueue=gameConfig.questions.map((a,r)=>r);for(let a=questionQueue.length-1;a>0;a--){const r=Math.floor(Math.random()*(a+1));[questionQueue[a],questionQueue[r]]=[questionQueue[r],questionQueue[a]]}Object.keys(bqOrderCache).forEach(a=>delete bqOrderCache[a]),raceInited=!0}setBoatsVisibility(!0),!isTeacher3DMonitor&&myPlayer.role==="student"&&myPlayer.hasJoinedGame&&(myPlayer.finishedRace?(myPlayer.currentBuilding="🏝️ Pantai Pulau Victory",myAvatarMesh&&(myAvatarMesh.visible=!0,myAvatarMesh.position.set(myPlayer.x,islandGroundY(myPlayer.x,myPlayer.z)+.05,myPlayer.z)),myBoatMesh&&(myBoatMesh.visible=!1),document.getElementById("joystick-zone").classList.remove("hidden"),document.getElementById("island-explore-banner").classList.remove("hidden")):(document.getElementById("joystick-zone").classList.add("hidden"),document.getElementById("race-quiz-panel").classList.remove("hidden"),renderCurrentRaceQuestion()))}else if(e==="reflection"){if(closeBuildingModal(),document.getElementById("building-prompt").classList.add("hidden"),setArrowGuideVisibility(!1),n.textContent="📝 FASE 3: REFLEKSI PEMBELAJARAN DI PULAU VICTORY",o&&(o.textContent="PENGISIAN REFLEKSI DI PULAU"),myPlayer.role==="student"&&myPlayer.hasJoinedGame){if(!myPlayer.finishedRace){const a=Math.max(1,gameConfig.questions.length);myPlayer.finalScore=Math.round(myPlayer.initialCorrect/a*100),myPlayer.finishedRace=!0,myPlayer.x=VICTORY_ISLAND.centerX-16+(Math.random()-.5)*10,myPlayer.z=VICTORY_ISLAND.centerZ+(Math.random()-.5)*10,myPlayer.rotY=Math.PI/2,cameraYaw=-Math.PI/2}myPlayer.currentBuilding="🏝️ Pulau Victory (Refleksi)",myAvatarMesh&&(myAvatarMesh.visible=!0,myAvatarMesh.position.set(myPlayer.x,islandGroundY(myPlayer.x,myPlayer.z)+.05,myPlayer.z)),myBoatMesh&&(myBoatMesh.visible=!1),document.getElementById("joystick-zone").classList.remove("hidden"),document.getElementById("island-explore-banner").classList.remove("hidden"),myPlayer.reflectionSubmitted||openReflectionModal()}Object.values(otherPlayers).forEach(a=>{a.finishedRace=!0,a.mesh&&(a.mesh.visible=!0),a.boatMesh&&(a.boatMesh.visible=!1)})}updateTimerDisplayUI(),broadcastMyState()}function openReflectionModal(){document.getElementById("reflection-sim-close").classList.toggle("hidden",!isTeacherMode),document.getElementById("reflection-modal").classList.remove("hidden")}function submitStudentReflection(){const e=document.getElementById("ref-feeling").value,t=document.getElementById("ref-understood").value.trim(),n=document.getElementById("ref-difficulty").value.trim(),o=document.getElementById("ref-suggestion").value.trim();if(!t||!n){alert("Mohon isi pertanyaan nomor 2 dan nomor 3 terlebih dahulu sebelum mengirim refleksi!");return}playSoundEffect("complete_building"),myPlayer.reflectionSubmitted=!0,myPlayer.reflectionFeeling=e,myPlayer.reflectionUnderstood=t,myPlayer.reflectionDifficulty=n,myPlayer.reflectionSuggestion=o||"-",myPlayer.currentBuilding="🏝️ Pulau Victory (Refleksi Terkirim ✓)",document.getElementById("reflection-modal").classList.add("hidden"),broadcastMyState(),alert("✅ Terima kasih! Refleksi belajarmu sudah terkirim ke Guru. Silakan jalan-jalan menikmati pantai Pulau Victory!")}function setBoatsVisibility(e){const t=myPlayer.role==="student"&&myPlayer.hasJoinedGame&&!isTeacher3DMonitor;myAvatarMesh&&(myAvatarMesh.visible=t&&(!e&&!myPlayer.atDock||myPlayer.finishedRace)),myBoatMesh&&(myBoatMesh.visible=t&&(e||myPlayer.atDock)&&!myPlayer.finishedRace,e&&!myPlayer.finishedRace&&myBoatMesh.position.set(BOAT_START_POS.x,.2,BOAT_START_POS.z)),Object.values(otherPlayers).forEach(n=>{const o=(e||n.atDock)&&!n.finishedRace;n.mesh&&(n.mesh.visible=!o&&!n.insideBuilding),n.boatMesh&&(n.boatMesh.visible=o)})}function startMasterClockLoop(){timerInterval&&clearInterval(timerInterval),timerInterval=setInterval(()=>{isTeacherMode&&gamePhase==="explore"&&remainingSeconds>0&&remainingSeconds%5===0&&publishTeacherCommand({action:"SYNC_TIME",phase:"explore",remainingSeconds}),gamePhase==="explore"&&remainingSeconds>0&&(remainingSeconds--,updateTimerDisplayUI(),remainingSeconds<=0&&(remainingSeconds=0,playSoundEffect("whistle_dock"),applyPhaseChange("walk_to_dock")))},1e3)}function updateTimerDisplayUI(){const e=String(Math.floor(remainingSeconds/60)).padStart(2,"0"),t=String(remainingSeconds%60).padStart(2,"0"),n=`${e}:${t}`,o=document.getElementById("hud-timer"),a=document.getElementById("teacher-live-timer");o&&(o.textContent=gamePhase==="race"||gamePhase==="reflection"?myPlayer.finishedRace?"🏝️ PULAU":"LOMBA!":n),a&&(a.textContent=n)}function removeMyAvatarFromScene(){myAvatarMesh&&scene&&(scene.remove(myAvatarMesh),myAvatarMesh=null),myBoatMesh&&scene&&(scene.remove(myBoatMesh),myBoatMesh=null)}function clearAllOtherPlayersFromScene(){Object.values(otherPlayers).forEach(e=>{e.mesh&&scene&&scene.remove(e.mesh),e.boatMesh&&scene&&scene.remove(e.boatMesh)}),otherPlayers={}}function switchToStudentModeDirectly(){playSoundEffect("click"),syncFormToConfig(),rebuildCityBuildings3D(),document.getElementById("teacher-screen").classList.add("hidden"),showStudentLoginModal()}function backToTeacherFromLogin(){playSoundEffect("click"),myPlayer.role="teacher",myPlayer.hasJoinedGame=!1,removeMyAvatarFromScene(),document.getElementById("student-login-screen").classList.add("hidden"),document.getElementById("teacher-screen").classList.remove("hidden"),refreshOnlinePlayersUI()}function enterTeacher3DMonitor(){playSoundEffect("click"),syncFormToConfig(),rebuildCityBuildings3D(),myPlayer.hasJoinedGame&&mqttClient&&mqttClient.connected&&mqttClient.publish(`aes_class_3d/${roomId}/player_leave`,JSON.stringify({id:myPlayer.id})),isTeacher3DMonitor=!0,myPlayer.role="teacher",myPlayer.hasJoinedGame=!1,removeMyAvatarFromScene(),document.getElementById("teacher-screen").classList.add("hidden"),document.getElementById("game-hud").classList.remove("hidden"),document.getElementById("teacher-clean-toggle-wrap").classList.remove("hidden"),document.getElementById("joystick-zone").classList.add("hidden"),document.getElementById("race-quiz-panel").classList.add("hidden"),document.getElementById("hud-role-badge").textContent="GURU MONITOR",document.getElementById("hud-player-name").textContent="Kamera Pantau Guru",document.getElementById("hud-top-bar").classList.add("teacher-monitor-offset"),updateHUDBuildingBadges(),startMasterClockLoop(),refreshOnlinePlayersUI()}function exitTeacher3DMonitor(){playSoundEffect("click"),myPlayer.hasJoinedGame&&mqttClient&&mqttClient.connected&&mqttClient.publish(`aes_class_3d/${roomId}/player_leave`,JSON.stringify({id:myPlayer.id})),isTeacher3DMonitor=!1,myPlayer.role="teacher",myPlayer.hasJoinedGame=!1,removeMyAvatarFromScene(),teacherFollowPlayerId=null,document.getElementById("teacher-follow-indicator").classList.add("hidden"),document.getElementById("teacher-clean-toggle-wrap").classList.add("hidden"),document.getElementById("hud-top-bar").classList.remove("teacher-monitor-offset"),_mapSel=[],refreshMapPick(),document.getElementById("game-hud").classList.add("hidden"),document.getElementById("teacher-screen").classList.remove("hidden"),refreshOnlinePlayersUI()}const SAVE_TTL_MS=12*3600*1e3;function _saveKey(e){return"aes_save:"+roomId+":"+String(e||"").trim().toLowerCase()}function loadSavedProgress(e){if(isTeacherMode||!e)return null;try{const t=localStorage.getItem(_saveKey(e));if(!t)return null;const n=JSON.parse(t);return!n||n.v!==1||Date.now()-(n.ts||0)>SAVE_TTL_MS?null:n}catch{return null}}function saveMyProgress(){if(!(isTeacherMode||myPlayer.role!=="student"||!myPlayer.hasJoinedGame||!myPlayer.name))try{const e=Object.assign({},myPlayer.buildingNotes||{},studentNotes);localStorage.setItem(_saveKey(myPlayer.name),JSON.stringify({v:1,ts:Date.now(),id:myPlayer.id,name:myPlayer.name,color:myPlayer.color,x:myPlayer.x,z:myPlayer.z,rotY:myPlayer.rotY,phase:gamePhase,remaining:remainingSeconds,completedBuildings:myPlayer.completedBuildings,coinBuildings:myPlayer.coinBuildings,buildingQuizResult:myPlayer.buildingQuizResult,buildingQuizPick:myPlayer.buildingQuizPick,buildingNotes:e,ownedItems:myPlayer.ownedItems,equip:myPlayer.equip,atDock:myPlayer.atDock,finishedRace:myPlayer.finishedRace,boatStrokes:myPlayer.boatStrokes,initialCorrect:myPlayer.initialCorrect,initialWrong:myPlayer.initialWrong,retryCorrect:myPlayer.retryCorrect,retryWrong:myPlayer.retryWrong,finalScore:myPlayer.finalScore,questionQueue,firstAttemptTracker,reflectionSubmitted:myPlayer.reflectionSubmitted,reflectionFeeling:myPlayer.reflectionFeeling,reflectionUnderstood:myPlayer.reflectionUnderstood,reflectionDifficulty:myPlayer.reflectionDifficulty,reflectionSuggestion:myPlayer.reflectionSuggestion})),localStorage.setItem("aes_last:"+roomId,myPlayer.name)}catch{}}function restoreMyProgress(e){const t=loadSavedProgress(e);if(!t)return!1;const n=l=>Array.isArray(l)?l.slice():[],o=l=>l&&typeof l=="object"&&!Array.isArray(l)?JSON.parse(JSON.stringify(l)):{},a=l=>typeof l=="number"&&isFinite(l)?l:0;t.id&&(myPlayer.id=t.id),t.color&&(myPlayer.color=t.color),myPlayer.completedBuildings=n(t.completedBuildings),myPlayer.coinBuildings=n(t.coinBuildings),myPlayer.buildingQuizResult=o(t.buildingQuizResult),myPlayer.buildingQuizPick=o(t.buildingQuizPick),myPlayer.ownedItems=n(t.ownedItems),myPlayer.equip=o(t.equip),studentNotes=o(t.buildingNotes),myPlayer.buildingNotes=Object.assign({},studentNotes),recalcCoins();const r=["waiting","explore","walk_to_dock"],s=["race","reflection"],i=isFinite(t.x)&&isFinite(t.z);if(s.includes(t.phase)&&s.includes(gamePhase)){myPlayer.boatStrokes=a(t.boatStrokes),myPlayer.initialCorrect=a(t.initialCorrect),myPlayer.initialWrong=a(t.initialWrong),myPlayer.retryCorrect=a(t.retryCorrect),myPlayer.retryWrong=a(t.retryWrong),myPlayer.finalScore=a(t.finalScore),myPlayer.finishedRace=!!t.finishedRace,myPlayer.atDock=!myPlayer.finishedRace,firstAttemptTracker=o(t.firstAttemptTracker),questionQueue=n(t.questionQueue).filter(m=>Number.isInteger(m)&&m>=0&&m<gameConfig.questions.length);const l=gameConfig.questions.length;raceInited=myPlayer.finishedRace||questionQueue.length>0||myPlayer.boatStrokes>=l,myPlayer.reflectionSubmitted=!!t.reflectionSubmitted,myPlayer.reflectionFeeling=t.reflectionFeeling||"",myPlayer.reflectionUnderstood=t.reflectionUnderstood||"",myPlayer.reflectionDifficulty=t.reflectionDifficulty||"",myPlayer.reflectionSuggestion=t.reflectionSuggestion||"",myPlayer.finishedRace&&i&&(myPlayer.x=t.x,myPlayer.z=t.z,myPlayer.rotY=a(t.rotY),cameraYaw=-Math.PI/2)}else r.includes(t.phase)&&r.includes(gamePhase)&&i&&(myPlayer.x=t.x,myPlayer.z=t.z,myPlayer.rotY=a(t.rotY),cameraYaw=myPlayer.rotY+Math.PI,gamePhase==="walk_to_dock"&&t.atDock&&(myPlayer.atDock=!0));return!0}function discardSavedProgress(){const e=document.getElementById("student-name-select"),t=document.getElementById("student-custom-name"),n=(e.value==="__CUSTOM__"?t.value:e.value).trim();if(n&&confirm("Hapus progres tersimpan atas nama "+n+" dan mulai dari awal?")){try{localStorage.removeItem(_saveKey(n))}catch{}updateResumeNotice()}}function updateResumeNotice(){const e=document.getElementById("student-resume-notice");if(!e)return;const t=document.getElementById("student-name-select"),n=document.getElementById("student-custom-name"),o=t?(t.value==="__CUSTOM__"?n.value:t.value).trim():"",a=o?loadSavedProgress(o):null;if(!a){e.classList.add("hidden"),e.innerHTML="";return}const r=Math.max(0,Math.round((Date.now()-(a.ts||0))/6e4)),s=r<1?"baru saja":r<60?r+" menit lalu":Math.floor(r/60)+" jam lalu",i=(a.completedBuildings||[]).length,l=(gameConfig.buildings||[]).length;e.innerHTML=`✅ Progres <b>${escQ(o)}</b> ditemukan (gedung ${i}/${l}, ${s}). Tekan <b>Masuk</b> untuk melanjutkan. <button type="button" onclick="discardSavedProgress()" class="underline text-amber-200 ml-1">Mulai dari awal</button>`,e.classList.remove("hidden")}let _loginPrefilled=!1;function showStudentLoginModal(){populateStudentSelectDropdown(),aesUpdateWaitNote(),document.getElementById("student-login-screen").classList.remove("hidden")}function populateStudentSelectDropdown(){const e=document.getElementById("student-name-select");if(!e)return;const t=e.value,n=e.options.length>0,o=document.getElementById("student-custom-name");e.innerHTML="",(gameConfig.students||[]).forEach(s=>{const i=document.createElement("option");i.value=s,i.textContent=s,e.appendChild(i)});const a=document.createElement("option");a.value="__CUSTOM__",a.textContent="✏️ Ketik Nama Sendiri...",e.appendChild(a);const r=s=>[...e.options].find(i=>i.value!=="__CUSTOM__"&&i.value.toLowerCase()===String(s||"").trim().toLowerCase());if(n)if(t==="__CUSTOM__"){const s=r(o&&o.value);e.value=s?s.value:"__CUSTOM__"}else[...e.options].some(s=>s.value===t)&&(e.value=t);else if(!isTeacherMode&&!_loginPrefilled){_loginPrefilled=!0;let s="";try{s=localStorage.getItem("aes_last:"+roomId)||""}catch{}if(s){const i=r(s);i?e.value=i.value:(e.value="__CUSTOM__",o&&(o.value=s))}}toggleCustomStudentNameInput(!0)}function toggleCustomStudentNameInput(e){const t=document.getElementById("student-name-select"),n=document.getElementById("student-custom-name");t.value==="__CUSTOM__"?(n.classList.remove("hidden"),e!==!0&&n.focus()):n.classList.add("hidden"),updateResumeNotice()}function selectAvatarColor(e,t){playSoundEffect("click"),myPlayer.color=e,document.querySelectorAll("#avatar-color-picker button").forEach(n=>{n.classList.remove("ring-4","ring-white"),n.classList.add("opacity-75")}),t.classList.add("ring-4","ring-white"),t.classList.remove("opacity-75")}function startStudentGame(){if(window._aesRevoked){aesRoomRevoked();return}initAudioEngine(),playSoundEffect("complete_building");const e=document.getElementById("student-name-select").value,t=document.getElementById("student-custom-name").value.trim(),n=(e==="__CUSTOM__"?t:e).trim();if(!n){alert("Pilih atau ketik namamu terlebih dahulu!");return}isTeacher3DMonitor=!1,myPlayer.name=n,myPlayer.role="student",myPlayer.hasJoinedGame=!0;{const a=(Math.random()-.5)*2,r=6.2+Math.random()*1.3;myPlayer.x=Math.sin(a)*r,myPlayer.z=52+Math.cos(a)*r}if(myPlayer.rotY=Math.PI,cameraYaw=0,cameraDistance=6.5,cameraPitch=.22,myPlayer.rideDriverId=null,myPlayer.inCar=!1,myPlayer.insideBuilding=null,myPlayer.atDock=!1,myPlayer.finishedRace=!1,!isTeacherMode&&!_teacherCmdSeen&&gamePhase==="waiting"){const a=loadSavedProgress(n);a&&a.phase&&a.phase!=="waiting"&&(gamePhase=a.phase,a.phase==="explore"&&typeof a.remaining=="number"?(remainingSeconds=Math.max(0,Math.round(a.remaining-Math.max(0,(Date.now()-(a.ts||Date.now()))/1e3))),remainingSeconds<=0&&(gamePhase="walk_to_dock")):a.phase!=="explore"&&(remainingSeconds=0),updateTimerDisplayUI())}const o=restoreMyProgress(n);document.getElementById("student-login-screen").classList.add("hidden"),document.getElementById("teacher-clean-toggle-wrap").classList.add("hidden"),document.getElementById("hud-top-bar").classList.remove("teacher-monitor-offset"),document.getElementById("game-hud").classList.remove("hidden"),document.getElementById("joystick-zone").classList.remove("hidden"),document.getElementById("hud-role-badge").textContent="AES CLASS",document.getElementById("hud-player-name").textContent=myPlayer.name,isTeacherMode&&gamePhase==="reflection"&&(gamePhase="waiting",myPlayer.reflectionSubmitted=!1),createOrUpdateMyAvatar3D(),updateHUDBuildingBadges(),applyPhaseChange(gamePhase),startMasterClockLoop(),connectMultiplayerMQTT(),broadcastMyState(),refreshOnlinePlayersUI(),saveMyProgress(),o&&showCoinToast("▶️ Progresmu dilanjutkan, "+n+"!")}function connectMultiplayerMQTT(){if(typeof mqtt>"u"){aesLoadMqttLib(connectMultiplayerMQTT);return}if(mqttClient)return;const e=mqttClient=mqtt.connect(aesBrokerUrl(),{clientId:"aes_"+myPlayer.id+"_"+Math.floor(Math.random()*9999),clean:!0,connectTimeout:4e3,reconnectPeriod:2e3}),t=`aes_class_3d/${roomId}/player_state`,n=`aes_class_3d/${roomId}/player_leave`,o=`aes_class_3d/${roomId}/teacher_cmd`,a=`aes_class_3d/${roomId}/ping_all`,r=`aes_class_3d/${roomId}/config_sync`,s=`aes_class_3d/${roomId}/player_pos`,i=`aes_class_3d/${roomId}/announce`,AESREV=`aes_class_3d/${roomId}/revoked`;let l=0,m=!1;const d=()=>{const p=Date.now(),u=2e4;p-l>=u?(l=p,mqttClient.publish(r,aesCfgPayload(),{retain:!0,qos:1})):m||(m=!0,setTimeout(()=>{m=!1,l=Date.now(),mqttClient&&mqttClient.publish(r,aesCfgPayload(),{retain:!0,qos:1})},u-(p-l)))};aesPubCfgNow=()=>{isTeacherMode&&mqttClient===e&&e.connected&&(l=Date.now(),e.publish(r,aesCfgPayload(),{retain:!0,qos:1}))};let w=!1;aesConnWarn(!0,7e3),isTeacherMode&&aesUpdateConnChip(!1),isTeacherMode&&!aesHasCustomBroker()&&setTimeout(()=>{!w&&mqttClient===e&&!_aesLinkShared&&aesSwitchBroker((AES_BROKER_IDX+1)%AES_BROKERS.length,!0)},7e3),e.on("offline",()=>{mqttClient===e&&(aesConnWarn(!0,3e3),isTeacherMode&&aesUpdateConnChip(!1))}),e.on("close",()=>{mqttClient===e&&(aesConnWarn(!0,3e3),isTeacherMode&&aesUpdateConnChip(!1))}),e.on("connect",()=>{if(mqttClient===e){if(w=!0,isTeacherMode){aesUpdateConnChip(!0);try{localStorage.setItem("aes_bk",String(AES_BROKER_IDX))}catch{}}aesConnWarn(!1),mqttClient.subscribe([t,n,o,a,r,s,i,AESREV]),broadcastMyState(),mqttClient.publish(a,JSON.stringify({requester:myPlayer.id})),isTeacherMode&&(l=Date.now(),mqttClient.publish(r,aesCfgPayload(),{retain:!0,qos:1}))}}),e.on("message",(p,u)=>{if(mqttClient===e)try{const H=u.toString(),M=JSON.parse(H);if(p===AESREV){isTeacherMode||aesRoomRevoked(M);return}if(p===s)M.id!==myPlayer.id&&handleIncomingPlayerPos(M);else if(p===t&&M.id!==myPlayer.id)handleIncomingPlayerState(M);else if(p===n&&M&&M.id)markOtherPlayerOffline(M.id);else if(p===o)handleIncomingTeacherCommand(M);else if(p===i)isTeacherMode||playTeacherAnnouncement(M);else if(p===a&&M.requester!==myPlayer.id)Date.now()-lastFullStateSent>3e3&&broadcastMyState(),isTeacherMode&&d();else if(p===r&&!isTeacherMode&&M&&M.buildings){if(AES_LITE&&H===_aesLastCfgRaw)return;_aesLastCfgRaw=H,gameConfig=M,_aesCfgGot=!0,populateStudentSelectDropdown(),aesUpdateWaitNote(),rebuildCityBuildings3D(),updateHUDBuildingBadges()}}catch{}}),mqttBroadcastLoop&&clearInterval(mqttBroadcastLoop),mqttBroadcastLoop=setInterval(()=>{broadcastMyPos(),Date.now()-lastFullStateSent>aesStateEvery()&&broadcastMyState(),cleanupDisconnectedGhostPlayers()},100)}let lastFullStateSent=0,lastPosKey="",lastPosSent=0;function broadcastMyPos(){if(!mqttClient||!mqttClient.connected||myPlayer.role!=="student"||!myPlayer.hasJoinedGame||!myPlayer.name)return;const e=Number(myPlayer.x.toFixed(2)),t=Number(myPlayer.z.toFixed(2)),n=Number(myPlayer.rotY.toFixed(2)),o=e+"|"+t+"|"+n+"|"+(myPlayer.inCar||"")+"|"+(myPlayer.rideDriverId||""),a=Date.now(),r=aesPosMinMove();r&&a-lastPosSent<r||o===lastPosKey&&a-lastPosSent<aesPosIdle()||(lastPosKey=o,lastPosSent=a,mqttClient.publish(`aes_class_3d/${roomId}/player_pos`,JSON.stringify({id:myPlayer.id,x:e,z:t,r:n,c:myPlayer.inCar||0,d:myPlayer.rideDriverId||0})))}function trackOtherMotion(e,t,n){const o=performance.now();if(e._lt!==void 0){const a=(o-e._lt)/1e3;if(a>.03&&a<1.2){let r=(t-e.targetX)/a,s=(n-e.targetZ)/a;const i=Math.hypot(r,s);i>45&&(r*=45/i,s*=45/i),e.vx=(e.vx||0)*.4+r*.6,e.vz=(e.vz||0)*.4+s*.6}else a>=1.2&&(e.vx=0,e.vz=0);Math.hypot(t-e.targetX,n-e.targetZ)>25&&e.mesh&&(e.mesh.position.x=t,e.mesh.position.z=n,e.vx=0,e.vz=0)}e.targetX=t,e.targetZ=n,e._lt=o}function handleIncomingPlayerPos(e){const t=otherPlayers[e.id];!t||t.offline||(t.lastSeenLocal=Date.now(),trackOtherMotion(t,e.x,e.z),t.rotY=e.r,t.inCar=e.c||!1,t.rideDriverId=e.d||null)}function broadcastMyState(){saveMyProgress(),!(!mqttClient||!mqttClient.connected)&&(myPlayer.role!=="student"||!myPlayer.hasJoinedGame||!myPlayer.name||(lastFullStateSent=Date.now(),mqttClient.publish(`aes_class_3d/${roomId}/player_state`,JSON.stringify({id:myPlayer.id,name:myPlayer.name,role:"student",hasJoinedGame:!0,color:myPlayer.color,x:Number(myPlayer.x.toFixed(2)),z:Number(myPlayer.z.toFixed(2)),rotY:Number(myPlayer.rotY.toFixed(2)),currentBuilding:myPlayer.currentBuilding,completedCount:myPlayer.completedBuildings.length,atDock:myPlayer.atDock,boatStrokes:myPlayer.boatStrokes,initialCorrect:myPlayer.initialCorrect,initialWrong:myPlayer.initialWrong,retryCorrect:myPlayer.retryCorrect,retryWrong:myPlayer.retryWrong,finishedRace:myPlayer.finishedRace,finalScore:myPlayer.finalScore,lastRowTime:myPlayer.lastRowTime,reflectionSubmitted:myPlayer.reflectionSubmitted,reflectionFeeling:myPlayer.reflectionFeeling,reflectionUnderstood:myPlayer.reflectionUnderstood,reflectionDifficulty:myPlayer.reflectionDifficulty,reflectionSuggestion:myPlayer.reflectionSuggestion,buildingNotes:myPlayer.buildingNotes||studentNotes,coins:myPlayer.coins||0,buildingQuizResult:myPlayer.buildingQuizResult||{},equip:myPlayer.equip||{},inCar:myPlayer.inCar||!1,rideDriverId:myPlayer.rideDriverId||null,insideBuilding:myPlayer.insideBuilding||null,phase:gamePhase,ts:Date.now()})),refreshOnlinePlayersUI()))}function removeOtherPlayerById(e){const t=otherPlayers[e];t&&(t.mesh&&scene&&scene.remove(t.mesh),t.boatMesh&&scene&&scene.remove(t.boatMesh),delete otherPlayers[e],refreshOnlinePlayersUI())}function markOtherPlayerOffline(e){const t=otherPlayers[e];!t||t.offline||(t.mesh&&scene&&scene.remove(t.mesh),t.boatMesh&&scene&&scene.remove(t.boatMesh),t.mesh=null,t.boatMesh=null,t.offline=!0,t.lastLabelStr="",t.inCar=!1,t.rideDriverId=null,t.insideBuilding=null,refreshOnlinePlayersUI())}function cleanupDisconnectedGhostPlayers(){const e=Date.now();let t=!1;Object.keys(otherPlayers).forEach(n=>{!otherPlayers[n].offline&&e-(otherPlayers[n].lastSeenLocal||0)>25e3&&(markOtherPlayerOffline(n),t=!0)}),t&&refreshOnlinePlayersUI()}function updatePlayerOverheadLabelIfChanged(e){const t=gamePhase==="race"||e.atDock||e.finishedRace?`🤖 ${e.name} [✓${e.initialCorrect||0} ✗${e.initialWrong||0}]`:`🤖 ${e.name}`;e.lastLabelStr!==t&&(e.lastLabelStr=t,e.mesh&&e.mesh.userData&&e.mesh.userData.nameSprite&&updateSpriteCanvasText(e.mesh.userData.nameSprite,t,e.color||"#0ea5e9"),e.boatMesh&&e.boatMesh.userData&&e.boatMesh.userData.pilotRobot&&e.boatMesh.userData.pilotRobot.userData.nameSprite&&updateSpriteCanvasText(e.boatMesh.userData.pilotRobot.userData.nameSprite,t,e.color||"#0ea5e9"))}function handleIncomingPlayerState(e){if(!e||e.role!=="student"||!e.hasJoinedGame||!e.name)return;if(Object.keys(otherPlayers).forEach(n=>{n!==e.id&&otherPlayers[n].name===e.name&&removeOtherPlayerById(n)}),!otherPlayers[e.id])otherPlayers[e.id]={...e,targetX:e.x,targetZ:e.z,vx:0,vz:0,_lt:performance.now(),lastSeenLocal:Date.now(),mesh:null,boatMesh:null,lastLabelStr:""},scene&&(otherPlayers[e.id].mesh=createRobotCharacterMesh(e.name,e.color),otherPlayers[e.id].mesh.position.set(e.x||0,0,e.z||0),scene.add(otherPlayers[e.id].mesh),otherPlayers[e.id].boatMesh=createSpeedboatMesh(e.name,e.color),otherPlayers[e.id].boatMesh.position.set(BOAT_START_POS.x,.2,BOAT_START_POS.z),scene.add(otherPlayers[e.id].boatMesh));else{const n=otherPlayers[e.id];Object.assign(n,{name:e.name,rotY:e.rotY,currentBuilding:e.currentBuilding,completedCount:e.completedCount,atDock:e.atDock,boatStrokes:e.boatStrokes,initialCorrect:e.initialCorrect||0,initialWrong:e.initialWrong||0,retryCorrect:e.retryCorrect||0,retryWrong:e.retryWrong||0,finishedRace:e.finishedRace||!1,finalScore:e.finalScore||0,lastRowTime:e.lastRowTime||0,reflectionSubmitted:e.reflectionSubmitted||!1,reflectionFeeling:e.reflectionFeeling||"",reflectionUnderstood:e.reflectionUnderstood||"",reflectionDifficulty:e.reflectionDifficulty||"",reflectionSuggestion:e.reflectionSuggestion||"",buildingNotes:e.buildingNotes||{},buildingQuizResult:e.buildingQuizResult||{},coins:e.coins||0,equip:e.equip||{},inCar:e.inCar||!1,rideDriverId:e.rideDriverId||null,insideBuilding:e.insideBuilding||null,lastSeenLocal:Date.now()}),n.offline||!n.mesh&&scene?(n.offline=!1,n.color=e.color||n.color,n.targetX=e.x,n.targetZ=e.z,n.vx=0,n.vz=0,n._lt=performance.now(),n.lastLabelStr="",scene&&(n.mesh=createRobotCharacterMesh(n.name,n.color),n.mesh.position.set(e.x||0,0,e.z||0),scene.add(n.mesh),n.boatMesh=createSpeedboatMesh(n.name,n.color),n.boatMesh.position.set(BOAT_START_POS.x,.2,BOAT_START_POS.z),scene.add(n.boatMesh))):(!n._lt||performance.now()-n._lt>300)&&trackOtherMotion(n,e.x,e.z)}const t=otherPlayers[e.id];if(t){updatePlayerOverheadLabelIfChanged(t);const n=(gamePhase==="race"||t.atDock)&&!t.finishedRace;t.mesh&&(t.mesh.visible=!n&&!t.insideBuilding),t.boatMesh&&(t.boatMesh.visible=n)}refreshOnlinePlayersUI()}function handleIncomingTeacherCommand(e){if(!isTeacherMode){if(_teacherCmdSeen=!0,typeof e.remainingSeconds=="number"){let t=e.remainingSeconds;if(e.phase==="explore"&&typeof e.sentAt=="number"){const n=(Date.now()-e.sentAt)/1e3;n>0&&n<6*3600&&(t=Math.max(0,Math.round(t-n)))}remainingSeconds=t,updateTimerDisplayUI(),e.phase==="explore"&&t<=0&&gamePhase==="explore"&&(playSoundEffect("whistle_dock"),applyPhaseChange("walk_to_dock"))}(e.action==="SET_PHASE"&&e.phase||e.action==="SYNC_TIME"&&e.phase&&e.phase!==gamePhase)&&applyPhaseChange(e.phase)}}function getAllStudentsListForReport(){const e=[];return myPlayer.role==="student"&&myPlayer.hasJoinedGame&&myPlayer.name&&e.push({...myPlayer,isMe:!0,completedCount:myPlayer.completedBuildings.length}),Object.values(otherPlayers).forEach(t=>{t.role==="student"&&t.hasJoinedGame&&t.name&&e.push(t)}),e}function openTeacherNotesModal(e){playSoundEffect("click");const n=getAllStudentsListForReport().find(r=>r.id===e);if(!n)return;document.getElementById("teacher-notes-modal-title").textContent=`📖 Catatan Belajar Gedung: ${n.name}`;const o=n.buildingNotes||{},a=document.getElementById("teacher-notes-modal-body");a.innerHTML=gameConfig.buildings.map((r,s)=>{const i=(o[r.id]||"").trim(),l=i.length>=15;return`\n          <div class="p-3.5 rounded-2xl bg-slate-950 border ${l?"border-emerald-500/40":"border-slate-800"} space-y-1.5">\n            <div class="flex items-center justify-between gap-2">\n              <span class="text-xs font-extrabold text-sky-300">[G${s+1}] ${r.name}</span>\n              <span class="px-2 py-0.5 rounded text-[10px] font-extrabold ${l?"bg-emerald-500/20 text-emerald-300 border border-emerald-500/30":"bg-rose-500/20 text-rose-300"}">${l?"✓ Sudah Mencatat":"Belum Mencatat"}</span>\n            </div>\n            <p class="text-xs ${i?"text-slate-100":"text-slate-500 italic"} whitespace-pre-line wrap-anywhere">${i?formatRichEducationalText(i):"Siswa belum menuliskan catatan di gedung ini."}</p>\n          </div>\n        `}).join(""),document.getElementById("teacher-notes-modal").classList.remove("hidden")}function closeTeacherNotesModal(){document.getElementById("teacher-notes-modal").classList.add("hidden")}let _refreshTimer=null,_lastRefresh=0;function setHtmlIfChanged(e,t){const n=typeof e=="string"?document.getElementById(e):e;!n||n._lastHtml===t||(n._lastHtml=t,n.innerHTML=t)}function refreshOnlinePlayersUI(){const e=Date.now();if(e-_lastRefresh>=700){_lastRefresh=e,refreshOnlinePlayersUINow();return}_refreshTimer||(_refreshTimer=setTimeout(()=>{_refreshTimer=null,_lastRefresh=Date.now(),refreshOnlinePlayersUINow()},700-(e-_lastRefresh)))}function refreshOnlinePlayersUINow(){const e=getAllStudentsListForReport(),t=gameConfig.questions.length;{const a=e.filter(r=>r.offline).length;document.getElementById("hud-online-count").textContent=`${e.length-a} Siswa`+(a?` (+${a} keluar)`:"")}const n=e.map(a=>{const r=Object.values(a.buildingNotes||{}).filter(s=>String(s||"").trim().length>=15).length;return`\n        <div class="p-2 rounded-xl bg-slate-900/90 border border-white/15 flex items-center justify-between gap-2">\n          <div class="truncate">\n            <span class="font-extrabold text-white text-xs">${a.name}${a.isMe?" (Kamu)":""}</span>\n            <div class="flex items-center gap-2 text-[11px] mt-0.5">\n              <span class="text-emerald-400 font-extrabold">✓${a.initialCorrect||0}</span>\n              <span class="text-rose-400 font-extrabold">✗${a.initialWrong||0}</span>\n              <span class="text-amber-300 font-bold">(${a.finalScore||0} Poin)</span>\n              <span class="text-yellow-300 font-extrabold">🪙${a.coins||0}</span>\n              ${a.reflectionSubmitted?'<span class="px-1.5 bg-purple-500 text-white rounded text-[9px] font-bold">📝✓</span>':""}\n            </div>\n            <div class="text-[10px] text-sky-200 truncate mt-0.5">📍 ${a.offline?"⚫ Keluar • ":""}${a.finishedRace?"🏝️ Pulau Victory":a.atDock?"🚤 Mendayung":a.currentBuilding||"Kota"}</div>\n          </div>\n          <div class="text-right shrink-0 flex items-center gap-1.5">\n            <div>\n              <span class="text-[10px] font-bold text-emerald-300">🏢 ${a.completedCount||0}/${gameConfig.buildings.length} (📝${r})</span>\n              <span class="text-[10px] font-bold text-sky-300 block">🚤 ${a.boatStrokes||0}/${t}</span>\n            </div>\n            ${isTeacherMode?`<button onclick="openTeacherNotesModal('${a.id}')" class="px-2 py-1 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold rounded-lg text-[10px]" title="Lihat Catatan Gedung">📖</button>`:""}\n            ${!a.isMe&&isTeacher3DMonitor?`<button onclick="focusCameraOnStudent('${a.id}')" class="px-2 py-1 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold rounded-lg text-[10px]" title="Pantau Siswa">👁️</button>`:""}\n          </div>\n        </div>\n      `}).join("");setHtmlIfChanged("hud-online-list",isTeacherMode?n:"");const o=document.getElementById("teacher-student-table-body");if(o)if(e.length===0)o.innerHTML='<tr><td colspan="9" class="py-4 text-center text-slate-500 italic">Menunggu siswa memilih nama dan masuk ke arena...</td></tr>';else{const a=e.map(r=>{const s=Object.values(r.buildingNotes||{}).filter(i=>String(i||"").trim().length>=15).length;return`\n            <tr class="hover:bg-slate-900/60">\n              <td class="py-3 px-3 font-bold text-white">${r.name}</td>\n              <td class="py-3 px-3">${r.offline?'<span class="px-1.5 py-0.5 bg-slate-700 text-slate-300 rounded text-[10px] font-bold mr-1">⚫ KELUAR</span>':""}${r.finishedRace?'<span class="px-2 py-0.5 bg-emerald-400 text-slate-950 rounded text-xs font-extrabold">🏝️ DI PULAU</span>':r.atDock?"🚤 Mendayung":"🤖 "+(r.currentBuilding||"Kota")}</td>\n              <td class="py-3 px-3">\n                <div class="flex items-center gap-2">\n                  <span class="text-sky-300 font-bold">${r.completedCount||0}/${gameConfig.buildings.length}</span>\n                  <span class="text-yellow-300 font-extrabold text-xs">🪙${r.coins||0}</span>\n                  <button onclick="openTeacherNotesModal('${r.id}')" class="px-2 py-1 bg-sky-500/20 hover:bg-sky-500/40 text-sky-200 border border-sky-400/40 rounded-lg text-[11px] font-extrabold transition">📖 Lihat Catatan (${s})</button>\n                </div>\n              </td>\n              <td class="py-3 px-3 font-bold text-white">${r.boatStrokes||0}/${t}</td>\n              <td class="py-3 px-3"><span class="text-emerald-400 font-bold">✓ ${r.initialCorrect||0} Benar</span> | <span class="text-rose-400 font-bold">✗ ${r.initialWrong||0} Salah</span></td>\n              <td class="py-3 px-3"><span class="text-amber-300 font-bold">↻ ${r.retryCorrect||0}</span> | <span class="text-rose-400 font-bold">✗ ${r.retryWrong||0}</span></td>\n              <td class="py-3 px-3 text-center"><span class="px-2.5 py-1 rounded-lg font-extrabold text-xs bg-slate-800 text-amber-300">${r.finalScore||0} Poin</span></td>\n              <td class="py-3 px-3">\n                ${r.reflectionSubmitted?`<div class="text-xs leading-snug"><span class="px-1.5 py-0.5 bg-purple-500/30 text-purple-200 border border-purple-400/40 rounded font-bold">${r.reflectionFeeling}</span><div class="text-slate-300 mt-0.5 truncate max-w-[180px]" title="Paham: ${r.reflectionUnderstood} | Sulit: ${r.reflectionDifficulty}">Paham: ${r.reflectionUnderstood}</div></div>`:'<span class="text-slate-500 italic text-xs">Belum Mengisi</span>'}\n              </td>\n              <td class="py-3 px-3 text-right">${r.isMe?"-":`<button onclick="focusCameraOnStudent('${r.id}')" class="px-2.5 py-1 bg-sky-400 text-slate-950 font-extrabold rounded-lg text-xs">👁️ Ikuti</button>`}</td>\n            </tr>\n          `}).join("");setHtmlIfChanged(o,a)}}function renderCurrentRaceQuestion(){const e=gameConfig.questions.length;document.getElementById("quiz-target-strokes").textContent=e,document.getElementById("quiz-my-strokes").textContent=myPlayer.boatStrokes;const t=document.getElementById("quiz-live-correct"),n=document.getElementById("quiz-live-wrong");if(t&&(t.textContent=`✓${myPlayer.initialCorrect}`),n&&(n.textContent=`✗${myPlayer.initialWrong}`),myPlayer.boatStrokes>=e&&questionQueue.length===0){disembarkOnVictoryIsland();return}const o=questionQueue[0],a=firstAttemptTracker[o]===!0,r=gameConfig.questions[o],s=document.getElementById("quiz-mode-badge");s.textContent=a?"↻ SOAL PENGULANGAN (WAJIB BENAR AGAR SAMPAI FINISH)":"🚤 PUTARAN UTAMA (BERPOIN NILAI)",s.className=a?"px-2 py-0.5 bg-rose-500 text-white font-extrabold text-[9px] rounded-md":"px-2 py-0.5 bg-amber-400 text-slate-950 font-extrabold text-[9px] rounded-md",document.getElementById("quiz-question-counter").textContent=`Soal ke-${Math.min(myPlayer.boatStrokes+1,e)} dari ${e}`;const i=document.getElementById("quiz-question-text");i.innerHTML=formatRichEducationalText(r.q,1);const l=document.getElementById("quiz-options-grid");l.innerHTML="",getShuffledOrder(r.options).forEach((m,d)=>{const w=r.options[m],p=document.createElement("button");p.className="w-full text-left px-2.5 py-1.5 rounded-xl bg-slate-900/85 hover:bg-sky-500/35 border border-white/20 text-[11px] font-bold text-white transition flex items-start gap-2",p.innerHTML=`<span class="w-5 h-5 rounded bg-sky-400/20 text-sky-200 flex items-center justify-center font-extrabold text-[10px] shrink-0">${String.fromCharCode(65+d)}</span><span class="flex-1 wrap-anywhere leading-tight">${formatRichEducationalText(w,1)}</span>`,p.onclick=()=>submitQuizAnswer(m,r.correct,o),l.appendChild(p)}),triggerMathJaxRender([i,l])}function submitQuizAnswer(e,t,n){if(isPenaltyLocked)return;const o=gameConfig.questions.length,a=!firstAttemptTracker[n];if(firstAttemptTracker[n]=!0,e===t)playSoundEffect("correct_row"),questionQueue.shift(),a?myPlayer.initialCorrect++:myPlayer.retryCorrect++,myPlayer.boatStrokes++,myPlayer.lastRowTime=Date.now(),myPlayer.finalScore=Math.round(myPlayer.initialCorrect/o*100),broadcastMyState(),renderCurrentRaceQuestion();else{playSoundEffect("wrong_answer"),questionQueue.push(questionQueue.shift()),a?myPlayer.initialWrong++:myPlayer.retryWrong++,myPlayer.finalScore=Math.round(myPlayer.initialCorrect/o*100),broadcastMyState();const r=document.getElementById("quiz-live-correct"),s=document.getElementById("quiz-live-wrong");r&&(r.textContent=`✓${myPlayer.initialCorrect}`),s&&(s.textContent=`✗${myPlayer.initialWrong}`),isPenaltyLocked=!0;const i=document.getElementById("wrong-penalty-overlay"),l=document.getElementById("penalty-countdown");i.classList.remove("hidden");let m=2;l.textContent=m.toFixed(1);const d=setInterval(()=>{m-=.1,m<=0?(clearInterval(d),i.classList.add("hidden"),isPenaltyLocked=!1,renderCurrentRaceQuestion()):l.textContent=m.toFixed(1)},100)}}function disembarkOnVictoryIsland(){playSoundEffect("finish_island");const e=gameConfig.questions.length;myPlayer.finishedRace=!0,myPlayer.finalScore=Math.round(myPlayer.initialCorrect/e*100),myPlayer.currentBuilding="🏝️ Pantai Pulau Victory",myPlayer.x=VICTORY_ISLAND.centerX-18+(Math.random()-.5)*6,myPlayer.z=VICTORY_ISLAND.centerZ+(Math.random()-.5)*8,myPlayer.rotY=Math.PI/2,cameraYaw=-Math.PI/2,myAvatarMesh&&(myAvatarMesh.visible=!0,myAvatarMesh.position.set(myPlayer.x,islandGroundY(myPlayer.x,myPlayer.z)+.05,myPlayer.z)),myBoatMesh&&(myBoatMesh.visible=!1);try{syncBeachedBoats()}catch{}document.getElementById("race-quiz-panel").classList.add("hidden"),document.getElementById("joystick-zone").classList.remove("hidden"),document.getElementById("island-explore-banner").classList.remove("hidden"),updateTimerDisplayUI(),broadcastMyState(),showRaceLeaderboard()}function showRaceLeaderboard(){const e=gameConfig.questions.length;document.getElementById("my-finish-summary").innerHTML=`\n        <div class="flex items-center justify-between border-b border-slate-800 pb-2">\n          <span class="text-slate-300 font-semibold">Nilai Akhir Murni (Putaran 1):</span>\n          <span class="text-xl font-extrabold text-emerald-400">${myPlayer.finalScore} / 100</span>\n        </div>\n        <div class="pt-1 text-slate-300">Putaran 1: <b class="text-emerald-400">✓ ${myPlayer.initialCorrect} Benar</b> | <b class="text-rose-400">✗ ${myPlayer.initialWrong} Salah</b> (dari ${e} Soal)</div>\n      `;const t=getAllStudentsListForReport().sort((n,o)=>o.finalScore-n.finalScore||o.boatStrokes-n.boatStrokes);document.getElementById("leaderboard-list").innerHTML=t.map((n,o)=>`\n        <div class="flex items-center justify-between p-2.5 rounded-xl bg-slate-900 border border-slate-800 text-xs">\n          <span class="font-bold text-white">#${o+1} ${n.name}${n.isMe?" (Kamu)":""} <span class="text-[10px] text-slate-400 ml-1">(✓${n.initialCorrect||0} ✗${n.initialWrong||0})</span></span>\n          <span class="font-extrabold text-emerald-400">${n.finalScore||0} Poin</span>\n        </div>\n      `).join(""),document.getElementById("winner-modal").classList.remove("hidden")}function getNextRecommendedBuildingIndex(){for(let e=0;e<gameConfig.buildings.length;e++)if(!myPlayer.completedBuildings.includes(gameConfig.buildings[e].id))return e;return-1}function updateHUDBuildingBadges(){const e=gameConfig.buildings.length,t=myPlayer.completedBuildings.length;document.getElementById("hud-building-progress").textContent=`${t} / ${e}`;const n=document.getElementById("hud-coins");n&&(n.textContent=myPlayer.coins||0),updateShopHud();const o=getNextRecommendedBuildingIndex();document.getElementById("hud-building-badges").innerHTML=gameConfig.buildings.map((r,s)=>{const i=myPlayer.completedBuildings.includes(r.id);return`<span class="px-2 py-0.5 rounded text-[10px] font-extrabold ${i?"bg-emerald-400 text-slate-950":s===o?"bg-amber-400 text-slate-950 ring-2 ring-white animate-pulse":"bg-slate-800 text-slate-300"}">G${s+1}${i?" ✓":""}</span>`}).join("");const a=document.getElementById("hud-next-target-hint");a&&(a.textContent=o===-1?"✅ Semua Gedung Selesai! Toko, mobil & bus terbuka 🛍️":`🎯 Urutan Berikutnya: G${o+1} (${gameConfig.buildings[o].type})`)}function updateNoteCharStatusUI(e){const t=document.getElementById("student-note-char-status");if(!t)return;const n=String(e||"").trim().length;n>=15?(t.textContent=`✓ Catatan siap disimpan (${n} karakter)`,t.className="text-[11px] font-extrabold text-emerald-400"):(t.textContent=`Wajib diisi minimal 15 karakter (${n}/15)`,t.className="text-[11px] font-extrabold text-amber-400")}function openCurrentBuildingModal(){if(!activeNearBuilding||gamePhase!=="explore")return;playSoundEffect("open_building"),myPlayer.rideDriverId&&leaveBus(),myPlayer.inCar&&setCarState(!1),myPlayer.insideBuilding=activeNearBuilding.id,myAvatarMesh&&(myAvatarMesh.visible=!1);const e=gameConfig.buildings.findIndex(a=>a.id===activeNearBuilding.id);document.getElementById("modal-building-type").textContent=`GEDUNG G${e+1} • ${activeNearBuilding.type}`,document.getElementById("modal-building-title").textContent=`[G${e+1}] ${activeNearBuilding.name}`;const t=document.getElementById("modal-building-content");t.innerHTML=formatRichEducationalText(activeNearBuilding.content,1),triggerMathJaxRender([t]);const n=document.getElementById("student-personal-note"),o=studentNotes[activeNearBuilding.id]||"";n.value=o,updateNoteCharStatusUI(o),n.oninput=()=>{studentNotes[activeNearBuilding.id]=n.value,myPlayer.buildingNotes={...studentNotes},updateNoteCharStatusUI(n.value),broadcastMyState()},renderBuildingQuiz(activeNearBuilding),updateFinishButtonLabel(activeNearBuilding),document.getElementById("building-material-modal").classList.remove("hidden"),updateDoorBoards(),broadcastMyState()}/* ===== HALTE BUS KOTA (AES CLASS) ===== */
const AES_HALTE={bay:{x:15,z:51},near:{x:12,z:51,r:11},streetZ:36,avenues:[-168,-84,0,84,168],speed:30};
let aesHalteBus=null,aesHalteBuilt=false,aesHalteUiReady=false;
window.__aesShuttle=null;

/* rute bus: bay halte -> jalan z=36 -> jalan/avenue kota -> depan pintu gedung */
function aesShuttlePath(bx,bz){
  const B=AES_HALTE.bay,sz=bz+30,pts=[{x:B.x,z:B.z},{x:B.x,z:AES_HALTE.streetZ}];
  if(Math.abs(sz-AES_HALTE.streetZ)<1){pts.push({x:bx,z:AES_HALTE.streetZ})}
  else{
    let xa=AES_HALTE.avenues[0],best=1e9;
    AES_HALTE.avenues.forEach(a=>{const c=Math.abs(a-B.x)+Math.abs(a-bx);if(c<best){best=c;xa=a}});
    pts.push({x:xa,z:AES_HALTE.streetZ},{x:xa,z:sz},{x:bx,z:sz});
  }
  pts.push({x:bx,z:bz+19});
  const P=[pts[0]];
  for(let k=1;k<pts.length;k++){const a=P[P.length-1],c=pts[k];if(Math.hypot(c.x-a.x,c.z-a.z)>.01)P.push(c)}
  const lens=[];let total=0;
  for(let k=0;k<P.length-1;k++){const l=Math.hypot(P[k+1].x-P[k].x,P[k+1].z-P[k].z);lens.push(l);total+=l}
  return{pts:P,lens,total};
}

function aesBuildHalte(){
  if(aesHalteBuilt||typeof scene==="undefined"||!scene)return;
  aesHalteBuilt=true;
  try{
    const g=new THREE.Group();
    const box=(w,h,d,c,x,y,z,p,o)=>{const mt=new THREE.MeshLambertMaterial({color:c});if(o){mt.transparent=true;mt.opacity=o}const m=new THREE.Mesh(new THREE.BoxGeometry(w,h,d),mt);m.position.set(x,y,z);(p||g).add(m);return m};
    const B=AES_HALTE.bay;
    box(7,.12,16,0x334155,B.x,.03,B.z);
    box(.25,.14,16,0xfacc15,B.x-3.2,.05,B.z);
    box(.25,.14,16,0xfacc15,B.x+3.2,.05,B.z);
    const sh=new THREE.Group();sh.position.set(10.4,0,51);g.add(sh);
    box(3.4,.2,9.2,0xcbd5e1,0,.1,0,sh);
    [[-1.4,-4],[-1.4,4],[1.4,-4],[1.4,4]].forEach(([x,z])=>box(.18,3.2,.18,0x475569,x,1.8,z,sh));
    box(3.6,.24,9.6,0x0ea5e9,0,3.5,0,sh);
    box(.08,2.3,8,0x7dd3fc,-1.4,1.55,0,sh,.45);
    box(.9,.14,5.6,0xf59e0b,-.55,.78,0,sh);
    box(.12,.7,5.6,0xf59e0b,-1.0,1.15,0,sh);
    [-2.2,2.2].forEach(z=>box(.7,.6,.14,0x475569,-.55,.5,z,sh));
    /* tiang & papan nama halte */
    const pole=new THREE.Mesh(new THREE.CylinderGeometry(.09,.09,4.6,8),new THREE.MeshLambertMaterial({color:0x475569}));
    pole.position.set(0,2.3,-5.6);sh.add(pole);
    box(.12,1.6,1.6,0x2563eb,0,4.6,-5.6,sh);
    box(.14,1.1,1.1,0xffffff,0,4.6,-5.6,sh);
    try{const lbl=createTextLabelSprite("🚏 HALTE BUS KOTA","#38bdf8",.85);lbl.position.set(0,5.9,0);sh.add(lbl)}catch(e){}
    /* bus kota yang menunggu */
    aesHalteBus=createRealisticVehicleMesh("bus",0x16a34a,false);
    aesHalteBus.position.set(B.x,.08,B.z);aesHalteBus.rotation.y=Math.PI;g.add(aesHalteBus);
    try{const lb=createTextLabelSprite("🚌 BUS KOTA • GRATIS","#4ade80",.75);lb.position.set(B.x,6.4,B.z);g.add(lb);aesHalteBus.userData.aesLabel=lb}catch(e){}
    scene.add(g);
    solidCircleObstacles.push({x:B.x,z:B.z-3,r:2.3},{x:B.x,z:B.z+3,r:2.3});
  }catch(err){try{console.warn("Halte gagal dibuat",err)}catch(e){}}
}

function aesHalteSetBus(v){
  if(!aesHalteBus)return;
  aesHalteBus.visible=v;
  const l=aesHalteBus.userData&&aesHalteBus.userData.aesLabel;
  if(l)l.visible=v;
}

function aesHalteEnsureUI(){
  if(aesHalteUiReady)return;aesHalteUiReady=true;
  const wrap=document.createElement("div");wrap.id="halte-board-wrap";
  wrap.style.cssText="position:fixed;left:50%;bottom:15rem;transform:translateX(-50%);z-index:30;display:none;text-align:center;pointer-events:auto";
  const btn=document.createElement("button");btn.id="halte-board-btn";btn.className="animate-pulse-glow";
  btn.style.cssText="padding:12px 22px;border-radius:16px;background:linear-gradient(90deg,#a5b4fc,#38bdf8);color:#0f172a;font-weight:800;font-size:15px;border:2px solid #fff;box-shadow:0 8px 30px rgba(0,0,0,.45);cursor:pointer";
  btn.textContent="🚏 Naik Bus Kota (Gratis)";
  btn.onclick=()=>aesOpenHalteModal();
  wrap.appendChild(btn);document.body.appendChild(wrap);

  const md=document.createElement("div");md.id="halte-modal";
  md.style.cssText="position:fixed;inset:0;z-index:60;display:none;align-items:center;justify-content:center;background:rgba(2,6,23,.7);padding:12px;pointer-events:auto";
  const card=document.createElement("div");card.className="glass";
  card.style.cssText="width:min(480px,96vw);max-height:88vh;display:flex;flex-direction:column;border-radius:20px;padding:16px;color:#fff;box-shadow:0 20px 60px rgba(0,0,0,.6)";
  card.innerHTML='<div style="font-size:18px;font-weight:800">🚏 Halte Bus Kota</div><div style="font-size:12px;color:#bae6fd;margin:2px 0 12px">Pilih gedung tujuanmu. Bus akan mengantarmu sampai di depan pintu gedung. Gratis!</div><div id="halte-list" class="custom-scroll" style="overflow-y:auto;touch-action:pan-y;display:flex;flex-direction:column;gap:8px;padding-right:4px"></div>';
  const cancel=document.createElement("button");cancel.textContent="Batal";
  cancel.style.cssText="margin-top:12px;padding:10px;border-radius:12px;background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.3);color:#fff;font-weight:800;cursor:pointer";
  cancel.onclick=()=>{playSoundEffect("click");md.style.display="none"};
  card.appendChild(cancel);md.appendChild(card);document.body.appendChild(md);
  md.addEventListener("click",ev=>{if(ev.target===md)md.style.display="none"});

  const hud=document.createElement("div");hud.id="halte-ride-hud";
  hud.style.cssText="position:fixed;left:50%;bottom:12rem;transform:translateX(-50%);z-index:30;display:none;align-items:center;gap:10px;padding:10px 14px;border-radius:9999px;background:rgba(15,23,42,.92);border:1px solid rgba(56,189,248,.6);color:#fff;font-weight:800;font-size:13px;pointer-events:auto;max-width:94vw";
  const tx=document.createElement("span");tx.id="halte-ride-text";tx.style.cssText="overflow-wrap:anywhere";
  const sk=document.createElement("button");sk.textContent="⏭️ Langsung tiba";
  sk.style.cssText="padding:6px 12px;border-radius:9999px;background:#facc15;color:#0f172a;font-weight:800;font-size:12px;border:0;cursor:pointer;white-space:nowrap";
  sk.onclick=()=>{playSoundEffect("click");aesShuttleStop(true)};
  hud.appendChild(tx);hud.appendChild(sk);document.body.appendChild(hud);
}

function aesHalteEligible(){
  return myPlayer.role==="student"&&myPlayer.hasJoinedGame&&!isTeacher3DMonitor&&gamePhase==="explore"&&!myPlayer.atDock&&!myPlayer.insideBuilding&&!myPlayer.rideDriverId&&!window.__aesShuttle&&((gameConfig&&gameConfig.buildings)||[]).length>0;
}
function aesHalteNear(){return Math.hypot(myPlayer.x-AES_HALTE.near.x,myPlayer.z-AES_HALTE.near.z)<AES_HALTE.near.r}

function aesHalteUI(){
  aesHalteEnsureUI();
  const w=document.getElementById("halte-board-wrap");if(!w)return;
  const ok=aesHalteEligible();
  w.style.display=(ok&&aesHalteNear())?"block":"none";
  if(!ok){const md=document.getElementById("halte-modal");if(md&&md.style.display!=="none")md.style.display="none"}
}

function aesOpenHalteModal(){
  if(!aesHalteEligible())return;
  if(!aesHalteNear()){showCoinToast("🚏 Dekati halte dulu");return}
  playSoundEffect("click");
  const list=document.getElementById("halte-list");list.innerHTML="";
  const nx=getNextRecommendedBuildingIndex();
  gameConfig.buildings.forEach((b,i)=>{
    const done=myPlayer.completedBuildings.includes(b.id),rec=i===nx;
    const it=document.createElement("button");
    it.style.cssText="display:flex;align-items:center;gap:10px;text-align:left;padding:10px 12px;border-radius:14px;cursor:pointer;color:#fff;background:"+(rec?"rgba(250,204,21,.18)":"rgba(255,255,255,.07)")+";border:1px solid "+(rec?"#facc15":"rgba(255,255,255,.25)");
    const tag=document.createElement("span");tag.textContent="G"+(i+1);
    tag.style.cssText="min-width:38px;text-align:center;padding:6px 0;border-radius:10px;font-weight:800;font-size:13px;background:"+(done?"#34d399":rec?"#facc15":"#334155")+";color:"+((done||rec)?"#0f172a":"#e2e8f0");
    const mid=document.createElement("span");mid.style.cssText="flex:1;min-width:0";
    const nm=document.createElement("div");nm.textContent=b.name||("Gedung "+(i+1));nm.style.cssText="font-weight:800;font-size:14px;overflow-wrap:anywhere";
    const ty=document.createElement("div");ty.textContent=b.type||"";ty.style.cssText="font-size:11px;color:#94a3b8";
    mid.appendChild(nm);mid.appendChild(ty);
    const st=document.createElement("span");st.textContent=done?"✅ Selesai":rec?"🎯 Berikutnya":"";
    st.style.cssText="font-size:11px;font-weight:800;color:#fde68a;white-space:nowrap";
    it.appendChild(tag);it.appendChild(mid);it.appendChild(st);
    it.onclick=()=>{document.getElementById("halte-modal").style.display="none";aesStartShuttle(i)};
    list.appendChild(it);
  });
  document.getElementById("halte-modal").style.display="flex";
}

function aesStartShuttle(idx){
  if(!aesHalteEligible()||!aesHalteNear())return;
  const b=gameConfig.buildings[idx];if(!b)return;
  const bx=Number.isFinite(b.x)?b.x:0,bz=Number.isFinite(b.z)?b.z:0;
  const r=aesShuttlePath(bx,bz);
  const speed=Math.min(44,Math.max(AES_HALTE.speed,r.total/9));
  aesHalteEnsureUI();
  walkVel.x=0;walkVel.z=0;
  myPlayer.x=AES_HALTE.bay.x;myPlayer.z=AES_HALTE.bay.z;myPlayer.rotY=Math.PI;
  window.__aesShuttle={pts:r.pts,lens:r.lens,total:r.total,d:0,speed:speed,idx:idx,bx:bx,bz:bz,name:b.name||"",lastText:""};
  aesHalteSetBus(false);
  playSoundEffect("complete_building");
  setCarState("bus");
  showCoinToast("🚌 Bus berangkat ke [G"+(idx+1)+"]!");
  aesHalteUpdateHud();
}

function aesHalteUpdateHud(){
  const h=document.getElementById("halte-ride-hud");if(!h)return;
  const sh=window.__aesShuttle;
  if(!sh){h.style.display="none";return}
  const sec=Math.max(0,Math.ceil((sh.total-sh.d)/Math.max(1,sh.speed*.8)));
  const t="🚌 Menuju [G"+(sh.idx+1)+"] "+sh.name+" • ±"+sec+" dtk";
  if(t!==sh.lastText){sh.lastText=t;document.getElementById("halte-ride-text").textContent=t}
  h.style.display="flex";
}

function aesShuttleTick(dt){
  const sh=window.__aesShuttle;if(!sh)return;
  if(myPlayer.insideBuilding||myPlayer.inCar!=="bus"||gamePhase!=="explore"||myPlayer.atDock){aesShuttleStop(false);return}
  const v=sh.speed*Math.max(.2,Math.min(1,sh.d/16,(sh.total-sh.d)/16));
  sh.d=Math.min(sh.total,sh.d+v*dt);
  let acc=0,i=0;
  for(;i<sh.lens.length-1;i++){if(sh.d<=acc+sh.lens[i])break;acc+=sh.lens[i]}
  const p=sh.pts[i],q=sh.pts[i+1],L=sh.lens[i]||1,u=Math.max(0,Math.min(1,(sh.d-acc)/L));
  myPlayer.x=p.x+(q.x-p.x)*u;myPlayer.z=p.z+(q.z-p.z)*u;
  let df=Math.atan2(q.x-p.x,q.z-p.z)-myPlayer.rotY;df=Math.atan2(Math.sin(df),Math.cos(df));
  myPlayer.rotY+=df*Math.min(1,dt*9);
  walkVel.x=0;walkVel.z=0;
  aesHalteUpdateHud();
  if(sh.d>=sh.total-.01)aesShuttleStop(true);
}

function aesShuttleStop(arrived){
  const sh=window.__aesShuttle;if(!sh)return;
  window.__aesShuttle=null;
  if(arrived){
    const c=resolveSolidCollisions(sh.bx,sh.bz+14.5,1.15);
    myPlayer.x=c.x;myPlayer.z=c.z;myPlayer.rotY=Math.PI;
  }
  walkVel.x=0;walkVel.z=0;
  if(myPlayer.inCar==="bus")setCarState(false);else broadcastMyState();
  aesHalteSetBus(true);
  aesHalteUpdateHud();
  if(arrived){playSoundEffect("complete_building");showCoinToast("🚌 Tiba di [G"+(sh.idx+1)+"] "+sh.name+"! Klik BELAJAR di pintu")}
}
/* ===== /HALTE BUS KOTA ===== */

function groundHeightAt(e,t){return e>-12.3&&e<12.3&&t>59.7&&t<74.3?1.1:0}function equipKeyOf(e,t){return e=e||{},(e.head||"")+"|"+(e.face||"")+"|"+(e.neck||"")+"|"+(e.back||"")+"|"+(e.pack||"")+"|"+(e.wrist||"")+"|"+(e.body||"")+(t?"|"+t:"")}function recalcCoins(){const e=(myPlayer.coinBuildings||[]).length,t=(myPlayer.ownedItems||[]).reduce((n,o)=>n+shopPrice(shopItemById(o)),0);myPlayer.coins=Math.max(0,e-t)}function allBuildingsLearned(){return(gameConfig.buildings||[]).length===0?!1:gameConfig.buildings.every(t=>myPlayer.completedBuildings.includes(t.id))}function canUseCarNow(){return(gamePhase==="explore"||gamePhase==="walk_to_dock")&&!myPlayer.atDock&&!myPlayer.finishedRace}function updateShopHud(){const e=document.getElementById("shop-hud-row"),t=document.getElementById("shop-lock-hint"),n=document.getElementById("btn-car-toggle"),o=document.getElementById("btn-bus-toggle");if(!e||!t)return;const a=myPlayer.role==="student"&&myPlayer.hasJoinedGame,r=a&&allBuildingsLearned();if(e.classList.toggle("hidden",!r),t.classList.toggle("hidden",!(a&&!r)),n){const s=(myPlayer.ownedItems||[]).includes("car");n.classList.toggle("hidden",!(r&&s&&(!myPlayer.inCar||myPlayer.inCar==="car"))),n.textContent=myPlayer.inCar==="car"?"🚗 Turun dari Mobil":"🚗 Naik Mobil"}if(o){const s=(myPlayer.ownedItems||[]).includes("bus");o.classList.toggle("hidden",!(r&&s&&(!myPlayer.inCar||myPlayer.inCar==="bus"))),o.textContent=myPlayer.inCar==="bus"?"🚌 Turun dari Bus":"🚌 Naik Bus"}}function openShopModal(){if(!allBuildingsLearned()){showCoinToast("🔒 Selesaikan semua gedung dulu!");return}playSoundEffect("open_building"),renderShop(),document.getElementById("shop-modal").classList.remove("hidden")}function closeShopModal(){document.getElementById("shop-modal").classList.add("hidden")}function renderShop(){recalcCoins(),document.getElementById("shop-coin-balance").textContent=myPlayer.coins;const e=document.getElementById("shop-items-grid");e.innerHTML=SHOP_ITEMS.map(t=>{const n=myPlayer.ownedItems.includes(t.id);let o;if(n)if(t.slot==="car")o=`<button onclick="toggleVehicle('${t.id}')" class="px-3 py-1.5 rounded-lg text-xs font-extrabold bg-sky-400 hover:bg-sky-300 text-slate-950">${myPlayer.inCar===t.id?"Turun dari ":"Naik "}${t.id==="bus"?"Bus":"Mobil"}</button>`;else{const a=myPlayer.equip[t.slot]===t.id;o=`<button onclick="toggleEquipItem('${t.id}')" class="px-3 py-1.5 rounded-lg text-xs font-extrabold ${a?"bg-emerald-400 text-slate-950":"bg-slate-700 hover:bg-slate-600 text-white"}">${a?"✓ Dipakai (Lepas)":"Pakai"}</button>`}else{const a=shopPrice(t),r=myPlayer.coins>=a;o=`<button onclick="buyShopItem('${t.id}')" class="px-3 py-1.5 rounded-lg text-xs font-extrabold ${r?"bg-amber-400 hover:bg-amber-300 text-slate-950":"bg-slate-700 text-slate-400"}">🪙 Beli ${a} Koin</button>`}return`<div class="bg-slate-950 border ${n?"border-emerald-400/50":"border-slate-700"} rounded-2xl p-3.5 flex items-center gap-3">\n          <div class="text-4xl shrink-0">${t.icon}</div>\n          <div class="flex-1 min-w-0">\n            <div class="font-extrabold text-white text-sm">${t.name} <span class="text-amber-300 text-[11px]">🪙${shopPrice(t)}</span></div>\n            <div class="text-[11px] text-slate-400 mb-1.5">${t.desc}</div>\n            ${o}\n          </div>\n        </div>`}).join("")}function buyShopItem(e){const t=shopItemById(e);if(!(!t||myPlayer.ownedItems.includes(e))){if(recalcCoins(),myPlayer.coins<shopPrice(t)){playSoundEffect("wrong_answer"),showCoinToast(`🪙 Koinmu belum cukup! (butuh ${shopPrice(t)})`);return}myPlayer.ownedItems.push(e),t.slot!=="car"&&(myPlayer.equip[t.slot]=e),recalcCoins(),playSoundEffect("finish_island"),showCoinToast(`${t.icon} ${t.name} dibeli!`),updateHUDBuildingBadges(),broadcastMyState(),renderShop()}}function toggleEquipItem(e){const t=shopItemById(e);!t||t.slot==="car"||!myPlayer.ownedItems.includes(e)||(playSoundEffect("click"),myPlayer.equip[t.slot]===e?delete myPlayer.equip[t.slot]:myPlayer.equip[t.slot]=e,broadcastMyState(),renderShop())}function setCarState(e){myPlayer.inCar=e||!1,updateShopHud(),broadcastMyState(),document.getElementById("shop-modal").classList.contains("hidden")||renderShop()}function toggleVehicle(e){if(!myPlayer.ownedItems.includes(e)){openShopModal();return}if(myPlayer.inCar===e){playSoundEffect("click"),setCarState(!1);return}if(!canUseCarNow()){showCoinToast("🚗 Kendaraan hanya bisa dipakai saat keliling kota");return}myPlayer.rideDriverId&&leaveBus(),playSoundEffect("click"),setCarState(e)}function toggleCar(){toggleVehicle("car")}function toggleBus(){toggleVehicle("bus")}const BUS_CAPACITY=6,CAR_SCALE=1.5,CAR_LIFT=.6,BUS_LIFT=.5;function vehicleLift(e){return e==="car"?CAR_LIFT:e==="bus"?BUS_LIFT:0}const BUS_SEATS=[{x:-1.65,z:-3.4},{x:1.65,z:-3.4},{x:-1.65,z:-6.4},{x:1.65,z:-6.4},{x:-1.65,z:-9.4},{x:1.65,z:-9.4}];function busDriverPose(e){if(e===myPlayer.id)return myPlayer.inCar==="bus"?{x:myPlayer.x,z:myPlayer.z,r:myPlayer.rotY}:null;const t=otherPlayers[e];return!t||t.inCar!=="bus"||!t.mesh?null:{x:t.mesh.position.x,z:t.mesh.position.z,r:t.mesh.rotation.y}}function busPassengerIds(e){const t=[];return myPlayer.rideDriverId===e&&t.push(myPlayer.id),Object.values(otherPlayers).forEach(n=>{n.rideDriverId===e&&t.push(n.id)}),t.sort()}function busPassengerCount(e){return busPassengerIds(e).length}function busSeatIndex(e,t){return busPassengerIds(e).indexOf(t)}function busSeatWorld(e,t){const n=Math.sin(e.r),o=Math.cos(e.r);return{x:e.x+t.x*o+t.z*n,z:e.z-t.x*n+t.z*o}}function findBoardableBus(){if(myPlayer.role!=="student"||!myPlayer.hasJoinedGame||isTeacher3DMonitor||!canUseCarNow()||myPlayer.inCar||myPlayer.rideDriverId)return null;let e=null,t=11;return Object.values(otherPlayers).forEach(n=>{if(n.inCar!=="bus"||!n.mesh||n.finishedRace||n.atDock||busPassengerCount(n.id)>=BUS_CAPACITY)return;const o=n.mesh.rotation.y,a=n.mesh.position.x-Math.sin(o)*5,r=n.mesh.position.z-Math.cos(o)*5,s=Math.min(Math.hypot(myPlayer.x-n.mesh.position.x,myPlayer.z-n.mesh.position.z),Math.hypot(myPlayer.x-a,myPlayer.z-r));s<t&&(t=s,e=n)}),e}function boardBus(){const e=findBoardableBus();if(!e){showCoinToast("🚌 Tidak ada bus kosong di dekatmu");return}playSoundEffect("complete_building"),myPlayer.rideDriverId=e.id,walkVel.x=0,walkVel.z=0,showCoinToast(`🚌 Naik bus ${e.name}! Gratis 🎉`),updateBusBoardUI(),updateShopHud(),broadcastMyState()}function leaveBus(){const e=myPlayer.rideDriverId;if(!e)return;const t=busDriverPose(e)||{x:myPlayer.x,z:myPlayer.z,r:myPlayer.rotY};myPlayer.rideDriverId=null;const n=myPlayer.x+Math.cos(t.r)*5,o=myPlayer.z-Math.sin(t.r)*5,a=resolveSolidCollisions(n,o,1.15);myPlayer.x=a.x,myPlayer.z=a.z,walkVel.x=0,walkVel.z=0,updateBusBoardUI(),updateShopHud(),broadcastMyState()}function updateMyBusRide(){const e=myPlayer.rideDriverId;if(!e)return;const t=busDriverPose(e);if(!t||!canUseCarNow()||myPlayer.inCar){leaveBus();return}const n=busSeatIndex(e,myPlayer.id);if(n<0||n>=BUS_CAPACITY){leaveBus();return}const o=busSeatWorld(t,BUS_SEATS[n]);myPlayer.x=o.x,myPlayer.z=o.z,myPlayer.rotY=t.r}function onBusBoardClick(){myPlayer.rideDriverId?(playSoundEffect("click"),leaveBus()):boardBus()}function updateBusBoardUI(){const e=document.getElementById("bus-board-wrap");if(!e)return;const t=document.getElementById("btn-bus-board"),n=document.getElementById("bus-driver-hint");if(!(myPlayer.role==="student"&&myPlayer.hasJoinedGame&&!isTeacher3DMonitor)){e.classList.add("hidden");return}if(window.__aesShuttle){e.classList.add("hidden");return}if(myPlayer.inCar==="bus"){n.textContent=`🚌 Kamu menyetir bus • Penumpang ${busPassengerCount(myPlayer.id)}/${BUS_CAPACITY} • Dekatkan bus ke temanmu agar mereka bisa naik gratis`,n.classList.remove("hidden"),t.classList.add("hidden"),e.classList.remove("hidden");return}if(n.classList.add("hidden"),t.classList.remove("hidden"),myPlayer.rideDriverId){const a=otherPlayers[myPlayer.rideDriverId];t.textContent=`🚌 Turun dari Bus${a?" "+a.name:""}`,e.classList.remove("hidden")}else{const a=findBoardableBus();a?(t.textContent=`🚌 Naik Bus ${a.name} (Gratis!)`,e.classList.remove("hidden")):e.classList.add("hidden")}}function disposeObject3D(e){e.traverse(t=>{t.geometry&&t.geometry.dispose(),t.material&&(Array.isArray(t.material)?t.material:[t.material]).forEach(n=>n.dispose())})}function buildAccessoryGroup(e,t){const n=new THREE.Group,o=(r,s)=>new THREE.MeshPhongMaterial({color:r,shininess:Math.min(s||60,30),specular:2039583}),a=(r,s,i,l,m,d,w,p)=>{const u=new THREE.Mesh(r,s);return u.position.set(i,l,m),d&&(u.rotation.x=d),w&&(u.rotation.y=w),p&&(u.rotation.z=p),n.add(u),u};if(e=e||{},e.head==="hat_cap")a(new THREE.SphereGeometry(.68,16,10,0,Math.PI*2,0,Math.PI/2),o(14427686),0,3.95,0).scale.set(1,.75,.95),a(new THREE.BoxGeometry(.95,.06,.65),o(10033947),0,3.98,.78);else if(e.head==="hat_magic")a(new THREE.CylinderGeometry(.85,.85,.06,20),o(1120295),0,4.02,0),a(new THREE.CylinderGeometry(.5,.5,.95,20),o(1120295),0,4.5,0),a(new THREE.CylinderGeometry(.51,.51,.16,20),o(8141549),0,4.2,0);else if(e.head==="crown"){const r=o(16436245,90);a(new THREE.CylinderGeometry(.55,.55,.3,16),r,0,4.15,0);for(let s=0;s<5;s++){const i=s/5*Math.PI*2;a(new THREE.ConeGeometry(.13,.38,8),r,Math.cos(i)*.5,4.5,Math.sin(i)*.5)}a(new THREE.SphereGeometry(.1,8,8),o(15680580,90),0,4.2,.56)}if(e.face==="glasses"&&([-.27,.27].forEach(r=>{a(new THREE.BoxGeometry(.44,.3,.05),o(16436245),r,3.55,.64),a(new THREE.BoxGeometry(.34,.2,.06),new THREE.MeshBasicMaterial({color:959977,transparent:!0,opacity:.5}),r,3.55,.67)}),a(new THREE.BoxGeometry(.12,.06,.05),o(16436245),0,3.6,.64)),e.neck==="bowtie"){const r=o(14753096,80);[-1,1].forEach(s=>a(new THREE.ConeGeometry(.2,.36,10),r,s*.2,2.82,.48,0,0,s*-Math.PI/2)),a(new THREE.SphereGeometry(.1,10,8),o(10424889,80),0,2.82,.48)}if(e.back==="cape"&&!t){const r=e.pack?-.55:0;a(new THREE.BoxGeometry(1.35,1.8,.05),o(14427686,40),0,1.95,-.92+r,.1),a(new THREE.BoxGeometry(1.5,.14,.12),o(16436245,80),0,2.85,-.8+r)}if(e.pack==="backpack"&&!t){const r=o(16347926,40),s=o(12730636,40),i=o(2042167,30);a(new THREE.BoxGeometry(1,1.25,.5),r,0,2.2,-1.05),a(new THREE.BoxGeometry(1.04,.3,.56),s,0,2.7,-1.05),a(new THREE.BoxGeometry(.7,.5,.2),s,0,1.85,-1.4),a(new THREE.BoxGeometry(.16,.1,.06),o(16436245,80),0,2.55,-1.34),[-1,1].forEach(l=>{a(new THREE.BoxGeometry(.14,.14,1.4),i,l*.6,2.84,-.15),a(new THREE.BoxGeometry(.14,1.1,.06),i,l*.62,2.28,.5)})}if(e.body==="jacket"){const r=o(1920728,40),s=o(16317180,40);a(new THREE.BoxGeometry(1.64,.98,.14),r,0,2.3,-.4),[-1,1].forEach(i=>{a(new THREE.BoxGeometry(.14,.98,.98),r,i*.79,2.3,0),a(new THREE.BoxGeometry(.32,.98,.12),r,i*.65,2.3,.5),a(new THREE.BoxGeometry(.08,.98,.14),s,i*.49,2.3,.52)}),a(new THREE.BoxGeometry(1.66,.1,1),s,0,1.82,0),a(new THREE.BoxGeometry(1.2,.16,.96),r,0,2.86,0)}return n}function createPlateTexture(){try{const e=document.createElement("canvas");e.width=512,e.height=160;const t=e.getContext("2d");return t.scale(2,2),t.fillStyle="#f8fafc",t.fillRect(0,0,256,80),t.strokeStyle="#1e3a8a",t.lineWidth=6,t.strokeRect(5,5,246,70),t.fillStyle="#0f172a",t.font="bold 44px Arial",t.textAlign="center",t.textBaseline="middle",t.fillText("AES 2026",128,42),new THREE.CanvasTexture(e)}catch{return null}}function buildCarGroup(e){const t=new THREE.Group;t.scale.set(CAR_SCALE,CAR_SCALE,CAR_SCALE),t.position.y=-CAR_LIFT;const n=new THREE.Group;n.position.z=.3,t.add(n);const o=(c,h,x)=>new THREE.MeshPhongMaterial({color:c,shininess:h||70,specular:x||5592405}),a=o(e||"#0ea5e9",190,12303291),r=o(14870768,240,16777215),s=o(1120295,40,2236962),i=o(2042167,30,3355443),l=o(14427686,50,4473924),m=o(725024,8,1118481),d=o(2042167,120,8947848),w=new THREE.MeshPhongMaterial({color:1986426,transparent:!0,opacity:.72,shininess:220,specular:16777215,side:THREE.DoubleSide,depthWrite:!1}),p=c=>new THREE.MeshBasicMaterial({color:c}),u=(c,h,x,T,k,G,v,I)=>{const b=new THREE.Mesh(c,h);return b.position.set(x,T,k),G&&(b.rotation.x=G),v&&(b.rotation.y=v),I&&(b.rotation.z=I),n.add(b),b},H=new THREE.Shape;H.moveTo(-2.75,.42),H.lineTo(2.62,.42),H.quadraticCurveTo(2.98,.44,2.97,.7),H.bezierCurveTo(2.96,.86,2.92,.96,2.78,1.04),H.bezierCurveTo(2.35,1.16,1.7,1.26,1,1.34),H.lineTo(.95,1.36),H.lineTo(.95,1.12),H.lineTo(-1.5,1.12),H.lineTo(-1.55,1.36),H.bezierCurveTo(-2,1.44,-2.5,1.46,-2.78,1.26),H.bezierCurveTo(-2.92,1.1,-2.95,.8,-2.86,.58),H.quadraticCurveTo(-2.84,.43,-2.75,.42);const M=new THREE.ExtrudeGeometry(H,{depth:2.6,bevelEnabled:!0,bevelThickness:.2,bevelSize:.16,bevelSegments:6,curveSegments:12});M.translate(0,0,-1.3);{const c=M.attributes.position;for(let k=0;k<c.count;k++){const G=Math.max(0,(Math.abs(c.getX(k))-1.5)/1.7);c.setZ(k,c.getZ(k)*(1-.16*G*G))}c.needsUpdate=!0,M.computeVertexNormals();const h=M.attributes.normal,x={},T=k=>Math.round(c.getX(k)*500)+"_"+Math.round(c.getY(k)*500)+"_"+Math.round(c.getZ(k)*500);for(let k=0;k<c.count;k++){const G=T(k),v=x[G]||(x[G]=[0,0,0]);v[0]+=h.getX(k),v[1]+=h.getY(k),v[2]+=h.getZ(k)}for(let k=0;k<c.count;k++){const G=x[T(k)],v=Math.hypot(G[0],G[1],G[2])||1;h.setXYZ(k,G[0]/v,G[1]/v,G[2]/v)}h.needsUpdate=!0}const E=new THREE.Mesh(M,a);E.rotation.y=-Math.PI/2,n.add(E),u(new THREE.BoxGeometry(2.5,.3,5.3),s,0,.3,0);try{const c=document.createElement("canvas");c.width=c.height=128;const h=c.getContext("2d"),x=h.createRadialGradient(64,64,4,64,64,64);x.addColorStop(0,"rgba(255,255,255,0.95)"),x.addColorStop(1,"rgba(255,255,255,0)"),h.fillStyle=x,h.fillRect(0,0,128,128);const T=new THREE.MeshBasicMaterial({map:new THREE.CanvasTexture(c),color:e||"#0ea5e9",transparent:!0,opacity:.55,blending:THREE.AdditiveBlending,depthWrite:!1}),k=u(new THREE.PlaneGeometry(4.2,7.4),T,0,.13,0,-Math.PI/2);k.renderOrder=1}catch{}[-1,1].forEach(c=>{u(new THREE.BoxGeometry(.03,.62,.04),s,c*1.47,.82,.55),u(new THREE.BoxGeometry(.03,.62,.04),s,c*1.47,.82,-1.35),u(new THREE.BoxGeometry(.03,.04,1.9),s,c*1.47,1.04,-.4),u(new THREE.BoxGeometry(.04,.07,.34),r,c*1.48,.98,-.2),u(new THREE.BoxGeometry(.03,.05,2.5),r,c*1.47,.58,-.4);for(let h=0;h<3;h++)u(new THREE.BoxGeometry(.03,.05,.34),s,c*1.47,.78+h*.1,1.25-h*.02)}),u(new THREE.BoxGeometry(2.55,.3,.55),i,0,1.3,1.1),u(new THREE.BoxGeometry(.7,.05,.3),p(3718648),0,1.47,1.02),[-.55,.55].forEach(c=>{const h=u(new THREE.CircleGeometry(.15,18),p(2282478),c,1.5,.93,-.95);h.position.z+=0}),u(new THREE.BoxGeometry(1.9,.22,1),i,0,1.2,-.25),u(new THREE.BoxGeometry(1.92,.03,.04),l,0,1.33,.2),u(new THREE.BoxGeometry(1.9,1,.24),i,0,1.75,-1.1,.12),u(new THREE.BoxGeometry(1,.8,.04),l,0,1.75,-.97,.12),[-.55,.55].forEach(c=>u(new THREE.BoxGeometry(.42,.28,.2),i,c,2.4,-1.15,.12)),u(new THREE.CylinderGeometry(.09,.07,.3,10),r,.95,1.38,.15);const g=u(new THREE.TorusGeometry(.34,.05,10,26),s,0,1.62,.8,-.95);u(new THREE.CylinderGeometry(.07,.07,.08,12),r,0,1.62,.8,-.95+Math.PI/2),u(new THREE.CylinderGeometry(.05,.06,.6,8),s,0,1.5,.95,-.95),[-.7,.7].forEach(c=>u(new THREE.CylinderGeometry(.06,.07,1,10),r,c,1.9,-1.5,.15)),u(new THREE.CylinderGeometry(.05,.05,1.5,10),r,0,2.4,-1.575,0,0,Math.PI/2);const f=-.61;u(new THREE.BoxGeometry(2.55,.9,.03),w,0,1.78,1,f).renderOrder=2,u(new THREE.BoxGeometry(2.62,.06,.07),r,0,2.22,.78,f),u(new THREE.BoxGeometry(2.62,.06,.07),r,0,1.36,1.24,f),[-1,1].forEach(c=>{u(new THREE.BoxGeometry(.06,.95,.07),r,c*1.3,1.79,1,f),u(new THREE.BoxGeometry(.05,.05,.22),r,c*1.42,1.72,1.15),u(new THREE.BoxGeometry(.26,.16,.08),a,c*1.55,1.74,1.15)}),[-.2,.2].forEach(c=>u(new THREE.BoxGeometry(.2,.03,1.65),p(16317180),c,1.42,1.95,.17)),u(new THREE.BoxGeometry(1.6,.34,.1),s,0,.74,3.08),[-.2,0,.2].forEach(c=>u(new THREE.BoxGeometry(1.52,.03,.12),r,0,.74+c*.8,3.1)),u(new THREE.CylinderGeometry(.11,.11,.04,20),r,0,1,3.06,Math.PI/2),u(new THREE.BoxGeometry(2.6,.08,.5),s,0,.44,2.9),[-1,1].forEach(c=>{const h=u(new THREE.TorusGeometry(.3,.045,10,26),r,c*1,.98,2.9);u(new THREE.SphereGeometry(.26,18,12),p(16710083),c*1,.98,2.86).scale.set(1,1,.45),u(new THREE.TorusGeometry(.15,.025,8,20),r,c*1,.98,2.95),u(new THREE.BoxGeometry(.55,.05,.05),p(14742270),c*1,1.32,2.5,.17)}),u(new THREE.BoxGeometry(2.9,.2,.22),r,0,.5,3),u(new THREE.BoxGeometry(2.3,.1,.06),p(14427686),0,1.16,-3.04),[-1,1].forEach(c=>{u(new THREE.BoxGeometry(.62,.2,.06),p(15680580),c*1,.98,-3.07),u(new THREE.CylinderGeometry(.1,.1,.45,14),r,c*.62,.52,-3,Math.PI/2),u(new THREE.CylinderGeometry(.07,.07,.47,14),s,c*.62,.52,-3,Math.PI/2),u(new THREE.BoxGeometry(.1,.24,.2),a,c*.72,1.7,-2.72),u(new THREE.BoxGeometry(.05,.3,.6),a,c*1.15,1.9,-2.72)}),u(new THREE.BoxGeometry(2.3,.06,.62),a,0,1.86,-2.72,.1),u(new THREE.BoxGeometry(1.7,.18,.18),s,0,.5,-3),u(new THREE.BoxGeometry(2.9,.2,.22),r,0,.5,-3);const R=createPlateTexture();u(new THREE.BoxGeometry(.95,.3,.04),R?new THREE.MeshBasicMaterial({map:R}):o(16317180),0,.82,-3.12);const y=[];return[-1,1].forEach(c=>[-1,1].forEach(h=>{const x=h*1.75;u(new THREE.CylinderGeometry(.8,.8,.14,24),s,c*1.4,.66,x,0,0,Math.PI/2),u(new THREE.TorusGeometry(.82,.04,8,32),r,c*1.48,.66,x,0,Math.PI/2,0);const T=new THREE.Group;T.position.set(c*1.52,.62,x),n.add(T);const k=(v,I)=>{const b=new THREE.Mesh(v,I);return b.rotation.z=Math.PI/2,T.add(b),b};k(new THREE.CylinderGeometry(.62,.62,.5,32),m),k(new THREE.CylinderGeometry(.44,.44,.52,26),d);const G=new THREE.Mesh(new THREE.TorusGeometry(.45,.04,8,28),r);G.rotation.y=Math.PI/2,G.position.x=c*.26,T.add(G);for(let v=0;v<5;v++){const I=new THREE.Mesh(new THREE.BoxGeometry(.06,.8,.1),r);I.position.x=c*.27,I.rotation.x=v/5*Math.PI,T.add(I)}k(new THREE.CylinderGeometry(.13,.13,.56,14),r),k(new THREE.CylinderGeometry(.06,.06,.58,10),l),y.push(T)})),t.userData.wheels=y,t.userData.wheelR=.62*CAR_SCALE,t}function buildWatchGroup(){const e=new THREE.Group,t=(r,s)=>new THREE.MeshPhongMaterial({color:r,shininess:Math.min(s||60,30),specular:2039583}),n=new THREE.Mesh(new THREE.TorusGeometry(.19,.05,8,18),t(1976635));n.rotation.x=Math.PI/2,n.position.y=-.5,e.add(n);const o=new THREE.Mesh(new THREE.BoxGeometry(.08,.2,.2),t(16436245,90));o.position.set(-.23,-.5,0),e.add(o);const a=new THREE.Mesh(new THREE.BoxGeometry(.03,.14,.14),new THREE.MeshBasicMaterial({color:3718648}));return a.position.set(-.28,-.5,0),e.add(a),e}function createBusSignTexture(){try{const e=document.createElement("canvas");e.width=1024,e.height=256;const t=e.getContext("2d");return t.scale(2,2),t.fillStyle="#facc15",t.fillRect(0,0,512,128),t.strokeStyle="#0f172a",t.lineWidth=8,t.strokeRect(6,6,500,116),t.fillStyle="#0f172a",t.font="bold 64px Arial",t.textAlign="center",t.textBaseline="middle",t.fillText("BUS WISATA",256,68),new THREE.CanvasTexture(e)}catch{return null}}function buildBusGroup(e){const t=new THREE.Group;t.position.y=-BUS_LIFT;const n=new THREE.Group;t.add(n);const o=(h,x,T)=>new THREE.MeshPhongMaterial({color:h,shininess:x||70,specular:T||5592405}),a=o(e||"#0ea5e9",120,7829367),r=o(16317180,80),s=o(14870768,220,16777215),i=o(1120295,40,2236962),l=o(4674921,20,1118481),m=o(12131356,30,3355443),d=o(725024,10,1118481),w=new THREE.MeshPhongMaterial({color:9684477,transparent:!0,opacity:.26,shininess:200,specular:16777215,side:THREE.DoubleSide,depthWrite:!1}),p=(h,x,T,k,G,v,I,b)=>{const S=new THREE.Mesh(h,x);return S.position.set(T,k,G),v&&(S.rotation.x=v),I&&(S.rotation.y=I),b&&(S.rotation.z=b),n.add(S),S},u=(h,x,T)=>new THREE.BoxGeometry(h,x,T),H=4.8,M=-11,E=(H+M)/2,g=H-M;p(u(6,.5,g-.2),i,0,.3,E),p(u(6.2,.12,g-.2),l,0,.54,E),[-1,1].forEach(h=>{p(u(.18,1.7,g),a,h*3.1,1.4,E),p(u(.2,.2,g+.02),r,h*3.1,1.55,E),p(u(.06,3.1,g-.6),w,h*3.14,3.85,E).renderOrder=2,[4.4,1.2,-2,-5.2,-8.4,-10.6].forEach(x=>p(u(.24,3.15,.3),a,h*3.14,3.85,x)),p(u(.2,.12,g),s,h*3.14,5.42,E)});const f=new THREE.MeshPhongMaterial({color:16317180,shininess:80,transparent:!0,opacity:.42,depthWrite:!1});p(u(6.5,.3,g+.3),f,0,5.6,E).renderOrder=1,p(u(3,.45,4),a,0,5.95,-5);const R=createBusSignTexture();p(u(3.8,.8,.1),R?new THREE.MeshBasicMaterial({map:R}):o(16436245),0,5.1,H+.12),p(u(6.4,.3,.25),a,0,5.38,H+.05),p(u(6,2.4,.06),w,0,3.5,H+.1,-.12).renderOrder=2,p(u(6.2,.1,.12),s,0,4.72,H+.02),[-1,1].forEach(h=>p(u(.1,2.5,.12),s,h*3,3.5,H+.08)),p(u(5.6,2.4,.06),w,0,3.5,M-.05).renderOrder=2,p(u(6.4,1.7,.3),a,0,1.4,H),p(u(6.4,.2,.32),r,0,1.55,H),p(u(6.4,1.7,.3),a,0,1.4,M),p(u(6.4,.2,.32),r,0,1.55,M),p(u(5.2,.7,.9),i,0,2.2,3.3),p(new THREE.TorusGeometry(.55,.07,8,24),i,0,2.9,2.2,-1),p(new THREE.CylinderGeometry(.08,.1,1.1,8),i,0,2.5,2.6,-1),p(u(2.6,.5,1.4),m,0,1.55,-.1),p(u(2.6,1.5,.22),m,0,2.5,-.85),[-3.4,-6.4,-9.4].forEach(h=>{[-1.65,1.65].forEach(x=>{p(u(2.5,.5,1.4),m,x,1.55,h-.1),p(u(2.5,1.5,.22),m,x,2.5,h-.85)}),p(new THREE.CylinderGeometry(.07,.07,4.8,8),s,0,3,h+.6)}),[-1,1].forEach(h=>{p(u(1,.45,.1),new THREE.MeshBasicMaterial({color:16710083}),h*2.3,1.25,H+.18),p(u(1.1,.55,.06),s,h*2.3,1.25,H+.14),p(u(.9,.4,.08),new THREE.MeshBasicMaterial({color:14427686}),h*2.4,1.25,M-.18),p(new THREE.CylinderGeometry(.05,.05,.7,6),s,h*3.5,3.9,H-.5,0,0,Math.PI/2),p(u(.14,.9,.4),a,h*3.95,3.9,H-.5)}),p(u(2.4,.9,.08),i,0,1.3,H+.18),p(u(6.6,.35,.35),s,0,.7,H+.25),p(u(6.6,.35,.35),s,0,.7,M-.25);const y=createPlateTexture();p(u(1.4,.4,.05),y?new THREE.MeshBasicMaterial({map:y}):o(16317180),0,1,M-.2);const c=[];return[-1,1].forEach(h=>[3.2,-8].forEach(x=>{const T=new THREE.Group;T.position.set(h*3.05,1.1,x),n.add(T);const k=new THREE.Mesh(new THREE.CylinderGeometry(1.1,1.1,.8,28),d);k.rotation.z=Math.PI/2,T.add(k);const G=new THREE.Mesh(new THREE.CylinderGeometry(.72,.72,.82,22),s);G.rotation.z=Math.PI/2,T.add(G);for(let I=0;I<5;I++){const b=new THREE.Mesh(new THREE.BoxGeometry(.1,1.3,.16),i);b.position.x=h*.42,b.rotation.x=I/5*Math.PI,T.add(b)}const v=new THREE.Mesh(new THREE.CylinderGeometry(.2,.2,.86,12),s);v.rotation.z=Math.PI/2,T.add(v),c.push(T)})),t.userData.wheels=c,t.userData.wheelR=1.1,t}function applyEquipToMesh(e,t,n){if(!e)return;const o=e.userData;o.accGroup&&(e.remove(o.accGroup),disposeObject3D(o.accGroup),o.accGroup=null),o.carGroup&&(e.remove(o.carGroup),disposeObject3D(o.carGroup),o.carGroup=null),o.watchObj&&o.leftArm&&(o.leftArm.remove(o.watchObj),disposeObject3D(o.watchObj),o.watchObj=null);const a=buildAccessoryGroup(t,n);if(e.add(a),o.accGroup=a,n){const r=n==="bus"?buildBusGroup(o.playerColor):buildCarGroup(o.playerColor);e.add(r),o.carGroup=r}if(t&&t.wrist==="watch"&&o.leftArm){const r=buildWatchGroup();o.leftArm.add(r),o.watchObj=r}o.equipKey=equipKeyOf(t,n)}function escQ(e){return String(e??"").replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;")}function buildingHasQuiz(e){const t=e&&e.quiz;return!t||!String(t.q||"").trim()?!1:(t.options||[]).filter(n=>String(n||"").trim()).length>=2}function showCoinToast(e){const t=document.createElement("div");t.textContent=e,t.style.cssText="position:fixed;top:18%;left:50%;transform:translateX(-50%);z-index:99999;padding:12px 22px;border-radius:9999px;background:#facc15;color:#0f172a;font-weight:800;font-size:16px;box-shadow:0 0 30px rgba(250,204,21,.9);transition:all .6s ease;pointer-events:none;",document.body.appendChild(t),setTimeout(()=>{t.style.opacity="0",t.style.top="12%"},1700),setTimeout(()=>t.remove(),2400)}function awardBuildingCoinIfEligible(e){return!e||myPlayer.coinBuildings.includes(e)||myPlayer.buildingQuizResult[e]!=="correct"||!myPlayer.completedBuildings.includes(e)?!1:(myPlayer.coinBuildings.push(e),recalcCoins(),playSoundEffect("finish_island"),showCoinToast("🪙 +1 Koin!"),updateHUDBuildingBadges(),broadcastMyState(),!0)}const bqOrderCache={};function optionsDependOnOrder(e){return e.some(t=>/semua (jawaban|opsi|pilihan)?.*(benar|salah|betul)|(benar|salah|betul) semua|keduanya|kedua-duanya|tidak ada .*(benar|salah|di atas)|di atas|(jawaban|opsi|pilihan)\s*[A-D]\b|\b[A-D]\s*(dan|&|serta)\s*[A-D]\b\s*(benar|salah|betul)/i.test(String(t||"")))}function getShuffledOrder(e){const t=e.map((n,o)=>o).filter(n=>String(e[n]||"").trim());if(optionsDependOnOrder(e))return t;for(let n=t.length-1;n>0;n--){const o=Math.floor(Math.random()*(n+1));[t[n],t[o]]=[t[o],t[n]]}return t}function getBuildingQuizOrder(e){const t=JSON.stringify(e.quiz.options),n=bqOrderCache[e.id];if(n&&n.sig===t)return n.order;const o=getShuffledOrder(e.quiz.options);return bqOrderCache[e.id]={sig:t,order:o},o}function renderBuildingQuiz(e){const t=document.getElementById("building-quiz-box");if(!t)return;if(!e||!buildingHasQuiz(e)||!myPlayer.completedBuildings.includes(e.id)){t.classList.add("hidden");return}t.classList.remove("hidden");const n=e.quiz,o=myPlayer.buildingQuizResult[e.id];document.getElementById("building-quiz-question").innerHTML=formatRichEducationalText(n.q,1);const a=document.getElementById("building-quiz-options"),r=document.getElementById("building-quiz-feedback"),s=(myPlayer.buildingQuizPick||{})[e.id];if(a.innerHTML=getBuildingQuizOrder(e).map((i,l)=>{const m=n.options[i];let d="bg-slate-900 border-slate-700 hover:border-amber-400 text-slate-100";return o&&(d="bg-slate-900 border-slate-800 text-slate-400 cursor-default",i===n.correct?d="bg-emerald-500/20 border-emerald-400 text-emerald-200 cursor-default":i===s&&(d="bg-rose-500/20 border-rose-400 text-rose-200 cursor-default")),`<button ${o?"disabled":""} onclick="answerBuildingQuiz('${e.id}', ${i})" class="text-left px-3.5 py-2.5 rounded-xl border-2 text-sm font-semibold transition ${d}"><span class="font-extrabold text-sky-300 mr-2">${String.fromCharCode(65+l)}.</span>${formatRichEducationalText(m,1)}</button>`}).join(""),!o)r.textContent="";else if(o==="correct"){const i=myPlayer.coinBuildings.includes(e.id);r.className="text-sm font-extrabold min-h-[1.25rem] text-emerald-300",r.textContent=i?"✅ Benar di percobaan pertama! 🪙 Kamu mendapat 1 koin.":"✅ Benar di percobaan pertama! Simpan catatan belajarmu (min. 15 karakter) untuk mendapatkan 🪙 1 koin."}else r.className="text-sm font-extrabold min-h-[1.25rem] text-rose-300",r.textContent="❌ Belum tepat. Jawaban benar ditandai hijau. Koin gedung ini tidak didapat.";triggerMathJaxRender([t])}function updateFinishButtonLabel(e){const t=document.getElementById("btn-finish-building");if(!t||!e)return;const n=myPlayer.completedBuildings.includes(e.id);t.textContent=n?"✖ Tutup":"✅ Simpan Catatan & Selesai Mempelajari Gedung Ini"}function answerBuildingQuiz(e,t){const n=gameConfig.buildings.find(a=>a.id===e);if(!n||!buildingHasQuiz(n)||myPlayer.buildingQuizResult[e])return;myPlayer.buildingQuizPick||(myPlayer.buildingQuizPick={}),myPlayer.buildingQuizPick[e]=t;const o=t===n.quiz.correct;myPlayer.buildingQuizResult[e]=o?"correct":"wrong",broadcastMyState(),playSoundEffect(o?"correct_row":"wrong_answer"),o&&awardBuildingCoinIfEligible(e),renderBuildingQuiz(n)}function closeBuildingModal(){document.getElementById("building-material-modal").classList.add("hidden"),myPlayer.insideBuilding&&(myPlayer.insideBuilding=null,myAvatarMesh&&myPlayer.hasJoinedGame&&!myPlayer.atDock&&!isTeacher3DMonitor&&(myAvatarMesh.visible=!0),updateDoorBoards(),broadcastMyState())}function markBuildingCompletedAndClose(){if(!activeNearBuilding)return;const e=activeNearBuilding;if(myPlayer.completedBuildings.includes(e.id)){closeBuildingModal();return}if((studentNotes[e.id]||"").trim().length<15){playSoundEffect("wrong_answer"),alert("⚠️ Silakan tulis rangkuman atau catatan belajarmu minimal 15 karakter terlebih dahulu agar Bapak/Ibu Guru dapat memastikan kamu benar-benar telah mempelajari materi di gedung ini!"),document.getElementById("student-personal-note").focus();return}if(playSoundEffect("complete_building"),myPlayer.buildingNotes={...studentNotes},myPlayer.completedBuildings.push(e.id),updateHUDBuildingBadges(),broadcastMyState(),updateFinishButtonLabel(e),buildingHasQuiz(e)&&!myPlayer.buildingQuizResult[e.id]){renderBuildingQuiz(e);const n=document.getElementById("building-quiz-box");n&&setTimeout(()=>n.scrollIntoView({behavior:"smooth",block:"center"}),80);return}closeBuildingModal()}let joystickVector={x:0,y:0},moveKeys={up:!1,down:!1,left:!1,right:!1},cameraYaw=0,cameraPitch=.22,cameraDistance=6.5;function initAnalogJoystick(){const e=document.getElementById("joystick-base"),t=document.getElementById("joystick-knob");let n=!1;const o=38;function a(s,i){const l=e.getBoundingClientRect();let m=s-(l.left+l.width/2),d=i-(l.top+l.height/2);const w=Math.hypot(m,d);w>o&&(m=m/w*o,d=d/w*o),t.style.transform=`translate(${m}px, ${d}px)`,joystickVector.x=m/o,joystickVector.y=d/o}function r(){n=!1,t.style.transform="translate(0px, 0px)",joystickVector.x=0,joystickVector.y=0}e.addEventListener("pointerdown",s=>{initAudioEngine(),n=!0,e.setPointerCapture(s.pointerId),a(s.clientX,s.clientY),s.stopPropagation()}),e.addEventListener("pointermove",s=>{n&&(a(s.clientX,s.clientY),s.stopPropagation())}),e.addEventListener("pointerup",r),e.addEventListener("pointercancel",r)}function initCameraOrbitControls(){const e=document.getElementById("canvas-container");let t=!1,n=0,o=0;e.addEventListener("pointerdown",a=>{initAudioEngine(),t=!0,n=a.clientX,o=a.clientY}),window.addEventListener("pointermove",a=>{t&&(cameraYaw-=(a.clientX-n)*.0075,cameraPitch=Math.max(-.22,Math.min(1.35,cameraPitch+(a.clientY-o)*.0065)),n=a.clientX,o=a.clientY)}),window.addEventListener("pointerup",()=>{t=!1}),window.addEventListener("wheel",a=>{setCameraDistanceFromSlider(cameraDistance+a.deltaY*.012)})}function setCameraDistanceFromSlider(e){cameraDistance=Math.max(3.5,Math.min(45,parseFloat(e)||6.5));const t=document.getElementById("camera-dist-slider");t&&(t.value=cameraDistance);const n=document.getElementById("cam-dist-label");n&&(n.textContent=cameraDistance<6?"Dekat":cameraDistance<16?"Sedang":"Jauh")}function setQuickCameraView(e,t){playSoundEffect("click"),setCameraDistanceFromSlider(e),cameraPitch=t,cameraYaw=myPlayer.rotY+Math.PI}let solidBoxObstacles=[],solidCircleObstacles=[];function resolveSolidCollisions(e,t,n=1.15){let o=e,a=t;for(const r of solidBoxObstacles){const s=Math.max(r.minX,Math.min(o,r.maxX)),i=Math.max(r.minZ,Math.min(a,r.maxZ)),l=o-s,m=a-i,d=Math.hypot(l,m);d<n&&(d>1e-4?(o+=l/d*(n-d),a+=m/d*(n-d)):a+=n)}for(const r of solidCircleObstacles){const s=o-r.x,i=a-r.z,l=Math.hypot(s,i),m=n+r.r;l<m&&l>1e-4&&(o+=s/l*(m-l),a+=i/l*(m-l))}for(const r of npcCarsList){const s=o-r.position.x,i=a-r.position.z,l=Math.hypot(s,i),m=n+(r.userData.hitRadius||3.2);l<m&&l>1e-4&&(o+=s/l*(m-l),a+=i/l*(m-l))}return{x:o,z:a}}let scene,camera,renderer,cityBuildingsGroup,buildingColliders=[],all20CityBuildingsMeta=[],animatedRoofProps=[],doorBoards={};function createDoorBoard(){const e=new THREE.Group,t=new THREE.Mesh(new THREE.CylinderGeometry(.12,.14,3.2,8),new THREE.MeshLambertMaterial({color:4674921}));t.position.y=1.6,e.add(t);const n=document.createElement("canvas");n.width=1024,n.height=640;const o=new THREE.CanvasTexture(n);o.generateMipmaps=!0,o.minFilter=THREE.LinearMipmapLinearFilter,o.magFilter=THREE.LinearFilter,o.anisotropy=labelAniso();const a=new THREE.Sprite(new THREE.SpriteMaterial({map:o,transparent:!0,fog:!1,depthTest:!0}));return a.scale.set(7.2,4.5,1),a.position.y=5.4,e.add(a),a.userData={baseW:7.2,baseH:4.5},registerLabelSprite(a),e.visible=!1,{group:e,canvas:n,texture:o,key:""}}function drawDoorBoard(e,t,n){const o=e.canvas,a=o.getContext("2d");a.clearRect(0,0,o.width,o.height),a.fillStyle="#0b1220",a.strokeStyle="#34d399",a.lineWidth=14,drawRoundedRect(a,10,10,1004,620,60),a.fill(),a.stroke(),a.textAlign="center",a.textBaseline="middle",a.lineJoin="round";const r=(l,m,d)=>{let w=m;for(a.font=`900 ${w}px 'Plus Jakarta Sans', Arial, sans-serif`;w>26&&a.measureText(l).width>d;)w-=2,a.font=`900 ${w}px 'Plus Jakarta Sans', Arial, sans-serif`};r(`🏢 ${t} • Sedang Belajar (${n.length})`,56,920),a.fillStyle="#facc15",a.fillText(`🏢 ${t} • Sedang Belajar (${n.length})`,512,84),a.fillStyle="#34d399",a.fillRect(80,134,864,6);const s=6;(n.length>s?n.slice(0,s-1).concat(["+"+(n.length-(s-1))+" siswa lainnya"]):n).forEach((l,m)=>{const d=n.length>s&&m===s-1?l:"👤 "+l;r(d,54,900),a.fillStyle="#ffffff",a.fillText(d,512,200+m*74)})}function updateDoorBoards(){const e={};getAllStudentsListForReport().forEach(t=>{t.insideBuilding&&(e[t.insideBuilding]=e[t.insideBuilding]||[]).push(t.name+(t.isMe?" (Kamu)":""))}),Object.keys(doorBoards).forEach(t=>{const n=doorBoards[t],o=(e[t]||[]).sort(),a=o.join("|");if(!o.length){n.group.visible=!1,n.key="";return}if(a!==n.key){n.key=a;const r=gameConfig.buildings.findIndex(s=>s.id===t);drawDoorBoard(n,"G"+(r+1),o),n.texture.needsUpdate=!0}n.group.visible=!0})}let myAvatarMesh=null,myBoatMesh=null,overheadArrowGroup=null,cloudsList=[],npcCarsList=[],dronesList=[],islandBirdsList=[],clock=null;function drawRoundedRect(e,t,n,o,a,r){e.beginPath(),e.moveTo(t+r,n),e.lineTo(t+o-r,n),e.quadraticCurveTo(t+o,n,t+o,n+r),e.lineTo(t+o,n+a-r),e.quadraticCurveTo(t+o,n+a,t+o-r,n+a),e.lineTo(t+r,n+a),e.quadraticCurveTo(t,n+a,t,n+a-r),e.lineTo(t,n+r),e.quadraticCurveTo(t,n,t+r,n),e.closePath()}function createSoftShadowTexture(){const e=document.createElement("canvas");e.width=128,e.height=128;const t=e.getContext("2d"),n=t.createRadialGradient(64,64,10,64,64,60);return n.addColorStop(0,"rgba(15, 23, 42, 0.30)"),n.addColorStop(.55,"rgba(15, 23, 42, 0.14)"),n.addColorStop(1,"rgba(15, 23, 42, 0)"),t.fillStyle=n,t.fillRect(0,0,128,128),new THREE.CanvasTexture(e)}const windowTextureCache={};function getProceduralWindowTexture(e,t,n=6,o=4){const a=`${e}_${t}_${n}_${o}`;if(windowTextureCache[a])return windowTextureCache[a];const r=document.createElement("canvas");r.width=256,r.height=512;const s=r.getContext("2d");s.fillStyle=e,s.fillRect(0,0,256,512);const i=18,l=24,m=(256-i*2)/o,d=(512-l*2)/n;for(let p=0;p<n;p++)for(let u=0;u<o;u++)s.fillStyle=(p+u)%3===0?"#fef08a":t,s.fillRect(i+u*m+5,l+p*d+6,m-10,d-12);const w=new THREE.CanvasTexture(r);return windowTextureCache[a]=w,w}function getFacadeTexture(e,t,n,o,a){o=o||5,a=a||4;const r="F_"+[e,t,n,o,a].join("_");if(windowTextureCache[r])return windowTextureCache[r];const s=document.createElement("canvas");s.width=256,s.height=256;const i=s.getContext("2d");i.fillStyle=t,i.fillRect(0,0,256,256);const l=256/a,m=256/o,d=p=>{for(let u=0;u<o;u++)for(let H=0;H<a;H++){const M=l*.5,E=H*l+l*.25,g=u*m+m*.16,f=m*.66;i.fillStyle=(u+H)%4===0?"#fde68a":p,i.fillRect(E,g+M/2,M,f-M/2),i.beginPath(),i.arc(E+M/2,g+M/2,M/2,Math.PI,0),i.fill(),i.strokeStyle="rgba(255,255,255,0.7)",i.lineWidth=2,i.strokeRect(E,g+M/2,M,f-M/2)}};if(e==="brick"){i.strokeStyle="rgba(0,0,0,0.22)",i.lineWidth=2;for(let p=0;p<256;p+=16){i.beginPath(),i.moveTo(0,p),i.lineTo(256,p),i.stroke();const u=p/16%2?0:16;for(let H=u;H<256;H+=32)i.beginPath(),i.moveTo(H,p),i.lineTo(H,p+16),i.stroke()}d(n)}else if(e==="stone"){i.strokeStyle="rgba(0,0,0,0.10)",i.lineWidth=2;for(let p=0;p<256;p+=32)i.beginPath(),i.moveTo(0,p),i.lineTo(256,p),i.stroke();d(n)}else if(e==="glass"){const p=i.createLinearGradient(0,0,256,256);p.addColorStop(0,t),p.addColorStop(1,n),i.fillStyle=p,i.fillRect(0,0,256,256);for(let u=0;u<o;u++)for(let H=0;H<a;H++)(u*7+H*3)%5===0&&(i.fillStyle="rgba(254,240,138,0.55)",i.fillRect(H*l,u*m,l,m));i.strokeStyle="rgba(255,255,255,0.55)",i.lineWidth=3;for(let u=0;u<=a;u++)i.beginPath(),i.moveTo(u*l,0),i.lineTo(u*l,256),i.stroke();for(let u=0;u<=o;u++)i.beginPath(),i.moveTo(0,u*m),i.lineTo(256,u*m),i.stroke()}else if(e==="bands")for(let p=0;p<o;p++){i.fillStyle=n,i.fillRect(0,p*m+m*.28,256,m*.44),i.fillStyle="rgba(255,255,255,0.35)";for(let u=0;u<a*2;u++)i.fillRect(u*l/2,p*m+m*.28,3,m*.44);p%2===0&&(i.fillStyle="rgba(254,240,138,0.7)",i.fillRect(l*(p%a),p*m+m*.28,l,m*.44))}else if(e==="film"){for(let p=6;p<256;p+=24)i.fillStyle="#fff",i.fillRect(8,p,12,14),i.fillRect(236,p,12,14);for(let p=0;p<o;p++)for(let u=0;u<a;u++)i.fillStyle=(p+u)%2?n:"#a78bfa",i.fillRect(34+u*(188/a),p*m+8,188/a-10,m-16)}else if(e==="pitch"){for(let p=0;p<8;p++)i.fillStyle=p%2?"#16a34a":"#22c55e",i.fillRect(p*32,0,32,256);i.strokeStyle="#fff",i.lineWidth=4,i.strokeRect(14,14,228,228),i.beginPath(),i.moveTo(128,14),i.lineTo(128,242),i.stroke(),i.beginPath(),i.arc(128,128,30,0,Math.PI*2),i.stroke(),i.strokeRect(14,78,40,100),i.strokeRect(202,78,40,100)}else if(e==="garage"){i.strokeStyle=n,i.lineWidth=3;for(let p=20;p<256;p+=22)i.beginPath(),i.moveTo(0,p),i.lineTo(256,p),i.stroke();i.fillStyle="#38bdf8";for(let p=0;p<4;p++)i.fillRect(16+p*60,22,46,16)}else for(let p=0;p<o;p++)for(let u=0;u<a;u++){const H=u*l+l*.18,M=p*m+m*.18,E=l*.64,g=m*.6;i.fillStyle=(p+u)%3===0?"#fef08a":n,i.fillRect(H,M,E,g),i.fillStyle="rgba(255,255,255,0.8)",i.fillRect(H-3,M+g,E+6,4),i.strokeStyle="rgba(0,0,0,0.25)",i.lineWidth=2,i.strokeRect(H,M,E,g)}const w=new THREE.CanvasTexture(s);return windowTextureCache[r]=w,w}function starShape(e,t){const n=new THREE.Shape;for(let o=0;o<10;o++){const a=Math.PI/2+o*Math.PI/5,r=o%2?t:e,s=Math.cos(a)*r,i=Math.sin(a)*r;o===0?n.moveTo(s,i):n.lineTo(s,i)}return n.closePath(),n}function createLushTreeMesh(e=0){const t=new THREE.Group,n=new THREE.Mesh(new THREE.CylinderGeometry(.48,.72,3.6,8),new THREE.MeshLambertMaterial({color:7877903}));if(n.position.y=1.8,t.add(n),e%2===0){const o=new THREE.Mesh(new THREE.SphereGeometry(2.6,12,12),new THREE.MeshLambertMaterial({color:1409085}));o.position.set(0,4.6,0),t.add(o);const a=new THREE.Mesh(new THREE.SphereGeometry(1.9,10,10),new THREE.MeshLambertMaterial({color:2278750}));a.position.set(.9,5.7,.5),t.add(a)}else{const o=new THREE.Mesh(new THREE.ConeGeometry(2.7,4.2,10),new THREE.MeshLambertMaterial({color:1467700}));o.position.y=4.2,t.add(o);const a=new THREE.Mesh(new THREE.ConeGeometry(2.1,3.6,10),new THREE.MeshLambertMaterial({color:2278750}));a.position.y=6.2,t.add(a)}return t}function initThreeJSWorld(){if(typeof THREE>"u")return;clock=new THREE.Clock;const e=document.getElementById("canvas-container");scene=new THREE.Scene,scene.background=new THREE.Color(6333946),scene.fog=new THREE.FogExp2(9684477,55e-5),camera=new THREE.PerspectiveCamera(60,window.innerWidth/window.innerHeight,.5,1800),camera.position.set(0,8,55);const t=!1;renderer=new THREE.WebGLRenderer({antialias:!0,logarithmicDepthBuffer:t,powerPreference:"high-performance"}),renderer.setSize(window.innerWidth,window.innerHeight);const n=aesGfxLow();baseDpr=aesGfxBaseDpr(),curDpr=baseDpr,renderer.setPixelRatio(curDpr);try{THREE.Texture.DEFAULT_ANISOTROPY=Math.min(renderer.capabilities.getMaxAnisotropy(),n?2:16)}catch{}e.appendChild(renderer.domElement);const o=new THREE.HemisphereLight(16777215,4906624,.88);o.position.set(0,160,0),scene.add(o);const a=new THREE.DirectionalLight(16776171,1.05);a.position.set(100,180,80),scene.add(a);const r=new THREE.Mesh(new THREE.PlaneGeometry(1600,620),new THREE.MeshLambertMaterial({color:2278750}));r.rotation.x=-Math.PI/2,r.position.set(0,-.25,-242),scene.add(r);const s=scene.children.length;if(createDistantMountainRanges(),createBrightCityRoadsTreesAndParks(),AES_LITE&&aesMergeStaticRange(s),aesBuildHalte(),createFluffyCloudsWithSoftShadows(),createSmartClosedLoopTrafficAndDrones(),createWideOceanDockAndDistantVictoryIsland(),AES_LITE&&ISL.group){const i=[].concat(ISL.swings,ISL.seesaw,ISL.flames,ISL.beam,ISL.foam,ISL.buoys,ISL.koi,ISL.butterflies,ISL.ripples);(ISL.kites||[]).forEach(l=>{i.push(l.g,l.line),(l.tail||[]).forEach(m=>i.push(m))}),aesMergeStaticTree(ISL.group,i)}createGuidingArrowSystem(),cityBuildingsGroup=new THREE.Group,scene.add(cityBuildingsGroup),window.addEventListener("keydown",i=>{initAudioEngine();const l=i.key.toLowerCase();(l==="w"||l==="arrowup")&&(moveKeys.up=!0),(l==="s"||l==="arrowdown")&&(moveKeys.down=!0),(l==="a"||l==="arrowleft")&&(moveKeys.left=!0),(l==="d"||l==="arrowright")&&(moveKeys.right=!0)}),window.addEventListener("keyup",i=>{const l=i.key.toLowerCase();(l==="w"||l==="arrowup")&&(moveKeys.up=!1),(l==="s"||l==="arrowdown")&&(moveKeys.down=!1),(l==="a"||l==="arrowleft")&&(moveKeys.left=!1),(l==="d"||l==="arrowright")&&(moveKeys.right=!1)}),window.addEventListener("resize",()=>{camera.aspect=window.innerWidth/window.innerHeight,camera.updateProjectionMatrix(),renderer.setSize(window.innerWidth,window.innerHeight)}),animate3D()}function createDistantMountainRanges(){const e=new THREE.Group,t=new THREE.MeshLambertMaterial({color:1409085}),n=new THREE.MeshLambertMaterial({color:1467700}),o=new THREE.MeshLambertMaterial({color:16317180});for(let a=0;a<36;a++){const r=Math.PI*.85+a/35*Math.PI*1.3,s=390+a%3*38,i=75+a%5*26,l=52+a%4*16,m=new THREE.Group;m.position.set(Math.cos(r)*s,0,Math.sin(r)*s-80);const d=new THREE.Mesh(new THREE.ConeGeometry(l,i,7),a%2===0?t:n);if(d.position.y=i/2-2,m.add(d),i>=90){const w=new THREE.Mesh(new THREE.ConeGeometry(l*.33,i*.32,7),o);w.position.y=i-i*.16-1.5,m.add(w)}e.add(m)}scene.add(e)}function createBrightCityRoadsTreesAndParks(){const e=new THREE.MeshLambertMaterial({color:3359061}),t=new THREE.MeshLambertMaterial({color:3359061,polygonOffset:!0,polygonOffsetFactor:-1,polygonOffsetUnits:-1}),n=new THREE.MeshLambertMaterial({color:9741240}),o=new THREE.MeshLambertMaterial({color:14870768});[-168,-84,0,84,168].forEach(l=>{const m=l===0,d=-272,w=m?60:44,p=w-d,u=(d+w)/2,H=new THREE.Mesh(new THREE.BoxGeometry(22,.16,p+4),n);H.position.set(l,-.1,u),scene.add(H);const M=new THREE.Mesh(new THREE.BoxGeometry(16,.18,p),e);M.position.set(l,-.04,u),scene.add(M);for(let E=-260;E<=w-4;E+=12){const g=new THREE.Mesh(new THREE.BoxGeometry(.45,.08,4.5),o);g.position.set(l,.08,E),scene.add(g)}}),[36,-24,-84,-144,-204,-264].forEach(l=>{const m=new THREE.Mesh(new THREE.BoxGeometry(358,.16,22),n);m.position.set(0,-.11,l),scene.add(m);const d=new THREE.Mesh(new THREE.BoxGeometry(352,.18,16),t);d.position.set(0,-.02,l),scene.add(d);for(let w=-160;w<=160;w+=12){if(Math.abs(w%84)<9)continue;const p=new THREE.Mesh(new THREE.BoxGeometry(4.5,.08,.45),o);p.position.set(w,.1,l),scene.add(p)}});const a=new THREE.Mesh(new THREE.CylinderGeometry(7.5,7.5,.22,32),n);a.position.set(0,-.02,52),scene.add(a);const r=new THREE.Mesh(new THREE.CylinderGeometry(3.8,4.4,.9,24),new THREE.MeshLambertMaterial({color:16317180}));r.position.set(0,.45,52),scene.add(r);const s=new THREE.Mesh(new THREE.CylinderGeometry(3.2,3.2,.98,24),new THREE.MeshBasicMaterial({color:3718648}));s.position.set(0,.52,52),scene.add(s),solidCircleObstacles.push({x:0,z:52,r:4.4});const i=[];[-150,-102,-66,-18,18,66,102,150].forEach(l=>{[22,-8,-38,-68,-98,-128,-158,-188,-218,-248].forEach(m=>{i.push([l,m])})}),[-130,-105,-75,-50,-25,25,50,75,105,130].forEach(l=>{i.push([l,54])}),i.forEach(([l,m],d)=>{const w=createLushTreeMesh(d);w.position.set(l,0,m),scene.add(w),solidCircleObstacles.push({x:l,z:m,r:1.25})})}function createFluffyCloudsWithSoftShadows(){cloudsList=[];const e=new THREE.MeshLambertMaterial({color:16777215}),t=createSoftShadowTexture(),n=!1;for(let o=0;o<22;o++){const a=new THREE.Group,r=3+o%3;for(let w=0;w<r;w++){const p=new THREE.Mesh(new THREE.SphereGeometry(5+Math.random()*2.8,12,12),e);p.position.set(w*4.5-5,(Math.random()-.5)*1.6,(Math.random()-.5)*2.5),p.scale.y=.65,a.add(p)}const s=(Math.random()-.5)*440,i=62+Math.random()*24,l=(Math.random()-.5)*380-60;a.position.set(s,i,l);const m=new THREE.MeshBasicMaterial({map:t,transparent:!0,depthWrite:!1}),d=new THREE.Mesh(new THREE.PlaneGeometry(44,28),m);d.rotation.x=-Math.PI/2,d.position.set(s+10,.16+o*.002,l+8),d.visible=n,scene.add(d),a.userData={speed:2.4+Math.random()*2.2,groundShadow:d},scene.add(a),cloudsList.push(a)}}function createWheelAssembly(e=.42,t=.28){const n=new THREE.Group,o=new THREE.MeshLambertMaterial({color:988970}),a=new THREE.MeshPhongMaterial({color:13358561,shininess:120,specular:6710886}),r=new THREE.MeshLambertMaterial({color:1976635}),s=new THREE.Mesh(new THREE.CylinderGeometry(e,e,t,20),o);s.rotation.z=Math.PI/2,n.add(s);const i=new THREE.Mesh(new THREE.CylinderGeometry(e*.66,e*.66,t+.03,18),r);i.rotation.z=Math.PI/2,n.add(i);for(let m=0;m<5;m++){const d=new THREE.Mesh(new THREE.BoxGeometry(t+.05,e*.1,e*1.1),a);d.rotation.x=m/5*Math.PI,n.add(d)}const l=new THREE.Mesh(new THREE.CylinderGeometry(e*.2,e*.2,t+.06,12),a);return l.rotation.z=Math.PI/2,n.add(l),AES_LITE&&aesBakeDirect(n),n}function createRealisticVehicleMesh(e,t,n=!1){const o=new THREE.Group,a=new THREE.MeshPhongMaterial({color:t,shininess:60,specular:2763306}),r=new THREE.MeshPhongMaterial({color:997983,shininess:200,specular:16777215,transparent:!0,opacity:.88}),s=new THREE.MeshLambertMaterial({color:3359061}),i=new THREE.MeshLambertMaterial({color:988970}),l=new THREE.MeshPhongMaterial({color:14870768,shininess:150,specular:8947848}),m=new THREE.MeshBasicMaterial({color:16775106}),d=new THREE.MeshBasicMaterial({color:15680580}),w=new THREE.MeshLambertMaterial({color:16317180}),p=[],u=(E,g,f,R,y,c,h,x)=>{const T=new THREE.Mesh(new THREE.BoxGeometry(E,g,f),R);return T.position.set(y,c,h),x&&(T.rotation.x=x),o.add(T),T},H=(E,g)=>{const f=new THREE.Shape;g.forEach((T,k)=>{k?f.lineTo(T[0],T[1]):f.moveTo(T[0],T[1])});const R=(T,k,G)=>{const v=new THREE.ExtrudeGeometry(k,{depth:T,bevelEnabled:!1});v.translate(0,0,-T/2);const I=new THREE.Mesh(v,G);return I.rotation.y=-Math.PI/2,o.add(I),I};R(E,f,a);let y=0,c=0;g.forEach(T=>{y+=T[0],c+=T[1]}),y/=g.length,c/=g.length;const h=new THREE.Shape;g.forEach((T,k)=>{const G=y+(T[0]-y)*.82,v=c+(T[1]-c)*.6+.02;k?h.lineTo(G,v):h.moveTo(G,v)}),R(E+.04,h,r);const x=(T,k)=>{const G=k[0]-T[0],v=k[1]-T[1],I=Math.hypot(G,v),b=Math.atan2(G,v),S=G<0?1:-1,B=u(E*.88,I*.86,.03,r,(T[0]+k[0])/2-S*Math.sin(b)*0,(T[1]+k[1])/2,(T[0]+k[0])/2,b);return B.position.set(0,(T[1]+k[1])/2+S*-Math.sin(b)*.03,(T[0]+k[0])/2+S*Math.cos(b)*.03),B};x(g[0],g[1]),x(g[g.length-1],g[g.length-2])},M=(E,g,f,R)=>{[-1,1].forEach(y=>{u(.5,.18,.06,m,y*(E*.68),f+.16,g+.01),u(.5,.16,.06,d,y*(E*.68),f+.16,-g-.01),u(.12,.1,.22,a,y*(E+.1),R-.04,.5),u(.03,.5,.03,i,y*(E+.005),f-.02,.45),u(.03,.5,.03,i,y*(E+.005),f-.02,-.65),u(.03,.04,.22,l,y*(E+.01),f+.14,-.1)}),u(.9,.22,.05,i,0,f+.1,g+.005),u(.9,.03,.06,l,0,f+.1,g+.015),u(E*2+.06,.2,.14,s,0,f-.22,g+.05),u(E*2+.06,.2,.14,s,0,f-.22,-g-.05),u(.42,.14,.04,w,0,f-.05,-g-.03)};return e==="sedan"?(u(2,.68,4.3,a,0,.66,0),H(1.76,[[1.15,1],[.55,1.59],[-.75,1.59],[-1.35,1]]),M(1,2.15,.66,1),n&&(u(.75,.24,.32,m,0,1.72,-.1),u(1.7,.05,.12,i,0,1.6,.3)),[[-.98,1.32],[.98,1.32],[-.98,-1.32],[.98,-1.32]].forEach(([E,g])=>{const f=createWheelAssembly(.4,.26);f.position.set(E,.4,g),o.add(f),p.push(f)})):e==="suv"?(u(2.15,.82,4.5,a,0,.8,0),H(1.95,[[1.5,1.21],[1,1.9],[-1.5,1.9],[-1.8,1.21]]),M(1.075,2.25,.8,1.21),u(1.6,.05,2,i,0,1.93,-.25),[[-1.06,1.42],[1.06,1.42],[-1.06,-1.38],[1.06,-1.38]].forEach(([E,g])=>{const f=createWheelAssembly(.48,.32);f.position.set(E,.48,g),o.add(f),p.push(f)})):e==="bus"?(u(2.45,2.15,6.8,a,0,1.55,0),u(2.49,.26,6.82,w,0,1.15,0),u(2.15,.95,.05,r,0,1.95,3.42),u(1.5,.22,.05,new THREE.MeshBasicMaterial({color:16498468}),0,2.45,3.42),u(2,.8,.05,r,0,1.95,-3.42),[-1,1].forEach(E=>{[2.3,1.2,.1,-1,-2.1].forEach(g=>u(.05,.8,.95,r,E*1.24,1.95,g)),u(.4,.2,.06,m,E*.85,.75,3.43),u(.4,.2,.06,d,E*.85,.75,-3.43),u(.12,.1,.25,i,E*1.35,2.2,3.1)}),u(2.5,.22,.16,s,0,.55,3.45),u(2.5,.22,.16,s,0,.55,-3.45),u(1.4,.16,2.2,w,0,2.7,-.4),[[-1.2,2.1],[1.2,2.1],[-1.2,-1.9],[1.2,-1.9]].forEach(([E,g])=>{const f=createWheelAssembly(.52,.34);f.position.set(E,.52,g),o.add(f),p.push(f)})):(u(2.1,.35,5.8,s,0,.62,0),u(2.2,1.65,1.85,a,0,1.55,1.9),u(2.42,2.35,3.85,w,0,1.95,-1.05),u(1.9,.78,.05,r,0,1.95,2.84),[-1,1].forEach(E=>{u(.05,.7,1.05,r,E*1.11,1.95,1.95),u(.45,.22,.06,m,E*.8,1.15,2.85),u(.4,.2,.06,d,E*.9,.95,-2.99),u(.12,.3,.12,i,E*1.3,2.05,2.55)}),u(1.2,.5,.06,i,0,1,2.85),u(1.3,.04,.07,l,0,1,2.88),u(2.2,.22,.16,s,0,.55,2.92),u(2.3,.2,.14,s,0,.55,-2.95),[[-1.12,1.95],[1.12,1.95],[-1.12,-1.8],[1.12,-1.8]].forEach(([E,g])=>{const f=createWheelAssembly(.5,.32);f.position.set(E,.5,g),o.add(f),p.push(f)})),o.scale.set(1.55,1.55,1.55),o.userData.wheels=p,AES_LITE&&aesBakeDirect(o),o}function createSmartClosedLoopTrafficAndDrones(){npcCarsList=[];const e=[{x:-164.2,z:32.2},{x:164.2,z:32.2},{x:164.2,z:-260.2},{x:-164.2,z:-260.2}],t=[{x:-87.8,z:39.8},{x:-87.8,z:-147.8},{x:87.8,z:-147.8},{x:87.8,z:39.8}],n=[{x:-80.2,z:-20.2},{x:-3.8,z:-20.2},{x:-3.8,z:-87.8},{x:-80.2,z:-87.8}],o=[{x:3.8,z:-20.2},{x:80.2,z:-20.2},{x:80.2,z:-87.8},{x:3.8,z:-87.8}],a=[{x:-171.8,z:-80.2},{x:171.8,z:-80.2},{x:171.8,z:-267.8},{x:-171.8,z:-267.8}];[{vType:"bus",color:16436245,isTaxi:!1,baseSpeed:13.5,hitRadius:4.8,seg:0,t:.15,wp:e},{vType:"truck",color:165063,isTaxi:!1,baseSpeed:13.5,hitRadius:4.5,seg:2,t:.25,wp:e},{vType:"sedan",color:3900150,isTaxi:!1,baseSpeed:14,hitRadius:3.4,seg:1,t:.5,wp:e},{vType:"suv",color:15680580,isTaxi:!1,baseSpeed:14.2,hitRadius:3.6,seg:0,t:.2,wp:t},{vType:"sedan",color:16096779,isTaxi:!0,baseSpeed:14.2,hitRadius:3.4,seg:2,t:.3,wp:t},{vType:"sedan",color:1096065,isTaxi:!1,baseSpeed:13.8,hitRadius:3.4,seg:0,t:.3,wp:n},{vType:"suv",color:9133302,isTaxi:!1,baseSpeed:13.8,hitRadius:3.6,seg:1,t:.4,wp:o},{vType:"truck",color:16347926,isTaxi:!1,baseSpeed:14,hitRadius:4.5,seg:0,t:.25,wp:a},{vType:"bus",color:889992,isTaxi:!1,baseSpeed:14,hitRadius:4.8,seg:2,t:.35,wp:a}].forEach((s,i)=>{const l=createRealisticVehicleMesh(s.vType,s.color,s.isTaxi),m=s.wp[s.seg],d=s.wp[(s.seg+1)%s.wp.length];l.position.set(THREE.MathUtils.lerp(m.x,d.x,s.t),.08,THREE.MathUtils.lerp(m.z,d.z,s.t)),l.rotation.y=Math.atan2(d.x-m.x,d.z-m.z),l.userData={...l.userData,id:i,waypoints:s.wp,segIndex:s.seg,baseSpeed:s.baseSpeed,currentSpeed:s.baseSpeed,hitRadius:s.hitRadius},scene.add(l),npcCarsList.push(l)}),dronesList=[];for(let s=0;s<6;s++){const i=new THREE.Group,l=new THREE.Mesh(new THREE.SphereGeometry(1.8,16,16),new THREE.MeshLambertMaterial({color:3718648}));l.position.y=.4,i.add(l);const m=new THREE.Mesh(new THREE.CylinderGeometry(3.2,1.8,.7,20),new THREE.MeshLambertMaterial({color:14870768}));i.add(m);const d=new THREE.Mesh(new THREE.TorusGeometry(3.6,.28,10,28),new THREE.MeshBasicMaterial({color:16436245}));d.rotation.x=Math.PI/2,i.add(d);const w=new THREE.Mesh(new THREE.SphereGeometry(.9,10,10),new THREE.MeshBasicMaterial({color:4906624}));w.position.y=-.45,i.add(w),i.userData={angle:s*(Math.PI/3),radius:52+s*18,height:36+s%3*6,speed:.32+s%3*.08},scene.add(i),dronesList.push(i)}}function updateSmartTrafficSystem(e){npcCarsList.forEach((t,n)=>{const o=t.userData,a=(o.segIndex+1)%o.waypoints.length,r=o.waypoints[a].x,s=o.waypoints[a].z,i=r-t.position.x,l=s-t.position.z,m=Math.hypot(i,l),d=m>.001?i/m:0,w=m>.001?l/m:1;let p=!1;for(let E=0;E<npcCarsList.length;E++){if(n===E)continue;const g=npcCarsList[E],f=g.position.x-t.position.x,R=g.position.z-t.position.z,y=Math.hypot(f,R),c=(o.hitRadius||3.6)+(g.userData.hitRadius||3.6)+5;if(y<c&&f*d+R*w>.7&&n>E){p=!0;break}}o.currentSpeed=THREE.MathUtils.lerp(o.currentSpeed,p?0:o.baseSpeed,e*7);const u=o.currentSpeed*e;m<=Math.max(.55,u)?(t.position.set(r,.08,s),o.segIndex=a):(t.position.x+=d*u,t.position.z+=w*u);let M=Math.atan2(d,w)-t.rotation.y;for(;M>Math.PI;)M-=Math.PI*2;for(;M<-Math.PI;)M+=Math.PI*2;t.rotation.y+=M*Math.min(1,e*11),o.wheels&&o.wheels.forEach(E=>{E.rotation.x+=u*1.6})})}function createWideOceanDockAndDistantVictoryIsland(){const e=new THREE.Mesh(new THREE.PlaneGeometry(1600,360),new THREE.MeshLambertMaterial({color:165063}));e.rotation.x=-Math.PI/2,e.position.set(0,-.05,248),scene.add(e);const t=new THREE.Mesh(new THREE.BoxGeometry(420,1.2,1.5),new THREE.MeshLambertMaterial({color:9741240}));t.position.set(0,.6,67.5),scene.add(t);const n=new THREE.Mesh(new THREE.BoxGeometry(24,1.1,14),new THREE.MeshLambertMaterial({color:14251782}));n.position.set(DOCK_TARGET.x,.55,DOCK_TARGET.z+3),scene.add(n);const o=createTextLabelSprite("⚓ DERMAGA KEBERANGKATAN SPEEDBOAT","#f59e0b",1.55);o.position.set(DOCK_TARGET.x,7.5,DOCK_TARGET.z),scene.add(o);const a=new THREE.Mesh(new THREE.BoxGeometry(2.2,.12,55),new THREE.MeshBasicMaterial({color:14870768}));a.position.set(BOAT_START_POS.x,.14,BOAT_START_POS.z),scene.add(a);const r=new THREE.Mesh(new THREE.BoxGeometry(3.8,.15,60),new THREE.MeshBasicMaterial({color:16436245}));r.position.set(VICTORY_ISLAND.finishLineX,.16,VICTORY_ISLAND.finishLineZ),scene.add(r),buildVictoryIslandWorld()}function _islandPlankTex(e,t){try{const n=document.createElement("canvas");n.width=n.height=128;const o=n.getContext("2d");o.fillStyle="#b9824a",o.fillRect(0,0,128,128);for(let r=0;r<4;r++)o.fillStyle=r%2?"rgba(120,70,30,0.35)":"rgba(230,180,120,0.18)",o.fillRect(0,r*32,128,32),o.fillStyle="rgba(60,30,10,0.7)",o.fillRect(0,r*32,128,3);const a=new THREE.CanvasTexture(n);return a.wrapS=a.wrapT=THREE.RepeatWrapping,a.repeat.set(e,t),a}catch{return null}}function _islandGradTex(e){try{const t=document.createElement("canvas");t.width=t.height=256;const n=t.getContext("2d"),o=n.createRadialGradient(128,128,0,128,128,128);return e.forEach(a=>o.addColorStop(a[0],a[1])),n.fillStyle=o,n.fillRect(0,0,256,256),new THREE.CanvasTexture(t)}catch{return null}}function buildVictoryIslandWorld(){const e=VICTORY_ISLAND,t=new THREE.Group;t.position.set(e.centerX,0,e.centerZ),ISL.group=t;const n=M=>new THREE.MeshLambertMaterial({color:M}),o=M=>new THREE.MeshBasicMaterial({color:M}),a=islandHeight;let r=20261016;const s=()=>(r=r*16807%2147483647)/2147483647,i=(M,E,g,f,R,y)=>{const c=new THREE.Mesh(M,E);return c.position.set(g,f,R),(y||t).add(c),c},l=(M,E,g)=>solidCircleObstacles.push({x:e.centerX+M,z:e.centerZ+E,r:g}),m=!1,d=(M,E,g,f,R,y)=>{if(!m)return null;const c=createTextLabelSprite(M,E,y||.95);return c.position.set(g,f,R),t.add(c),c};{const g=new THREE.PlaneGeometry(124,124,110,110);g.rotateX(-Math.PI/2);const f=g.attributes.position,R=new Float32Array(f.count*3),y=new THREE.Color(16639626),c=new THREE.Color(14268531),h=new THREE.Color(15981739),x=new THREE.Color(4906624),T=new THREE.Color(2278750),k=new THREE.Color(10259036),G=new THREE.Color,v=new THREE.Color;for(let I=0;I<f.count;I++){const b=f.getX(I),S=f.getZ(I),B=Math.hypot(b,S);f.setY(I,islandHeight(b,S)),B<36?v.copy(y):B<40?v.copy(y).lerp(c,(B-36)/4):v.copy(c).lerp(h,_sstep(40,47,B));const C=.5+.5*Math.sin(b*.9)*Math.cos(S*.8+b*.2);G.copy(x).lerp(T,C),v.lerp(G,1-_sstep(25.5,30,B));const D=Math.hypot(b-ISLAND_POND.x,S-ISLAND_POND.z);D<5.4&&v.lerp(k,(1-D/5.4)*.85),R[I*3]=v.r,R[I*3+1]=v.g,R[I*3+2]=v.b}g.setAttribute("color",new THREE.BufferAttribute(R,3)),g.computeVertexNormals(),t.add(new THREE.Mesh(g,new THREE.MeshLambertMaterial({vertexColors:!0})))}{const M=_islandGradTex([[0,"rgba(110,231,215,0.78)"],[.66,"rgba(94,214,230,0.72)"],[.8,"rgba(56,189,248,0.55)"],[1,"rgba(2,132,199,0)"]]),E=i(new THREE.CircleGeometry(62,72),new THREE.MeshBasicMaterial({map:M,color:M?16777215:6220500,transparent:!0,depthWrite:!1,opacity:M?1:.5}),0,.32,0);E.rotation.x=-Math.PI/2,E.renderOrder=1,[[39.4,40.9,.36],[41.4,42.2,.36]].forEach((c,h)=>{const x=i(new THREE.RingGeometry(c[0],c[1],80),new THREE.MeshBasicMaterial({color:16777215,transparent:!0,opacity:.5,depthWrite:!1,side:THREE.DoubleSide}),0,c[2],0);x.rotation.x=-Math.PI/2,x.renderOrder=2,ISL.foam.push(x)});const g=i(new THREE.TorusGeometry(47.5,.07,6,180),o(16317180),0,.42,0);g.rotation.x=Math.PI/2;const f=new THREE.SphereGeometry(.5,12,10),R=n(15680580),y=n(16317180);for(let c=0;c<44;c++){const h=c/44*Math.PI*2,x=i(f,c%2?R:y,Math.cos(h)*47.5,.4,Math.sin(h)*47.5);x.userData.ph=c*.9,ISL.buoys.push(x)}[.7,2.3,3.9,5.5].forEach(c=>d("⛔ BATAS AMAN: main air hanya di pinggir pantai","#ef4444",Math.cos(c)*47.5,4.2,Math.sin(c)*47.5,1));for(let c=0;c<5;c++)ISL.ripples.push((()=>{const h=i(new THREE.RingGeometry(.4,.6,28),new THREE.MeshBasicMaterial({color:16777215,transparent:!0,opacity:0,depthWrite:!1,side:THREE.DoubleSide}),0,.37,0);return h.rotation.x=-Math.PI/2,h.visible=!1,h.renderOrder=3,h.userData.t=1,h})())}{const g=ISLAND_PIER.y,f=_islandPlankTex(5,4),R=i(new THREE.BoxGeometry(20,.3,16),new THREE.MeshLambertMaterial(f?{map:f}:{color:11817737}),-34,g-.15,-4),y=new THREE.CylinderGeometry(.28,.32,2,8),c=n(5978650);for(let z=0;z<6;z++)[-1,1].forEach(A=>i(y,c,-34-9.5+z*3.8,g-1,-4+A*7.6));for(let z=0;z<6;z++)[-1,1].forEach(A=>{i(new THREE.CylinderGeometry(.07,.07,1,6),c,-34-9.6+z*3.84,g+.5,-4+A*7.9)});[-1,1].forEach(z=>i(new THREE.BoxGeometry(19.4,.1,.1),n(16317180),-34,g+.95,-4+z*7.9));const h=_islandPlankTex(1,1),x=new THREE.MeshLambertMaterial(h?{map:h}:{color:12157514});for(let z=-26;z<-3;z+=1.5){const A=a(z,-3),$=a(z+1.5,-3),O=i(new THREE.BoxGeometry(1.56,.12,3),x,z+.75,(A+$)/2+.06,-3);O.rotation.z=Math.atan2($-A,1.5)}const T=[-24,-17,-10,-3.2];T.forEach(z=>{const A=a(z,-3);i(new THREE.CylinderGeometry(.1,.12,4.4,8),n(7877903),z,A+2.2,-4.9),i(new THREE.CylinderGeometry(.1,.12,4.4,8),n(7877903),z,A+2.2,-1.1)});const k=new THREE.Shape;k.moveTo(-.28,0),k.lineTo(.28,0),k.lineTo(0,-.55),k.closePath();const G=new THREE.ShapeGeometry(k),v=new THREE.MeshBasicMaterial({color:16777215,side:THREE.DoubleSide}),I=[15680580,16436245,2278750,3718648,11032055,16347926],b=(T.length-1)*2*8,S=new THREE.InstancedMesh(G,v,b);let B=0;const C=new THREE.Matrix4,D=new THREE.Color;[-4.9,-1.1].forEach(z=>{for(let A=0;A<T.length-1;A++)for(let $=0;$<8;$++){const O=($+.5)/8,j=T[A]+(T[A+1]-T[A])*O,X=a(T[A],-3)*(1-O)+a(T[A+1],-3)*O+4.2-Math.sin(O*Math.PI)*.55;C.makeRotationY(Math.PI/2*0).setPosition(j,X,z),S.setMatrixAt(B,C),S.setColorAt(B,D.setHex(I[(B+A)%I.length])),B++}}),S.frustumCulled=!1,t.add(S)}{const g=a(4,0)+.08,f=new THREE.Group;f.position.set(4,0,0),t.add(f),i(new THREE.CylinderGeometry(6.5,6.8,.8,8),n(9584654),0,g-.4,0,f);const R=n(7877903);for(let h=0;h<6;h++){const x=h/6*Math.PI*2+Math.PI/6;i(new THREE.CylinderGeometry(.28,.3,5.2,8),R,Math.cos(x)*5.2,g+2.6,Math.sin(x)*5.2,f);const T=i(new THREE.BoxGeometry(2.6,.18,.7),n(11817737),Math.cos(x+.52)*4.4,g+.55,Math.sin(x+.52)*4.4,f);T.rotation.y=-(x+.52)+Math.PI/2;const k=i(new THREE.SphereGeometry(.28,10,8),o(16639626),Math.cos(x)*4.6,g+4.4,Math.sin(x)*4.6,f);i(new THREE.CylinderGeometry(.02,.02,.8,4),n(3359061),Math.cos(x)*4.6,g+4.9,Math.sin(x)*4.6,f)}const y=i(new THREE.ConeGeometry(8.2,4.2,8),n(14251782),0,g+7.2,0,f),c=i(new THREE.TorusGeometry(7.6,.18,6,32),n(16436245),0,g+5.4,0,f);c.rotation.x=Math.PI/2,i(new THREE.CylinderGeometry(1,1,.9,12),n(9584654),0,g+.45,0,f),i(new THREE.CylinderGeometry(1.25,1.25,.1,12),n(16708551),0,g+.95,0,f),i(new THREE.CylinderGeometry(.28,.2,.4,8),n(15680580),.5,g+1.2,.3,f),i(new THREE.SphereGeometry(.3,8,6),n(8736014),-.5,g+1.15,-.2,f),d("🛖 Gazebo Santai","#f59e0b",4,10.6,0)}{const g=a(19,-6),f=new THREE.Group;f.position.set(19,g,-6),f.rotation.y=-Math.PI/2,t.add(f),i(new THREE.BoxGeometry(5.6,.25,4.6),n(11817737),0,.1,0,f),i(new THREE.BoxGeometry(5,3.2,.3),n(16708551),0,1.9,-1.9,f),[-1,1].forEach(R=>i(new THREE.BoxGeometry(.3,3.2,3.6),n(16639626),R*2.5,1.9,-.2,f)),i(new THREE.BoxGeometry(4.6,1,.8),n(9584654),0,.7,1.2,f),i(new THREE.BoxGeometry(4.8,.12,1),n(16569165),0,1.25,1.2,f);for(let R=0;R<8;R++){const y=i(new THREE.BoxGeometry(.72,.1,3),n(R%2?16317180:14427686),-2.5+R*.72+.36,3.7199999999999998,.45,f);y.rotation.x=-.24}for(let R=0;R<4;R++)i(new THREE.SphereGeometry(.22,8,6),n(8736014),-1.5+R*1,1.5,1.2,f);for(let R=0;R<3;R++)i(new THREE.CylinderGeometry(.34,.34,.1,10),n(14427686),-1.4+R*1.4,.78,3.2,f),i(new THREE.CylinderGeometry(.06,.06,.7,6),n(4674921),-1.4+R*1.4,.4,3.2,f);i(new THREE.CylinderGeometry(.6,.6,1.1,10),n(7877903),3.3,.65,-1,f),l(19,-6,3.2),d("🥥 Warung Kelapa","#fb7185",19,7,-6)}{const g=a(-13,-10),f=new THREE.IcosahedronGeometry(.42,0),R=n(9741240);for(let x=0;x<9;x++){const T=x/9*Math.PI*2,k=i(f,R,-13+Math.cos(T)*1.5,g+.2,-10+Math.sin(T)*1.5);k.scale.set(1,.7,1),k.rotation.y=x}const y=n(7877903);for(let x=0;x<3;x++){const T=i(new THREE.CylinderGeometry(.14,.16,1.7,7),y,-13,g+.3,-10);T.rotation.z=Math.PI/2-.25,T.rotation.y=x*1.05}[[.55,1.6,16347926],[.4,1.2,16498468],[.3,.8,16707722]].forEach((x,T)=>{const k=i(new THREE.ConeGeometry(x[0],x[1],8),o(x[2]),-13,g+.5+x[1]/2,-10);k.userData={ph:T*1.7,base:x[1]},ISL.flames.push(k)});const h=new THREE.CylinderGeometry(.42,.42,2,9);for(let x=0;x<6;x++){const T=x/6*Math.PI*2+.3,k=i(h,y,-13+Math.cos(T)*3.6,g+.42,-10+Math.sin(T)*3.6);k.rotation.z=Math.PI/2,k.rotation.y=-T}l(-13,-10,1.6),d("🔥 Api Unggun","#fb923c",-13,5.2,-10)}{const g=a(-10,15),f=n(14427686),R=new THREE.Group;R.position.set(-10,g,15),R.rotation.y=.4,t.add(R),[-2.8,2.8].forEach(S=>[-1,1].forEach(B=>{const C=i(new THREE.CylinderGeometry(.12,.12,4.2,8),f,S,1.9,B*1.1,R);C.rotation.x=-B*.28}));const y=i(new THREE.CylinderGeometry(.13,.13,6.2,8),f,0,3.75,0,R);y.rotation.z=Math.PI/2,[-1.1,1.1].forEach((S,B)=>{const C=new THREE.Group;C.position.set(S,3.7,0),R.add(C),[-.35,.35].forEach(D=>i(new THREE.CylinderGeometry(.02,.02,2.5,4),n(3359061),D,-1.25,0,C)),i(new THREE.BoxGeometry(.95,.1,.4),n(B?3718648:16436245),0,-2.5,0,C),C.userData.ph=B*1.4,ISL.swings.push(C)}),l(-10,15,2.4);const c=1,h=18.5,x=a(c,h),T=new THREE.Group;T.position.set(c,x,h),t.add(T);const k=i(new THREE.CylinderGeometry(.05,.6,.9,3),n(4674921),0,.45,0,T);k.rotation.z=Math.PI/2,k.rotation.y=Math.PI/2;const G=new THREE.Group;G.position.y=.9,T.add(G),i(new THREE.BoxGeometry(5.2,.14,.7),n(1483594),0,0,0,G),[-2.3,2.3].forEach(S=>i(new THREE.BoxGeometry(.2,.4,.1),n(16436245),S,.25,0,G)),ISL.seesaw=G,l(c,h,2);const v=-4,I=20,b=a(v,I);[[0,-1.6,3.4,.2],[0,1.6,3.4,.2],[-1.6,0,.2,3.4],[1.6,0,.2,3.4]].forEach(S=>i(new THREE.BoxGeometry(S[2],.3,S[3]),n(11817737),v+S[0],b+.15,I+S[1])),i(new THREE.BoxGeometry(3.1,.2,3.1),n(16639626),v,b+.12,I),i(new THREE.CylinderGeometry(.3,.22,.4,8),n(15680580),v+.5,b+.35,I+.4),d("🎠 Taman Bermain","#a78bfa",-5,7.4,17)}{const M=ISLAND_POND,E=i(new THREE.CircleGeometry(M.r,36),new THREE.MeshPhongMaterial({color:2282478,transparent:!0,opacity:.72,shininess:120,specular:16777215}),M.x,M.y,M.z);E.rotation.x=-Math.PI/2;const g=new THREE.CircleGeometry(.55,14),f=new THREE.MeshLambertMaterial({color:1409085,side:THREE.DoubleSide});for(let h=0;h<9;h++){const x=s()*6.28,T=.6+s()*2.7,k=i(g,f,M.x+Math.cos(x)*T,M.y+.03,M.z+Math.sin(x)*T);k.rotation.x=-Math.PI/2,k.scale.setScalar(.7+s()*.7)}for(let h=0;h<4;h++){const x=h*1.7+.4,T=1+h%2*1.3;i(new THREE.ConeGeometry(.28,.4,8),n(h%2?16361684:16642808),M.x+Math.cos(x)*T,M.y+.2,M.z+Math.sin(x)*T)}const R=[n(16347926),n(16317180),n(16498468),n(15680580)];for(let h=0;h<4;h++){const x=new THREE.Group;i(new THREE.SphereGeometry(.28,10,8),R[h],0,0,0,x).scale.set(.55,.4,1.3);const k=i(new THREE.ConeGeometry(.16,.35,5),R[h],0,0,-.42,x);k.rotation.x=-Math.PI/2,x.userData={r:1.2+h*.55,sp:.45+h*.12,a:h*1.6},t.add(x),ISL.koi.push(x)}const y=new THREE.IcosahedronGeometry(.5,0),c=n(9149360);for(let h=0;h<12;h++){const x=h/12*6.28+s()*.3,T=4.6+s()*.7,k=M.x+Math.cos(x)*T,G=M.z+Math.sin(x)*T,v=i(y,c,k,a(k,G)+.1,G);v.scale.set(.8+s()*.9,.5+s()*.5,.8+s()*.9),v.rotation.y=s()*3}d("🌸 Kolam & Taman Bunga","#f472b6",M.x,5.6,M.z)}{const M=[[4,0,9],[19,-6,4.5],[-13,-10,5],[-10,15,4],[1,18.5,4],[-4,20,3],[ISLAND_POND.x,ISLAND_POND.z,6],[2,-12,4.5],[0,-18.5,3.5]],E=(z,A,$)=>{if(Math.abs(A+3)<2.6&&z<-2&&z>-27)return!1;for(const O of M)if(Math.hypot(z-O[0],A-O[1])<O[2]+($||0))return!1;return!0},g=[[ISLAND_POND.x,ISLAND_POND.z,6.2,11.5,130],[-17,3,0,5.5,55],[11,-20,0,5.2,55]],f=new THREE.CylinderGeometry(.03,.04,.6,5);f.translate(0,.3,0);const R=new THREE.SphereGeometry(.17,7,6);R.translate(0,.66,0);const y=g.reduce((z,A)=>z+A[4],0),c=new THREE.InstancedMesh(f,n(1483594),y),h=new THREE.InstancedMesh(R,n(16777215),y),x=[16007006,16436245,16347926,11032055,15485081,16777215,6333946],T=new THREE.Matrix4,k=new THREE.Quaternion,G=new THREE.Vector3,v=new THREE.Vector3,I=new THREE.Color;let b=0;const S=[];g.forEach(z=>{S.push([z[0],z[1]]);for(let A=0;A<z[4];A++){let $,O,j=0;do{const P=s()*6.28,L=z[2]+s()*(z[3]-z[2]);$=z[0]+Math.cos(P)*L,O=z[1]+Math.sin(P)*L,j++}while((!E($,O,0)||Math.hypot($-ISLAND_POND.x,O-ISLAND_POND.z)<5.3)&&j<30);const X=.8+s()*.6;v.set($,a($,O),O),G.set(X,X,X),k.identity(),T.compose(v,k,G),c.setMatrixAt(b,T),h.setMatrixAt(b,T),h.setColorAt(b,I.setHex(x[Math.floor(s()*x.length)])),b++}}),c.frustumCulled=!1,h.frustumCulled=!1,t.add(c),t.add(h),ISL.flowerCenters=S;const B=new THREE.IcosahedronGeometry(1,1),C=new THREE.InstancedMesh(B,n(1483594),26);let D=0;for(;D<26;){const z=s()*6.28,A=8+s()*17,$=Math.cos(z)*A,O=Math.sin(z)*A;if(!E($,O,1.5)||Math.hypot($-ISLAND_POND.x,O-ISLAND_POND.z)<6)continue;const j=.7+s()*.8;v.set($,a($,O)+j*.55,O),G.set(j*1.2,j*.85,j*1.2),T.compose(v,k,G),C.setMatrixAt(D,T),C.setColorAt(D,I.setHex(s()>.5?1409085:2278750)),D++}C.frustumCulled=!1,t.add(C)}{const g=a(2,-12);let f=null;try{const c=document.createElement("canvas");c.width=c.height=128;const h=c.getContext("2d");h.fillStyle="#f8fafc",h.fillRect(0,0,128,128),h.fillStyle="#ef4444";for(let x=0;x<4;x++)h.fillRect(x*32,0,16,128),h.fillRect(0,x*32,128,16);f=new THREE.CanvasTexture(c)}catch{}const R=i(new THREE.BoxGeometry(4.4,.06,3.2),f?new THREE.MeshLambertMaterial({map:f}):n(15680580),2,g+.05,-12);R.rotation.y=.35;const y=i(new THREE.CylinderGeometry(.38,.32,.4,10),n(11817737),2+.5,g+.28,-12-.2);i(new THREE.TorusGeometry(.3,.03,6,14,Math.PI),n(9584654),2+.5,g+.48,-12-.2),i(new THREE.SphereGeometry(.18,8,6),n(15680580),2-.6,g+.22,-12+.3),i(new THREE.SphereGeometry(.18,8,6),n(16436245),2-.2,g+.22,-12+.55),i(new THREE.CylinderGeometry(.06,.06,4.2,6),n(16317180),2-1.9,g+2.1,-12+.8),i(new THREE.ConeGeometry(2.4,1,12),n(3718648),2-1.9,g+4.3,-12+.8),d("🧺 Area Piknik","#34d399",2,5.6,-12)}{const M=n(8736014),E=n(1409085),g=n(5978650),f=(y,c,h,x)=>{const T=a(y,c),k=new THREE.Group;k.position.set(y,T-.1,c),t.add(k);for(let I=0;I<5;I++){const b=i(new THREE.CylinderGeometry(.45-I*.05,.52-I*.05,1.6,8),M,I*.22*x,I*1.45+.8,0,k);b.rotation.z=-.12*x}const G=1.08*x,v=7.75;for(let I=0;I<7;I++){const b=I/7*Math.PI*2+h,S=i(new THREE.BoxGeometry(3.8,.15,.85),E,G+Math.cos(b)*1.8,v+.1,Math.sin(b)*1.8,k);S.rotation.y=-b,S.rotation.z=-.35}for(let I=0;I<3;I++)i(new THREE.SphereGeometry(.28,8,6),g,G+Math.cos(I*2.1)*.5,v-.3,Math.sin(I*2.1)*.5,k);l(y,c,1.1)};[[-12,-6],[-10,10],[0,-14],[2,14],[14,-8],[15,10],[22,0],[-20,-20],[-20,20],[10,22]].forEach(([y,c],h)=>f(y,c,h,1)),[[-3,-18],[3.2,-19],[-13,22],[-8.6,22.6],[31,-8],[-32,-2],[-3,-33],[34,12]].forEach(([y,c],h)=>f(y,c,h+10,h%2?-1:1));const R=(y,c,h,x,T)=>{const k=a(y,c)+2.9,G=a(h,x)+2.9,v=Math.hypot(h-y,x-c),I=Math.atan2(x-c,h-y),b=new THREE.PlaneGeometry(v*.84,1.3,14,1);b.rotateX(-Math.PI/2);const S=b.attributes.position;for(let C=0;C<S.count;C++){const D=S.getX(C)/(v*.84)+.5;S.setY(C,-Math.sin(D*Math.PI)*.75+(k*(1-D)+G*D)-(k+G)/2)}b.computeVertexNormals();const B=new THREE.Mesh(b,new THREE.MeshLambertMaterial({color:T,side:THREE.DoubleSide}));B.position.set((y+h)/2,(k+G)/2-.1,(c+x)/2),B.rotation.y=-I,t.add(B),d("😴 Hammock Santai","#fcd34d",(y+h)/2,6.2,(c+x)/2,.85)};R(-3,-18,3.2,-19,16478597),R(-13,22,-8.6,22.6,3718648)}{[[30,-12,16007006],[34,5,959977],[29,16,16096779],[-32,14,11032055],[-31,-17,1096065],[6,-33,15485081],[-8,33,1357990]].forEach(x=>{const T=x[0],k=x[1],G=a(T,k),v=new THREE.Group;v.position.set(T,G,k),t.add(v),i(new THREE.CylinderGeometry(.12,.15,4.2,8),n(16777215),0,2.1,0,v),i(new THREE.ConeGeometry(2.8,1.3,12),n(x[2]),0,4.2,0,v),i(new THREE.BoxGeometry(.9,.12,2.2),n(16707722),1.5,.25,.9,v);const I=i(new THREE.BoxGeometry(.9,.12,1),n(16707722),1.5,.55,-.25,v);I.rotation.x=.7,i(new THREE.BoxGeometry(1.1,.04,2),n(x[2]),-1.4,.06,.8,v),l(T,k,1.2)});const M=a(32,0);i(new THREE.BoxGeometry(7.2,.04,.12),o(16777215),32.5,M+.05,-5),i(new THREE.BoxGeometry(7.2,.04,.12),o(16777215),32.5,M+.05,5),i(new THREE.BoxGeometry(.12,.04,10),o(16777215),29,M+.05,0),i(new THREE.BoxGeometry(.12,.04,10),o(16777215),36,M+.05,0),[29,36].forEach(x=>{i(new THREE.CylinderGeometry(.09,.09,2.6,8),n(14870768),x,M+1.3,0),l(x,0,.3)});let E=null;try{const x=document.createElement("canvas");x.width=x.height=64;const T=x.getContext("2d");T.clearRect(0,0,64,64),T.strokeStyle="rgba(248,250,252,0.9)",T.lineWidth=3;for(let k=0;k<=64;k+=16)T.beginPath(),T.moveTo(k,0),T.lineTo(k,64),T.stroke(),T.beginPath(),T.moveTo(0,k),T.lineTo(64,k),T.stroke();E=new THREE.CanvasTexture(x),E.wrapS=E.wrapT=THREE.RepeatWrapping,E.repeat.set(7,1.5)}catch{}i(new THREE.PlaneGeometry(7,1.1),new THREE.MeshBasicMaterial({map:E,color:E?16777215:14870768,transparent:!0,side:THREE.DoubleSide,opacity:E?1:.4}),32.5,M+2.05,0),i(new THREE.SphereGeometry(.36,12,10),n(16436245),31,M+.36,3.3),d("🏐 Voli Pantai","#facc15",32.5,5.4,0);const g=27,f=-20,R=a(g,f),y=n(15254634);i(new THREE.BoxGeometry(2.6,.6,2.6),y,g,R+.3,f),[[-.9,-.9],[.9,-.9],[-.9,.9],[.9,.9]].forEach(x=>{i(new THREE.CylinderGeometry(.42,.5,1.1,10),y,g+x[0],R+1.1,f+x[1]),i(new THREE.ConeGeometry(.5,.6,10),n(14427686),g+x[0],R+1.95,f+x[1])}),i(new THREE.CylinderGeometry(.7,.8,1.7,10),y,g,R+1.45,f),i(new THREE.ConeGeometry(.85,.9,10),n(16436245),g,R+2.75,f),l(g,f,1.8),[[-28,19,16007006],[-27,21,3718648],[-29,17,16436245]].forEach((x,T)=>{const k=i(new THREE.SphereGeometry(1,12,10),n(x[2]),x[0],a(x[0],x[1])+1.7,x[1]);k.scale.set(.42,2.1,.11),k.rotation.z=(T-1)*.18,k.rotation.x=.1});const c=new THREE.IcosahedronGeometry(1,0),h=n(9741240);[[-30,24,2],[33,-20,2.2],[27,26,1.8],[-36,-14,1.7],[-12,36,1.6]].forEach(([x,T,k])=>{for(let G=0;G<3;G++){const v=i(c,h,x+(G-1)*k*.9,a(x,T)+k*.3,T+G%2*k*.6);v.scale.set(k*(.8+G*.15),k*(.55+G%2*.2),k*.8),v.rotation.y=G*1.3}l(x,T,k*1.2)})}{const g=a(14,-33.5),f=new THREE.Group;f.position.set(14,g,-33.5),t.add(f);const R=new THREE.IcosahedronGeometry(1,0);[[0,0,3.4],[2.8,1.5,2.2],[-2.6,1.2,2],[.6,-2.6,2.4]].forEach(c=>{i(R,n(8161952),c[0],c[2]*.2,c[1],f).scale.set(c[2],c[2]*.6,c[2])});for(let c=0;c<5;c++)i(new THREE.CylinderGeometry(1.5-c*.14,1.64-c*.14,2.8,16),n(c%2?14427686:16317180),0,2.2+c*2.8,0,f);i(new THREE.CylinderGeometry(2.1,1.7,.35,16),n(3359061),0,16.4,0,f),i(new THREE.CylinderGeometry(1.2,1.2,1.8,16),new THREE.MeshBasicMaterial({color:16707722}),0,17.4,0,f),i(new THREE.ConeGeometry(1.6,1.6,16),n(14427686),0,19.1,0,f);const y=new THREE.Group;y.position.y=17.4,f.add(y),[0,Math.PI].forEach(c=>{const h=new THREE.Mesh(new THREE.ConeGeometry(2.8,22,16,1,!0),new THREE.MeshBasicMaterial({color:16774064,transparent:!0,opacity:.2,depthWrite:!1,side:THREE.DoubleSide,blending:THREE.AdditiveBlending}));h.rotation.z=Math.PI/2,h.position.x=11;const x=new THREE.Group;x.rotation.y=c,x.add(h),y.add(x)}),ISL.beam=y,l(14,-33.5,3.2),d("🗼 Mercusuar","#fde047",14,23.5,-33.5)}{const M=[[-6,-24],[10,-23],[24,-9],[25,9],[-25,-8],[12,25]],E=[[15680580,16436245],[3718648,16317180],[11032055,16436245],[2278750,16707722],[16347926,16317180],[15485081,3718648]];M.forEach((g,f)=>{const R=a(g[0],g[1]);i(new THREE.CylinderGeometry(.06,.06,1.4,6),n(7877903),g[0],R+.7,g[1]),i(new THREE.CylinderGeometry(.22,.22,.2,10),n(E[f][0]),g[0],R+1.4,g[1]);const y=new THREE.Group,c=new THREE.Shape;c.moveTo(0,1.25),c.lineTo(.85,.3),c.lineTo(0,-1.05),c.lineTo(-.85,.3),c.closePath();const h=new THREE.Shape;h.moveTo(0,.7),h.lineTo(.46,.22),h.lineTo(0,-.55),h.lineTo(-.46,.22),h.closePath(),i(new THREE.ShapeGeometry(c),new THREE.MeshBasicMaterial({color:E[f][0],side:THREE.DoubleSide}),0,0,0,y),i(new THREE.ShapeGeometry(h),new THREE.MeshBasicMaterial({color:E[f][1],side:THREE.DoubleSide}),0,0,.01,y),i(new THREE.BoxGeometry(.04,2.3,.03),n(7877903),0,.1,.02,y),i(new THREE.BoxGeometry(1.7,.04,.03),n(7877903),0,.3,.02,y);const x=[];for(let G=0;G<8;G++)x.push(i(new THREE.BoxGeometry(.34,.2,.02),o(G%2?E[f][1]:E[f][0]),0,-1.3-G*.5,0,y));t.add(y);const T=new THREE.BufferGeometry;T.setAttribute("position",new THREE.BufferAttribute(new Float32Array(36),3));const k=new THREE.Line(T,new THREE.LineBasicMaterial({color:16317180}));k.frustumCulled=!1,t.add(k),ISL.kites.push({g:y,tail:x,line:k,ax:g[0],ay:R+1.45,az:g[1],ph:f*1.3,off:[9+f%3*3,14+f%4*2.5,f%2?4:-4]})}),d("🪁 Lapangan Layangan","#fb7185",10,9,-20,1)}{const M=[16486972,16020150,16436245,6333946];for(let E=0;E<10;E++){const g=ISL.flowerCenters[E%ISL.flowerCenters.length],f=new THREE.Group,R=()=>{const h=new THREE.Group,x=new THREE.Mesh(new THREE.PlaneGeometry(.34,.26),new THREE.MeshBasicMaterial({color:M[E%4],side:THREE.DoubleSide}));return x.rotation.x=-Math.PI/2,h.add(x),{p:h,w:x}},y=R(),c=R();y.w.position.x=-.17,c.w.position.x=.17,f.add(y.p),f.add(c.p),f.userData={cx:g[0],cz:g[1],r:2+E%4*1.2,ph:E*1.1,sp:.5+E%3*.15,L:y.p,R:c.p},t.add(f),ISL.butterflies.push(f)}}scene.add(t),islandBirdsList=[];const w=new THREE.MeshLambertMaterial({color:16317180}),p=new THREE.MeshBasicMaterial({color:16777215,side:THREE.DoubleSide}),u=new THREE.MeshBasicMaterial({color:3359061,side:THREE.DoubleSide}),H=n(16096779);for(let M=0;M<18;M++){const E=new THREE.Group,g=new THREE.Mesh(new THREE.SphereGeometry(.28,10,8),w);g.scale.set(.8,.75,1.9),E.add(g);const f=new THREE.Mesh(new THREE.SphereGeometry(.17,8,6),w);f.position.set(0,.07,.5),E.add(f);const R=new THREE.Mesh(new THREE.ConeGeometry(.06,.25,6),H);R.rotation.x=Math.PI/2,R.position.set(0,.04,.7),E.add(R);const y=new THREE.Mesh(new THREE.PlaneGeometry(.3,.35),p);y.rotation.x=-Math.PI/2,y.position.set(0,0,-.62),E.add(y);const c=k=>{const G=new THREE.Group;G.position.set(k*.18,.05,.05);const v=new THREE.Mesh(new THREE.PlaneGeometry(1.15,.5),p);v.rotation.x=-Math.PI/2,v.position.x=k*.58,G.add(v);const I=new THREE.Mesh(new THREE.PlaneGeometry(.3,.38),u);return I.rotation.x=-Math.PI/2,I.position.x=k*1.2,G.add(I),E.add(G),G},h=c(-1),x=c(1),T=12+M%6*7.5;E.scale.setScalar(1.25),E.userData={leftWing:h,rightWing:x,angle:M/18*Math.PI*2,radius:T,height:9+M%5*4.5,speed:(.5+M%3*.12)*(20/T)+.1,flapOffset:M*1.3},AES_LITE&&aesBakeDirect(E),scene.add(E),islandBirdsList.push(E)}}function updateIslandLife(e,t){if(!ISL.group)return;ISL.swings.forEach(o=>{o.rotation.x=Math.sin(e*1.7+o.userData.ph)*.55}),ISL.seesaw&&(ISL.seesaw.rotation.z=Math.sin(e*1.3)*.2),ISL.flames.forEach(o=>{const a=.85+.25*Math.sin(e*11+o.userData.ph)+.1*Math.sin(e*23+o.userData.ph);o.scale.set(1+.1*Math.sin(e*9+o.userData.ph),a,1+.1*Math.cos(e*8+o.userData.ph)),o.rotation.y=e*2+o.userData.ph}),ISL.beam&&(ISL.beam.rotation.y=e*.9),ISL.foam.forEach((o,a)=>{o.material.opacity=.32+.22*Math.sin(e*1.4+a*1.8),o.scale.setScalar(1+.006*Math.sin(e*1.4+a*1.8))}),ISL.buoys.forEach(o=>{o.position.y=.4+Math.sin(e*1.8+o.userData.ph)*.07}),ISL.koi.forEach(o=>{const a=o.userData,r=a.a+e*a.sp;o.position.set(ISLAND_POND.x+Math.cos(r)*a.r,ISLAND_POND.y-.12,ISLAND_POND.z+Math.sin(r)*a.r),o.rotation.y=-r+Math.PI}),ISL.butterflies.forEach(o=>{const a=o.userData,r=e*a.sp+a.ph;o.position.set(a.cx+Math.cos(r)*a.r,islandHeight(a.cx+Math.cos(r)*a.r,a.cz+Math.sin(r)*a.r)+1.5+Math.sin(e*2+a.ph)*.5,a.cz+Math.sin(r)*a.r),o.rotation.y=-r;const s=Math.sin(e*22+a.ph)*.9;a.L.rotation.z=s,a.R.rotation.z=-s}),ISL.kites.forEach(o=>{const a=o.ph,r=o.ax+o.off[0]+Math.sin(e*.7+a)*2.2,s=o.ay+o.off[1]+Math.sin(e*1.1+a*2)*1.2,i=o.az+o.off[2]+Math.sin(e*.5+a)*3;o.g.position.set(r,s,i),o.g.rotation.set(.45,Math.atan2(o.ax-r,o.az-i)+Math.PI,Math.sin(e*1.6+a)*.22),o.tail.forEach((d,w)=>{d.position.x=Math.sin(e*3.2-w*.7+a)*.12*(w+1)*.55,d.rotation.z=Math.cos(e*3.2-w*.7+a)*.5});const l=o.line.geometry.attributes.position.array,m=12;for(let d=0;d<m;d++){const w=d/(m-1);l[d*3]=o.ax+(r-o.ax)*w,l[d*3+1]=o.ay+(s-o.ay)*w-Math.sin(w*Math.PI)*1.4,l[d*3+2]=o.az+(i-o.az)*w}o.line.geometry.attributes.position.needsUpdate=!0});const n=VICTORY_ISLAND;if(myPlayer&&myPlayer.finishedRace&&(gamePhase==="race"||gamePhase==="reflection")){const o=myPlayer.x-n.centerX,a=myPlayer.z-n.centerZ,r=Math.hypot(o,a),s=Math.hypot(o-ISL.lx,a-ISL.lz)>.02;if(r>ISLAND_SHORE_R-.5&&s&&(ISL.rippleT-=t,ISL.rippleT<=0)){ISL.rippleT=.28;const i=ISL.ripples.find(l=>!l.visible);i&&(i.visible=!0,i.userData.t=0,i.position.set(o,.38,a))}ISL.lx=o,ISL.lz=a}ISL.ripples.forEach(o=>{if(!o.visible)return;o.userData.t+=t*1.4;const a=o.userData.t;if(a>=1){o.visible=!1;return}o.scale.setScalar(1+a*3.2),o.material.opacity=.6*(1-a)})}function createGuidingArrowSystem(){overheadArrowGroup=new THREE.Group;const e=new THREE.Mesh(new THREE.ConeGeometry(.95,2.2,8),new THREE.MeshBasicMaterial({color:16707722}));e.rotation.x=Math.PI/2,overheadArrowGroup.add(e),overheadArrowGroup.visible=!1,scene.add(overheadArrowGroup)}function setArrowGuideVisibility(e){overheadArrowGroup&&(overheadArrowGroup.visible=e)}let _doorWoodTex=null;function createDoorWoodTexture(){if(_doorWoodTex)return _doorWoodTex;try{const e=document.createElement("canvas");e.width=256,e.height=340;const t=e.getContext("2d");t.fillStyle="#8b5a2b",t.fillRect(0,0,256,340);for(let n=0;n<80;n++){const o=Math.random()*256;t.strokeStyle=n%2?"rgba(60,30,10,0.22)":"rgba(220,170,110,0.16)",t.lineWidth=1+Math.random()*2,t.beginPath(),t.moveTo(o,0),t.bezierCurveTo(o+8,110,o-8,230,o+4,340),t.stroke()}return _doorWoodTex=new THREE.CanvasTexture(e),_doorWoodTex}catch{return null}}function buildRealDoor(e,t){const n=new THREE.Group;n.position.set(0,0,7.1);const o=f=>new THREE.MeshLambertMaterial({color:f}),a=(f,R)=>new THREE.MeshPhongMaterial({color:f,shininess:R||90,specular:16777215}),r=createDoorWoodTexture(),s=r?new THREE.MeshLambertMaterial({map:r}):o(9132587),i=o(11104314),l=o(5978650),m=o(15857145),d=a(16436245,160),w=a(14870768,220),p=new THREE.MeshPhongMaterial({color:9684477,transparent:!0,opacity:.55,shininess:200,specular:16777215}),u=(f,R,y,c,h,x,T,k)=>{const G=new THREE.Mesh(new THREE.BoxGeometry(f,R,y),c);return G.position.set(h,x,T),k&&(G.rotation.x=k),n.add(G),G},H=(f,R,y,c,h,x,T,k)=>{const G=new THREE.Mesh(new THREE.CylinderGeometry(f,f,R,14),y);return G.position.set(c,h,x),T&&(G.rotation.x=T),k&&(G.rotation.z=k),n.add(G),G};u(3.3,4.2,.8,o(1976635),0,2.1,0),[-1.8,1.8].forEach(f=>u(.6,4.6,1,m,f,2.3,.1)),u(4.2,.57,1,m,0,4.315,.1),u(4.6,.16,1.15,t,0,4.68,.1),u(3,.1,1,o(9741240),0,.14,.1);const M=[l,l,l,l,s,s],E=new THREE.Mesh(new THREE.BoxGeometry(3,3.9,.16),M);E.position.set(0,2.08,.38),n.add(E);const g=.38+.08;return[-.72,.72].forEach(f=>{u(1.2,1.75,.05,i,f,1.38,g+.025),u(1,1.55,.04,s,f,1.38,g+.06)}),u(2.3,1.3,.06,l,0,3.15,g+.03),u(1.95,1,.03,p,0,3.15,g+.07),u(.07,1,.05,l,0,3.15,g+.08),u(1.95,.07,.05,l,0,3.15,g+.08),u(2.8,.3,.03,d,0,.3,g+.02),H(.11,.05,d,1.12,2.05,g+.03,Math.PI/2),H(.045,.28,w,1.12,2.05,g+.16,Math.PI/2),H(.04,.6,w,.84,2.05,g+.3,0,Math.PI/2),H(.1,.08,d,1.12,2.4,g+.05,Math.PI/2),[.8,2.1,3.4].forEach(f=>H(.06,.38,d,-1.5,f,g+.02)),u(4.8,.14,1.8,t,0,5,1,.22),[-2.1,2.1].forEach(f=>u(.1,.1,1.3,l,f,4.75,.9,-.35)),[-2.7,2.7].forEach(f=>{u(.12,.12,.35,o(3359061),f,3.4,.28);const R=new THREE.Mesh(new THREE.SphereGeometry(.22,14,10),new THREE.MeshBasicMaterial({color:16639626}));R.position.set(f,3.4,.55),n.add(R)}),u(2.4,.04,1.1,o(8330525),0,.15,1.35),n}function buildUnique3DBuilding(e,t,n){const o=new THREE.Group;o.position.set(e.x,0,e.z);const a=e.style||BUILDING_ARCHETYPES[t%BUILDING_ARCHETYPES.length].style,r=e.color||"#0284c7",s=new THREE.MeshLambertMaterial({color:r}),i=new THREE.MeshLambertMaterial({color:16317180}),l=new THREE.MeshLambertMaterial({color:1976635}),m=new THREE.MeshLambertMaterial({color:3718648}),d=new THREE.MeshLambertMaterial({color:16436245}),w=new THREE.MeshBasicMaterial({color:14753096}),p=new THREE.Mesh(new THREE.BoxGeometry(44,.2,34),new THREE.MeshLambertMaterial({color:1483594}));p.position.set(0,-.05,1),o.add(p);const u=new THREE.Mesh(new THREE.BoxGeometry(6.2,.22,12),new THREE.MeshLambertMaterial({color:13358561}));u.position.set(0,.02,12),o.add(u),[[-15.5,10.5],[15.5,10.5],[-16.5,-6.5],[16.5,-6.5]].forEach(([b,S],B)=>{const C=createLushTreeMesh(t+B);C.position.set(b,0,S),o.add(C),solidCircleObstacles.push({x:e.x+b,z:e.z+S,r:1.25})});let M=20,E=9.2,g=7.8;const f=b=>new THREE.MeshLambertMaterial({color:b}),R=b=>new THREE.MeshBasicMaterial({color:b}),y=(b,S,B,C,D,z,A,$,O)=>{const j=new THREE.Mesh(b,S);return j.position.set(B,C,D),z&&(j.rotation.x=z),A&&(j.rotation.y=A),$&&(j.rotation.z=$),(O||o).add(j),j},c=(b,S,B,C,D,z,A,$)=>y(new THREE.BoxGeometry(b,S,B),C,D,z,A,0,0,0,$),h=(b,S,B,C,D,z,A,$,O)=>y(new THREE.CylinderGeometry(b,S,B,$||16),C,D,z,A,0,0,0,O),x=(b,S,B,C,D)=>new THREE.MeshLambertMaterial({map:getFacadeTexture(b,S,B,C,D)}),T=(b,S,B,C,D,z,A)=>{const $=new THREE.Shape;$.moveTo(-b/2,0),$.lineTo(b/2,0),$.lineTo(0,S),$.closePath();const O=new THREE.ExtrudeGeometry($,{depth:B,bevelEnabled:!1});return O.translate(0,0,-B/2),y(O,C,D,z,A)},k=(b,S,B,C,D,z)=>b.forEach(A=>h(B*.9,B,S,D,A,(z||0)+S/2,C,14)),G=(b,S,B,C,D)=>{const z=new THREE.Group;return z.position.set(b,0,S),o.add(z),c(D,1.5,2.1,f(B),0,1.25,0,z),c(D*.5,1,1.9,m,D*.12,2.5,0,z),c(D+.05,.3,2.15,f(C),0,1.25,0,z),[-1,1].forEach(A=>[-1,1].forEach($=>y(new THREE.CylinderGeometry(.5,.5,.4,10),l,A*D*.33,.5,$*1.05,Math.PI/2,0,0,z))),z},v=f(15197668),I=f(14078929);if(a==="library")M=24,E=9.5,c(18,16,14,x("stone","#efe3c8","#0369a1",3,5),0,8,0),c(18.6,.8,14.6,f(11570519),0,16.4,0),k([-6.5,-2.2,2.2,6.5],12,.6,7.6,i,.5),c(15.5,1,2.4,i,0,13,7.6),T(15.5,3.2,2.2,s,0,13.5,7.6),c(14,.5,1.8,I,0,.25,8.8),h(4.6,4.8,2.2,i,0,17.6,0,20),y(new THREE.SphereGeometry(4.4,20,14,0,Math.PI*2,0,Math.PI/2),d,0,18.7,0),h(.9,1.1,2.2,i,0,23.2,0,12),y(new THREE.ConeGeometry(1,1.6,12),d,0,25,0),[-7.2,7.2].forEach(b=>[14427686,2450411,1483594].forEach((S,B)=>c(3.2-B*.4,.8,2.2,f(S),b,17.2+B*.8,-2)));else if(a==="cafe"){M=18,c(16,12,12,x("brick","#b45309","#fde68a",3,4),0,6,-1),c(16.6,.6,12.6,f(8138002),0,12.2,-1);for(let S=-7;S<=7;S+=2)y(new THREE.BoxGeometry(1.8,.5,3.2),f(Math.abs(S)%4===0?15357964:16777215),S,5.2,6.2,.38);const b=new THREE.Group;h(2.5,1.9,3.5,i,0,0,0,18,b),h(2.3,2.3,.2,f(7877903),0,1.75,0,18,b),y(new THREE.TorusGeometry(1.1,.3,8,14),i,2.7,0,0,0,0,0,b),b.position.set(0,14.8,-1),o.add(b),animatedRoofProps.push(b),h(.8,.9,4,f(5722958),-6,14,-3,10),[-8,-5.4,5.4,8].forEach((S,B)=>{h(.9,.9,.15,f(8138002),S,1.2,10.2,12),h(.12,.12,1.1,f(4472892),S,.6,10.2,6),h(.07,.07,2.1,i,S,2.1,10.2,6),y(new THREE.ConeGeometry(1.7,.8,10),f(B%2?15357964:16436245),S,3.2,10.2)})}else if(a==="hospital"){M=25,E=10;const b=x("bands","#f8fafc","#38bdf8",6,5);c(10,22,13,b,0,11,0),[-6.7,6.7].forEach(B=>c(5,15,14,b,B,7.5,0)),c(10.4,.8,13.4,s,0,17,0),c(2.2,6.5,.6,w,0,12,6.7),c(6.5,2.2,.6,w,0,12,6.7),h(3.2,3.2,.4,l,0,22.2,0,24),c(.5,.1,2.6,R(16777215),-.9,22.45,0),c(.5,.1,2.6,R(16777215),.9,22.45,0),c(1.8,.1,.5,R(16777215),0,22.45,0);const S=G(9,10,16777215,14427686,4.4);c(.3,1.2,.3,w,0,3.4,0,S)}else if(a==="mall"){M=28,E=10,c(20,15,14,x("bands","#faf5ff","#a855f7",5,5),0,7.5,0),[5,10].forEach(S=>c(20.5,.7,14.5,s,0,S,0)),c(20.5,.9,14.5,f(3868516),0,15.4,0),y(new THREE.SphereGeometry(5.5,18,12,0,Math.PI*2,0,Math.PI/2),m,0,15.8,-1);const b=new THREE.Group;c(4.4,4,2.2,s,0,0,0,b),c(4.5,.5,2.3,d,0,.6,0,b),y(new THREE.TorusGeometry(1.1,.18,8,14,Math.PI),d,0,2,0,0,0,0,b),b.position.set(0,24.2,-1),o.add(b),animatedRoofProps.push(b),[-9.3,9.3].forEach((S,B)=>{h(.1,.1,8,i,S,19,6.3,6),c(.1,1.2,2.2,f(B?16096779:2278750),S,22.4,7.3)})}else if(a==="office"){M=40,E=7.5;const b=x("glass","#0c4a6e","#38bdf8",9,4);c(12,14,12,b,0,7,0),c(10,12,10,b,0,20,0),c(7,9,7,b,0,30.5,0),[-6,6].forEach(S=>[-6,6].forEach(B=>c(.7,14,.7,l,S,7,B))),c(12.6,.6,12.6,s,0,14.2,0),c(10.6,.6,10.6,s,0,26.3,0),c(7.6,.6,7.6,s,0,35.2,0),h(.15,.4,9,l,0,39.9,0,8),y(new THREE.SphereGeometry(.5,8,8),R(15680580),0,44.6,0),y(new THREE.SphereGeometry(1.6,12,8,0,Math.PI*2,0,Math.PI/2),i,2.2,36,1.5,.9)}else if(a==="cinema"){M=22,c(18,16,14,x("film","#2e1065","#f5d0fe",4,3),0,8,0),c(18.6,1,14.6,s,0,16.5,0),c(15,3,2,d,0,7.4,7.6);for(let B=-7;B<=7;B++)y(new THREE.SphereGeometry(.22,6,6),R(16777215),B,9.1,8.7),y(new THREE.SphereGeometry(.22,6,6),R(16777215),B,5.8,8.7);const b=y(new THREE.CylinderGeometry(3.6,3.6,1,16),d,0,21,0,Math.PI/2);animatedRoofProps.push(b);const S=new THREE.MeshBasicMaterial({color:16707722,transparent:!0,opacity:.22});[-6,6].forEach((B,C)=>y(new THREE.CylinderGeometry(.2,1.4,22,10),S,B,28,0,0,0,C?-.3:.3)),c(3.4,.08,9,f(14427686),0,.2,12)}else if(a==="supermarket"){M=18,E=10,c(20,11,14,x("plain","#fef9c3","#65a30d",3,6),0,5.5,0),c(20.6,1.6,14.6,f(1483594),0,10.2,0),c(13,4.8,.3,m,0,3.2,7.02),c(12,2.2,.9,f(1409085),0,8.4,7.3),[[-7,14427686],[-5.2,16096779],[5.2,6660877],[7,15357964]].forEach(([S,B])=>c(1.6,1.1,1.4,f(B),S,.7,9));const b=new THREE.Group;c(5,2.4,3,f(9741240),0,1.6,0,b),c(.3,1.6,3,f(6583435),-2.6,3,0,b),[-1.8,1.8].forEach(S=>[-1.1,1.1].forEach(B=>y(new THREE.SphereGeometry(.45,8,8),l,S,.2,B,0,0,0,b))),b.position.set(0,12.3,0),o.add(b),animatedRoofProps.push(b)}else if(a==="museum"){M=30,E=9.5;const b=new THREE.Group;b.scale.z=.72,o.add(b),h(8.5,9.5,18,x("bands","#e0e7ff","#6366f1",5,8),0,9,0,28,b),[5,11,17].forEach(C=>y(new THREE.TorusGeometry(9.5-C/18+.15,.3,8,40),s,0,C,0,Math.PI/2,0,0,b)),y(new THREE.SphereGeometry(7,20,12,0,Math.PI*2,0,Math.PI/2),new THREE.MeshLambertMaterial({color:8246268,transparent:!0,opacity:.55}),0,18,0,0,0,0,b);const S=new THREE.Group;S.add(new THREE.Mesh(new THREE.SphereGeometry(1.8,14,14),s)),[0,1.05,-1.05].forEach(C=>{const D=new THREE.Mesh(new THREE.TorusGeometry(4,.18,8,24),d);D.rotation.x=Math.PI/3,D.rotation.z=C,S.add(D)}),S.position.set(0,22,0),o.add(S),animatedRoofProps.push(S);const B=new THREE.Group;B.position.set(-7.5,0,9.5),o.add(B),h(1.4,1.4,.6,l,0,.3,0,12,B),c(1.6,1.8,1.2,i,0,1.5,0,B),c(1.3,1,1,i,0,3,0,B),c(.9,.25,.1,R(3718648),0,3.05,.55,B),h(.05,.05,.9,l,0,3.9,0,6,B),y(new THREE.SphereGeometry(.18,8,8),w,0,4.4,0,0,0,0,B)}else if(a==="tvstation"){M=34,E=10,c(17,16,14,x("glass","#134e4a","#2dd4bf",5,5),0,8,0),c(17.6,.8,14.6,s,0,16.4,0),c(8,3,6,i,-4,18.3,2),c(5,1.6,.5,R(14427686),0,13.5,7.2);const b=new THREE.Group;b.position.set(5,17,-1),o.add(b),h(.4,.5,3,l,0,1.5,0,8,b),y(new THREE.SphereGeometry(3.2,16,10,0,Math.PI*2,0,Math.PI/2),i,0,4.2,0,-.9,0,0,b),animatedRoofProps.push(b),h(.2,.8,14,l,-6,24,-3,6),y(new THREE.SphereGeometry(.45,8,8),R(15680580),-6,31.4,-3),G(9.5,10.5,16777215,889992,4.6)}else if(a==="stadium"){M=26,E=10.5;const b=new THREE.Group;b.scale.set(1,1,.66),o.add(b),h(10.5,8.6,12,s,0,6,0,32,b),[3,6,9].forEach(S=>y(new THREE.TorusGeometry(10.5-S/12*1.9+.05,.25,6,40),i,0,S,0,Math.PI/2,0,0,b)),y(new THREE.TorusGeometry(8.7,.7,8,40),i,0,12,0,Math.PI/2,0,0,b),h(8,8,12.2,f(1409085),0,6,0,32,b),y(new THREE.TorusGeometry(8.3,.35,6,40),f(16436245),0,12.15,0,Math.PI/2,0,0,b),y(new THREE.CircleGeometry(7.9,40),new THREE.MeshLambertMaterial({map:getFacadeTexture("pitch","#16a34a","#ffffff",1,1)}),0,12.2,0,-Math.PI/2,0,0,b),[[-9.2,-5.5],[9.2,-5.5],[-9.2,5.8],[9.2,5.8]].forEach(([S,B])=>{h(.25,.35,22,l,S,11,B,8),y(new THREE.BoxGeometry(3,1.6,.5),R(16710083),S,22.5,B,0,Math.atan2(-S,-B),0)})}else if(a==="cityhall")M=32,E=10,c(19,17,13,x("stone","#f1f5f9","#1d4ed8",3,6),0,8.5,-.5),c(19.6,.8,13.6,f(9741240),0,17.4,-.5),k([-8,-5.6,-3.2,3.2,5.6,8],11.5,.55,7.2,i,.6),c(17.5,1,2.2,i,0,12.6,7.2),T(17.5,3.4,2,i,0,13.1,7.2),c(15,.5,1.6,I,0,.25,8.6),c(5.4,8,5.4,i,0,22,-1),y(new THREE.CylinderGeometry(1.7,1.7,.3,20),R(16777215),0,22.5,1.85,Math.PI/2),c(.15,1.2,.1,l,0,22.8,2.05),c(.9,.15,.1,l,.35,22.5,2.05),y(new THREE.ConeGeometry(4.3,5.5,4),s,0,28.75,-1,0,Math.PI/4,0),h(.08,.08,4,i,0,33.4,-1,6),c(2,1.2,.08,f(14427686),1,34.6,-1);else if(a==="hotel"){M=36,c(15,28,12,x("plain","#fef3c7","#b45309",9,5),0,14,0);for(let S=0;S<8;S++)c(15.6,.35,1.5,S%2?s:i,0,3.6+S*3.2,6.6);c(15.4,2,12.4,s,0,28.4,0),c(9.4,2.8,.8,d,0,31.4,-.1),c(9,2.4,1,f(1841431),0,31.4,0);const b=y(new THREE.OctahedronGeometry(2.4,0),d,0,35.2,0);animatedRoofProps.push(b),c(8,.5,4.5,s,0,4.6,9),[-3.6,3.6].forEach(S=>h(.2,.2,4.4,i,S,2.3,10.8,8))}else if(a==="bank"){M=21,E=9,c(17,14,13,x("stone","#d6d3d1","#365314",3,5),0,7,0),c(17.6,.8,13.6,f(4472892),0,14.4,0),k([-6.5,-4.1,4.1,6.5],10.5,.8,7.4,v,.6),c(15,1,2.6,v,0,11.6,7.4),T(15,3,2.4,I,0,12.1,7.4),c(14,.5,1.8,f(11051678),0,.25,8.8),y(new THREE.CylinderGeometry(1.8,1.8,.5,24),d,0,7.6,6.6,Math.PI/2),y(new THREE.TorusGeometry(1.1,.15,8,20),l,0,7.6,6.9);const b=y(new THREE.CylinderGeometry(3,3,.8,24),d,0,18.5,0,Math.PI/2);animatedRoofProps.push(b)}else if(a==="university"){M=30,E=10.5;const b=x("brick","#9a3412","#fde68a",4,3);c(7.5,22,13,b,0,11,0),c(7.9,.6,13.4,v,0,22.2,0),[-7.5,7.5].forEach(B=>{c(6,12,12,x("brick","#9a3412","#fde68a",3,2),B,6,0),y(new THREE.ConeGeometry(4.4,3.5,4),s,B,13.75,0,0,Math.PI/4,0),h(.07,.07,4,i,B,17.5,0,6),c(.1,1,1.6,f(16436245),B,18.7,.9)});const S=new THREE.Group;S.position.set(0,24.2,0),o.add(S),h(2.2,2.5,1.4,l,0,0,0,12,S),y(new THREE.BoxGeometry(8,.5,8),l,0,.9,0,0,Math.PI/4,0,S),h(.05,.05,2.4,d,3.4,-.3,0,6,S),y(new THREE.SphereGeometry(.3,8,8),d,3.4,-1.3,0,0,0,0,S),animatedRoofProps.push(S)}else if(a==="opera")M=26,E=10,c(19,8,14,x("stone","#fafaf9","#a16207",2,7),0,4,0),c(19.4,.5,14.4,d,0,8.1,0),[[-5,12,4.6,.18],[0,15,5.2,0],[5,11,4.4,-.18]].forEach(([b,S,B,C])=>y(new THREE.ConeGeometry(B,S,14),i,b,8+S/2,0,0,0,C)),c(14,6,.1,m,0,4,7.02),c(14,.4,1.6,I,0,.2,8.4);else if(a==="spacelab"){M=27,E=11,c(13,16,13,x("glass","#e2e8f0","#0284c7",4,4),-2.5,8,0),c(13.6,.7,13.6,s,-2.5,16.2,0),y(new THREE.SphereGeometry(3.2,16,10,0,Math.PI*2,0,Math.PI/2),i,-2.5,16.6,0),c(.3,7,5,f(1982639),-10.2,10,2.2),c(.3,7,5,f(1982639),-10.2,10,-2.8),h(1.5,1.7,17,i,6.8,9.5,1,14),h(1.55,1.55,2.4,s,6.8,11,1,14),y(new THREE.ConeGeometry(1.5,4.5,14),w,6.8,20.2,1);for(let b=0;b<3;b++){const S=b*Math.PI*2/3;y(new THREE.BoxGeometry(.25,3.2,1.6),f(14427686),6.8+Math.cos(S)*1.9,2.4,1+Math.sin(S)*1.9,0,-S,0)}c(.5,22,.5,f(4674921),9.4,11,1),[6,12,18].forEach(b=>c(2.4,.3,.3,f(4674921),8.2,b,1))}else if(a==="firestation"){M=25,E=9.5,c(18,14,14,f(12131356),0,7,0),c(18.4,.8,14.4,i,0,9.6,0),c(18.6,.8,14.6,f(8330525),0,14.4,0),[-5.8,5.8].forEach(B=>c(5.2,5.8,.3,x("garage","#f8fafc","#94a3b8",1,1),B,2.9,7.05)),c(3.6,22,3.6,f(14427686),-7.6,11,-3.5),[6,14].forEach(B=>c(3.8,.6,3.8,i,-7.6,B,-3.5)),y(new THREE.ConeGeometry(2.8,3.5,4),f(8330525),-7.6,23.75,-3.5,0,Math.PI/4,0),y(new THREE.SphereGeometry(.9,10,8,0,Math.PI*2,0,Math.PI/2),d,-7.6,19.5,-1.7,Math.PI);const b=new THREE.Group;b.position.set(6,15.2,0),o.add(b),c(1.4,.9,.9,R(15680580),-.7,0,0,b),c(1.4,.9,.9,R(3900150),.7,0,0,b),animatedRoofProps.push(b);const S=G(8.5,11,14427686,16777215,5.6);c(4.4,.2,.5,i,-.2,3.1,0,S)}else if(a==="police"){M=26,c(17,18,14,x("bands","#1e3a8a","#93c5fd",5,5),0,9,0),c(17.6,.8,14.6,f(988970),0,18.4,0),y(new THREE.ExtrudeGeometry(starShape(2.6,1.1),{depth:.5,bevelEnabled:!1}),d,0,13.4,6.8);const b=new THREE.Group;b.position.set(0,19.6,0),o.add(b),c(4.4,.6,1.4,l,0,0,0,b),c(1.6,.8,1.2,R(15680580),-1.3,.6,0,b),c(1.6,.8,1.2,R(3900150),1.3,.6,0,b),animatedRoofProps.push(b),h(.1,.2,8,l,-6,22,-3,6),h(.08,.08,5,i,7,21,3,6),c(.1,1.2,2,f(1920728),7,23.2,4);const S=G(8.5,11,1981066,16777215,4.6);c(.8,.3,1.6,R(15680580),0,3.1,0,S)}else if(a==="skyport"){M=32,E=9,h(4.4,5.6,18,i,0,9,0,18),[4,9,14].forEach(C=>y(new THREE.TorusGeometry(5.6-C/18*1.2+.1,.25,8,28),s,0,C,0,Math.PI/2)),h(7.6,5,4.5,m,0,20.5,0,18),h(7.8,7.8,.6,s,0,23,0,24),h(9,9,.7,f(3359061),0,23.6,0,28),y(new THREE.TorusGeometry(8.2,.12,6,36),R(16436245),0,24,0,Math.PI/2),c(.6,.05,3.4,R(16777215),-1.2,24,5.2),c(.6,.05,3.4,R(16777215),1.2,24,5.2),c(2.4,.05,.6,R(16777215),0,24,5.2);const b=new THREE.Group;b.position.set(0,25.2,0),o.add(b),y(new THREE.SphereGeometry(1.6,12,10),f(14427686),0,1.4,0,0,0,0,b).scale.set(1.5,.9,.9),c(3.6,.35,.35,f(14427686),-3.2,1.7,0,b),c(3.2,.1,.15,l,0,.1,.9,b),c(3.2,.1,.15,l,0,.1,-.9,b),h(.12,.12,.9,l,0,2.7,0,6,b);const B=new THREE.Group;B.position.y=3.2,b.add(B),c(7,.1,.35,l,0,0,0,B),c(.35,.1,7,l,0,0,0,B),animatedRoofProps.push(B)}else{M=44,E=11;const b=x("glass","#94a3b8","#bae6fd",12,3),S=f(13358561),B=x("glass","#64748b","#bae6fd",2,9);c(20,7.5,11.65,B,0,3.75,1.075),c(20.8,.55,12.45,s,0,7.78,1.075),c(20.8,.3,12.45,i,0,7.35,1.075),[-1,1].forEach(C=>c(.5,7.5,.5,i,C*10.1,3.75,6.95)),c(7.2,.12,3.2,i,0,.06,8.5),[-5.8,5.8].forEach(C=>{h(3.6,4.1,16,b,C,8,0,16),h(3,3.5,9,b,C,20.5,0,16),h(2.3,2.8,8,b,C,29,0,16),h(1.6,2.1,3,S,C,34.5,0,16),y(new THREE.ConeGeometry(1.4,3.5,12),S,C,37.75,0),h(.1,.25,6,S,C,42.5,0,6),[[16,3.6],[25,3],[33,2.3]].forEach(([D,z])=>y(new THREE.TorusGeometry(z+.05,.28,8,24),f(14870768),C,D,0,Math.PI/2))}),c(5,1.8,2.6,S,0,18,0),y(new THREE.BoxGeometry(.4,5.5,.4),S,-1.4,15.3,0,0,0,.35),y(new THREE.BoxGeometry(.4,5.5,.4),S,1.4,15.3,0,0,0,-.35)}if(solidBoxObstacles.push({minX:e.x-E,maxX:e.x+E,minZ:e.z-g,maxZ:e.z+g}),o.add(buildRealDoor(r,s)),n){const b=createTextLabelSprite(`GEDUNG G${t+1} • ${e.type.toUpperCase()}`,"#facc15",1.15);b.position.set(0,6.2,8.4),o.add(b);const S=createTextLabelSprite(`[G${t+1}] ${e.name}`,"#facc15",1.65);S.position.set(0,M+8,0),o.add(S);const B=new THREE.Mesh(new THREE.RingGeometry(2.5,3.5,32),new THREE.MeshBasicMaterial({color:16436245,side:THREE.DoubleSide}));B.rotation.x=-Math.PI/2,B.position.set(0,.22,11.5),o.add(B),buildingColliders.push({...e,gIndex:t+1,doorX:e.x,doorZ:e.z+11.5});const C=createDoorBoard();C.group.position.set(5.2,0,11),o.add(C.group),doorBoards[e.id]=C}else{const b=createTextLabelSprite(e.type.toUpperCase(),r,1);b.position.set(0,6.2,8.4),o.add(b)}cityBuildingsGroup.add(o)}function aesAssignBuildingSlots(){const e=gameConfig.buildings,t=new Set,n=[];e.forEach((a,r)=>{const s=BUILDING_ARCHETYPES.findIndex(i=>i.style===a.style);s>=0&&!t.has(s)?(t.add(s),n[r]=s):n[r]=-1});let o=BUILDING_ARCHETYPES.length;return e.forEach((a,r)=>{if(n[r]>=0)return;const s=aesFirstFreeArchetype(t);if(s>=0){t.add(s),n[r]=s;const i=BUILDING_ARCHETYPES[s];a.style=i.style,a.type=i.type,a.color=i.color}else n[r]=o++}),n}function aesFirstFreeArchetype(e){for(let t=0;t<BUILDING_ARCHETYPES.length;t++)if(!e.has(t))return t;return-1}function rebuildCityBuildings3D(){if(!cityBuildingsGroup)return;for(;cityBuildingsGroup.children.length>0;){const o=cityBuildingsGroup.children[0];cityBuildingsGroup.remove(o),AES_LITE&&aesDisposeDeep(o)}buildingColliders=[],all20CityBuildingsMeta=[],animatedRoofProps=[],solidBoxObstacles=[],doorBoards={};const e=aesAssignBuildingSlots(),t={};e.forEach((o,a)=>{t[o]=a});const n=Math.max(20,e.reduce((o,a)=>Math.max(o,a+1),0));for(let o=0;o<n;o++){const a=getBuildingSlotCoordinate(o),r=BUILDING_ARCHETYPES[o%BUILDING_ARCHETYPES.length];if(t[o]!==void 0){const s=t[o],i=gameConfig.buildings[s];i.x=a.x,i.z=a.z,i.color||(i.color=r.color),buildUnique3DBuilding(i,s,!0),all20CityBuildingsMeta.push({x:i.x,z:i.z,isMaterial:!0,gLabel:"G"+(s+1),id:i.id,name:i.name,type:i.type})}else{const s={id:"deco_"+o,type:r.type,style:r.style,name:r.type,color:r.color,x:a.x,z:a.z};buildUnique3DBuilding(s,o,!1),all20CityBuildingsMeta.push({x:s.x,z:s.z,isMaterial:!1,gLabel:"",id:s.id,name:s.name,type:s.type})}}AES_LITE&&aesMergeStaticTree(cityBuildingsGroup,animatedRoofProps.concat(Object.keys(doorBoards).map(o=>doorBoards[o]&&doorBoards[o].group)))}function createRobotCharacterMesh(e,t){const n=new THREE.Group,o=t||"#0ea5e9",a=(c,h)=>new THREE.MeshPhongMaterial({color:c,shininess:Math.min(h||60,30),specular:2039583}),r=a(15857145,70),s=a(o,70),i=a(1976635,40),l=a(6583435,50),m=new THREE.MeshBasicMaterial({color:3718648}),d=(c,h,x,T,k,G)=>{const v=new THREE.Mesh(h,x);return v.position.set(T,k,G),c.add(v),v},w=(c,h,x,T)=>new THREE.CylinderGeometry(c,h,x,T||14),p=c=>new THREE.SphereGeometry(c,14,10);d(n,new THREE.BoxGeometry(1.25,.95,1.1),r,0,3.5,0),d(n,new THREE.BoxGeometry(1.05,.6,.1),i,0,3.5,.55),[-.27,.27].forEach(c=>d(n,new THREE.BoxGeometry(.3,.16,.05),m,c,3.55,.6)),d(n,new THREE.BoxGeometry(.3,.12,.8),s,0,4,-.05),[-1,1].forEach(c=>{const h=d(n,w(.24,.24,.2,16),s,c*.7,3.5,0);h.rotation.z=Math.PI/2}),d(n,w(.03,.03,.45,6),l,.38,4.25,-.2),d(n,p(.08),m,.38,4.5,-.2),d(n,w(.22,.26,.25,12),i,0,2.92,0),d(n,new THREE.BoxGeometry(1.5,1,.9),s,0,2.3,0),d(n,new THREE.BoxGeometry(1.1,.7,.06),r,0,2.35,.46);const u=d(n,w(.17,.17,.06,16),m,0,2.35,.5);u.rotation.x=Math.PI/2,d(n,new THREE.TorusGeometry(.22,.03,8,20),i,0,2.35,.5),d(n,new THREE.BoxGeometry(1,.5,.7),i,0,1.5,0),d(n,new THREE.BoxGeometry(1.25,.2,.78),l,0,1.25,0),d(n,new THREE.BoxGeometry(.95,.95,.35),i,0,2.25,-.62),[-.28,.28].forEach(c=>{d(n,w(.12,.14,.35,10),l,c,1.65,-.62),d(n,w(.09,.09,.04,10),m,c,1.45,-.62)});const H=c=>{const h=new THREE.Group;return h.position.set(c*1.02,2,0),d(h,p(.38),r,0,.62,0).scale.set(1,.8,1),d(h,w(.17,.17,.5,12),r,0,.3,0),d(h,p(.19),i,0,0,0),d(h,w(.2,.17,.5,12),s,0,-.3,0),d(h,p(.21),i,0,-.65,0),n.add(h),h},M=H(-1),E=H(1),g=c=>{const h=new THREE.Group;return h.position.set(c*.4,.6,0),d(h,p(.25),i,0,.6,0),d(h,w(.23,.2,.5,12),r,0,.32,0),d(h,p(.2),i,0,.02,0),d(h,w(.2,.17,.45,12),l,0,-.24,0),d(h,new THREE.BoxGeometry(.5,.22,.74),r,0,-.49,.1),d(h,new THREE.BoxGeometry(.5,.1,.2),s,0,-.52,.42),n.add(h),h},f=g(-1),R=g(1);AES_LITE&&(aesBakeDirect(n),aesBakeDirect(M),aesBakeDirect(E),aesBakeDirect(f),aesBakeDirect(R));const y=createTextLabelSprite(`🤖 ${e}`,t||"#0ea5e9",.6);return y.position.set(0,5.7,0),n.add(y),n.userData={leftLeg:f,rightLeg:R,leftArm:M,rightArm:E,nameSprite:y,playerColor:o},n}function aesBoatSlot(id){ /* urutan kapal 20-50 siswa: kolom (jalur) + baris belakang, sama di semua layar */
  try{
    var now=performance.now(),c=window.__aesBS;
    var ids=Object.keys(otherPlayers),me=(myPlayer&&myPlayer.id!=null)?String(myPlayer.id):"";
    if(!c||c.n!==ids.length||now-c.t>1500){
      var all=ids.slice();if(me&&all.indexOf(me)<0)all.push(me);all.sort();
      c=window.__aesBS={n:ids.length,t:now,all:all};
    }
    var n=c.all.length,rank=Math.max(0,c.all.indexOf(String(id))),cols=Math.max(1,Math.min(12,n)),sp=n<=6?4.5:3.6;
    return{w:((rank%cols)-(cols-1)/2)*sp,back:Math.floor(rank/cols)*7};
  }catch(e){return{w:0,back:0}}
}
function createSpeedboatMesh(e,t,n){const o=new THREE.Group,a=t||"#0ea5e9",r=(P,L)=>new THREE.MeshPhongMaterial({color:P,shininess:L||50,specular:3355443,side:THREE.DoubleSide}),s=P=>new THREE.MeshLambertMaterial({color:P,side:THREE.DoubleSide}),i=r(16317180,70),l=r(988970,30),m=r(a,70),d=s(11565637),w=s(8146725),p=s(1976635),u=r(14870768,100),H=r(6583435,40),M=new THREE.MeshPhongMaterial({color:8246268,transparent:!0,opacity:.5,shininess:100,side:THREE.DoubleSide,depthWrite:!1}),E=-3.4,g=5.2,f=P=>(P-E)/(g-E),R=P=>{const L=P<.38?1.28+.12*Math.sin(P/.38*Math.PI/2):1.4*Math.pow(Math.max(0,1-(P-.38)/.62),.85),_=Math.max(0,(P-.45)/.55);return{x:E+(g-E)*P,W:Math.max(L,.03),H:1.22+.78*Math.pow(P,2.4),K:-.35+1.55*Math.pow(_,1.6)}},y=(P,L)=>Math.min(1,Math.max(0,(L.H-P)/(L.H-L.K))),c=(P,L)=>P.W*(1-Math.pow(L,1.5)),h=(P,L)=>P.H-(P.H-P.K)*L,x=(P,L,_,N)=>{const F=[],q=[];for(let J=0;J<=P;J++)for(let U=0;U<=L;U++)F.push(..._(J/P,U/L));for(let J=0;J<P;J++)for(let U=0;U<L;U++){const Z=J*(L+1)+U,Y=Z+L+1;q.push(Z,Y,Z+1,Z+1,Y,Y+1)}const W=new THREE.BufferGeometry;W.setAttribute("position",new THREE.Float32BufferAttribute(F,3)),W.setIndex(q),W.computeVertexNormals();const K=new THREE.Mesh(W,N);return o.add(K),K},T=(P,L,_,N,F,q,W,K,J)=>{const U=new THREE.Mesh(new THREE.BoxGeometry(P,L,_),N);return U.position.set(F,q,W),K&&(U.rotation.z=K),J&&(U.rotation.y=J),o.add(U),U},k=.3,G=.06;[-1,1].forEach(P=>{const L=(_,N,F)=>x(40,5,(q,W)=>{const K=R(q),J=_(K),U=N(K),Z=J+(U-J)*W;return[K.x,h(K,Z),P*c(K,Z)]},F);L(()=>0,_=>y(k,_),i),L(_=>y(k,_),_=>y(G,_),m),L(_=>y(G,_),()=>1,l)});const v=R(0);[[0,y(k,v),i],[y(k,v),y(G,v),m],[y(G,v),1,l]].forEach(([P,L,_])=>x(1,4,(N,F)=>{const q=P+(L-P)*F;return[E,h(v,q),(N?1:-1)*c(v,q)]},_));const I=f(1.7);x(24,8,(P,L)=>{const _=R(I+(1-I)*P),N=L*2-1;return[_.x,_.H+.07*(1-N*N),N*_.W]},i),x(20,1,(P,L)=>{const _=R(I+(.955-I)*P);return[_.x,_.H+.085,(L*2-1)*.12]},m);const b=-3.35,S=1.3,B=P=>{const L=R(P);return c(L,y(.84,L))-.04};x(30,1,(P,L)=>{const _=f(b+(S-b)*P);return[E+(g-E)*_,.84,(L*2-1)*B(_)]},d),[-.6,-.2,.2,.6].forEach(P=>T(S-b,.012,.035,w,(b+S)/2,.848,P)),[-1,1].forEach(P=>{const L=[];for(let _=0;_<=24;_++){const N=R(_/24*.995);L.push(new THREE.Vector3(N.x,N.H+.02,P*N.W))}o.add(new THREE.Mesh(new THREE.TubeGeometry(new THREE.CatmullRomCurve3(L),60,.06,6,!1),u))}),T(.6,.72,1.3,i,1.45,1.2,0),T(.62,.06,1.32,l,1.45,1.57,0),T(.05,.8,1.1,M,1.54,1.96,0,.42),[-1,1].forEach(P=>T(.05,.75,.5,M,1.42,1.92,P*.75,.42,P*-.54)),T(.05,.05,1.1,u,1.377,2.325,0,.42),T(.04,.4,.04,H,1.3,1.75,0,.59);const C=new THREE.Mesh(new THREE.TorusGeometry(.26,.04,8,18),l);C.position.set(1.2,1.9,0),C.rotation.y=Math.PI/2,o.add(C);const D=B(f(-2.75))*2-.08;T(.7,.4,D,i,-2.75,1.04,0),T(.74,.12,D-.1,p,-2.75,1.3,0);const z=new THREE.Group;z.position.set(-3.95,0,0);const A=(P,L,_,N,F)=>{const q=new THREE.Mesh(P,L);return q.position.set(_,N,F),z.add(q),q};A(new THREE.BoxGeometry(.4,.55,.8),H,.35,1,0),A(new THREE.CylinderGeometry(.34,.44,.85,16),i,0,1.45,0),A(new THREE.SphereGeometry(.34,16,8,0,Math.PI*2,0,Math.PI/2),i,0,1.875,0),A(new THREE.CylinderGeometry(.42,.42,.16,16),m,0,1.3,0),A(new THREE.CylinderGeometry(.2,.26,1.5,12),H,0,.3,0),A(new THREE.SphereGeometry(.3,12,8),H,-.1,-.45,0).scale.set(1.8,.8,.8),A(new THREE.BoxGeometry(.5,.45,.05),H,-.1,-.7,0),o.add(z);const $=n?null:createRobotCharacterMesh(e,t);$&&($.position.set(-.4,.85,0),$.rotation.y=Math.PI/2,o.add($));const O=new THREE.Group;O.position.set(-3.4,.8,0),o.add(O);const j=[-1,1].map(P=>{const L=new THREE.Group;L.position.set(-.4,1.4,P*1.34);const _=new THREE.Group;_.rotation.x=P*.6;const N=new THREE.Mesh(new THREE.CylinderGeometry(.045,.045,3,8),d);N.rotation.x=Math.PI/2,N.position.z=P*.95,_.add(N);const F=new THREE.Mesh(new THREE.BoxGeometry(.05,.42,.95),m);F.position.z=P*2.1,_.add(F);const q=new THREE.Mesh(new THREE.BoxGeometry(.06,.44,.1),i);q.position.z=P*2.55,_.add(q);const W=new THREE.Mesh(new THREE.CylinderGeometry(.07,.07,.3,8),l);return W.rotation.x=Math.PI/2,W.position.z=P*-.4,_.add(W),L.add(_),o.add(L),T(.14,.22,.14,u,-.4,1.34,P*1.34),L}),X=new THREE.Mesh(new THREE.SphereGeometry(.04,6,4),u);return X.onBeforeRender=()=>{j[0].rotation.y=-O.rotation.y,j[1].rotation.y=O.rotation.y},O.add(X),AES_LITE&&(aesBakeDirect(o),aesBakeDirect(z)),o.userData={oar:O,pilotRobot:$},o}function createOrUpdateMyAvatar3D(){scene&&(removeMyAvatarFromScene(),!(myPlayer.role!=="student"||!myPlayer.hasJoinedGame||!myPlayer.name)&&(myAvatarMesh=createRobotCharacterMesh(myPlayer.name,myPlayer.color),myAvatarMesh.userData.nameSprite&&(myAvatarMesh.userData.nameSprite.visible=!1),myAvatarMesh.position.set(myPlayer.x,0,myPlayer.z),scene.add(myAvatarMesh),myBoatMesh=createSpeedboatMesh(myPlayer.name,myPlayer.color),myBoatMesh.userData&&myBoatMesh.userData.pilotRobot&&myBoatMesh.userData.pilotRobot.userData.nameSprite&&(myBoatMesh.userData.pilotRobot.userData.nameSprite.visible=!1),myBoatMesh.position.set(BOAT_START_POS.x,.2,BOAT_START_POS.z),myBoatMesh.visible=(gamePhase==="race"||myPlayer.atDock)&&!myPlayer.finishedRace,scene.add(myBoatMesh)))}function renderHighResLabelCanvas(e,t,n){const o=e.getContext("2d");o.setTransform(1,0,0,1,0,0),o.clearRect(0,0,e.width,e.height);{const p=e.width/2048;p!==1&&o.setTransform(p,0,0,p,0,0)}o.fillStyle="#090d16",o.strokeStyle=n||"#facc15",o.lineWidth=36,drawRoundedRect(o,44,60,1960,392,110),o.fill(),o.stroke();const a=String(t).trim(),r=p=>`900 ${p}px 'Plus Jakarta Sans', Arial, sans-serif`,s=1780;o.textAlign="center",o.textBaseline="middle";let i=120;for(o.font=r(i);i>64&&o.measureText(a).width>s;)i-=4,o.font=r(i);let l=[a];if(o.measureText(a).width>s){const p=a.split(/\s+/);if(p.length>1){let u=null;i=92,o.font=r(i);for(let H=1;H<p.length;H++){const M=p.slice(0,H).join(" "),E=p.slice(H).join(" "),g=Math.max(o.measureText(M).width,o.measureText(E).width);(!u||g<u.w)&&(u={l1:M,l2:E,w:g})}l=[u.l1,u.l2]}else{const u=Math.ceil(a.length/2);l=[a.slice(0,u),a.slice(u)],i=92,o.font=r(i)}for(;i>44&&l.some(u=>o.measureText(u).width>s);)i-=4,o.font=r(i)}const m=Math.max(8,Math.round(i*.15)),d=i*1.08,w=256-(l.length-1)*d/2+4;l.forEach((p,u)=>{const H=w+u*d;o.lineWidth=m,o.lineJoin="round",o.strokeStyle="#000000",o.strokeText(p,1024,H),o.fillStyle="#ffffff",o.fillText(p,1024,H)})}function createTextLabelSprite(e,t,n=1){const o=document.createElement("canvas");o.width=2048,o.height=512,renderHighResLabelCanvas(o,e,t);const a=new THREE.CanvasTexture(o);a.generateMipmaps=!0,a.minFilter=THREE.LinearMipmapLinearFilter,a.magFilter=THREE.LinearFilter,a.anisotropy=labelAniso(),a.needsUpdate=!0;const r=new THREE.SpriteMaterial({map:a,transparent:!0,fog:!1,depthTest:!0}),s=new THREE.Sprite(r);return s.scale.set(10.2*n,2.55*n,1),s.userData={canvas:o,texture:a,baseW:10.2*n,baseH:2.55*n},registerLabelSprite(s),s}function labelAniso(){try{return renderer?Math.min(renderer.capabilities.getMaxAnisotropy(),16):8}catch{return 8}}var _labelSprites=[],_lblPos=null;function registerLabelSprite(e){_labelSprites||(_labelSprites=[]),_labelSprites.push(e)}function _isInScene(e){for(;e;){if(e===scene)return!0;e=e.parent}return!1}function updateLabelScaling(){if(_labelSprites.length>300)for(let t=_labelSprites.length-1;t>=0;t--)_isInScene(_labelSprites[t])||_labelSprites.splice(t,1);_lblPos||(_lblPos=new THREE.Vector3);const e=!!isTeacher3DMonitor;if(!(AES_LITE&&!e))for(let t=0;t<_labelSprites.length;t++){const n=_labelSprites[t],o=n.userData;if(!o||!o.baseW||!n.visible)continue;let a=1;e&&(n.getWorldPosition(_lblPos),a=Math.min(2.6,Math.max(1,camera.position.distanceTo(_lblPos)/50))),o.curF!==a&&(o.curF=a,n.scale.set(o.baseW*a,o.baseH*a,1))}}function updateSpriteCanvasText(e,t,n){!e||!e.userData||!e.userData.canvas||(renderHighResLabelCanvas(e.userData.canvas,t,n),e.userData.texture.needsUpdate=!0)}let _mapHits=[],_mapSel=[];function _mapEsc(e){return String(e??"").replace(/[&<>"']/g,t=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"})[t])}function _mapPoint(e){const t=e.currentTarget,n=t.getBoundingClientRect();return{x:(e.clientX-n.left)*t.width/n.width,y:(e.clientY-n.top)*t.height/n.height}}function _mapFindHits(e,t){return _mapHits.map(n=>({h:n,d:Math.hypot(n.x-e.x,n.y-e.y)})).filter(n=>n.d<=t).sort((n,o)=>n.d-o.d).map(n=>n.h)}function initMiniMapPick(){const e=document.getElementById("minimap-canvas");!e||e._pickBound||(e._pickBound=!0,e.addEventListener("click",t=>{if(!isTeacherMode)return;const n=_mapFindHits(_mapPoint(t),9);_mapSel=n.slice(0,5).map(o=>o.id),n.length&&playSoundEffect("click"),renderMiniMapRadar(),refreshMapPick()}),e.addEventListener("mousemove",t=>{e.style.cursor=isTeacherMode&&_mapFindHits(_mapPoint(t),9).length?"pointer":"default"}))}function clearMapPick(){_mapSel=[],renderMiniMapRadar(),refreshMapPick()}function refreshMapPick(){const e=document.getElementById("hud-map-pick");if(!e)return;const t=()=>{e.innerHTML&&(e.innerHTML=""),e.classList.add("hidden")};if(!isTeacherMode||!_mapSel.length)return t();const n=getAllStudentsListForReport(),o=_mapSel.map(s=>n.find(i=>String(i.id)===String(s))).filter(Boolean);if(!o.length)return _mapSel=[],t();const a=gameConfig.buildings.length,r=`<div class="flex items-center justify-between"><span class="text-[10px] font-extrabold uppercase tracking-wider text-amber-300">📍 ${o.length>1?o.length+" siswa di titik ini":"Siswa dipilih"}</span><button onclick="clearMapPick()" class="px-1.5 text-slate-300 hover:text-white font-extrabold" title="Tutup">✕</button></div>`+o.map(s=>`<div class="flex items-center justify-between gap-2 p-1.5 rounded-lg bg-slate-800/90 border border-white/10">\n          <div class="truncate"><div class="font-extrabold text-white text-xs truncate">${_mapEsc(s.name)}</div>\n          <div class="text-[10px] text-sky-200 truncate">📍 ${s.offline?"⚫ Keluar • ":""}${s.finishedRace?"🏝️ Pulau Victory":s.atDock?"🚤 Mendayung":_mapEsc(s.currentBuilding||"Kota")}</div>\n          <div class="text-[10px] text-slate-300">🏢 ${s.completedCount||0}/${a} • <span class="text-emerald-400 font-bold">✓${s.initialCorrect||0}</span> <span class="text-rose-400 font-bold">✗${s.initialWrong||0}</span> • 🪙${s.coins||0}</div></div>\n          <div class="shrink-0 flex items-center gap-1">\n            <button onclick="openTeacherNotesModal('${_mapEsc(s.id)}')" class="px-2 py-1 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold rounded-lg text-[10px]" title="Lihat Catatan Gedung">📖</button>\n            ${!s.isMe&&isTeacher3DMonitor?`<button onclick="focusCameraOnStudent('${_mapEsc(s.id)}')" class="px-2 py-1 bg-sky-400 hover:bg-sky-300 text-slate-950 font-extrabold rounded-lg text-[10px]" title="Pantau Siswa">👁️</button>`:""}\n          </div></div>`).join("");e.classList.remove("hidden"),setHtmlIfChanged("hud-map-pick",r)}function renderMiniMapRadar(){const e=document.getElementById("minimap-canvas");if(!e)return;e._pickBound||initMiniMapPick(),_mapHits.length=0;const t=e.getContext("2d"),n=e.width,o=e.height;t.fillStyle="#14532d",t.fillRect(0,0,n,o);const a=i=>(i+190)/380*n,r=i=>(i+280)/480*o;t.fillStyle="#0284c7",t.fillRect(0,r(68),n,o-r(68)),t.fillStyle="#fde68a",t.beginPath(),t.arc(a(VICTORY_ISLAND.centerX),r(VICTORY_ISLAND.centerZ),10,0,Math.PI*2),t.fill(),t.strokeStyle="#475569",t.lineWidth=2.2,t.beginPath(),[-168,-84,0,84,168].forEach(i=>{t.moveTo(a(i),r(-264)),t.lineTo(a(i),r(i===0?64:36))}),[36,-24,-84,-144,-204,-264].forEach(i=>{t.moveTo(a(-168),r(i)),t.lineTo(a(168),r(i))}),t.stroke(),npcCarsList.forEach(i=>{t.fillStyle="#f97316",t.fillRect(a(i.position.x)-1.5,r(i.position.z)-1.5,3,3)}),all20CityBuildingsMeta.forEach(i=>{if(i.isMaterial){const l=a(i.x),m=r(i.z),d=myPlayer.completedBuildings.includes(i.id);t.fillStyle=d?"#22c55e":"#facc15",t.beginPath(),t.arc(l,m,7.2,0,Math.PI*2),t.fill(),t.fillStyle="#0f172a",t.font="bold 9px sans-serif",t.textAlign="center",t.textBaseline="middle",t.fillText(i.gLabel,l,m+.5)}});const s=isTeacherMode||isTeacher3DMonitor;(s?Object.values(otherPlayers):[]).forEach(i=>{if(!i.offline){if(i.role==="student"&&i.hasJoinedGame&&i.insideBuilding){if(!s)return;const l=all20CityBuildingsMeta.find(p=>p.id===i.insideBuilding),m=String(i.id).charCodeAt(String(i.id).length-1)%4*4,d=a(l?l.x:i.targetX||0)+9+m,w=r(l?l.z:i.targetZ||0)-7;t.fillStyle="#c084fc",t.strokeStyle="#ffffff",t.lineWidth=1.5,t.beginPath(),t.arc(d,w,4.5,0,Math.PI*2),t.fill(),t.stroke(),_mapHits.push({id:i.id,x:d,y:w});return}i.role==="student"&&i.hasJoinedGame&&(t.fillStyle="#38bdf8",t.beginPath(),t.arc(a(i.targetX||0),r(i.targetZ||0),4,0,Math.PI*2),t.fill(),_mapHits.push({id:i.id,x:a(i.targetX||0),y:r(i.targetZ||0)}))}}),isTeacherMode&&_mapSel.length&&_mapSel.forEach(i=>{const l=_mapHits.find(m=>String(m.id)===String(i));if(l&&(t.strokeStyle="#fde047",t.lineWidth=2.4,t.beginPath(),t.arc(l.x,l.y,8,0,Math.PI*2),t.stroke(),_mapSel.length===1)){const m=otherPlayers[i],d=String(m&&m.name||"Siswa");t.font="bold 10px sans-serif",t.textAlign="left",t.textBaseline="middle";const w=t.measureText(d).width+10;let p=l.x-w/2,u=l.y-19;u<8&&(u=l.y+19),p=Math.max(2,Math.min(n-w-2,p)),t.fillStyle="rgba(15,23,42,0.94)",t.fillRect(p,u-8,w,16),t.strokeStyle="#fde047",t.lineWidth=1,t.strokeRect(p,u-8,w,16),t.fillStyle="#ffffff",t.fillText(d,p+5,u+.5)}}),!isTeacher3DMonitor&&myPlayer.role==="student"&&myPlayer.hasJoinedGame&&(t.fillStyle="#4ade80",t.beginPath(),t.arc(a(myPlayer.x),r(myPlayer.z),4.5,0,Math.PI*2),t.fill()),_mapSel.length&&refreshMapPick()}const WALK_SPEED=8;let walkVel={x:0,z:0},walkAmt=0,lastMiniMapDraw=0,baseDpr=1,curDpr=1,fpsFrames=0,fpsLast=Date.now(),_goodFpsStreak=0;function adaptResolution(e){if(!renderer||!aesGfxAdaptive())return;let t=curDpr;e<22&&curDpr>1?(t=Math.max(1,curDpr-.25),_goodFpsStreak=0):e>58&&curDpr<baseDpr?++_goodFpsStreak>=3&&(t=Math.min(baseDpr,curDpr+.25),_goodFpsStreak=0):_goodFpsStreak=0,t!==curDpr&&(curDpr=t,renderer.setPixelRatio(curDpr),renderer.setSize(window.innerWidth,window.innerHeight))}const parkedBoats={};let lastParkSync=0;function parkedSlotPos(e){const t=e%2?1:-1,n=Math.floor(e/2);return{x:t*(19+n%14*10),z:71.8+Math.floor(n/14)*8}}function syncParkedBoats(){if(!scene)return;const e=gamePhase==="waiting"||gamePhase==="explore"||gamePhase==="walk_to_dock",t=getAllStudentsListForReport(),n=new Set(t.map(a=>String(a.id)));Object.keys(parkedBoats).forEach(a=>{n.has(a)||(scene.remove(parkedBoats[a].mesh),delete parkedBoats[a])});const o=new Set(Object.values(parkedBoats).map(a=>a.slot));t.forEach(a=>{const r=String(a.id);let s=parkedBoats[r];if(!s){let i=0;for(;o.has(i);)i++;o.add(i);const l=createSpeedboatMesh(a.name,a.color,!0),m=parkedSlotPos(i);l.position.set(m.x,.2,m.z),scene.add(l),s=parkedBoats[r]={mesh:l,slot:i}}s.mesh.visible=e&&!a.atDock}),syncBeachedBoats()}const beachedBoats={};function beachedSlotPose(e){const t=Math.floor(e/12),n=e%12,o=n%2?1:-1,a=.42+Math.floor(n/2)*.17,r=Math.PI+o*a,s=ISLAND_SHORE_R+4+t*8;return{x:VICTORY_ISLAND.centerX+Math.cos(r)*s,z:VICTORY_ISLAND.centerZ+Math.sin(r)*s,ry:-o*a}}function syncBeachedBoats(){if(!scene)return;const e=getAllStudentsListForReport().filter(o=>o.finishedRace),t=new Set(e.map(o=>String(o.id)));Object.keys(beachedBoats).forEach(o=>{t.has(o)||(scene.remove(beachedBoats[o].mesh),delete beachedBoats[o])});const n=new Set(Object.values(beachedBoats).map(o=>o.slot));e.forEach(o=>{const a=String(o.id);if(beachedBoats[a])return;let r=0;for(;n.has(r);)r++;n.add(r);const s=createSpeedboatMesh(o.name,o.color,!0),i=beachedSlotPose(r);s.position.set(i.x,.2,i.z),s.rotation.y=i.ry,scene.add(s),beachedBoats[a]={mesh:s,slot:r}})}function animate3D(){if(requestAnimationFrame(animate3D),!clock||!renderer||!scene||!camera)return;const e=Math.min(clock.getDelta(),.1),t=clock.getElapsedTime(),n=Date.now();if(fpsFrames++,n-fpsLast>=2e3&&(n-fpsLast<4e3&&adaptResolution(fpsFrames*1e3/(n-fpsLast)),fpsFrames=0,fpsLast=n),n-lastParkSync>400&&(lastParkSync=n,syncParkedBoats(),updateBusBoardUI(),updateDoorBoards(),aesHalteUI()),Object.values(parkedBoats).forEach(s=>{s.mesh.visible&&(s.mesh.position.y=.2+Math.sin(t*1.6+s.slot)*.05)}),Object.values(beachedBoats).forEach(s=>{s.mesh.position.y=.2+Math.sin(t*1.6+s.slot)*.05}),cloudsList.forEach(s=>{s.position.x+=s.userData.speed*e,s.position.x>220&&(s.position.x=-220),s.userData.groundShadow&&(s.userData.groundShadow.position.x=s.position.x+10,s.userData.groundShadow.position.z=s.position.z+8)}),animatedRoofProps.forEach(s=>{s.rotation.y+=1.2*e}),updateSmartTrafficSystem(e),dronesList.forEach((s,i)=>{const l=s.userData,m=l.angle+t*l.speed;s.position.set(Math.cos(m)*l.radius,l.height+Math.sin(t*2.2+i)*1.6,Math.sin(m)*l.radius-85),s.rotation.y+=1.8*e}),islandBirdsList.forEach((s,i)=>{const l=s.userData,m=l.angle+t*l.speed,d=VICTORY_ISLAND.centerX+Math.cos(m)*l.radius,w=VICTORY_ISLAND.centerZ+Math.sin(m)*l.radius,p=l.height+Math.sin(t*2.5+i)*1.1;s.position.set(d,p,w),s.rotation.y=-m;const u=Math.sin(t*12+l.flapOffset)*.55;l.leftWing.rotation.z=u,l.rightWing.rotation.z=-u}),updateIslandLife(t,e),myAvatarMesh&&myPlayer.hasJoinedGame){myPlayer.inCar&&!canUseCarNow()&&setCarState(!1),updateMyBusRide(),aesShuttleTick(e);const s=equipKeyOf(myPlayer.equip,myPlayer.inCar);myAvatarMesh.userData.equipKey!==s&&applyEquipToMesh(myAvatarMesh,myPlayer.equip,myPlayer.inCar)}const o=gamePhase==="waiting"||gamePhase==="explore"||gamePhase==="walk_to_dock",a=(gamePhase==="race"||gamePhase==="reflection")&&myPlayer.finishedRace;if(o||a){const s=myPlayer.hasJoinedGame&&((gamePhase==="explore"||gamePhase==="walk_to_dock")&&!myPlayer.atDock||a)&&!isTeacher3DMonitor&&!myPlayer.rideDriverId&&!window.__aesShuttle;let i=joystickVector.x,l=joystickVector.y;moveKeys.up&&(l-=1),moveKeys.down&&(l+=1),moveKeys.left&&(i-=1),moveKeys.right&&(i+=1);let m=!1;const d=s&&(Math.abs(i)>.05||Math.abs(l)>.05),w=-Math.sin(cameraYaw),p=-Math.cos(cameraYaw),u=Math.cos(cameraYaw),H=-Math.sin(cameraYaw);if(!s)walkVel.x=0,walkVel.z=0;else{const E=1-Math.exp(-e*11);walkVel.x+=((d?(u*i+w*-l)*(myPlayer.inCar==="bus"?32:myPlayer.inCar?40:WALK_SPEED):0)-walkVel.x)*E,walkVel.z+=((d?(H*i+p*-l)*(myPlayer.inCar==="bus"?32:myPlayer.inCar?40:WALK_SPEED):0)-walkVel.z)*E}const M=Math.hypot(walkVel.x,walkVel.z);if(walkAmt+=(Math.min(1,M/WALK_SPEED)-walkAmt)*(1-Math.exp(-e*10)),s&&M>.25){m=!0,d&&!myPlayer.inCar&&playSoundEffect("step");let E=1;a&&Math.hypot(myPlayer.x-VICTORY_ISLAND.centerX,myPlayer.z-VICTORY_ISLAND.centerZ)>ISLAND_SHORE_R&&(E=.6);const g=walkVel.x*e*E,f=walkVel.z*e*E;let R=myPlayer.x+g,y=myPlayer.z+f;if(a){const h=R-VICTORY_ISLAND.centerX,x=y-VICTORY_ISLAND.centerZ,T=Math.hypot(h,x);if(T>ISLAND_WADE_R&&(R=VICTORY_ISLAND.centerX+h/T*ISLAND_WADE_R,y=VICTORY_ISLAND.centerZ+x/T*ISLAND_WADE_R,n-(window._wadeToastAt||0)>4e3)){window._wadeToastAt=n;try{showCoinToast("🌊 Batas aman! Main air hanya boleh di pinggir pantai")}catch{}}}else R=Math.max(-175,Math.min(175,R)),y=Math.max(-272,Math.min(66,y));const c=resolveSolidCollisions(R,y,myPlayer.inCar==="bus"?6:myPlayer.inCar?3:1.15);myPlayer.x=c.x,myPlayer.z=c.z;{let h=Math.atan2(g,f)-myPlayer.rotY;h=Math.atan2(Math.sin(h),Math.cos(h)),myPlayer.rotY+=h*(1-Math.exp(-e*14))}d&&Math.abs(i)>.2&&(cameraYaw-=i*1.4*e)}if(myAvatarMesh&&myPlayer.hasJoinedGame){{const y=a?islandGroundY(myPlayer.x,myPlayer.z)+.05:groundHeightAt(myPlayer.x,myPlayer.z)+.1+(myPlayer.rideDriverId?BUS_LIFT:vehicleLift(myPlayer.inCar)),c=myAvatarMesh.position.y;myAvatarMesh.position.set(myPlayer.x,Math.abs(y-c)<.002?y:c+(y-c)*(1-Math.exp(-e*16)),myPlayer.z)}myAvatarMesh.rotation.y=myPlayer.rotY;const{leftLeg:E,rightLeg:g,leftArm:f,rightArm:R}=myAvatarMesh.userData;if(E&&g){const y=myPlayer.inCar?0:walkAmt;E.rotation.x=Math.sin(t*8)*.65*y,g.rotation.x=-Math.sin(t*8)*.65*y,f.rotation.x=-Math.sin(t*8)*.55*y,R.rotation.x=Math.sin(t*8)*.55*y;const c=myAvatarMesh.userData.carGroup;c&&c.userData.wheels&&c.userData.wheels.forEach(h=>{h.rotation.x+=Math.sign(walkVel.x*Math.sin(myPlayer.rotY)+walkVel.z*Math.cos(myPlayer.rotY)||1)*M*e/(c.userData.wheelR||.62)})}}if(gamePhase==="walk_to_dock"&&!myPlayer.atDock&&!isTeacher3DMonitor&&myPlayer.hasJoinedGame){const E=Math.hypot(DOCK_TARGET.x-myPlayer.x,DOCK_TARGET.z-myPlayer.z),g=document.getElementById("dock-distance-text");g&&(g.textContent=`Jarak ke Dermaga: ${Math.ceil(E)} meter`),overheadArrowGroup&&(overheadArrowGroup.visible=!0,overheadArrowGroup.position.set(myPlayer.x,6.4,myPlayer.z),overheadArrowGroup.rotation.y=Math.atan2(DOCK_TARGET.x-myPlayer.x,DOCK_TARGET.z-myPlayer.z)),E<6.8&&(playSoundEffect("complete_building"),myPlayer.atDock=!0,myPlayer.currentBuilding="Siap di Dermaga Perahu",setArrowGuideVisibility(!1),document.getElementById("walk-to-dock-banner").classList.add("hidden"),document.getElementById("ready-on-boat-banner").classList.remove("hidden"),myAvatarMesh&&(myAvatarMesh.visible=!1),myBoatMesh&&(myBoatMesh.visible=!0,myBoatMesh.position.set(BOAT_START_POS.x,.2,BOAT_START_POS.z)),broadcastMyState())}if(isTeacher3DMonitor||!myPlayer.hasJoinedGame){const E=teacherFollowPlayerId?otherPlayers[teacherFollowPlayerId]:null;if(E){const g=E.targetX||0,f=E.targetZ||0,R=Math.max(.08,cameraPitch),y=cameraDistance*Math.cos(R),c=cameraDistance*Math.sin(R);camera.position.lerp(new THREE.Vector3(g+Math.sin(cameraYaw)*y,3.5+c,f+Math.cos(cameraYaw)*y),.14),camera.lookAt(g,3.2,f)}else if(gamePhase==="reflection")camera.position.lerp(new THREE.Vector3(VICTORY_ISLAND.centerX-45,28,VICTORY_ISLAND.centerZ+35),.08),camera.lookAt(VICTORY_ISLAND.centerX,2,VICTORY_ISLAND.centerZ);else{const g=cameraDistance/6.5;camera.position.lerp(new THREE.Vector3(Math.sin(cameraYaw)*80*g,48*g+Math.max(0,cameraPitch)*30,Math.cos(cameraYaw)*80*g-35),.08),camera.lookAt(0,0,-60)}}else{const E=myPlayer.atDock&&!myPlayer.finishedRace&&myBoatMesh?myBoatMesh.position.x:myPlayer.x,g=myPlayer.atDock&&!myPlayer.finishedRace&&myBoatMesh?myBoatMesh.position.z:myPlayer.z,f=a?islandGroundY(myPlayer.x,myPlayer.z):.08,R=Math.max(.04,cameraPitch),y=cameraDistance*Math.cos(R),c=cameraDistance*Math.sin(R);camera.position.lerp(new THREE.Vector3(E+Math.sin(cameraYaw)*y,Math.max(f+2.1,f+2.9+c),g+Math.cos(cameraYaw)*y),1-Math.exp(-e*12)),camera.lookAt(E-Math.sin(cameraYaw)*6,f+3.4-cameraPitch*3.5,g-Math.cos(cameraYaw)*6)}(gamePhase==="explore"||gamePhase==="waiting")&&myPlayer.hasJoinedGame&&checkProximityToBuildings()}else if(gamePhase==="race"&&!myPlayer.finishedRace){const s=Math.max(1,gameConfig.questions.length);if(racePassiveDrift=Math.min(.18,racePassiveDrift+e*.0028),myBoatMesh&&myPlayer.hasJoinedGame){const i=myPlayer.boatStrokes/s,l=myPlayer.boatStrokes>=s?1:Math.min(.86,i*.85+racePassiveDrift),bs=aesBoatSlot(myPlayer.id),m=THREE.MathUtils.lerp(BOAT_START_POS.x,VICTORY_ISLAND.finishLineX,l)-bs.back*(1-l),d=THREE.MathUtils.lerp(BOAT_START_POS.z,VICTORY_ISLAND.finishLineZ,l)+bs.w,w=Math.hypot(m-myBoatMesh.position.x,d-myBoatMesh.position.z),p=Math.max(2.5,Math.min(15,w*1.8))*e;if(w>.01){const E=Math.min(1,p/w);myBoatMesh.position.x+=(m-myBoatMesh.position.x)*E,myBoatMesh.position.z+=(d-myBoatMesh.position.z)*E}myBoatMesh.position.y=.2+Math.sin(t*3.5)*.06;const u=w>1.2||n-myPlayer.lastRowTime<1400,H=u?13:4.5,M=u?.65:.32;if(myBoatMesh.userData.oar&&(myBoatMesh.userData.oar.rotation.y=Math.sin(t*H)*M),myBoatMesh.userData.pilotRobot){const{leftArm:E,rightArm:g}=myBoatMesh.userData.pilotRobot.userData;E&&g&&(E.rotation.x=Math.sin(t*H)*M,g.rotation.x=Math.sin(t*H)*M)}if(!isTeacher3DMonitor){const E=myBoatMesh.position.x-13+Math.sin(cameraYaw)*5,g=10.5+Math.max(0,cameraPitch)*6,f=myBoatMesh.position.z+10+Math.cos(cameraYaw)*4;camera.position.lerp(new THREE.Vector3(E,g,f),.1),camera.lookAt(myBoatMesh.position.x+18,2,myBoatMesh.position.z+8)}}if(isTeacher3DMonitor||!myPlayer.hasJoinedGame){const i=teacherFollowPlayerId?otherPlayers[teacherFollowPlayerId]:null;if(i&&i.boatMesh&&i.boatMesh.visible){const l=i.boatMesh.position.x,m=i.boatMesh.position.z,d=Math.max(.08,cameraPitch),w=cameraDistance*Math.cos(d),p=cameraDistance*Math.sin(d);camera.position.lerp(new THREE.Vector3(l-w,3.5+p,m+w*.7),.12),camera.lookAt(l+6,2.5,m)}else{const l=cameraDistance/6.5,m=25+Math.sin(cameraYaw)*35*l,d=32*l+Math.max(0,cameraPitch)*25,w=165+Math.cos(cameraYaw)*25*l;camera.position.lerp(new THREE.Vector3(m,d,w),.08),camera.lookAt(35,2,125)}}}const r=Math.max(1,gameConfig.questions.length);Object.values(otherPlayers).forEach((s,i)=>{if(s.mesh){const m=equipKeyOf(s.equip,s.inCar);s.mesh.userData.equipKey!==m&&applyEquipToMesh(s.mesh,s.equip,s.inCar)}const l=s.mesh&&s.rideDriverId?busDriverPose(s.rideDriverId):null;if(s.mesh&&s.mesh.visible&&l){const m=busSeatIndex(s.rideDriverId,s.id),d=BUS_SEATS[Math.max(0,m)%BUS_SEATS.length],w=busSeatWorld(l,d);s.mesh.position.set(w.x,groundHeightAt(w.x,w.z)+.1+BUS_LIFT,w.z),s.mesh.rotation.y=l.r,s.walkAmt=0;const p=s.mesh.userData;p&&p.leftLeg&&(p.leftLeg.rotation.x=0,p.rightLeg.rotation.x=0,p.leftArm.rotation.x=0,p.rightArm.rotation.x=0)}else if(s.mesh&&s.mesh.visible){const m=s.mesh.position.x,d=s.mesh.position.z,w=1-Math.exp(-e*14),p=Math.min(.25,(performance.now()-(s._lt||0))/1e3),u=(s.targetX||0)+(s.vx||0)*p,H=(s.targetZ||0)+(s.vz||0)*p;s.mesh.position.x=THREE.MathUtils.lerp(m,u,w);{const g=s.finishedRace?islandGroundY(s.mesh.position.x,s.mesh.position.z)+.05:groundHeightAt(s.mesh.position.x,s.mesh.position.z)+.1+vehicleLift(s.inCar);s.mesh.position.y+=(g-s.mesh.position.y)*(1-Math.exp(-e*12))}s.mesh.position.z=THREE.MathUtils.lerp(d,H,w);let M=(s.rotY||0)-s.mesh.rotation.y;M=Math.atan2(Math.sin(M),Math.cos(M)),s.mesh.rotation.y+=M*(1-Math.exp(-e*12));const E=s.mesh.userData;if(E&&E.leftLeg){const g=Math.hypot(s.mesh.position.x-m,s.mesh.position.z-d)/Math.max(e,.001);s.walkAmt=(s.walkAmt||0)+(Math.min(1,g/14)-(s.walkAmt||0))*(1-Math.exp(-e*10));const f=Math.sin(t*12+i)*(s.inCar?0:s.walkAmt);E.carGroup&&E.carGroup.userData.wheels&&E.carGroup.userData.wheels.forEach(R=>{R.rotation.x+=g*e/(E.carGroup.userData.wheelR||.62)}),E.leftLeg.rotation.x=f*.65,E.rightLeg.rotation.x=-f*.65,E.leftArm.rotation.x=-f*.55,E.rightArm.rotation.x=f*.55}}if(s.boatMesh&&s.boatMesh.visible){const m=Math.min(1,(s.boatStrokes||0)/r),d=(s.boatStrokes||0)>=r?1:Math.min(.86,m*.85+racePassiveDrift),bs=aesBoatSlot(Object.keys(otherPlayers)[i]),w=bs.w,p=THREE.MathUtils.lerp(BOAT_START_POS.x,VICTORY_ISLAND.finishLineX,d)-bs.back*(1-d),u=THREE.MathUtils.lerp(BOAT_START_POS.z,VICTORY_ISLAND.finishLineZ,d)+w,H=Math.hypot(p-s.boatMesh.position.x,u-s.boatMesh.position.z),M=Math.max(2.5,Math.min(15,H*1.8))*e;if(H>.01){const R=Math.min(1,M/H);s.boatMesh.position.x+=(p-s.boatMesh.position.x)*R,s.boatMesh.position.z+=(u-s.boatMesh.position.z)*R}s.boatMesh.position.y=.2+Math.sin(t*3.5+i)*.06;const E=H>1.2||n-(s.lastRowTime||0)<1400,g=E?13:4.5,f=E?.65:.32;if(s.boatMesh.userData.oar&&(s.boatMesh.userData.oar.rotation.y=Math.sin(t*g+i)*f),s.boatMesh.userData.pilotRobot){const{leftArm:R,rightArm:y}=s.boatMesh.userData.pilotRobot.userData;R&&y&&(R.rotation.x=Math.sin(t*g+i)*f,y.rotation.x=Math.sin(t*g+i)*f)}}}),n-lastMiniMapDraw>100&&(lastMiniMapDraw=n,renderMiniMapRadar()),AES_LITE&&aesLiteCull(n),updateLabelScaling(),renderer.render(scene,camera)}function checkProximityToBuildings(){if(myPlayer.insideBuilding){const o=gameConfig.buildings.findIndex(a=>a.id===myPlayer.insideBuilding);o>=0&&(myPlayer.currentBuilding=`🏢 Di dalam [G${o+1}] ${gameConfig.buildings[o].name}`);return}let e=null;for(const o of buildingColliders)if(Math.hypot(myPlayer.x-o.doorX,myPlayer.z-o.doorZ)<6.8){e=o;break}const t=document.getElementById("building-prompt"),n=document.getElementById("hud-location-indicator");e?(activeNearBuilding=e,myPlayer.currentBuilding=`[G${e.gIndex}] ${e.name}`,n.textContent=`📍 Di Pintu [G${e.gIndex}]: ${e.name}`,gamePhase==="explore"&&(document.getElementById("building-prompt-text").textContent=`KLIK BELAJAR [G${e.gIndex}]: ${e.name}`,t.classList.remove("hidden"))):(activeNearBuilding=null,myPlayer.currentBuilding="Jalan Raya Metropolis",n.textContent="📍 Lokasi: Jalan Raya Metropolis",t.classList.add("hidden"))}</script> <script>(function(){window.__aesBuild="AESC1-2026-10C8CD16";try{console.info("%c© 2026 AES CLASS. Seluruh hak cipta dilindungi. Dilarang menyalin, memodifikasi, merapikan ulang, atau mendistribusikan kode ini tanpa izin tertulis, termasuk dengan bantuan alat AI. [AESC1-2026-10C8CD16]","color:#0284c7;font-weight:bold")}catch{}})();const ACCESS_GATE={ENABLED:!0,GATE_STUDENTS:!1},LOCAL_LOGIN={SHARED_HASH:"b26e23c5166166afe6146caa4a584bb4ee0f4451c57a557836b69fdb887ac9ad",USERS:{}};let _gateProceed=null,gateMode="login",ADMIN_CRED=null,adminData=[],adminFilter="Menunggu";const $g=e=>document.getElementById(e);function gateMsg(e,t){const n=$g("gate-msg");n.textContent=e,n.style.color=t?"#6ee7b7":"#fcd34d"}function gateOpen(){$g("access-gate").style.display="block"}function gateClose(){$g("access-gate").style.display="none"}function sha256js(e){const t=new TextEncoder().encode(e),n=t.length,d=[];for(let i=2,s=0;s<64;i++){let r=!0;for(let o=2;o*o<=i;o++)if(i%o===0){r=!1;break}r&&(d[s++]=Math.pow(i,1/3)%1*4294967296|0)}let a=[];for(let i=2,s=0;s<8;i++){let r=!0;for(let o=2;o*o<=i;o++)if(i%o===0){r=!1;break}r&&(a[s++]=Math.sqrt(i)%1*4294967296|0)}const g=n+9+63>>6<<6,y=new Uint8Array(g);y.set(t),y[n]=128;const x=new DataView(y.buffer);x.setUint32(g-4,n*8>>>0),x.setUint32(g-8,Math.floor(n*8/4294967296));const c=(i,s)=>i>>>s|i<<32-s,f=new Int32Array(64);for(let i=0;i<g;i+=64){for(let l=0;l<16;l++)f[l]=x.getInt32(i+l*4);for(let l=16;l<64;l++){const m=f[l-15],b=f[l-2];f[l]=f[l-16]+(c(m,7)^c(m,18)^m>>>3)+f[l-7]+(c(b,17)^c(b,19)^b>>>10)|0}let[s,r,o,k,u,h,p,w]=a;for(let l=0;l<64;l++){const m=w+(c(u,6)^c(u,11)^c(u,25))+(u&h^~u&p)+d[l]+f[l]|0,b=(c(s,2)^c(s,13)^c(s,22))+(s&r^s&o^r&o)|0;w=p,p=h,h=u,u=k+m|0,k=o,o=r,r=s,s=m+b|0}a=[a[0]+s|0,a[1]+r|0,a[2]+o|0,a[3]+k|0,a[4]+u|0,a[5]+h|0,a[6]+p|0,a[7]+w|0]}return a.map(i=>(i>>>0).toString(16).padStart(8,"0")).join("")}async function sha256hex(e){if(window.crypto&&crypto.subtle)try{const t=await crypto.subtle.digest("SHA-256",new TextEncoder().encode(e));return[...new Uint8Array(t)].map(n=>n.toString(16).padStart(2,"0")).join("")}catch{}return sha256js(e)}const passHash=(e,t)=>sha256hex(e+":"+t+":aes-class"),sharedHash=e=>sha256hex("shared:"+e+":aes-class");async function gateCall(){throw new Error("Server dinonaktifkan")}let gateModeNow="login";function gateSetMode(e){gateModeNow="login",$g("gate-pass").classList.remove("hidden"),$g("gate-key").classList.add("hidden"),$g("gate-btn").textContent="Masuk",gateMsg("",!0)}function gateAdminToggle(){gateSetMode("login")}function expectedHashFor(e){return LOCAL_LOGIN.USERS[e]||LOCAL_LOGIN.SHARED_HASH||""}async function localLoginHash(e,t){return LOCAL_LOGIN.USERS[e]?await passHash(e,t):await sharedHash(t)}function gateGranted(e,t){try{sessionStorage.setItem("aes_user",JSON.stringify({email:e,h:t}))}catch{}if(gateClose(),_gateProceed){const n=_gateProceed;_gateProceed=null,n()}}async function gateSubmit(){const e=$g("gate-email").value.trim().toLowerCase(),t=$g("gate-pass").value,n=$g("gate-btn");if(!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(e)){gateMsg("Isi email yang valid.",!1);return}if(!t){gateMsg("Isi password.",!1);return}n.disabled=!0,gateMsg("Memeriksa...",!0);try{const d=await localLoginHash(e,t),a=expectedHashFor(e);a&&d===a?gateGranted(e,d):gateMsg("Email atau password salah.",!1)}catch{gateMsg("Gagal memeriksa password di browser ini.",!1)}n.disabled=!1}async function gateStart(e){if(!ACCESS_GATE.ENABLED){e();return}_gateProceed=e,gateSetMode("login");try{const t=JSON.parse(sessionStorage.getItem("aes_user")||"null");if(t&&t.email&&t.h&&t.h===expectedHashFor(t.email)){gateGranted(t.email,t.h);return}}catch{}gateOpen()}["gate-email","gate-pass","gate-key"].forEach(e=>{const t=document.getElementById(e);t&&t.addEventListener("keydown",n=>{n.key==="Enter"&&gateSubmit()})});let adminStats={total:0,totalLogin:0,hariIni:0,gagal:0};function adminActivate(e,t){ADMIN_CRED={email:e,key:t};try{sessionStorage.setItem("aes_admin",JSON.stringify(ADMIN_CRED))}catch{}$g("admin-fab").style.display="block"}const adminCall=(e,t)=>gateCall(e,Object.assign({email:ADMIN_CRED.email,key:ADMIN_CRED.key},t||{}));function adminOpen(){$g("admin-panel").style.display="block",adminRefresh()}function adminClose(){$g("admin-panel").style.display="none"}async function adminRefresh(){const e=$g("admin-info");e.textContent="Memuat data...";try{const t=await adminCall("list");if(!t.ok){e.textContent=t.status==="terkunci"?"Terlalu banyak percobaan salah. Coba lagi 15 menit lagi.":"Gagal: sesi admin tidak valid. Muat ulang halaman dan masuk lagi.";return}adminData=t.list||[],adminStats={total:t.total||0,totalLogin:t.totalLogin||0,hariIni:t.hariIni||0,gagal:t.gagal||0},e.textContent="",adminRender()}catch{e.textContent="Gagal terhubung ke server. Pastikan Code.gs terbaru sudah di-deploy."}}function adminRender(){const e=a=>String(a).replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;").replace(/"/g,"&quot;"),t=(a,g,y)=>`<div class="bg-slate-900/80 border border-slate-700 rounded-2xl p-3 text-center"><div class="text-2xl font-extrabold ${y}">${g}</div><div class="text-[11px] text-slate-400 font-bold mt-0.5">${a}</div></div>`;$g("admin-filters").innerHTML=t("Pengguna (email unik)",adminStats.total,"text-emerald-300")+t("Total login berhasil",adminStats.totalLogin,"text-sky-300")+t("Login hari ini",adminStats.hariIni,"text-amber-300")+t("Percobaan gagal",adminStats.gagal,"text-rose-300");const n=(($g("admin-search")||{}).value||"").trim().toLowerCase(),d=adminData.filter(a=>!n||String(a.email).toLowerCase().indexOf(n)>-1);$g("admin-list").innerHTML=d.length?d.map((a,g)=>`\n    <div class="bg-slate-900/80 border border-slate-700 rounded-2xl p-3 flex flex-col md:flex-row md:items-center justify-between gap-2">\n      <div class="min-w-0"><div class="font-extrabold text-white wrap-anywhere">${g+1}. ${e(a.email)}</div>\n        <div class="text-[11px] text-slate-400">Pertama masuk: ${e(a.pertama||"-")} • Terakhir: ${e(a.terakhir||"-")}</div></div>\n      <div class="shrink-0 px-3 py-1.5 bg-sky-500/20 border border-sky-400/40 rounded-xl text-xs font-extrabold text-sky-200">${e(a.jumlah)}x masuk</div>\n    </div>`).join(""):'<p class="text-sm text-slate-400 text-center py-8">Belum ada pengguna yang tercatat.</p>'}</script> <script>(function(){var c=document.documentElement,e=document.createElement("div");e.id="aes-hud-ctl",e.style.display="none";function s(a,n,d){var t=document.createElement("button");return t.textContent=a,t.title=d,t.onclick=function(){var m=c.classList.toggle(n);t.className=m?"off":""},t}var o=s("ℹ️","aes-hide-left","Info"),l=s("🗺️","aes-hide-map","Peta");e.appendChild(o),e.appendChild(l),document.body.appendChild(e);var i=window.matchMedia("(max-height:570px)");i.matches&&(c.classList.add("aes-hide-map"),l.className="off"),setInterval(function(){var a=document.getElementById("game-hud"),n=document.getElementById("teacher-clean-toggle-wrap"),d=a&&!a.classList.contains("hidden")&&i.matches&&!(n&&!n.classList.contains("hidden"));e.style.display=d?"flex":"none"},400)})();</script><script>window.addEventListener("load",function(){setTimeout(function(){var n=[];if(typeof tailwind>"u"&&n.push("Tailwind (cdn.tailwindcss.com)"),typeof THREE>"u"&&n.push("three.js (cdnjs.cloudflare.com)"),typeof mqtt>"u"&&n.push("MQTT (unpkg.com)"),typeof LZString>"u"&&n.push("LZ-String (cdnjs.cloudflare.com)"),typeof JSZip>"u"&&n.push("JSZip (cdnjs.cloudflare.com)"),!!n.length){var e=document.createElement("div");e.style.cssText="position:fixed;left:0;right:0;top:0;z-index:2147483647;background:#be123c;color:#fff;font:600 14px sans-serif;padding:10px 14px;text-align:center",e.textContent="Sebagian komponen gagal dimuat dari internet: "+n.join(", ")+". Cek koneksi, atau minta admin jaringan sekolah membuka situs itu, lalu muat ulang halaman.",document.body.appendChild(e)}},4e3)});</script> <!-- ===== AES CLASS • TAMBAHAN: LOMBA LARI (3D, jawab A/B/C/D) ===== -->
<style id="rn-style">
#rn-launch{position:fixed;right:.6rem;top:46%;z-index:9400;display:none;align-items:center;gap:6px;padding:9px 13px;border-radius:9999px;background:linear-gradient(135deg,#f97316,#ef4444);color:#fff;font:800 12px 'Plus Jakarta Sans',sans-serif;border:2px solid #fff;box-shadow:0 4px 18px rgba(239,68,68,.55);cursor:pointer;touch-action:manipulation}
#rn-launch:hover{filter:brightness(1.1)}
#rn-overlay{position:fixed;inset:0;z-index:9600;background:#0f172a;display:none;font-family:'Plus Jakarta Sans',"Noto Sans","Segoe UI","Noto Sans Arabic","Noto Sans Hebrew","Noto Sans JP","Hiragino Sans","Yu Gothic","Noto Sans KR","Malgun Gothic","Noto Sans SC","Microsoft YaHei","PingFang SC","Noto Sans TC","Noto Sans Devanagari","Nirmala UI","Noto Sans Thai","Arial Unicode MS",sans-serif;color:#f1f5f9;touch-action:manipulation;overflow:hidden}
#rn-overlay.rn-open{display:block}
#rn-canvas{position:absolute;inset:0}
#rn-canvas canvas{display:block;width:100%;height:100%}
#rn-speedfx{position:absolute;inset:0;pointer-events:none;opacity:0;transition:opacity .25s;background:radial-gradient(ellipse at 50% 45%,rgba(255,255,255,0) 45%,rgba(255,255,255,.28) 100%)}
#rn-hud{position:absolute;top:8px;left:8px;right:8px;display:flex;flex-wrap:wrap;gap:8px;align-items:flex-start;pointer-events:none;z-index:3}
.rn-card{background:rgba(15,23,42,.82);border:1px solid rgba(255,255,255,.28);border-radius:14px;padding:6px 12px;pointer-events:none}
#rn-exit{pointer-events:auto;width:38px;height:38px;border-radius:12px;background:rgba(15,23,42,.85);color:#fecaca;border:1px solid rgba(255,255,255,.35);font-size:16px;font-weight:800;cursor:pointer}
.rn-lbl{font-size:9px;font-weight:800;letter-spacing:.08em;color:#7dd3fc}
#rn-kmh{font-size:26px;font-weight:800;line-height:1;color:#fde047;font-variant-numeric:tabular-nums}
.rn-unit{font-size:10px;color:#cbd5e1;margin-left:3px}
.rn-bar{height:6px;border-radius:9px;background:rgba(255,255,255,.18);margin-top:4px;overflow:hidden;min-width:96px}
#rn-spdbar{display:block;height:100%;width:0;background:linear-gradient(90deg,#22c55e,#facc15,#ef4444);border-radius:9px}
.rn-spacer{flex:1 1 0}
#rn-place{font-size:26px;font-weight:800;line-height:1;color:#fff}
#rn-place small{font-size:12px;color:#94a3b8}
#rn-time{font-size:12px;font-weight:700;color:#bae6fd;font-variant-numeric:tabular-nums;text-align:right}
.rn-track{order:3;flex:1 1 100%;pointer-events:none}
#rn-trackbar{position:relative;height:16px;border-radius:9px;background:rgba(15,23,42,.78);border:1px solid rgba(255,255,255,.3);margin:2px 8px 0 4px}
#rn-trackbar .rn-dot{position:absolute;top:50%;width:11px;height:11px;border-radius:50%;transform:translate(-50%,-50%);border:2px solid #fff;transition:left .15s linear}
#rn-trackbar .rn-dot.me{width:16px;height:16px;z-index:5;box-shadow:0 0 10px #fff}
#rn-trackbar .rn-flag{position:absolute;right:-6px;top:-4px;font-size:15px}
#rn-dist{font-size:10px;font-weight:700;color:#e2e8f0;text-align:center;margin-top:2px;text-shadow:0 1px 3px #000}
#rn-fx{position:absolute;left:0;right:0;top:34%;text-align:center;pointer-events:none;z-index:4;font-size:clamp(22px,6vw,44px);font-weight:800;text-shadow:0 3px 14px rgba(0,0,0,.7);opacity:0}
#rn-fx.show{animation:rnpop .9s ease-out}
#rn-fx.ok{color:#4ade80}#rn-fx.bad{color:#fb7185}
#rn-flash{position:absolute;inset:0;pointer-events:none;z-index:2;opacity:0}
#rn-flash.ok.go{animation:rnflash .5s ease-out;box-shadow:inset 0 0 130px 40px rgba(74,222,128,.6)}
#rn-flash.bad.go{animation:rnflash .6s ease-out;box-shadow:inset 0 0 140px 50px rgba(244,63,94,.7)}
@keyframes rnflash{0%{opacity:1}100%{opacity:0}}
@keyframes rnpop{0%{opacity:0;transform:scale(.6) translateY(14px)}20%{opacity:1;transform:scale(1.15)}100%{opacity:0;transform:scale(1) translateY(-30px)}}
#rn-count{position:absolute;left:0;right:0;top:26%;text-align:center;font-size:clamp(60px,18vw,150px);font-weight:800;color:#fff;text-shadow:0 6px 30px rgba(0,0,0,.7);pointer-events:none;z-index:4}
#rn-qpanel{position:absolute;left:0;right:0;bottom:0;max-height:47vh;overflow-y:auto;padding:10px 12px calc(10px + env(safe-area-inset-bottom,0px));background:linear-gradient(to top,rgba(15,23,42,.97),rgba(15,23,42,.9));border-top:1px solid rgba(125,211,252,.5);z-index:3;touch-action:pan-y;display:none}
#rn-qpanel.show{display:block}
.rn-qhead{display:flex;align-items:center;justify-content:space-between;gap:8px;font-size:11px;font-weight:800;margin-bottom:5px}
.rn-chip{padding:2px 8px;border-radius:9999px;background:rgba(255,255,255,.12)}
.rn-chip.ok{color:#4ade80}.rn-chip.bad{color:#fb7185}.rn-chip.fire{color:#fdba74}
#rn-qtext{font-size:clamp(12px,2.6vw,17px);font-weight:700;line-height:1.35;margin-bottom:8px;overflow-wrap:anywhere}
#rn-qtext img,#rn-qimg{max-height:110px;border-radius:10px;margin:4px auto;display:block}
#rn-opts{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.rn-opt{display:flex;align-items:center;gap:8px;text-align:left;padding:8px 10px;min-height:48px;border-radius:12px;background:rgba(30,41,59,.95);border:2px solid rgba(255,255,255,.22);color:#fff;font:700 clamp(11px,2.3vw,15px) 'Plus Jakarta Sans',sans-serif;cursor:pointer;overflow-wrap:anywhere;touch-action:manipulation;transition:transform .08s}
.rn-opt:active{transform:scale(.97)}
.rn-opt b{flex:0 0 auto;width:28px;height:28px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:14px;color:#0f172a}
.rn-opt:nth-child(1) b{background:#38bdf8}.rn-opt:nth-child(2) b{background:#4ade80}.rn-opt:nth-child(3) b{background:#fbbf24}.rn-opt:nth-child(4) b{background:#fb7185}
.rn-opt.rn-ok{background:#15803d;border-color:#4ade80}
.rn-opt.rn-bad{background:#9f1239;border-color:#fb7185}
.rn-opt[disabled]{cursor:default}
#rn-fb{font-size:11px;font-weight:800;min-height:15px;margin-top:6px}
.rn-modal{position:absolute;inset:0;z-index:6;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.62);overflow-y:auto}
.rn-modal.rn-hide{display:none}
#rn-result{background:rgba(2,6,23,.3)}
.rn-box{width:min(94vw,470px);max-height:94vh;overflow-y:auto;background:#0f172a;border:2px solid rgba(125,211,252,.55);border-radius:20px;padding:18px 18px 16px;box-shadow:0 18px 60px rgba(0,0,0,.6)}
.rn-box h2{margin:0 0 4px;font-size:21px;font-weight:800;color:#fde047;text-align:center}
.rn-box p{margin:0 0 10px;font-size:12px;color:#cbd5e1;text-align:center;line-height:1.45}
.rn-rules{font-size:12px;color:#e2e8f0;line-height:1.5;background:rgba(255,255,255,.06);border-radius:12px;padding:8px 12px;margin-bottom:10px}
.rn-sel{margin-bottom:10px}
.rn-sel .rn-lbl{margin-bottom:4px}
.rn-seg{display:flex;gap:6px}
.rn-seg button{flex:1;padding:8px 4px;border-radius:10px;background:rgba(255,255,255,.08);border:2px solid transparent;color:#e2e8f0;font:800 11px 'Plus Jakarta Sans',sans-serif;cursor:pointer}
.rn-seg button.on{background:rgba(250,204,21,.18);border-color:#facc15;color:#fde047}
.rn-btn{width:100%;padding:12px;border-radius:14px;border:0;background:linear-gradient(135deg,#22c55e,#16a34a);color:#fff;font:800 15px 'Plus Jakarta Sans',sans-serif;cursor:pointer;margin-top:4px}
.rn-btn.alt{background:rgba(255,255,255,.1);font-size:12px;padding:9px}
.rn-btn:disabled{opacity:.5}
.rn-row{display:flex;align-items:center;gap:8px;padding:7px 10px;border-radius:10px;background:rgba(255,255,255,.06);margin-bottom:5px;font-size:12px;font-weight:700}
.rn-row.me{background:rgba(250,204,21,.2);border:1px solid #facc15}
.rn-row .pl{width:26px;font-weight:800;color:#fde047}
.rn-row .nm{flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.rn-row .tm{color:#bae6fd;font-variant-numeric:tabular-nums}
.rn-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:6px;margin:8px 0 10px}
.rn-stats div{background:rgba(255,255,255,.07);border-radius:10px;padding:6px 4px;text-align:center}
.rn-stats b{display:block;font-size:17px;color:#fff}
.rn-stats span{font-size:9px;color:#94a3b8;font-weight:700}
#rn-tpanel{position:fixed;inset:0;z-index:9650;font-family:'Plus Jakarta Sans',"Noto Sans","Segoe UI","Noto Sans Arabic","Noto Sans Hebrew","Noto Sans JP","Hiragino Sans","Yu Gothic","Noto Sans KR","Malgun Gothic","Noto Sans SC","Microsoft YaHei","PingFang SC","Noto Sans TC","Noto Sans Devanagari","Nirmala UI","Noto Sans Thai","Arial Unicode MS",sans-serif;color:#f1f5f9}
.rn-tnote{font-size:11px;color:#94a3b8;text-align:center;margin:6px 0}
@media (orientation:portrait){
 #rn-hud{gap:6px}
 .rn-card{padding:5px 9px}
 #rn-kmh,#rn-place{font-size:22px}
 .rn-bar{min-width:78px}
 #rn-qpanel{max-height:52vh}
 #rn-qtext{font-size:clamp(14px,4vw,18px)}
 .rn-opt{font:700 clamp(13px,3.7vw,16px) 'Plus Jakarta Sans',sans-serif;min-height:52px}
 #rn-fx{top:30%}
 #rn-count{top:22%}
 .rn-box{max-height:92vh}
}
@media (max-height:520px) and (orientation:landscape){
 #rn-qpanel{left:auto;right:8px;bottom:8px;top:104px;width:min(54vw,540px);max-height:none;border-radius:14px;border:1px solid rgba(125,211,252,.5)}
 #rn-kmh,#rn-place{font-size:19px}
 .rn-card{padding:4px 9px}
}
#rn-wboard{display:none;position:absolute;right:8px;top:64px;width:min(270px,46vw);max-height:calc(100% - 140px);flex-direction:column;z-index:4;background:rgba(15,23,42,.88);border:1px solid rgba(125,211,252,.45);border-radius:14px;padding:8px;color:#fff;font-family:'Plus Jakarta Sans',"Noto Sans","Segoe UI","Noto Sans Arabic","Noto Sans Hebrew","Noto Sans JP","Hiragino Sans","Yu Gothic","Noto Sans KR","Malgun Gothic","Noto Sans SC","Microsoft YaHei","PingFang SC","Noto Sans TC","Noto Sans Devanagari","Nirmala UI","Noto Sans Thai","Arial Unicode MS",sans-serif}
#rn-overlay.rn-watching #rn-wboard{display:flex}
#rn-overlay.rn-watching #rn-hud .rn-card{display:none}
#rn-wtitle{font-size:11px;font-weight:800;color:#7dd3fc;margin-bottom:6px}
#rn-wlist{overflow-y:auto;flex:1;min-height:40px}
#rn-wlist .rn-row{cursor:pointer}
#rn-whelp{font-size:10px;color:#fde047;font-weight:700;margin:0 0 5px}
#rn-wctl{display:none;position:absolute;left:8px;top:58px;z-index:4;flex-direction:column;gap:6px}
#rn-overlay.rn-watching #rn-wctl{display:flex}
#rn-wctl button{width:40px;height:40px;border-radius:12px;background:rgba(15,23,42,.88);color:#e0f2fe;border:1px solid rgba(125,211,252,.5);font-size:18px;font-weight:800;cursor:pointer;padding:0}
#rn-wctl button:active{background:rgba(14,165,233,.75)}
#rn-whint{display:none;position:absolute;left:50%;transform:translateX(-50%);bottom:10px;z-index:4;font-size:11px;font-weight:700;color:#bae6fd;background:rgba(15,23,42,.8);border:1px solid rgba(125,211,252,.35);border-radius:9999px;padding:5px 12px;pointer-events:none;white-space:nowrap;max-width:94vw;overflow:hidden;text-overflow:ellipsis}
#rn-overlay.rn-watching #rn-whint{display:block}
#rn-canvas{touch-action:none}
#rn-whead{display:flex;align-items:center;gap:6px;margin-bottom:6px}
#rn-whead #rn-wtitle{flex:1;margin-bottom:0}
#rn-wtoggle{flex:none;padding:5px 9px;border-radius:9px;border:1px solid rgba(125,211,252,.5);background:rgba(14,165,233,.25);color:#e0f2fe;font-size:11px;font-weight:800;cursor:pointer}
#rn-wboard.rn-wmin #rn-wlist,#rn-wboard.rn-wmin #rn-whelp,#rn-wboard.rn-wmin .rn-wbtns{display:none}
#rn-wboard.rn-wmin #rn-whead{margin-bottom:0}
@media (orientation:portrait){
 #rn-wboard{left:6px;right:6px;top:auto;bottom:calc(6px + env(safe-area-inset-bottom,0px));width:auto;max-height:34vh;padding:6px 8px}
 #rn-wlist{max-height:20vh}
 #rn-whint{display:none!important}
 #rn-wctl{left:auto;right:6px;top:calc(96px + env(safe-area-inset-top,0px));gap:5px}
 #rn-wctl button{width:36px;height:36px;font-size:16px;background:rgba(15,23,42,.7)}
}
#rn-wlist .rn-row i{display:inline-block;width:9px;height:9px;border-radius:50%;margin-right:5px}
.rn-wbtns{display:flex;gap:5px;margin-top:6px;flex-wrap:wrap}
.rn-wbtns button{flex:1;min-width:70px;padding:6px 4px;border-radius:9px;border:1px solid rgba(255,255,255,.3);background:rgba(255,255,255,.1);color:#fff;font-size:10px;font-weight:800;cursor:pointer}
</style>

<button id="rn-launch" type="button" onclick="AESRun.open()">🏃 LOMBA LARI</button>

<div id="rn-overlay">
 <div id="rn-canvas"></div>
 <div id="rn-speedfx"></div>
 <div id="rn-flash"></div>
 <div id="rn-hud">
  <button id="rn-exit" type="button" title="Keluar">✕</button>
  <div class="rn-card"><div class="rn-lbl">KECEPATAN</div><div><span id="rn-kmh">0</span><span class="rn-unit">km/jam</span></div><div class="rn-bar"><i id="rn-spdbar"></i></div></div>
  <div class="rn-spacer"></div>
  <div class="rn-card"><div class="rn-lbl" style="text-align:right">POSISI</div><div id="rn-place">#1<small>/6</small></div><div id="rn-time">00:00.0</div></div>
  <div class="rn-track"><div id="rn-trackbar"><span class="rn-flag">🏁</span></div><div id="rn-dist">0 / 400 m</div></div>
 </div>
 <div id="rn-wctl"><button type="button" data-w="in" title="Perbesar">＋</button><button type="button" data-w="out" title="Perkecil">－</button><button type="button" data-w="L" title="Putar ke kiri">↺</button><button type="button" data-w="R" title="Putar ke kanan">↻</button><button type="button" data-w="up" title="Naikkan sudut">⤒</button><button type="button" data-w="down" title="Turunkan sudut">⤓</button><button type="button" data-w="reset" title="Kembalikan tampilan">⌖</button></div>
 <div id="rn-whint">Geser layar = putar • cubit / scroll = zoom • ketuk nama siswa = lihat posisinya</div>
 <div id="rn-wboard"><div id="rn-whead"><div id="rn-wtitle"></div><button id="rn-wtoggle" type="button">Daftar ▾</button></div><div id="rn-whelp">👆 Ketuk nama siswa untuk melihat posisinya</div><div id="rn-wlist"></div><div class="rn-wbtns"><button id="rn-wauto" type="button">🎯 Ikuti pemimpin</button><button id="rn-wend" type="button">🏁 Akhiri lomba</button><button id="rn-wclose" type="button">✕ Tutup</button></div></div>
 <div id="rn-fx"></div>
 <div id="rn-count"></div>
 <div id="rn-qpanel">
  <div class="rn-qhead"><span id="rn-qno">Soal 1</span><span><span class="rn-chip ok" id="rn-cok">✓0</span> <span class="rn-chip bad" id="rn-cbad">✗0</span> <span class="rn-chip fire" id="rn-cstreak">🔥0</span></span></div>
  <div id="rn-qtext"></div>
  <div id="rn-opts"></div>
  <div id="rn-fb"></div>
 </div>

 <div id="rn-start" class="rn-modal">
  <div class="rn-box">
   <h2>🏃 LOMBA LARI AES CLASS</h2>
   <p id="rn-who">Siap, juara?</p>
   <div class="rn-rules">
    • Kamu <b>terus berlari</b> menuju garis finish.<br>
    • Pilih jawaban <b>A / B / C / D</b> (bisa juga tekan tombol keyboard A-D atau 1-4).<br>
    • Jawaban <b style="color:#4ade80">benar</b> = lari makin <b>cepat</b> 🚀. Jawaban <b style="color:#fb7185">salah</b> = <b>melambat</b> 🐢.<br>
    • Lomba kelas: lawanmu adalah <b>teman sekelas</b> yang ikut berlari di lintasan ini. Jadilah yang pertama finish!<br>• Mode latihan guru: lawan adalah pelari komputer.
   </div>
   <div class="rn-sel"><div class="rn-lbl">JARAK LINTASAN</div><div class="rn-seg" id="rn-seg-len"><button data-v="200">Sprint 200 m</button><button data-v="400" class="on">Standar 400 m</button><button data-v="800">Jauh 800 m</button></div></div>
   <div id="rn-best" style="font-size:11px;color:#94a3b8;text-align:center;margin-bottom:6px"></div>
   <button class="rn-btn" id="rn-go" type="button">▶ MULAI LOMBA</button>
   <button class="rn-btn alt" id="rn-close1" type="button">Tutup</button>
  </div>
 </div>

 <div id="rn-miss" class="rn-modal rn-hide">
  <div class="rn-box">
   <h2>🏁 LOMBA SEDANG BERLANGSUNG</h2>
   <p id="rn-miss-t">Guru sudah memulai lomba lari, tetapi kamu belum ikut. Pelarimu berdiri diam di garis start. Tunggu guru mengakhiri lomba — skormu akan muncul di sini.</p>
   <button class="rn-btn alt" id="rn-close3" type="button">Tutup</button>
  </div>
 </div>

 <div id="rn-result" class="rn-modal rn-hide">
  <div class="rn-box">
   <h2 id="rn-rtitle">🏁 FINISH!</h2>
   <p id="rn-rsub"></p>
   <div class="rn-stats" id="rn-rstats"></div>
   <div id="rn-rtable"></div>
   <button class="rn-btn" id="rn-again" type="button">🔄 Main Lagi</button>
   <button class="rn-btn alt" id="rn-close2" type="button">Tutup</button>
  </div>
 </div>
</div>

<div id="rn-tpanel" class="rn-modal rn-hide">
 <div class="rn-box">
  <h2>🏃 LOMBA LARI • PANEL GURU</h2>
  <p>Tekan <b>MULAI</b>: lomba langsung berjalan di layar semua siswa yang sudah masuk. Siswa saling berlomba satu sama lain secara langsung (tanpa pelari komputer), jadi guru tidak perlu memilih lawan. Soal diambil dari bank soal yang diatur di kolom <b>Edit</b> pada halaman awal. Siswa yang tertinggal atau belum membuka aplikasi hanya berdiri diam di garis start; skornya muncul begitu guru menekan <b>Akhiri</b>.</p>
  <div class="rn-sel"><div class="rn-lbl">JARAK LINTASAN</div><div class="rn-seg" id="rn-t-seg-len"><button data-v="200">Sprint 200 m</button><button data-v="400" class="on">Standar 400 m</button><button data-v="800">Jauh 800 m</button></div></div>
  <button class="rn-btn" id="rn-t-go" type="button">📣 MULAI LOMBA SEMUA SISWA</button>
  <button class="rn-btn" id="rn-t-watch" type="button">👁 TONTON LOMBA LANGSUNG</button>
  <button class="rn-btn alt" id="rn-t-stop" type="button">🏁 Akhiri lomba &amp; umumkan skor</button>
  <div id="rn-t-stat" class="rn-tnote"></div>
  <div id="rn-t-table"></div>
  <button class="rn-btn alt" id="rn-t-docx" type="button">📄 Unduh nilai lomba (Word)</button>
  <button class="rn-btn alt" id="rn-t-self" type="button">🎮 Coba sendiri (latihan guru)</button>
  <button class="rn-btn alt" id="rn-t-close" type="button">Tutup panel</button>
 </div>
</div>

<script id="rn-script">
(function(){
"use strict";
if(window.AESRun)return;

/* ---------- helper aman (memakai fungsi bawaan aplikasi bila ada) ---------- */
var $=function(id){return document.getElementById(id)};
function esc(s){return String(s==null?"":s).replace(/[&<>"]/g,function(c){return{"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]})}
function rich(s){try{if(typeof formatRichEducationalText==="function")return formatRichEducationalText(s,1)}catch(e){}return esc(s)}
function typeset(a){try{if(typeof triggerMathJaxRender==="function")triggerMathJaxRender(a)}catch(e){}}
function sfx(n){try{if(typeof playSoundEffect==="function")playSoundEffect(n)}catch(e){}}
function clamp(v,a,b){return v<a?a:v>b?b:v}
function rnd(a,b){return a+Math.random()*(b-a)}
function shuffle(a){for(var i=a.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1)),t=a[i];a[i]=a[j];a[j]=t}return a}

function getQs(){
  try{
    var qs=(typeof gameConfig!=="undefined"&&gameConfig&&gameConfig.questions)||[];
    return qs.filter(function(q){return q&&q.q&&Array.isArray(q.options)&&q.options.filter(function(o){return String(o||"").trim()}).length>=2});
  }catch(e){return[]}
}
function optOrder(q){
  try{if(typeof getShuffledOrder==="function")return getShuffledOrder(q.options)}catch(e){}
  var idx=[];q.options.forEach(function(o,i){if(String(o||"").trim())idx.push(i)});return shuffle(idx);
}
function myName(){try{return(myPlayer&&myPlayer.name)||(typeof isTeacherMode!=="undefined"&&isTeacherMode?"Guru":"Kamu")}catch(e){return"Kamu"}}
function myColor(){try{return(myPlayer&&myPlayer.color)||"#0ea5e9"}catch(e){return"#0ea5e9"}}
function otherNames(){
  var pool=[];
  try{(gameConfig.students||[]).forEach(function(n){n=String(n||"").trim();if(n&&n!==myName())pool.push(n)})}catch(e){}
  shuffle(pool);
  var fb=shuffle(["Rani","Dimas","Putri","Fajar","Salsa","Rizky","Nadia","Bagas"]);
  while(pool.length<5)pool.push(fb.pop()||("Lawan "+pool.length));
  return pool.slice(0,5);
}

/* ---------- konstanta permainan ---------- */
var NLANE=6,LANEW=2.4,TRACKW=NLANE*LANEW;
function setLanes(n){NLANE=n;TRACKW=NLANE*LANEW}
var BASEV=4.5,MINV=1.6,MAXV=15,BOOST=1.5,SLOW=2.1;
/* TARGET SOAL: jarak yang boleh ditempuh = jumlah jawaban benar / target soal x panjang lintasan */
function qNeed(){return S.L<=200?8:S.L<=400?12:16}
var CREEP=BASEV*.18; /* kecepatan merayap saat belum menjawab: tetap bergerak, tapi pelan */
function capQ(r){var n=qNeed();return r.correct>=n?Infinity:S.L*r.correct/n}
var LEVELS=[{acc:[.35,.6],think:[5,8]},{acc:[.55,.8],think:[4,6.5]},{acc:[.75,.95],think:[3,5]}];
var BOTCOL=["#ef4444","#f59e0b","#22c55e","#a855f7","#ec4899","#14b8a6"];

/* ---------- state ---------- */
var S={open:false,state:"idle",L:400,lvl:1,raf:0,last:0,T:0,cd:0,cdStep:0,timers:[],
  renderer:null,scene:null,camera:null,racers:[],me:null,finishCount:0,
  qList:[],qPtr:0,cur:null,locked:true,streak:0,bestStreak:0,maxV:0,stumble:0,remote:{},follow:null,freeLanes:[],laneX:null,pubT:0,pubN:0,fovT:60,resultShown:false,lastQ:-1,shake:0,kick:0,roll:0,orbit:0,fwT:0,fwN:0,ps:null,rings:[],streaks:[],streakMat:null,neonMats:[],finNeon:null,sky:null,lowFx:false};

function later(fn,ms){var id=setTimeout(function(){fn()},ms);S.timers.push(id);return id}
function clearTimers(){S.timers.forEach(clearTimeout);S.timers=[]}

/* ---------- tombol peluncur ---------- */
function canShowLauncher(){
  if(S.open)return false;
  var tp=$("rn-tpanel");if(tp&&!tp.classList.contains("rn-hide"))return false;
  var hud=$("game-hud"),ts=$("teacher-screen");
  var hudOn=hud&&!hud.classList.contains("hidden"),tsOn=ts&&!ts.classList.contains("hidden");
  try{
    if(typeof isTeacherMode!=="undefined"&&isTeacherMode)return !!(hudOn||tsOn);
    // siswa: tombol LOMBA LARI tidak ditampilkan (lomba lari hanya diatur oleh guru)
    return false;
  }catch(e){return false}
}
setInterval(function(){var b=$("rn-launch");if(b)b.style.display=canShowLauncher()?"flex":"none"},500);

/* ---------- 3D ---------- */
function textTex(text,w,h,o){
  var c=document.createElement("canvas");c.width=w;c.height=h;var x=c.getContext("2d");
  if(o.bg){x.fillStyle=o.bg;x.fillRect(0,0,w,h)}
  x.fillStyle=o.fg||"#fff";x.font=o.font||"bold 40px sans-serif";x.textAlign="center";x.textBaseline="middle";x.fillText(text,w/2,h/2);
  var t=new THREE.CanvasTexture(c);t.anisotropy=4;return t;
}
function nameSprite(name,color,isMe){
  var c=document.createElement("canvas");c.width=320;c.height=72;var x=c.getContext("2d");
  x.fillStyle=isMe?"rgba(250,204,21,.95)":"rgba(15,23,42,.82)";
  var r=30;x.beginPath();x.moveTo(r,4);x.lineTo(320-r,4);x.quadraticCurveTo(316,4,316,r);x.lineTo(316,72-r);x.quadraticCurveTo(316,68,320-r,68);x.lineTo(r,68);x.quadraticCurveTo(4,68,4,72-r);x.lineTo(4,r);x.quadraticCurveTo(4,4,r,4);x.fill();
  x.fillStyle=isMe?"#0f172a":"#fff";x.font="bold 34px sans-serif";x.textAlign="center";x.textBaseline="middle";
  var t=String(name);if(t.length>14)t=t.slice(0,13)+"…";x.fillText(t,160,38);
  var tex=new THREE.CanvasTexture(c);var sp=new THREE.Sprite(new THREE.SpriteMaterial({map:tex,transparent:true,depthWrite:false}));
  sp.scale.set(2.0,.45,1);return sp;
}
function makeRunnerBasic(color,name,isMe){
  var g=new THREE.Group(),L=function(c){return new THREE.MeshLambertMaterial({color:c})};
  var skin=L(0xf5cfa5),shirt=L(new THREE.Color(color)),shorts=L(0x1e293b),shoe=L(0xf8fafc);
  var body=new THREE.Group();g.add(body);
  var torso=new THREE.Mesh(new THREE.BoxGeometry(.56,.72,.3),shirt);torso.position.y=1.2;body.add(torso);
  var hips=new THREE.Mesh(new THREE.BoxGeometry(.56,.26,.32),shorts);hips.position.y=.78;body.add(hips);
  var head=new THREE.Mesh(new THREE.SphereGeometry(.23,14,12),skin);head.position.y=1.78;body.add(head);
  var hair=new THREE.Mesh(new THREE.SphereGeometry(.245,14,10,0,Math.PI*2,0,Math.PI*.52),L(0x1f2937));hair.position.y=1.80;body.add(hair);
  [-.09,.09].forEach(function(ex){var e=new THREE.Mesh(new THREE.BoxGeometry(.05,.06,.02),L(0x0f172a));e.position.set(ex,1.80,-.215);body.add(e)});
  function limb(x,y,w,h,mat,tip){
    var p=new THREE.Group();p.position.set(x,y,0);
    var m=new THREE.Mesh(new THREE.BoxGeometry(w,h,w),mat);m.position.y=-h/2;p.add(m);
    if(tip){var s=new THREE.Mesh(new THREE.BoxGeometry(w+.02,.1,w+.18),tip);s.position.set(0,-h+.03,-.05);p.add(s)}
    body.add(p);return p;
  }
  var armL=limb(-.4,1.5,.14,.62,skin),armR=limb(.4,1.5,.14,.62,skin);
  var legL=limb(-.14,.72,.19,.72,skin,shoe),legR=limb(.14,.72,.19,.72,skin,shoe);
  var sp=nameSprite(name,color,isMe);sp.position.y=2.55;g.add(sp);
  if(isMe){var ar=new THREE.Mesh(new THREE.ConeGeometry(.2,.38,4),new THREE.MeshBasicMaterial({color:0xfacc15}));ar.rotation.x=Math.PI;ar.position.y=3.05;g.add(ar);g.userData.arrow=ar}
  g.userData={body:body,armL:armL,armR:armR,legL:legL,legR:legR,arrow:g.userData.arrow};
  return g;
}


/* ---------- karakter: robot ASLI aplikasi (sama dengan avatar di kota) ---------- */
var RS=.6,_shTex=null;
function blobShadow(){
  if(!_shTex){var c=document.createElement("canvas");c.width=c.height=64;var x=c.getContext("2d");var gr=x.createRadialGradient(32,32,2,32,32,30);gr.addColorStop(0,"rgba(0,0,0,.6)");gr.addColorStop(1,"rgba(0,0,0,0)");x.fillStyle=gr;x.fillRect(0,0,64,64);_shTex=new THREE.CanvasTexture(c)}
  var m=new THREE.Mesh(new THREE.PlaneGeometry(1.8,1.8),new THREE.MeshBasicMaterial({map:_shTex,transparent:true,depthWrite:false}));
  m.rotation.x=-Math.PI/2;m.position.y=.04;return m;
}
function randEquip(){
  var e={},r=Math.random;
  if(r()<.5)e.head=["hat_cap","hat_magic","crown"][Math.floor(r()*3)];
  if(r()<.35)e.face="glasses";if(r()<.3)e.neck="bowtie";if(r()<.3)e.back="cape";
  if(r()<.25)e.pack="backpack";if(r()<.2)e.wrist="watch";if(r()<.25)e.body="jacket";
  return e;
}
function makeRunner(color,name,isMe,equip){
  var robot=null;
  try{if(typeof createRobotCharacterMesh==="function")robot=createRobotCharacterMesh(name,color)}catch(e){robot=null}
  if(!robot)return makeRunnerBasic(color,name,isMe);
  var g=new THREE.Group(),ns=robot.userData.nameSprite;
  if(ns){robot.remove(ns);try{ns.material.map.dispose();ns.material.dispose()}catch(e){}}
  try{if(equip&&typeof applyEquipToMesh==="function")applyEquipToMesh(robot,equip,null)}catch(e){}
  var pivot=new THREE.Group();robot.rotation.y=Math.PI;robot.scale.setScalar(RS);pivot.add(robot);g.add(pivot);
  g.add(blobShadow());
  var sp=nameSprite(name,color,isMe);sp.position.y=3.75;g.add(sp);
  var arrow=null;
  if(isMe){arrow=new THREE.Mesh(new THREE.ConeGeometry(.22,.4,4),new THREE.MeshBasicMaterial({color:0xfacc15}));arrow.rotation.x=Math.PI;arrow.position.y=4.25;g.add(arrow)}
  var u=robot.userData;
  g.userData={body:pivot,robot:robot,armL:u.leftArm,armR:u.rightArm,legL:u.leftLeg,legR:u.rightLeg,arrow:arrow};
  return g;
}

/* ---------- sistem partikel (debu, api booster, percikan, kembang api, konfeti) ---------- */
var PV="attribute float size;attribute vec4 color4;uniform float uScale;varying vec4 vC;void main(){vC=color4;vec4 mv=modelViewMatrix*vec4(position,1.0);gl_PointSize=max(0.0,size*uScale/max(0.1,-mv.z));gl_Position=projectionMatrix*mv;}";
var PF="varying vec4 vC;void main(){float d=length(gl_PointCoord-vec2(0.5))*2.0;float a=smoothstep(1.0,0.12,d);gl_FragColor=vec4(vC.rgb,vC.a*a);}";
function PS(max,additive){
  this.max=max;this.k=0;
  this.P=new Float32Array(max*3);this.C=new Float32Array(max*4);this.Z=new Float32Array(max);
  this.V=new Float32Array(max*3);this.L=new Float32Array(max);this.M=new Float32Array(max);
  this.A=new Float32Array(max*2);this.R=new Float32Array(max*4);this.G=new Float32Array(max);
  var geo=new THREE.BufferGeometry();
  geo.setAttribute("position",new THREE.BufferAttribute(this.P,3));
  geo.setAttribute("color4",new THREE.BufferAttribute(this.C,4));
  geo.setAttribute("size",new THREE.BufferAttribute(this.Z,1));
  this.geo=geo;
  this.mat=new THREE.ShaderMaterial({uniforms:{uScale:{value:600}},vertexShader:PV,fragmentShader:PF,transparent:true,depthWrite:false,blending:additive?THREE.AdditiveBlending:THREE.NormalBlending});
  this.pts=new THREE.Points(geo,this.mat);this.pts.frustumCulled=false;
}
PS.prototype.emit=function(x,y,z,vx,vy,vz,life,s0,s1,r,g,b,a,grav){
  var i=this.k;this.k=(i+1)%this.max;var i3=i*3;
  this.P[i3]=x;this.P[i3+1]=y;this.P[i3+2]=z;this.V[i3]=vx;this.V[i3+1]=vy;this.V[i3+2]=vz;
  this.L[i]=life;this.M[i]=life;this.A[i*2]=s0;this.A[i*2+1]=s1;
  this.R[i*4]=r;this.R[i*4+1]=g;this.R[i*4+2]=b;this.R[i*4+3]=a;this.G[i]=grav||0;
};
PS.prototype.update=function(dt){
  for(var i=0;i<this.max;i++){
    var l=this.L[i];
    if(l<=0){this.Z[i]=0;continue}
    l-=dt;this.L[i]=l;
    if(l<=0){this.Z[i]=0;this.C[i*4+3]=0;continue}
    var i3=i*3,t=1-l/this.M[i],g=this.G[i];
    this.V[i3+1]-=g*dt;
    this.P[i3]+=this.V[i3]*dt;this.P[i3+1]+=this.V[i3+1]*dt;this.P[i3+2]+=this.V[i3+2]*dt;
    if(g>0&&this.P[i3+1]<.05){this.P[i3+1]=.05;this.V[i3+1]*=-.3;this.V[i3]*=.7;this.V[i3+2]*=.7}
    this.Z[i]=this.A[i*2]+(this.A[i*2+1]-this.A[i*2])*t;
    this.C[i*4]=this.R[i*4];this.C[i*4+1]=this.R[i*4+1];this.C[i*4+2]=this.R[i*4+2];
    this.C[i*4+3]=this.R[i*4+3]*(1-t)*Math.min(1,t*12+.2);
  }
  var a=this.geo.attributes;a.position.needsUpdate=true;a.color4.needsUpdate=true;a.size.needsUpdate=true;
};

function ringAt(r,hex){
  for(var i=0;i<S.rings.length;i++){var R=S.rings[i];if(R.t<=0){R.t=.001;R.f=r;R.mesh.material.color.setHex(hex);R.mesh.visible=true;return}}
}
function burstGood(r){
  var G=S.ps.glow,n=S.lowFx?24:46;
  ringAt(r,0x4ade80);
  for(var i=0;i<n;i++){var a=Math.random()*6.283,sp=rnd(3,8);G.emit(r.x,1.1,-r.dist,Math.cos(a)*sp,rnd(1.5,5),Math.sin(a)*sp,rnd(.5,.95),.5,.08,Math.random()<.5?.3:1,1,Math.random()<.5?.4:.2,1,7)}
  r.boost=1.3;
}
function burstBad(r){
  var G=S.ps.glow,D=S.ps.dust;
  ringAt(r,0xfb7185);
  for(var i=0;i<30;i++){var a=Math.random()*6.283,sp=rnd(2,6);G.emit(r.x,1.0,-r.dist,Math.cos(a)*sp,rnd(1,4),Math.sin(a)*sp,rnd(.4,.8),.4,.05,1,rnd(.2,.5),.15,1,9)}
  for(var j=0;j<14;j++)D.emit(r.x+rnd(-.3,.3),.5,-r.dist+rnd(-.3,.3),rnd(-1.2,1.2),rnd(.8,2),rnd(-1,2),rnd(.8,1.3),.7,2.2,.35,.35,.38,.55,-.2);
}
function fireworkAt(x,y,z){
  var G=S.ps.glow,c=new THREE.Color().setHSL(Math.random(),1,.6),n=S.lowFx?40:70;
  for(var i=0;i<n;i++){var th=Math.random()*6.283,ph=Math.acos(rnd(-1,1)),sp=rnd(5,12);G.emit(x,y,z,Math.sin(ph)*Math.cos(th)*sp,Math.cos(ph)*sp,Math.sin(ph)*Math.sin(th)*sp,rnd(1.1,1.8),.9,.1,c.r,c.g,c.b,1,5)}
}
function confetti(x,z){
  var C=S.ps.conf,c=new THREE.Color(),n=S.lowFx?70:140;
  for(var i=0;i<n;i++){c.setHSL(Math.random(),.9,.6);C.emit(x+rnd(-7,7),rnd(7,13),z+rnd(-9,5),rnd(-.8,.8),rnd(-.5,.5),rnd(-.8,.8),rnd(3,4.5),.38,.3,c.r,c.g,c.b,1,.7)}
}
function respawnStreak(m,init){
  var cam=S.camera,side=Math.random()<.5?-1:1;
  m.position.set(cam.position.x+side*rnd(1.6,7),Math.max(.25,cam.position.y+rnd(-1.4,3.2)),cam.position.z-(init?rnd(2,60):rnd(45,70)));
}
function makeSky(scene){
  var g=new THREE.Group();
  var mat=new THREE.ShaderMaterial({side:THREE.BackSide,depthWrite:false,fog:false,
    vertexShader:"varying vec3 vP;void main(){vP=position;gl_Position=projectionMatrix*modelViewMatrix*vec4(position,1.0);}",
    fragmentShader:"varying vec3 vP;void main(){float h=normalize(vP).y;vec3 hor=vec3(1.0,.86,.71);vec3 mid=vec3(.45,.74,.96);vec3 top=vec3(.1,.33,.78);vec3 c=mix(hor,mid,smoothstep(0.0,.28,h));c=mix(c,top,smoothstep(.2,.85,h));if(h<0.0)c=hor;gl_FragColor=vec4(c,1.0);}"});
  var dome=new THREE.Mesh(new THREE.SphereGeometry(520,24,14),mat);dome.renderOrder=-10;g.add(dome);
  var c=document.createElement("canvas");c.width=c.height=128;var x=c.getContext("2d"),gr=x.createRadialGradient(64,64,0,64,64,64);
  gr.addColorStop(0,"rgba(255,255,235,1)");gr.addColorStop(.18,"rgba(255,236,170,.95)");gr.addColorStop(.5,"rgba(255,190,110,.35)");gr.addColorStop(1,"rgba(255,160,90,0)");x.fillStyle=gr;x.fillRect(0,0,128,128);
  var sp=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(c),transparent:true,depthWrite:false,fog:false,blending:THREE.AdditiveBlending}));
  sp.scale.set(200,200,1);sp.position.set(-190,95,-440);g.add(sp);scene.add(g);return g;
}
function trackTex(L){
  var c=document.createElement("canvas");c.width=c.height=128;var x=c.getContext("2d");
  x.fillStyle="#c75a2e";x.fillRect(0,0,128,128);
  for(var i=0;i<900;i++){x.fillStyle=Math.random()<.5?"rgba(120,40,15,.18)":"rgba(255,170,110,.14)";x.fillRect(Math.random()*128,Math.random()*128,2,2)}
  var t=new THREE.CanvasTexture(c);t.wrapS=t.wrapT=THREE.RepeatWrapping;t.repeat.set(4,(L+130)/6);t.anisotropy=4;return t;
}
function flash(kind){var e=$("rn-flash");e.className=kind;void e.offsetWidth;e.className=kind+" go"}

function disposeScene(){
  try{
    if(S.scene)S.scene.traverse(function(o){
      if(o.geometry)o.geometry.dispose();
      if(o.material){(Array.isArray(o.material)?o.material:[o.material]).forEach(function(m){if(m.map)m.map.dispose();m.dispose()})}
    });
  }catch(e){}
}

function build3D(){
  setLanes((S.mode==="watch"||S.auto)?16:6); /* 16 jalur untuk 20-50 siswa */
  var wrap=$("rn-canvas");
  if(!S.renderer){
    S.renderer=new THREE.WebGLRenderer({antialias:true});
    S.lowFx=(typeof AES_LOWEND!=="undefined"&&!!AES_LOWEND);S.renderer.setPixelRatio(aesGfxRaceDpr(1.75));
    wrap.appendChild(S.renderer.domElement);
    S.camera=new THREE.PerspectiveCamera(60,1,.1,700);
  }else{disposeScene()}
  var L=S.L,scene=S.scene=new THREE.Scene();
  scene.fog=new THREE.Fog(0xf3d9bd,90,470);S.sky=makeSky(scene);
  scene.add(new THREE.HemisphereLight(0xe3f1ff,0x5b7d52,.9));
  var sun=new THREE.DirectionalLight(0xffe0b0,1.0);sun.position.set(-60,70,20);scene.add(sun);
  var M=function(c){return new THREE.MeshLambertMaterial({color:c})};
  var totalLen=L+200,cz=-(L/2)-20;

  var ground=new THREE.Mesh(new THREE.PlaneGeometry(600,totalLen+300),M(0x3fb866));ground.rotation.x=-Math.PI/2;ground.position.set(0,-.02,cz);scene.add(ground);
  var track=new THREE.Mesh(new THREE.PlaneGeometry(TRACKW+2,L+130),new THREE.MeshLambertMaterial({map:trackTex(L)}));track.rotation.x=-Math.PI/2;track.position.set(0,0,-(L/2)-20);scene.add(track);

  // garis lajur
  var lineMat=new THREE.MeshBasicMaterial({color:0xffffff});
  for(var i=0;i<=NLANE;i++){
    var lx=-TRACKW/2+i*LANEW;
    var ln=new THREE.Mesh(new THREE.PlaneGeometry(.1,L+130),lineMat);ln.rotation.x=-Math.PI/2;ln.position.set(lx,.015,-(L/2)-20);scene.add(ln);
  }
  // garis start
  var st=new THREE.Mesh(new THREE.PlaneGeometry(TRACKW,.4),lineMat);st.rotation.x=-Math.PI/2;st.position.set(0,.02,0);scene.add(st);
  // garis finish kotak-kotak
  var cc=document.createElement("canvas");cc.width=64;cc.height=16;var cx=cc.getContext("2d");
  for(var a=0;a<16;a++)for(var b=0;b<4;b++){cx.fillStyle=((a+b)%2)?"#111":"#fff";cx.fillRect(a*4,b*4,4,4)}
  var ctex=new THREE.CanvasTexture(cc);ctex.magFilter=THREE.NearestFilter;
  var fl=new THREE.Mesh(new THREE.PlaneGeometry(TRACKW,1.6),new THREE.MeshBasicMaterial({map:ctex}));fl.rotation.x=-Math.PI/2;fl.position.set(0,.025,-L);scene.add(fl);
  // gerbang finish
  var postM=M(0x334155),gh=6.2;
  [-1,1].forEach(function(s){var p=new THREE.Mesh(new THREE.BoxGeometry(.5,gh,.5),postM);p.position.set(s*(TRACKW/2+.6),gh/2,-L);scene.add(p)});
  var banner=new THREE.Mesh(new THREE.PlaneGeometry(TRACKW+1.6,2.4),new THREE.MeshBasicMaterial({map:textTex("🏁 FINISH 🏁",1024,192,{bg:"#dc2626",fg:"#fff",font:"bold 120px sans-serif"})}));
  banner.position.set(0,gh-.6,-L+.3);scene.add(banner);
  var bb=new THREE.Mesh(new THREE.BoxGeometry(TRACKW+1.8,2.5,.3),M(0x7f1d1d));bb.position.set(0,gh-.6,-L-.05);scene.add(bb);
  // gerbang start
  var sb=new THREE.Mesh(new THREE.PlaneGeometry(TRACKW+1.6,1.6),new THREE.MeshBasicMaterial({map:textTex("START",1024,128,{bg:"#16a34a",fg:"#fff",font:"bold 92px sans-serif"})}));
  sb.position.set(0,5.4,.3);sb.rotation.y=Math.PI;scene.add(sb);
  [-1,1].forEach(function(s){var p=new THREE.Mesh(new THREE.BoxGeometry(.4,5.6,.4),postM);p.position.set(s*(TRACKW/2+.6),2.8,0);scene.add(p)});

  // papan jarak
  var step=L<=200?25:50;
  for(var d=step;d<L;d+=step){
    [-1,1].forEach(function(s){
      var m=new THREE.Mesh(new THREE.PlaneGeometry(2.6,1.3),new THREE.MeshBasicMaterial({map:textTex(d+" m",256,128,{bg:"#fde047",fg:"#111827",font:"bold 80px sans-serif"})}));
      m.position.set(s*(TRACKW/2+1.9),1.4,-d);m.rotation.y=s>0?-Math.PI/2:Math.PI/2;scene.add(m);
    });
  }

  // tribun + penonton (instanced, bersorak & bergelombang)
  var sLen=L+150,sCz=-(L/2)-20,steps=5,STX=TRACKW/2+6;
  var CU={uTime:{value:0},uExc:{value:.35}};S.crowdU=CU;
  function crowdMat(kind){
    var m=new THREE.MeshLambertMaterial({color:0xffffff});
    m.onBeforeCompile=function(sh){
      sh.uniforms.uTime=CU.uTime;sh.uniforms.uExc=CU.uExc;
      var rr="float cr=fract(sin(instanceMatrix[3].z*12.9898+instanceMatrix[3].x*78.233)*43758.5453);";
      var jump="float bn=(.12+.88*uExc)*abs(sin(uTime*(4.0+cr*3.0)+cr*6.283))*.2;float wv=pow(max(0.0,sin(uTime*3.0-instanceMatrix[3].z*.22)),3.0)*.28*(.3+uExc);";
      var body;
      if(kind==="armL"||kind==="armR"){
        var sg=kind==="armL"?"1.0":"-1.0";
        body=rr+jump+"float ag="+sg+"*(.5+(.35+.65*uExc)*sin(uTime*(6.0+cr*3.0)+cr*6.283)*.7);float cg=cos(ag),sn=sin(ag);transformed.xy=vec2(cg*transformed.x-sn*transformed.y,sn*transformed.x+cg*transformed.y);transformed.y+=bn+wv;";
      }else{
        body=rr+jump+"transformed.y+=bn+wv;";
      }
      sh.vertexShader=sh.vertexShader.replace("#include <begin_vertex>","#include <begin_vertex>\n"+body).replace("void main() {","uniform float uTime;uniform float uExc;\nvoid main() {");
    };
    return m;
  }
  var skins=[0xf5cfa5,0xe0ac82,0xc68642,0x8d5524,0xffdbb0,0xd9a066],hairs=[0x111827,0x1f2937,0x3b2314,0x6b4423,0x0b0b0b,0x7c2d12];
  var bodyG=new THREE.BoxGeometry(.4,.52,.26);bodyG.translate(0,.26,0);
  var headG=new THREE.SphereGeometry(.17,8,6);headG.translate(0,.7,0);
  var hairG=new THREE.SphereGeometry(.18,8,5,0,Math.PI*2,0,Math.PI*.55);hairG.translate(0,.72,0);
  var armG=new THREE.BoxGeometry(.08,.3,.08);armG.translate(0,.15,0);armG.translate(0,0,0);
  var armGL=armG.clone(),armGR=armG.clone();armGL.translate(-.21,.42,0);armGR.translate(.21,.42,0);
  var colSp=S.lowFx?1.4:.85,colsN=Math.floor(sLen/colSp),dm=new THREE.Object3D(),col=new THREE.Color();
  var panelTex=(function(){
    var c=document.createElement("canvas");c.width=1024;c.height=128;var x=c.getContext("2d");
    var tx=["AES CLASS","SEMANGAT!","JUARA!","AYO LARI!","KELAS KITA","PANTANG MENYERAH"],cl=["#dc2626","#2563eb","#16a34a","#f59e0b","#9333ea","#0891b2"];
    var pw=1024/tx.length;
    for(var q=0;q<tx.length;q++){x.fillStyle=cl[q];x.fillRect(q*pw,0,pw,128);x.fillStyle="rgba(255,255,255,.9)";x.fillRect(q*pw,0,pw,6);x.fillRect(q*pw,122,pw,6);x.fillStyle="#fff";x.font="bold 36px sans-serif";x.textAlign="center";x.textBaseline="middle";x.fillText(tx[q],q*pw+pw/2,66)}
    var t=new THREE.CanvasTexture(c);t.wrapS=THREE.RepeatWrapping;t.repeat.set(Math.max(2,Math.round(sLen/40)),1);t.anisotropy=4;return t;
  })();
  var flagN=Math.floor(sLen/9),flagPole=new THREE.CylinderGeometry(.05,.05,3.4,5),flagG=new THREE.PlaneGeometry(1.5,.85,6,1);flagPole.translate(0,1.7,0);flagG.translate(.75,3.0,0);
  var flagM=new THREE.MeshLambertMaterial({color:0xffffff,side:THREE.DoubleSide});
  flagM.onBeforeCompile=function(sh){
    sh.uniforms.uTime=CU.uTime;
    sh.vertexShader=sh.vertexShader.replace("#include <begin_vertex>","#include <begin_vertex>\ntransformed.z+=sin(uTime*5.0+position.x*4.0+instanceMatrix[3].z)*.2*position.x;").replace("void main() {","uniform float uTime;\nvoid main() {");
  };
  [-1,1].forEach(function(s){
    var N=colsN*steps,cB=new THREE.InstancedMesh(bodyG,crowdMat("body"),N),cH=new THREE.InstancedMesh(headG,crowdMat("head"),N),cR=new THREE.InstancedMesh(hairG,crowdMat("hair"),N),cAL=new THREE.InstancedMesh(armGL,crowdMat("armL"),N),cAR=new THREE.InstancedMesh(armGR,crowdMat("armR"),N);
    var k=0;
    for(var st2=0;st2<steps;st2++){
      var h=(st2+1)*.8,xx=s*(STX+st2*1.8);
      // anak tangga tribun (belang) + bibir tepi
      var box=new THREE.Mesh(new THREE.BoxGeometry(1.8,h,sLen),M(st2%2?0x64748b:0x7b8ba3));box.position.set(xx,h/2,sCz);scene.add(box);
      var lip=new THREE.Mesh(new THREE.BoxGeometry(.14,.08,sLen),M(0xfacc15));lip.position.set(xx-s*.86,h+.04,sCz);scene.add(lip);
      for(var c2=0;c2<colsN;c2++){
        var cz2=sCz-sLen/2+c2*colSp+rnd(-.2,.2);
        dm.position.set(xx+rnd(-.35,.35),h,cz2);dm.rotation.set(0,s>0?-Math.PI/2:Math.PI/2,0);dm.scale.setScalar(rnd(.9,1.12));dm.updateMatrix();
        cB.setMatrixAt(k,dm.matrix);cH.setMatrixAt(k,dm.matrix);cR.setMatrixAt(k,dm.matrix);cAL.setMatrixAt(k,dm.matrix);cAR.setMatrixAt(k,dm.matrix);
        col.setHSL(Math.random(),.65,.52);cB.setColorAt(k,col);cAL.setColorAt(k,col);cAR.setColorAt(k,col);
        col.setHex(skins[Math.floor(Math.random()*skins.length)]);cH.setColorAt(k,col);cAL.setColorAt(k,col);cAR.setColorAt(k,col);
        col.setHex(hairs[Math.floor(Math.random()*hairs.length)]);cR.setColorAt(k,col);
        k++;
      }
    }
    // warna lengan = warna kulit (lengan terbuka), jadi atur ulang dari kepala
    [cB,cH,cR,cAL,cAR].forEach(function(m){m.instanceMatrix.needsUpdate=true;if(m.instanceColor)m.instanceColor.needsUpdate=true;scene.add(m)});
    // dinding belakang + papan sponsor/semangat
    var wx=s*(STX+steps*1.8+.2);
    var wall=new THREE.Mesh(new THREE.BoxGeometry(.5,9,sLen),M(0x334155));wall.position.set(wx,4.5,sCz);scene.add(wall);
    var pnl=new THREE.Mesh(new THREE.PlaneGeometry(sLen,2.6),new THREE.MeshBasicMaterial({map:panelTex}));
    pnl.rotation.y=s>0?-Math.PI/2:Math.PI/2;pnl.position.set(wx-s*.3,5.6,sCz);scene.add(pnl);
    // pagar depan tribun
    var rail=new THREE.Mesh(new THREE.BoxGeometry(.1,.55,sLen),M(0xe2e8f0));rail.position.set(s*(STX-1.3),.5,sCz);scene.add(rail);
    var railB=new THREE.Mesh(new THREE.BoxGeometry(.06,.06,sLen),M(0xdc2626));railB.position.set(s*(STX-1.3),.85,sCz);scene.add(railB);
    // bendera berkibar
    var fp=new THREE.InstancedMesh(flagPole,M(0xcbd5e1),flagN),fg=new THREE.InstancedMesh(flagG,flagM,flagN),fo=new THREE.Object3D(),fc=new THREE.Color(),fcols=[0xef4444,0x3b82f6,0xfacc15,0x22c55e,0xec4899,0xffffff];
    for(var fI=0;fI<flagN;fI++){
      fo.position.set(s*(STX-1.7),0,sCz-sLen/2+fI*9+4);fo.rotation.set(0,s>0?Math.PI:0,0);fo.scale.set(1,1,1);fo.updateMatrix();
      fp.setMatrixAt(fI,fo.matrix);fg.setMatrixAt(fI,fo.matrix);fc.setHex(fcols[fI%fcols.length]);fg.setColorAt(fI,fc);
    }
    fp.instanceMatrix.needsUpdate=true;fg.instanceMatrix.needsUpdate=true;if(fg.instanceColor)fg.instanceColor.needsUpdate=true;scene.add(fp);scene.add(fg);
  });
  // pohon (instanced)
  var TN=90,trunk=new THREE.InstancedMesh(new THREE.CylinderGeometry(.25,.35,2.2,6),M(0x7c4a24),TN),leaf=new THREE.InstancedMesh(new THREE.ConeGeometry(1.7,4.6,7),M(0x15803d),TN),o3=new THREE.Object3D();
  for(var t=0;t<TN;t++){
    var sd=Math.random()<.5?-1:1,tx=sd*(TRACKW/2+22+Math.random()*40),tz=-L-60+Math.random()*(L+120);
    o3.position.set(tx,1.1,tz);o3.scale.set(1,1,1);o3.updateMatrix();trunk.setMatrixAt(t,o3.matrix);
    var sc=rnd(.9,1.5);o3.position.set(tx,3.7*sc,tz);o3.scale.set(sc,sc,sc);o3.updateMatrix();leaf.setMatrixAt(t,o3.matrix);
  }
  scene.add(trunk);scene.add(leaf);
  // awan
  var cloudM=new THREE.MeshBasicMaterial({color:0xffffff,transparent:true,opacity:.85,fog:false});
  for(var cI=0;cI<14;cI++){
    var cg=new THREE.Group(),cxp=rnd(-220,220),czp=-rnd(0,L+200),cy=rnd(60,100);
    for(var q=0;q<4;q++){var sp=new THREE.Mesh(new THREE.SphereGeometry(rnd(7,13),8,6),cloudM);sp.position.set(q*9-14,rnd(-2,2),rnd(-3,3));sp.scale.y=.55;cg.add(sp)}
    cg.position.set(cxp,cy,czp);scene.add(cg);
  }

  // neon tepi lintasan + nomor lajur
  S.neonMats=[];
  [-1,1].forEach(function(s2,i2){var nm=new THREE.MeshBasicMaterial({color:i2?0xff3df2:0x22d3ee});S.neonMats.push(nm);var n=new THREE.Mesh(new THREE.BoxGeometry(.28,.12,L+130),nm);n.position.set(s2*(TRACKW/2+.14),.06,-(L/2)-20);scene.add(n)});
  for(var ln2=0;ln2<NLANE;ln2++){var nmesh=new THREE.Mesh(new THREE.PlaneGeometry(1.4,1.4),new THREE.MeshBasicMaterial({map:textTex(String(ln2+1),128,128,{fg:"rgba(255,255,255,.9)",font:"bold 110px sans-serif"}),transparent:true,depthWrite:false}));nmesh.rotation.x=-Math.PI/2;nmesh.position.set(-TRACKW/2+LANEW*(ln2+.5),.03,-3.2);scene.add(nmesh)}
  // lampu neon gerbang finish
  S.finNeon=new THREE.MeshBasicMaterial({color:0x22d3ee});
  var fb1=new THREE.Mesh(new THREE.BoxGeometry(TRACKW+2.2,.28,.4),S.finNeon);fb1.position.set(0,gh+.85,-L+.1);scene.add(fb1);
  var fb2=new THREE.Mesh(new THREE.BoxGeometry(TRACKW+2.2,.28,.4),S.finNeon);fb2.position.set(0,gh-2.05,-L+.1);scene.add(fb2);
  // menara lampu stadion
  var TW=Math.ceil((L+120)/90)+1,od2=new THREE.Object3D();
  var pole=new THREE.InstancedMesh(new THREE.CylinderGeometry(.3,.45,18,6),M(0x475569),TW*2),lamp=new THREE.InstancedMesh(new THREE.BoxGeometry(.7,2.6,5.5),new THREE.MeshBasicMaterial({color:0xfff6d6}),TW*2),kk2=0;
  [-1,1].forEach(function(s3){for(var tI=0;tI<TW;tI++){var tz2=40-tI*90,tx2=s3*(TRACKW/2+19);od2.position.set(tx2,9,tz2);od2.updateMatrix();pole.setMatrixAt(kk2,od2.matrix);od2.position.set(tx2-s3*.6,18.6,tz2);od2.updateMatrix();lamp.setMatrixAt(kk2,od2.matrix);kk2++}});
  scene.add(pole);scene.add(lamp);
  // pegunungan jauh
  var MN=22,mtn=new THREE.InstancedMesh(new THREE.ConeGeometry(1,1,5),new THREE.MeshLambertMaterial({color:0x7e9bc4,flatShading:true}),MN);
  for(var mI=0;mI<MN;mI++){
    var sd2=mI<MN-6?(mI%2?-1:1):0,hh=rnd(70,150),rr=rnd(60,110),mx,mz;
    if(sd2){mx=sd2*rnd(300,380);mz=-rnd(-100,L+250)}else{mx=rnd(-300,300);mz=-L-rnd(330,420)}
    od2.position.set(mx,hh/2-2,mz);od2.scale.set(rr,hh,rr);od2.rotation.set(0,rnd(0,3),0);od2.updateMatrix();mtn.setMatrixAt(mI,od2.matrix);
  }
  scene.add(mtn);
  // cincin energi, garis kecepatan, partikel
  S.rings=[];
  for(var rg=0;rg<4;rg++){var rm=new THREE.Mesh(new THREE.RingGeometry(.8,1.05,40),new THREE.MeshBasicMaterial({color:0x4ade80,transparent:true,opacity:0,depthWrite:false,blending:THREE.AdditiveBlending,side:THREE.DoubleSide}));rm.rotation.x=-Math.PI/2;rm.position.y=.07;rm.visible=false;scene.add(rm);S.rings.push({mesh:rm,t:0,f:null})}
  S.streakMat=new THREE.MeshBasicMaterial({color:0xffffff,transparent:true,opacity:0,depthWrite:false,blending:THREE.AdditiveBlending,fog:false});
  S.streaks=[];var sgeo=new THREE.BoxGeometry(.03,.03,1),sn=S.lowFx?24:46;
  for(var sI=0;sI<sn;sI++){var sm=new THREE.Mesh(sgeo,S.streakMat);sm.visible=false;scene.add(sm);S.streaks.push(sm)}
  S.ps={dust:new PS(420,false),glow:new PS(1100,true),conf:new PS(260,false)};
  scene.add(S.ps.dust.pts);scene.add(S.ps.glow.pts);scene.add(S.ps.conf.pts);

  // pelari
  S.racers=[];
  var lanes=shuffle(Array.apply(null,{length:NLANE}).map(function(_,i){return i})),laneX=function(i){return -TRACKW/2+LANEW*(i+.5)};
  var meLane=lanes[0],lv=LEVELS[1];
  var me={isMe:true,name:myName(),color:myColor(),x:laneX(meLane)};
  S.racers.push(me);
  S.laneX=laneX;S.freeLanes=lanes.slice(1);S.remote={};
  if(S.mode==="watch"){ // guru hanya penonton: tidak ada pelari sendiri
    S.racers.pop();me.ghost=true;me.x=0;me.dist=0;me.v=0;me.finished=false;me.finishT=0;me.correct=0;me.wrong=0;me.target=0;
    S.freeLanes=lanes.slice();
  }
  if(!S.auto&&!S.mode){ // hanya mode latihan guru yang memakai pelari komputer
    var names=otherNames();
    for(var bI=0;bI<5;bI++)S.racers.push({isMe:false,name:names[bI],color:BOTCOL[bI],x:laneX(lanes[bI+1]),
      acc:rnd(lv.acc[0],lv.acc[1]),think:rnd(lv.think[0],lv.think[1]),timer:rnd(2.5,5)});
    S.freeLanes=[];
  }
  S.racers.forEach(function(r,i){
    r.dist=0;r.v=0;r.target=BASEV;r.finished=false;r.finishT=0;r.ph=Math.random()*6;r.correct=0;r.wrong=0;r.idx=i;r.lean=0;r.boost=0;r.dacc=0;r.facc=0;
    r.equip=r.isMe?((typeof myPlayer!=="undefined"&&myPlayer&&myPlayer.equip)||null):randEquip();
    r.mesh=makeRunner(r.color,r.name,r.isMe,r.equip);r.mesh.position.set(r.x,0,0);scene.add(r.mesh);
  });
  S.me=me;S.finishCount=0;
  if(S.auto)layoutLanes();

  // kamera awal
  S.camera.position.set(me.x*.7,3.6,9);S.camera.lookAt(me.x*.9,1.5,-14);
  buildDots();onResize();
}

function buildDots(){
  var tb=$("rn-trackbar");Array.prototype.slice.call(tb.querySelectorAll(".rn-dot")).forEach(function(n){n.remove()});
  S.racers.forEach(function(r){var d=document.createElement("span");d.className="rn-dot"+(r.isMe?" me":"");d.style.background=r.color;d.style.left="0%";d.title=r.name;tb.appendChild(d);r.dot=d});
}

function onResize(){
  if(!S.renderer)return;
  var w=window.innerWidth,h=window.innerHeight;
  S.renderer.setSize(w,h);S.camera.aspect=w/h;
  var land=h<=520&&w>h,ox=0,oy=0;
  if(S.state==="run"||S.state==="countdown"){ if(land)ox=w*.2; else oy=h*.13 }
  if(ox||oy)S.camera.setViewOffset(w,h,ox,oy,w,h);else S.camera.clearViewOffset();
  S.camera.updateProjectionMatrix();
}

/* ---------- soal ---------- */
function resetQueue(){
  var qs=getQs();S.qList=(window.AESQBag?window.AESQBag.order(qs):shuffle(qs.map(function(_,i){return i})));S.qPtr=0;
}
function nextQuestion(){
  var qs=getQs();if(!qs.length)return;
  if(S.qPtr>=S.qList.length){resetQueue();if(S.qList.length>1&&S.qList[0]===S.lastQ){var t=S.qList.shift();S.qList.push(t)}}
  var qi=S.qList[S.qPtr++],q=qs[qi];try{window.AESQBag&&window.AESQBag.mark(q)}catch(e){}S.lastQ=qi;S.cur={qi:qi,q:q};S.locked=false;
  var ord=optOrder(q);
  $("rn-qno").textContent="Soal #"+(S.me.correct+S.me.wrong+1)+" • benar "+S.me.correct+"/"+qNeed();
  var html=rich(q.q);
  if(q.image&&/^(https?:|data:image)/i.test(q.image))html+='<img id="rn-qimg" src="'+esc(q.image)+'">';
  $("rn-qtext").innerHTML=html;
  var box=$("rn-opts");box.innerHTML="";
  ord.forEach(function(oi,pos){
    var b=document.createElement("button");b.type="button";b.className="rn-opt";b.dataset.oi=oi;
    b.innerHTML="<b>"+String.fromCharCode(65+pos)+"</b><span>"+rich(q.options[oi])+"</span>";
    b.onclick=function(){pick(pos)};box.appendChild(b);
  });
  $("rn-fb").textContent="";
  typeset([$("rn-qtext"),box]);
  var panel=$("rn-qpanel");panel.scrollTop=0;
}
function updateChips(){
  $("rn-cok").textContent="✓"+S.me.correct;$("rn-cbad").textContent="✗"+S.me.wrong;$("rn-cstreak").textContent="🔥"+S.streak;
}
function fx(text,cls){
  var e=$("rn-fx");e.textContent=text;e.className=cls;void e.offsetWidth;e.className=cls+" show";
}
function pick(pos){
  if(S.locked||S.state!=="run"||!S.cur)return;
  var btns=$("rn-opts").children;if(pos<0||pos>=btns.length)return;
  S.locked=true;
  var chosen=Number(btns[pos].dataset.oi),right=Number(S.cur.q.correct),me=S.me;
  var ok=chosen===right;
  if(ok){
    me.correct++;S.streak++;if(S.streak>S.bestStreak)S.bestStreak=S.streak;
    me.target=Math.min(MAXV,me.target+BOOST+Math.min(S.streak-1,5)*.25);me.v+=.9;
    btns[pos].classList.add("rn-ok");sfx("correct_row");burstGood(me);S.kick=1;flash("ok");
    fx(S.streak>=3?"🔥 KOMBO x"+S.streak+"! NGEBUT!":"🚀 BENAR! LARI MAKIN CEPAT","ok");
    $("rn-fb").style.color="#4ade80";$("rn-fb").textContent="✅ Benar! Kecepatan naik.";
    updateChips();later(nextQuestion,450);
  }else{
    me.wrong++;S.streak=0;me.target=Math.max(MINV,me.target-SLOW);me.v*=.68;S.stumble=1;burstBad(me);S.shake=1;S.roll=(Math.random()<.5?-1:1)*.12;flash("bad");
    btns[pos].classList.add("rn-bad");
    for(var i=0;i<btns.length;i++)if(Number(btns[i].dataset.oi)===right)btns[i].classList.add("rn-ok");
    sfx("wrong_answer");fx("🐢 SALAH! MELAMBAT","bad");
    $("rn-fb").style.color="#fb7185";$("rn-fb").textContent="❌ Salah. Jawaban yang benar ditandai hijau.";
    // soal yang salah akan muncul lagi sebentar lagi
    var at=Math.min(S.qList.length,S.qPtr+2+Math.floor(Math.random()*3));S.qList.splice(at,0,S.cur.qi);
    updateChips();later(nextQuestion,1250);
  }
}

/* ---------- alur lomba ---------- */
function fmt(t){t=Math.max(0,t);var m=Math.floor(t/60),s=t-m*60;return(m<10?"0":"")+m+":"+(s<10?"0":"")+s.toFixed(1)}
function bestKey(){return"aes_run_best_"+S.L}
function getBest(){try{var v=parseFloat(localStorage.getItem(bestKey()));return isFinite(v)?v:null}catch(e){return null}}
function setBest(t){try{localStorage.setItem(bestKey(),String(t))}catch(e){}}
function showBest(){var b=getBest();$("rn-best").textContent=b?("🏆 Rekor pribadimu ("+S.L+" m): "+fmt(b)):"Belum ada rekor untuk jarak ini — ayo catat yang pertama!"}

function showStart(){
  S.state="idle";clearTimers();
  $("rn-start").classList.remove("rn-hide");$("rn-result").classList.add("rn-hide");$("rn-qpanel").classList.remove("show");$("rn-count").textContent="";
  var n=getQs().length;
  $("rn-who").innerHTML="Halo <b>"+esc(myName())+"</b>! "+(n?("Bank soal: <b>"+n+" soal</b> dari materi kelas.")  :'<span style="color:#fca5a5">Belum ada soal. Guru perlu mengisi soal di kolom Edit pada halaman awal.</span>');
  $("rn-go").disabled=!n;showBest();
}
function startRace(){
  if(!getQs().length)return;
  $("rn-start").classList.add("rn-hide");
  build3D(); // reset pelari bersih
  S.T=0;S.streak=0;S.bestStreak=0;S.maxV=0;S.stumble=0;S.resultShown=false;S.finishCount=0;S.shake=0;S.kick=0;S.roll=0;S.orbit=0;S.fwT=0;S.fwN=0;
  resetQueue();updateChips();
  S.state="countdown";S.cdStep=3;S.cd=0;S.pubT=0;S.pubN=0;
  $("rn-qpanel").classList.add("show");onResize();
  nextQuestion();S.locked=true; // soal terlihat, tombol aktif saat GO
  $("rn-count").textContent="3";sfx("click");
}
function onFinishMe(){
  S.state="done";S.locked=true;sfx("finish_island");
  var t=S.me.finishT,best=getBest(),newRec=false;
  if(S.auto){NET.myFin[S.auto]=1;pubRun(topicRes(),{a:"fin",id:S.auto,pid:myPid(),name:myName(),t:Math.round(t*10)/10,ok:S.me.correct,bad:S.me.wrong,L:S.L})}
  if(!best||t<best){setBest(t);newRec=true}
  fx(newRec?"🏆 REKOR BARU!":"🏁 FINISH!","ok");
  $("rn-qpanel").classList.remove("show");
  S.orbit=0;S.fwT=0;S.fwN=0;S.kick=1;confetti(S.me.x,-S.L-3);later(function(){if(S.open)confetti(S.me.x,-S.L-8)},1300);
  later(function(){showResult(newRec)},3600);
}
function ranking(){
  return S.racers.slice().sort(function(a,b){
    if(a.finished&&b.finished)return a.finishT-b.finishT;
    if(a.finished)return-1;if(b.finished)return 1;return b.dist-a.dist;
  });
}
function showResult(newRec){
  if(S.resultShown)return;S.resultShown=true;
  var rk=ranking(),pl=rk.indexOf(S.me)+1,me=S.me,tot=me.correct+me.wrong;
  var medal=pl===1?"🥇":pl===2?"🥈":pl===3?"🥉":"🏅";
  $("rn-rtitle").textContent=medal+(pl===1?" JUARA 1!":" POSISI KE-"+pl);
  $("rn-rsub").textContent=newRec?"🏆 Rekor pribadi baru untuk jarak "+S.L+" m!":"Jarak "+S.L+" m • "+(S.auto?"lomba melawan teman sekelas":"mode latihan");
  $("rn-rstats").innerHTML=
    "<div><b>"+fmt(me.finishT)+"</b><span>WAKTU</span></div>"+
    "<div><b>"+(tot?Math.round(me.correct/tot*100):0)+"%</b><span>AKURASI</span></div>"+
    "<div><b>"+Math.round(S.maxV*3.6)+"</b><span>KM/JAM MAKS</span></div>"+
    "<div><b style='color:#4ade80'>"+me.correct+"</b><span>BENAR</span></div>"+
    "<div><b style='color:#fb7185'>"+me.wrong+"</b><span>SALAH</span></div>"+
    "<div><b style='color:#fdba74'>"+S.bestStreak+"</b><span>KOMBO TERBAIK</span></div>";
  $("rn-rtable").innerHTML=rk.map(function(r,i){
    return '<div class="rn-row'+(r.isMe?" me":"")+'"><span class="pl">#'+(i+1)+'</span><span class="nm">'+esc(r.name)+(r.isMe?" (Kamu)":"")+'</span><span class="tm">'+(r.finished?fmt(r.finishT):Math.round(Math.min(r.dist,S.L))+" m")+'</span></div>';
  }).join("");
  $("rn-result").classList.remove("rn-hide");
}

/* ---------- loop ---------- */
function update(dt){
  var me=S.me;if(!me)return;
  var racing=S.state==="run"||S.state==="done";
  if((S.auto||S.mode==="watch")&&S.scene){S.lt=(S.lt||0)-dt;if(S.lt<=0){S.lt=.2;try{layoutLanes()}catch(e){}}}
  if(S.state==="countdown"){
    S.cd+=dt;
    if(S.cd>=.9){
      S.cd=0;S.cdStep--;
      if(S.cdStep>0){$("rn-count").textContent=String(S.cdStep);sfx("click")}
      else{$("rn-count").textContent="GO!";sfx("finish_island");S.state="run";S.T=0;S.locked=false;S.kick=.8;onResize();later(function(){if(S.state!=="idle")$("rn-count").textContent=""},700)}
    }
  }
  if(S.auto&&(S.state==="countdown"||racing)){
    S.pubT-=dt;
    if(S.pubT<=0){S.pubT=me.finished?2:posEvery();pubPos()}
  }
  if(racing){
    S.T+=dt;
    S.racers.forEach(function(r){
      if(r.remote){ // siswa lain: ikuti posisi yang dikirim lewat jaringan
        var age=(performance.now()-r.nat)/1000,stale=age>4&&!r.fin;
        var tv=stale?0:r.nv,td=Math.min(r.nd+tv*.85*Math.min(age,1.2),L_runoff());
        // jarak pelari hanya boleh maju: jika tebakan lebih jauh dari data asli, tahan dulu (jangan ditarik mundur)
        if(td>r.dist)r.dist+=(td-r.dist)*Math.min(1,dt*5);
        if(r.dist<0)r.dist=0;
        r.v+=(tv-r.v)*Math.min(1,dt*4);if(r.v<0)r.v=0;
        if(r.fin&&!r.finished){r.finished=true;r.finishT=r.fin;S.finishCount++}
        return;
      }
      if(!r.isMe&&!r.finished){
        r.timer-=dt;
        if(r.timer<=0){
          r.timer=r.think*rnd(.8,1.25);
          if(Math.random()<r.acc){r.correct++;r.target=Math.min(MAXV,r.target+BOOST*rnd(.8,1.1));r.v+=.5;r.boost=.8}
          else{r.wrong++;r.target=Math.max(MINV,r.target-SLOW*rnd(.8,1.1));r.v*=.75}
        }
      }
      if(r.finished)r.target=0;
      else{ // kelelahan / pemulihan perlahan menuju kecepatan dasar
        if(r.target>BASEV)r.target=Math.max(BASEV,r.target-.14*dt);
        else if(r.target<BASEV)r.target=Math.min(BASEV,r.target+.1*dt);
      }
      r.v+=(r.target-r.v)*Math.min(1,dt*(r.finished?1.3:2.4));
      if(r.v<0)r.v=0;
      if(!r.finished){var _g=capQ(r)-r.dist;if(_g<1e9){var _vm=Math.max(0,_g)*1.6+CREEP;if(r.v>_vm)r.v=_vm}}
      r.dist=Math.min(r.dist+r.v*dt,L_runoff());
      if(!r.finished&&r.correct<qNeed()){var _h=S.L*.98;if(r.dist>_h){r.dist=_h;r.v=0}}
      if(!r.finished&&r.dist>=S.L){
        r.finished=true;r.finishT=S.T;S.finishCount++;
        if(r.isMe)onFinishMe();
      }
    });
    Object.keys(S.remote).forEach(function(k){var r=S.remote[k];if(r.mesh)return; // siswa yang jauh (belum digambar) tetap dihitung posisinya
      var age=(performance.now()-r.nat)/1000,stale=age>4&&!r.fin,tv=stale?0:r.nv,td=Math.min(r.nd+tv*.85*Math.min(age,1.2),L_runoff());
      if(td>r.dist)r.dist+=(td-r.dist)*Math.min(1,dt*5);if(r.dist<0)r.dist=0;
      r.v+=(tv-r.v)*Math.min(1,dt*4);if(r.v<0)r.v=0;
      if(r.fin&&!r.finished){r.finished=true;r.finishT=r.fin;S.finishCount++}
    });
    if(me.v>S.maxV)S.maxV=me.v;
    // lawan lanjut hingga hasil tampil; jika semua sudah selesai tampilkan hasil
    if(S.state==="done"&&S.orbit>=1&&S.racers.every(function(r){return r.finished}))showResult(false);
  }
  // animasi pelari + efek partikel
  var tnow=performance.now()/1000,dustG=S.ps.dust,glowG=S.ps.glow;
  S.racers.forEach(function(r){
    if(r.remote&&r.mesh&&!r.mesh.visible)return;
    var u=r.mesh.userData,v=racing?r.v:0,rob=!!u.robot,sg=rob?-1:1,vis=Math.min(1,v/6);
    r.ph+=dt*(v>.3?(2.1+v*.62):0);
    var amp=v>.3?Math.min(1.2,.35+v*.07):0,s=Math.sin(r.ph),c=Math.cos(r.ph);
    if(r.boost>0)r.boost-=dt;
    var crouch=(S.state==="countdown"&&S.cdStep<=2)?1:0;
    var leanT=v<.3?0:-Math.min(.42,.07+v*.026);if(crouch)leanT=-.5;
    r.lean+=(leanT-r.lean)*Math.min(1,dt*9);
    var win=r.finished&&r.v<1.6&&racing,by=Math.abs(c)*.09*vis-(crouch?.28:0);
    if(win){
      u.legL.rotation.x*=.85;u.legR.rotation.x*=.85;
      u.armL.rotation.x=u.armR.rotation.x=sg*2.9;
      if(rob){u.armL.rotation.z=-.35;u.armR.rotation.z=.35}
      by=Math.abs(Math.sin(tnow*7+r.idx))*.4;
    }else{
      u.legL.rotation.x=sg*s*amp;u.legR.rotation.x=-sg*s*amp;
      u.armL.rotation.x=-sg*s*amp*1.05;u.armR.rotation.x=sg*s*amp*1.05;
      if(rob){
        u.armL.rotation.z=-.14;u.armR.rotation.z=.14;
        var lf=vis*.2;u.legL.position.y=.6+Math.max(0,s)*lf;u.legR.position.y=.6+Math.max(0,-s)*lf;
      }
    }
    if(rob){ // poros lengan robot ada di tengah lengan: saat pose menang, jaga pangkal lengan tetap di bahu
      [u.armL,u.armR].forEach(function(A){
        var p0=A.userData.p0||(A.userData.p0=A.position.clone());
        if(win){var cx=Math.cos(A.rotation.x),sx=Math.sin(A.rotation.x),cz=Math.cos(A.rotation.z),sz=Math.sin(A.rotation.z),SH=.62;A.position.set(p0.x+SH*sz,p0.y+SH-SH*cz*cx,p0.z-SH*cz*sx)}
        else A.position.copy(p0);
      });
    }
    if(rob)u.robot.rotation.y=Math.PI+s*.16*vis;
    var sc=1+(r.boost>0?Math.min(1,r.boost)*.06:0);
    u.body.scale.set(sc,sc*(1+Math.sin(r.ph*2)*.015*vis),sc);
    u.body.rotation.x=r.lean;u.body.rotation.z=Math.sin(r.ph)*.04*vis;
    if(r.isMe&&S.stumble>0){u.body.rotation.z=Math.sin(S.T*38)*.16*S.stumble;u.body.rotation.x=r.lean+.3*S.stumble;by-=.1*S.stumble}
    u.body.position.y=by;
    if(r.tx!==undefined)r.x+=(r.tx-r.x)*Math.min(1,dt*4);
    if(r.vbT!==undefined)r.vb=(r.vb||0)+(r.vbT-(r.vb||0))*Math.min(1,dt*3);
    r.mesh.position.set(r.x,0,-(r.dist-(r.vb||0)));
    if(u.arrow){u.arrow.position.y=4.25+Math.sin(performance.now()/180)*.12;u.arrow.rotation.y+=dt*3}
    // debu di kaki
    if(racing&&v>3){
      r.dacc+=dt*v*(r.isMe?3.4:1.8)*(S.lowFx?.5:1);
      while(r.dacc>1){r.dacc-=1;dustG.emit(r.x+rnd(-.35,.35),.08,-r.dist+rnd(-.1,.5),rnd(-.7,.7),rnd(.5,1.5),rnd(.6,2.2)+v*.12,rnd(.45,.85),.3,1.0,.82,.7,.55,.42,-.25)}
    }
    // api booster di punggung robot
    if(racing&&!r.finished&&(r.boost>0||v>10.5)){
      var hot=v>10.5;
      r.facc+=dt*(r.isMe?90:40)*(r.boost>0?1.4:.7)*(S.lowFx?.5:1);
      while(r.facc>1){r.facc-=1;glowG.emit(r.x+rnd(-.15,.15),rnd(1.0,1.6),-r.dist+.45,rnd(-.4,.4),rnd(-.3,.5),rnd(2.5,5)+v*.25,rnd(.22,.4),.55,.05,hot?.3:1,hot?.8:.5,hot?1:.1,.9,0)}
    }
  });
  if(S.stumble>0)S.stumble=Math.max(0,S.stumble-dt*1.2);
  S.ps.dust.update(dt);S.ps.glow.update(dt);S.ps.conf.update(dt);
  S.rings.forEach(function(R){
    if(R.t>0){R.t+=dt;var q=R.t/.7;
      if(q>=1){R.t=0;R.mesh.visible=false}
      else{if(R.f)R.mesh.position.set(R.f.x,.07,-R.f.dist);R.mesh.scale.setScalar(1+q*6);R.mesh.material.opacity=.85*(1-q)}
    }
  });
  if(S.state==="done"){S.fwT+=dt;if(S.fwT>.4&&S.fwN<9){S.fwT=0;S.fwN++;fireworkAt(rnd(-14,14),rnd(9,18),-S.L+rnd(-4,22))}}
  S.neonMats.forEach(function(m,i){m.color.setHSL((tnow*.12+i*.5)%1,1,.58)});
  if(S.finNeon)S.finNeon.color.setHSL((tnow*.35)%1,1,.6);

  // kamera sinematik mengikuti pelari kita
  var fo=(S.mode==="watch")?(watchTarget()||me):me;
  var k=1-Math.exp(-dt*6),cam=S.camera,sp=fo.v,lx=fo.x*.9,ly=1.6,lz=-fo.dist-14;
  if(S.state==="done"){
    S.orbit=Math.min(1,S.orbit+dt/2.4);var e=S.orbit*S.orbit*(3-2*S.orbit),th=Math.PI*e,kk=1-Math.exp(-dt*9);
    var pk=cam.aspect<.95?1+Math.min(1,(.95-cam.aspect)/.5)*.7:1;
    cam.position.x+=(me.x+Math.sin(th)*6.5*pk-cam.position.x)*kk;
    cam.position.y+=(2.3+Math.sin(th)*.9-cam.position.y)*kk;
    cam.position.z+=(-me.dist+Math.cos(th)*8*pk-cam.position.z)*kk;
    lx=me.x;ly=1.7;lz=-me.dist;
  }else{
    var tx=fo.x*.7,ty=3.2+Math.min(1,sp*.045),tz=-fo.dist+7.2+sp*.15;
    if(S.mode==="watch"){ty+=1.6;tz+=5}
    if(S.state==="idle"){tz=-me.dist+9;ty=3.8;tx=me.x*.7+Math.sin(performance.now()/2600)*2.5}
    if(cam.aspect<.95){var pq=Math.min(1,(.95-cam.aspect)/.5);tz+=4.5*pq;ty+=1.1*pq;tx=fo.x*.5}  // layar tegak: mundur & naik agar semua lajur terlihat
    if(S.mode==="watch"&&S.wCust){ // guru: kamera bebas (zoom / putar / miring) mengitari siswa yang ditonton
      var Rr=13.3*S.wZoom,cp=S.wPitch,ca=S.wOrbit;
      tx=fo.x+Rr*Math.cos(cp)*Math.sin(ca);ty=Math.max(.8,1.2+Rr*Math.sin(cp));tz=-fo.dist+Rr*Math.cos(cp)*Math.cos(ca);
      lx=fo.x;ly=1.2;lz=-fo.dist;
    }
    cam.position.x+=(tx-cam.position.x)*k;cam.position.y+=(ty-cam.position.y)*k;cam.position.z+=(tz-cam.position.z)*k;
  }
  S.shake=Math.max(0,S.shake-dt*2.4);S.kick=Math.max(0,S.kick-dt*2.2);S.roll*=Math.exp(-dt*4);
  cam.lookAt(lx+(Math.random()-.5)*S.shake*.9,ly+(Math.random()-.5)*S.shake*.6,lz);
  var rl=S.roll+(S.shake>0?(Math.random()-.5)*S.shake*.04:0)+Math.sin(tnow*1.7)*.004*clamp(sp/MAXV,0,1);
  if(rl)cam.rotateZ(rl);
  var fovT=S.state==="done"?50:58+clamp(sp/MAXV,0,1)*17+S.kick*9,kf=1-Math.exp(-dt*10);
  if(cam.aspect<.95){var hn=2*Math.atan(Math.tan(33*Math.PI/180)/cam.aspect)*180/Math.PI;fovT=Math.min(92,Math.max(fovT,hn))}  // layar tegak: lebarkan sudut pandang
  if(Math.abs(cam.fov-fovT)>.05){cam.fov+=(fovT-cam.fov)*kf;cam.updateProjectionMatrix()}
  if(S.sky)S.sky.position.copy(cam.position);
  // garis kecepatan 3D
  var so=racing&&S.state==="run"&&!S.wCust?clamp((fo.v-7)/7,0,.5):0;S.streakMat.opacity=so;
  S.streaks.forEach(function(m){
    m.visible=so>.01;
    if(m.visible){if(m.position.z>cam.position.z+1||m.position.z===0)respawnStreak(m,m.position.z===0);m.scale.z=2+fo.v*.6}
  });
  var us=S.renderer.domElement.height/(2*Math.tan(cam.fov*Math.PI/360));
  S.ps.dust.mat.uniforms.uScale.value=us;S.ps.glow.mat.uniforms.uScale.value=us;S.ps.conf.mat.uniforms.uScale.value=us;

  hud(racing);
}
function L_runoff(){return S.L+70}

var _hudT=0;
function hud(racing){
  var me=S.me;
  if(S.mode==="watch"){
    var now0=performance.now();if(now0-_hudT>=60){_hudT=now0;
      S.racers.forEach(function(r){r.dot.style.left=clamp(r.dist/S.L,0,1)*100+"%"});
      var ld=0;Object.keys(S.remote).forEach(function(k){if(S.remote[k].dist>ld)ld=S.remote[k].dist});
      $("rn-dist").textContent="Terdepan: "+Math.round(Math.min(ld,S.L))+" / "+S.L+" m";
    }
    renderBoard();return;
  }
  $("rn-speedfx").style.opacity=String(clamp((me.v-7)/8,0,.9));
  var now=performance.now();if(now-_hudT<60)return;_hudT=now;
  $("rn-kmh").textContent=Math.round(me.v*3.6);
  $("rn-spdbar").style.width=clamp(me.v/MAXV*100,0,100)+"%";
  var rk=ranking(),pl=rk.indexOf(me)+1;
  $("rn-place").innerHTML="#"+pl+"<small>/"+S.racers.length+"</small>";
  $("rn-time").textContent=fmt(racing?(S.state==="done"&&me.finished?me.finishT:S.T):0);
  $("rn-dist").textContent=Math.round(Math.min(me.dist,S.L))+" / "+S.L+" m";
  S.racers.forEach(function(r){r.dot.style.left=clamp(r.dist/S.L,0,1)*100+"%"});
}

function frame(ts){
  if(!S.open)return;
  S.raf=requestAnimationFrame(frame);
  var dt=Math.min(.1,(ts-S.last)/1000||0);S.last=ts;
  try{
    if(S.crowdU){var ex=S.state==="done"?1:S.state==="run"?.8:S.state==="countdown"?.55:.3;S.crowdU.uTime.value=ts/1000;S.crowdU.uExc.value+=(ex-S.crowdU.uExc.value)*Math.min(1,dt*2.5)}
    update(dt);S.renderer.render(S.scene,S.camera)}catch(e){console.error("[LombaLari]",e)}
}

/* ---------- buka / tutup ---------- */
function onKey(e){
  if(!S.open)return;
  e.stopPropagation(); // jangan sampai tombol A-D menggerakkan avatar di aplikasi utama
  var k=(e.key||"").toLowerCase(),map={a:0,b:1,c:2,d:3,"1":0,"2":1,"3":2,"4":3};
  if(k==="escape"){closeRun(true);return}
  if(k in map&&S.state==="run"){e.preventDefault();pick(map[k])}
}
function pauseMainRender(){
  try{
    if(typeof renderer!=="undefined"&&renderer&&renderer!==S.renderer&&!renderer.__rnPatched){
      var orig=renderer.render;
      renderer.render=function(){if(S.open)return;return orig.apply(this,arguments)};
      renderer.__rnPatched=true;
    }
  }catch(e){}
}
function openRunCore(mode){
  if(S.open)return;
  if(typeof THREE==="undefined"){alert("Three.js belum termuat. Cek koneksi internet lalu muat ulang halaman.");return}
  if(mode!=="auto")S.auto=null;
  S.mode=mode||null;
  S.open=true;pauseMainRender();$("rn-overlay").classList.add("rn-open");$("rn-launch").style.display="none";
  $("rn-tpanel").classList.add("rn-hide");$("rn-miss").classList.add("rn-hide");
  $("rn-again").style.display=mode?"none":"";
  S.state="idle";
  if(mode==="watch"){
    $("rn-start").classList.add("rn-hide");$("rn-result").classList.add("rn-hide");$("rn-qpanel").classList.remove("show");$("rn-count").textContent="";
    build3D();S.state="run";S.T=0;$("rn-overlay").classList.add("rn-watching");onResize();
  }
  else if(mode==="auto"){$("rn-result").classList.add("rn-hide");startRace()}
  else if(mode==="miss"||mode==="final"){
    $("rn-start").classList.add("rn-hide");$("rn-result").classList.add("rn-hide");$("rn-qpanel").classList.remove("show");$("rn-count").textContent="";
    build3D();
    if(mode==="miss")$("rn-miss").classList.remove("rn-hide");
  }else{build3D();showStart()}
  S.last=performance.now();S.raf=requestAnimationFrame(frame);
}
function openRun(){ // tombol LOMBA LARI: hanya guru -> buka panel guru
  if(!isTeacherNow())return;
  openTPanel();
}
function closeRun(ask){
  if(!S.open)return;
  if(ask&&S.mode!=="watch"&&(S.state==="run"||S.state==="countdown")&&!confirm("Keluar dari lomba lari? Progres lomba ini tidak disimpan."))return;
  var wasWatch=S.mode==="watch";
  S.open=false;cancelAnimationFrame(S.raf);clearTimers();
  $("rn-overlay").classList.remove("rn-watching");
  $("rn-overlay").classList.remove("rn-open");
  disposeScene();
  if(S.renderer){try{S.renderer.dispose();S.renderer.forceContextLoss&&S.renderer.forceContextLoss();S.renderer.domElement.remove()}catch(e){}S.renderer=null}
  S.scene=null;S.state="idle";S.auto=null;S.mode=null;S.follow=null;S.remote={};S.wCust=false;
  if(wasWatch&&isTeacherNow())openTPanel();
}

window.addEventListener("keydown",onKey,true);
window.addEventListener("resize",onResize);
$("rn-exit").onclick=function(){closeRun(true)};
$("rn-close1").onclick=function(){closeRun(false)};
$("rn-close2").onclick=function(){closeRun(false)};
$("rn-close3").onclick=function(){closeRun(false)};
$("rn-go").onclick=startRace;
$("rn-again").onclick=function(){if(S.auto)return;$("rn-result").classList.add("rn-hide");build3D();showStart()};
function segHandler(id,cb){
  $(id).addEventListener("click",function(e){
    var b=e.target.closest("button");if(!b)return;
    Array.prototype.forEach.call($(id).children,function(x){x.classList.remove("on")});b.classList.add("on");cb(Number(b.dataset.v));
  });
}
segHandler("rn-seg-len",function(v){S.L=v;if(S.open&&S.state==="idle"){build3D();showBest()}});


/* ---------- LOMBA LARI DIATUR GURU (siswa tidak bisa memulai sendiri) ---------- */
var NET={c:null,room:null,subs:{},handled:{},myFin:{},state:null,missT:null,finalShown:null,run:null,pt:0,tL:400};
function topicCmd(){return "aes_class_3d/"+roomId+"/run_cmd"}
function topicRes(){return "aes_class_3d/"+roomId+"/run_res"}
function topicState(){return "aes_class_3d/"+roomId+"/run_state"}
function topicPos(){return "aes_class_3d/"+roomId+"/run_pos"}
function isTeacherNow(){try{return typeof isTeacherMode!=="undefined"&&!!isTeacherMode}catch(e){return false}}
function isStudentNow(){try{return !isTeacherNow()&&!!myPlayer&&myPlayer.role==="student"&&!!myPlayer.hasJoinedGame&&!(typeof isTeacher3DMonitor!=="undefined"&&isTeacher3DMonitor)}catch(e){return false}}
function myPid(){try{return String(myPlayer.id||myName())}catch(e){return myName()}}
function nk(n){return String(n==null?"":n).trim().toLowerCase()}
function pubRun(topic,obj,retain){
  try{var c=(typeof mqttClient!=="undefined")?mqttClient:null;if(c&&c.connected){c.publish(topic,JSON.stringify(obj),{qos:1,retain:!!retain});return true}}catch(e){}
  return false;
}
function note(msg){
  var n=document.createElement("div");n.textContent=msg;
  n.style.cssText="position:fixed;left:50%;top:14px;transform:translateX(-50%);z-index:9700;background:#0f172a;color:#fde047;border:1px solid rgba(255,255,255,.4);padding:8px 14px;border-radius:12px;font:800 13px 'Plus Jakarta Sans',sans-serif;max-width:90vw;text-align:center";
  document.body.appendChild(n);setTimeout(function(){n.remove()},3800);
}
function isSeen(id){try{return localStorage.getItem("aes_run_seen")===id}catch(e){return false}}
function setSeen(id){try{localStorage.setItem("aes_run_seen",id)}catch(e){}}
/* interval kirim posisi menyesuaikan jumlah siswa online, agar jaringan sekolah/broker tidak kewalahan */
function posEvery(){
  var n=1;try{if(typeof aesOnlineN==="function")n=aesOnlineN()}catch(e){}
  return n<=12?.6:n<=30?.9:n<=60?1.3:1.8;
}
function onNetMsg(topic,payload,packet){
  var d;try{d=JSON.parse(payload.toString())}catch(e){return}
  if(!d||typeof d!=="object")return;
  try{
    if(topic===topicCmd()){if(isStudentNow())onCmd(d)}
    else if(topic===topicState()){if(isStudentNow()){NET.state=d;NET.stLive=!(packet&&packet.retain);evalState()}}
    else if(topic===topicRes()){if(isTeacherNow())onRes(d)}
    else if(topic===topicPos()){onPos(d)}
  }catch(e){console.error("[LombaLari net]",e)}
}
function bindNet(){
  try{
    var c=(typeof mqttClient!=="undefined")?mqttClient:null,rm=(typeof roomId!=="undefined")?roomId:null;
    if(!c||!rm||!c.connected)return;
    if(!c.__rnL){c.__rnL=true;c.on("message",onNetMsg)}
    if(NET.c!==c||NET.room!==rm){NET.c=c;NET.room=rm;NET.subs={}}
    var watching=S.open&&S.mode==="watch";
    if(!watching&&NET.subs[topicPos()]&&isTeacherNow()){try{c.unsubscribe(topicPos())}catch(e){}delete NET.subs[topicPos()]}
    var want=isTeacherNow()?(watching?[topicRes(),topicPos()]:[topicRes()]):(isStudentNow()?[topicCmd(),topicState(),topicPos()]:[]);
    want.forEach(function(t){if(!NET.subs[t]){NET.subs[t]=1;c.subscribe(t,{qos:1})}});
    if(isStudentNow())evalState();
  }catch(e){}
}
setInterval(bindNet,1200);

/* siswa: pastikan guru benar-benar menerima "ikut" dan "finish" kita; kirim ulang bila paket hilang */
function reconcile(){
  try{
    if(!S.open||!S.auto||!S.me||!isStudentNow())return;
    var st=NET.state;
    if(!st||st.id!==S.auto||!Array.isArray(st.rows))return;
    var me=nk(myName()),row=null;
    st.rows.forEach(function(r){if(nk(r.n)===me)row=r});
    if(S.state==="done"&&(!row||row.s!=="fin")){
      pubRun(topicRes(),{a:"fin",id:S.auto,pid:myPid(),name:myName(),t:Math.round(S.me.finishT*10)/10,ok:S.me.correct,bad:S.me.wrong,L:S.L});
    }else if(!row){
      pubRun(topicRes(),{a:"join",id:S.auto,pid:myPid(),name:myName()});
    }
  }catch(e){}
}
setInterval(reconcile,4000);

/* penanda koneksi di layar lomba + kirim posisi segera setelah tersambung kembali */
var _netWasOk=true;
function netBadge(){
  var el=$("rn-net");
  if(!el){
    el=document.createElement("div");el.id="rn-net";
    el.style.cssText="display:none;position:absolute;left:50%;top:118px;transform:translateX(-50%);z-index:7;max-width:92vw;text-align:center;background:#b45309;color:#fff;border:1px solid #fde68a;border-radius:12px;padding:6px 12px;font:800 12px 'Plus Jakarta Sans',sans-serif;pointer-events:none";
    $("rn-overlay").appendChild(el);
  }
  var c=(typeof mqttClient!=="undefined")?mqttClient:null,ok=!!(c&&c.connected);
  var show=S.open&&!ok&&(S.mode==="auto"||S.mode==="watch"||S.mode==="miss"||S.mode==="final");
  el.style.display=show?"block":"none";
  if(show)el.textContent=S.mode==="watch"?"⚠ Koneksi terputus, menyambung ulang… posisi murid sementara berhenti.":"⚠ Koneksi terputus, menyambung ulang… lomba tetap berjalan dan hasilmu dikirim otomatis saat tersambung.";
  if(ok&&!_netWasOk){S.pubT=0;NET.subs={}}   // tersambung kembali: langsung kirim posisi & langganan ulang
  _netWasOk=ok;
}
setInterval(netBadge,1000);


/* siswa: posisi pelari antar siswa (lawan = teman sekelas) */
var RCOLS=["#ef4444","#f59e0b","#22c55e","#a855f7","#ec4899","#14b8a6","#0ea5e9","#f97316"];
function pubPos(){
  try{
    var c=(typeof mqttClient!=="undefined")?mqttClient:null,me=S.me;
    if(!c||!c.connected||!me||!S.auto)return;
    var o={id:S.auto,pid:myPid(),name:myName(),col:myColor(),d:Math.round(me.dist*10)/10,v:Math.round(me.v*10)/10,f:me.finished?Math.round(me.finishT*10)/10:0};
    var pn=S.pubN++;if(pn<3||pn%12===0){try{var eq=(typeof myPlayer!=="undefined"&&myPlayer&&myPlayer.equip)||null;if(eq&&JSON.stringify(eq).length<700)o.eq=eq}catch(e){}}
    c.publish(topicPos(),JSON.stringify(o),{qos:0,retain:false});
  }catch(e){}
}
function mkRemoteMesh(r){
  var m=makeRunner(r.color,r.name,false,r.equip);m.position.set(r.x,0,-r.dist);return m;
}
function hashStr(t){var h=5381;t=String(t);for(var i=0;i<t.length;i++)h=((h<<5)+h+t.charCodeAt(i))|0;return Math.abs(h)}
/* lajur ditentukan dari ID siswa (sama di semua layar), jadi posisi kiri/kanan tiap siswa konsisten antara layar siswa dan layar guru */
function layoutLanes(){
  if(!S.scene||!S.laneX||!window.aesLanePlan)return;
  var N=NLANE,watch=S.mode==="watch",me=S.me,myK=(!watch&&me)?myPid():null;
  var keys=Object.keys(S.remote),ref=0,i;
  if(watch){var ft=S.follow&&S.remote[S.follow];if(ft)ref=ft.dist;else keys.forEach(function(k){if(S.remote[k].dist>ref)ref=S.remote[k].dist})}
  else if(me)ref=me.dist||0;
  var MAXVIS=(typeof aesGfxMaxVis==="function")?aesGfxMaxVis():((typeof AES_LOWEND!=="undefined"&&AES_LOWEND)?10:18);
  var vis=keys.map(function(k){return S.remote[k]}).sort(function(a,b){return Math.abs(a.dist-ref)-Math.abs(b.dist-ref)}).slice(0,Math.max(0,MAXVIS-(myK?1:0)));
  var items=vis.map(function(r){return{k:r.pid,d:r.dist,p:(r.cell===undefined?-1:r.cell),h:hashStr(r.pid)%N}});
  if(myK&&me)items.push({k:myK,d:me.dist,p:(me.cell===undefined?-1:me.cell),h:hashStr(myK)%N,fix:true});
  var plan=window.aesLanePlan(items,N,1,2.6),visSet={};
  if(myK&&me&&plan[myK]){var mx=S.laneX(plan[myK].c);me.cell=plan[myK].c;if(me.tx===undefined)me.x=mx;me.tx=mx;me.vbT=0}
  vis.forEach(function(r){
    var pl=plan[r.pid];if(!pl)return;visSet[r.pid]=1;
    var x=S.laneX(pl.c);r.cell=pl.c;r.vbT=pl.back;
    if(!r.mesh){r.x=x;r.tx=x;r.vb=pl.back;r.mesh=mkRemoteMesh(r);S.scene.add(r.mesh);r.idx=S.racers.length;S.racers.push(r);buildDots()}
    else{r.tx=x;if(!r.mesh.visible){r.x=x;r.vb=pl.back;r.mesh.visible=true}}
  });
  keys.forEach(function(k){var r=S.remote[k];if(!visSet[k]&&r.mesh)r.mesh.visible=false});
}
function addRemote(m){
  if(!S.scene||!S.laneX)return null;
  var key=String(m.pid);
  var col=/^#[0-9a-fA-F]{6}$/.test(String(m.col||""))?m.col:RCOLS[Object.keys(S.remote).length%RCOLS.length];
  var eq=(m.eq&&typeof m.eq==="object")?m.eq:null;
  var r={isMe:false,remote:true,pid:key,name:String(m.name||"?").slice(0,24),color:col,x:0,equip:eq,hasEq:!!eq,
    dist:0,v:0,target:BASEV,finished:false,finishT:0,ph:Math.random()*6,correct:0,wrong:0,idx:0,lean:0,boost:0,dacc:0,facc:0,nd:0,nv:0,nat:performance.now(),fin:0,mesh:null};
  S.remote[key]=r;
  layoutLanes();
  return r;
}
function onPos(d){
  if(!S.open||!S.scene||!S.me)return;
  var watch=S.mode==="watch";
  if(watch){if(!NET.run||d.id!==NET.run.id)return}
  else if(!S.auto||d.id!==S.auto)return;
  var key=String(d.pid);if(!key||(!watch&&key===myPid()))return;
  var r=S.remote[key]||addRemote(d);if(!r)return;
  var nd0=Number(d.d)||0;
  if(nd0<r.nd-0.05&&!(Number(d.f)>0))return; // paket lama yang datang terlambat/tidak berurutan: abaikan
  r.nd=Math.max(r.nd,nd0);r.nv=clamp(Number(d.v)||0,0,MAXV+3);r.nat=performance.now();
  if(Number(d.f)>0)r.fin=Number(d.f);
  if(d.eq&&typeof d.eq==="object"&&!r.hasEq&&r.mesh){ // perlengkapan avatar baru diterima: ganti tampilan
    r.hasEq=true;r.equip=d.eq;
    try{S.scene.remove(r.mesh);r.mesh=mkRemoteMesh(r);S.scene.add(r.mesh)}catch(e){}
  }
  if(!r.mesh){r.dist=r.nd;if(r.fin){r.finished=true;r.finishT=r.fin}} // tanpa lajur: hanya data papan skor
}
function watchTarget(){
  var f=S.follow&&S.remote[S.follow];if(f&&f.mesh)return f;
  var best=null;
  S.racers.forEach(function(r){if(r.remote&&!r.finished&&(!best||r.dist>best.dist))best=r});
  if(!best)S.racers.forEach(function(r){if(r.remote&&(!best||r.dist>best.dist))best=r});
  return best;
}
var _wbT=0;
function renderBoard(){
  var now=performance.now();if(now-_wbT<400)return;_wbT=now;
  var arr=Object.keys(S.remote).map(function(k){return S.remote[k]});
  arr.sort(function(a,b){var fa=a.fin>0,fb=b.fin>0;if(fa&&fb)return a.fin-b.fin;if(fa)return-1;if(fb)return 1;return b.dist-a.dist});
  var ended=NET.run&&NET.run.status==="ended",nf=arr.filter(function(r){return r.fin>0}).length;
  $("rn-wtitle").textContent=(ended?"🏁 LOMBA DIAKHIRI • ":"👁 LIVE • ")+arr.length+" siswa • "+nf+" selesai • "+S.L+" m"+(S.follow&&S.remote[S.follow]?" • 📍 "+S.remote[S.follow].name:"");
  $("rn-wlist").innerHTML=arr.length?arr.map(function(r,i){
    var lost=!r.fin&&!ended&&(now-r.nat)>6000,tm=r.fin>0?fmt(r.fin):(Math.round(Math.min(r.dist,S.L))+" m"+(lost?" ⚠":""));
    return '<div class="rn-row'+(S.follow===r.pid?" me":"")+'" data-pid="'+esc(r.pid)+'"><span class="pl">#'+(i+1)+'</span><span class="nm"><i style="background:'+esc(r.color)+'"></i>'+esc(r.name)+'</span><span class="tm">'+tm+'</span></div>';
  }).join(""):'<div style="font-size:11px;color:#94a3b8;padding:6px">Menunggu siswa mulai berlari…</div>';
  $("rn-wauto").style.opacity=S.follow?".6":"1";
}
function openWatch(){
  if(!isTeacherNow())return;
  if(!NET.run||NET.run.status!=="running"){note("Mulai lomba dulu, baru bisa ditonton.");return}
  if(S.open)return;
  S.follow=null;S.wOrbit=0;S.wPitch=.42;S.wZoom=1;S.wCust=false;
  try{var _pt=!!(window.matchMedia&&window.matchMedia("(orientation:portrait)").matches);$("rn-wboard").classList.toggle("rn-wmin",_pt);$("rn-wtoggle").textContent=_pt?"Daftar ▴":"Daftar ▾"}catch(e){}
  openRunCore("watch");bindNet();
}

/* siswa: perintah mulai dari guru */
function onCmd(d){
  if(d.a!=="start")return;
  if(!d.id||NET.handled[d.id])return;NET.handled[d.id]=1;
  if(S.open&&S.mode==="miss")closeRun(false);   // sempat dikira tertinggal, ternyata perintah baru sampai
  if(S.open)return;
  if(!getQs().length){pubRun(topicRes(),{a:"noq",id:d.id,pid:myPid(),name:myName()});note("Belum ada soal, lomba lari belum bisa dimulai.");return}
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  var L=Number(d.L);S.auto=d.id;S.L=(L===200||L===400||L===800)?L:400;
  openRunCore("auto");
  pubRun(topicRes(),{a:"join",id:d.id,pid:myPid(),name:myName()});
}

/* siswa: status lomba dari guru (tersimpan di server, jadi terbaca juga saat buka aplikasi belakangan) */
function evalState(){
  var d=NET.state;if(!d||!d.id||!isStudentNow())return;
  var age=Date.now()-(Number(d.at)||0);
  if(d.st==="running"){
    if(age>10800000||NET.handled[d.id]||NET.missT===d.id)return;
    NET.missT=d.id;
    setTimeout(function(){ // beri waktu perintah mulai langsung tiba; kalau tidak, siswa ini tertinggal
      var c=NET.state;
      if(!c||c.id!==d.id||c.st!=="running"||NET.handled[d.id]||S.open||!isStudentNow())return;
      // status "mulai" diterima langsung (bukan tersimpan di server) tetapi perintah mulai tidak sampai = paket hilang di jaringan: tetap ikut lomba
      if(NET.stLive){onCmd({a:"start",id:c.id,L:c.L});return}
      openMissed(c);
    },2500);
  }else if(d.st==="ended"){
    if(age>43200000)return;
    if(NET.finalShown===d.id&&S.open){showFinalBoard(d);return}
    if(isSeen(d.id)||NET.myFin[d.id])return;
    if(S.open&&S.auto===d.id){
      if(S.state==="done"||S.resultShown||!S.me)return;   // sudah finis: lihat hasil sendiri
      pubRun(topicRes(),{a:"dnf",id:d.id,pid:myPid(),name:myName(),ok:S.me.correct,bad:S.me.wrong});
      NET.myFin[d.id]=0;closeRun(false);openFinal(d);return;
    }
    if(S.open&&S.mode==="miss"){showFinalBoard(d);return}
    if(S.open)return;
    openFinal(d);
  }
}
function openMissed(d){
  if(S.open)return;
  var L=Number(d.L);S.L=(L===200||L===400||L===800)?L:400;
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  openRunCore("miss");
}
function openFinal(d){
  if(S.open)return;
  var L=Number(d.L);S.L=(L===200||L===400||L===800)?L:400;
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  openRunCore("final");showFinalBoard(d);
}
function showFinalBoard(d){
  setSeen(d.id);NET.finalShown=d.id;
  $("rn-miss").classList.add("rn-hide");$("rn-start").classList.add("rn-hide");
  var me=nk(myName()),rows=Array.isArray(d.rows)?d.rows:[];
  var fin=rows.filter(function(r){return r.s==="fin"}).sort(function(a,b){return a.t-b.t});
  var part=rows.filter(function(r){return r.s==="dnf"||r.s==="run"});
  var miss=rows.filter(function(r){return r.s==="miss"});
  var mine=null,rank=0;
  fin.forEach(function(r,i){if(nk(r.n)===me){mine=r;rank=i+1}});
  if(!mine)part.forEach(function(r){if(nk(r.n)===me)mine=r});
  var ok=mine?(Number(mine.ok)||0):0,bad=mine?(Number(mine.bad)||0):0,tot=ok+bad,ac=tot?Math.round(ok/tot*100):0;
  var st=mine?(mine.s==="fin"?"Selesai":"Belum selesai"):"Tidak ikut";
  var medal=rank===1?"🥇":rank===2?"🥈":rank===3?"🥉":"🏁";
  $("rn-rtitle").textContent=rank?(medal+(rank===1?" JUARA 1!":" POSISI KE-"+rank)):"🏁 LOMBA SUDAH SELESAI";
  $("rn-rsub").textContent="Jarak "+d.L+" m • lomba sudah diakhiri guru"+(mine?"":" • kamu tidak ikut, skormu 0");
  $("rn-rstats").innerHTML=
    "<div><b>"+(mine&&mine.s==="fin"?fmt(mine.t):"-")+"</b><span>WAKTU</span></div>"+
    "<div><b>"+ac+"%</b><span>AKURASI</span></div>"+
    "<div><b>"+(rank?("#"+rank+"/"+fin.length):"-")+"</b><span>POSISI</span></div>"+
    "<div><b style='color:#4ade80'>"+ok+"</b><span>BENAR</span></div>"+
    "<div><b style='color:#fb7185'>"+bad+"</b><span>SALAH</span></div>"+
    "<div><b style='color:#fdba74;font-size:12px'>"+st+"</b><span>STATUS</span></div>";
  function row(pl,r,tm){return '<div class="rn-row'+(nk(r.n)===me?" me":"")+'"><span class="pl">'+pl+'</span><span class="nm">'+esc(r.n)+(nk(r.n)===me?" (Kamu)":"")+'</span><span class="tm">'+tm+'</span></div>'}
  $("rn-rtable").innerHTML=
    fin.map(function(r,i){return row("#"+(i+1),r,fmt(r.t)+" • ✓"+(r.ok||0)+" ✗"+(r.bad||0))}).join("")+
    part.map(function(r){return row("…",r,"belum selesai")}).join("")+
    miss.map(function(r){return row("–",r,"tidak ikut")}).join("");
  $("rn-result").classList.remove("rn-hide");
}

/* guru: panel, status lomba & papan hasil */
function openTPanel(){renderT();$("rn-tpanel").classList.remove("rn-hide");$("rn-launch").style.display="none"}
function onRes(d){
  var r=NET.run;if(!r||!d||d.id!==r.id)return;
  var nm=String(d.name||"?").slice(0,40),key=nk(nm);if(!key)return;
  if(d.a==="join"){r.joined[key]=nm}
  else if(d.a==="fin"){r.joined[key]=nm;r.fin[key]={name:nm,t:Number(d.t)||0,ok:Number(d.ok)||0,bad:Number(d.bad)||0};delete r.dnf[key]}
  else if(d.a==="dnf"){r.joined[key]=nm;if(!r.fin[key])r.dnf[key]={name:nm,ok:Number(d.ok)||0,bad:Number(d.bad)||0}}
  else if(d.a==="noq"){r.noq[key]=nm}
  renderT();pubState(false);
}
function buildRows(){
  var r=NET.run,rows=[],seen={};
  Object.keys(r.fin).forEach(function(k){var x=r.fin[k];rows.push({n:x.name,s:"fin",t:x.t,ok:x.ok,bad:x.bad});seen[k]=1});
  Object.keys(r.dnf).forEach(function(k){if(seen[k])return;var x=r.dnf[k];rows.push({n:x.name,s:"dnf",ok:x.ok,bad:x.bad});seen[k]=1});
  Object.keys(r.joined).forEach(function(k){if(seen[k])return;rows.push({n:r.joined[k],s:"run",ok:0,bad:0});seen[k]=1});
  if(r.status==="ended"){
    try{(gameConfig.students||[]).forEach(function(n){n=String(n||"").trim();if(n&&!seen[nk(n)]){rows.push({n:n.slice(0,40),s:"miss"});seen[nk(n)]=1}})}catch(e){}
  }
  return rows;
}
function pubState(now){
  clearTimeout(NET.pt);
  var go=function(){var r=NET.run;if(!r)return;pubRun(topicState(),{id:r.id,L:r.L,st:r.status,at:Date.now(),rows:buildRows()},true)};
  if(now)go();else NET.pt=setTimeout(go,400);
}
function renderT(){
  var st=$("rn-t-stat"),tb=$("rn-t-table");if(!st||!tb)return;
  var r=NET.run;
  if(!r){st.textContent="Belum ada lomba yang dimulai.";tb.innerHTML="";return}
  var nj=Object.keys(r.joined).length,nf=Object.keys(r.fin).length,nq=Object.keys(r.noq).length;
  st.textContent=(r.status==="ended"?"🏁 LOMBA DIAKHIRI • ":"🏃 LOMBA BERJALAN • ")+"jarak "+r.L+" m • siswa saling berlomba • ikut: "+nj+" • selesai: "+nf+(nq?" • tanpa soal: "+nq:"");
  var rows=buildRows(),k=0;
  tb.innerHTML=rows.filter(function(x){return x.s==="fin"}).sort(function(a,b){return a.t-b.t}).map(function(x,i){
    var tot=x.ok+x.bad,ac=tot?Math.round(x.ok/tot*100):0;
    return '<div class="rn-row"><span class="pl">#'+(i+1)+'</span><span class="nm">'+esc(x.n)+'</span><span class="tm">'+fmt(x.t)+' • ✓'+x.ok+' ✗'+x.bad+' ('+ac+'%)</span></div>';
  }).join("")+rows.filter(function(x){return x.s==="run"||x.s==="dnf"}).map(function(x){
    return '<div class="rn-row"><span class="pl">…</span><span class="nm">'+esc(x.n)+'</span><span class="tm">'+(x.s==="run"?"sedang berlari":"belum selesai")+'</span></div>';
  }).join("")+rows.filter(function(x){return x.s==="miss"}).map(function(x){
    return '<div class="rn-row"><span class="pl">–</span><span class="nm">'+esc(x.n)+'</span><span class="tm">tidak ikut</span></div>';
  }).join("");
}
segHandler("rn-t-seg-len",function(v){NET.tL=v});
$("rn-t-go").onclick=function(){
  if(!isTeacherNow())return;
  if(!getQs().length){note("Belum ada soal. Isi soal dulu di kolom Edit pada halaman awal.");return}
  var id="r"+Date.now().toString(36)+Math.floor(Math.random()*1000);
  var prev=NET.run;
  NET.run={id:id,L:NET.tL,status:"running",joined:{},fin:{},dnf:{},noq:{}};
  bindNet();
  if(!pubRun(topicState(),{id:id,L:NET.tL,st:"running",at:Date.now(),rows:[]},true)){NET.run=prev;renderT();note("Belum tersambung ke server kelas. Coba lagi sebentar lagi.");return}
  pubRun(topicCmd(),{a:"start",id:id,L:NET.tL});
  renderT();note("📣 Lomba lari dimulai di layar siswa!");
};
$("rn-t-stop").onclick=function(){
  if(!isTeacherNow())return;
  var r=NET.run;if(!r||r.status==="ended"){note("Belum ada lomba yang berjalan.");return}
  if(!confirm("Akhiri lomba dan umumkan skor ke semua siswa? Siswa yang masih berlari akan dihentikan."))return;
  r.status="ended";renderT();pubState(true);note("🏁 Lomba diakhiri. Skor ditampilkan ke siswa.");
};
$("rn-t-watch").onclick=openWatch;
$("rn-wlist").addEventListener("click",function(e){var row=e.target.closest(".rn-row");if(!row)return;var p=row.dataset.pid;S.follow=(S.follow===p)?null:p;_wbT=0;renderBoard();try{if(window.matchMedia("(orientation:portrait)").matches){$("rn-wboard").classList.add("rn-wmin");$("rn-wtoggle").textContent="Daftar ▴"}}catch(x){}});
$("rn-wauto").onclick=function(){S.follow=null;_wbT=0;renderBoard()};
(function(){ /* kontrol kamera layar tonton guru: zoom, putar, miring */
  var cv=$("rn-canvas"),pts={},lastD=0;
  function ensure(){if(S.wZoom==null){S.wOrbit=0;S.wPitch=.42;S.wZoom=1}}
  function clampW(){S.wZoom=Math.max(.35,Math.min(3.5,S.wZoom));S.wPitch=Math.max(.12,Math.min(1.35,S.wPitch))}
  function act(w){
    ensure();
    if(w==="reset"){S.wOrbit=0;S.wPitch=.42;S.wZoom=1;S.wCust=false;return}
    S.wCust=true;
    if(w==="in")S.wZoom/=1.25;else if(w==="out")S.wZoom*=1.25;
    else if(w==="L")S.wOrbit-=.35;else if(w==="R")S.wOrbit+=.35;
    else if(w==="up")S.wPitch+=.15;else if(w==="down")S.wPitch-=.15;
    clampW();
  }
  $("rn-wctl").addEventListener("click",function(e){var b=e.target.closest("button");if(!b||S.mode!=="watch")return;act(b.dataset.w)});
  cv.addEventListener("pointerdown",function(e){if(S.mode!=="watch")return;pts[e.pointerId]={x:e.clientX,y:e.clientY};try{cv.setPointerCapture(e.pointerId)}catch(x){}lastD=0});
  cv.addEventListener("pointermove",function(e){
    if(S.mode!=="watch"||!pts[e.pointerId])return;
    ensure();var ids=Object.keys(pts),p=pts[e.pointerId],dx=e.clientX-p.x,dy=e.clientY-p.y;
    if(ids.length>=2){
      p.x=e.clientX;p.y=e.clientY;var a=pts[ids[0]],b=pts[ids[1]],d=Math.hypot(a.x-b.x,a.y-b.y);
      if(lastD>0&&d>0){S.wCust=true;S.wZoom*=lastD/d;clampW()}lastD=d;return;
    }
    p.x=e.clientX;p.y=e.clientY;
    if(Math.abs(dx)+Math.abs(dy)<1)return;
    S.wCust=true;S.wOrbit-=dx*.008;S.wPitch+=dy*.006;clampW();
  });
  function up(e){delete pts[e.pointerId];lastD=0}
  cv.addEventListener("pointerup",up);cv.addEventListener("pointercancel",up);
  cv.addEventListener("wheel",function(e){if(S.mode!=="watch")return;e.preventDefault();ensure();S.wCust=true;S.wZoom*=Math.exp(e.deltaY*.0012);clampW()},{passive:false});
})();
$("rn-wend").onclick=function(){var b=$("rn-t-stop");if(b&&b.onclick)b.onclick();_wbT=0;renderBoard()};
$("rn-wclose").onclick=function(){closeRun(false)};
$("rn-wtoggle").onclick=function(){var b=$("rn-wboard"),m=b.classList.toggle("rn-wmin");$("rn-wtoggle").textContent=m?"Daftar ▴":"Daftar ▾"};
$("rn-t-docx").onclick=function(){
  var r=NET.run;if(!r){alert("Belum ada lomba yang dimulai.");return}
  var rows=buildRows(),fin=rows.filter(function(x){return x.s==="fin"}).sort(function(a,b){return a.t-b.t}),
    oth=rows.filter(function(x){return x.s==="run"||x.s==="dnf"}),miss=rows.filter(function(x){return x.s==="miss"}),list=[];
  fin.forEach(function(x){list.push({n:x.n,st:"Selesai",time:fmt(x.t),ok:x.ok,bad:x.bad,prog:"100%"})});
  oth.forEach(function(x){list.push({n:x.n,st:"Belum selesai",time:"-",ok:x.s==="dnf"?x.ok:null,bad:x.s==="dnf"?x.bad:null,prog:"-"})});
  miss.forEach(function(x){list.push({n:x.n,st:"Tidak ikut",time:"-",ok:null,bad:null,prog:"-"})});
  window.aesRaceDocx({title:"Nilai Lomba Lari AES CLASS",fname:"Nilai_Lomba_Lari_"+window.aesRaceStamp()+".docx",
    info:["Jarak lintasan: "+r.L+" m","Target soal: "+(r.L<=200?8:r.L<=400?12:16)+" jawaban benar untuk finis","Status: "+(r.status==="ended"?"lomba sudah diakhiri":"lomba masih berjalan")+" • ikut: "+Object.keys(r.joined).length+" • selesai: "+fin.length],
    rows:list});
};
$("rn-t-self").onclick=function(){if(isTeacherNow())openRunCore()};
$("rn-t-close").onclick=function(){$("rn-tpanel").classList.add("rn-hide")};

window.AESRun={open:openRun,close:function(){closeRun(false)},_state:S};
})();
</script>
<!-- ===== /LOMBA LARI ===== -->

<script id="aes-lane-plan">
/* AES CLASS • Penata jalur 20-50 pelari (dipakai Lomba Lari, Balap Mobil, Balap Pesawat)
   list: [{k:id, d:jarak, p:sel_sebelumnya(-1 jika belum ada), h:sel_asal, fix:true jika tidak boleh digeser mundur}]
   Hasil: {id:{c:sel, back:geser_mundur_visual}}. Sel = jalur + (baris). Yang di depan diproses dulu; yang di belakang
   pindah ke jalur kosong terdekat untuk MENYALIP. Jika semua penuh (misal di garis start), pelari digeser mundur
   (hanya tampilan) agar membentuk barisan start dan tidak saling menembus. */
window.aesLanePlan=function(list,nLane,nRow,gap){
  var N=nLane*nRow,arr=list.slice().sort(function(a,b){return (b.d-a.d)||(a.k<b.k?-1:a.k>b.k?1:0)});
  var last=new Array(N),out={},maxBack=gap*3;
  arr.forEach(function(it){
    var pref=(it.p>=0&&it.p<N)?it.p:((it.h%N)+N)%N,pl=pref%nLane,pr=Math.floor(pref/nLane),cand=[],c;
    for(c=0;c<N;c++){var ln=c%nLane,rw=Math.floor(c/nLane);cand.push({c:c,cost:Math.abs(ln-pl)+Math.abs(rw-pr)*.6+(c===pref?-.01:0)})}
    cand.sort(function(a,b){return a.cost-b.cost});
    var best=-1,fb=cand[0].c,fbGap=-1e9,i;
    for(i=0;i<cand.length;i++){
      var cc=cand[i].c,g=(last[cc]===undefined)?1e9:last[cc]-it.d;
      if(g>=gap){best=cc;break}
      if(g>fbGap){fbGap=g;fb=cc}
    }
    var back=0;
    if(best<0){best=fb;if(!it.fix)back=Math.min(maxBack,gap-fbGap)}
    last[best]=it.d-back;
    out[it.k]={c:best,back:back};
  });
  return out;
};

</script>
<!-- ===== AES CLASS • TAMBAHAN: UNDUH NILAI LOMBA (Word, khusus lomba, terpisah dari rekap lain) ===== -->
<script>
window.aesRaceDocx=async function(o){
  try{
    var rows=(o&&o.rows)||[];
    if(!rows.length){alert("Belum ada data nilai lomba untuk diunduh.");return}
    if(typeof createWordTableXml!=="function"||typeof buildAndDownloadDocxFile!=="function"){alert("Fitur Word belum siap. Muat ulang halaman lalu coba lagi.");return}
    var P=function(r,a){return createWordParagraphXml(r,a==null?80:a)};
    var out=[];
    out.push(P([{text:o.title,size:36,bold:true,color:"0F172A"}],80));
    out.push(P([{text:"Dicetak: "+new Date().toLocaleString("id-ID"),size:20,color:"475569"}],40));
    (o.info||[]).forEach(function(t){out.push(P([{text:t,size:20,color:"334155"}],40))});
    out.push(P([{text:" ",size:12}],60));
    var n=0;
    var body=rows.map(function(x){
      var fin=x.st==="Selesai";if(fin)n++;
      var col=fin?"166534":(x.st==="Tidak ikut"?"B91C1C":"92400E");
      var tot=(x.ok==null||x.bad==null)?null:(x.ok+x.bad);
      return [
        {text:fin?String(n):"-",align:"center"},
        {text:String(x.n||"-"),bold:true},
        {text:x.st,color:col,bold:true,align:"center"},
        {text:x.time||"-",align:"center"},
        {text:x.ok==null?"-":String(x.ok),align:"center"},
        {text:x.bad==null?"-":String(x.bad),align:"center"},
        {text:tot?Math.round(x.ok/tot*100)+"%":"-",align:"center"},
        {text:x.prog||"-",align:"center"}
      ];
    });
    out.push(createWordTableXml(["No","Nama Siswa","Status","Waktu","Benar","Salah","Akurasi","Progres"],body,"0284C7"));
    await buildAndDownloadDocxFile(out,o.fname||"Nilai_Lomba_AES_CLASS.docx",true);
  }catch(e){alert("Gagal membuat file Word: "+((e&&e.message)||e))}
};
window.aesRaceStamp=function(){var d=new Date(),z=function(n){return(n<10?"0":"")+n};return d.getFullYear()+"-"+z(d.getMonth()+1)+"-"+z(d.getDate())+"_"+z(d.getHours())+z(d.getMinutes())};
</script>
<!-- ===== AES CLASS • TAMBAHAN: BALAP MOBIL (3D, sirkuit bertikungan, jawab A/B/C/D) ===== -->
<style id="cr-style">

#cr-launch{position:fixed;right:.6rem;top:56%;z-index:9400;display:none;align-items:center;gap:6px;padding:9px 13px;border-radius:9999px;background:linear-gradient(135deg,#0ea5e9,#6366f1);color:#fff;font:800 12px 'Plus Jakarta Sans',sans-serif;border:2px solid #fff;box-shadow:0 4px 18px rgba(99,102,241,.55);cursor:pointer;touch-action:manipulation}
#cr-launch:hover{filter:brightness(1.1)}
#cr-overlay{position:fixed;inset:0;z-index:9600;background:#0f172a;display:none;font-family:'Plus Jakarta Sans',"Noto Sans","Segoe UI","Noto Sans Arabic","Noto Sans Hebrew","Noto Sans JP","Hiragino Sans","Yu Gothic","Noto Sans KR","Malgun Gothic","Noto Sans SC","Microsoft YaHei","PingFang SC","Noto Sans TC","Noto Sans Devanagari","Nirmala UI","Noto Sans Thai","Arial Unicode MS",sans-serif;color:#f1f5f9;touch-action:manipulation;overflow:hidden}
#cr-overlay.cr-open{display:block}
#cr-canvas{position:absolute;inset:0}
#cr-canvas canvas{display:block;width:100%;height:100%}
#cr-speedfx{position:absolute;inset:0;pointer-events:none;opacity:0;transition:opacity .25s;background:radial-gradient(ellipse at 50% 45%,rgba(255,255,255,0) 45%,rgba(255,255,255,.28) 100%)}
#cr-hud{position:absolute;top:8px;left:8px;right:8px;display:flex;flex-wrap:wrap;gap:8px;align-items:flex-start;pointer-events:none;z-index:3}
.cr-card{background:rgba(15,23,42,.82);border:1px solid rgba(255,255,255,.28);border-radius:14px;padding:6px 12px;pointer-events:none}
#cr-exit{pointer-events:auto;width:38px;height:38px;border-radius:12px;background:rgba(15,23,42,.85);color:#fecaca;border:1px solid rgba(255,255,255,.35);font-size:16px;font-weight:800;cursor:pointer}
.cr-lbl{font-size:9px;font-weight:800;letter-spacing:.08em;color:#7dd3fc}
#cr-kmh{font-size:26px;font-weight:800;line-height:1;color:#fde047;font-variant-numeric:tabular-nums}
.cr-unit{font-size:10px;color:#cbd5e1;margin-left:3px}
.cr-bar{height:6px;border-radius:9px;background:rgba(255,255,255,.18);margin-top:4px;overflow:hidden;min-width:96px}
#cr-spdbar{display:block;height:100%;width:0;background:linear-gradient(90deg,#22c55e,#facc15,#ef4444);border-radius:9px}
.cr-spacer{flex:1 1 0}
#cr-place{font-size:26px;font-weight:800;line-height:1;color:#fff}
#cr-place small{font-size:12px;color:#94a3b8}
#cr-time{font-size:12px;font-weight:700;color:#bae6fd;font-variant-numeric:tabular-nums;text-align:right}
.cr-track{order:3;flex:1 1 100%;pointer-events:none}
#cr-trackbar{position:relative;height:16px;border-radius:9px;background:rgba(15,23,42,.78);border:1px solid rgba(255,255,255,.3);margin:2px 8px 0 4px}
#cr-trackbar .cr-dot{position:absolute;top:50%;width:11px;height:11px;border-radius:50%;transform:translate(-50%,-50%);border:2px solid #fff;transition:left .15s linear}
#cr-trackbar .cr-dot.me{width:16px;height:16px;z-index:5;box-shadow:0 0 10px #fff}
#cr-trackbar .cr-flag{position:absolute;right:-6px;top:-4px;font-size:15px}
#cr-dist{font-size:10px;font-weight:700;color:#e2e8f0;text-align:center;margin-top:2px;text-shadow:0 1px 3px #000}
#cr-fx{position:absolute;left:0;right:0;top:34%;text-align:center;pointer-events:none;z-index:4;font-size:clamp(22px,6vw,44px);font-weight:800;text-shadow:0 3px 14px rgba(0,0,0,.7);opacity:0}
#cr-fx.show{animation:crpop .9s ease-out}
#cr-fx.ok{color:#4ade80}#cr-fx.bad{color:#fb7185}
#cr-flash{position:absolute;inset:0;pointer-events:none;z-index:2;opacity:0}
#cr-flash.ok.go{animation:crflash .5s ease-out;box-shadow:inset 0 0 130px 40px rgba(74,222,128,.6)}
#cr-flash.bad.go{animation:crflash .6s ease-out;box-shadow:inset 0 0 140px 50px rgba(244,63,94,.7)}
@keyframes crflash{0%{opacity:1}100%{opacity:0}}
@keyframes crpop{0%{opacity:0;transform:scale(.6) translateY(14px)}20%{opacity:1;transform:scale(1.15)}100%{opacity:0;transform:scale(1) translateY(-30px)}}
#cr-count{position:absolute;left:0;right:0;top:26%;text-align:center;font-size:clamp(60px,18vw,150px);font-weight:800;color:#fff;text-shadow:0 6px 30px rgba(0,0,0,.7);pointer-events:none;z-index:4}
#cr-qpanel{position:absolute;left:0;right:0;bottom:0;max-height:47vh;overflow-y:auto;padding:10px 12px calc(10px + env(safe-area-inset-bottom,0px));background:linear-gradient(to top,rgba(15,23,42,.97),rgba(15,23,42,.9));border-top:1px solid rgba(125,211,252,.5);z-index:3;touch-action:pan-y;display:none}
#cr-qpanel.show{display:block}
.cr-qhead{display:flex;align-items:center;justify-content:space-between;gap:8px;font-size:11px;font-weight:800;margin-bottom:5px}
.cr-chip{padding:2px 8px;border-radius:9999px;background:rgba(255,255,255,.12)}
.cr-chip.ok{color:#4ade80}.cr-chip.bad{color:#fb7185}.cr-chip.fire{color:#fdba74}
#cr-qtext{font-size:clamp(12px,2.6vw,17px);font-weight:700;line-height:1.35;margin-bottom:8px;overflow-wrap:anywhere}
#cr-qtext img,#cr-qimg{max-height:110px;border-radius:10px;margin:4px auto;display:block}
#cr-opts{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.cr-opt{display:flex;align-items:center;gap:8px;text-align:left;padding:8px 10px;min-height:48px;border-radius:12px;background:rgba(30,41,59,.95);border:2px solid rgba(255,255,255,.22);color:#fff;font:700 clamp(11px,2.3vw,15px) 'Plus Jakarta Sans',sans-serif;cursor:pointer;overflow-wrap:anywhere;touch-action:manipulation;transition:transform .08s}
.cr-opt:active{transform:scale(.97)}
.cr-opt b{flex:0 0 auto;width:28px;height:28px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:14px;color:#0f172a}
.cr-opt:nth-child(1) b{background:#38bdf8}.cr-opt:nth-child(2) b{background:#4ade80}.cr-opt:nth-child(3) b{background:#fbbf24}.cr-opt:nth-child(4) b{background:#fb7185}
.cr-opt.cr-ok{background:#15803d;border-color:#4ade80}
.cr-opt.cr-bad{background:#9f1239;border-color:#fb7185}
.cr-opt[disabled]{cursor:default}
#cr-fb{font-size:11px;font-weight:800;min-height:15px;margin-top:6px}
.cr-modal{position:absolute;inset:0;z-index:6;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.62);overflow-y:auto}
.cr-modal.cr-hide{display:none}
#cr-tpanel{position:fixed;inset:0;z-index:9600;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.72);overflow-y:auto}
#cr-tpanel.cr-hide{display:none}
#cr-t-stat{font-size:12px;font-weight:800;color:#fde047;text-align:center;margin:8px 0}
#cr-t-table{max-height:34vh;overflow-y:auto;margin-bottom:8px}
.cr-bar2{height:5px;border-radius:9px;background:rgba(255,255,255,.14);overflow:hidden;margin-top:3px}
.cr-bar2 i{display:block;height:100%;background:linear-gradient(90deg,#38bdf8,#4ade80);width:0}
#cr-result{background:rgba(2,6,23,.3)}
.cr-box{width:min(94vw,470px);max-height:94vh;overflow-y:auto;background:#0f172a;border:2px solid rgba(125,211,252,.55);border-radius:20px;padding:18px 18px 16px;box-shadow:0 18px 60px rgba(0,0,0,.6)}
.cr-box h2{margin:0 0 4px;font-size:21px;font-weight:800;color:#fde047;text-align:center}
.cr-box p{margin:0 0 10px;font-size:12px;color:#cbd5e1;text-align:center;line-height:1.45}
.cr-rules{font-size:12px;color:#e2e8f0;line-height:1.5;background:rgba(255,255,255,.06);border-radius:12px;padding:8px 12px;margin-bottom:10px}
.cr-sel{margin-bottom:10px}
.cr-sel .cr-lbl{margin-bottom:4px}
.cr-seg{display:flex;gap:6px}
.cr-seg button{flex:1;padding:8px 4px;border-radius:10px;background:rgba(255,255,255,.08);border:2px solid transparent;color:#e2e8f0;font:800 11px 'Plus Jakarta Sans',sans-serif;cursor:pointer}
.cr-seg button.on{background:rgba(250,204,21,.18);border-color:#facc15;color:#fde047}
.cr-btn{width:100%;padding:12px;border-radius:14px;border:0;background:linear-gradient(135deg,#22c55e,#16a34a);color:#fff;font:800 15px 'Plus Jakarta Sans',sans-serif;cursor:pointer;margin-top:4px}
.cr-btn.alt{background:rgba(255,255,255,.1);font-size:12px;padding:9px}
.cr-btn:disabled{opacity:.5}
.cr-row{display:flex;align-items:center;gap:8px;padding:7px 10px;border-radius:10px;background:rgba(255,255,255,.06);margin-bottom:5px;font-size:12px;font-weight:700}
.cr-row.me{background:rgba(250,204,21,.2);border:1px solid #facc15}
.cr-row .pl{width:26px;font-weight:800;color:#fde047}
.cr-row .nm{flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.cr-row .tm{color:#bae6fd;font-variant-numeric:tabular-nums}
.cr-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:6px;margin:8px 0 10px}
.cr-stats div{background:rgba(255,255,255,.07);border-radius:10px;padding:6px 4px;text-align:center}
.cr-stats b{display:block;font-size:17px;color:#fff}
.cr-stats span{font-size:9px;color:#94a3b8;font-weight:700}
@media (orientation:portrait){
 #cr-hud{gap:6px}
 .cr-card{padding:5px 9px}
 #cr-kmh,#cr-place{font-size:22px}
 .cr-bar{min-width:78px}
 #cr-qpanel{max-height:52vh}
 #cr-qtext{font-size:clamp(14px,4vw,18px)}
 .cr-opt{font:700 clamp(13px,3.7vw,16px) 'Plus Jakarta Sans',sans-serif;min-height:52px}
 #cr-fx{top:30%}
 #cr-count{top:22%}
 .cr-box{max-height:92vh}
}
@media (max-height:520px) and (orientation:landscape){
 #cr-qpanel{left:auto;right:8px;bottom:8px;top:104px;width:min(54vw,540px);max-height:none;border-radius:14px;border:1px solid rgba(125,211,252,.5)}
 #cr-kmh,#cr-place{font-size:19px}
 .cr-card{padding:4px 9px}
}

#cr-lapcard #cr-lap{font-size:22px;font-weight:800;line-height:1;color:#fff;text-align:center}
#cr-lapcard #cr-lap small{font-size:11px;color:#94a3b8}
#cr-mm{position:absolute;right:8px;top:106px;width:100px;height:100px;z-index:3;border-radius:14px;background:rgba(15,23,42,.72);border:1px solid rgba(255,255,255,.28);pointer-events:none}
#cr-corner{position:absolute;left:8px;top:106px;max-width:calc(100% - 130px);z-index:3;padding:5px 11px;border-radius:9999px;background:rgba(15,23,42,.82);border:1px solid rgba(255,255,255,.3);font-size:12px;font-weight:800;color:#e2e8f0;pointer-events:none;display:none;white-space:nowrap}
#cr-corner.warn{background:#b45309;border-color:#fde68a;color:#fff}
#cr-corner.slip{background:#be123c;border-color:#fecdd3;color:#fff}
.cr-seg3 button{font-size:11px}
@media (max-height:520px) and (orientation:landscape){
 #cr-mm{right:auto;left:8px;top:auto;bottom:8px;width:84px;height:84px}
 #cr-corner{top:98px}
}
.cr-opt img{max-height:90px;max-width:100%;object-fit:contain;margin:2px 0;border-radius:8px}
.cr-opt .my-3{margin:2px 0}
.cr-opt a{pointer-events:none;color:inherit;text-decoration:none}
.cr-opt .aes-video,.cr-opt video{display:none}
#cr-qtext,.cr-opt span{unicode-bidi:plaintext}

</style>

<button id="cr-launch" type="button" onclick="AESCar.open()">🏎️ BALAP MOBIL</button>

<div id="cr-overlay">
 <div id="cr-canvas"></div>
 <div id="cr-speedfx"></div>
 <div id="cr-flash"></div>
 <div id="cr-hud">
  <button id="cr-exit" type="button" title="Keluar">✕</button>
  <div class="cr-card"><div class="cr-lbl">KECEPATAN</div><div><span id="cr-kmh">0</span><span class="cr-unit">km/jam</span></div><div class="cr-bar"><i id="cr-spdbar"></i></div></div>
  <div class="cr-spacer"></div>
  <div class="cr-card" id="cr-lapcard"><div class="cr-lbl" style="text-align:center">PUTARAN</div><div id="cr-lap">1<small>/1</small></div></div>
  <div class="cr-card"><div class="cr-lbl" style="text-align:right">POSISI</div><div id="cr-place">#1<small>/6</small></div><div id="cr-time">00:00.0</div></div>
  <div class="cr-track"><div id="cr-trackbar"><span class="cr-flag">🏁</span></div><div id="cr-dist">0 / 0 m</div></div>
 </div>
 <canvas id="cr-mm" width="200" height="200"></canvas>
 <div id="cr-corner"></div>
 <div id="cr-fx"></div>
 <div id="cr-count"></div>
 <div id="cr-qpanel">
  <div class="cr-qhead"><span id="cr-qno">Soal 1</span><span><span class="cr-chip ok" id="cr-cok">✓0</span> <span class="cr-chip bad" id="cr-cbad">✗0</span> <span class="cr-chip fire" id="cr-cstreak">🔥0</span></span></div>
  <div id="cr-qtext"></div>
  <div id="cr-opts"></div>
  <div id="cr-fb"></div>
 </div>

 <div id="cr-start" class="cr-modal">
  <div class="cr-box">
   <h2>🏎️ BALAP MOBIL AES CLASS</h2>
   <p id="cr-who">Siap, pembalap?</p>
   <div class="cr-rules">
    • Mobilmu <b>melaju otomatis</b> di sirkuit yang punya <b>tikungan</b>; tugasmu menjawab soal.<br>
    • Pilih jawaban <b>A / B / C / D</b> (bisa juga tekan tombol keyboard A-D atau 1-4).<br>
    • Jawaban <b style="color:#4ade80">benar</b> = mobil makin <b>ngebut</b> 🚀. Jawaban <b style="color:#fb7185">salah</b> = <b>melambat</b> 🐢.<br>
    • Awas <b>tikungan</b>: kalau terlalu ngebut, mobil <b>tergelincir</b> ke luar jalur dan kecepatannya turun. Perhatikan penanda tikungan di layar.<br>
    • Kamu berlomba melawan pembalap komputer. Jadilah yang pertama melewati garis finish!
   </div>
   <div class="cr-sel"><div class="cr-lbl">SIRKUIT</div><div class="cr-seg" id="cr-seg-circ"><button data-v="oval" class="on">Oval Lebar</button><button data-v="berliku">Berliku (banyak tikungan)</button></div></div>
   <div class="cr-sel"><div class="cr-lbl">JUMLAH PUTARAN</div><div class="cr-seg" id="cr-seg-laps"><button data-v="1">1 putaran</button><button data-v="2" class="on">2 putaran</button><button data-v="3">3 putaran</button></div></div>
   <div class="cr-sel"><div class="cr-lbl">LAWAN KOMPUTER</div><div class="cr-seg" id="cr-seg-lvl"><button data-v="0">Santai</button><button data-v="1" class="on">Sedang</button><button data-v="2">Ngebut</button></div></div>
   <div id="cr-best" style="font-size:11px;color:#94a3b8;text-align:center;margin-bottom:6px"></div>
   <button class="cr-btn" id="cr-go" type="button">▶ MULAI BALAPAN</button>
   <button class="cr-btn alt" id="cr-close1" type="button">Tutup</button>
  </div>
 </div>

 <div id="cr-result" class="cr-modal cr-hide">
  <div class="cr-box">
   <h2 id="cr-rtitle">🏁 FINISH!</h2>
   <p id="cr-rsub"></p>
   <div class="cr-stats" id="cr-rstats"></div>
   <div id="cr-rtable"></div>
   <button class="cr-btn" id="cr-again" type="button">🔄 Main Lagi</button>
   <button class="cr-btn alt" id="cr-close2" type="button">Tutup</button>
  </div>
 </div>

 <div id="cr-miss" class="cr-modal cr-hide">
  <div class="cr-box">
   <h2>🏁 BALAPAN SUDAH DIMULAI</h2>
   <p id="cr-miss-t">Guru sudah memulai balapan mobil, tetapi kamu belum ikut. Mobilmu berdiri diam di garis start. Tunggu guru mengakhiri balapan — skormu akan muncul di sini.</p>
   <button class="cr-btn alt" id="cr-close3" type="button">Tutup</button>
  </div>
 </div>
</div>

<div id="cr-tpanel" class="cr-hide">
 <div class="cr-box">
  <h2>🏎️ BALAP MOBIL • PANEL GURU</h2>
  <p>Tekan <b>MULAI</b>: balapan langsung berjalan di layar semua siswa yang sudah masuk. Siswa saling berlomba di sirkuit yang sama.</p>
  <div class="cr-sel"><div class="cr-lbl">SIRKUIT</div><div class="cr-seg" id="cr-t-seg-circ"><button data-v="oval" class="on">Oval Lebar</button><button data-v="berliku">Berliku</button></div></div>
  <div class="cr-sel"><div class="cr-lbl">JUMLAH PUTARAN</div><div class="cr-seg" id="cr-t-seg-laps"><button data-v="1">1 putaran</button><button data-v="2" class="on">2 putaran</button><button data-v="3">3 putaran</button></div></div>
  <button class="cr-btn" id="cr-t-go" type="button">📣 MULAI BALAPAN SEMUA SISWA</button>
  <button class="cr-btn alt" id="cr-t-stop" type="button">🏁 Akhiri balapan &amp; umumkan skor</button>
  <div id="cr-t-stat">Belum ada balapan yang dimulai.</div>
  <div id="cr-t-table"></div>
  <button class="cr-btn alt" id="cr-t-docx" type="button">📄 Unduh nilai lomba (Word)</button>
  <button class="cr-btn alt" id="cr-t-self" type="button">🏎️ Coba sendiri (latihan melawan komputer)</button>
  <button class="cr-btn alt" id="cr-t-close" type="button">Tutup</button>
 </div>
</div>

<script id="cr-script">
(function(){
"use strict";
if(window.AESCar)return;

/* ---------- helper aman (memakai fungsi bawaan aplikasi bila ada) ---------- */
var $=function(id){return document.getElementById(id)};
function esc(s){return String(s==null?"":s).replace(/[&<>"]/g,function(c){return{"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]})}
function rich(s){try{if(typeof formatRichEducationalText==="function")return formatRichEducationalText(s,1)}catch(e){}return esc(s)}
function typeset(a){try{if(typeof triggerMathJaxRender==="function")triggerMathJaxRender(a)}catch(e){}}
function sfx(n){try{if(typeof playSoundEffect==="function")playSoundEffect(n)}catch(e){}}
function clamp(v,a,b){return v<a?a:v>b?b:v}
function rnd(a,b){return a+Math.random()*(b-a)}
function shuffle(a){for(var i=a.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1)),t=a[i];a[i]=a[j];a[j]=t}return a}

function getQs(){
  try{
    var qs=(typeof gameConfig!=="undefined"&&gameConfig&&gameConfig.questions)||[];
    return qs.filter(function(q){return q&&q.q&&Array.isArray(q.options)&&q.options.filter(function(o){return String(o||"").trim()}).length>=2});
  }catch(e){return[]}
}
function optOrder(q){
  try{if(typeof getShuffledOrder==="function")return getShuffledOrder(q.options)}catch(e){}
  var idx=[];q.options.forEach(function(o,i){if(String(o||"").trim())idx.push(i)});return shuffle(idx);
}
function myName(){try{return(myPlayer&&myPlayer.name)||(typeof isTeacherMode!=="undefined"&&isTeacherMode?"Guru":"Kamu")}catch(e){return"Kamu"}}
function myColor(){try{return(myPlayer&&myPlayer.color)||"#0ea5e9"}catch(e){return"#0ea5e9"}}
function otherNames(){
  var pool=[];
  try{(gameConfig.students||[]).forEach(function(n){n=String(n||"").trim();if(n&&n!==myName())pool.push(n)})}catch(e){}
  shuffle(pool);
  var fb=shuffle(["Rani","Dimas","Putri","Fajar","Salsa","Rizky","Nadia","Bagas"]);
  while(pool.length<5)pool.push(fb.pop()||("Lawan "+pool.length));
  return pool.slice(0,5);
}

/* ---------- matematika sirkuit: spline Catmull-Rom sentripetal tertutup, disampel rata per panjang busur ---------- */
function crPoint(p0,p1,p2,p3,t){
  function d(a,b){return Math.pow(Math.sqrt((b[0]-a[0])*(b[0]-a[0])+(b[1]-a[1])*(b[1]-a[1]))||1e-6,.5)}
  var t0=0,t1=t0+d(p0,p1),t2=t1+d(p1,p2),t3=t2+d(p2,p3),tt=t1+(t2-t1)*t,r=[0,0];
  for(var k=0;k<2;k++){
    var A1=(t1-tt)/(t1-t0)*p0[k]+(tt-t0)/(t1-t0)*p1[k];
    var A2=(t2-tt)/(t2-t1)*p1[k]+(tt-t1)/(t2-t1)*p2[k];
    var A3=(t3-tt)/(t3-t2)*p2[k]+(tt-t2)/(t3-t2)*p3[k];
    var B1=(t2-tt)/(t2-t0)*A1+(tt-t0)/(t2-t0)*A2;
    var B2=(t3-tt)/(t3-t1)*A2+(tt-t1)/(t3-t1)*A3;
    r[k]=(t2-tt)/(t2-t1)*B1+(tt-t1)/(t2-t1)*B2;
  }
  return r;
}
/* hasil: P titik tengah jalur, T arah (satuan), K kelengkungan bertanda (+ = belok kanan, - = belok kiri, satuan 1/m) */
function buildTrack(ctrl,step){
  var n=ctrl.length,dense=[],sub=40,i,j;
  for(i=0;i<n;i++){
    var p0=ctrl[(i-1+n)%n],p1=ctrl[i],p2=ctrl[(i+1)%n],p3=ctrl[(i+2)%n];
    for(j=0;j<sub;j++)dense.push(crPoint(p0,p1,p2,p3,j/sub));
  }
  var cum=[0];
  for(i=1;i<=dense.length;i++){var a=dense[i-1],b=dense[i%dense.length];cum.push(cum[i-1]+Math.hypot(b[0]-a[0],b[1]-a[1]))}
  var total=cum[cum.length-1],N=Math.max(24,Math.round(total/step)),ds=total/N,P=[],k=0;
  for(i=0;i<N;i++){
    var s=i*ds;while(cum[k+1]<s)k++;
    var f=(s-cum[k])/((cum[k+1]-cum[k])||1),a2=dense[k],b2=dense[(k+1)%dense.length];
    P.push([a2[0]+(b2[0]-a2[0])*f,a2[1]+(b2[1]-a2[1])*f]);
  }
  var T=[],K=[];
  for(i=0;i<N;i++){var u=P[(i-1+N)%N],w=P[(i+1)%N],dx=w[0]-u[0],dz=w[1]-u[1],l=Math.hypot(dx,dz)||1;T.push([dx/l,dz/l])}
  for(i=0;i<N;i++){
    var t0=T[(i-1+N)%N],t1=T[(i+1)%N],cr=t0[0]*t1[1]-t0[1]*t1[0],dt=t0[0]*t1[0]+t0[1]*t1[1];
    K.push(Math.atan2(cr,dt)/(2*ds));
  }
  var K2=K.map(function(_,i){var s=0;for(var d=-2;d<=2;d++)s+=K[(i+d+N)%N];return s/5});
  return{P:P,T:T,K:K2,N:N,ds:ds,len:total};
}
function posAt(tr,dist,lat){
  var u=(((dist%tr.len)+tr.len)%tr.len)/tr.ds,i=Math.floor(u)%tr.N,f=u-Math.floor(u),j=(i+1)%tr.N;
  var px=tr.P[i][0]+(tr.P[j][0]-tr.P[i][0])*f,pz=tr.P[i][1]+(tr.P[j][1]-tr.P[i][1])*f;
  var tx=tr.T[i][0]+(tr.T[j][0]-tr.T[i][0])*f,tz=tr.T[i][1]+(tr.T[j][1]-tr.T[i][1])*f,l=Math.hypot(tx,tz)||1;tx/=l;tz/=l;
  return{x:px-tz*lat,z:pz+tx*lat,tx:tx,tz:tz,h:Math.atan2(tx,tz)};
}
function curvAt(tr,dist){
  var u=(((dist%tr.len)+tr.len)%tr.len)/tr.ds,i=Math.floor(u)%tr.N,j=(i+1)%tr.N,f=u-Math.floor(u);
  return tr.K[i]+(tr.K[j]-tr.K[i])*f;
}

/* ---------- konstanta permainan ---------- */
var STUDENT_SOLO=false;   // true = siswa yang sudah masuk juga boleh berlatih sendiri melawan komputer (default: hanya guru, seperti Lomba Lari)
var NLANE=8,LANEW=3,ROADW=NLANE*LANEW,CURB=1.3,WALLOFF=ROADW/2+CURB+2.2;
var BASEV=14.5,MINV=5,MAXV=48,BOOST=4.8,SLOW=6.7,ALAT=26,RUNOFF=90;
/* TARGET SOAL: jarak yang boleh ditempuh = jumlah jawaban benar / target soal x panjang balapan */
function qNeed(){return S.laps<=1?8:S.laps===2?12:16}
var CREEP=BASEV*.18; /* kecepatan merayap saat belum menjawab: tetap bergerak, tapi pelan */
function capQ(r){var n=qNeed();return r.correct>=n?Infinity:S.L*r.correct/n}
var LEVELS=[{acc:[.35,.6],think:[5,8]},{acc:[.55,.8],think:[4,6.5]},{acc:[.75,.95],think:[3,5]}];
var BOTCOL=["#ef4444","#f59e0b","#22c55e","#a855f7","#ec4899","#14b8a6"];
var CIRCUITS={
  oval:{name:"Oval Lebar",R:140,n:28,t:[[.30,2,"c"],[.05,3,"s"]]},
  berliku:{name:"Berliku",R:150,n:36,t:[[.26,2,"c"],[.14,3,"s"],[.06,5,"c"],[.05,4,"s"]]}
};
var TRK={};
function getTrack(key){
  if(TRK[key])return TRK[key];
  var d=CIRCUITS[key]||CIRCUITS.oval,ctrl=[],i;
  for(i=0;i<d.n;i++){
    var th=i/d.n*Math.PI*2,r=1;
    d.t.forEach(function(q){r+=q[0]*(q[2]==="s"?Math.sin(q[1]*th):Math.cos(q[1]*th))});
    ctrl.push([d.R*r*Math.cos(th),d.R*r*Math.sin(th)]);
  }
  var tr=buildTrack(ctrl,2.5),N=tr.N,w=Math.round(55/tr.ds),best=0,bs=1e9;
  for(i=0;i<N;i++){var s=0;for(var q=-w;q<=w;q++)s+=Math.abs(tr.K[(i+q+N)%N]);if(s<bs){bs=s;best=i}}
  function rot(a){return a.slice(best).concat(a.slice(0,best))}
  tr.P=rot(tr.P);tr.T=rot(tr.T);tr.K=rot(tr.K); // garis start/finish di bagian paling lurus
  var x0=1e9,x1=-1e9,z0=1e9,z1=-1e9;
  tr.P.forEach(function(p){x0=Math.min(x0,p[0]);x1=Math.max(x1,p[0]);z0=Math.min(z0,p[1]);z1=Math.max(z1,p[1])});
  tr.box={x0:x0,x1:x1,z0:z0,z1:z1};tr.key=key;tr.name=d.name;
  return TRK[key]=tr;
}

/* ---------- state ---------- */
var S={open:false,state:"idle",circ:"oval",laps:2,lvl:1,L:0,tr:null,raf:0,last:0,T:0,cd:0,cdStep:0,timers:[],
  renderer:null,scene:null,camera:null,racers:[],me:null,finishCount:0,
  qList:[],qPtr:0,cur:null,locked:true,streak:0,bestStreak:0,maxV:0,stumble:0,resultShown:false,lastQ:-1,
  shake:0,kick:0,roll:0,orbit:0,fwT:0,pool:null,lowFx:false,mmBase:null,tmm:0,mode:null,auto:null,remote:{},pubN:0,pubT:0,rt:0,mt:0};
function later(fn,ms){var id=setTimeout(function(){fn()},ms);S.timers.push(id);return id}
function clearTimers(){S.timers.forEach(clearTimeout);S.timers=[]}

/* ---------- tombol peluncur ---------- */
function isTeacherNow(){try{return typeof isTeacherMode!=="undefined"&&!!isTeacherMode}catch(e){return false}}
function canShowLauncher(){
  if(S.open)return false;
  try{var tp=$("cr-tpanel");if(tp&&!tp.classList.contains("cr-hide"))return false}catch(e){}
  try{if(window.AESRun&&window.AESRun._state&&window.AESRun._state.open)return false}catch(e){}
  var hud=$("game-hud"),ts=$("teacher-screen");
  var hudOn=hud&&!hud.classList.contains("hidden"),tsOn=ts&&!ts.classList.contains("hidden");
  try{
    if(isTeacherNow())return !!(hudOn||tsOn);
    if(STUDENT_SOLO)return !!(hudOn&&myPlayer&&myPlayer.hasJoinedGame);
    return false;
  }catch(e){return false}
}
setInterval(function(){var b=$("cr-launch");if(b)b.style.display=canShowLauncher()?"flex":"none"},500);

/* ---------- 3D: tekstur & model ---------- */
function textTex(text,w,h,o){
  var c=document.createElement("canvas");c.width=w;c.height=h;var x=c.getContext("2d");
  if(o.bg){x.fillStyle=o.bg;x.fillRect(0,0,w,h)}
  x.fillStyle=o.fg||"#fff";x.font=o.font||"bold 40px sans-serif";x.textAlign="center";x.textBaseline="middle";x.fillText(text,w/2,h/2);
  var t=new THREE.CanvasTexture(c);t.anisotropy=4;return t;
}
function nameSprite(name,isMe){
  var c=document.createElement("canvas");c.width=320;c.height=72;var x=c.getContext("2d");
  x.fillStyle=isMe?"rgba(250,204,21,.95)":"rgba(15,23,42,.82)";
  var r=30;x.beginPath();x.moveTo(r,4);x.lineTo(320-r,4);x.quadraticCurveTo(316,4,316,r);x.lineTo(316,72-r);x.quadraticCurveTo(316,68,320-r,68);x.lineTo(r,68);x.quadraticCurveTo(4,68,4,72-r);x.lineTo(4,r);x.quadraticCurveTo(4,4,r,4);x.fill();
  x.fillStyle=isMe?"#0f172a":"#fff";x.font="bold 34px sans-serif";x.textAlign="center";x.textBaseline="middle";
  var t=String(name);if(t.length>14)t=t.slice(0,13)+"…";x.fillText(t,160,38);
  var tex=new THREE.CanvasTexture(c);var sp=new THREE.Sprite(new THREE.SpriteMaterial({map:tex,transparent:true,depthWrite:false}));
  sp.scale.set(3.1,.7,1);return sp;
}
function roadTex(){
  var c=document.createElement("canvas");c.width=256;c.height=256;var x=c.getContext("2d");
  x.fillStyle="#3a3f47";x.fillRect(0,0,256,256);
  for(var i=0;i<1800;i++){var g=40+Math.floor(Math.random()*40);x.fillStyle="rgba("+g+","+g+","+(g+6)+",.45)";x.fillRect(Math.random()*256,Math.random()*256,2,2)}
  x.fillStyle="#fff";
  x.fillRect(5,0,6,256);x.fillRect(245,0,6,256);                 // garis tepi
  for(var k=1;k<NLANE;k++){var lx=Math.round(k*256/NLANE)-2;for(var y=0;y<256;y+=64)x.fillRect(lx,y,4,32)} // garis lajur putus-putus
  var t=new THREE.CanvasTexture(c);t.wrapS=THREE.ClampToEdgeWrapping;t.wrapT=THREE.RepeatWrapping;t.anisotropy=4;return t;
}
function grassTex(){
  var c=document.createElement("canvas");c.width=128;c.height=128;var x=c.getContext("2d");
  x.fillStyle="#3f9d5c";x.fillRect(0,0,128,128);
  for(var i=0;i<900;i++){x.fillStyle=Math.random()<.5?"rgba(30,110,60,.35)":"rgba(110,190,100,.3)";x.fillRect(Math.random()*128,Math.random()*128,3,3)}
  var t=new THREE.CanvasTexture(c);t.wrapS=t.wrapT=THREE.RepeatWrapping;t.repeat.set(260,260);return t;
}
function checkerTex(){
  var c=document.createElement("canvas");c.width=128;c.height=32;var x=c.getContext("2d");
  for(var a=0;a<16;a++)for(var b=0;b<4;b++){x.fillStyle=(a+b)%2?"#111":"#fff";x.fillRect(a*8,b*8,8,8)}
  var t=new THREE.CanvasTexture(c);t.anisotropy=4;return t;
}
function crowdTex(){
  var c=document.createElement("canvas");c.width=256;c.height=64;var x=c.getContext("2d");
  x.fillStyle="#475569";x.fillRect(0,0,256,64);
  var cols=["#ef4444","#facc15","#38bdf8","#4ade80","#f472b6","#fff","#fb923c"];
  for(var i=0;i<420;i++){x.fillStyle=cols[Math.floor(Math.random()*cols.length)];x.beginPath();x.arc(Math.random()*256,6+Math.random()*54,2.6,0,6.3);x.fill()}
  return new THREE.CanvasTexture(c);
}
function softTex(){
  var c=document.createElement("canvas");c.width=c.height=64;var x=c.getContext("2d");
  var g=x.createRadialGradient(32,32,2,32,32,31);g.addColorStop(0,"rgba(255,255,255,1)");g.addColorStop(1,"rgba(255,255,255,0)");
  x.fillStyle=g;x.fillRect(0,0,64,64);return new THREE.CanvasTexture(c);
}

/* pita jalan: a,b = posisi lateral tepi kiri/kanan (kanan positif), y = tinggi */
function ribbon(tr,a,b,y,vrep,alt){
  var N=tr.N,pos=[],nor=[],uv=[],col=[],idx=[],i;
  for(i=0;i<=N;i++){
    var k=i%N,p=tr.P[k],t=tr.T[k],nx=-t[1],nz=t[0],v=i*tr.ds/vrep;
    pos.push(p[0]+nx*a,y,p[1]+nz*a,p[0]+nx*b,y,p[1]+nz*b);
    nor.push(0,1,0,0,1,0);uv.push(0,v,1,v);
    if(alt){var c=(Math.floor(i/2)%2)?alt[0]:alt[1];col.push(c.r,c.g,c.b,c.r,c.g,c.b)}
  }
  for(i=0;i<N;i++){var j=i*2;idx.push(j,j+2,j+1,j+1,j+2,j+3)}
  var g=new THREE.BufferGeometry();
  g.setAttribute("position",new THREE.Float32BufferAttribute(pos,3));
  g.setAttribute("normal",new THREE.Float32BufferAttribute(nor,3));
  g.setAttribute("uv",new THREE.Float32BufferAttribute(uv,2));
  if(alt)g.setAttribute("color",new THREE.Float32BufferAttribute(col,3));
  g.setIndex(idx);return g;
}
/* dinding pembatas tegak di jarak lateral lat */
function wall(tr,lat,h,alt){
  var N=tr.N,pos=[],nor=[],col=[],idx=[],i;
  for(i=0;i<=N;i++){
    var k=i%N,p=tr.P[k],t=tr.T[k],nx=-t[1],nz=t[0],x=p[0]+nx*lat,z=p[1]+nz*lat;
    pos.push(x,0,z,x,h,z);nor.push(nx,0,nz,nx,0,nz);
    var c=(Math.floor(i/6)%2)?alt[0]:alt[1];col.push(c.r,c.g,c.b,c.r,c.g,c.b);
  }
  for(i=0;i<N;i++){var j=i*2;idx.push(j,j+1,j+2,j+1,j+3,j+2)}
  var g=new THREE.BufferGeometry();
  g.setAttribute("position",new THREE.Float32BufferAttribute(pos,3));
  g.setAttribute("normal",new THREE.Float32BufferAttribute(nor,3));
  g.setAttribute("color",new THREE.Float32BufferAttribute(col,3));
  g.setIndex(idx);return g;
}

/* ---------- partikel (asap ban, debu, konfeti) ---------- */
function Pool(scene,n,tex){
  this.items=[];
  for(var i=0;i<n;i++){
    var m=new THREE.SpriteMaterial({map:tex,transparent:true,depthWrite:false,opacity:0});
    var sp=new THREE.Sprite(m);sp.visible=false;scene.add(sp);
    this.items.push({sp:sp,life:0,max:1,vx:0,vy:0,vz:0,s0:1,s1:1,op:1,g:0});
  }
  this.n=n;this.ptr=0;
}
Pool.prototype.emit=function(x,y,z,vx,vy,vz,life,s0,s1,color,op,g){
  var it=this.items[this.ptr];this.ptr=(this.ptr+1)%this.n;
  it.life=life;it.max=life;it.vx=vx;it.vy=vy;it.vz=vz;it.s0=s0;it.s1=s1;it.op=op;it.g=g||0;
  it.sp.position.set(x,y,z);it.sp.material.color.setHex(color);it.sp.visible=true;it.sp.scale.set(s0,s0,1);it.sp.material.opacity=op;
};
Pool.prototype.update=function(dt){
  for(var i=0;i<this.n;i++){
    var it=this.items[i];if(it.life<=0)continue;
    it.life-=dt;
    if(it.life<=0){it.sp.visible=false;it.sp.material.opacity=0;continue}
    var q=1-it.life/it.max;
    it.vy-=it.g*dt;
    it.sp.position.x+=it.vx*dt;it.sp.position.y=Math.max(.05,it.sp.position.y+it.vy*dt);it.sp.position.z+=it.vz*dt;
    var s=it.s0+(it.s1-it.s0)*q;it.sp.scale.set(s,s,1);
    it.sp.material.opacity=it.op*(1-q);
  }
};

/* ---------- model mobil (arah depan = +Z) ---------- */
/* ---------- mobil balap = MOBIL TERBUKA YANG SAMA DENGAN MOBIL KOTA (dibeli dengan koin), siswa duduk di dalamnya ---------- */
var TOWN_S=.55; /* skala agar mobil kota (panjang ±9 m) muat di jalur balap */
function disposeTree(o){
  try{o.traverse(function(x){if(x.geometry)x.geometry.dispose();if(x.material){(Array.isArray(x.material)?x.material:[x.material]).forEach(function(m){if(m.map)m.map.dispose();m.dispose()})}})}catch(e){}
}
function dropCarMesh(r){try{if(r.mesh){S.scene.remove(r.mesh);disposeTree(r.mesh)}}catch(e){}r.mesh=null}
function makeTownCar(color,name,isMe,tier){
  if(typeof createRobotCharacterMesh!=="function"||typeof applyEquipToMesh!=="function")return null;
  var robot=createRobotCharacterMesh(name,color);
  var ns0=robot.userData&&robot.userData.nameSprite;
  if(ns0){robot.remove(ns0);try{ns0.material.map.dispose();ns0.material.dispose()}catch(e){}}
  var eq=null;try{if(isMe&&myPlayer&&myPlayer.equip)eq=myPlayer.equip}catch(e){}
  applyEquipToMesh(robot,eq||{},"car");   // sama persis dengan siswa naik mobil di kota
  var cg=robot.userData&&robot.userData.carGroup;
  if(!cg||!cg.userData||!cg.userData.wheels||!cg.userData.wheels.length)return null;
  robot.position.y=(typeof CAR_LIFT==="number")?CAR_LIFT:.6;   // mobil menapak di jalan, siswa duduk di atas jok
  var g=new THREE.Group(),body=new THREE.Group(),inner=new THREE.Group();
  inner.scale.set(TOWN_S,TOWN_S,TOWN_S);inner.add(robot);body.add(inner);g.add(body);
  var sh=new THREE.Mesh(new THREE.PlaneGeometry(2.8,5.6),new THREE.MeshBasicMaterial({color:0x000000,transparent:true,opacity:.28,depthWrite:false}));
  sh.rotation.x=-Math.PI/2;sh.position.y=.04;g.add(sh);
  var ns=nameSprite(name,isMe);ns.position.y=3.5+(tier%3)*.8;g.add(ns);
  g.userData={wheels:cg.userData.wheels,body:body};
  return g;
}
function makeCar(color,name,isMe,tier,hi){
  var g=null;
  if(hi){try{g=makeTownCar(color,name,isMe,tier)}catch(e){g=null}}
  return g||makeCarBasic(color,name,isMe,tier);
}
function makeCarBasic(color,name,isMe,tier){
  var g=new THREE.Group(),u={wheels:[]};
  var body=new THREE.Group();g.add(body);u.body=body;
  var paint=new THREE.MeshLambertMaterial({color:color}),dark=new THREE.MeshLambertMaterial({color:0x1e293b});
  var glass=new THREE.MeshLambertMaterial({color:0x7dd3fc}),white=new THREE.MeshLambertMaterial({color:0xf8fafc});
  function box(w,h,d,m,x,y,z){var b=new THREE.Mesh(new THREE.BoxGeometry(w,h,d),m);b.position.set(x,y,z);body.add(b);return b}
  box(1.9,.55,4.4,paint,0,.62,0);            // sasis
  box(1.7,.3,1.5,paint,0,.98,1.35);          // kap mesin
  box(1.55,.55,1.9,glass,0,1.2,-.35);        // kabin
  box(1.5,.1,1.5,paint,0,1.52,-.35);         // atap
  box(.34,.02,4.4,white,0,.91,0);            // garis balap
  box(1.9,.18,.35,dark,0,.4,2.15);           // bumper depan
  box(.1,.5,.1,dark,-.7,.95,-2.0);box(.1,.5,.1,dark,.7,.95,-2.0);   // tiang spoiler
  box(2.1,.09,.55,paint,0,1.25,-2.05);       // sayap belakang
  var hl=new THREE.MeshBasicMaterial({color:0xfef08a}),tl=new THREE.MeshBasicMaterial({color:0xef4444});
  box(.4,.18,.08,hl,-.6,.7,2.22);box(.4,.18,.08,hl,.6,.7,2.22);
  box(.4,.16,.08,tl,-.6,.75,-2.22);box(.4,.16,.08,tl,.6,.75,-2.22);
  var wg=new THREE.CylinderGeometry(.42,.42,.36,14),wm=new THREE.MeshLambertMaterial({color:0x111827});
  [[-1.0,1.45],[1.0,1.45],[-1.0,-1.45],[1.0,-1.45]].forEach(function(p){
    var piv=new THREE.Group();piv.position.set(p[0],.42,p[1]);
    var w=new THREE.Mesh(wg,wm);w.rotation.z=Math.PI/2;piv.add(w);
    var hub=new THREE.Mesh(new THREE.BoxGeometry(.38,.2,.1),white);hub.position.x=0;piv.add(hub); // penanda putaran roda
    g.add(piv);u.wheels.push(piv);
  });
  var sh=new THREE.Mesh(new THREE.PlaneGeometry(2.4,5),new THREE.MeshBasicMaterial({color:0x000000,transparent:true,opacity:.28,depthWrite:false}));
  sh.rotation.x=-Math.PI/2;sh.position.y=.04;g.add(sh);
  var ns=nameSprite(name,isMe);ns.position.y=2.7+(tier%3)*.8;g.add(ns);
  g.userData=u;return g;
}

function flash(kind){var e=$("cr-flash");e.className=kind;void e.offsetWidth;e.className=kind+" go"}
function disposeScene(){
  try{
    if(S.scene)S.scene.traverse(function(o){
      if(o.geometry)o.geometry.dispose();
      if(o.material){(Array.isArray(o.material)?o.material:[o.material]).forEach(function(m){if(m.map)m.map.dispose();m.dispose()})}
    });
  }catch(e){}
}

/* ---------- membangun dunia 3D ---------- */
function build3D(){
  var wrap=$("cr-canvas");
  if(!S.renderer){
    S.renderer=new THREE.WebGLRenderer({antialias:true});
    S.lowFx=(typeof AES_LOWEND!=="undefined"&&!!AES_LOWEND);S.renderer.setPixelRatio(aesGfxRaceDpr(1.75));
    wrap.appendChild(S.renderer.domElement);
    S.camera=new THREE.PerspectiveCamera(60,1,.4,1100);
  }else{disposeScene()}
  var tr=S.tr=getTrack(S.circ),scene=S.scene=new THREE.Scene();
  S.L=S.laps*tr.len;
  scene.background=new THREE.Color(0xa8d4f2);scene.fog=new THREE.Fog(0xcfe6f7,140,760);
  scene.add(new THREE.HemisphereLight(0xe3f1ff,0x5b7d52,.95));
  var sun=new THREE.DirectionalLight(0xfff0cc,.95);sun.position.set(-120,160,60);scene.add(sun);
  var M=function(c){return new THREE.MeshLambertMaterial({color:c})};
  var mid=new THREE.Vector3((tr.box.x0+tr.box.x1)/2,0,(tr.box.z0+tr.box.z1)/2);

  var ground=new THREE.Mesh(new THREE.PlaneGeometry(4200,4200),new THREE.MeshLambertMaterial({map:grassTex()}));
  ground.rotation.x=-Math.PI/2;ground.position.set(mid.x,-.06,mid.z);scene.add(ground);

  var vrep=tr.len/Math.max(1,Math.round(tr.len/20));
  var road=new THREE.Mesh(ribbon(tr,-ROADW/2,ROADW/2,.02,vrep),new THREE.MeshLambertMaterial({map:roadTex(),side:THREE.DoubleSide}));scene.add(road);
  var red=new THREE.Color(0xdc2626),wh=new THREE.Color(0xf8fafc),cm=new THREE.MeshLambertMaterial({vertexColors:true,side:THREE.DoubleSide});
  scene.add(new THREE.Mesh(ribbon(tr,-ROADW/2-CURB,-ROADW/2,.035,1,[red,wh]),cm));
  scene.add(new THREE.Mesh(ribbon(tr,ROADW/2,ROADW/2+CURB,.035,1,[wh,red]),cm));
  // bahu jalan aspal tipis di luar curb
  var shoulder=new THREE.MeshLambertMaterial({color:0x6b7280,side:THREE.DoubleSide});
  scene.add(new THREE.Mesh(ribbon(tr,-WALLOFF,-ROADW/2-CURB,.01,1),shoulder));
  scene.add(new THREE.Mesh(ribbon(tr,ROADW/2+CURB,WALLOFF,.01,1),shoulder));
  // dinding pembatas
  var wm=new THREE.MeshLambertMaterial({vertexColors:true,side:THREE.DoubleSide}),b1=new THREE.Color(0x2563eb),b2=new THREE.Color(0xf1f5f9);
  scene.add(new THREE.Mesh(wall(tr,-WALLOFF,1.1,[b1,b2]),wm));
  scene.add(new THREE.Mesh(wall(tr,WALLOFF,1.1,[b2,b1]),wm));

  // garis start/finish + gerbang
  var s0=posAt(tr,0,0),grp=new THREE.Group();grp.position.set(s0.x,0,s0.z);grp.rotation.y=s0.h;scene.add(grp);
  var chk=new THREE.Mesh(new THREE.PlaneGeometry(ROADW,1.6),new THREE.MeshBasicMaterial({map:checkerTex(),side:THREE.DoubleSide}));
  chk.rotation.x=-Math.PI/2;chk.position.y=.05;grp.add(chk);
  var postM=M(0x334155);
  [-1,1].forEach(function(sd){var p=new THREE.Mesh(new THREE.BoxGeometry(.6,8,.6),postM);p.position.set(sd*(WALLOFF+.6),4,0);grp.add(p)});
  var banner=new THREE.Mesh(new THREE.BoxGeometry((WALLOFF+.6)*2+.6,1.8,.5),new THREE.MeshBasicMaterial({map:textTex("🏁  START / FINISH  🏁",1024,128,{bg:"#0f172a",fg:"#fde047",font:"bold 66px sans-serif"})}));
  banner.position.set(0,8,0);grp.add(banner);
  // tribun penonton di sisi luar dekat garis start
  var tribune=new THREE.Group();tribune.position.set(WALLOFF+17,0,-6);grp.add(tribune);
  var tb=new THREE.Mesh(new THREE.BoxGeometry(9,5,60),M(0x94a3b8));tb.position.y=2.5;tribune.add(tb);
  var tc=new THREE.Mesh(new THREE.PlaneGeometry(60,5),new THREE.MeshBasicMaterial({map:crowdTex(),side:THREE.DoubleSide}));
  tc.rotation.y=-Math.PI/2;tc.position.set(-4.55,2.6,0);tribune.add(tc);

  // pohon & gunung
  var tm=[M(0x2f855a),M(0x38a169),M(0x276749)],trunkM=M(0x7c4a21),trunkG=new THREE.CylinderGeometry(.3,.42,2.4,6),coneG=new THREE.ConeGeometry(2.3,6,7);
  var want=S.lowFx?40:95,placed=0,tries=0,minD=WALLOFF+9;
  while(placed<want&&tries<900){
    tries++;
    var ii=Math.floor(Math.random()*tr.N),sd=Math.random()<.5?-1:1,off=WALLOFF+8+Math.random()*70;
    var q=tr.P[ii],tx=q[0]-tr.T[ii][1]*off*sd,tz=q[1]+tr.T[ii][0]*off*sd,ok=true;
    for(var kk=0;kk<tr.N;kk+=3){var dx=tr.P[kk][0]-tx,dz=tr.P[kk][1]-tz;if(dx*dx+dz*dz<minD*minD){ok=false;break}}
    if(!ok)continue;
    var tg=new THREE.Group();tg.position.set(tx,0,tz);
    var trk=new THREE.Mesh(trunkG,trunkM);trk.position.y=1.2;tg.add(trk);
    var cone=new THREE.Mesh(coneG,tm[placed%3]);cone.position.y=5;var sc=.8+Math.random()*.7;tg.scale.set(sc,sc,sc);tg.add(cone);
    scene.add(tg);placed++;
  }
  var mtM=new THREE.MeshLambertMaterial({color:0x8aa3c9,flatShading:true});
  for(var mI=0;mI<18;mI++){
    var an=mI/18*Math.PI*2+rnd(-.1,.1),rr=rnd(60,120),hh=rnd(70,160),dd=620+rnd(0,120);
    var mt=new THREE.Mesh(new THREE.ConeGeometry(rr,hh,5),mtM);
    mt.position.set(mid.x+Math.cos(an)*dd,hh/2-3,mid.z+Math.sin(an)*dd);mt.rotation.y=rnd(0,3);scene.add(mt);
  }
  S.pool=new Pool(scene,S.lowFx?70:150,softTex());

  // pembalap
  var lanes=shuffle(Array.apply(null,{length:NLANE}).map(function(_,i){return i})),latOf=function(i){return -ROADW/2+LANEW*(i+.5)};
  var lv=LEVELS[S.lvl]||LEVELS[1],names=otherNames();
  S.remote={};
  S.racers=[{isMe:true,name:myName(),color:myColor(),lat:(S.mode?latOfKey(myPid()):latOf(lanes[0]))}];
  if(!S.mode)for(var bI=0;bI<5;bI++)S.racers.push({isMe:false,name:names[bI],color:BOTCOL[bI],lat:latOf(lanes[bI+1]),acc:rnd(lv.acc[0],lv.acc[1]),think:rnd(lv.think[0],lv.think[1]),timer:rnd(2.5,5)});
  S.racers.forEach(function(r,i){
    r.dist=0;r.v=0;r.target=BASEV;r.finished=false;r.finishT=0;r.correct=0;r.wrong=0;r.idx=i;r.boost=0;
    r.slip=0;r.slide=0;r.roll=0;r.spin=0;r.lap=0;r.lapT=0;r.bestLap=0;r.dacc=0;r.sacc=0;
    r.hi=true; /* semua mobil siswa sama: terbuka + robot duduk */r.mesh=makeCar(r.color,r.name,r.isMe,i,r.hi);scene.add(r.mesh);placeCar(r,0);
  });
  S.me=S.racers[0];S.finishCount=0;
  var cp=posAt(tr,-14,S.me.lat*.6);S.camera.position.set(cp.x,3.8,cp.z);
  buildDots();buildMini();onResize();
}
function placeCar(r,dt){
  var tr=S.tr,k=curvAt(tr,r.dist),sgn=k>0?1:-1;
  if(r.latT!==undefined){var kk=Math.min(1,(dt||0)*3.2);r.lat+=(r.latT-r.lat)*kk;r.vb=(r.vb||0)+((r.vbT||0)-(r.vb||0))*kk} // pindah jalur / menyalip
  r.slide+=((r.slip>.05?r.slip:0)*1.5-r.slide)*Math.min(1,(dt||0)*6);
  var lat=clamp(r.lat-sgn*r.slide,-ROADW/2-.9,ROADW/2+.9),p=posAt(tr,r.dist-2-(r.vb||0),lat);
  var rollT=-clamp(k*r.v*r.v*.0042,-.11,.11);r.roll+=(rollT-r.roll)*Math.min(1,(dt||0)*8);
  r.mesh.position.set(p.x,0,p.z);
  var yaw=sgn*r.slip*.38;
  if(r.isMe&&S.stumble>0)yaw+=Math.sin(S.T*34)*.16*S.stumble;
  r.mesh.rotation.y=p.h+yaw;
  var u=r.mesh.userData;u.body.rotation.z=r.roll+(r.isMe&&S.stumble>0?Math.sin(S.T*38)*.07*S.stumble:0);
  u.body.rotation.x=-clamp((r.target-r.v)*.004,-.04,.05);
  r.x=p.x;r.z=p.z;r.h=p.h;
}
function latOfLane(c){return -ROADW/2+LANEW*(c+.5)}
/* penata jalur: mobil di belakang pindah ke jalur kosong untuk menyalip; di garis start dibuat barisan (grid) */
function planCars(){
  try{
    if(!S.scene||!window.aesLanePlan)return;
    var items=[],byK={};
    S.racers.forEach(function(r){
      if(!r.mesh||(r.remote&&!r.mesh.visible))return;
      var k=r.isMe?"me":String(r.pid||r.name);byK[k]=r;
      items.push({k:k,d:r.dist,p:(r.cell===undefined?-1:r.cell),h:hashStr(r.isMe?myPid():(r.pid||r.name))%NLANE,fix:!!r.isMe});
    });
    var pl=window.aesLanePlan(items,NLANE,1,8.5);
    Object.keys(pl).forEach(function(k){
      var r=byK[k],q=pl[k];if(!r)return;
      var first=r.cell===undefined;r.cell=q.c;r.latT=latOfLane(q.c);r.vbT=q.back;
      if(first){r.lat=r.latT;r.vb=q.back}
    });
  }catch(e){}
}
function buildDots(){
  var tb=$("cr-trackbar");Array.prototype.slice.call(tb.querySelectorAll(".cr-dot")).forEach(function(n){n.remove()});
  S.racers.forEach(function(r){var d=document.createElement("span");d.className="cr-dot"+(r.isMe?" me":"");d.style.background=r.color;d.style.left="0%";d.title=r.name;tb.appendChild(d);r.dot=d});
}
/* peta mini sirkuit: garis dasar digambar sekali, titik pembalap digambar ulang berkala */
function mmXY(p,w,h,pad){
  var b=S.tr.box,sc=Math.min((w-pad*2)/(b.x1-b.x0),(h-pad*2)/(b.z1-b.z0));
  return[(w-(b.x1-b.x0)*sc)/2+(p[0]-b.x0)*sc,(h-(b.z1-b.z0)*sc)/2+(p[1]-b.z0)*sc];
}
function buildMini(){
  var cv=$("cr-mm"),w=cv.width,h=cv.height,base=document.createElement("canvas");base.width=w;base.height=h;
  var x=base.getContext("2d"),tr=S.tr;
  x.lineJoin="round";x.lineCap="round";
  x.beginPath();tr.P.forEach(function(p,i){var q=mmXY(p,w,h,18);if(i)x.lineTo(q[0],q[1]);else x.moveTo(q[0],q[1])});x.closePath();
  x.strokeStyle="rgba(255,255,255,.28)";x.lineWidth=14;x.stroke();
  x.strokeStyle="#e2e8f0";x.lineWidth=5;x.stroke();
  var s=mmXY(tr.P[0],w,h,18);x.fillStyle="#fff";x.fillRect(s[0]-9,s[1]-3,18,6);
  S.mmBase=base;drawMini();
}
function drawMini(){
  var cv=$("cr-mm");if(!cv||!S.mmBase||!S.tr)return;
  var w=cv.width,h=cv.height,x=cv.getContext("2d");
  x.clearRect(0,0,w,h);x.drawImage(S.mmBase,0,0);
  S.racers.slice().reverse().forEach(function(r){
    var p=posAt(S.tr,r.dist,0),q=mmXY([p.x,p.z],w,h,18);
    x.beginPath();x.arc(q[0],q[1],r.isMe?11:7,0,6.3);x.fillStyle=r.color;x.fill();x.lineWidth=r.isMe?4:3;x.strokeStyle="#fff";x.stroke();
  });
}
function onResize(){
  if(!S.renderer)return;
  var w=window.innerWidth,h=window.innerHeight;
  S.renderer.setSize(w,h);S.camera.aspect=w/h;
  var land=h<=520&&w>h,ox=0,oy=0;
  if(S.state==="run"||S.state==="countdown"){ if(land)ox=w*.2; else oy=h*.13 }
  if(ox||oy)S.camera.setViewOffset(w,h,ox,oy,w,h);else S.camera.clearViewOffset();
  S.camera.updateProjectionMatrix();
}

/* ---------- soal ---------- */
function resetQueue(){var qs=getQs();S.qList=(window.AESQBag?window.AESQBag.order(qs):shuffle(qs.map(function(_,i){return i})));S.qPtr=0}
function nextQuestion(){
  var qs=getQs();if(!qs.length)return;
  if(S.qPtr>=S.qList.length){resetQueue();if(S.qList.length>1&&S.qList[0]===S.lastQ){var t=S.qList.shift();S.qList.push(t)}}
  var qi=S.qList[S.qPtr++],q=qs[qi];try{window.AESQBag&&window.AESQBag.mark(q)}catch(e){}S.lastQ=qi;S.cur={qi:qi,q:q};S.locked=false;
  var ord=optOrder(q);
  $("cr-qno").textContent="Soal #"+(S.me.correct+S.me.wrong+1)+" • benar "+S.me.correct+"/"+qNeed();
  var html=rich(q.q);
  if(q.image&&/^(https?:|data:image)/i.test(q.image))html+='<img id="cr-qimg" src="'+esc(q.image)+'">';
  $("cr-qtext").innerHTML=html;
  var box=$("cr-opts");box.innerHTML="";
  ord.forEach(function(oi,pos){
    var b=document.createElement("button");b.type="button";b.className="cr-opt";b.dataset.oi=oi;
    b.innerHTML="<b>"+String.fromCharCode(65+pos)+"</b><span>"+rich(q.options[oi])+"</span>";
    b.onclick=function(){pick(pos)};box.appendChild(b);
  });
  $("cr-fb").textContent="";
  typeset([$("cr-qtext"),box]);
  $("cr-qpanel").scrollTop=0;
}
function updateChips(){$("cr-cok").textContent="✓"+S.me.correct;$("cr-cbad").textContent="✗"+S.me.wrong;$("cr-cstreak").textContent="🔥"+S.streak}
function fx(text,cls){var e=$("cr-fx");e.textContent=text;e.className=cls;void e.offsetWidth;e.className=cls+" show"}
function pick(pos){
  if(S.locked||S.state!=="run"||!S.cur)return;
  var btns=$("cr-opts").children;if(pos<0||pos>=btns.length)return;
  S.locked=true;
  var chosen=Number(btns[pos].dataset.oi),right=Number(S.cur.q.correct),me=S.me,ok=chosen===right;
  if(ok){
    me.correct++;S.streak++;if(S.streak>S.bestStreak)S.bestStreak=S.streak;
    me.target=Math.min(MAXV,me.target+BOOST+Math.min(S.streak-1,5)*.8);me.v+=2.8;
    btns[pos].classList.add("cr-ok");sfx("correct_row");S.kick=1;flash("ok");me.boost=1;
    fx(S.streak>=3?"🔥 KOMBO x"+S.streak+"! NGEBUT!":"🚀 BENAR! MOBIL MAKIN KENCANG","ok");
    $("cr-fb").style.color="#4ade80";$("cr-fb").textContent="✅ Benar! Kecepatan naik.";
    updateChips();later(nextQuestion,450);
  }else{
    me.wrong++;S.streak=0;me.target=Math.max(MINV,me.target-SLOW);me.v*=.68;S.stumble=1;S.shake=1;S.roll=(Math.random()<.5?-1:1)*.1;flash("bad");
    btns[pos].classList.add("cr-bad");
    for(var i=0;i<btns.length;i++)if(Number(btns[i].dataset.oi)===right)btns[i].classList.add("cr-ok");
    sfx("wrong_answer");fx("🐢 SALAH! MELAMBAT","bad");
    $("cr-fb").style.color="#fb7185";$("cr-fb").textContent="❌ Salah. Jawaban yang benar ditandai hijau.";
    var at=Math.min(S.qList.length,S.qPtr+2+Math.floor(Math.random()*3));S.qList.splice(at,0,S.cur.qi);  // soal yang salah muncul lagi sebentar lagi
    updateChips();later(nextQuestion,1250);
  }
}

/* ---------- alur balapan ---------- */
function fmt(t){t=Math.max(0,t);var m=Math.floor(t/60),s=t-m*60;return(m<10?"0":"")+m+":"+(s<10?"0":"")+s.toFixed(1)}
function bestKey(){return"aes_car_best_"+S.circ+"_"+S.laps}
function getBest(){try{var v=parseFloat(localStorage.getItem(bestKey()));return isFinite(v)?v:null}catch(e){return null}}
function setBest(t){try{localStorage.setItem(bestKey(),String(t))}catch(e){}}
function showBest(){
  var b=getBest(),nm=(CIRCUITS[S.circ]||{}).name||"";
  $("cr-best").textContent=b?("🏆 Rekor pribadimu ("+nm+", "+S.laps+" putaran): "+fmt(b)):"Belum ada rekor untuk kombinasi ini — ayo catat yang pertama!";
}
function showStart(){
  S.state="idle";clearTimers();
  $("cr-start").classList.remove("cr-hide");$("cr-result").classList.add("cr-hide");$("cr-qpanel").classList.remove("show");$("cr-count").textContent="";
  var n=getQs().length;
  $("cr-who").innerHTML="Halo <b>"+esc(myName())+"</b>! "+(n?("Bank soal: <b>"+n+" soal</b> dari materi kelas."):'<span style="color:#fca5a5">Belum ada soal. Guru perlu mengisi soal di kolom Edit pada halaman awal.</span>');
  $("cr-go").disabled=!n;showBest();
}
function startRace(){
  if(!getQs().length)return;
  $("cr-start").classList.add("cr-hide");
  build3D();
  S.T=0;S.streak=0;S.bestStreak=0;S.maxV=0;S.stumble=0;S.resultShown=false;S.finishCount=0;S.shake=0;S.kick=0;S.roll=0;S.orbit=0;S.fwT=0;
  resetQueue();updateChips();
  S.state="countdown";S.cdStep=3;S.cd=0;
  $("cr-qpanel").classList.add("show");onResize();
  nextQuestion();S.locked=true;  // soal terlihat, tombol aktif saat GO
  $("cr-count").textContent="3";sfx("click");
}
function confetti(me){
  var p=S.pool;if(!p)return;
  var cols=[0xef4444,0xfacc15,0x38bdf8,0x4ade80,0xf472b6,0xffffff];
  for(var i=0;i<60;i++)p.emit(me.x+rnd(-3,3),rnd(3,6),me.z+rnd(-3,3),rnd(-6,6),rnd(5,12),rnd(-6,6),rnd(1.6,2.6),rnd(.5,.9),rnd(.4,.8),cols[i%cols.length],1,16);
}
function onFinishMe(){
  S.state="done";S.locked=true;sfx("finish_island");
  if(S.auto){NET.myFin[S.auto]=1;pubRun(topicRes(),{a:"fin",id:S.auto,pid:myPid(),name:myName(),t:Math.round(S.me.finishT*10)/10,ok:S.me.correct,bad:S.me.wrong,L:S.L});pubPos()}
  var t=S.me.finishT,best=getBest(),newRec=false;
  if(!best||t<best){setBest(t);newRec=true}
  fx(newRec?"🏆 REKOR BARU!":"🏁 FINISH!","ok");
  $("cr-qpanel").classList.remove("show");
  S.orbit=0;S.kick=1;confetti(S.me);later(function(){if(S.open)confetti(S.me)},1300);
  later(function(){showResult(newRec)},3600);
}
function ranking(){
  return S.racers.slice().sort(function(a,b){
    if(a.finished&&b.finished)return a.finishT-b.finishT;
    if(a.finished)return-1;if(b.finished)return 1;return b.dist-a.dist;
  });
}
function showResult(newRec){
  if(S.resultShown)return;S.resultShown=true;
  var rk=ranking(),pl=rk.indexOf(S.me)+1,me=S.me,tot=me.correct+me.wrong;
  var medal=pl===1?"🥇":pl===2?"🥈":pl===3?"🥉":"🏅";
  $("cr-rtitle").textContent=medal+(pl===1?" JUARA 1!":" POSISI KE-"+pl);
  $("cr-rsub").textContent=newRec?"🏆 Rekor pribadi baru di "+CIRCUITS[S.circ].name+" ("+S.laps+" putaran)!":CIRCUITS[S.circ].name+" • "+S.laps+" putaran • "+(S.auto?"melawan teman sekelas":"melawan komputer");
  $("cr-rstats").innerHTML=
    "<div><b>"+fmt(me.finishT)+"</b><span>WAKTU</span></div>"+
    "<div><b>"+(tot?Math.round(me.correct/tot*100):0)+"%</b><span>AKURASI</span></div>"+
    "<div><b>"+Math.round(S.maxV*3.6)+"</b><span>KM/JAM MAKS</span></div>"+
    "<div><b style='color:#4ade80'>"+me.correct+"</b><span>BENAR</span></div>"+
    "<div><b style='color:#fb7185'>"+me.wrong+"</b><span>SALAH</span></div>"+
    "<div><b style='color:#fdba74'>"+S.bestStreak+"</b><span>KOMBO TERBAIK</span></div>"+
    (me.bestLap?"<div style='grid-column:1/-1'><b style='font-size:14px'>⏱ "+fmt(me.bestLap)+"</b><span>PUTARAN TERCEPAT</span></div>":"");
  fillResultTable();
  $("cr-result").classList.remove("cr-hide");
}

function fillResultTable(){
  var rk=ranking();
  $("cr-rtable").innerHTML=rk.map(function(r,i){
    return '<div class="cr-row'+(r.isMe?" me":"")+'"><span class="pl">#'+(i+1)+'</span><span class="nm">'+esc(r.name)+(r.isMe?" (Kamu)":"")+'</span><span class="tm">'+(r.finished?fmt(r.finishT):Math.round(Math.min(r.dist,S.L)/S.L*100)+"%")+'</span></div>';
  }).join("");
}

/* ---------- pembaruan tiap frame ---------- */
function update(dt){
  var me=S.me;if(!me)return;
  if(S.auto&&S.scene){S.lpt=(S.lpt||0)-dt;if(S.lpt<=0){S.lpt=.2;planCars()}}
  var tr=S.tr,racing=S.state==="run"||S.state==="done",tnow=performance.now()/1000;
  if(S.state==="countdown"){
    S.cd+=dt;
    if(S.cd>=.9){
      S.cd=0;S.cdStep--;
      if(S.cdStep>0){$("cr-count").textContent=String(S.cdStep);sfx("click")}
      else{$("cr-count").textContent="GO!";sfx("finish_island");S.state="run";S.T=0;S.locked=false;S.kick=.8;onResize();later(function(){if(S.state!=="idle")$("cr-count").textContent=""},700)}
    }
  }
  if(racing){
    S.T+=dt;
    S.racers.forEach(function(r){
      if(r.remote){ // mobil teman sekelas: ikuti posisi yang dikirim lewat jaringan (dihaluskan)
        var ag=Math.min(1.6,(performance.now()-r.nat)/1000);
        var pd=r.nd+(r.fin>0?0:r.nv*ag);
        if(r.fin>0){r.finished=true;r.finishT=r.fin;pd=Math.max(pd,S.L)}
        r.dist+=(pd-r.dist)*Math.min(1,dt*5);
        if(r.dist>S.L+RUNOFF)r.dist=S.L+RUNOFF;
        r.v+=(r.nv-r.v)*Math.min(1,dt*5);if(r.v<0)r.v=0;
        r.spin+=r.v*dt/.42;
        return;
      }
      if(!r.isMe&&!r.finished){
        r.timer-=dt;
        if(r.timer<=0){
          r.timer=r.think*rnd(.8,1.25);
          if(Math.random()<r.acc){r.correct++;r.target=Math.min(MAXV,r.target+BOOST*rnd(.8,1.1));r.v+=1.6;r.boost=.8}
          else{r.wrong++;r.target=Math.max(MINV,r.target-SLOW*rnd(.8,1.1));r.v*=.75}
        }
      }
      if(r.finished)r.target=0;
      else{ // kelelahan / pemulihan perlahan menuju kecepatan dasar
        if(r.target>BASEV)r.target=Math.max(BASEV,r.target-.45*dt);
        else if(r.target<BASEV)r.target=Math.min(BASEV,r.target+.32*dt);
      }
      r.v+=(r.target-r.v)*Math.min(1,dt*(r.finished?1.3:2.4));
      if(r.v<0)r.v=0;
      // tikungan: batas kecepatan aman bergantung pada kelengkungan di depan mobil
      var kk=0;for(var la=0;la<=10;la+=5){var kv=Math.abs(curvAt(tr,r.dist+la));if(kv>kk)kk=kv}
      var vsafe=Math.sqrt(ALAT/Math.max(kk,1e-4));
      if(!r.finished&&r.v>vsafe){
        var over=r.v-vsafe;
        r.v-=over*Math.min(1,dt*1.8);
        r.slip=Math.min(1,r.slip+dt*(.8+over*.08));
      }else r.slip=Math.max(0,r.slip-dt*1.8);
      if(!r.finished){var _g=capQ(r)-r.dist;if(_g<1e9){var _vm=Math.max(0,_g)*1.6+CREEP;if(r.v>_vm)r.v=_vm}}
      r.dist=Math.min(r.dist+r.v*dt,S.L+RUNOFF);
      if(!r.finished&&r.correct<qNeed()){var _h=S.L*.98;if(r.dist>_h){r.dist=_h;r.v=0}}
      r.spin+=r.v*dt/.42;
      if(r.boost>0)r.boost-=dt;
      // catat putaran
      var lapNow=Math.min(S.laps,Math.floor(r.dist/tr.len)+1);
      if(r.lap===0){r.lap=1;r.lapT=S.T}
      else if(!r.finished&&lapNow>r.lap){
        var lt=S.T-r.lapT;if(!r.bestLap||lt<r.bestLap)r.bestLap=lt;
        r.lap=lapNow;r.lapT=S.T;
        if(r.isMe){fx("🏁 PUTARAN "+r.lap+" / "+S.laps,"ok");sfx("click")}
      }
      if(!r.finished&&r.dist>=S.L){
        var lt2=S.T-r.lapT;if(!r.bestLap||lt2<r.bestLap)r.bestLap=lt2;
        r.finished=true;r.finishT=S.T;S.finishCount++;
        if(r.isMe)onFinishMe();
      }
    });
    if(me.v>S.maxV)S.maxV=me.v;
    if(S.auto){
      S.pubT-=dt;if(S.pubT<=0){S.pubT=posEvery();pubPos()}
      S.mt-=dt;if(S.mt<=0){S.mt=.6;refreshMeshes()}
      if(S.state==="done"&&S.resultShown&&NET.finalShown!==S.auto){S.rt-=dt;if(S.rt<=0){S.rt=1.5;fillResultTable()}}
    }
    if(S.state==="done"&&S.orbit>=1&&S.racers.every(function(r){return r.finished}))showResult(false);
  }
  // posisi mobil, putaran roda, asap
  S.racers.forEach(function(r){
    if(!r.mesh||(r.remote&&!r.mesh.visible))return;
    placeCar(r,dt);
    var u=r.mesh.userData;
    for(var w=0;w<u.wheels.length;w++)u.wheels[w].rotation.x=r.spin;
    if(racing&&!r.finished||racing&&r.v>6){
      var back=posAt(tr,r.dist-4,r.lat);
      if(r.slip>.12){ // ban berasap saat tergelincir di tikungan
        r.sacc+=dt*(r.isMe?42:20)*r.slip*(S.lowFx?.5:1);
        while(r.sacc>1){r.sacc-=1;S.pool.emit(back.x+rnd(-.9,.9),.3,back.z+rnd(-.5,.5),rnd(-1.2,1.2),rnd(.4,1.4),rnd(-1.2,1.2),rnd(.7,1.2),.8,3.4,0xe5e7eb,.55,0)}
      }else if(r.v>20){ // debu tipis di belakang
        r.dacc+=dt*r.v*.35*(S.lowFx?.5:1);
        while(r.dacc>1){r.dacc-=1;S.pool.emit(back.x+rnd(-1,1),.2,back.z+rnd(-.4,.4),rnd(-.6,.6),rnd(.2,.7),rnd(-.6,.6),rnd(.45,.8),.5,1.6,0xcbd5e1,.22,0)}
      }
      if(r.boost>0&&r.v>12){ // percikan knalpot saat boost
        S.pool.emit(back.x+rnd(-.6,.6),.55,back.z+rnd(-.3,.3),rnd(-.6,.6),rnd(.2,.8),rnd(-.6,.6),.35,.7,.2,0xfbbf24,.9,0);
      }
    }
  });
  if(S.stumble>0)S.stumble=Math.max(0,S.stumble-dt*1.2);
  S.pool.update(dt);

  // kamera
  var cam=S.camera,p0=posAt(tr,me.dist-2,me.lat*.6),sp=me.v,port=cam.aspect<.95?Math.min(1,(.95-cam.aspect)/.5):0;
  var lx,ly,lz;
  if(S.state==="idle"){ // sebelum mulai: kamera berputar pelan mengitari area start
    var s0=posAt(tr,0,0),a=tnow*.25;
    var cx=s0.x+Math.sin(a)*21,cz=s0.z+Math.cos(a)*21;
    cam.position.x+=(cx-cam.position.x)*.1;cam.position.y+=(9-cam.position.y)*.1;cam.position.z+=(cz-cam.position.z)*.1;
    lx=s0.x;ly=1.5;lz=s0.z;
  }else if(S.state==="done"){
    S.orbit=Math.min(1,S.orbit+dt/2.4);
    var e=S.orbit*S.orbit*(3-2*S.orbit),th=Math.PI*e,kk2=1-Math.exp(-dt*9),pk=1+port*.7;
    var wx=me.x-p0.tx*Math.cos(th)*8*pk-p0.tz*Math.sin(th)*7*pk,wz=me.z-p0.tz*Math.cos(th)*8*pk+p0.tx*Math.sin(th)*7*pk;
    cam.position.x+=(wx-cam.position.x)*kk2;cam.position.y+=(2.6+Math.sin(th)*.9-cam.position.y)*kk2;cam.position.z+=(wz-cam.position.z)*kk2;
    lx=me.x;ly=1.2;lz=me.z;
  }else{
    var back=9+sp*.07+port*3.5,hgt=3.5+Math.min(1,sp/MAXV)*.9+port*1.1;
    var cp=posAt(tr,me.dist-2-back,me.lat*.5),kc=1-Math.exp(-dt*7);
    cam.position.x+=(cp.x-cam.position.x)*kc;cam.position.y+=(hgt-cam.position.y)*kc;cam.position.z+=(cp.z-cam.position.z)*kc;
    var la=posAt(tr,me.dist+13,me.lat*.4);lx=la.x;ly=1.3;lz=la.z;
  }
  S.shake=Math.max(0,S.shake-dt*2.4);S.kick=Math.max(0,S.kick-dt*2.2);S.roll*=Math.exp(-dt*4);
  cam.lookAt(lx+(Math.random()-.5)*S.shake*.9,ly+(Math.random()-.5)*S.shake*.6,lz+(Math.random()-.5)*S.shake*.9);
  var rl=S.roll+(S.shake>0?(Math.random()-.5)*S.shake*.04:0)+Math.sin(tnow*1.7)*.004*clamp(sp/MAXV,0,1);
  if(rl)cam.rotateZ(rl);
  var fovT=S.state==="done"?50:58+clamp(sp/MAXV,0,1)*16+S.kick*9,kf=1-Math.exp(-dt*10);
  if(cam.aspect<.95){var hn=2*Math.atan(Math.tan(33*Math.PI/180)/cam.aspect)*180/Math.PI;fovT=Math.min(92,Math.max(fovT,hn))}
  if(Math.abs(cam.fov-fovT)>.05){cam.fov+=(fovT-cam.fov)*kf;cam.updateProjectionMatrix()}
  hud(racing,dt);
}

var _hudT=0;
function hud(racing,dt){
  var me=S.me,tr=S.tr;
  $("cr-speedfx").style.opacity=String(clamp((me.v-26)/22,0,.9));
  var now=performance.now();if(now-_hudT<60)return;_hudT=now;
  $("cr-kmh").textContent=Math.round(me.v*3.6);
  $("cr-spdbar").style.width=clamp(me.v/MAXV*100,0,100)+"%";
  var rk=ranking(),pl=rk.indexOf(me)+1;
  $("cr-place").innerHTML="#"+pl+"<small>/"+S.racers.length+"</small>";
  $("cr-lap").innerHTML=Math.min(S.laps,Math.max(1,me.lap||1))+"<small>/"+S.laps+"</small>";
  $("cr-time").textContent=fmt(racing?(S.state==="done"&&me.finished?me.finishT:S.T):0);
  $("cr-dist").textContent=Math.round(Math.min(me.dist,S.L))+" / "+Math.round(S.L)+" m";
  S.racers.forEach(function(r){r.dot.style.left=clamp(r.dist/S.L,0,1)*100+"%"});
  drawMini();
  // penanda tikungan di depan
  var cn=$("cr-corner");
  if(!racing||S.state==="done"){cn.style.display="none";return}
  var best=0,bd=0,bk=0;
  for(var d=8;d<=130;d+=6){var kv=curvAt(tr,me.dist+d),a=Math.abs(kv);if(a>best){best=a;bd=d;bk=kv}}
  var R=best>1e-4?1/best:9999;
  if(me.slip>.2){cn.style.display="block";cn.className="slip";cn.textContent="💨 Tergelincir di tikungan! Kecepatan turun"}
  else if(R<95){
    var vs=Math.sqrt(ALAT*R),danger=me.v>vs*1.02;
    cn.style.display="block";cn.className=danger?"warn":"";
    cn.textContent=(bk>0?"↱ Tikungan kanan":"↰ Tikungan kiri")+" • "+Math.round(bd)+" m"+(R<45?" (tajam)":"")+(danger?" ⚠ kamu terlalu kencang":"");
  }else cn.style.display="none";
}

function frame(ts){
  if(!S.open)return;
  S.raf=requestAnimationFrame(frame);
  var dt=Math.min(.1,(ts-S.last)/1000||0);S.last=ts;
  try{update(dt);S.renderer.render(S.scene,S.camera)}catch(e){console.error("[BalapMobil]",e)}
}

/* ---------- buka / tutup ---------- */
function onKey(e){
  if(!S.open)return;
  e.stopPropagation();  // jangan sampai tombol A-D menggerakkan avatar di aplikasi utama
  var k=(e.key||"").toLowerCase(),map={a:0,b:1,c:2,d:3,"1":0,"2":1,"3":2,"4":3};
  if(k==="escape"){closeRun(true);return}
  if(k in map&&S.state==="run"){e.preventDefault();pick(map[k])}
}
function pauseMainRender(){
  try{
    if(typeof renderer!=="undefined"&&renderer&&renderer!==S.renderer&&!renderer.__crPatched){
      var orig=renderer.render;
      renderer.render=function(){if(S.open)return;return orig.apply(this,arguments)};
      renderer.__crPatched=true;
    }
  }catch(e){}
}
function openRunCore(mode){
  if(S.open)return;
  if(typeof THREE==="undefined"){alert("Three.js belum termuat. Cek koneksi internet lalu muat ulang halaman.");return}
  if(mode!=="auto")S.auto=null;
  S.mode=mode||null;
  S.pubN=0;S.pubT=0;S.rt=0;S.mt=0;
  S.open=true;pauseMainRender();$("cr-overlay").classList.add("cr-open");$("cr-launch").style.display="none";
  $("cr-tpanel").classList.add("cr-hide");$("cr-miss").classList.add("cr-hide");
  $("cr-again").style.display=mode?"none":"";
  S.state="idle";
  if(mode==="auto"){$("cr-result").classList.add("cr-hide");startRace()}
  else if(mode==="miss"||mode==="final"){
    $("cr-start").classList.add("cr-hide");$("cr-result").classList.add("cr-hide");$("cr-qpanel").classList.remove("show");$("cr-count").textContent="";
    build3D();
    if(mode==="miss")$("cr-miss").classList.remove("cr-hide");
  }else{build3D();showStart()}
  S.last=performance.now();S.raf=requestAnimationFrame(frame);
}
function openRun(){ // tombol BALAP MOBIL: guru -> panel guru (siswa tidak bisa memulai sendiri)
  if(S.open)return;
  if(isTeacherNow()){openTPanel();return}
  if(STUDENT_SOLO)openRunCore();
}
function closeRun(ask){
  if(!S.open)return;
  if(ask&&(S.state==="run"||S.state==="countdown")&&!confirm("Keluar dari balapan? Progres balapan ini tidak disimpan."))return;
  S.open=false;cancelAnimationFrame(S.raf);clearTimers();
  $("cr-overlay").classList.remove("cr-open");
  disposeScene();
  if(S.renderer){try{S.renderer.dispose();S.renderer.forceContextLoss&&S.renderer.forceContextLoss();S.renderer.domElement.remove()}catch(e){}S.renderer=null}
  S.scene=null;S.state="idle";S.auto=null;S.mode=null;S.remote={};
}

/* ---------- BALAPAN DIATUR GURU: perintah mulai, posisi antar siswa, hasil ---------- */
var NET={c:null,room:null,subs:{},handled:{},myFin:{},state:null,stLive:false,missT:null,finalShown:null,finalAt:null,run:null,pt:0,tCirc:"oval",tLaps:2};
function topicCmd(){return "aes_class_3d/"+roomId+"/car_cmd"}
function topicRes(){return "aes_class_3d/"+roomId+"/car_res"}
function topicState(){return "aes_class_3d/"+roomId+"/car_state"}
function topicPos(){return "aes_class_3d/"+roomId+"/car_pos"}
function isStudentNow(){try{return !isTeacherNow()&&!!myPlayer&&myPlayer.role==="student"&&!!myPlayer.hasJoinedGame&&!(typeof isTeacher3DMonitor!=="undefined"&&isTeacher3DMonitor)}catch(e){return false}}
function myPid(){try{return String(myPlayer.id||myName())}catch(e){return myName()}}
function nk(n){return String(n==null?"":n).trim().toLowerCase()}
function hashStr(t){var h=5381;t=String(t);for(var i=0;i<t.length;i++)h=((h<<5)+h+t.charCodeAt(i))|0;return Math.abs(h)}
function latOfKey(k){return -ROADW/2+LANEW*((hashStr(k)%NLANE)+.5)}   // lajur ditentukan dari ID siswa, jadi konsisten di semua layar
function pubRun(topic,obj,retain){
  try{var c=(typeof mqttClient!=="undefined")?mqttClient:null;if(c&&c.connected){c.publish(topic,JSON.stringify(obj),{qos:1,retain:!!retain});return true}}catch(e){}
  return false;
}
function note(msg){
  var n=document.createElement("div");n.textContent=msg;
  n.style.cssText="position:fixed;left:50%;top:14px;transform:translateX(-50%);z-index:9700;background:#0f172a;color:#fde047;border:1px solid rgba(255,255,255,.4);padding:8px 14px;border-radius:12px;font:800 13px 'Plus Jakarta Sans',sans-serif;max-width:90vw;text-align:center";
  document.body.appendChild(n);setTimeout(function(){n.remove()},3800);
}
function isSeen(id){try{return localStorage.getItem("aes_car_seen")===id}catch(e){return false}}
function setSeen(id){try{localStorage.setItem("aes_car_seen",id)}catch(e){}}
/* interval kirim posisi menyesuaikan jumlah siswa online, agar jaringan sekolah tidak kewalahan */
function posEvery(){
  var n=1;try{if(typeof aesOnlineN==="function")n=aesOnlineN()}catch(e){}
  return n<=12?.5:n<=30?.8:n<=60?1.2:1.8;
}
function onNetMsg(topic,payload,packet){
  if(topic.indexOf("/car_")<0)return;
  var d;try{d=JSON.parse(payload.toString())}catch(e){return}
  if(!d||typeof d!=="object")return;
  try{
    if(topic===topicCmd()){if(isStudentNow())onCmd(d)}
    else if(topic===topicState()){if(isStudentNow()){NET.state=d;NET.stLive=!(packet&&packet.retain);evalState()}}
    else if(topic===topicRes()){if(isTeacherNow())onRes(d)}
    else if(topic===topicPos()){onPos(d)}
  }catch(e){console.error("[BalapMobil net]",e)}
}
function bindNet(){
  try{
    var c=(typeof mqttClient!=="undefined")?mqttClient:null,rm=(typeof roomId!=="undefined")?roomId:null;
    if(!c||!rm||!c.connected)return;
    if(!c.__crL){c.__crL=true;c.on("message",onNetMsg)}
    if(NET.c!==c||NET.room!==rm){NET.c=c;NET.room=rm;NET.subs={}}
    var want=isTeacherNow()?[topicRes(),topicPos()]:(isStudentNow()?[topicCmd(),topicState(),topicPos()]:[]);
    want.forEach(function(t){if(!NET.subs[t]){NET.subs[t]=1;c.subscribe(t,{qos:1})}});
    if(isStudentNow())evalState();
  }catch(e){}
}
setInterval(bindNet,1200);

/* siswa: pastikan guru benar-benar menerima "ikut" dan "finish" kita; kirim ulang bila paket hilang */
function reconcile(){
  try{
    if(!S.open||!S.auto||!S.me||!isStudentNow())return;
    var st=NET.state;
    if(!st||st.id!==S.auto||!Array.isArray(st.rows))return;
    var me=nk(myName()),row=null;
    st.rows.forEach(function(r){if(nk(r.n)===me)row=r});
    if(S.state==="done"&&(!row||row.s!=="fin")){
      pubRun(topicRes(),{a:"fin",id:S.auto,pid:myPid(),name:myName(),t:Math.round(S.me.finishT*10)/10,ok:S.me.correct,bad:S.me.wrong,L:S.L});
    }else if(!row){
      pubRun(topicRes(),{a:"join",id:S.auto,pid:myPid(),name:myName()});
    }
  }catch(e){}
}
setInterval(reconcile,4000);

/* penanda koneksi terputus + kirim posisi segera setelah tersambung kembali */
var _netWasOk=true;
function netBadge(){
  var el=$("cr-net");
  if(!el){
    el=document.createElement("div");el.id="cr-net";
    el.style.cssText="display:none;position:absolute;left:50%;top:118px;transform:translateX(-50%);z-index:7;max-width:92vw;text-align:center;background:#b45309;color:#fff;border:1px solid #fde68a;border-radius:12px;padding:6px 12px;font:800 12px 'Plus Jakarta Sans',sans-serif;pointer-events:none";
    $("cr-overlay").appendChild(el);
  }
  var c=(typeof mqttClient!=="undefined")?mqttClient:null,ok=!!(c&&c.connected);
  var show=S.open&&!ok&&!!S.auto;
  el.style.display=show?"block":"none";
  if(show)el.textContent="⚠ Koneksi terputus, menyambung ulang… balapan tetap berjalan dan hasilmu dikirim otomatis saat tersambung.";
  if(ok&&!_netWasOk){S.pubT=0;NET.subs={}}
  _netWasOk=ok;
}
setInterval(netBadge,1000);

/* siswa: kirim posisi mobilku ke teman sekelas & guru */
function pubPos(){
  try{
    var c=(typeof mqttClient!=="undefined")?mqttClient:null,me=S.me;
    if(!c||!c.connected||!me||!S.auto)return;
    c.publish(topicPos(),JSON.stringify({id:S.auto,pid:myPid(),name:myName(),col:myColor(),d:Math.round(me.dist*10)/10,v:Math.round(me.v*10)/10,f:me.finished?Math.round(me.finishT*10)/10:0}),{qos:0,retain:false});
  }catch(e){}
}
function addRemote(m){
  if(!S.scene||!S.tr)return null;
  var key=String(m.pid);
  var col=/^#[0-9a-fA-F]{6}$/.test(String(m.col||""))?m.col:BOTCOL[Object.keys(S.remote).length%BOTCOL.length];
  var r={isMe:false,remote:true,pid:key,name:String(m.name||"?").slice(0,24),color:col,lat:latOfKey(key),
    dist:0,v:0,target:BASEV,finished:false,finishT:0,correct:0,wrong:0,idx:S.racers.length,boost:0,slip:0,slide:0,roll:0,spin:0,lap:0,lapT:0,bestLap:0,dacc:0,sacc:0,
    nd:0,nv:0,nat:performance.now(),fin:0,mesh:null,dot:null};
  S.remote[key]=r;S.racers.push(r);buildDots();
  return r;
}
/* gambar 3D hanya untuk 12 lawan terdekat (supaya Chromebook tetap lancar); sisanya tetap dihitung di peringkat */
var MAXMESH=(typeof AES_LOWEND!=="undefined"&&AES_LOWEND)?10:16;
function refreshMeshes(){
  if(!S.scene||!S.me)return;
  try{MAXMESH=aesGfxMaxMesh()}catch(e){}
  var arr=S.racers.filter(function(r){return r.remote});
  arr.sort(function(a,b){return Math.abs(a.dist-S.me.dist)-Math.abs(b.dist-S.me.dist)});
  /* mobil kota (detail penuh) hanya untuk 4 lawan terdekat agar HP tetap lancar; sisanya model sederhana */
  var HI=99; /* semua lawan pakai mobil kota yang sama (terbuka + robot) */
  arr.forEach(function(r,i){
    var want=i<MAXMESH,hi=r.hi?(i<HI+3):(i<HI);
    if(r.mesh&&((!want&&i>=MAXMESH+8)||(want&&!!r.hi!==hi)))dropCarMesh(r);
    if(want&&!r.mesh){
      try{r.hi=hi;r.mesh=makeCar(r.color,r.name,false,hashStr(r.pid)%6,hi);S.scene.add(r.mesh);placeCar(r,0)}catch(e){r.mesh=null;return}
    }
    if(r.mesh)r.mesh.visible=want;
  });
}
function onPos(d){
  if(isTeacherNow()){ // guru: papan pantauan langsung
    var rn=NET.run;if(!rn||d.id!==rn.id)return;
    var nm=String(d.name||"?").slice(0,40),k=nk(nm);if(!k)return;
    rn.joined[k]=nm;rn.live[k]={name:nm,d:Number(d.d)||0,v:Number(d.v)||0,f:Number(d.f)||0,at:Date.now()};
    renderTSoft();return;
  }
  if(!S.open||!S.scene||!S.me||!S.auto||d.id!==S.auto)return;
  var key=String(d.pid);if(!key||key===myPid())return;
  var r=S.remote[key]||addRemote(d);if(!r)return;
  var nd0=Number(d.d)||0;
  if(nd0<r.nd-0.05&&!(Number(d.f)>0))return; // paket lama yang datang terlambat: abaikan
  r.nd=Math.max(r.nd,nd0);r.nv=clamp(Number(d.v)||0,0,MAXV+3);r.nat=performance.now();
  if(Number(d.f)>0)r.fin=Number(d.f);
}

/* siswa: perintah mulai dari guru */
function onCmd(d){
  if(d.a!=="start")return;
  if(!d.id||NET.handled[d.id])return;NET.handled[d.id]=1;
  if(S.open&&S.mode==="miss")closeRun(false);   // sempat dikira tertinggal, ternyata perintah baru sampai
  if(S.open)return;
  try{if(window.AESRun&&window.AESRun._state&&window.AESRun._state.open)window.AESRun.close()}catch(e){}
  if(!getQs().length){pubRun(topicRes(),{a:"noq",id:d.id,pid:myPid(),name:myName()});note("Belum ada soal, balapan mobil belum bisa dimulai.");return}
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  S.auto=d.id;S.circ=CIRCUITS[d.c]?d.c:"oval";
  var lp=Number(d.p);S.laps=(lp>=1&&lp<=3)?Math.round(lp):2;
  openRunCore("auto");
  pubRun(topicRes(),{a:"join",id:d.id,pid:myPid(),name:myName()});
}

/* siswa: status balapan dari guru (tersimpan di server, jadi terbaca juga saat buka aplikasi belakangan) */
function evalState(){
  var d=NET.state;if(!d||!d.id||!isStudentNow())return;
  var age=Date.now()-(Number(d.at)||0);
  if(d.st==="running"){
    if(age>10800000||NET.handled[d.id]||NET.missT===d.id)return;
    NET.missT=d.id;
    setTimeout(function(){ // beri waktu perintah mulai langsung tiba; kalau tidak, siswa ini tertinggal
      var c=NET.state;
      if(!c||c.id!==d.id||c.st!=="running"||NET.handled[d.id]||S.open||!isStudentNow())return;
      // status diterima langsung (bukan tersimpan di server) tetapi perintah mulai tidak sampai = paket hilang: tetap ikut
      if(NET.stLive){onCmd({a:"start",id:c.id,c:c.c,p:c.p});return}
      openMissed(c);
    },2500);
  }else if(d.st==="ended"){
    if(age>43200000)return;
    if(NET.finalShown===d.id&&S.open){if(NET.finalAt!==d.at)showFinalBoard(d);return}
    if(isSeen(d.id))return;
    if(S.open&&S.auto===d.id){
      if(S.state==="done"){if(S.resultShown)showFinalBoard(d);return}   // sudah finis: ganti ke papan hasil akhir
      if(!S.me)return;
      pubRun(topicRes(),{a:"dnf",id:d.id,pid:myPid(),name:myName(),ok:S.me.correct,bad:S.me.wrong});
      NET.myFin[d.id]=0;closeRun(false);openFinal(d);return;
    }
    if(NET.myFin[d.id])return;
    if(S.open&&S.mode==="miss"){showFinalBoard(d);return}
    if(S.open)return;
    openFinal(d);
  }
}
function applyCfg(d){
  S.circ=CIRCUITS[d.c]?d.c:"oval";
  var lp=Number(d.p);S.laps=(lp>=1&&lp<=3)?Math.round(lp):2;
}
function openMissed(d){
  if(S.open)return;
  applyCfg(d);
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  openRunCore("miss");
}
function openFinal(d){
  if(S.open)return;
  applyCfg(d);
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  openRunCore("final");showFinalBoard(d);
}
function showFinalBoard(d){
  setSeen(d.id);NET.finalShown=d.id;NET.finalAt=d.at;
  $("cr-miss").classList.add("cr-hide");$("cr-start").classList.add("cr-hide");
  var me=nk(myName()),rows=Array.isArray(d.rows)?d.rows:[];
  var fin=rows.filter(function(r){return r.s==="fin"}).sort(function(a,b){return a.t-b.t});
  var part=rows.filter(function(r){return r.s==="dnf"||r.s==="run"});
  var miss=rows.filter(function(r){return r.s==="miss"});
  var mine=null,rank=0;
  fin.forEach(function(r,i){if(nk(r.n)===me){mine=r;rank=i+1}});
  if(!mine)part.forEach(function(r){if(nk(r.n)===me)mine=r});
  var ok=mine?(Number(mine.ok)||0):0,bad=mine?(Number(mine.bad)||0):0,tot=ok+bad,ac=tot?Math.round(ok/tot*100):0;
  var st=mine?(mine.s==="fin"?"Selesai":"Belum selesai"):"Tidak ikut";
  var medal=rank===1?"🥇":rank===2?"🥈":rank===3?"🥉":"🏁";
  var cn=(CIRCUITS[d.c]||CIRCUITS.oval).name;
  $("cr-rtitle").textContent=rank?(medal+(rank===1?" JUARA 1!":" POSISI KE-"+rank)):"🏁 BALAPAN SUDAH SELESAI";
  $("cr-rsub").textContent=cn+" • "+(Number(d.p)||2)+" putaran • balapan sudah diakhiri guru"+(mine?"":" • kamu tidak ikut, skormu 0");
  $("cr-rstats").innerHTML=
    "<div><b>"+(mine&&mine.s==="fin"?fmt(mine.t):"-")+"</b><span>WAKTU</span></div>"+
    "<div><b>"+ac+"%</b><span>AKURASI</span></div>"+
    "<div><b>"+(rank?("#"+rank+"/"+fin.length):"-")+"</b><span>POSISI</span></div>"+
    "<div><b style='color:#4ade80'>"+ok+"</b><span>BENAR</span></div>"+
    "<div><b style='color:#fb7185'>"+bad+"</b><span>SALAH</span></div>"+
    "<div><b style='color:#fdba74;font-size:12px'>"+st+"</b><span>STATUS</span></div>";
  function row(pl,r,tm){return '<div class="cr-row'+(nk(r.n)===me?" me":"")+'"><span class="pl">'+pl+'</span><span class="nm">'+esc(r.n)+(nk(r.n)===me?" (Kamu)":"")+'</span><span class="tm">'+tm+'</span></div>'}
  $("cr-rtable").innerHTML=
    fin.map(function(r,i){return row("#"+(i+1),r,fmt(r.t)+" • ✓"+(r.ok||0)+" ✗"+(r.bad||0))}).join("")+
    part.map(function(r){return row("…",r,"belum selesai")}).join("")+
    miss.map(function(r){return row("–",r,"tidak ikut")}).join("");
  $("cr-result").classList.remove("cr-hide");
}

/* guru: panel, status balapan & papan pantauan */
function openTPanel(){renderT();$("cr-tpanel").classList.remove("cr-hide");$("cr-launch").style.display="none"}
function onRes(d){
  var r=NET.run;if(!r||!d||d.id!==r.id)return;
  var nm=String(d.name||"?").slice(0,40),key=nk(nm);if(!key)return;
  if(d.a==="join"){r.joined[key]=nm}
  else if(d.a==="fin"){r.joined[key]=nm;r.fin[key]={name:nm,t:Number(d.t)||0,ok:Number(d.ok)||0,bad:Number(d.bad)||0};delete r.dnf[key]}
  else if(d.a==="dnf"){r.joined[key]=nm;if(!r.fin[key])r.dnf[key]={name:nm,ok:Number(d.ok)||0,bad:Number(d.bad)||0}}
  else if(d.a==="noq"){r.noq[key]=nm}
  renderT();pubState(false);
}
function buildRows(){
  var r=NET.run,rows=[],seen={};
  Object.keys(r.fin).forEach(function(k){var x=r.fin[k];rows.push({n:x.name,s:"fin",t:x.t,ok:x.ok,bad:x.bad});seen[k]=1});
  Object.keys(r.dnf).forEach(function(k){if(seen[k])return;var x=r.dnf[k];rows.push({n:x.name,s:"dnf",ok:x.ok,bad:x.bad});seen[k]=1});
  Object.keys(r.joined).forEach(function(k){if(seen[k])return;rows.push({n:r.joined[k],s:"run",ok:0,bad:0});seen[k]=1});
  if(r.status==="ended"){
    try{(gameConfig.students||[]).forEach(function(n){n=String(n||"").trim();if(n&&!seen[nk(n)]){rows.push({n:n.slice(0,40),s:"miss"});seen[nk(n)]=1}})}catch(e){}
  }
  return rows;
}
function pubState(now){
  clearTimeout(NET.pt);
  var go=function(){var r=NET.run;if(!r)return;pubRun(topicState(),{id:r.id,c:r.circ,p:r.laps,st:r.status,at:Date.now(),rows:buildRows()},true)};
  if(now)go();else NET.pt=setTimeout(go,400);
}
var _tT=0;
function renderTSoft(){var n=performance.now();if(n-_tT<600)return;_tT=n;renderT()}
function renderT(){
  var st=$("cr-t-stat"),tb=$("cr-t-table");if(!st||!tb)return;
  var r=NET.run;
  if(!r){st.textContent="Belum ada balapan yang dimulai.";tb.innerHTML="";return}
  var nj=Object.keys(r.joined).length,nf=Object.keys(r.fin).length,nq=Object.keys(r.noq).length;
  st.textContent=(r.status==="ended"?"🏁 BALAPAN DIAKHIRI • ":"🏎️ BALAPAN BERJALAN • ")+((CIRCUITS[r.circ]||{}).name||"")+" • "+r.laps+" putaran • ikut: "+nj+" • selesai: "+nf+(nq?" • tanpa soal: "+nq:"");
  var now=Date.now(),items=[];
  Object.keys(r.joined).forEach(function(k){
    var f=r.fin[k],lv=r.live[k],dn=r.dnf[k];
    items.push({n:r.joined[k],t:f?f.t:(lv&&lv.f>0?lv.f:0),ok:f?f.ok:(dn?dn.ok:0),bad:f?f.bad:(dn?dn.bad:0),d:lv?lv.d:0,at:lv?lv.at:0,dnf:!!dn&&!f});
  });
  items.sort(function(a,b){if(a.t>0&&b.t>0)return a.t-b.t;if(a.t>0)return-1;if(b.t>0)return 1;return b.d-a.d});
  var html=items.map(function(x,i){
    var pct=x.t>0?100:clamp(Math.round(x.d/Math.max(1,r.L)*100),0,100);
    var lost=!x.t&&!x.dnf&&r.status!=="ended"&&x.at&&(now-x.at)>6000;
    var tm=x.t>0?(fmt(x.t)+" • ✓"+x.ok+" ✗"+x.bad):(x.dnf?"belum selesai":(pct+"%"+(lost?" ⚠":"")));
    return '<div class="cr-row"><span class="pl">#'+(i+1)+'</span><span class="nm">'+esc(x.n)+'<div class="cr-bar2"><i style="width:'+pct+'%"></i></div></span><span class="tm">'+tm+'</span></div>';
  }).join("");
  html+=buildRows().filter(function(x){return x.s==="miss"}).map(function(x){
    return '<div class="cr-row"><span class="pl">–</span><span class="nm">'+esc(x.n)+'</span><span class="tm">tidak ikut</span></div>';
  }).join("");
  tb.innerHTML=html;
}
setInterval(function(){try{var tp=$("cr-tpanel");if(isTeacherNow()&&tp&&!tp.classList.contains("cr-hide"))renderT()}catch(e){}},1500);

function segHandler(id,cb){
  $(id).addEventListener("click",function(e){
    var b=e.target.closest("button");if(!b)return;
    Array.prototype.forEach.call($(id).children,function(x){x.classList.remove("on")});b.classList.add("on");cb(b.dataset.v);
  });
}
segHandler("cr-seg-circ",function(v){S.circ=v;if(S.open&&S.state==="idle"){build3D();showBest()}});
segHandler("cr-seg-laps",function(v){S.laps=Number(v)||1;if(S.open&&S.state==="idle"){build3D();showBest()}});
segHandler("cr-seg-lvl",function(v){S.lvl=Number(v)||0});
window.addEventListener("keydown",onKey,true);
window.addEventListener("resize",onResize);
$("cr-exit").onclick=function(){closeRun(true)};
$("cr-close1").onclick=function(){closeRun(false)};
$("cr-close2").onclick=function(){closeRun(false)};
$("cr-go").onclick=startRace;
$("cr-again").onclick=function(){$("cr-result").classList.add("cr-hide");build3D();showStart()};

/* ---------- tombol & pilihan panel guru ---------- */
segHandler("cr-t-seg-circ",function(v){NET.tCirc=(v==="berliku")?"berliku":"oval"});
segHandler("cr-t-seg-laps",function(v){NET.tLaps=Math.max(1,Math.min(3,Number(v)||2))});
$("cr-t-go").onclick=function(){
  if(!isTeacherNow())return;
  if(!getQs().length){note("Belum ada soal. Isi soal dulu di kolom Edit pada halaman awal.");return}
  var id="c"+Date.now().toString(36)+Math.floor(Math.random()*1000);
  var prev=NET.run,circ=NET.tCirc,laps=NET.tLaps;
  NET.run={id:id,circ:circ,laps:laps,L:getTrack(circ).len*laps,status:"running",joined:{},fin:{},dnf:{},noq:{},live:{}};
  bindNet();
  if(!pubRun(topicState(),{id:id,c:circ,p:laps,st:"running",at:Date.now(),rows:[]},true)){NET.run=prev;renderT();note("Belum tersambung ke server kelas. Coba lagi sebentar lagi.");return}
  pubRun(topicCmd(),{a:"start",id:id,c:circ,p:laps});
  renderT();note("📣 Balap mobil dimulai di layar siswa!");
};
$("cr-t-stop").onclick=function(){
  if(!isTeacherNow())return;
  var r=NET.run;if(!r||r.status==="ended"){note("Belum ada balapan yang berjalan.");return}
  if(!confirm("Akhiri balapan dan umumkan skor ke semua siswa? Siswa yang masih membalap akan dihentikan."))return;
  r.status="ended";renderT();pubState(true);note("🏁 Balapan diakhiri. Skor ditampilkan ke siswa.");
};
$("cr-t-docx").onclick=function(){
  var r=NET.run;if(!r){alert("Belum ada balapan yang dimulai.");return}
  var items=[];
  Object.keys(r.joined).forEach(function(k){
    var f=r.fin[k],lv=r.live[k],dn=r.dnf[k];
    items.push({n:r.joined[k],t:f?f.t:(lv&&lv.f>0?lv.f:0),ok:f?f.ok:(dn?dn.ok:null),bad:f?f.bad:(dn?dn.bad:null),d:lv?lv.d:0});
  });
  items.sort(function(a,b){if(a.t>0&&b.t>0)return a.t-b.t;if(a.t>0)return-1;if(b.t>0)return 1;return b.d-a.d});
  var list=items.map(function(x){
    var done=x.t>0,pct=done?100:clamp(Math.round(x.d/Math.max(1,r.L)*100),0,100);
    return{n:x.n,st:done?"Selesai":"Belum selesai",time:done?fmt(x.t):"-",ok:x.ok,bad:x.bad,prog:pct+"%"};
  });
  buildRows().filter(function(x){return x.s==="miss"}).forEach(function(x){list.push({n:x.n,st:"Tidak ikut",time:"-",ok:null,bad:null,prog:"-"})});
  window.aesRaceDocx({title:"Nilai Balap Mobil AES CLASS",fname:"Nilai_Balap_Mobil_"+window.aesRaceStamp()+".docx",
    info:["Sirkuit: "+((CIRCUITS[r.circ]||{}).name||"-")+" • "+r.laps+" putaran","Target soal: "+(r.laps<=1?8:r.laps===2?12:16)+" jawaban benar untuk finis","Status: "+(r.status==="ended"?"balapan sudah diakhiri":"balapan masih berjalan")+" • ikut: "+Object.keys(r.joined).length+" • selesai: "+Object.keys(r.fin).length],
    rows:list});
};
$("cr-t-self").onclick=function(){if(isTeacherNow())openRunCore()};
$("cr-t-close").onclick=function(){$("cr-tpanel").classList.add("cr-hide")};
$("cr-close3").onclick=function(){closeRun(false)};

window.AESCar={open:openRun,close:function(){closeRun(false)},_state:S,_track:getTrack};
})();

</script>
<!-- ===== /BALAP MOBIL ===== -->


<!-- ===== AES CLASS • TAMBAHAN: BALAP PESAWAT (3D, jarak lurus, jawab A/B/C/D, guru klik MULAI untuk semua siswa) ===== -->
<style id="pl-style">

#pl-launch{position:fixed;right:.6rem;top:66%;z-index:9400;display:none;align-items:center;gap:6px;padding:9px 13px;border-radius:9999px;background:linear-gradient(135deg,#38bdf8,#f59e0b);color:#fff;font:800 12px 'Plus Jakarta Sans',sans-serif;border:2px solid #fff;box-shadow:0 4px 18px rgba(245,158,11,.55);cursor:pointer;touch-action:manipulation}
#pl-launch:hover{filter:brightness(1.1)}
#pl-overlay{position:fixed;inset:0;z-index:9600;background:#0f172a;display:none;font-family:'Plus Jakarta Sans',"Noto Sans","Segoe UI","Noto Sans Arabic","Noto Sans Hebrew","Noto Sans JP","Hiragino Sans","Yu Gothic","Noto Sans KR","Malgun Gothic","Noto Sans SC","Microsoft YaHei","PingFang SC","Noto Sans TC","Noto Sans Devanagari","Nirmala UI","Noto Sans Thai","Arial Unicode MS",sans-serif;color:#f1f5f9;touch-action:manipulation;overflow:hidden}
#pl-overlay.pl-open{display:block}
#pl-canvas{position:absolute;inset:0}
#pl-canvas canvas{display:block;width:100%;height:100%}
#pl-net{display:none}
#pl-speedfx{position:absolute;inset:0;pointer-events:none;opacity:0;transition:opacity .25s;background:radial-gradient(ellipse at 50% 45%,rgba(255,255,255,0) 45%,rgba(255,255,255,.28) 100%)}
#pl-hud{position:absolute;top:8px;left:8px;right:8px;display:flex;flex-wrap:wrap;gap:8px;align-items:flex-start;pointer-events:none;z-index:3}
.pl-card{background:rgba(15,23,42,.82);border:1px solid rgba(255,255,255,.28);border-radius:14px;padding:6px 12px;pointer-events:none}
#pl-exit{pointer-events:auto;width:38px;height:38px;border-radius:12px;background:rgba(15,23,42,.85);color:#fecaca;border:1px solid rgba(255,255,255,.35);font-size:16px;font-weight:800;cursor:pointer}
.pl-lbl{font-size:9px;font-weight:800;letter-spacing:.08em;color:#7dd3fc}
#pl-kmh{font-size:26px;font-weight:800;line-height:1;color:#fde047;font-variant-numeric:tabular-nums}
.pl-unit{font-size:10px;color:#cbd5e1;margin-left:3px}
.pl-bar{height:6px;border-radius:9px;background:rgba(255,255,255,.18);margin-top:4px;overflow:hidden;min-width:96px}
#pl-spdbar{display:block;height:100%;width:0;background:linear-gradient(90deg,#22c55e,#facc15,#ef4444);border-radius:9px}
.pl-spacer{flex:1 1 0}
#pl-place{font-size:26px;font-weight:800;line-height:1;color:#fff}
#pl-place small{font-size:12px;color:#94a3b8}
#pl-time{font-size:12px;font-weight:700;color:#bae6fd;font-variant-numeric:tabular-nums;text-align:right}
.pl-track{order:3;flex:1 1 100%;pointer-events:none}
#pl-trackbar{position:relative;height:16px;border-radius:9px;background:rgba(15,23,42,.78);border:1px solid rgba(255,255,255,.3);margin:2px 8px 0 4px}
#pl-trackbar .pl-dot{position:absolute;top:50%;width:11px;height:11px;border-radius:50%;transform:translate(-50%,-50%);border:2px solid #fff;transition:left .15s linear}
#pl-trackbar .pl-dot.me{width:16px;height:16px;z-index:5;box-shadow:0 0 10px #fff}
#pl-trackbar .pl-flag{position:absolute;right:-6px;top:-4px;font-size:15px}
#pl-dist{font-size:10px;font-weight:700;color:#e2e8f0;text-align:center;margin-top:2px;text-shadow:0 1px 3px #000}
#pl-fx{position:absolute;left:0;right:0;top:34%;text-align:center;pointer-events:none;z-index:4;font-size:clamp(22px,6vw,44px);font-weight:800;text-shadow:0 3px 14px rgba(0,0,0,.7);opacity:0}
#pl-fx.show{animation:plpop .9s ease-out}
#pl-fx.ok{color:#4ade80}#pl-fx.bad{color:#fb7185}
#pl-flash{position:absolute;inset:0;pointer-events:none;z-index:2;opacity:0}
#pl-flash.ok.go{animation:plflash .5s ease-out;box-shadow:inset 0 0 130px 40px rgba(74,222,128,.6)}
#pl-flash.bad.go{animation:plflash .6s ease-out;box-shadow:inset 0 0 140px 50px rgba(244,63,94,.7)}
@keyframes plflash{0%{opacity:1}100%{opacity:0}}
@keyframes plpop{0%{opacity:0;transform:scale(.6) translateY(14px)}20%{opacity:1;transform:scale(1.15)}100%{opacity:0;transform:scale(1) translateY(-30px)}}
#pl-count{position:absolute;left:0;right:0;top:26%;text-align:center;font-size:clamp(60px,18vw,150px);font-weight:800;color:#fff;text-shadow:0 6px 30px rgba(0,0,0,.7);pointer-events:none;z-index:4}
#pl-qpanel{position:absolute;left:0;right:0;bottom:0;max-height:47vh;overflow-y:auto;padding:10px 12px calc(10px + env(safe-area-inset-bottom,0px));background:linear-gradient(to top,rgba(15,23,42,.97),rgba(15,23,42,.9));border-top:1px solid rgba(125,211,252,.5);z-index:3;touch-action:pan-y;display:none}
#pl-qpanel.show{display:block}
.pl-qhead{display:flex;align-items:center;justify-content:space-between;gap:8px;font-size:11px;font-weight:800;margin-bottom:5px}
.pl-chip{padding:2px 8px;border-radius:9999px;background:rgba(255,255,255,.12)}
.pl-chip.ok{color:#4ade80}.pl-chip.bad{color:#fb7185}.pl-chip.fire{color:#fdba74}
#pl-qtext{font-size:clamp(12px,2.6vw,17px);font-weight:700;line-height:1.35;margin-bottom:8px;overflow-wrap:anywhere}
#pl-qtext img,#pl-qimg{max-height:110px;border-radius:10px;margin:4px auto;display:block}
#pl-opts{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.pl-opt{display:flex;align-items:center;gap:8px;text-align:left;padding:8px 10px;min-height:48px;border-radius:12px;background:rgba(30,41,59,.95);border:2px solid rgba(255,255,255,.22);color:#fff;font:700 clamp(11px,2.3vw,15px) 'Plus Jakarta Sans',sans-serif;cursor:pointer;overflow-wrap:anywhere;touch-action:manipulation;transition:transform .08s}
.pl-opt:active{transform:scale(.97)}
.pl-opt b{flex:0 0 auto;width:28px;height:28px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:14px;color:#0f172a}
.pl-opt:nth-child(1) b{background:#38bdf8}.pl-opt:nth-child(2) b{background:#4ade80}.pl-opt:nth-child(3) b{background:#fbbf24}.pl-opt:nth-child(4) b{background:#fb7185}
.pl-opt.pl-ok{background:#15803d;border-color:#4ade80}
.pl-opt.pl-bad{background:#9f1239;border-color:#fb7185}
.pl-opt[disabled]{cursor:default}
#pl-fb{font-size:11px;font-weight:800;min-height:15px;margin-top:6px}
.pl-modal{position:absolute;inset:0;z-index:6;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.62);overflow-y:auto}
.pl-modal.pl-hide{display:none}
#pl-tpanel{position:fixed;inset:0;z-index:9600;display:flex;align-items:center;justify-content:center;padding:14px;background:rgba(2,6,23,.72);overflow-y:auto}
#pl-tpanel.pl-hide{display:none}
#pl-t-stat{font-size:12px;font-weight:800;color:#fde047;text-align:center;margin:8px 0}
#pl-t-table{max-height:34vh;overflow-y:auto;margin-bottom:8px}
.pl-bar2{height:5px;border-radius:9px;background:rgba(255,255,255,.14);overflow:hidden;margin-top:3px}
.pl-bar2 i{display:block;height:100%;background:linear-gradient(90deg,#38bdf8,#4ade80);width:0}
#pl-result{background:rgba(2,6,23,.3)}
.pl-box{width:min(94vw,470px);max-height:94vh;overflow-y:auto;background:#0f172a;border:2px solid rgba(125,211,252,.55);border-radius:20px;padding:18px 18px 16px;box-shadow:0 18px 60px rgba(0,0,0,.6)}
.pl-box h2{margin:0 0 4px;font-size:21px;font-weight:800;color:#fde047;text-align:center}
.pl-box p{margin:0 0 10px;font-size:12px;color:#cbd5e1;text-align:center;line-height:1.45}
.pl-rules{font-size:12px;color:#e2e8f0;line-height:1.5;background:rgba(255,255,255,.06);border-radius:12px;padding:8px 12px;margin-bottom:10px}
.pl-sel{margin-bottom:10px}
.pl-sel .pl-lbl{margin-bottom:4px}
.pl-seg{display:flex;gap:6px}
.pl-seg button{flex:1;padding:8px 4px;border-radius:10px;background:rgba(255,255,255,.08);border:2px solid transparent;color:#e2e8f0;font:800 11px 'Plus Jakarta Sans',sans-serif;cursor:pointer}
.pl-seg button.on{background:rgba(250,204,21,.18);border-color:#facc15;color:#fde047}
.pl-btn{width:100%;padding:12px;border-radius:14px;border:0;background:linear-gradient(135deg,#22c55e,#16a34a);color:#fff;font:800 15px 'Plus Jakarta Sans',sans-serif;cursor:pointer;margin-top:4px}
.pl-btn.alt{background:rgba(255,255,255,.1);font-size:12px;padding:9px}
.pl-btn:disabled{opacity:.5}
.pl-row{display:flex;align-items:center;gap:8px;padding:7px 10px;border-radius:10px;background:rgba(255,255,255,.06);margin-bottom:5px;font-size:12px;font-weight:700}
.pl-row.me{background:rgba(250,204,21,.2);border:1px solid #facc15}
.pl-row .pl{width:26px;font-weight:800;color:#fde047}
.pl-row .nm{flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.pl-row .tm{color:#bae6fd;font-variant-numeric:tabular-nums}
.pl-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:6px;margin:8px 0 10px}
.pl-stats div{background:rgba(255,255,255,.07);border-radius:10px;padding:6px 4px;text-align:center}
.pl-stats b{display:block;font-size:17px;color:#fff}
.pl-stats span{font-size:9px;color:#94a3b8;font-weight:700}
@media (orientation:portrait){
 #pl-hud{gap:6px}
 .pl-card{padding:5px 9px}
 #pl-kmh,#pl-place{font-size:22px}
 .pl-bar{min-width:78px}
 #pl-qpanel{max-height:52vh}
 #pl-qtext{font-size:clamp(14px,4vw,18px)}
 .pl-opt{font:700 clamp(13px,3.7vw,16px) 'Plus Jakarta Sans',sans-serif;min-height:52px}
 #pl-fx{top:30%}
 #pl-count{top:22%}
 .pl-box{max-height:92vh}
}
@media (max-height:520px) and (orientation:landscape){
 #pl-qpanel{left:auto;right:8px;bottom:8px;top:104px;width:min(54vw,540px);max-height:none;border-radius:14px;border:1px solid rgba(125,211,252,.5)}
 #pl-kmh,#pl-place{font-size:19px}
 .pl-card{padding:4px 9px}
}

@media (max-height:520px) and (orientation:landscape){
}
.pl-opt img{max-height:90px;max-width:100%;object-fit:contain;margin:2px 0;border-radius:8px}
.pl-opt .my-3{margin:2px 0}
.pl-opt a{pointer-events:none;color:inherit;text-decoration:none}
.pl-opt .aes-video,.pl-opt video{display:none}
#pl-qtext,.pl-opt span{unicode-bidi:plaintext}

</style>

<button id="pl-launch" type="button" onclick="AESPlane.open()">✈️ BALAP PESAWAT</button>

<div id="pl-overlay"><div id="pl-season"></div>
 <div id="pl-canvas"></div>
 <div id="pl-speedfx"></div>
 <div id="pl-flash"></div>
 <div id="pl-hud">
  <button id="pl-exit" type="button" title="Keluar">✕</button>
  <div class="pl-card"><div class="pl-lbl">KECEPATAN</div><div><span id="pl-kmh">0</span><span class="pl-unit">km/jam</span></div><div class="pl-bar"><i id="pl-spdbar"></i></div></div>
  <div class="pl-spacer"></div>
  <div class="pl-card"><div class="pl-lbl" style="text-align:center">SISA JARAK</div><div id="pl-left" style="font-size:20px;font-weight:800;line-height:1;color:#fff;text-align:center">0<small style="font-size:11px;color:#94a3b8"> m</small></div></div>
  <div class="pl-card"><div class="pl-lbl" style="text-align:right">POSISI</div><div id="pl-place">#1<small>/6</small></div><div id="pl-time">00:00.0</div></div>
  <div class="pl-track"><div id="pl-trackbar"><span class="pl-flag">🏁</span></div><div id="pl-dist">0 / 0 m</div></div>
 </div>
 <div id="pl-fx"></div>
 <div id="pl-count"></div>
 <div id="pl-qpanel">
  <div class="pl-qhead"><span id="pl-qno">Soal 1</span><span><span class="pl-chip ok" id="pl-cok">✓0</span> <span class="pl-chip bad" id="pl-cbad">✗0</span> <span class="pl-chip fire" id="pl-cstreak">🔥0</span></span></div>
  <div id="pl-qtext"></div>
  <div id="pl-opts"></div>
  <div id="pl-fb"></div>
 </div>

 <div id="pl-start" class="pl-modal">
  <div class="pl-box">
   <h2>✈️ BALAP PESAWAT AES CLASS</h2>
   <p id="pl-who">Siap terbang, pilot?</p>
   <div class="pl-rules">
    • Pesawatmu <b>terbang otomatis</b> menuju garis finish; tugasmu menjawab soal.<br>
    • Pilih jawaban <b>A / B / C / D</b> (bisa juga tekan tombol keyboard A-D atau 1-4).<br>
    • Jawaban <b style="color:#4ade80">benar</b> = pesawat makin <b>ngebut</b> 🚀. Jawaban <b style="color:#fb7185">salah</b> = <b>melambat</b> 🐢.<br>
    • Terbang melewati gerbang-gerbang berwarna dan jadilah yang <b>pertama menembus garis finish</b>!
   </div>
   <div class="pl-sel"><div class="pl-lbl">JARAK TERBANG</div><div class="pl-seg" id="pl-seg-course"><button data-v="s">Pendek</button><button data-v="m" class="on">Sedang</button><button data-v="l">Panjang</button></div></div>
   <div class="pl-sel"><div class="pl-lbl">LAWAN KOMPUTER</div><div class="pl-seg" id="pl-seg-lvl"><button data-v="0">Santai</button><button data-v="1" class="on">Sedang</button><button data-v="2">Ngebut</button></div></div>
   <div id="pl-best" style="font-size:11px;color:#94a3b8;text-align:center;margin-bottom:6px"></div>
   <button class="pl-btn" id="pl-go" type="button">▶ MULAI TERBANG</button>
   <button class="pl-btn alt" id="pl-close1" type="button">Tutup</button>
  </div>
 </div>

 <div id="pl-result" class="pl-modal pl-hide">
  <div class="pl-box">
   <h2 id="pl-rtitle">🏁 FINISH!</h2>
   <p id="pl-rsub"></p>
   <div class="pl-stats" id="pl-rstats"></div>
   <div id="pl-rtable"></div>
   <button class="pl-btn" id="pl-again" type="button">🔄 Main Lagi</button>
   <button class="pl-btn alt" id="pl-close2" type="button">Tutup</button>
  </div>
 </div>

 <div id="pl-miss" class="pl-modal pl-hide">
  <div class="pl-box">
   <h2>🏁 BALAPAN SUDAH DIMULAI</h2>
   <p id="pl-miss-t">Guru sudah memulai balap pesawat, tetapi kamu belum ikut. Pesawatmu masih di landasan. Tunggu guru mengakhiri balapan — skormu akan muncul di sini.</p>
   <button class="pl-btn alt" id="pl-close3" type="button">Tutup</button>
  </div>
 </div>
</div>

<div id="pl-tpanel" class="pl-hide">
 <div class="pl-box">
  <h2>✈️ BALAP PESAWAT • PANEL GURU</h2>
  <p>Tekan <b>MULAI</b>: balap pesawat langsung berjalan di layar semua siswa yang sudah masuk. Semua siswa terbang di jalur yang sama dan saling berlomba.</p>
  <div class="pl-sel"><div class="pl-lbl">JARAK TERBANG</div><div class="pl-seg" id="pl-t-seg-course"><button data-v="s">Pendek (±1 mnt)</button><button data-v="m" class="on">Sedang (±1,5 mnt)</button><button data-v="l">Panjang (±2,5 mnt)</button></div></div>
  <button class="pl-btn" id="pl-t-go" type="button">📣 MULAI BALAPAN SEMUA SISWA</button>
  <button class="pl-btn" id="pl-t-watch" type="button" style="background:linear-gradient(135deg,#38bdf8,#0ea5e9)">👁️ TONTON BALAPAN LANGSUNG (3D)</button>
  <button class="pl-btn alt" id="pl-t-stop" type="button">🏁 Akhiri balapan &amp; umumkan skor</button>
  <div id="pl-t-stat">Belum ada balapan yang dimulai.</div>
  <div id="pl-t-table"></div>
  <button class="pl-btn alt" id="pl-t-docx" type="button">📄 Unduh nilai lomba (Word)</button>
  <button class="pl-btn alt" id="pl-t-self" type="button">✈️ Coba sendiri (latihan melawan komputer)</button>
  <button class="pl-btn alt" id="pl-t-close" type="button">Tutup</button>
 </div>
</div>

<script id="pl-script">
(function(){
"use strict";
if(window.AESPlane)return;

/* ---------- helper aman (memakai fungsi bawaan aplikasi bila ada) ---------- */
var $=function(id){return document.getElementById(id)};
function esc(s){return String(s==null?"":s).replace(/[&<>"]/g,function(c){return{"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]})}
function rich(s){try{if(typeof formatRichEducationalText==="function")return formatRichEducationalText(s,1)}catch(e){}return esc(s)}
function typeset(a){try{if(typeof triggerMathJaxRender==="function")triggerMathJaxRender(a)}catch(e){}}
function sfx(n){try{if(typeof playSoundEffect==="function")playSoundEffect(n)}catch(e){}}
function clamp(v,a,b){return v<a?a:v>b?b:v}
function rnd(a,b){return a+Math.random()*(b-a)}
function shuffle(a){for(var i=a.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1)),t=a[i];a[i]=a[j];a[j]=t}return a}

function getQs(){
  try{
    var qs=(typeof gameConfig!=="undefined"&&gameConfig&&gameConfig.questions)||[];
    return qs.filter(function(q){return q&&q.q&&Array.isArray(q.options)&&q.options.filter(function(o){return String(o||"").trim()}).length>=2});
  }catch(e){return[]}
}
function optOrder(q){
  try{if(typeof getShuffledOrder==="function")return getShuffledOrder(q.options)}catch(e){}
  var idx=[];q.options.forEach(function(o,i){if(String(o||"").trim())idx.push(i)});return shuffle(idx);
}
function myName(){try{return(myPlayer&&myPlayer.name)||(typeof isTeacherMode!=="undefined"&&isTeacherMode?"Guru":"Kamu")}catch(e){return"Kamu"}}
function myColor(){try{return(myPlayer&&myPlayer.color)||"#ef4444"}catch(e){return"#ef4444"}}
function otherNames(){
  var pool=[];
  try{(gameConfig.students||[]).forEach(function(n){n=String(n||"").trim();if(n&&n!==myName())pool.push(n)})}catch(e){}
  shuffle(pool);
  var fb=shuffle(["Rani","Dimas","Putri","Fajar","Salsa","Rizky","Nadia","Bagas"]);
  while(pool.length<5)pool.push(fb.pop()||("Lawan "+pool.length));
  return pool.slice(0,5);
}
function hashStr(t){var h=5381;t=String(t);for(var i=0;i<t.length;i++)h=((h<<5)+h+t.charCodeAt(i))|0;return Math.abs(h)}
function nk(n){return String(n==null?"":n).trim().toLowerCase()}

/* ---------- konstanta permainan ---------- */
var STUDENT_SOLO=false;   // true = siswa juga boleh berlatih sendiri melawan komputer (default: hanya guru, seperti Balap Mobil)
var NLANE=8,LANEW=9,SPAN=NLANE*LANEW,GATEGAP=150,RUNOFF=140,SEAY=-42;
var BASEV=20,MINV=8,MAXV=62,BOOST=6.5,SLOW=8.5;
var LEVELS=[{acc:[.35,.6],think:[5,8]},{acc:[.55,.8],think:[4,6.5]},{acc:[.75,.95],think:[3,5]}];
var BOTCOL=["#ef4444","#f59e0b","#22c55e","#a855f7","#ec4899","#14b8a6"];
var COURSES={s:{name:"Pendek",L:1500},m:{name:"Sedang",L:2500},l:{name:"Panjang",L:4000}};
/* TARGET SOAL: jarak yang boleh ditempuh = jumlah jawaban benar / target soal x panjang rute */
function qNeed(){return S.course==="s"?8:S.course==="l"?16:12}
var CREEP=BASEV*.18; /* kecepatan merayap saat belum menjawab: tetap bergerak, tapi pelan */
function capQ(r){var n=qNeed();return r.correct>=n?Infinity:S.L*r.correct/n}
function cKey(k){return COURSES[k]?k:"m"}
function latOfKey(k){return -SPAN/2+LANEW*((hashStr(k)%NLANE)+.5)}            // lajur ditentukan dari ID siswa, jadi sama di semua layar
function altOfKey(k){return((Math.floor(hashStr(k)/8)%5)-2)*2.4}               // ketinggian sedikit berbeda agar pesawat tidak menumpuk

/* ---------- state ---------- */
var S={open:false,state:"idle",course:"m",lvl:1,L:2500,raf:0,last:0,T:0,cd:0,cdStep:0,timers:[],
  renderer:null,scene:null,camera:null,racers:[],me:null,finishCount:0,G:null,M:null,
  qList:[],qPtr:0,cur:null,locked:true,streak:0,bestStreak:0,maxV:0,resultShown:false,lastQ:-1,
  shake:0,kick:0,orbit:0,sea:null,clouds:[],isles:[],gates:[],gmats:[],fin:null,
  mode:null,auto:null,remote:{},pubT:0,rt:0,mt:0,dt4:0,shiftX:0,shiftY:0};
function later(fn,ms){var id=setTimeout(function(){fn()},ms);S.timers.push(id);return id}
function clearTimers(){S.timers.forEach(clearTimeout);S.timers=[]}

/* ---------- tombol peluncur ---------- */
function isTeacherNow(){try{return typeof isTeacherMode!=="undefined"&&!!isTeacherMode}catch(e){return false}}
function canShowLauncher(){
  if(S.open)return false;
  try{var tp=$("pl-tpanel");if(tp&&!tp.classList.contains("pl-hide"))return false}catch(e){}
  try{if(window.AESRun&&window.AESRun._state&&window.AESRun._state.open)return false}catch(e){}
  try{if(window.AESCar&&window.AESCar._state&&window.AESCar._state.open)return false}catch(e){}
  var hud=$("game-hud"),ts=$("teacher-screen");
  var hudOn=hud&&!hud.classList.contains("hidden"),tsOn=ts&&!ts.classList.contains("hidden");
  try{
    if(isTeacherNow())return !!(hudOn||tsOn);
    if(STUDENT_SOLO)return !!(hudOn&&myPlayer&&myPlayer.hasJoinedGame);
    return false;
  }catch(e){return false}
}
setInterval(function(){var b=$("pl-launch");if(b)b.style.display=canShowLauncher()?"flex":"none"},500);

/* ---------- 3D: tekstur & model ---------- */
function canvasTex(w,h,fn){var c=document.createElement("canvas");c.width=w;c.height=h;fn(c.getContext("2d"),w,h);var t=new THREE.CanvasTexture(c);return t}
function nameSprite(name,isMe){
  var c=document.createElement("canvas");c.width=320;c.height=72;var x=c.getContext("2d");
  x.fillStyle=isMe?"rgba(250,204,21,.95)":"rgba(15,23,42,.82)";
  var r=30;x.beginPath();x.moveTo(r,4);x.lineTo(320-r,4);x.quadraticCurveTo(316,4,316,r);x.lineTo(316,72-r);x.quadraticCurveTo(316,68,320-r,68);x.lineTo(r,68);x.quadraticCurveTo(4,68,4,72-r);x.lineTo(4,r);x.quadraticCurveTo(4,4,r,4);x.fill();
  x.fillStyle=isMe?"#0f172a":"#fff";x.font="bold 34px sans-serif";x.textAlign="center";x.textBaseline="middle";
  var t=String(name);if(t.length>14)t=t.slice(0,13)+"…";x.fillText(t,160,38);
  var tex=new THREE.CanvasTexture(c);var sp=new THREE.Sprite(new THREE.SpriteMaterial({map:tex,transparent:true,depthWrite:false,fog:false}));
  sp.scale.set(4.6,1.04,1);return sp;
}
function lam(c,o){return new THREE.MeshLambertMaterial(Object.assign({color:c},o||{}))}
/* geometri & bahan dipakai bersama oleh semua pesawat dalam satu adegan (hemat memori di Chromebook) */
function shared(){
  if(S.G)return;
  var G={},M={};
  G.body=new THREE.LatheGeometry([[.001,-2.6],[.14,-2.5],[.4,-1.4],[.62,-.2],[.6,.8],[.46,1.5],[.3,2],[.001,2.15]].map(function(a){return new THREE.Vector2(a[0],a[1])}),16);
  G.ring=new THREE.CylinderGeometry(.625,.615,.25,16,1,true);
  var ws=new THREE.Shape();[[-4.6,.15],[-4.6,-.45],[-.5,-.55],[.5,-.55],[4.6,-.45],[4.6,.15],[.5,.75],[-.5,.75]].forEach(function(p,i){i?ws.lineTo(p[0],p[1]):ws.moveTo(p[0],p[1])});
  G.wing=new THREE.ExtrudeGeometry(ws,{depth:.12,bevelEnabled:false});G.wing.rotateX(-Math.PI/2);
  G.tip=new THREE.BoxGeometry(.6,.16,.62);G.strut=new THREE.BoxGeometry(.08,.7,.08);
  G.wheel=new THREE.CylinderGeometry(.28,.28,.16,10);
  var fs=new THREE.Shape();[[-2.6,0],[-1.5,0],[-2.05,1.2],[-2.55,1.2]].forEach(function(p,i){i?fs.lineTo(p[0],p[1]):fs.moveTo(p[0],p[1])});
  G.fin=new THREE.ExtrudeGeometry(fs,{depth:.1,bevelEnabled:false});G.fin.translate(0,0,-.05);G.fin.rotateY(Math.PI/2);
  G.can=new THREE.SphereGeometry(.42,12,9);G.head=new THREE.SphereGeometry(.17,8,6);
  G.cap=new THREE.SphereGeometry(.185,8,4,0,Math.PI*2,0,Math.PI/2);
  G.blade=new THREE.BoxGeometry(.2,1.8,.05);G.disc=new THREE.CircleGeometry(.95,20);G.spin=new THREE.ConeGeometry(.2,.5,10);
  M.wing=lam(0xffc828);M.white=lam(0xffffff,{side:2});M.dark=lam(0x555f78);M.tire=lam(0x222a3d);
  M.can=lam(0x9fdcff,{transparent:true,opacity:.8});M.skin=lam(0xf2c9a0);M.cap=lam(0x2a4f8f);M.blade=lam(0x2f3752);
  M.disc=new THREE.MeshBasicMaterial({color:0xffffff,transparent:true,opacity:.2,side:2,depthWrite:false});M.spin=lam(0xffd23c);
  S.G=G;S.M=M;
}
function makePlane(col,name,isMe){
  shared();var G=S.G,M=S.M,paint=lam(col),P=new THREE.Group(),m;
  m=new THREE.Mesh(G.body,paint);m.rotation.x=-Math.PI/2;P.add(m);
  m=new THREE.Mesh(G.ring,M.white);m.rotation.x=Math.PI/2;m.position.z=-.2;P.add(m);
  m=new THREE.Mesh(G.wing,M.wing);m.position.set(0,-.15,-.2);P.add(m);
  m=new THREE.Mesh(G.wing,M.wing);m.scale.set(.38,1,.38);m.position.set(0,.05,2);P.add(m);
  [-1,1].forEach(function(s){
    m=new THREE.Mesh(G.tip,paint);m.position.set(s*4.35,-.09,-.05);P.add(m);
    m=new THREE.Mesh(G.strut,M.dark);m.position.set(s*1.2,-.5,-.5);P.add(m);
    m=new THREE.Mesh(G.wheel,M.tire);m.rotation.z=Math.PI/2;m.position.set(s*1.2,-.88,-.5);P.add(m);
  });
  m=new THREE.Mesh(G.fin,paint);m.position.y=.45;P.add(m);
  m=new THREE.Mesh(G.can,M.can);m.scale.set(1,.85,1.9);m.position.set(0,.5,-.1);P.add(m);
  m=new THREE.Mesh(G.head,M.skin);m.position.set(0,.56,-.05);P.add(m);
  m=new THREE.Mesh(G.cap,M.cap);m.position.set(0,.6,-.05);P.add(m);
  var prop=new THREE.Group();prop.position.z=-2.3;P.add(prop);
  for(var k=0;k<3;k++){var b=new THREE.Mesh(G.blade,M.blade),h=new THREE.Group();h.add(b);h.rotation.z=k*2.094;prop.add(h)}
  prop.add(new THREE.Mesh(G.disc,M.disc));
  m=new THREE.Mesh(G.spin,M.spin);m.rotation.x=-Math.PI/2;m.position.z=-.22;prop.add(m);
  var root=new THREE.Group();P.scale.setScalar(.8);root.add(P);
  var sp=nameSprite(name,isMe);sp.position.set(0,3.4,0);root.add(sp);
  root.userData={prop:prop,body:P,paint:paint};
  return root;
}
function seaTex(){
  var t=canvasTex(256,256,function(x,w,h){
    x.fillStyle="#2f89c9";x.fillRect(0,0,w,h);
    for(var i=0;i<90;i++){x.strokeStyle=i%2?"rgba(255,255,255,"+(.25+Math.random()*.35).toFixed(2)+")":"rgba(10,60,110,"+(.1+Math.random()*.18).toFixed(2)+")";x.lineWidth=1+Math.random()*2;var a=Math.random()*w,b=Math.random()*h,l=8+Math.random()*22;x.beginPath();x.moveTo(a,b);x.quadraticCurveTo(a+l/2,b-3,a+l,b);x.stroke()}
  });
  t.wrapS=t.wrapT=THREE.RepeatWrapping;t.repeat.set(1600/30,1600/30);t.anisotropy=2;return t;
}
function checkerTex(){
  return canvasTex(256,32,function(x,w,h){var n=16,s=w/n;for(var i=0;i<n;i++)for(var j=0;j<2;j++){x.fillStyle=((i+j)%2)?"#111827":"#ffffff";x.fillRect(i*s,j*16,s,16)}});
}
function labelSprite(text,w,h,fs){
  var c=document.createElement("canvas");c.width=w;c.height=h;var x=c.getContext("2d");
  x.font="900 "+fs+"px sans-serif";x.textAlign="center";x.textBaseline="middle";x.lineJoin="round";x.lineWidth=12;x.strokeStyle="rgba(10,30,90,.85)";x.fillStyle="#fff";
  x.strokeText(text,w/2,h/2);x.fillText(text,w/2,h/2);
  var sp=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(c),transparent:true,depthWrite:false}));return sp;
}
var GCOL=[0xff4d6d,0x3d8bff,0xffc21a,0x2fd07a];
/* ---------- MUSIM: berganti tiap jawaban benar, hanya di layar pemain sendiri (tidak dikirim ke jaringan) ---------- */
var SEASONS=[
 {n:"Musim Panas",i:"☀️",sky:0x8fd0ff,fog:0xcfeaff,hs:0xdff0ff,hg:0x3a8fc0,sun:0xfff2d0,si:.85,hi:.95,sea:0xffffff,hill:0x3fbf6f,sand:0xf3dc9a,pc:0,pn:0},
 {n:"Musim Gugur",i:"🍂",sky:0xf2a65a,fog:0xffd6a0,hs:0xffe2bf,hg:0x8a4a22,sun:0xffc27a,si:.9,hi:.9,sea:0xffd2a0,hill:0xd9822b,sand:0xe8c48a,pc:0xff8a2b,pn:1},
 {n:"Musim Dingin",i:"❄️",sky:0xb7cde6,fog:0xe3edf7,hs:0xeef5ff,hg:0x7a90ad,sun:0xe6f0ff,si:.7,hi:1,sea:0xdbeaf7,hill:0xf4f9ff,sand:0xe9f1f8,pc:0xffffff,pn:2},
 {n:"Musim Semi",i:"🌸",sky:0xa9dcff,fog:0xe6f4ff,hs:0xfff0f6,hg:0x58b878,sun:0xfff4e0,si:.9,hi:.95,sea:0xd8f6ff,hill:0x7ed957,sand:0xf6e2b0,pc:0xffb7d5,pn:3}
];
function seasonSet(t,instant){
  var m=S.season;if(!m)return;var c=m.cur;
  m.from={};m.to={};
  ["sky","fog","hs","hg","sun","sea","hill","sand"].forEach(function(n){m.from[n]=c[n].clone();m.to[n]=new THREE.Color(t[n])});
  m.from.si=c.si;m.from.hi=c.hi;m.to.si=t.si;m.to.hi=t.hi;
  m.k=instant?1:0;m.name=t;
  if(instant)seasonApply(0);
}
function seasonApply(dt){
  var m=S.season,sc=S.scene;if(!m||!sc||!m.to)return;
  if(m.k<1)m.k=Math.min(1,m.k+dt/1.6);
  var e=m.k*m.k*(3-2*m.k),c=m.cur,f=m.from,t=m.to;
  ["sky","fog","hs","hg","sun","sea","hill","sand"].forEach(function(n){c[n].copy(f[n]).lerp(t[n],e)});
  c.si=f.si+(t.si-f.si)*e;c.hi=f.hi+(t.hi-f.hi)*e;
  if(sc.background&&sc.background.copy)sc.background.copy(c.sky);
  if(sc.fog)sc.fog.color.copy(c.fog);
  if(S.hemi){S.hemi.color.copy(c.hs);S.hemi.groundColor.copy(c.hg);S.hemi.intensity=c.hi}
  if(S.sun){S.sun.color.copy(c.sun);S.sun.intensity=c.si}
  if(S.sea&&S.sea.material)S.sea.material.color.copy(c.sea);
  if(S.hillM)S.hillM.color.copy(c.hill);
  if(S.sandM)S.sandM.color.copy(c.sand);
}
function dotTex(){
  var c=document.createElement("canvas");c.width=c.height=32;var x=c.getContext("2d"),g=x.createRadialGradient(16,16,1,16,16,15);
  g.addColorStop(0,"rgba(255,255,255,1)");g.addColorStop(.6,"rgba(255,255,255,.9)");g.addColorStop(1,"rgba(255,255,255,0)");
  x.fillStyle=g;x.fillRect(0,0,32,32);return new THREE.CanvasTexture(c);
}
function initSeason(){
  var t=SEASONS[0],cc=function(h){return new THREE.Color(h)};
  S.season={cur:{sky:cc(t.sky),fog:cc(t.fog),hs:cc(t.hs),hg:cc(t.hg),sun:cc(t.sun),sea:cc(t.sea),hill:cc(t.hill),sand:cc(t.sand),si:t.si,hi:t.hi},k:1,idx:0,from:null,to:null,name:t,np:0};
  seasonSet(t,true);
  // partikel musim (kelopak, daun, salju) mengalir melewati pesawat; hanya ada di sisi pemain ini
  var N=S.lowFx?110:240,pos=new Float32Array(N*3),vel=new Float32Array(N*3);
  for(var i=0;i<N;i++){pos[i*3]=rnd(-34,34);pos[i*3+1]=rnd(-14,26);pos[i*3+2]=rnd(-75,8);vel[i*3]=rnd(-1,1);vel[i*3+1]=rnd(.6,1.4);vel[i*3+2]=rnd(.8,1.2)}
  var geo=new THREE.BufferGeometry();geo.setAttribute("position",new THREE.BufferAttribute(pos,3));
  var mat=new THREE.PointsMaterial({color:0xffffff,size:1.5,map:dotTex(),transparent:true,opacity:.9,depthWrite:false,sizeAttenuation:true});
  var pts=new THREE.Points(geo,mat);pts.frustumCulled=false;pts.visible=false;S.scene.add(pts);
  S.season.pts=pts;S.season.vel=vel;S.season.N=N;
  seasonParticles(t);
}
function seasonParticles(t){
  var m=S.season;if(!m||!m.pts)return;
  m.pts.visible=!!t.pc;
  if(t.pc){m.pts.material.color.setHex(t.pc);m.pts.material.size=t.pn===2?1.25:t.pn===1?2:1.6;m.fall=t.pn===2?.55:t.pn===1?1.05:.8;m.sway=t.pn===2?.8:1.6}
}
function seasonUpdate(dt){
  var m=S.season;if(!m)return;
  seasonApply(dt);
  var pts=m.pts,cam=S.camera;if(!pts||!cam||!pts.visible)return;
  var a=pts.geometry.attributes.position,p=a.array,v=m.vel,sp=(S.me?S.me.v:20)*.55,tt=performance.now()/1000;
  for(var i=0;i<m.N;i++){
    var k=i*3;
    p[k]+=Math.sin(tt*1.3+i)*(m.sway||1)*dt*v[k];
    p[k+1]-=(m.fall||.8)*5*dt*v[k+1];
    p[k+2]+=(sp+4)*dt*v[k+2];
    if(p[k+1]<-16||p[k+2]>10){p[k]=rnd(-34,34);p[k+1]=rnd(14,28);p[k+2]=-rnd(60,80)}
  }
  a.needsUpdate=true;
  pts.position.set(cam.position.x,cam.position.y,cam.position.z);
}
function nextSeason(){
  var m=S.season;if(!m)return;
  m.idx=(m.idx+1)%SEASONS.length;var t=SEASONS[m.idx];
  seasonSet(t,false);seasonParticles(t);
  var el=$("pl-season");
  if(el){el.textContent=t.i+" "+t.n;el.classList.remove("show");void el.offsetWidth;el.classList.add("show")}
}
function seasonLabel(){var m=S.season;return m?m.name.i+" "+m.name.n:""}

function buildWorld(){
  var sc=S.scene;
  sc.background=new THREE.Color(0x8fd0ff);sc.fog=new THREE.Fog(0xcfeaff,140,620);
  S.hemi=new THREE.HemisphereLight(0xdff0ff,0x3a8fc0,.95);sc.add(S.hemi);
  var sun=new THREE.DirectionalLight(0xfff2d0,.85);sun.position.set(-30,60,40);sc.add(sun);S.sun=sun;
  S.sea=new THREE.Mesh(new THREE.PlaneGeometry(1600,1600),new THREE.MeshLambertMaterial({map:seaTex()}));
  S.sea.rotation.x=-Math.PI/2;S.sea.position.y=SEAY;sc.add(S.sea);
  // awan & pulau didaur ulang di sekitar pesawat
  var cg=new THREE.SphereGeometry(1,8,6),cm=new THREE.MeshLambertMaterial({color:0xffffff,emissive:0x6f8fb5});
  S.clouds=[];
  for(var i=0;i<(S.lowFx?14:24);i++){
    var c=new THREE.Group(),n=4+Math.floor(Math.random()*3);
    for(var k=0;k<n;k++){var m=new THREE.Mesh(cg,cm);m.position.set(k*3.2-n*1.6,Math.random()*2,Math.random()*3);m.scale.setScalar(3+Math.random()*3.2);m.scale.y*=.7;c.add(m)}
    c.userData.far=(i%2===0);sc.add(c);S.clouds.push(c);
    placeFar(c,true);
  }
  var sandM=lam(0xf3dc9a),hillM=new THREE.MeshLambertMaterial({color:0x3fbf6f});S.hillM=hillM;S.sandM=sandM;
  var sg=new THREE.CylinderGeometry(14,18,3,12),hg=new THREE.ConeGeometry(10,12,9);
  S.isles=[];
  for(var j=0;j<8;j++){
    var g=new THREE.Group(),s=new THREE.Mesh(sg,sandM),h=new THREE.Mesh(hg,hillM);h.position.y=7;g.add(s,h);g.position.y=SEAY+1;
    g.scale.setScalar(.8+Math.random()*1.4);sc.add(g);S.isles.push(g);placeFar(g,true);
  }
  // gerbang berwarna sepanjang lintasan (didaur ulang) + garis finish
  var pm=lam(0xf8fafc),bg=new THREE.BoxGeometry(2.4,60,2.4),barG=new THREE.BoxGeometry(SPAN+12,3,2);
  S.gmats=GCOL.map(function(c){return new THREE.MeshLambertMaterial({color:c,emissive:c,emissiveIntensity:.45})});
  S.gates=[];
  for(var q=0;q<8;q++){
    var gr=new THREE.Group(),l=new THREE.Mesh(bg,pm),r=new THREE.Mesh(bg,pm),bar=new THREE.Mesh(barG,S.gmats[0]);
    l.position.set(-SPAN/2-6,SEAY+28,0);r.position.set(SPAN/2+6,SEAY+28,0);bar.position.set(0,SEAY+56,0);
    gr.add(l,r,bar);gr.userData.bar=bar;gr.userData.k=-99;sc.add(gr);S.gates.push(gr);
  }
  var f=new THREE.Group();
  var l2=new THREE.Mesh(bg,pm),r2=new THREE.Mesh(bg,pm);l2.position.set(-SPAN/2-6,SEAY+28,0);r2.position.set(SPAN/2+6,SEAY+28,0);
  var fb=new THREE.Mesh(new THREE.BoxGeometry(SPAN+12,7,2.4),new THREE.MeshBasicMaterial({map:checkerTex()}));fb.position.set(0,SEAY+56,0);
  var lbl=labelSprite("🏁 FINISH",512,128,84);lbl.scale.set(50,12.5,1);lbl.position.set(0,SEAY+70,0);
  f.add(l2,r2,fb,lbl);f.position.z=-S.L;sc.add(f);S.fin=f;
  // garis start
  var st=new THREE.Mesh(new THREE.BoxGeometry(SPAN+12,.4,3),new THREE.MeshBasicMaterial({map:checkerTex()}));st.position.set(0,SEAY+.3,0);sc.add(st);
  initSeason();
}
function placeFar(o,init){
  var cz=S.camera?S.camera.position.z:0,isIsle=!!(o.children&&o.children[0]&&o.children[0].geometry&&o.children[0].geometry.type==="CylinderGeometry");
  var side=Math.random()<.5?-1:1,x=side*((isIsle?70:SPAN/2+14)+Math.random()*(isIsle?220:170));
  o.position.x=x;
  o.position.z=cz-(init?rnd(-60,620):rnd(560,640));
  if(!isIsle)o.position.y=rnd(-8,34)
}
function updateWorld(dt){
  var cz=S.camera.position.z;
  S.sea.position.z=Math.round(cz/30)*30;
  S.clouds.concat(S.isles).forEach(function(o){if(o.position.z>cz+60)placeFar(o,false)});
  var k0=Math.floor(S.me?S.me.dist/GATEGAP:0)-1;
  S.gates.forEach(function(g,i){
    var k=k0+i;
    if(g.userData.k!==k){g.userData.k=k;g.userData.bar.material=S.gmats[((k%4)+4)%4]}
    g.position.z=-Math.max(0,k)*GATEGAP;g.visible=k>=1&&k*GATEGAP<S.L-60;
  });
}

/* ---------- adegan 3D ---------- */
function disposeScene(){
  try{
    if(S.scene)S.scene.traverse(function(o){
      if(o.geometry&&o.geometry.dispose)o.geometry.dispose();
      var m=o.material;if(m){(Array.isArray(m)?m:[m]).forEach(function(mm){if(mm.map&&mm.map.dispose)mm.map.dispose();if(mm.dispose)mm.dispose()})}
    });
    if(S.G)Object.keys(S.G).forEach(function(k){try{S.G[k].dispose()}catch(e){}});
    if(S.M)Object.keys(S.M).forEach(function(k){try{S.M[k].dispose()}catch(e){}});
  }catch(e){}
  S.G=null;S.M=null;S.sea=null;S.clouds=[];S.isles=[];S.gates=[];S.gmats=[];S.fin=null;S.racers=[];S.me=null;S.hemi=null;S.sun=null;S.hillM=null;S.sandM=null;S.season=null;
}
function racerBase(o){
  var base={isMe:false,remote:false,pid:"",name:"?",color:"#38bdf8",lat:0,ly:0,dist:0,v:0,target:BASEV,finished:false,finishT:0,correct:0,wrong:0,
    boost:0,roll:0,spin:0,timer:0,think:5,acc:.6,nd:0,nv:0,nat:performance.now(),fin:0,mesh:null,dot:null,x:0,y:0,z:0};
  for(var k in o)base[k]=o[k];return base;
}
function build3D(){
  disposeScene();
  if(S.renderer){try{S.renderer.dispose();S.renderer.domElement.remove()}catch(e){}S.renderer=null}
  S.L=COURSES[S.course].L;S.remote={};
  S.lowFx=false;try{S.lowFx=/CrOS/i.test(navigator.userAgent)||(navigator.hardwareConcurrency||8)<=4}catch(e){}
  try{if(AES_GFX_MODE!=="auto")S.lowFx=aesGfxLow()}catch(e){}
  var holder=$("pl-canvas");
  var r=new THREE.WebGLRenderer({antialias:!S.lowFx,powerPreference:"high-performance"});
  r.setPixelRatio(aesGfxRaceDpr(1.5));
  holder.appendChild(r.domElement);S.renderer=r;
  S.scene=new THREE.Scene();S.camera=new THREE.PerspectiveCamera(62,1,.5,900);
  buildWorld();
  // pembalap: aku + (latihan) lima pembalap komputer; dalam balapan guru, teman sekelas ditambahkan saat posisinya diterima
  var me=racerBase({isMe:true,pid:myPid(),name:myName(),color:myColor(),lat:latOfKey(myPid()),ly:altOfKey(myPid())});
  S.me=me;S.racers=[me];
  if(!S.auto&&!S.mode){
    var lv=LEVELS[S.lvl]||LEVELS[1],names=otherNames(),lanes=shuffle([0,1,2,3,4,5,6,7]);
    names.forEach(function(n,i){
      S.racers.push(racerBase({name:n,color:BOTCOL[i%BOTCOL.length],lat:-SPAN/2+LANEW*(lanes[i]+.5),ly:(i%5-2)*2.4,
        acc:rnd(lv.acc[0],lv.acc[1]),think:rnd(lv.think[0],lv.think[1]),timer:rnd(2,5)}));
    });
  }
  S.racers.forEach(function(rc){rc.mesh=makePlane(rc.color,rc.name,rc.isMe);S.scene.add(rc.mesh);placePlane(rc,0)});
  buildDots();onResize();
  var p=S.me;S.camera.position.set(p.x,p.y+5,p.z+17);
}
function placePlane(r,dt){
  if(!r.mesh)return;
  if(r.latT!==undefined){var kk=Math.min(1,(dt||0)*3);r.lat+=(r.latT-r.lat)*kk;r.ly+=(r.lyT-r.ly)*kk;r.vb=(r.vb||0)+((r.vbT||0)-(r.vb||0))*kk}
  r.x=r.lat;r.z=-(r.dist-(r.vb||0));
  var tt=performance.now()/1000,bob=Math.sin(tt*1.7+r.lat)*.35;
  r.y=r.ly+bob;
  r.mesh.position.set(r.x,r.y,r.z);
  var u=r.mesh.userData;
  r.roll+=(0-r.roll)*Math.min(1,(dt||0)*3);
  u.body.rotation.z=r.roll+Math.sin(tt*1.3+r.lat*.3)*.03;
  u.body.rotation.x=-clamp((r.v-BASEV)/MAXV,-.4,.8)*.12;
  u.prop.rotation.z+=(dt||0)*(34+r.v);
}
/* penata posisi: 8 jalur x 5 ketinggian = 40 sel; pesawat di belakang pindah sel kosong agar tidak bertumpuk */
function planPlanes(){
  try{
    if(!S.scene||!window.aesLanePlan)return;
    var items=[],byK={};
    S.racers.forEach(function(r){
      if(!r.mesh||(r.remote&&!r.mesh.visible))return;
      var key=r.isMe?"me":String(r.pid||r.name),hk=hashStr(r.isMe?myPid():(r.pid||r.name));byK[key]=r;
      items.push({k:key,d:r.dist,p:(r.cell===undefined?-1:r.cell),h:(Math.floor(hk/NLANE)%5)*NLANE+(hk%NLANE),fix:!!r.isMe});
    });
    var pl=window.aesLanePlan(items,NLANE,5,14);
    Object.keys(pl).forEach(function(k){
      var r=byK[k],q=pl[k];if(!r)return;
      var ln=q.c%NLANE,rw=Math.floor(q.c/NLANE),first=r.cell===undefined;
      r.cell=q.c;r.latT=-SPAN/2+LANEW*(ln+.5);r.lyT=(rw-2)*2.4;r.vbT=q.back;
      if(first){r.lat=r.latT;r.ly=r.lyT;r.vb=q.back}
    });
  }catch(e){}
}
function buildDots(){
  var tb=$("pl-trackbar");if(!tb)return;
  Array.prototype.slice.call(tb.querySelectorAll(".pl-dot")).forEach(function(d){d.remove()});
  var n=0;
  S.racers.forEach(function(r){
    r.dot=null;if(!r.isMe&&n>=40)return;if(!r.isMe)n++;
    var d=document.createElement("div");d.className="pl-dot"+(r.isMe?" me":"");d.style.background=r.color;d.title=r.name;tb.appendChild(d);r.dot=d;
  });
}
function onResize(){
  if(!S.renderer||!S.camera)return;
  var w=Math.max(2,window.innerWidth),h=Math.max(2,window.innerHeight);
  S.renderer.setSize(w,h);S.camera.aspect=w/h;S.camera.updateProjectionMatrix();
  var qp=$("pl-qpanel").classList.contains("show"),port=w/h<.95,land=h<=520&&w>h;
  S.shiftY=qp?(port?1:land?0:.7):0;S.shiftX=(qp&&land)?1:0;
}

/* ---------- soal ---------- */
function resetQueue(){var qs=getQs();S.qList=(window.AESQBag?window.AESQBag.order(qs):shuffle(qs.map(function(_,i){return i})));S.qPtr=0}
function nextQuestion(){
  var qs=getQs();if(!qs.length)return;
  if(S.qPtr>=S.qList.length){resetQueue();if(S.qList.length>1&&S.qList[0]===S.lastQ){var t=S.qList.shift();S.qList.push(t)}}
  var qi=S.qList[S.qPtr++],q=qs[qi];try{window.AESQBag&&window.AESQBag.mark(q)}catch(e){}S.lastQ=qi;S.cur={qi:qi,q:q};S.locked=false;
  var ord=optOrder(q);
  $("pl-qno").textContent="Soal #"+(S.me.correct+S.me.wrong+1)+" • benar "+S.me.correct+"/"+qNeed();
  var html=rich(q.q);
  if(q.image&&/^(https?:|data:image)/i.test(q.image))html+='<img id="pl-qimg" src="'+esc(q.image)+'">';
  $("pl-qtext").innerHTML=html;
  var box=$("pl-opts");box.innerHTML="";
  ord.forEach(function(oi,pos){
    var b=document.createElement("button");b.type="button";b.className="pl-opt";b.dataset.oi=oi;
    b.innerHTML="<b>"+String.fromCharCode(65+pos)+"</b><span>"+rich(q.options[oi])+"</span>";
    b.onclick=function(){pick(pos)};box.appendChild(b);
  });
  $("pl-fb").textContent="";
  typeset([$("pl-qtext"),box]);
  $("pl-qpanel").scrollTop=0;
}
function updateChips(){$("pl-cok").textContent="✓"+S.me.correct;$("pl-cbad").textContent="✗"+S.me.wrong;$("pl-cstreak").textContent="🔥"+S.streak}
function fx(text,cls){var e=$("pl-fx");e.textContent=text;e.className=cls;void e.offsetWidth;e.className=cls+" show"}
function flash(cls){var e=$("pl-flash");e.className=cls;void e.offsetWidth;e.className=cls+" go"}
function pick(pos){
  if(S.locked||S.state!=="run"||!S.cur)return;
  var btns=$("pl-opts").children;if(pos<0||pos>=btns.length)return;
  S.locked=true;
  var chosen=Number(btns[pos].dataset.oi),right=Number(S.cur.q.correct),me=S.me,ok=chosen===right;
  if(ok){
    me.correct++;S.streak++;if(S.streak>S.bestStreak)S.bestStreak=S.streak;
    me.target=Math.min(MAXV,me.target+BOOST+Math.min(S.streak-1,5)*.9);me.v+=3.2;
    btns[pos].classList.add("pl-ok");sfx("correct_row");S.kick=1;flash("ok");me.boost=1;nextSeason();
    fx(S.streak>=3?"🔥 KOMBO x"+S.streak+"! NGEBUT!":"🚀 BENAR! PESAWAT MAKIN KENCANG","ok");
    $("pl-fb").style.color="#4ade80";$("pl-fb").textContent="✅ Benar! Kecepatan naik.  "+seasonLabel();
    updateChips();later(nextQuestion,450);
  }else{
    me.wrong++;S.streak=0;me.target=Math.max(MINV,me.target-SLOW);me.v*=.68;S.shake=1;me.roll=(Math.random()<.5?-1:1)*.5;flash("bad");
    btns[pos].classList.add("pl-bad");
    for(var i=0;i<btns.length;i++)if(Number(btns[i].dataset.oi)===right)btns[i].classList.add("pl-ok");
    sfx("wrong_answer");fx("🌪️ SALAH! MELAMBAT","bad");
    $("pl-fb").style.color="#fb7185";$("pl-fb").textContent="❌ Salah. Jawaban yang benar ditandai hijau.";
    var at=Math.min(S.qList.length,S.qPtr+2+Math.floor(Math.random()*3));S.qList.splice(at,0,S.cur.qi);  // soal yang salah muncul lagi sebentar lagi
    updateChips();later(nextQuestion,1250);
  }
}

/* ---------- alur balapan ---------- */
function fmt(t){t=Math.max(0,t);var m=Math.floor(t/60),s=t-m*60;return(m<10?"0":"")+m+":"+(s<10?"0":"")+s.toFixed(1)}
function bestKey(){return"aes_plane_best_"+S.course}
function getBest(){try{var v=parseFloat(localStorage.getItem(bestKey()));return isFinite(v)?v:null}catch(e){return null}}
function setBest(t){try{localStorage.setItem(bestKey(),String(t))}catch(e){}}
function showBest(){
  var b=getBest(),nm=COURSES[S.course].name;
  $("pl-best").textContent=b?("🏆 Rekor pribadimu (jarak "+nm+"): "+fmt(b)):"Belum ada rekor untuk jarak ini — ayo catat yang pertama!";
}
function showStart(){
  S.state="idle";clearTimers();
  $("pl-start").classList.remove("pl-hide");$("pl-result").classList.add("pl-hide");$("pl-qpanel").classList.remove("show");$("pl-count").textContent="";
  var n=getQs().length;
  $("pl-who").innerHTML="Halo <b>"+esc(myName())+"</b>! "+(n?("Bank soal: <b>"+n+" soal</b> dari materi kelas."):'<span style="color:#fca5a5">Belum ada soal. Guru perlu mengisi soal di kolom Edit pada halaman awal.</span>');
  $("pl-go").disabled=!n;showBest();
}
function startRace(){
  if(!getQs().length)return;
  $("pl-start").classList.add("pl-hide");
  build3D();
  S.T=0;S.streak=0;S.bestStreak=0;S.maxV=0;S.resultShown=false;S.finishCount=0;S.shake=0;S.kick=0;S.orbit=0;
  resetQueue();updateChips();
  S.state="countdown";S.cdStep=3;S.cd=0;
  $("pl-qpanel").classList.add("show");onResize();
  nextQuestion();S.locked=true;  // soal terlihat, tombol aktif saat GO
  $("pl-count").textContent="3";sfx("click");
}
function onFinishMe(){
  S.state="done";S.locked=true;sfx("finish_island");
  if(S.auto){NET.myFin[S.auto]=1;pubRun(topicRes(),{a:"fin",id:S.auto,pid:myPid(),name:myName(),t:Math.round(S.me.finishT*10)/10,ok:S.me.correct,bad:S.me.wrong,L:S.L});pubPos()}
  var t=S.me.finishT,best=getBest(),newRec=false;
  if(!best||t<best){setBest(t);newRec=true}
  fx(newRec?"🏆 REKOR BARU!":"🏁 FINISH!","ok");
  $("pl-qpanel").classList.remove("show");onResize();
  S.orbit=0;S.kick=1;
  later(function(){showResult(newRec)},3600);
}
function ranking(){
  return S.racers.slice().sort(function(a,b){
    if(a.finished&&b.finished)return a.finishT-b.finishT;
    if(a.finished)return-1;if(b.finished)return 1;return b.dist-a.dist;
  });
}
function showResult(newRec){
  if(S.resultShown)return;S.resultShown=true;
  var rk=ranking(),pl=rk.indexOf(S.me)+1,me=S.me,tot=me.correct+me.wrong;
  var medal=pl===1?"🥇":pl===2?"🥈":pl===3?"🥉":"🏅";
  $("pl-rtitle").textContent=medal+(pl===1?" JUARA 1!":" POSISI KE-"+pl);
  $("pl-rsub").textContent=newRec?"🏆 Rekor pribadi baru untuk jarak "+COURSES[S.course].name+"!":"Jarak "+COURSES[S.course].name+" • "+S.L+" m • "+(S.auto?"melawan teman sekelas":"melawan komputer");
  $("pl-rstats").innerHTML=
    "<div><b>"+fmt(me.finishT)+"</b><span>WAKTU</span></div>"+
    "<div><b>"+(tot?Math.round(me.correct/tot*100):0)+"%</b><span>AKURASI</span></div>"+
    "<div><b>"+Math.round(S.maxV*3.6)+"</b><span>KM/JAM MAKS</span></div>"+
    "<div><b style='color:#4ade80'>"+me.correct+"</b><span>BENAR</span></div>"+
    "<div><b style='color:#fb7185'>"+me.wrong+"</b><span>SALAH</span></div>"+
    "<div><b style='color:#fdba74'>"+S.bestStreak+"</b><span>KOMBO TERBAIK</span></div>";
  fillResultTable();
  $("pl-result").classList.remove("pl-hide");
}
function fillResultTable(){
  var rk=ranking().slice(0,60);
  $("pl-rtable").innerHTML=rk.map(function(r,i){
    return '<div class="pl-row'+(r.isMe?" me":"")+'"><span class="pl">#'+(i+1)+'</span><span class="nm">'+esc(r.name)+(r.isMe?" (Kamu)":"")+'</span><span class="tm">'+(r.finished?fmt(r.finishT):Math.round(Math.min(r.dist,S.L)/S.L*100)+"%")+'</span></div>';
  }).join("");
}

/* ---------- pembaruan tiap frame ---------- */
function update(dt){
  var me=S.me;if(!me)return;
  if(S.auto&&S.scene){S.lpt=(S.lpt||0)-dt;if(S.lpt<=0){S.lpt=.2;planPlanes()}}
  var racing=S.state==="run"||S.state==="done",tnow=performance.now()/1000;
  if(S.state==="countdown"){
    S.cd+=dt;
    if(S.cd>=.9){
      S.cd=0;S.cdStep--;
      if(S.cdStep>0){$("pl-count").textContent=String(S.cdStep);sfx("click")}
      else{$("pl-count").textContent="GO!";sfx("finish_island");S.state="run";S.T=0;S.locked=false;S.kick=.8;onResize();later(function(){if(S.state!=="idle")$("pl-count").textContent=""},700)}
    }
  }
  if(racing){
    S.T+=dt;
    S.racers.forEach(function(r){
      if(r.remote){ // pesawat teman sekelas: ikuti posisi yang dikirim lewat jaringan (dihaluskan)
        var ag=Math.min(1.6,(performance.now()-r.nat)/1000);
        var pd=r.nd+(r.fin>0?0:r.nv*ag);
        if(r.fin>0){r.finished=true;r.finishT=r.fin;pd=Math.max(pd,S.L)}
        r.dist+=(pd-r.dist)*Math.min(1,dt*5);
        if(r.dist>S.L+RUNOFF)r.dist=S.L+RUNOFF;
        r.v+=(r.nv-r.v)*Math.min(1,dt*5);if(r.v<0)r.v=0;
        return;
      }
      if(!r.isMe&&!r.finished){
        r.timer-=dt;
        if(r.timer<=0){
          r.timer=r.think*rnd(.8,1.25);
          if(Math.random()<r.acc){r.correct++;r.target=Math.min(MAXV,r.target+BOOST*rnd(.8,1.1));r.v+=1.8;r.boost=.8}
          else{r.wrong++;r.target=Math.max(MINV,r.target-SLOW*rnd(.8,1.1));r.v*=.75}
        }
      }
      if(r.finished)r.target=BASEV*.8;
      else{ // kelelahan / pemulihan perlahan menuju kecepatan dasar
        if(r.target>BASEV)r.target=Math.max(BASEV,r.target-.55*dt);
        else if(r.target<BASEV)r.target=Math.min(BASEV,r.target+.4*dt);
      }
      r.v+=(r.target-r.v)*Math.min(1,dt*2.4);
      if(r.v<0)r.v=0;
      if(!r.finished){var _g=capQ(r)-r.dist;if(_g<1e9){var _vm=Math.max(0,_g)*1.6+CREEP;if(r.v>_vm)r.v=_vm}}
      r.dist=Math.min(r.dist+r.v*dt,S.L+RUNOFF);
      if(!r.finished&&r.correct<qNeed()){var _h=S.L*.98;if(r.dist>_h){r.dist=_h;r.v=0}}
      if(r.dist>=S.L+RUNOFF)r.v=0;
      if(r.boost>0)r.boost-=dt;
      if(!r.finished&&r.dist>=S.L){
        r.finished=true;r.finishT=S.T;S.finishCount++;
        if(r.isMe)onFinishMe();
      }
    });
    if(me.v>S.maxV)S.maxV=me.v;
    if(S.auto){
      S.pubT-=dt;if(S.pubT<=0){S.pubT=posEvery();pubPos()}
      S.mt-=dt;if(S.mt<=0){S.mt=.6;refreshMeshes()}
      if(S.state==="done"&&S.resultShown&&NET.finalShown!==S.auto){S.rt-=dt;if(S.rt<=0){S.rt=1.5;fillResultTable()}}
    }
    if(S.state==="done"&&S.orbit>=1&&!S.auto&&S.racers.every(function(r){return r.finished}))showResult(false);
  }
  S.racers.forEach(function(r){if(r.mesh&&(!r.remote||r.mesh.visible))placePlane(r,dt)});

  // kamera
  var cam=S.camera,port=cam.aspect<.95?Math.min(1,(.95-cam.aspect)/.5):0;
  var tx,ty,tz,lx,ly,lz;
  if(S.state==="idle"){ // sebelum mulai: kamera berputar pelan mengitari landasan start
    var a=tnow*.25;
    tx=Math.sin(a)*40;ty=SEAY+34;tz=Math.cos(a)*40;lx=0;ly=0;lz=-10;
  }else if(S.state==="done"){
    S.orbit=Math.min(1,S.orbit+dt/2.6);
    var e=S.orbit*S.orbit*(3-2*S.orbit),th=Math.PI*1.1*e,rr=17+port*7;
    tx=me.x+Math.sin(th)*rr;ty=me.y+4.5-e*1.5;tz=me.z+Math.cos(th)*rr;lx=me.x;ly=me.y;lz=me.z;
  }else{
    var back=17+port*8+(me.v>40?(me.v-40)*.15:0);
    tx=me.x;ty=me.y+5.2+port*1.5;tz=me.z+back;
    lx=me.x+S.shiftX*10;ly=me.y+1-S.shiftY*4.5;lz=me.z-28;
  }
  var kk=S.state==="idle"?.08:1-Math.exp(-dt*7);
  cam.position.x+=(tx-cam.position.x)*kk;cam.position.y+=(ty-cam.position.y)*kk;cam.position.z+=(tz-cam.position.z)*kk;
  if(S.shake>0){cam.position.x+=(Math.random()-.5)*S.shake*1.4;cam.position.y+=(Math.random()-.5)*S.shake*1.1;S.shake=Math.max(0,S.shake-dt*2.2)}
  cam.lookAt(lx,ly,lz);
  var fov=62+Math.min(18,Math.max(0,(me.v-BASEV)*.45))+S.kick*6+port*6;
  if(Math.abs(cam.fov-fov)>.05){cam.fov+=(fov-cam.fov)*Math.min(1,dt*5);cam.updateProjectionMatrix()}
  S.kick=Math.max(0,S.kick-dt*1.6);
  updateWorld(dt);seasonUpdate(dt);

  // HUD
  var kmh=Math.round(me.v*3.6);
  $("pl-kmh").textContent=kmh;$("pl-spdbar").style.width=clamp(me.v/MAXV*100,0,100)+"%";
  $("pl-speedfx").style.opacity=clamp((me.v-BASEV-6)/22,0,1);
  S.dt4-=dt;
  if(S.dt4<=0){
    S.dt4=.25;
    var rk=ranking(),pl=rk.indexOf(me)+1;
    $("pl-place").innerHTML="#"+pl+"<small>/"+S.racers.length+"</small>";
    $("pl-time").textContent=fmt(me.finished?me.finishT:(racing?S.T:0));
    $("pl-left").innerHTML=Math.max(0,Math.ceil(S.L-me.dist))+'<small style="font-size:11px;color:#94a3b8"> m</small>';
    $("pl-dist").textContent=Math.min(Math.round(me.dist),S.L)+" / "+S.L+" m";
    S.racers.forEach(function(r){if(r.dot)r.dot.style.left=clamp(r.dist/S.L,0,1)*100+"%"});
  }
}
function frame(ts){
  if(!S.open)return;
  S.raf=requestAnimationFrame(frame);
  var dt=Math.min(.1,(ts-S.last)/1000||0);S.last=ts;
  try{if(S.mode==="watch")updateWatch(dt);else update(dt);S.renderer.render(S.scene,S.camera)}catch(e){console.error("[BalapPesawat]",e)}
}

/* ---------- buka / tutup ---------- */
function onKey(e){
  if(!S.open)return;
  e.stopPropagation();  // jangan sampai tombol A-D menggerakkan avatar di aplikasi utama
  var k=(e.key||"").toLowerCase(),map={a:0,b:1,c:2,d:3,"1":0,"2":1,"3":2,"4":3};
  if(k==="escape"){closeRun(true);return}
  if(k in map&&S.state==="run"){e.preventDefault();pick(map[k])}
}
function pauseMainRender(){
  try{
    if(typeof renderer!=="undefined"&&renderer&&renderer!==S.renderer&&!renderer.__plPatched){
      var orig=renderer.render;
      renderer.render=function(){if(S.open)return;return orig.apply(this,arguments)};
      renderer.__plPatched=true;
    }
  }catch(e){}
}
function openRunCore(mode){
  if(S.open)return;
  if(typeof THREE==="undefined"){alert("Three.js belum termuat. Cek koneksi internet lalu muat ulang halaman.");return}
  try{if(window.AESCar&&window.AESCar._state&&window.AESCar._state.open)window.AESCar.close()}catch(e){}
  try{if(window.AESRun&&window.AESRun._state&&window.AESRun._state.open)window.AESRun.close()}catch(e){}
  if(mode!=="auto")S.auto=null;
  S.mode=mode||null;
  S.pubT=0;S.rt=0;S.mt=0;
  try{var _w=$("pl-watch"),_k=$("pl-w-rank");if(_w)_w.style.display="none";if(_k)_k.style.display="none"}catch(e){}
  S.open=true;pauseMainRender();$("pl-overlay").classList.add("pl-open");$("pl-launch").style.display="none";
  $("pl-tpanel").classList.add("pl-hide");$("pl-miss").classList.add("pl-hide");
  $("pl-again").style.display=mode?"none":"";
  S.state="idle";
  if(mode==="auto"){$("pl-result").classList.add("pl-hide");$("pl-start").classList.add("pl-hide");startRace()}
  else if(mode==="watch"){
    $("pl-start").classList.add("pl-hide");$("pl-result").classList.add("pl-hide");$("pl-qpanel").classList.remove("show");$("pl-count").textContent="";
    build3D();
    try{if(S.me&&S.me.mesh){S.scene.remove(S.me.mesh);S.me.mesh=null}}catch(e){}
    S.me=racerBase({isMe:true,pid:"watch",name:"Guru"});S.racers=[];S.remote={};   // "me" hanya penanda kamera, bukan pesawat
    S.state="watch";S.T=0;S.watchCam=S.watchCam||0;S._wsig="";S.dt4=0;S.lpt=0;S.mt=0;
    buildDots();showWatchUI();
  }
  else if(mode==="miss"||mode==="final"){
    $("pl-start").classList.add("pl-hide");$("pl-result").classList.add("pl-hide");$("pl-qpanel").classList.remove("show");$("pl-count").textContent="";
    build3D();
    if(mode==="miss")$("pl-miss").classList.remove("pl-hide");
  }else{build3D();showStart()}
  S.last=performance.now();S.raf=requestAnimationFrame(frame);
}
function openRun(){ // tombol BALAP PESAWAT: guru -> panel guru (siswa tidak bisa memulai sendiri)
  if(S.open)return;
  if(isTeacherNow()){openTPanel();return}
  if(STUDENT_SOLO)openRunCore();
}
function closeRun(ask){
  if(!S.open)return;
  if(ask&&(S.state==="run"||S.state==="countdown")&&!confirm("Keluar dari balapan? Progres balapan ini tidak disimpan."))return;
  S.open=false;cancelAnimationFrame(S.raf);clearTimers();
  $("pl-overlay").classList.remove("pl-open");
  try{var _w2=$("pl-watch"),_k2=$("pl-w-rank");if(_w2)_w2.style.display="none";if(_k2)_k2.style.display="none"}catch(e){}
  S.watchId=null;S.watchFollow=null;
  disposeScene();
  if(S.renderer){try{S.renderer.dispose();S.renderer.forceContextLoss&&S.renderer.forceContextLoss();S.renderer.domElement.remove()}catch(e){}S.renderer=null}
  S.scene=null;S.state="idle";S.auto=null;S.mode=null;S.remote={};
}

/* ---------- BALAPAN DIATUR GURU: perintah mulai, posisi antar siswa, hasil ---------- */
var NET={c:null,room:null,subs:{},handled:{},myFin:{},state:null,stLive:false,missT:null,finalShown:null,finalAt:null,run:null,pt:0,tCourse:"m"};
function topicCmd(){return"aes_class_3d/"+roomId+"/plane_cmd"}
function topicRes(){return"aes_class_3d/"+roomId+"/plane_res"}
function topicState(){return"aes_class_3d/"+roomId+"/plane_state"}
function topicPos(){return"aes_class_3d/"+roomId+"/plane_pos"}
function isStudentNow(){try{return !isTeacherNow()&&!!myPlayer&&myPlayer.role==="student"&&!!myPlayer.hasJoinedGame&&!(typeof isTeacher3DMonitor!=="undefined"&&isTeacher3DMonitor)}catch(e){return false}}
function myPid(){try{return String(myPlayer.id||myName())}catch(e){return myName()}}
function pubRun(topic,obj,retain){
  try{var c=(typeof mqttClient!=="undefined")?mqttClient:null;if(c&&c.connected){c.publish(topic,JSON.stringify(obj),{qos:1,retain:!!retain});return true}}catch(e){}
  return false;
}
function note(msg){
  var n=document.createElement("div");n.textContent=msg;
  n.style.cssText="position:fixed;left:50%;top:14px;transform:translateX(-50%);z-index:9700;background:#0f172a;color:#fde047;border:1px solid rgba(255,255,255,.4);padding:8px 14px;border-radius:12px;font:800 13px 'Plus Jakarta Sans',sans-serif;max-width:90vw;text-align:center";
  document.body.appendChild(n);setTimeout(function(){n.remove()},3800);
}
function isSeen(id){try{return localStorage.getItem("aes_plane_seen")===id}catch(e){return false}}
function setSeen(id){try{localStorage.setItem("aes_plane_seen",id)}catch(e){}}
/* interval kirim posisi menyesuaikan jumlah siswa online, agar jaringan sekolah tidak kewalahan */
function posEvery(){
  var n=1;try{if(typeof aesOnlineN==="function")n=aesOnlineN()}catch(e){}
  return n<=12?.5:n<=30?.8:n<=60?1.2:1.8;
}
function onNetMsg(topic,payload,packet){
  if(topic.indexOf("/plane_")<0)return;
  var d;try{d=JSON.parse(payload.toString())}catch(e){return}
  if(!d||typeof d!=="object")return;
  try{
    if(topic===topicCmd()){if(isStudentNow())onCmd(d)}
    else if(topic===topicState()){if(isStudentNow()){NET.state=d;NET.stLive=!(packet&&packet.retain);evalState()}}
    else if(topic===topicRes()){if(isTeacherNow())onRes(d)}
    else if(topic===topicPos()){onPos(d)}
  }catch(e){console.error("[BalapPesawat net]",e)}
}
function bindNet(){
  try{
    var c=(typeof mqttClient!=="undefined")?mqttClient:null,rm=(typeof roomId!=="undefined")?roomId:null;
    if(!c||!rm||!c.connected)return;
    if(!c.__plL){c.__plL=true;c.on("message",onNetMsg)}
    if(NET.c!==c||NET.room!==rm){NET.c=c;NET.room=rm;NET.subs={}}
    var want=isTeacherNow()?[topicRes(),topicPos()]:(isStudentNow()?[topicCmd(),topicState(),topicPos()]:[]);
    want.forEach(function(t){if(!NET.subs[t]){NET.subs[t]=1;c.subscribe(t,{qos:1})}});
    if(isStudentNow())evalState();
  }catch(e){}
}
setInterval(bindNet,1200);

/* siswa: pastikan guru benar-benar menerima "ikut" dan "finish" kita; kirim ulang bila paket hilang */
function reconcile(){
  try{
    if(!S.open||!S.auto||!S.me||!isStudentNow())return;
    var st=NET.state;
    if(!st||st.id!==S.auto||!Array.isArray(st.rows))return;
    var me=nk(myName()),row=null;
    st.rows.forEach(function(r){if(nk(r.n)===me)row=r});
    if(S.state==="done"&&(!row||row.s!=="fin")){
      pubRun(topicRes(),{a:"fin",id:S.auto,pid:myPid(),name:myName(),t:Math.round(S.me.finishT*10)/10,ok:S.me.correct,bad:S.me.wrong,L:S.L});
    }else if(!row){
      pubRun(topicRes(),{a:"join",id:S.auto,pid:myPid(),name:myName()});
    }
  }catch(e){}
}
setInterval(reconcile,4000);

/* penanda koneksi terputus + kirim posisi segera setelah tersambung kembali */
var _netWasOk=true;
function netBadge(){
  var el=$("pl-net");
  if(!el){
    el=document.createElement("div");el.id="pl-net";
    el.style.cssText="display:none;position:absolute;left:50%;top:118px;transform:translateX(-50%);z-index:7;max-width:92vw;text-align:center;background:#b45309;color:#fff;border:1px solid #fde68a;border-radius:12px;padding:6px 12px;font:800 12px 'Plus Jakarta Sans',sans-serif;pointer-events:none";
    $("pl-overlay").appendChild(el);
  }
  var c=(typeof mqttClient!=="undefined")?mqttClient:null,ok=!!(c&&c.connected);
  var show=S.open&&!ok&&!!S.auto;
  el.style.display=show?"block":"none";
  if(show)el.textContent="⚠ Koneksi terputus, menyambung ulang… balapan tetap berjalan dan hasilmu dikirim otomatis saat tersambung.";
  if(ok&&!_netWasOk){S.pubT=0;NET.subs={}}
  _netWasOk=ok;
}
setInterval(netBadge,1000);

/* siswa: kirim posisi pesawatku ke teman sekelas & guru */
function pubPos(){
  try{
    var c=(typeof mqttClient!=="undefined")?mqttClient:null,me=S.me;
    if(!c||!c.connected||!me||!S.auto)return;
    c.publish(topicPos(),JSON.stringify({id:S.auto,pid:myPid(),name:myName(),col:myColor(),d:Math.round(me.dist*10)/10,v:Math.round(me.v*10)/10,f:me.finished?Math.round(me.finishT*10)/10:0}),{qos:0,retain:false});
  }catch(e){}
}
function addRemote(m){
  if(!S.scene)return null;
  var key=String(m.pid);
  var col=/^#[0-9a-fA-F]{6}$/.test(String(m.col||""))?m.col:BOTCOL[Object.keys(S.remote).length%BOTCOL.length];
  var r=racerBase({remote:true,pid:key,name:String(m.name||"?").slice(0,24),color:col,lat:latOfKey(key),ly:altOfKey(key),idx:S.racers.length});
  S.remote[key]=r;S.racers.push(r);buildDots();
  return r;
}
/* gambar 3D hanya untuk 12 lawan terdekat (supaya Chromebook tetap lancar); sisanya tetap dihitung di peringkat */
var MAXMESH=(typeof AES_LOWEND!=="undefined"&&AES_LOWEND)?10:16;
function refreshMeshes(){
  if(!S.scene||!S.me)return;
  try{MAXMESH=aesGfxMaxMesh()}catch(e){}
  var arr=S.racers.filter(function(r){return r.remote});
  arr.sort(function(a,b){return Math.abs(a.dist-S.me.dist)-Math.abs(b.dist-S.me.dist)});
  arr.forEach(function(r,i){
    var want=i<(S.mode==="watch"?24:MAXMESH);
    if(want&&!r.mesh){
      try{r.mesh=makePlane(r.color,r.name,false);S.scene.add(r.mesh);placePlane(r,0)}catch(e){r.mesh=null;return}
    }
    if(r.mesh)r.mesh.visible=want;
  });
}

/* ---------- GURU: TONTON BALAPAN PESAWAT LANGSUNG (3D) ---------- */
function openWatch(){
  var r=NET.run;
  if(!r||r.status==="ended"){note("Mulai balapan dulu (📣 MULAI BALAPAN SEMUA SISWA), lalu tekan Tonton langsung.");return}
  if(S.open)return;
  if(typeof THREE==="undefined"){alert("Three.js belum termuat. Cek koneksi internet lalu muat ulang halaman.");return}
  bindNet();
  S.course=cKey(r.course);S.watchId=r.id;S.watchFollow=null;S._wrestart=false;
  openRunCore("watch");
}
function feedRemote(d){
  var key=String(d.pid);if(!key)return;
  var r=S.remote[key];
  if(!r){r=addRemote(d);if(!r)return;r.dist=Number(d.d)||0}
  var nd0=Number(d.d)||0;
  if(nd0<r.nd-0.05&&!(Number(d.f)>0))return;
  r.nd=Math.max(r.nd,nd0);r.nv=clamp(Number(d.v)||0,0,MAXV+3);r.nat=performance.now();
  if(Number(d.f)>0)r.fin=Number(d.f);
}
function showWatchUI(){
  var ov=$("pl-overlay"),w=$("pl-watch"),k=$("pl-w-rank");
  var bs="border:0;border-radius:10px;padding:7px 11px;background:#0ea5e9;color:#fff;font:800 12px system-ui,sans-serif;cursor:pointer;pointer-events:auto";
  if(!w){
    w=document.createElement("div");w.id="pl-watch";
    w.style.cssText="position:absolute;left:50%;bottom:calc(14px + env(safe-area-inset-bottom,0px));transform:translateX(-50%);z-index:9;display:flex;gap:8px;align-items:center;flex-wrap:wrap;justify-content:center;max-width:94vw;background:rgba(15,23,42,.85);border:1px solid rgba(148,163,184,.4);border-radius:14px;padding:8px 10px;color:#fff;font:800 12px system-ui,sans-serif;pointer-events:auto";
    w.innerHTML='<span>👁️ TONTON LANGSUNG</span><select id="pl-w-sel" style="background:#1e293b;color:#fff;border:1px solid #475569;border-radius:8px;padding:6px 8px;font:700 12px system-ui,sans-serif;max-width:46vw"><option value="">🥇 Ikuti pemimpin</option></select><button id="pl-w-cam" type="button" style="'+bs+'">🎥 Kamera: Dekat</button><button id="pl-w-panel" type="button" style="'+bs+';background:#475569">📋 Panel guru</button>';
    ov.appendChild(w);
    $("pl-w-sel").onchange=function(){S.watchFollow=this.value||null};
    $("pl-w-cam").onclick=function(){S.watchCam=S.watchCam?0:1;this.textContent=S.watchCam?"🎥 Kamera: Jauh":"🎥 Kamera: Dekat"};
    $("pl-w-panel").onclick=function(){closeRun(false);openTPanel()};
  }
  if(!k){
    k=document.createElement("div");k.id="pl-w-rank";
    k.style.cssText="position:absolute;left:10px;top:150px;z-index:8;min-width:180px;max-width:48vw;background:rgba(15,23,42,.75);border:1px solid rgba(148,163,184,.35);border-radius:12px;padding:8px 10px;color:#fff;font:600 12px/1.55 system-ui,sans-serif;pointer-events:none";
    ov.appendChild(k);
  }
  w.style.display="flex";k.style.display="block";
  $("pl-w-cam").textContent=S.watchCam?"🎥 Kamera: Jauh":"🎥 Kamera: Dekat";
  $("pl-w-sel").value="";k.innerHTML="Menunggu pesawat siswa…";
}
function updateWatch(dt){
  var me=S.me;if(!me)return;
  var nowp=performance.now();
  if(NET.run&&NET.run.id!==S.watchId&&!S._wrestart){ // guru memulai balapan baru: muat ulang tampilan
    S._wrestart=true;
    setTimeout(function(){if(S.open&&S.mode==="watch"){closeRun(false);if(NET.run&&NET.run.status!=="ended")openWatch()}},0);
  }
  S.racers.forEach(function(r){ // pesawat siswa mengikuti posisi dari jaringan (dihaluskan)
    var ag=Math.min(1.6,(nowp-r.nat)/1000),pd=r.nd+(r.fin>0?0:r.nv*ag);
    if(r.fin>0){r.finished=true;r.finishT=r.fin;pd=Math.max(pd,S.L)}
    r.dist+=(pd-r.dist)*Math.min(1,dt*5);
    if(r.dist>S.L+RUNOFF)r.dist=S.L+RUNOFF;
    r.v+=(r.nv-r.v)*Math.min(1,dt*5);if(r.v<0)r.v=0;
  });
  S.lpt=(S.lpt||0)-dt;if(S.lpt<=0){S.lpt=.2;planPlanes()}
  S.mt=(S.mt||0)-dt;if(S.mt<=0){S.mt=.6;refreshMeshes()}
  S.racers.forEach(function(r){if(r.mesh&&r.mesh.visible)placePlane(r,dt)});
  var rk=ranking(),tgt=(S.watchFollow&&S.remote[S.watchFollow])||rk[0]||null;
  if(tgt){me.dist=tgt.dist;me.v=tgt.v;me.x=tgt.x;me.y=tgt.y;me.z=tgt.z}else{me.dist=0;me.v=0}
  // kamera
  var cam=S.camera,tx,ty,tz,lx,ly,lz;
  if(!tgt){var a=nowp/1000*.25;tx=Math.sin(a)*40;ty=SEAY+34;tz=Math.cos(a)*40;lx=0;ly=0;lz=-10}
  else if(S.watchCam===1){tx=0;ty=tgt.y+24;tz=tgt.z+52;lx=0;ly=tgt.y-2;lz=tgt.z-26}
  else{var back=17+(tgt.v>40?(tgt.v-40)*.15:0);tx=tgt.x;ty=tgt.y+5.2;tz=tgt.z+back;lx=tgt.x;ly=tgt.y+1;lz=tgt.z-28}
  var kk=tgt?1-Math.exp(-dt*6):.08;
  cam.position.x+=(tx-cam.position.x)*kk;cam.position.y+=(ty-cam.position.y)*kk;cam.position.z+=(tz-cam.position.z)*kk;
  cam.lookAt(lx,ly,lz);
  var fov=62+Math.min(18,Math.max(0,((tgt?tgt.v:0)-BASEV)*.45));
  if(Math.abs(cam.fov-fov)>.05){cam.fov+=(fov-cam.fov)*Math.min(1,dt*5);cam.updateProjectionMatrix()}
  updateWorld(dt);seasonUpdate(dt);
  // HUD & papan peringkat
  S.dt4-=dt;
  if(S.dt4<=0){
    S.dt4=.25;
    var run=NET.run,ended=!!(run&&run.status==="ended");
    if(tgt){
      $("pl-kmh").textContent=Math.round(tgt.v*3.6);$("pl-spdbar").style.width=clamp(tgt.v/MAXV*100,0,100)+"%";
      $("pl-speedfx").style.opacity=clamp((tgt.v-BASEV-6)/22,0,1);
      $("pl-left").innerHTML=Math.max(0,Math.ceil(S.L-tgt.dist))+'<small style="font-size:11px;color:#94a3b8"> m</small>';
      $("pl-dist").textContent=Math.min(Math.round(tgt.dist),S.L)+" / "+S.L+" m";
      $("pl-place").innerHTML="#"+(rk.indexOf(tgt)+1)+"<small>/"+rk.length+"</small>";
    }
    $("pl-time").textContent=ended?"SELESAI":fmt((Date.now()-((run&&run.t0)||Date.now()))/1000);
    S.racers.forEach(function(r){if(r.dot)r.dot.style.left=clamp(r.dist/S.L,0,1)*100+"%"});
    var k=$("pl-w-rank");
    if(k){
      k.innerHTML=rk.length?('<div style="font-weight:800;margin-bottom:3px">'+(ended?"🏁 Balapan diakhiri":"🏁 Peringkat langsung")+'</div>'+rk.slice(0,10).map(function(r,i){
        var pct=clamp(Math.round(r.dist/Math.max(1,S.L)*100),0,100);
        return'<div'+(r===tgt?' style="color:#fde047"':'')+'>'+(i+1)+'. <span style="color:'+r.color+'">●</span> '+esc(r.name)+' <span style="opacity:.75">'+(r.finished?"✔ "+fmt(r.finishT):pct+"%")+'</span></div>';
      }).join('')+(rk.length>10?'<div style="opacity:.6">+'+(rk.length-10)+' lainnya</div>':'')):"Menunggu pesawat siswa…";
    }
    var sg=rk.map(function(r){return r.pid}).join("|"),sel=$("pl-w-sel");
    if(sel&&sg!==S._wsig){
      S._wsig=sg;var cur=S.watchFollow||"";
      sel.innerHTML='<option value="">🥇 Ikuti pemimpin</option>'+rk.slice().sort(function(a,b){return String(a.name).localeCompare(String(b.name))}).map(function(r){return'<option value="'+esc(r.pid)+'">✈️ '+esc(r.name)+'</option>'}).join("");
      sel.value=cur;
    }
  }
}
function onPos(d){
  if(isTeacherNow()){ // guru: papan pantauan langsung
    var rn=NET.run;if(!rn||d.id!==rn.id)return;
    var nm=String(d.name||"?").slice(0,40),k=nk(nm);if(!k)return;
    rn.joined[k]=nm;rn.live[k]={name:nm,d:Number(d.d)||0,v:Number(d.v)||0,f:Number(d.f)||0,at:Date.now()};
    if(S.open&&S.mode==="watch"&&S.scene&&S.watchId===d.id)feedRemote(d);
    renderTSoft();return;
  }
  if(!S.open||!S.scene||!S.me||!S.auto||d.id!==S.auto)return;
  var key=String(d.pid);if(!key||key===myPid())return;
  var r=S.remote[key]||addRemote(d);if(!r)return;
  var nd0=Number(d.d)||0;
  if(nd0<r.nd-0.05&&!(Number(d.f)>0))return; // paket lama yang datang terlambat: abaikan
  r.nd=Math.max(r.nd,nd0);r.nv=clamp(Number(d.v)||0,0,MAXV+3);r.nat=performance.now();
  if(Number(d.f)>0)r.fin=Number(d.f);
}

/* siswa: perintah mulai dari guru */
function onCmd(d){
  if(d.a!=="start")return;
  if(!d.id||NET.handled[d.id])return;NET.handled[d.id]=1;
  if(S.open&&S.mode==="miss")closeRun(false);   // sempat dikira tertinggal, ternyata perintah baru sampai
  if(S.open)return;
  try{if(window.AESRun&&window.AESRun._state&&window.AESRun._state.open)window.AESRun.close()}catch(e){}
  try{if(window.AESCar&&window.AESCar._state&&window.AESCar._state.open)window.AESCar.close()}catch(e){}
  if(!getQs().length){pubRun(topicRes(),{a:"noq",id:d.id,pid:myPid(),name:myName()});note("Belum ada soal, balap pesawat belum bisa dimulai.");return}
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  S.auto=d.id;S.course=cKey(d.c);
  openRunCore("auto");
  pubRun(topicRes(),{a:"join",id:d.id,pid:myPid(),name:myName()});
}

/* siswa: status balapan dari guru (tersimpan di server, jadi terbaca juga saat buka aplikasi belakangan) */
function evalState(){
  var d=NET.state;if(!d||!d.id||!isStudentNow())return;
  var age=Date.now()-(Number(d.at)||0);
  if(d.st==="running"){
    if(age>10800000||NET.handled[d.id]||NET.missT===d.id)return;
    NET.missT=d.id;
    setTimeout(function(){ // beri waktu perintah mulai langsung tiba; kalau tidak, siswa ini tertinggal
      var c=NET.state;
      if(!c||c.id!==d.id||c.st!=="running"||NET.handled[d.id]||S.open||!isStudentNow())return;
      // status diterima langsung (bukan tersimpan di server) tetapi perintah mulai tidak sampai = paket hilang: tetap ikut
      if(NET.stLive){onCmd({a:"start",id:c.id,c:c.c});return}
      openMissed(c);
    },2500);
  }else if(d.st==="ended"){
    if(age>43200000)return;
    if(NET.finalShown===d.id&&S.open){if(NET.finalAt!==d.at)showFinalBoard(d);return}
    if(isSeen(d.id))return;
    if(S.open&&S.auto===d.id){
      if(S.state==="done"){if(S.resultShown)showFinalBoard(d);return}   // sudah finis: ganti ke papan hasil akhir
      if(!S.me)return;
      pubRun(topicRes(),{a:"dnf",id:d.id,pid:myPid(),name:myName(),ok:S.me.correct,bad:S.me.wrong});
      NET.myFin[d.id]=0;closeRun(false);openFinal(d);return;
    }
    if(NET.myFin[d.id])return;
    if(S.open&&S.mode==="miss"){showFinalBoard(d);return}
    if(S.open)return;
    openFinal(d);
  }
}
function applyCfg(d){S.course=cKey(d.c)}
function openMissed(d){
  if(S.open)return;
  applyCfg(d);
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  openRunCore("miss");
}
function openFinal(d){
  if(S.open)return;
  applyCfg(d);
  try{if(typeof closeBuildingModal==="function")closeBuildingModal()}catch(e){}
  openRunCore("final");showFinalBoard(d);
}
function showFinalBoard(d){
  setSeen(d.id);NET.finalShown=d.id;NET.finalAt=d.at;
  $("pl-miss").classList.add("pl-hide");$("pl-start").classList.add("pl-hide");
  var me=nk(myName()),rows=Array.isArray(d.rows)?d.rows:[];
  var fin=rows.filter(function(r){return r.s==="fin"}).sort(function(a,b){return a.t-b.t});
  var part=rows.filter(function(r){return r.s==="dnf"||r.s==="run"});
  var miss=rows.filter(function(r){return r.s==="miss"});
  var mine=null,rank=0;
  fin.forEach(function(r,i){if(nk(r.n)===me){mine=r;rank=i+1}});
  if(!mine)part.forEach(function(r){if(nk(r.n)===me)mine=r});
  var ok=mine?(Number(mine.ok)||0):0,bad=mine?(Number(mine.bad)||0):0,tot=ok+bad,ac=tot?Math.round(ok/tot*100):0;
  var st=mine?(mine.s==="fin"?"Selesai":"Belum selesai"):"Tidak ikut";
  var medal=rank===1?"🥇":rank===2?"🥈":rank===3?"🥉":"🏁";
  var cn=(COURSES[cKey(d.c)]||COURSES.m);
  $("pl-rtitle").textContent=rank?(medal+(rank===1?" JUARA 1!":" POSISI KE-"+rank)):"🏁 BALAPAN SUDAH SELESAI";
  $("pl-rsub").textContent="Jarak "+cn.name+" • "+cn.L+" m • balapan sudah diakhiri guru"+(mine?"":" • kamu tidak ikut, skormu 0");
  $("pl-rstats").innerHTML=
    "<div><b>"+(mine&&mine.s==="fin"?fmt(mine.t):"-")+"</b><span>WAKTU</span></div>"+
    "<div><b>"+ac+"%</b><span>AKURASI</span></div>"+
    "<div><b>"+(rank?("#"+rank+"/"+fin.length):"-")+"</b><span>POSISI</span></div>"+
    "<div><b style='color:#4ade80'>"+ok+"</b><span>BENAR</span></div>"+
    "<div><b style='color:#fb7185'>"+bad+"</b><span>SALAH</span></div>"+
    "<div><b style='color:#fdba74;font-size:12px'>"+st+"</b><span>STATUS</span></div>";
  function row(pl,r,tm){return'<div class="pl-row'+(nk(r.n)===me?" me":"")+'"><span class="pl">'+pl+'</span><span class="nm">'+esc(r.n)+(nk(r.n)===me?" (Kamu)":"")+'</span><span class="tm">'+tm+'</span></div>'}
  $("pl-rtable").innerHTML=
    fin.map(function(r,i){return row("#"+(i+1),r,fmt(r.t)+" • ✓"+(r.ok||0)+" ✗"+(r.bad||0))}).join("")+
    part.map(function(r){return row("…",r,"belum selesai")}).join("")+
    miss.map(function(r){return row("–",r,"tidak ikut")}).join("");
  $("pl-result").classList.remove("pl-hide");
}

/* guru: panel, status balapan & papan pantauan */
function openTPanel(){renderT();$("pl-tpanel").classList.remove("pl-hide");$("pl-launch").style.display="none"}
function onRes(d){
  var r=NET.run;if(!r||!d||d.id!==r.id)return;
  var nm=String(d.name||"?").slice(0,40),key=nk(nm);if(!key)return;
  if(d.a==="join"){r.joined[key]=nm}
  else if(d.a==="fin"){r.joined[key]=nm;r.fin[key]={name:nm,t:Number(d.t)||0,ok:Number(d.ok)||0,bad:Number(d.bad)||0};delete r.dnf[key]}
  else if(d.a==="dnf"){r.joined[key]=nm;if(!r.fin[key])r.dnf[key]={name:nm,ok:Number(d.ok)||0,bad:Number(d.bad)||0}}
  else if(d.a==="noq"){r.noq[key]=nm}
  renderT();pubState(false);
}
function buildRows(){
  var r=NET.run,rows=[],seen={};
  Object.keys(r.fin).forEach(function(k){var x=r.fin[k];rows.push({n:x.name,s:"fin",t:x.t,ok:x.ok,bad:x.bad});seen[k]=1});
  Object.keys(r.dnf).forEach(function(k){if(seen[k])return;var x=r.dnf[k];rows.push({n:x.name,s:"dnf",ok:x.ok,bad:x.bad});seen[k]=1});
  Object.keys(r.joined).forEach(function(k){if(seen[k])return;rows.push({n:r.joined[k],s:"run",ok:0,bad:0});seen[k]=1});
  if(r.status==="ended"){
    try{(gameConfig.students||[]).forEach(function(n){n=String(n||"").trim();if(n&&!seen[nk(n)]){rows.push({n:n.slice(0,40),s:"miss"});seen[nk(n)]=1}})}catch(e){}
  }
  return rows;
}
function pubState(now){
  clearTimeout(NET.pt);
  var go=function(){var r=NET.run;if(!r)return;pubRun(topicState(),{id:r.id,c:r.course,st:r.status,at:Date.now(),rows:buildRows()},true)};
  if(now)go();else NET.pt=setTimeout(go,400);
}
var _tT=0;
function renderTSoft(){var n=performance.now();if(n-_tT<600)return;_tT=n;renderT()}
function renderT(){
  var st=$("pl-t-stat"),tb=$("pl-t-table");if(!st||!tb)return;
  var r=NET.run;
  if(!r){st.textContent="Belum ada balapan yang dimulai.";tb.innerHTML="";return}
  var nj=Object.keys(r.joined).length,nf=Object.keys(r.fin).length,nq=Object.keys(r.noq).length;
  st.textContent=(r.status==="ended"?"🏁 BALAPAN DIAKHIRI • ":"✈️ BALAPAN BERJALAN • ")+(COURSES[r.course]||COURSES.m).name+" • "+r.L+" m • ikut: "+nj+" • selesai: "+nf+(nq?" • tanpa soal: "+nq:"");
  var now=Date.now(),items=[];
  Object.keys(r.joined).forEach(function(k){
    var f=r.fin[k],lv=r.live[k],dn=r.dnf[k];
    items.push({n:r.joined[k],t:f?f.t:(lv&&lv.f>0?lv.f:0),ok:f?f.ok:(dn?dn.ok:0),bad:f?f.bad:(dn?dn.bad:0),d:lv?lv.d:0,at:lv?lv.at:0,dnf:!!dn&&!f});
  });
  items.sort(function(a,b){if(a.t>0&&b.t>0)return a.t-b.t;if(a.t>0)return-1;if(b.t>0)return 1;return b.d-a.d});
  var html=items.map(function(x,i){
    var pct=x.t>0?100:clamp(Math.round(x.d/Math.max(1,r.L)*100),0,100);
    var lost=!x.t&&!x.dnf&&r.status!=="ended"&&x.at&&(now-x.at)>6000;
    var tm=x.t>0?(fmt(x.t)+" • ✓"+x.ok+" ✗"+x.bad):(x.dnf?"belum selesai":(pct+"%"+(lost?" ⚠":"")));
    return'<div class="pl-row"><span class="pl">#'+(i+1)+'</span><span class="nm">'+esc(x.n)+'<div class="pl-bar2"><i style="width:'+pct+'%"></i></div></span><span class="tm">'+tm+'</span></div>';
  }).join("");
  html+=buildRows().filter(function(x){return x.s==="miss"}).map(function(x){
    return'<div class="pl-row"><span class="pl">–</span><span class="nm">'+esc(x.n)+'</span><span class="tm">tidak ikut</span></div>';
  }).join("");
  tb.innerHTML=html;
}
setInterval(function(){try{var tp=$("pl-tpanel");if(isTeacherNow()&&tp&&!tp.classList.contains("pl-hide"))renderT()}catch(e){}},1500);

function segHandler(id,cb){
  $(id).addEventListener("click",function(e){
    var b=e.target.closest("button");if(!b)return;
    Array.prototype.forEach.call($(id).children,function(x){x.classList.remove("on")});b.classList.add("on");cb(b.dataset.v);
  });
}
segHandler("pl-seg-course",function(v){S.course=cKey(v);if(S.open&&S.state==="idle"){build3D();showBest()}});
segHandler("pl-seg-lvl",function(v){S.lvl=Number(v)||0});
window.addEventListener("keydown",onKey,true);
window.addEventListener("resize",onResize);
$("pl-exit").onclick=function(){closeRun(true)};
$("pl-close1").onclick=function(){closeRun(false)};
$("pl-close2").onclick=function(){closeRun(false)};
$("pl-go").onclick=startRace;
$("pl-again").onclick=function(){$("pl-result").classList.add("pl-hide");build3D();showStart()};

/* ---------- tombol & pilihan panel guru ---------- */
segHandler("pl-t-seg-course",function(v){NET.tCourse=cKey(v)});
$("pl-t-go").onclick=function(){
  if(!isTeacherNow())return;
  if(!getQs().length){note("Belum ada soal. Isi soal dulu di kolom Edit pada halaman awal.");return}
  var id="p"+Date.now().toString(36)+Math.floor(Math.random()*1000);
  var prev=NET.run,course=NET.tCourse;
  NET.run={id:id,course:course,L:COURSES[course].L,status:"running",joined:{},fin:{},dnf:{},noq:{},live:{},t0:Date.now()};
  bindNet();
  if(!pubRun(topicState(),{id:id,c:course,st:"running",at:Date.now(),rows:[]},true)){NET.run=prev;renderT();note("Belum tersambung ke server kelas. Coba lagi sebentar lagi.");return}
  pubRun(topicCmd(),{a:"start",id:id,c:course});
  renderT();note("📣 Balap pesawat dimulai di layar siswa!");
};
$("pl-t-stop").onclick=function(){
  if(!isTeacherNow())return;
  var r=NET.run;if(!r||r.status==="ended"){note("Belum ada balapan yang berjalan.");return}
  if(!confirm("Akhiri balapan dan umumkan skor ke semua siswa? Siswa yang masih terbang akan dihentikan."))return;
  r.status="ended";renderT();pubState(true);note("🏁 Balapan diakhiri. Skor ditampilkan ke siswa.");
};
$("pl-t-docx").onclick=function(){
  var r=NET.run;if(!r){alert("Belum ada balapan yang dimulai.");return}
  var items=[];
  Object.keys(r.joined).forEach(function(k){
    var f=r.fin[k],lv=r.live[k],dn=r.dnf[k];
    items.push({n:r.joined[k],t:f?f.t:(lv&&lv.f>0?lv.f:0),ok:f?f.ok:(dn?dn.ok:null),bad:f?f.bad:(dn?dn.bad:null),d:lv?lv.d:0});
  });
  items.sort(function(a,b){if(a.t>0&&b.t>0)return a.t-b.t;if(a.t>0)return-1;if(b.t>0)return 1;return b.d-a.d});
  var list=items.map(function(x){
    var done=x.t>0,pct=done?100:clamp(Math.round(x.d/Math.max(1,r.L)*100),0,100);
    return{n:x.n,st:done?"Selesai":"Belum selesai",time:done?fmt(x.t):"-",ok:x.ok,bad:x.bad,prog:pct+"%"};
  });
  buildRows().filter(function(x){return x.s==="miss"}).forEach(function(x){list.push({n:x.n,st:"Tidak ikut",time:"-",ok:null,bad:null,prog:"-"})});
  window.aesRaceDocx({title:"Nilai Balap Pesawat AES CLASS",fname:"Nilai_Balap_Pesawat_"+window.aesRaceStamp()+".docx",
    info:["Rute: "+(COURSES[r.course]||COURSES.m).name+" ("+r.L+" m)","Target soal: "+(r.course==="s"?8:r.course==="l"?16:12)+" jawaban benar untuk finis","Status: "+(r.status==="ended"?"balapan sudah diakhiri":"balapan masih berjalan")+" • ikut: "+Object.keys(r.joined).length+" • selesai: "+Object.keys(r.fin).length],
    rows:list});
};
$("pl-t-watch").onclick=function(){if(isTeacherNow())openWatch()};
$("pl-t-self").onclick=function(){if(isTeacherNow())openRunCore()};
$("pl-t-close").onclick=function(){$("pl-tpanel").classList.add("pl-hide")};
$("pl-close3").onclick=function(){closeRun(false)};

window.AESPlane={open:openRun,close:function(){closeRun(false)},_state:S};
})();
</script>

<script id="aes-rich-tools">
(function(){
var T=null,SY=[["Matematika","± × ÷ ≠ ≈ ≤ ≥ < > √ ∛ π ∞ ∑ ∏ ∫ ∂ ∆ ∇ ° ′ ″ % ‰ ∠ ⊥ ∥ ∈ ∉ ⊂ ⊃ ∪ ∩ ∅ ∴ ∵ ∝ ⌊ ⌋ ⌈ ⌉"],["Pangkat, indeks, pecahan","⁰ ¹ ² ³ ⁴ ⁵ ⁶ ⁷ ⁸ ⁹ ⁺ ⁻ ⁿ ₀ ₁ ₂ ₃ ₄ ₅ ₆ ₇ ₈ ₉ ₊ ₋ ½ ¼ ¾ ⅓ ⅔ ⅛"],["Huruf Yunani","α β γ δ ε ζ η θ λ μ ν ξ π ρ σ τ φ χ ψ ω Γ Δ Θ Λ Ξ Π Σ Φ Ψ Ω"],["Panah dan logika","→ ← ↑ ↓ ↔ ⇒ ⇐ ⇔ ⇌ ∀ ∃ ¬ ∧ ∨ ⊕ ✓ ✗ ★ ☆ ● ■ ▲ ▼ ◆"],["Satuan dan mata uang","° ℃ ℉ µ Ω Å € £ ¥ ₹ ₩ ₽ ₫ № © ® ™"],["Kimia","H₂O CO₂ O₂ NaCl H₂SO₄ → ⇌ ⁺ ⁻ Δ ↑ ↓"],["Aksen Latin (Prancis, Spanyol, Jerman, dll.)","á à â ä ã å æ ç é è ê ë í ì î ï ñ ó ò ô ö õ ø œ ú ù û ü ý ÿ ß Á É Í Ó Ú Ñ Ü Ö Ä ¿ ¡ « » ‹ ›"],["Huruf Cyrillic (Rusia)","а б в г д е ё ж з и й к л м н о п р с т у ф х ц ч ш щ ъ ы ь э ю я"]];
function isEd(el){if(!el||!el.closest||!el.closest("#questions-editor-list,#buildings-editor-list"))return false;if(el.tagName==="TEXTAREA")return true;if(el.tagName!=="INPUT"||el.type!=="text")return false;return (el.getAttribute("oninput")||"").indexOf("updateBuildingName")<0}
document.addEventListener("focusin",function(e){if(isEd(e.target))T=e.target});
function ins(txt){
  if(!T||!document.contains(T)){alert("Klik dulu kolom materi, soal, atau pilihan jawaban tempat kamu ingin menyisipkan.");return}
  var a=T.selectionStart==null?T.value.length:T.selectionStart,b=T.selectionEnd==null?a:T.selectionEnd;
  if(T.tagName==="TEXTAREA"&&txt.charAt(0)==="["&&a>0&&T.value.charAt(a-1)!=="\n")txt="\n"+txt;
  T.value=T.value.slice(0,a)+txt+T.value.slice(b);var p=a+txt.length;try{T.setSelectionRange(p,p)}catch(e){}
  T.dispatchEvent(new Event("input",{bubbles:true}));T.focus();
}
function askUrl(msg){
  var u=prompt(msg);if(!u)return null;u=u.trim();
  if(!/^https?:\/\//i.test(u)){alert("Alamat harus diawali http:// atau https://");return null}
  return u;
}
function preview(){
  if(!T||!document.contains(T)){alert("Klik dulu kolom yang ingin dilihat pratinjaunya.");return}
  var o=document.getElementById("aes-prev");if(o)o.remove();
  o=document.createElement("div");o.id="aes-prev";
  o.innerHTML='<div class="bx"></div>';
  o.querySelector(".bx").innerHTML=formatRichEducationalText(T.value,1)||"<i>(kosong)</i>";
  o.onclick=function(e){if(e.target===o)o.remove()};
  document.body.appendChild(o);
  try{triggerMathJaxRender([o])}catch(e){}
}
function symPanel(box){
  if(box.dataset.on){box.innerHTML="";box.dataset.on="";return}
  box.dataset.on="1";
  box.innerHTML=SY.map(function(g){return '<div class="g"><div class="gl">'+g[0]+'</div>'+g[1].split(" ").map(function(c){return '<button type="button" data-s="'+c+'">'+c+'</button>'}).join("")+'</div>'}).join("")+
   '<div class="gl" style="margin-top:4px">Rumus: tulis di antara tanda dolar, misalnya $x^2+1$ atau $\\frac{a}{b}$. Huruf Arab, Jepang, Mandarin, Korea, Hindi, Thai, dan lainnya cukup diketik atau ditempel langsung.</div>';
}
function mkBar(before){
  if(!before||before.previousElementSibling&&before.previousElementSibling.classList.contains("aes-ins-bar"))return;
  var bar=document.createElement("div");bar.className="aes-ins-bar";
  bar.innerHTML='<span>Sisipkan ke kolom yang dipilih:</span><button type="button" data-a="img">🖼 Gambar</button><button type="button" data-a="link">🔗 Tautan</button><button type="button" data-a="vid">▶ Video</button><button type="button" data-a="sym">Ω Simbol</button><button type="button" data-a="prev">👁 Pratinjau</button><div class="aes-sym"></div>';
  bar.addEventListener("mousedown",function(e){if(e.target.closest("button"))e.preventDefault()});
  bar.addEventListener("click",function(e){
    var b=e.target.closest("button");if(!b)return;
    if(b.dataset.s){ins(b.dataset.s);return}
    var a=b.dataset.a,u;
    if(a==="img"){u=askUrl("Tempel alamat (URL) gambar.\nContoh: https://situs.com/gambar.png");if(u)ins("[img:"+u+"]")}
    else if(a==="link"){u=askUrl("Tempel alamat (URL) tautan:");if(!u)return;var x=prompt("Teks yang ditampilkan (boleh dikosongkan):");x=(x||"").replace(/[\[\]\n]/g," ").trim();ins(x?"["+x+"]("+u+")":u)}
    else if(a==="vid"){u=askUrl("Tempel alamat (URL) video.\nYouTube, Vimeo, Google Drive, atau file .mp4/.webm:");if(u)ins("[video:"+u+"]")}
    else if(a==="sym")symPanel(bar.querySelector(".aes-sym"));
    else if(a==="prev")preview();
  });
  before.parentNode.insertBefore(bar,before);
}
function init(){mkBar(document.getElementById("buildings-editor-list"));mkBar(document.getElementById("questions-editor-list"))}
if(document.readyState==="loading")document.addEventListener("DOMContentLoaded",init);else init();
// rumus pada soal koin gedung (isi soal dibuat ulang dinamis)
try{var qb=document.getElementById("building-quiz-box");if(qb)new MutationObserver(function(){try{triggerMathJaxRender([qb])}catch(e){}}).observe(qb,{childList:true,subtree:true})}catch(e){}
})();
</script>
<script id="aes-share-reset">/* ===== AES CLASS • Bagikan Link (panjang, pendek, barcode) + Reset Link ===== */
(function(){var M={},C={};function req(p){p=p.replace(/^\.\//,'./');if(C[p])return C[p].exports;var m={exports:{}};C[p]=m;M[p](m,m.exports,req);return m.exports;}
M['./QR8bitByte']=function(module,exports,require){var QRMode = require('./QRMode');

function QR8bitByte(data) {
	this.mode = QRMode.MODE_8BIT_BYTE;
	this.data = data;
}

QR8bitByte.prototype = {

	getLength : function() {
		return this.data.length;
	},
	
	write : function(buffer) {
		for (var i = 0; i < this.data.length; i++) {

			buffer.put(this.data.charCodeAt(i), 8);
		}
	}
};

module.exports = QR8bitByte;

};
M['./QRMode']=function(module,exports,require){module.exports = {
    MODE_NUMBER :       1 << 0,
    MODE_ALPHA_NUM :    1 << 1,
    MODE_8BIT_BYTE :    1 << 2,
    MODE_KANJI :        1 << 3
};

};
M['./QRErrorCorrectLevel']=function(module,exports,require){module.exports = {
	L : 1,
	M : 0,
	Q : 3,
	H : 2
};


};
M['./QRMaskPattern']=function(module,exports,require){module.exports = {
	PATTERN000 : 0,
	PATTERN001 : 1,
	PATTERN010 : 2,
	PATTERN011 : 3,
	PATTERN100 : 4,
	PATTERN101 : 5,
	PATTERN110 : 6,
	PATTERN111 : 7
};

};
M['./QRMath']=function(module,exports,require){var QRMath = {

	glog : function(n) {
	
		if (n < 1) {
			throw new Error("glog(" + n + ")");
		}
		
		return QRMath.LOG_TABLE[n];
	},
	
	gexp : function(n) {
	
		while (n < 0) {
			n += 255;
		}
	
		while (n >= 256) {
			n -= 255;
		}
	
		return QRMath.EXP_TABLE[n];
	},
	
	EXP_TABLE : new Array(256),
	
	LOG_TABLE : new Array(256)

};
	
for (var i = 0; i < 8; i++) {
	QRMath.EXP_TABLE[i] = 1 << i;
}
for (var i = 8; i < 256; i++) {
	QRMath.EXP_TABLE[i] = QRMath.EXP_TABLE[i - 4]
		^ QRMath.EXP_TABLE[i - 5]
		^ QRMath.EXP_TABLE[i - 6]
		^ QRMath.EXP_TABLE[i - 8];
}
for (var i = 0; i < 255; i++) {
	QRMath.LOG_TABLE[QRMath.EXP_TABLE[i] ] = i;
}

module.exports = QRMath;

};
M['./QRPolynomial']=function(module,exports,require){var QRMath = require('./QRMath');

function QRPolynomial(num, shift) {
	if (num.length === undefined) {
		throw new Error(num.length + "/" + shift);
	}

	var offset = 0;

	while (offset < num.length && num[offset] === 0) {
		offset++;
	}

	this.num = new Array(num.length - offset + shift);
	for (var i = 0; i < num.length - offset; i++) {
		this.num[i] = num[i + offset];
	}
}

QRPolynomial.prototype = {

	get : function(index) {
		return this.num[index];
	},
	
	getLength : function() {
		return this.num.length;
	},
	
	multiply : function(e) {
	
		var num = new Array(this.getLength() + e.getLength() - 1);
	
		for (var i = 0; i < this.getLength(); i++) {
			for (var j = 0; j < e.getLength(); j++) {
				num[i + j] ^= QRMath.gexp(QRMath.glog(this.get(i) ) + QRMath.glog(e.get(j) ) );
			}
		}
	
		return new QRPolynomial(num, 0);
	},
	
	mod : function(e) {
	
		if (this.getLength() - e.getLength() < 0) {
			return this;
		}
	
		var ratio = QRMath.glog(this.get(0) ) - QRMath.glog(e.get(0) );
	
		var num = new Array(this.getLength() );
		
		for (var i = 0; i < this.getLength(); i++) {
			num[i] = this.get(i);
		}
		
		for (var x = 0; x < e.getLength(); x++) {
			num[x] ^= QRMath.gexp(QRMath.glog(e.get(x) ) + ratio);
		}

		return new QRPolynomial(num, 0).mod(e);
	}
};

module.exports = QRPolynomial;

};
M['./QRRSBlock']=function(module,exports,require){var QRErrorCorrectLevel = require('./QRErrorCorrectLevel');

function QRRSBlock(totalCount, dataCount) {
	this.totalCount = totalCount;
	this.dataCount  = dataCount;
}

QRRSBlock.RS_BLOCK_TABLE = [





	[1, 26, 19],
	[1, 26, 16],
	[1, 26, 13],
	[1, 26, 9],

	[1, 44, 34],
	[1, 44, 28],
	[1, 44, 22],
	[1, 44, 16],

	[1, 70, 55],
	[1, 70, 44],
	[2, 35, 17],
	[2, 35, 13],

	[1, 100, 80],
	[2, 50, 32],
	[2, 50, 24],
	[4, 25, 9],

	[1, 134, 108],
	[2, 67, 43],
	[2, 33, 15, 2, 34, 16],
	[2, 33, 11, 2, 34, 12],

	[2, 86, 68],
	[4, 43, 27],
	[4, 43, 19],
	[4, 43, 15],

	[2, 98, 78],
	[4, 49, 31],
	[2, 32, 14, 4, 33, 15],
	[4, 39, 13, 1, 40, 14],

	[2, 121, 97],
	[2, 60, 38, 2, 61, 39],
	[4, 40, 18, 2, 41, 19],
	[4, 40, 14, 2, 41, 15],

	[2, 146, 116],
	[3, 58, 36, 2, 59, 37],
	[4, 36, 16, 4, 37, 17],
	[4, 36, 12, 4, 37, 13],

	[2, 86, 68, 2, 87, 69],
	[4, 69, 43, 1, 70, 44],
	[6, 43, 19, 2, 44, 20],
	[6, 43, 15, 2, 44, 16],

	[4, 101, 81],
	[1, 80, 50, 4, 81, 51],
	[4, 50, 22, 4, 51, 23],
	[3, 36, 12, 8, 37, 13],

	[2, 116, 92, 2, 117, 93],
	[6, 58, 36, 2, 59, 37],
	[4, 46, 20, 6, 47, 21],
	[7, 42, 14, 4, 43, 15],

	[4, 133, 107],
	[8, 59, 37, 1, 60, 38],
	[8, 44, 20, 4, 45, 21],
	[12, 33, 11, 4, 34, 12],

	[3, 145, 115, 1, 146, 116],
	[4, 64, 40, 5, 65, 41],
	[11, 36, 16, 5, 37, 17],
	[11, 36, 12, 5, 37, 13],

	[5, 109, 87, 1, 110, 88],
	[5, 65, 41, 5, 66, 42],
	[5, 54, 24, 7, 55, 25],
	[11, 36, 12],

	[5, 122, 98, 1, 123, 99],
	[7, 73, 45, 3, 74, 46],
	[15, 43, 19, 2, 44, 20],
	[3, 45, 15, 13, 46, 16],

	[1, 135, 107, 5, 136, 108],
	[10, 74, 46, 1, 75, 47],
	[1, 50, 22, 15, 51, 23],
	[2, 42, 14, 17, 43, 15],

	[5, 150, 120, 1, 151, 121],
	[9, 69, 43, 4, 70, 44],
	[17, 50, 22, 1, 51, 23],
	[2, 42, 14, 19, 43, 15],

	[3, 141, 113, 4, 142, 114],
	[3, 70, 44, 11, 71, 45],
	[17, 47, 21, 4, 48, 22],
	[9, 39, 13, 16, 40, 14],

	[3, 135, 107, 5, 136, 108],
	[3, 67, 41, 13, 68, 42],
	[15, 54, 24, 5, 55, 25],
	[15, 43, 15, 10, 44, 16],

	[4, 144, 116, 4, 145, 117],
	[17, 68, 42],
	[17, 50, 22, 6, 51, 23],
	[19, 46, 16, 6, 47, 17],

	[2, 139, 111, 7, 140, 112],
	[17, 74, 46],
	[7, 54, 24, 16, 55, 25],
	[34, 37, 13],

	[4, 151, 121, 5, 152, 122],
	[4, 75, 47, 14, 76, 48],
	[11, 54, 24, 14, 55, 25],
	[16, 45, 15, 14, 46, 16],

	[6, 147, 117, 4, 148, 118],
	[6, 73, 45, 14, 74, 46],
	[11, 54, 24, 16, 55, 25],
	[30, 46, 16, 2, 47, 17],

	[8, 132, 106, 4, 133, 107],
	[8, 75, 47, 13, 76, 48],
	[7, 54, 24, 22, 55, 25],
	[22, 45, 15, 13, 46, 16],

	[10, 142, 114, 2, 143, 115],
	[19, 74, 46, 4, 75, 47],
	[28, 50, 22, 6, 51, 23],
	[33, 46, 16, 4, 47, 17],

	[8, 152, 122, 4, 153, 123],
	[22, 73, 45, 3, 74, 46],
	[8, 53, 23, 26, 54, 24],
	[12, 45, 15, 28, 46, 16],

	[3, 147, 117, 10, 148, 118],
	[3, 73, 45, 23, 74, 46],
	[4, 54, 24, 31, 55, 25],
	[11, 45, 15, 31, 46, 16],

	[7, 146, 116, 7, 147, 117],
	[21, 73, 45, 7, 74, 46],
	[1, 53, 23, 37, 54, 24],
	[19, 45, 15, 26, 46, 16],

	[5, 145, 115, 10, 146, 116],
	[19, 75, 47, 10, 76, 48],
	[15, 54, 24, 25, 55, 25],
	[23, 45, 15, 25, 46, 16],

	[13, 145, 115, 3, 146, 116],
	[2, 74, 46, 29, 75, 47],
	[42, 54, 24, 1, 55, 25],
	[23, 45, 15, 28, 46, 16],

	[17, 145, 115],
	[10, 74, 46, 23, 75, 47],
	[10, 54, 24, 35, 55, 25],
	[19, 45, 15, 35, 46, 16],

	[17, 145, 115, 1, 146, 116],
	[14, 74, 46, 21, 75, 47],
	[29, 54, 24, 19, 55, 25],
	[11, 45, 15, 46, 46, 16],

	[13, 145, 115, 6, 146, 116],
	[14, 74, 46, 23, 75, 47],
	[44, 54, 24, 7, 55, 25],
	[59, 46, 16, 1, 47, 17],

	[12, 151, 121, 7, 152, 122],
	[12, 75, 47, 26, 76, 48],
	[39, 54, 24, 14, 55, 25],
	[22, 45, 15, 41, 46, 16],

	[6, 151, 121, 14, 152, 122],
	[6, 75, 47, 34, 76, 48],
	[46, 54, 24, 10, 55, 25],
	[2, 45, 15, 64, 46, 16],

	[17, 152, 122, 4, 153, 123],
	[29, 74, 46, 14, 75, 47],
	[49, 54, 24, 10, 55, 25],
	[24, 45, 15, 46, 46, 16],

	[4, 152, 122, 18, 153, 123],
	[13, 74, 46, 32, 75, 47],
	[48, 54, 24, 14, 55, 25],
	[42, 45, 15, 32, 46, 16],

	[20, 147, 117, 4, 148, 118],
	[40, 75, 47, 7, 76, 48],
	[43, 54, 24, 22, 55, 25],
	[10, 45, 15, 67, 46, 16],

	[19, 148, 118, 6, 149, 119],
	[18, 75, 47, 31, 76, 48],
	[34, 54, 24, 34, 55, 25],
	[20, 45, 15, 61, 46, 16]
];

QRRSBlock.getRSBlocks = function(typeNumber, errorCorrectLevel) {
	
	var rsBlock = QRRSBlock.getRsBlockTable(typeNumber, errorCorrectLevel);
	
	if (rsBlock === undefined) {
		throw new Error("bad rs block @ typeNumber:" + typeNumber + "/errorCorrectLevel:" + errorCorrectLevel);
	}

	var length = rsBlock.length / 3;
	
	var list = [];
	
	for (var i = 0; i < length; i++) {

		var count = rsBlock[i * 3 + 0];
		var totalCount = rsBlock[i * 3 + 1];
		var dataCount  = rsBlock[i * 3 + 2];

		for (var j = 0; j < count; j++) {
			list.push(new QRRSBlock(totalCount, dataCount) );	
		}
	}
	
	return list;
};

QRRSBlock.getRsBlockTable = function(typeNumber, errorCorrectLevel) {

	switch(errorCorrectLevel) {
	case QRErrorCorrectLevel.L :
		return QRRSBlock.RS_BLOCK_TABLE[(typeNumber - 1) * 4 + 0];
	case QRErrorCorrectLevel.M :
		return QRRSBlock.RS_BLOCK_TABLE[(typeNumber - 1) * 4 + 1];
	case QRErrorCorrectLevel.Q :
		return QRRSBlock.RS_BLOCK_TABLE[(typeNumber - 1) * 4 + 2];
	case QRErrorCorrectLevel.H :
		return QRRSBlock.RS_BLOCK_TABLE[(typeNumber - 1) * 4 + 3];
	default :
		return undefined;
	}
};

module.exports = QRRSBlock;

};
M['./QRBitBuffer']=function(module,exports,require){function QRBitBuffer() {
	this.buffer = [];
	this.length = 0;
}

QRBitBuffer.prototype = {

	get : function(index) {
		var bufIndex = Math.floor(index / 8);
		return ( (this.buffer[bufIndex] >>> (7 - index % 8) ) & 1) == 1;
	},
	
	put : function(num, length) {
		for (var i = 0; i < length; i++) {
			this.putBit( ( (num >>> (length - i - 1) ) & 1) == 1);
		}
	},
	
	getLengthInBits : function() {
		return this.length;
	},
	
	putBit : function(bit) {
	
		var bufIndex = Math.floor(this.length / 8);
		if (this.buffer.length <= bufIndex) {
			this.buffer.push(0);
		}
	
		if (bit) {
			this.buffer[bufIndex] |= (0x80 >>> (this.length % 8) );
		}
	
		this.length++;
	}
};

module.exports = QRBitBuffer;

};
M['./QRUtil']=function(module,exports,require){var QRMode = require('./QRMode');
var QRPolynomial = require('./QRPolynomial');
var QRMath = require('./QRMath');
var QRMaskPattern = require('./QRMaskPattern');

var QRUtil = {

    PATTERN_POSITION_TABLE : [
        [],
        [6, 18],
        [6, 22],
        [6, 26],
        [6, 30],
        [6, 34],
        [6, 22, 38],
        [6, 24, 42],
        [6, 26, 46],
        [6, 28, 50],
        [6, 30, 54],        
        [6, 32, 58],
        [6, 34, 62],
        [6, 26, 46, 66],
        [6, 26, 48, 70],
        [6, 26, 50, 74],
        [6, 30, 54, 78],
        [6, 30, 56, 82],
        [6, 30, 58, 86],
        [6, 34, 62, 90],
        [6, 28, 50, 72, 94],
        [6, 26, 50, 74, 98],
        [6, 30, 54, 78, 102],
        [6, 28, 54, 80, 106],
        [6, 32, 58, 84, 110],
        [6, 30, 58, 86, 114],
        [6, 34, 62, 90, 118],
        [6, 26, 50, 74, 98, 122],
        [6, 30, 54, 78, 102, 126],
        [6, 26, 52, 78, 104, 130],
        [6, 30, 56, 82, 108, 134],
        [6, 34, 60, 86, 112, 138],
        [6, 30, 58, 86, 114, 142],
        [6, 34, 62, 90, 118, 146],
        [6, 30, 54, 78, 102, 126, 150],
        [6, 24, 50, 76, 102, 128, 154],
        [6, 28, 54, 80, 106, 132, 158],
        [6, 32, 58, 84, 110, 136, 162],
        [6, 26, 54, 82, 110, 138, 166],
        [6, 30, 58, 86, 114, 142, 170]
    ],

    G15 : (1 << 10) | (1 << 8) | (1 << 5) | (1 << 4) | (1 << 2) | (1 << 1) | (1 << 0),
    G18 : (1 << 12) | (1 << 11) | (1 << 10) | (1 << 9) | (1 << 8) | (1 << 5) | (1 << 2) | (1 << 0),
    G15_MASK : (1 << 14) | (1 << 12) | (1 << 10)    | (1 << 4) | (1 << 1),

    getBCHTypeInfo : function(data) {
        var d = data << 10;
        while (QRUtil.getBCHDigit(d) - QRUtil.getBCHDigit(QRUtil.G15) >= 0) {
            d ^= (QRUtil.G15 << (QRUtil.getBCHDigit(d) - QRUtil.getBCHDigit(QRUtil.G15) ) );    
        }
        return ( (data << 10) | d) ^ QRUtil.G15_MASK;
    },

    getBCHTypeNumber : function(data) {
        var d = data << 12;
        while (QRUtil.getBCHDigit(d) - QRUtil.getBCHDigit(QRUtil.G18) >= 0) {
            d ^= (QRUtil.G18 << (QRUtil.getBCHDigit(d) - QRUtil.getBCHDigit(QRUtil.G18) ) );    
        }
        return (data << 12) | d;
    },

    getBCHDigit : function(data) {

        var digit = 0;

        while (data !== 0) {
            digit++;
            data >>>= 1;
        }

        return digit;
    },

    getPatternPosition : function(typeNumber) {
        return QRUtil.PATTERN_POSITION_TABLE[typeNumber - 1];
    },

    getMask : function(maskPattern, i, j) {
        
        switch (maskPattern) {
            
        case QRMaskPattern.PATTERN000 : return (i + j) % 2 === 0;
        case QRMaskPattern.PATTERN001 : return i % 2 === 0;
        case QRMaskPattern.PATTERN010 : return j % 3 === 0;
        case QRMaskPattern.PATTERN011 : return (i + j) % 3 === 0;
        case QRMaskPattern.PATTERN100 : return (Math.floor(i / 2) + Math.floor(j / 3) ) % 2 === 0;
        case QRMaskPattern.PATTERN101 : return (i * j) % 2 + (i * j) % 3 === 0;
        case QRMaskPattern.PATTERN110 : return ( (i * j) % 2 + (i * j) % 3) % 2 === 0;
        case QRMaskPattern.PATTERN111 : return ( (i * j) % 3 + (i + j) % 2) % 2 === 0;

        default :
            throw new Error("bad maskPattern:" + maskPattern);
        }
    },

    getErrorCorrectPolynomial : function(errorCorrectLength) {

        var a = new QRPolynomial([1], 0);

        for (var i = 0; i < errorCorrectLength; i++) {
            a = a.multiply(new QRPolynomial([1, QRMath.gexp(i)], 0) );
        }

        return a;
    },

    getLengthInBits : function(mode, type) {

        if (1 <= type && type < 10) {


            switch(mode) {
            case QRMode.MODE_NUMBER     : return 10;
            case QRMode.MODE_ALPHA_NUM  : return 9;
            case QRMode.MODE_8BIT_BYTE  : return 8;
            case QRMode.MODE_KANJI      : return 8;
            default :
                throw new Error("mode:" + mode);
            }

        } else if (type < 27) {


            switch(mode) {
            case QRMode.MODE_NUMBER     : return 12;
            case QRMode.MODE_ALPHA_NUM  : return 11;
            case QRMode.MODE_8BIT_BYTE  : return 16;
            case QRMode.MODE_KANJI      : return 10;
            default :
                throw new Error("mode:" + mode);
            }

        } else if (type < 41) {


            switch(mode) {
            case QRMode.MODE_NUMBER     : return 14;
            case QRMode.MODE_ALPHA_NUM  : return 13;
            case QRMode.MODE_8BIT_BYTE  : return 16;
            case QRMode.MODE_KANJI      : return 12;
            default :
                throw new Error("mode:" + mode);
            }

        } else {
            throw new Error("type:" + type);
        }
    },

    getLostPoint : function(qrCode) {
        
        var moduleCount = qrCode.getModuleCount();
        var lostPoint = 0;
        var row = 0; 
        var col = 0;

        
        for (row = 0; row < moduleCount; row++) {

            for (col = 0; col < moduleCount; col++) {

                var sameCount = 0;
                var dark = qrCode.isDark(row, col);

                for (var r = -1; r <= 1; r++) {

                    if (row + r < 0 || moduleCount <= row + r) {
                        continue;
                    }

                    for (var c = -1; c <= 1; c++) {

                        if (col + c < 0 || moduleCount <= col + c) {
                            continue;
                        }

                        if (r === 0 && c === 0) {
                            continue;
                        }

                        if (dark === qrCode.isDark(row + r, col + c) ) {
                            sameCount++;
                        }
                    }
                }

                if (sameCount > 5) {
                    lostPoint += (3 + sameCount - 5);
                }
            }
        }


        for (row = 0; row < moduleCount - 1; row++) {
            for (col = 0; col < moduleCount - 1; col++) {
                var count = 0;
                if (qrCode.isDark(row,     col    ) ) count++;
                if (qrCode.isDark(row + 1, col    ) ) count++;
                if (qrCode.isDark(row,     col + 1) ) count++;
                if (qrCode.isDark(row + 1, col + 1) ) count++;
                if (count === 0 || count === 4) {
                    lostPoint += 3;
                }
            }
        }


        for (row = 0; row < moduleCount; row++) {
            for (col = 0; col < moduleCount - 6; col++) {
                if (qrCode.isDark(row, col) && 
                        !qrCode.isDark(row, col + 1) && 
                         qrCode.isDark(row, col + 2) && 
                         qrCode.isDark(row, col + 3) && 
                         qrCode.isDark(row, col + 4) && 
                        !qrCode.isDark(row, col + 5) && 
                         qrCode.isDark(row, col + 6) ) {
                    lostPoint += 40;
                }
            }
        }

        for (col = 0; col < moduleCount; col++) {
            for (row = 0; row < moduleCount - 6; row++) {
                if (qrCode.isDark(row, col) &&
                        !qrCode.isDark(row + 1, col) &&
                         qrCode.isDark(row + 2, col) &&
                         qrCode.isDark(row + 3, col) &&
                         qrCode.isDark(row + 4, col) &&
                        !qrCode.isDark(row + 5, col) &&
                         qrCode.isDark(row + 6, col) ) {
                    lostPoint += 40;
                }
            }
        }

        
        var darkCount = 0;

        for (col = 0; col < moduleCount; col++) {
            for (row = 0; row < moduleCount; row++) {
                if (qrCode.isDark(row, col) ) {
                    darkCount++;
                }
            }
        }
        
        var ratio = Math.abs(100 * darkCount / moduleCount / moduleCount - 50) / 5;
        lostPoint += ratio * 10;

        return lostPoint;       
    }

};

module.exports = QRUtil;

};
M['./index']=function(module,exports,require){

















var QR8bitByte = require('./QR8bitByte');
var QRUtil = require('./QRUtil');
var QRPolynomial = require('./QRPolynomial');
var QRRSBlock = require('./QRRSBlock');
var QRBitBuffer = require('./QRBitBuffer');

function QRCode(typeNumber, errorCorrectLevel) {
	this.typeNumber = typeNumber;
	this.errorCorrectLevel = errorCorrectLevel;
	this.modules = null;
	this.moduleCount = 0;
	this.dataCache = null;
	this.dataList = [];
}

QRCode.prototype = {
	
	addData : function(data) {
		var newData = new QR8bitByte(data);
		this.dataList.push(newData);
		this.dataCache = null;
	},
	
	isDark : function(row, col) {
		if (row < 0 || this.moduleCount <= row || col < 0 || this.moduleCount <= col) {
			throw new Error(row + "," + col);
		}
		return this.modules[row][col];
	},

	getModuleCount : function() {
		return this.moduleCount;
	},
	
	make : function() {

		if (this.typeNumber < 1 ){
			var typeNumber = 1;
			for (typeNumber = 1; typeNumber < 40; typeNumber++) {
				var rsBlocks = QRRSBlock.getRSBlocks(typeNumber, this.errorCorrectLevel);

				var buffer = new QRBitBuffer();
				var totalDataCount = 0;
				for (var i = 0; i < rsBlocks.length; i++) {
					totalDataCount += rsBlocks[i].dataCount;
				}

				for (var x = 0; x < this.dataList.length; x++) {
					var data = this.dataList[x];
					buffer.put(data.mode, 4);
					buffer.put(data.getLength(), QRUtil.getLengthInBits(data.mode, typeNumber) );
					data.write(buffer);
				}
				if (buffer.getLengthInBits() <= totalDataCount * 8)
					break;
			}
			this.typeNumber = typeNumber;
		}
		this.makeImpl(false, this.getBestMaskPattern() );
	},
	
	makeImpl : function(test, maskPattern) {
		
		this.moduleCount = this.typeNumber * 4 + 17;
		this.modules = new Array(this.moduleCount);
		
		for (var row = 0; row < this.moduleCount; row++) {
			
			this.modules[row] = new Array(this.moduleCount);
			
			for (var col = 0; col < this.moduleCount; col++) {
				this.modules[row][col] = null;//(col + row) % 3;
			}
		}
	
		this.setupPositionProbePattern(0, 0);
		this.setupPositionProbePattern(this.moduleCount - 7, 0);
		this.setupPositionProbePattern(0, this.moduleCount - 7);
		this.setupPositionAdjustPattern();
		this.setupTimingPattern();
		this.setupTypeInfo(test, maskPattern);
		
		if (this.typeNumber >= 7) {
			this.setupTypeNumber(test);
		}
	
		if (this.dataCache === null) {
			this.dataCache = QRCode.createData(this.typeNumber, this.errorCorrectLevel, this.dataList);
		}
	
		this.mapData(this.dataCache, maskPattern);
	},

	setupPositionProbePattern : function(row, col)  {
		
		for (var r = -1; r <= 7; r++) {
			
			if (row + r <= -1 || this.moduleCount <= row + r) continue;
			
			for (var c = -1; c <= 7; c++) {
				
				if (col + c <= -1 || this.moduleCount <= col + c) continue;
				
				if ( (0 <= r && r <= 6 && (c === 0 || c === 6) ) || 
                     (0 <= c && c <= 6 && (r === 0 || r === 6) ) || 
                     (2 <= r && r <= 4 && 2 <= c && c <= 4) ) {
					this.modules[row + r][col + c] = true;
				} else {
					this.modules[row + r][col + c] = false;
				}
			}		
		}		
	},
	
	getBestMaskPattern : function() {
	
		var minLostPoint = 0;
		var pattern = 0;
	
		for (var i = 0; i < 8; i++) {
			
			this.makeImpl(true, i);
	
			var lostPoint = QRUtil.getLostPoint(this);
	
			if (i === 0 || minLostPoint >  lostPoint) {
				minLostPoint = lostPoint;
				pattern = i;
			}
		}
	
		return pattern;
	},
	
	createMovieClip : function(target_mc, instance_name, depth) {
	
		var qr_mc = target_mc.createEmptyMovieClip(instance_name, depth);
		var cs = 1;
	
		this.make();

		for (var row = 0; row < this.modules.length; row++) {
			
			var y = row * cs;
			
			for (var col = 0; col < this.modules[row].length; col++) {
	
				var x = col * cs;
				var dark = this.modules[row][col];
			
				if (dark) {
					qr_mc.beginFill(0, 100);
					qr_mc.moveTo(x, y);
					qr_mc.lineTo(x + cs, y);
					qr_mc.lineTo(x + cs, y + cs);
					qr_mc.lineTo(x, y + cs);
					qr_mc.endFill();
				}
			}
		}
		
		return qr_mc;
	},

	setupTimingPattern : function() {
		
		for (var r = 8; r < this.moduleCount - 8; r++) {
			if (this.modules[r][6] !== null) {
				continue;
			}
			this.modules[r][6] = (r % 2 === 0);
		}
	
		for (var c = 8; c < this.moduleCount - 8; c++) {
			if (this.modules[6][c] !== null) {
				continue;
			}
			this.modules[6][c] = (c % 2 === 0);
		}
	},
	
	setupPositionAdjustPattern : function() {
	
		var pos = QRUtil.getPatternPosition(this.typeNumber);
		
		for (var i = 0; i < pos.length; i++) {
		
			for (var j = 0; j < pos.length; j++) {
			
				var row = pos[i];
				var col = pos[j];
				
				if (this.modules[row][col] !== null) {
					continue;
				}
				
				for (var r = -2; r <= 2; r++) {
				
					for (var c = -2; c <= 2; c++) {
					
						if (Math.abs(r) === 2 || 
                            Math.abs(c) === 2 ||
                            (r === 0 && c === 0) ) {
							this.modules[row + r][col + c] = true;
						} else {
							this.modules[row + r][col + c] = false;
						}
					}
				}
			}
		}
	},
	
	setupTypeNumber : function(test) {
	
		var bits = QRUtil.getBCHTypeNumber(this.typeNumber);
        var mod;
	
		for (var i = 0; i < 18; i++) {
			mod = (!test && ( (bits >> i) & 1) === 1);
			this.modules[Math.floor(i / 3)][i % 3 + this.moduleCount - 8 - 3] = mod;
		}
	
		for (var x = 0; x < 18; x++) {
			mod = (!test && ( (bits >> x) & 1) === 1);
			this.modules[x % 3 + this.moduleCount - 8 - 3][Math.floor(x / 3)] = mod;
		}
	},
	
	setupTypeInfo : function(test, maskPattern) {
	
		var data = (this.errorCorrectLevel << 3) | maskPattern;
		var bits = QRUtil.getBCHTypeInfo(data);
        var mod;

		for (var v = 0; v < 15; v++) {
	
			mod = (!test && ( (bits >> v) & 1) === 1);
	
			if (v < 6) {
				this.modules[v][8] = mod;
			} else if (v < 8) {
				this.modules[v + 1][8] = mod;
			} else {
				this.modules[this.moduleCount - 15 + v][8] = mod;
			}
		}

		for (var h = 0; h < 15; h++) {
	
			mod = (!test && ( (bits >> h) & 1) === 1);
			
			if (h < 8) {
				this.modules[8][this.moduleCount - h - 1] = mod;
			} else if (h < 9) {
				this.modules[8][15 - h - 1 + 1] = mod;
			} else {
				this.modules[8][15 - h - 1] = mod;
			}
		}

		this.modules[this.moduleCount - 8][8] = (!test);
	
	},
	
	mapData : function(data, maskPattern) {
		
		var inc = -1;
		var row = this.moduleCount - 1;
		var bitIndex = 7;
		var byteIndex = 0;
		
		for (var col = this.moduleCount - 1; col > 0; col -= 2) {
	
			if (col === 6) col--;
	
			while (true) {
	
				for (var c = 0; c < 2; c++) {
					
					if (this.modules[row][col - c] === null) {
						
						var dark = false;
	
						if (byteIndex < data.length) {
							dark = ( ( (data[byteIndex] >>> bitIndex) & 1) === 1);
						}
	
						var mask = QRUtil.getMask(maskPattern, row, col - c);
	
						if (mask) {
							dark = !dark;
						}
						
						this.modules[row][col - c] = dark;
						bitIndex--;
	
						if (bitIndex === -1) {
							byteIndex++;
							bitIndex = 7;
						}
					}
				}
								
				row += inc;
	
				if (row < 0 || this.moduleCount <= row) {
					row -= inc;
					inc = -inc;
					break;
				}
			}
		}
		
	}

};

QRCode.PAD0 = 0xEC;
QRCode.PAD1 = 0x11;

QRCode.createData = function(typeNumber, errorCorrectLevel, dataList) {
	
	var rsBlocks = QRRSBlock.getRSBlocks(typeNumber, errorCorrectLevel);
	
	var buffer = new QRBitBuffer();
	
	for (var i = 0; i < dataList.length; i++) {
		var data = dataList[i];
		buffer.put(data.mode, 4);
		buffer.put(data.getLength(), QRUtil.getLengthInBits(data.mode, typeNumber) );
		data.write(buffer);
	}

	var totalDataCount = 0;
	for (var x = 0; x < rsBlocks.length; x++) {
		totalDataCount += rsBlocks[x].dataCount;
	}

	if (buffer.getLengthInBits() > totalDataCount * 8) {
		throw new Error("code length overflow. (" + 
            buffer.getLengthInBits() + 
            ">" +  
            totalDataCount * 8 + 
            ")");
	}

	if (buffer.getLengthInBits() + 4 <= totalDataCount * 8) {
		buffer.put(0, 4);
	}

	while (buffer.getLengthInBits() % 8 !== 0) {
		buffer.putBit(false);
	}

	while (true) {
		
		if (buffer.getLengthInBits() >= totalDataCount * 8) {
			break;
		}
		buffer.put(QRCode.PAD0, 8);
		
		if (buffer.getLengthInBits() >= totalDataCount * 8) {
			break;
		}
		buffer.put(QRCode.PAD1, 8);
	}

	return QRCode.createBytes(buffer, rsBlocks);
};

QRCode.createBytes = function(buffer, rsBlocks) {

	var offset = 0;
	
	var maxDcCount = 0;
	var maxEcCount = 0;
	
	var dcdata = new Array(rsBlocks.length);
	var ecdata = new Array(rsBlocks.length);
	
	for (var r = 0; r < rsBlocks.length; r++) {

		var dcCount = rsBlocks[r].dataCount;
		var ecCount = rsBlocks[r].totalCount - dcCount;

		maxDcCount = Math.max(maxDcCount, dcCount);
		maxEcCount = Math.max(maxEcCount, ecCount);
		
		dcdata[r] = new Array(dcCount);
		
		for (var i = 0; i < dcdata[r].length; i++) {
			dcdata[r][i] = 0xff & buffer.buffer[i + offset];
		}
		offset += dcCount;
		
		var rsPoly = QRUtil.getErrorCorrectPolynomial(ecCount);
		var rawPoly = new QRPolynomial(dcdata[r], rsPoly.getLength() - 1);

		var modPoly = rawPoly.mod(rsPoly);
		ecdata[r] = new Array(rsPoly.getLength() - 1);
		for (var x = 0; x < ecdata[r].length; x++) {
            var modIndex = x + modPoly.getLength() - ecdata[r].length;
			ecdata[r][x] = (modIndex >= 0)? modPoly.get(modIndex) : 0;
		}

	}
	
	var totalCodeCount = 0;
	for (var y = 0; y < rsBlocks.length; y++) {
		totalCodeCount += rsBlocks[y].totalCount;
	}

	var data = new Array(totalCodeCount);
	var index = 0;

	for (var z = 0; z < maxDcCount; z++) {
		for (var s = 0; s < rsBlocks.length; s++) {
			if (z < dcdata[s].length) {
				data[index++] = dcdata[s][z];
			}
		}
	}

	for (var xx = 0; xx < maxEcCount; xx++) {
		for (var t = 0; t < rsBlocks.length; t++) {
			if (xx < ecdata[t].length) {
				data[index++] = ecdata[t][xx];
			}
		}
	}

	return data;

};

module.exports = QRCode;

};
var QRCode=req('./index');var EC=req('./QRErrorCorrectLevel');
window.AesQR={make:function(t,lvl){var best=null;for(var v=2;v<=40;v++){try{var q=new QRCode(v,EC[lvl||'M']);q.addData(t);q.make();best=q;break}catch(e){}}if(!best)return null;var n=best.getModuleCount(),r=[];for(var i=0;i<n;i++){var row=[];for(var j=0;j<n;j++)row.push(best.isDark(i,j)?1:0);r.push(row)}return r}};})();
(function(){
var PK="aes_pending_revoke_v1";

/* ---------- Barcode (QR) ---------- */
function drawQr(canvas,text,target){
  if(!canvas||!window.AesQR)return false;
  var m=window.AesQR.make(text,"M");if(!m)return false;
  var n=m.length,q=4,sc=Math.max(2,Math.floor((target||480)/(n+2*q))),size=(n+2*q)*sc;
  canvas.width=size;canvas.height=size;
  var c=canvas.getContext("2d");c.fillStyle="#ffffff";c.fillRect(0,0,size,size);c.fillStyle="#000000";
  for(var r=0;r<n;r++)for(var k=0;k<n;k++)if(m[r][k])c.fillRect((k+q)*sc,(r+q)*sc,sc,sc);
  return true;
}
function shortLink(){return aesBuildStudentLink(true)}

window.aesRefreshShareUI=function(){
  try{
    if(typeof isTeacherMode==="undefined"||!isTeacherMode)return;
    var inp=document.getElementById("generated-link-short");if(!inp)return;
    var l=shortLink();inp.value=l;
    drawQr(document.getElementById("aes-qr-canvas"),l,480);
  }catch(e){console.error(e)}
};
window.aesShareRefreshSoon=function(){clearTimeout(window._aesShT);window._aesShT=setTimeout(window.aesRefreshShareUI,30)};

function markShared(){try{_aesLinkShared=true}catch(e){}try{aesPubCfgNow()}catch(e){}}
function copyText(txt,okMsg){
  function fallback(){
    var t=document.createElement("textarea");t.value=txt;t.style.cssText="position:fixed;left:-9999px;top:0";
    document.body.appendChild(t);t.select();try{document.execCommand("copy")}catch(e){}t.remove();alert(okMsg);
  }
  try{
    if(navigator.clipboard&&navigator.clipboard.writeText)navigator.clipboard.writeText(txt).then(function(){alert(okMsg)},fallback);
    else fallback();
  }catch(e){fallback()}
}
window.aesCopyShortLink=function(){
  try{playSoundEffect("click")}catch(e){}
  try{syncFormToConfig()}catch(e){}
  window.aesRefreshShareUI();markShared();
  var inp=document.getElementById("generated-link-short");
  if(inp){try{inp.select()}catch(e){}copyText(inp.value,"Link pendek berhasil disalin!")}
};
window.aesDownloadQr=function(){
  try{playSoundEffect("click")}catch(e){}
  window.aesRefreshShareUI();markShared();
  var cv=document.getElementById("aes-qr-canvas");if(!cv)return;
  cv.toBlob(function(b){
    if(!b)return;var a=document.createElement("a");a.href=URL.createObjectURL(b);
    a.download="barcode-siswa-"+roomId+".png";document.body.appendChild(a);a.click();
    setTimeout(function(){URL.revokeObjectURL(a.href);a.remove()},1500);
  },"image/png");
};
window.aesShowQrBig=function(){
  try{playSoundEffect("click")}catch(e){}
  try{syncFormToConfig()}catch(e){}
  window.aesRefreshShareUI();markShared();
  var old=document.getElementById("aes-qr-modal");if(old)old.remove();
  var d=document.createElement("div");d.id="aes-qr-modal";
  d.style.cssText="position:fixed;inset:0;z-index:2147483000;background:rgba(2,6,23,.94);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:14px;padding:16px;cursor:pointer;font-family:inherit";
  var box=document.createElement("div");box.style.cssText="background:#fff;padding:10px;border-radius:18px";
  var cv=document.createElement("canvas");cv.style.cssText="display:block;width:min(72vmin,520px);height:min(72vmin,520px);image-rendering:pixelated";
  drawQr(cv,shortLink(),900);box.appendChild(cv);
  var t1=document.createElement("div");t1.textContent="Scan barcode ini dengan kamera HP untuk masuk kelas";t1.style.cssText="color:#e2e8f0;font-weight:800;font-size:clamp(14px,2.4vmin,22px);text-align:center";
  var t2=document.createElement("div");t2.textContent=shortLink();t2.style.cssText="color:#7dd3fc;font:600 clamp(11px,1.8vmin,15px) monospace;text-align:center;word-break:break-all;max-width:90vw";
  var t3=document.createElement("div");t3.textContent="(klik di mana saja untuk menutup)";t3.style.cssText="color:#94a3b8;font-size:12px";
  d.appendChild(box);d.appendChild(t1);d.appendChild(t2);d.appendChild(t3);
  d.onclick=function(){d.remove()};document.body.appendChild(d);
};

/* ---------- Mematikan link lama (revoke) ---------- */
function pend(){try{return JSON.parse(localStorage.getItem(PK)||"[]")||[]}catch(e){return[]}}
function savePend(L){try{localStorage.setItem(PK,JSON.stringify(L))}catch(e){}}
function pendAdd(r){var L=pend().filter(function(x){return x.r!==r});L.push({r:r,t:Date.now(),n:0});savePend(L)}
function pendDel(r){savePend(pend().filter(function(x){return x.r!==r}))}
function pendBump(r){savePend(pend().map(function(x){if(x.r===r)x.n=(x.n||0)+1;return x}))}

/* publikasikan tanda "dicabut" ke semua server; cb(hasil, urlYangDipakaiSekarang) */
window.aesRevokeRoom=function(room,cb){
  var cur="";try{cur=aesBrokerUrl()}catch(e){}
  var urls=[];if(cur)urls.push(cur);
  try{AES_BROKERS.forEach(function(b){if(urls.indexOf(b.url)<0)urls.push(b.url)})}catch(e){}
  var res={},left=urls.length;
  function fin(){if(--left<=0&&cb)cb(res,cur)}
  if(typeof mqtt==="undefined"||!urls.length){urls.forEach(function(u){res[u]=false});if(cb)cb(res,cur);return}
  urls.forEach(function(url){
    var done=false,c=null,tm=null;
    function end(ok){
      if(done)return;done=true;clearTimeout(tm);res[url]=!!ok;
      try{c&&c.end(true)}catch(e){}fin();
    }
    try{
      c=mqtt.connect(url,{clientId:"aes_rv_"+Math.random().toString(36).slice(2,9),clean:true,connectTimeout:5000,reconnectPeriod:0});
      c.on("connect",function(){
        c.publish("aes_class_3d/"+room+"/revoked",JSON.stringify({t:Date.now()}),{retain:true,qos:1},function(err){
          if(err){end(false);return}
          c.publish("aes_class_3d/"+room+"/config_sync","",{retain:true,qos:1},function(){end(true)});
        });
      });
      c.on("error",function(){end(false)});
      tm=setTimeout(function(){end(false)},7000);
    }catch(e){end(false)}
  });
};

function note(kind,txt){
  var n=document.getElementById("aes-reset-note");if(!n)return;
  var col={ok:["#064e3b","#6ee7b7","#10b981"],warn:["#78350f","#fcd34d","#f59e0b"],err:["#7f1d1d","#fca5a5","#ef4444"],wait:["#1e293b","#cbd5e1","#64748b"]}[kind];
  n.style.cssText="display:block;background:"+col[0]+";color:"+col[1]+";border:1px solid "+col[2]+";";
  n.textContent=txt;
}
function revokeAndReport(room){
  pendAdd(room);
  note("wait","⏳ Mematikan link lama di server…");
  window.aesRevokeRoom(room,function(res,cur){
    if(res[cur]){
      pendDel(room);
      note("ok","✅ Link baru sudah dibuat. Link lama (link panjang, link pendek, dan barcode) sudah dimatikan; siswa yang masih di link lama akan dikeluarkan. Bagikan link/barcode yang baru.");
    }else{
      var any=Object.keys(res).some(function(k){return res[k]});
      note(any?"warn":"err","⚠️ Link baru sudah dibuat, tetapi link lama BELUM bisa dimatikan di server yang sedang dipakai (internet/server bermasalah). Biarkan halaman ini terbuka; sistem akan mencoba lagi otomatis.");
    }
  });
}
window.aesRevokeIfLive=function(){
  if(typeof isTeacherMode==="undefined"||!isTeacherMode)return;
  if(typeof _tsLive==="undefined"||!_tsLive||!roomId||roomId==="aesclass-default")return;
  window._aesRevokedByReset=true;
  revokeAndReport(roomId);
};
function retryPending(){
  var L=pend().filter(function(x){return x&&x.r&&Date.now()-x.t<864e5&&(x.n||0)<8});savePend(L);
  L.forEach(function(x){
    if(typeof roomId!=="undefined"&&x.r===roomId)return;
    window.aesRevokeRoom(x.r,function(res,cur){if(res[cur])pendDel(x.r);else pendBump(x.r)});
  });
}
setTimeout(function(){try{if(typeof isTeacherMode!=="undefined"&&isTeacherMode)retryPending()}catch(e){}},5000);
setInterval(function(){try{if(typeof isTeacherMode!=="undefined"&&isTeacherMode&&pend().length)retryPending()}catch(e){}},60000);

window.aesResetLink=function(){
  if(typeof isTeacherMode==="undefined"||!isTeacherMode)return;
  if(!confirm("Reset link?\n\n• Link panjang, link pendek, dan barcode yang lama akan MATI.\n• Siswa yang sedang masuk akan dikeluarkan dan harus memakai link/barcode yang baru.\n• Soal dan pengaturan tetap tersimpan.\n• Kelas kembali ke tahap \"Menunggu guru memulai\".\n\nLanjutkan?"))return;
  try{playSoundEffect("click")}catch(e){}
  window._aesRevokedByReset=false;
  generateSessionAndLink();
  if(!window._aesRevokedByReset)note("ok","✅ Link baru sudah dibuat. Bagikan link/barcode yang baru ke siswa.");
};


/* ---------- Kode ruang unik: tidak pernah sama dengan link sebelumnya ---------- */
window.aesNewRoomId=function(){
  var HK="aes_room_history_v1",H=[];
  try{H=JSON.parse(localStorage.getItem(HK)||"[]")||[]}catch(e){}
  var cur=(typeof roomId!=="undefined")?roomId:"",id="",n=0;
  do{
    var a=new Uint32Array(2);
    try{crypto.getRandomValues(a)}catch(e){a[0]=Math.random()*4294967296;a[1]=Math.random()*4294967296}
    id="aes_"+a[0].toString(36).padStart(7,"0")+a[1].toString(36).padStart(7,"0");
    if(++n>50)id+=Date.now().toString(36);
  }while(id===cur||H.indexOf(id)>=0);
  H.push(id);if(cur&&H.indexOf(cur)<0)H.push(cur);
  try{localStorage.setItem(HK,JSON.stringify(H.slice(-300)))}catch(e){}
  return id;
};

/* ---------- Sisi siswa: link sudah dicabut ---------- */
window._aesRevoked=false;
window.aesRoomRevoked=function(){
  if(typeof isTeacherMode!=="undefined"&&isTeacherMode)return;
  window._aesRevoked=true;
  try{if(mqttClient)mqttClient.end(true)}catch(e){}
  try{clearInterval(mqttBroadcastLoop)}catch(e){}
  if(document.getElementById("aes-revoked-overlay"))return;
  var d=document.createElement("div");d.id="aes-revoked-overlay";
  d.style.cssText="position:fixed;inset:0;z-index:2147483646;background:#0f172a;color:#e2e8f0;display:flex;align-items:center;justify-content:center;text-align:center;padding:20px;font-family:'Plus Jakarta Sans',sans-serif";
  d.innerHTML='<div style="max-width:420px"><div style="font-size:48px">🔒</div><h2 style="font-size:20px;font-weight:800;margin:8px 0">Link ini sudah tidak berlaku</h2><p style="font-size:14px;line-height:1.6;color:#cbd5e1">Gurumu sudah membuat link baru. Minta <b>link atau barcode terbaru</b> dari gurumu, lalu buka lagi.</p></div>';
  document.body.appendChild(d);
};
})();
</script><style id="aes-race-compact">
/* === PERKECIL PANEL SOAL & JAWABAN: rn === */
#rn-qpanel{max-height:32vh;padding:6px 10px calc(6px + env(safe-area-inset-bottom,0px))}
#rn-qpanel .rn-qhead,#rn-qpanel .rn-qhead{font-size:12px;margin-bottom:3px}
#rn-qtext{font-size:clamp(13px,2.6vw,16px);line-height:1.25;margin-bottom:5px}
#rn-qtext img,#rn-qimg{max-height:70px;margin:2px auto}
#rn-opts{gap:5px}
.rn-opt{gap:6px;padding:4px 8px;min-height:38px;border-radius:10px;font:700 clamp(12px,2.4vw,15px) 'Plus Jakarta Sans',sans-serif}
.rn-opt b{width:24px;height:24px;border-radius:7px;font-size:13px}
.rn-opt img{max-height:56px}
#rn-fb{font-size:12px;min-height:14px;margin-top:3px}
@media (orientation:portrait){
 #rn-qpanel{max-height:36vh}
 #rn-qtext{font-size:clamp(14px,3.9vw,17px)}
 .rn-opt{min-height:44px;font:700 clamp(13px,3.7vw,16px) 'Plus Jakarta Sans',sans-serif}
}
@media (max-height:520px) and (orientation:landscape){
 #rn-qpanel{top:96px;width:min(42vw,420px);max-height:none;padding:6px 8px}
 .rn-opt{min-height:34px}
}

/* === PERKECIL PANEL SOAL & JAWABAN: cr === */
#cr-qpanel{max-height:32vh;padding:6px 10px calc(6px + env(safe-area-inset-bottom,0px))}
#cr-qpanel .rn-qhead,#cr-qpanel .cr-qhead{font-size:12px;margin-bottom:3px}
#cr-qtext{font-size:clamp(13px,2.6vw,16px);line-height:1.25;margin-bottom:5px}
#cr-qtext img,#cr-qimg{max-height:70px;margin:2px auto}
#cr-opts{gap:5px}
.cr-opt{gap:6px;padding:4px 8px;min-height:38px;border-radius:10px;font:700 clamp(12px,2.4vw,15px) 'Plus Jakarta Sans',sans-serif}
.cr-opt b{width:24px;height:24px;border-radius:7px;font-size:13px}
.cr-opt img{max-height:56px}
#cr-fb{font-size:12px;min-height:14px;margin-top:3px}
@media (orientation:portrait){
 #cr-qpanel{max-height:36vh}
 #cr-qtext{font-size:clamp(14px,3.9vw,17px)}
 .cr-opt{min-height:44px;font:700 clamp(13px,3.7vw,16px) 'Plus Jakarta Sans',sans-serif}
}
@media (max-height:520px) and (orientation:landscape){
 #cr-qpanel{top:96px;width:min(42vw,420px);max-height:none;padding:6px 8px}
 .cr-opt{min-height:34px}
}

/* === PERKECIL PANEL SOAL & JAWABAN: pl === */
#pl-qpanel{max-height:32vh;padding:6px 10px calc(6px + env(safe-area-inset-bottom,0px))}
#pl-qpanel .rn-qhead,#pl-qpanel .pl-qhead{font-size:12px;margin-bottom:3px}
#pl-qtext{font-size:clamp(13px,2.6vw,16px);line-height:1.25;margin-bottom:5px}
#pl-qtext img,#pl-qimg{max-height:70px;margin:2px auto}
#pl-opts{gap:5px}
.pl-opt{gap:6px;padding:4px 8px;min-height:38px;border-radius:10px;font:700 clamp(12px,2.4vw,15px) 'Plus Jakarta Sans',sans-serif}
.pl-opt b{width:24px;height:24px;border-radius:7px;font-size:13px}
.pl-opt img{max-height:56px}
#pl-fb{font-size:12px;min-height:14px;margin-top:3px}
@media (orientation:portrait){
 #pl-qpanel{max-height:36vh}
 #pl-qtext{font-size:clamp(14px,3.9vw,17px)}
 .pl-opt{min-height:44px;font:700 clamp(13px,3.7vw,16px) 'Plus Jakarta Sans',sans-serif}
}
@media (max-height:520px) and (orientation:landscape){
 #pl-qpanel{top:96px;width:min(42vw,420px);max-height:none;padding:6px 8px}
 .pl-opt{min-height:34px}
}
</style><style id="aes-race-portrait">/* === MODE POTRET HP: 3 game balapan === */
@media (orientation:portrait){
 #rn-hud{top:calc(6px + env(safe-area-inset-top,0px));left:6px;right:6px;gap:4px}
 .rn-card{padding:3px 8px;border-radius:11px}
 #rn-exit{width:36px;height:36px;border-radius:10px;font-size:15px}
 .rn-lbl{font-size:10px}
 #rn-kmh,#rn-place{font-size:22px}
 .rn-unit{font-size:11px}
 .rn-bar{min-width:60px;height:4px;margin-top:2px}
 #rn-time{font-size:12px}
 #rn-trackbar{height:12px;margin:0 8px 0 4px}
 #rn-trackbar .rn-dot{width:9px;height:9px}
 #rn-trackbar .rn-dot.me{width:13px;height:13px}
 #rn-trackbar .rn-flag{font-size:12px;top:-3px}
 #rn-dist{font-size:11px;margin-top:1px}
 #rn-wboard{left:6px;right:6px;top:auto;bottom:6px;width:auto;max-height:32vh;padding:6px}
 #rn-fx{top:24%;font-size:clamp(18px,5.5vw,30px)}
 #rn-count{top:18%;font-size:clamp(48px,16vw,100px)}
 .rn-modal{padding:8px}
 .rn-box{width:min(96vw,430px);max-height:90vh;padding:12px 12px 10px;border-radius:16px}
 .rn-box h2{font-size:19px}
 .rn-box p{font-size:12px;margin-bottom:6px}
 .rn-rules{font-size:13px;line-height:1.4;padding:6px 10px;margin-bottom:6px}
 .rn-sel{margin-bottom:6px}
 .rn-seg button{padding:7px 3px;font-size:12px}
 .rn-btn{padding:11px;font-size:15px}
 .rn-row{padding:6px 8px;font-size:13px;margin-bottom:3px}
 .rn-stats{margin:6px 0 8px}
 .rn-stats b{font-size:17px}

 #cr-hud{top:calc(6px + env(safe-area-inset-top,0px));left:6px;right:6px;gap:4px}
 .cr-card{padding:3px 8px;border-radius:11px}
 #cr-exit{width:36px;height:36px;border-radius:10px;font-size:15px}
 .cr-lbl{font-size:10px}
 #cr-kmh,#cr-place{font-size:22px}
 .cr-unit{font-size:11px}
 .cr-bar{min-width:60px;height:4px;margin-top:2px}
 #cr-time{font-size:12px}
 #cr-trackbar{height:12px;margin:0 8px 0 4px}
 #cr-trackbar .cr-dot{width:9px;height:9px}
 #cr-trackbar .cr-dot.me{width:13px;height:13px}
 #cr-trackbar .cr-flag{font-size:12px;top:-3px}
 #cr-dist{font-size:11px;margin-top:1px}
 #cr-wboard{left:6px;right:6px;top:auto;bottom:6px;width:auto;max-height:32vh;padding:6px}
 #cr-fx{top:24%;font-size:clamp(18px,5.5vw,30px)}
 #cr-count{top:18%;font-size:clamp(48px,16vw,100px)}
 .cr-modal{padding:8px}
 .cr-box{width:min(96vw,430px);max-height:90vh;padding:12px 12px 10px;border-radius:16px}
 .cr-box h2{font-size:19px}
 .cr-box p{font-size:12px;margin-bottom:6px}
 .cr-rules{font-size:13px;line-height:1.4;padding:6px 10px;margin-bottom:6px}
 .cr-sel{margin-bottom:6px}
 .cr-seg button{padding:7px 3px;font-size:12px}
 .cr-btn{padding:11px;font-size:15px}
 .cr-row{padding:6px 8px;font-size:13px;margin-bottom:3px}
 .cr-stats{margin:6px 0 8px}
 .cr-stats b{font-size:17px}

 #pl-hud{top:calc(6px + env(safe-area-inset-top,0px));left:6px;right:6px;gap:4px}
 .pl-card{padding:3px 8px;border-radius:11px}
 #pl-exit{width:36px;height:36px;border-radius:10px;font-size:15px}
 .pl-lbl{font-size:10px}
 #pl-kmh,#pl-place{font-size:22px}
 .pl-unit{font-size:11px}
 .pl-bar{min-width:60px;height:4px;margin-top:2px}
 #pl-time{font-size:12px}
 #pl-trackbar{height:12px;margin:0 8px 0 4px}
 #pl-trackbar .pl-dot{width:9px;height:9px}
 #pl-trackbar .pl-dot.me{width:13px;height:13px}
 #pl-trackbar .pl-flag{font-size:12px;top:-3px}
 #pl-dist{font-size:11px;margin-top:1px}
 #pl-wboard{left:6px;right:6px;top:auto;bottom:6px;width:auto;max-height:32vh;padding:6px}
 #pl-fx{top:24%;font-size:clamp(18px,5.5vw,30px)}
 #pl-count{top:18%;font-size:clamp(48px,16vw,100px)}
 .pl-modal{padding:8px}
 .pl-box{width:min(96vw,430px);max-height:90vh;padding:12px 12px 10px;border-radius:16px}
 .pl-box h2{font-size:19px}
 .pl-box p{font-size:12px;margin-bottom:6px}
 .pl-rules{font-size:13px;line-height:1.4;padding:6px 10px;margin-bottom:6px}
 .pl-sel{margin-bottom:6px}
 .pl-seg button{padding:7px 3px;font-size:12px}
 .pl-btn{padding:11px;font-size:15px}
 .pl-row{padding:6px 8px;font-size:13px;margin-bottom:3px}
 .pl-stats{margin:6px 0 8px}
 .pl-stats b{font-size:17px}

 #cr-mm{top:calc(90px + env(safe-area-inset-top,0px));right:6px;width:76px;height:76px;border-radius:12px}
 #cr-corner{top:calc(90px + env(safe-area-inset-top,0px));left:6px;max-width:calc(100% - 96px);font-size:12px;padding:4px 9px}
 #cr-lapcard #cr-lap{font-size:20px}

 #rn-launch,#cr-launch,#pl-launch{right:6px;padding:8px 11px;font-size:12px}
 #rn-launch{top:34%}#cr-launch{top:42%}#pl-launch{top:50%}
}
</style><script id="aes-qbag">
/* Kantong soal bersama untuk 3 game balapan (Lari, Mobil, Pesawat):
   soal yang sudah tampil di game mana pun tidak diulang sebelum semua soal tampil.
   Riwayat disimpan per perangkat siswa; otomatis mulai baru jika tidak dipakai > 6 jam. */
(function(){
var KEY="aes_race_seen_v1",TTL=6*3600*1000,mem=null;
function keyOf(q){var t=String(q&&q.q||"")+"\u0001"+((q&&q.options)||[]).join("\u0001"),h=5381;for(var i=0;i<t.length;i++)h=((h<<5)+h+t.charCodeAt(i))|0;return(h>>>0).toString(36)+t.length}
function load(){
  var d=null;
  try{d=JSON.parse(localStorage.getItem(KEY)||"null")}catch(e){}
  if(!d)d=mem;
  if(!d||!d.seen||Date.now()-(d.t||0)>TTL)d={t:Date.now(),seen:{}};
  return d;
}
function save(d){d.t=Date.now();mem=d;try{localStorage.setItem(KEY,JSON.stringify(d))}catch(e){}}
function shuf(a){for(var i=a.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1)),t=a[i];a[i]=a[j];a[j]=t}return a}
window.AESQBag={
  order:function(qs){
    var d=load(),keys=qs.map(keyOf),cur={},un=[],sn=[];
    keys.forEach(function(k){cur[k]=1});
    Object.keys(d.seen).forEach(function(k){if(!cur[k])delete d.seen[k]});
    qs.forEach(function(_,i){(d.seen[keys[i]]?sn:un).push(i)});
    if(!un.length){d.seen={};un=sn;sn=[]}
    save(d);
    return shuf(un).concat(shuf(sn));
  },
  mark:function(q){var d=load();d.seen[keyOf(q)]=1;save(d)},
  reset:function(){mem=null;try{localStorage.removeItem(KEY)}catch(e){}}
};
})();
</script><style id="aes-plane-season">
#pl-season{position:absolute;top:21%;left:50%;transform:translateX(-50%) scale(.9);padding:6px 16px;border-radius:999px;background:rgba(15,23,42,.62);color:#fff;font:800 clamp(15px,4.2vw,22px) 'Plus Jakarta Sans',sans-serif;letter-spacing:.3px;opacity:0;pointer-events:none;z-index:6;white-space:nowrap;text-shadow:0 2px 6px rgba(0,0,0,.4)}
#pl-season.show{animation:plSeasonIn 2.1s ease forwards}
@keyframes plSeasonIn{0%{opacity:0;transform:translateX(-50%) scale(.8)}15%{opacity:1;transform:translateX(-50%) scale(1.05)}25%{transform:translateX(-50%) scale(1)}80%{opacity:1}100%{opacity:0;transform:translateX(-50%) scale(1)}}
</style></body></html>
