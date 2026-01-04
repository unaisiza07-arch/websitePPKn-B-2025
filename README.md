<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PPKn-B 2025 | Final Galactic Portal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@900&family=Space+Grotesk:wght@300;500;700&display=swap');
        
        body { 
            font-family: 'Space Grotesk', sans-serif;
            background: #080a0f;
            color: #ffffff;
            min-height: 100vh;
            margin: 0;
            overflow-x: hidden;
        }

        .constellation-bg {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: -1;
            background: radial-gradient(circle at center, #0d121d 0%, #05070a 100%);
        }

        .star-field {
            position: absolute;
            width: 100%; height: 100%;
            background-image: radial-gradient(white 1px, transparent 1px);
            background-size: 60px 60px;
            opacity: 0.25;
        }

        .nav-layout {
            background: rgba(10, 15, 25, 0.95);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            display: grid;
            grid-template-columns: 1fr 2fr 1fr;
            align-items: center;
            padding: 0 40px;
        }

        .fish-unj-text {
            font-weight: 900;
            letter-spacing: 2px;
            background: linear-gradient(to right, #ff4b2b, #ff416c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-size: 14px;
        }

        .galaxy-title {
            font-family: 'Cinzel', serif;
            background: linear-gradient(to bottom, #fff, #86a8e7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .card-solid {
            background: #11141b;
            border: 1px solid #2d333b;
            border-radius: 12px;
            position: relative;
            text-align: center;
            transition: all 0.3s ease;
        }
        .card-solid:hover { transform: translateY(-5px); border-color: #3b82f6; }

        .pj-locked { cursor: default !important; pointer-events: none; }
        .pj-avatar { 
            background: url('https://pixabay.com/id/illustrations/tanda-tanya-pertanyaan-tanda-2061539/') center/cover !important;
            filter: contrast(1.2) brightness(0.8);
        }

        .desc-box {
            background: #0a0c10 !important;
            border: 1px solid #30363d !important;
            border-radius: 8px;
            padding: 10px;
            color: #d1d5db;
            font-size: 12px;
            margin-top: 10px;
            width: 100%;
        }

        .btn-del {
            position: absolute; top: -8px; right: -8px;
            background: #f85149; width: 22px; height: 22px;
            border-radius: 50%; font-size: 10px;
            display: flex; align-items: center; justify-content: center;
            z-index: 50; cursor: pointer; opacity: 0; transition: 0.2s;
        }
        .card-solid:hover .btn-del:not(.hidden) { opacity: 1; }

        .section-active { display: block; animation: fadeIn 0.4s ease-out; }
        .section-hidden { display: none; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body>

    <div class="constellation-bg"><div class="star-field"></div></div>

    <nav class="fixed top-0 w-full z-50 nav-layout h-20">
        <div class="flex items-center gap-4">
            <div class="w-10 h-10 border border-gray-700 rounded-md overflow-hidden bg-gray-900 cursor-pointer" onclick="document.getElementById('in-logo').click()">
                <img id="logo-img" class="w-full h-full object-cover hidden">
                <p id="logo-txt" class="text-[7px] text-center mt-3 opacity-40 uppercase font-bold text-white">Logo</p>
            </div>
            <input type="file" id="in-logo" class="hidden" onchange="saveImg(event, 'logo-data', 'logo-img', 'logo-txt')">
            <span class="fish-unj-text">Fakultas Ilmu Sosial dan Hukum</span>
        </div>

        <div class="text-center">
            <h2 class="galaxy-title text-xl md:text-2xl tracking-[0.3em]">PPKn-B 2025</h2>
        </div>

        <div class="flex justify-end gap-6">
            <button onclick="show('beranda')" class="text-[10px] font-bold text-blue-300 uppercase hover:text-white transition">Home</button>
            <button onclick="show('struktur')" class="text-[10px] font-bold text-blue-300 uppercase hover:text-white transition">Astronot</button>
            <button onclick="show('anggota')" class="text-[10px] font-bold text-blue-300 uppercase hover:text-white transition">Orbit</button>
            <button onclick="show('album')" class="text-[10px] font-bold text-blue-300 uppercase hover:text-white transition">Nebula</button>
        </div>
    </nav>

    <main class="pt-32 px-6 pb-20 max-w-7xl mx-auto relative z-10">

        <section id="beranda" class="section-active">
            <h2 class="text-cyan-400 text-2xl font-bold uppercase tracking-[0.2em] text-center mb-8">Selamat datang di ruang PPKn B 2025</h2>
            <div class="card-solid p-4 max-w-5xl mx-auto aspect-video mb-16 group">
                <div class="btn-del !w-10 !h-10 !text-xl group-hover:!opacity-100" onclick="delImg('h-img-data', 'h-img', 'l-h')">✕</div>
                <img id="h-img" class="w-full h-full object-cover rounded-xl hidden">
                <label id="l-h" class="absolute inset-0 flex items-center justify-center text-gray-500 font-bold cursor-pointer">UNGGAH COVER KELAS</label>
                <input type="file" class="hidden" id="in-h" onchange="saveImg(event, 'h-img-data', 'h-img', 'l-h')">
                <div onclick="document.getElementById('in-h').click()" class="absolute inset-0 cursor-pointer"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <div class="card-solid p-10 border-t-4 border-cyan-500 shadow-cyan-900/20">
                    <h3 class="font-bold text-cyan-400 text-xl mb-4 uppercase tracking-widest text-center">Visi Kosmik</h3>
                    <p class="text-gray-300 italic text-sm text-center">Menjadi komunitas pembelajar yang unggul secara intelektual, berintegritas dalam karakter, dan menjadi pelopor harmoni sosial berdasarkan nilai-nilai Pancasila.</p>
                </div>
                <div class="card-solid p-10 border-t-4 border-red-500 shadow-red-900/20">
                    <h3 class="font-bold text-red-500 text-xl mb-4 uppercase tracking-widest text-center">Misi Antarkita</h3>
                    <p class="text-gray-300 italic text-sm text-center">Membangun sistem pendukung di kelas di mana berbagi ilmu menjadi budaya, sehingga tidak ada kasta antara yang pintar dan yang kurang.</p>
                </div>
            </div>
        </section>

        <section id="struktur" class="section-hidden">
            <h2 class="galaxy-title text-4xl mb-16 uppercase text-center w-full">The Astronots</h2>
            <div id="cont-struktur" class="grid grid-cols-2 md:grid-cols-5 gap-8"></div>
        </section>

        <section id="anggota" class="section-hidden">
            <h2 class="galaxy-title text-4xl mb-16 uppercase text-center w-full">The Orbit</h2>
            <div id="cont-anggota" class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6"></div>
        </section>

        <section id="album" class="section-hidden">
            <h2 class="galaxy-title text-4xl mb-10 uppercase text-center w-full">Nebula Gallery</h2>
            <div class="flex justify-center mb-10"><button onclick="addPost()" class="bg-blue-600 px-10 py-2 rounded-full font-bold hover:bg-blue-500 transition shadow-lg shadow-blue-900/40">TAMBAH MEMORI</button></div>
            <div id="cont-album" class="grid grid-cols-1 md:grid-cols-3 gap-6"></div>
        </section>

    </main>

    <script>
        const astronots = [
            {n: "Fernando Yehezkiel Sihombing", j: "Ketua Kelas", lock: false}, 
            {n: "Jibri Al Fathir", j: "Wakil Ketua", lock: false}, 
            {n: "Cindy Nasywatul Maula", j: "Sekretaris", lock: false}, 
            {n: "Rosa Salsabila", j: "Bendahara", lock: false}, 
            {n: "Adalah Pokoknya", j: "PJ Matkul", lock: true}
        ];

        // Daftar Nama Lengkap Sesuai Input User (Sudah Alfabetis A-Z)
        const orbit = [
            "ADE LIA RAMADIANTI", "ANNISA TRI WULANDARI YUDANTI", "AZ ZAHRA SALSABILLA", 
            "BILQIS ISMI AZIZ", "CEYLLA ANGGITA INTANY", "CINDY NASYWATUL MAULA", 
            "DANIN MAHIRA", "DIVA AURA AISYAH", "FERNANDO YEHEZKIEL SIHOMBING", 
            "HAURA DZIKRA", "IBNU FADHIL", "IMMANUEL SHINE V SIMARE MARE", 
            "JIBRI AL FATHIR", "KAYLILA", "KEMAL RAMADHAN", "LEPIRA AMELIA", 
            "LISANA SIDQIN ALIYYA", "LOLI DANIELA PANGGABEAN", "MAHARGHA PUTRA WIYANA", 
            "MISION RENATA TOBING", "MOHAMAD BINTANG", "MOHAMAD FAISOL ZUHDI", 
            "MUAMAR KHADAFI", "MUHAMAD SHALPASYA PERDANA", "MUHAMMAD ADERO GUSTIA NASRULLAH", 
            "NADIRA RAMA DIYANTI", "NAILA ANINDA SAFITRI", "NAJI DEA KATON JATI MARYONO", 
            "NEYVA NURAINI PUTRI", "NUGROHO BAGUS SETIAJI", "RARA CAHAYA NINGSIH", 
            "RIVAEL PASARIBU", "ROSA SALSABILA", "SANDRO IMANUEL PANGGABEAN", 
            "SANIA NURAININ", "SASKIA LUKITA SARI", "SHASKHIYA AULIANDA RHAMDIANI", 
            "TSAKILLAH NUR SAYIDAH", "UNAIS RAZIN AHNAFI", "ZASKIA ROBIATUL ADAWIAH", 
            "ZATIA DWI ARYANTI"
        ];

        function saveImg(e, key, imgId, labelId) {
            const f = e.target.files[0];
            if(f) {
                const r = new FileReader();
                r.onload = (ev) => {
                    localStorage.setItem(key, ev.target.result);
                    loadImg(key, imgId, labelId);
                };
                r.readAsDataURL(f);
            }
        }

        function loadImg(key, imgId, labelId) {
            const data = localStorage.getItem(key);
            const img = document.getElementById(imgId);
            const lbl = document.getElementById(labelId);
            if(data && img) {
                img.src = data;
                img.classList.remove('hidden');
                if(lbl) lbl.classList.add('hidden');
            } else if(img) {
                img.classList.add('hidden');
                if(lbl) lbl.classList.remove('hidden');
            }
        }

        function delImg(key, imgId, labelId) {
            if(confirm("Hapus elemen ini?")) {
                localStorage.removeItem(key);
                loadImg(key, imgId, labelId);
            }
        }

        function show(id) {
            document.querySelectorAll('main > section').forEach(s => s.className = 'section-hidden');
            document.getElementById(id).className = 'section-active';
            window.scrollTo(0,0);
        }

        function addPost(savedId = null, savedText = '') {
            const id = savedId || 'post-' + Date.now();
            const div = document.createElement('div');
            div.className = 'card-solid p-4';
            div.id = id;
            div.innerHTML = `
                <div class="btn-del" onclick="removePost('${id}')">✕</div>
                <div class="relative w-full h-48 bg-black/40 rounded-lg overflow-hidden">
                    <img id="img-${id}" class="w-full h-full object-cover hidden">
                    <label id="lbl-${id}" class="absolute inset-0 flex items-center justify-center text-[10px] opacity-20">UNGGAH MEMORI</label>
                    <input type="file" class="hidden" onchange="saveImg(event, 'post-img-${id}', 'img-${id}', 'lbl-${id}'); saveAlbumData();">
                    <div onclick="this.previousElementSibling.click()" class="absolute inset-0 cursor-pointer"></div>
                </div>
                <textarea oninput="saveAlbumData()" class="desc-box" placeholder="Tulis cerita nebula ini...">${savedText}</textarea>
            `;
            document.getElementById('cont-album').prepend(div);
            loadImg('post-img-' + id, 'img-' + id, 'lbl-' + id);
        }

        function removePost(id) {
            if(confirm("Hapus memori?")) {
                localStorage.removeItem('post-img-' + id);
                document.getElementById(id).remove();
                saveAlbumData();
            }
        }

        function saveAlbumData() {
            const posts = [];
            document.querySelectorAll('#cont-album > div').forEach(el => {
                posts.push({ id: el.id, text: el.querySelector('textarea').value });
            });
            localStorage.setItem('nebula-posts', JSON.stringify(posts));
        }

        window.onload = () => {
            loadImg('logo-data', 'logo-img', 'logo-txt');
            loadImg('h-img-data', 'h-img', 'l-h');
            
            // Render Astronots (Centered)
            document.getElementById('cont-struktur').innerHTML = astronots.map((p, i) => {
                const key = `s-${i}`;
                const isPJ = p.lock;
                if(!isPJ) setTimeout(() => loadImg(key, `img-${key}`, `lbl-${key}`), 0);
                return `<div class="card-solid p-6 flex flex-col items-center">
                    ${!isPJ ? `<div class="btn-del" onclick="delImg('${key}', 'img-${key}', 'lbl-${key}')">✕</div>` : ''}
                    <div class="w-24 h-24 border-2 border-gray-700 rounded-full overflow-hidden mb-4 relative ${isPJ ? 'pj-locked pj-avatar' : 'bg-gray-800'}">
                        <img id="img-${key}" class="w-full h-full object-cover hidden">
                        ${!isPJ ? `<label id="lbl-${key}" class="absolute inset-0 flex items-center justify-center text-[8px] opacity-30">FOTO</label>
                        <input type="file" id="in-${key}" class="hidden" onchange="saveImg(event, '${key}', 'img-${key}', 'lbl-${key}')">
                        <div onclick="document.getElementById('in-${key}').click()" class="absolute inset-0 cursor-pointer"></div>` : ''}
                    </div>
                    <p class="text-[10px] text-red-500 font-bold uppercase mb-1">${p.j}</p>
                    <p class="text-xs text-white font-bold px-2">${p.n}</p>
                </div>`;
            }).join('');

            // Render Orbit (Full Original Names & Centered)
            document.getElementById('cont-anggota').innerHTML = orbit.map((n, i) => {
                const key = `a-${i}`;
                setTimeout(() => loadImg(key, `img-${key}`, null), 0);
                return `<div class="card-solid p-5 flex flex-col items-center justify-between min-h-[160px]">
                    <div class="btn-del" onclick="delImg('${key}', 'img-${key}', null)">✕</div>
                    <div class="w-16 h-16 border border-gray-700 rounded-full overflow-hidden bg-gray-900 mb-3 relative flex-shrink-0">
                        <img id="img-${key}" class="w-full h-full object-cover hidden">
                        <input type="file" id="in-${key}" class="hidden" onchange="saveImg(event, '${key}', 'img-${key}', null)">
                        <div onclick="document.getElementById('in-${key}').click()" class="absolute inset-0 cursor-pointer"></div>
                    </div>
                    <p class="text-[9px] text-gray-300 font-bold uppercase leading-tight tracking-tight">${n}</p>
                </div>`;
            }).join('');

            const saved = JSON.parse(localStorage.getItem('nebula-posts') || '[]');
            saved.reverse().forEach(p => addPost(p.id, p.text));
        };
    </script>
</body>
</html>
