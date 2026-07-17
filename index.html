<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistem Pemutus Listrik Pelanggan - IoT Monitoring System</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons+Round" rel="stylesheet">
    
    <script src="https://cdn.jsdelivr.net/npm/xlsx@0.18.5/dist/xlsx.full.min.js"></script>
    
    <style>
        /* --- MODEREN UI DESIGN SYSTEM --- */
        :root {
            --bg-primary: #f8fafc;
            --bg-sidebar: #0f172a;
            --text-main: #1e293b;
            --text-muted: #64748b;
            --accent-color: #3b82f6;
            --accent-light: #eff6ff;
            --success: #10b981;
            --success-light: #ecfdf5;
            --danger: #ef4444;
            --danger-light: #fef2f2;
            --warning: #f59e0b;
            --card-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.05), 0 2px 4px -2px rgb(0 0 0 / 0.05);
            --border-radius: 12px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-main);
            display: flex;
            height: 100vh;
            overflow: hidden;
        }

        /* --- HALAMAN LOGIN --- */
        #login-page {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 10% 20%, rgb(90, 142, 251) 0%, rgb(41, 61, 166) 100%);
            display: flex; justify-content: center; align-items: center;
            z-index: 1000;
        }

        .login-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(12px);
            padding: 40px;
            border-radius: 24px;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.5);
            width: 100%;
            max-width: 400px;
            text-align: center;
        }

        .pln-logo {
            width: 2cm;
            height: 2cm;
            margin-bottom: 16px;
            object-fit: contain;
            display: inline-block;
        }
        
        .sidebar-logo {
            width: auto;
            height: 35px;
            object-fit: contain;
        }

        .login-card h2 { font-weight: 700; color: #0f172a; margin-bottom: 2px; font-size: 20px; }
        .login-card p { color: var(--text-muted); font-size: 14px; margin-bottom: 24px; }

        .input-box {
            position: relative; margin-bottom: 20px; text-align: left;
        }
        .input-box label { font-size: 13px; font-weight: 500; color: var(--text-main); display: block; margin-bottom: 6px; }
        .input-box input {
            width: 100%; padding: 12px 16px; border: 1.5px solid #e2e8f0; border-radius: var(--border-radius);
            font-size: 14px; transition: all 0.3s; background: #fff;
        }
        .input-box input:focus { outline: none; border-color: var(--accent-color); box-shadow: 0 0 0 4px var(--accent-light); }

        /* --- LAYOUT UTAMA --- */
        #main-layout { display: none; width: 100%; height: 100%; }

        /* SIDEBAR */
        sidebar {
            width: 280px; background-color: var(--bg-sidebar); color: white;
            display: flex; flex-direction: column; float: left; height: 100%;
            padding: 24px; justify-content: space-between;
        }

        sidebar .brand {
            display: flex; align-items: center; gap: 12px; font-size: 16px; font-weight: 700;
            padding-bottom: 24px; border-bottom: 1px solid #1e293b;
        }

        sidebar ul { list-style: none; margin-top: 24px; }
        sidebar ul li {
            display: flex; align-items: center; gap: 14px; padding: 12px 16px;
            border-radius: var(--border-radius); cursor: pointer; margin-bottom: 8px;
            color: #94a3b8; font-weight: 500; transition: all 0.3s;
        }
        sidebar ul li:hover, sidebar ul li.active { background-color: #1e293b; color: white; }
        sidebar ul li.active { background-color: var(--accent-color); color: white; }
        sidebar ul li.logout-btn { background-color: #1e293b; color: #f87171; }
        sidebar ul li.logout-btn:hover { background-color: var(--danger); color: white; }

        /* CONTENT AREA */
        .content { margin-left: 280px; padding: 40px; height: 100%; overflow-y: auto; }
        .content-section { display: none; }
        .content-section.active { display: block; animation: fadeIn 0.4s ease-in-out; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        header {
            display: flex; justify-content: space-between; align-items: center; margin-bottom: 32px;
        }
        header h2 { font-size: 26px; font-weight: 700; color: #0f172a; }
        .server-time { font-size: 14px; background: white; padding: 8px 16px; border-radius: 30px; box-shadow: var(--card-shadow); display: flex; align-items: center; gap: 8px; font-weight: 500;}

        /* BUTTONS & BADGES */
        .btn {
            display: inline-flex; align-items: center; gap: 8px; padding: 10px 20px; border: none;
            border-radius: var(--border-radius); cursor: pointer; font-weight: 600; font-size: 14px; transition: all 0.3s;
        }
        .btn-primary { background-color: var(--accent-color); color: white; }
        .btn-primary:hover { opacity: 0.9; transform: translateY(-1px); }
        .btn-danger { background-color: var(--danger-light); color: var(--danger); }
        .btn-danger:hover { background-color: var(--danger); color: white; }
        .btn-success { background-color: var(--success-light); color: var(--success); }
        .btn-success:hover { background-color: var(--success); color: white; }

        .badge { padding: 6px 12px; border-radius: 30px; font-size: 12px; font-weight: 600; display: inline-block; }
        .badge-active { background-color: var(--success-light); color: var(--success); }
        .badge-cut { background-color: var(--danger-light); color: var(--danger); }

        /* CARDS */
        .grid-cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 24px; margin-bottom: 32px; }
        .card { background: white; padding: 24px; border-radius: var(--border-radius); box-shadow: var(--card-shadow); display: flex; align-items: center; justify-content: space-between; }
        .card-info h3 { font-size: 14px; color: var(--text-muted); font-weight: 500; margin-bottom: 6px; }
        .card-info p { font-size: 28px; font-weight: 700; color: #0f172a; }
        .card-icon { width: 48px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; }

        /* TABLES */
        .table-container { background: white; border-radius: var(--border-radius); box-shadow: var(--card-shadow); overflow: hidden; margin-top: 20px; }
        table { width: 100%; border-collapse: collapse; text-align: left; font-size: 14px; }
        table th { background-color: #f8fafc; padding: 16px 24px; color: var(--text-muted); font-weight: 600; border-bottom: 1px solid #e2e8f0; }
        table td { padding: 16px 24px; border-bottom: 1px solid #f1f5f9; color: var(--text-main); font-weight: 500; }

        /* BANNER */
        .alert-banner { display: flex; gap: 12px; background: #fffbeb; border: 1px solid #fef3c7; padding: 16px; border-radius: var(--border-radius); margin-bottom: 24px; color: #b45309; font-size: 14px; }
        
        /* FILE UPLOAD STYLING */
        .upload-wrapper {
            background: white; padding: 24px; border-radius: var(--border-radius); box-shadow: var(--card-shadow);
            border: 2px dashed #cbd5e1; text-align: center; margin-bottom: 24px; transition: all 0.3s;
        }
        .upload-wrapper:hover { border-color: var(--accent-color); background: var(--accent-light); }
        .upload-wrapper input[type="file"] { display: none; }
        .upload-wrapper label { cursor: pointer; display: flex; flex-direction: column; align-items: center; gap: 8px; color: var(--text-muted); font-weight: 500; }
    </style>
</head>
<body>

    <div id="login-page">
        <div class="login-card">
            <img src="https://cdn.prod.website-files.com/64f9d0036cb97160cc26feba/67c5b4c0e514894449aca0cd_Logo%20PLN.png" alt="Logo PLN" class="pln-logo">
            <h2>Sistem Pemutus Listrik Pelanggan</h2>
            <p>Unit Layanan Pelanggan Bintan Center</p>
            
            <div class="input-box">
                <label>Username</label>
                <input type="text" id="username" placeholder="Masukkan username">
            </div>
            <div class="input-box">
                <label>Password</label>
                <input type="password" id="password" placeholder="Masukkan password">
            </div>
            <button class="btn btn-primary" style="width: 100%; justify-content: center; padding: 12px;" onclick="handleLogin()">Login</button>
        </div>
    </div>

    <div id="main-layout">
        <sidebar>
            <div>
                <div class="brand">
                    <img src="https://cdn.prod.website-files.com/64f9d0036cb97160cc26feba/67c5b4c0e514894449aca0cd_Logo%20PLN.png" alt="Logo PLN" class="sidebar-logo">
                    <span>Sistem Pemutus Listrik</span>
                </div>
                <ul>
                    <li class="menu-item active" onclick="switchMenu('dashboard', event)"><span class="material-icons-round">dashboard</span>Dashboard</li>
                    <li class="menu-item" onclick="switchMenu('pemutusan', event)"><span class="material-icons-round">power_settings_new</span>Pemutusan Listrik</li>
                    <li class="menu-item" onclick="switchMenu('pembacaan', event)"><span class="material-icons-round">bolt</span>Pembacaan kWh</li>
                    <li class="menu-item" onclick="switchMenu('tagihan', event)"><span class="material-icons-round">receipt_long</span> Tagihan Pelanggan</li>
                    <li class="menu-item" onclick="switchMenu('kelola-data', event)"><span class="material-icons-round">upload_file</span> Input Data Pelanggan</li>
                </ul>
            </div>
            <ul>
                <li class="logout-btn" onclick="handleLogout()"><span class="material-icons-round">logout</span>Logout</li>
            </ul>
        </sidebar>

        <div class="content">
            
            <div id="dashboard" class="content-section active">
                <header>
                    <h2>PT PLN (PERSERO) ULP BINTAN CENTER</h2>
                    <div class="server-time"><span class="material-icons-round" style="color: var(--accent-color); font-size: 18px;">schedule</span><span id="live-clock"></span></div>
                </header>
                <div class="grid-cards">
                    <div class="card">
                        <div class="card-info"><h3>Total Pelanggan</h3><p id="dash-total-user">0</p></div>
                        <div class="card-icon" style="background: var(--accent-light); color: var(--accent-color);"><span class="material-icons-round">people</span></div>
                    </div>
                    <div class="card">
                        <div class="card-info"><h3>Kwh Meter Aktif</h3><p id="dash-active-user">0</p></div>
                        <div class="card-icon" style="background: var(--success-light); color: var(--success);"><span class="material-icons-round">bolt</span></div>
                    </div>
                    <div class="card">
                        <div class="card-info"><h3>Kwh Meter Terputus</h3><p id="dash-cut-user">0</p></div>
                        <div class="card-icon" style="background: var(--danger-light); color: var(--danger);"><span class="material-icons-round">power_off</span></div>
                    </div>
                </div>
                <h3 style="font-weight: 600; font-size: 18px; margin-bottom: 12px;">Log Aktivitas</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr>
                                <th>Tanggal & Waktu</th> 
                                <th>ID Pelanggan</th>
                                <th>Aktivitas Pemutusan Listrik</th>
                                <th>Status Perintah</th>
                            </tr>
                        </thead>
                        <tbody id="log-table-body"></tbody>
                    </table>
                </div>
            </div>

            <div id="pemutusan" class="content-section">
                <header><h2>Sistem Kontrol Alat Pada Pelanggan</h2></header>
                <div class="alert-banner">
                    <span class="material-icons-round">warning</span>
                    <span><b>Perhatian:</b> Menekan tombol putus akan langsung mengirim sinyal ke mikrokontroler IoT untuk mematikan relay utama fisik pelanggan.</span>
                </div>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>ID Pelanggan</th><th>Nama Pelanggan</th><th>Alamat</th><th>Status Listrik</th><th>Status IoT</th></tr>
                        </thead>
                        <tbody id="pemutusan-table-body"></tbody>
                    </table>
                </div>
            </div>

            <div id="pembacaan" class="content-section">
                <header>
                    <h2>Sistem Parameter Kwh Meter Pascabayar</h2>
                    
                </header>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>ID Pelanggan</th><th>Nama Pelanggan</th><th>Alamat</th><th>Total(kWh)</th><th>Tegangan</th><th>Arus</th><th>Daya Saat Ini</th></tr>
                        </thead>
                        <tbody id="pembacaan-table-body"></tbody>
                    </table>
                </div>
            </div>

            <div id="tagihan" class="content-section">
                <header><h2>Status Administrasi & Tunggakan</h2></header>
                <div class="alert-banner" style="background: #eff6ff; border-color: #dbeafe; color: #1e40af;">
                    <span class="material-icons-round">info</span>
                    <span>Halaman review status keuangan sinkron dengan sistem billing pusat ULP Bintan Center.</span>
                </div>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>ID Pelanggan</th><th>Nama Pelanggan</th><th>Alamat</th><th>Penggunaan</th><th>Total Tagihan</th><th>Status Keuangan</th><th>Rekomendasi IoT</th></tr>
                        </thead>
                        <tbody id="tagihan-table-body"></tbody>
                    </table>
                </div>
            </div>

            <div id="kelola-data" class="content-section">
                <header>
                    <h2>Kelola & Unggah Data Riil Pelanggan</h2>
                    <div style="display: flex; gap: 10px;">
                        <button class="btn btn-success" onclick="unduhLaporanExcel()"><span class="material-icons-round">download</span>Unduh Laporan Excel (Semua Data)</button>
                        <button class="btn btn-danger" onclick="hapusSemuaDataSimulasi()"><span class="material-icons-round">delete_sweep</span>Kosongkan Semua Data</button>
                    </div>
                </header>
                
                <div class="alert-banner" style="background: #eff6ff; border-color: #dbeafe; color: #1e40af;">
                    <span class="material-icons-round">info</span>
                    <span>Format unggahan wajib memiliki 3 kolom: <b>Id Pelanggan</b>, <b>Nama</b>, dan <b>Alamat</b>. Silahkan Untuk Mengupload File Excel (.xlsx / .xls) untuk mengunggah data pelanggan & Data disimpan permanen di laman ini.</span>
                </div>

                <div class="upload-wrapper">
                    <input type="file" id="excel-file-input" accept=".xlsx, .xls" onchange="prosesFileExcel(event)">
                    <label for="excel-file-input">
                        <span class="material-icons-round" style="font-size: 48px; color: var(--accent-color);">upload_file</span>
                        <span>Klik di sini untuk mengunggah berkas Excel (.xlsx / .xls)</span>
                    </label>
                </div>

                <h3 style="font-weight: 600; font-size: 18px; margin-bottom: 12px;">Daftar Kontrol Data Aktif</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr>
                                <th>ID Pelanggan</th>
                                <th>Nama Pelanggan</th>
                                <th>Alamat</th>
                                <th>Status Listrik</th>
                                <th>Tagihan Aktif</th>
                                <th>Aksi Pembersihan</th>
                            </tr>
                        </thead>
                        <tbody id="kelola-table-body"></tbody>
                    </table>
                </div>
            </div>

        </div>
    </div>

    <script>
        // ==========================================
        // CONFIG UTAMA BLYNK IOT API
        // ==========================================
        const BLYNK_AUTH_TOKEN = "eAyNEf99daUEEYCLVu4RSVFKGml4zu5G"; 
        const BLYNK_API_URL = "https://blynk.cloud/external/api";
        // ==========================================

        // KINI DATA AWAL DIBACA DARI LOCALSTORAGE (PERMANEN) ATAU KOSONG JIKA BELUM ADA FILE UPLOAD
        let dataPelanggan = JSON.parse(localStorage.getItem('pln_data_pelanggan')) || [];

        // Log aktivitas juga disimpan di LocalStorage agar sinkron
        let logAktivitas = JSON.parse(localStorage.getItem('pln_log_aktivitas')) || [];

        function simpanDataKeStorage() {
            localStorage.setItem('pln_data_pelanggan', JSON.stringify(dataPelanggan));
            localStorage.setItem('pln_log_aktivitas', JSON.stringify(logAktivitas));
        }

        function handleLogin() {
            const user = document.getElementById('username').value;
            const pass = document.getElementById('password').value;
            if(user === "UlpBintan" && pass === "Listrikpln123") {
                document.getElementById('login-page').style.display = 'none';
                document.getElementById('main-layout').style.display = 'block';
                renderSemuaData();
            } else { 
                alert("Akses ditolak! Username/Password salah."); 
            }
        }

        function handleLogout() {
            document.getElementById('username').value = '';
            document.getElementById('password').value = '';
            document.getElementById('login-page').style.display = 'flex';
            document.getElementById('main-layout').style.display = 'none';
        }

        function switchMenu(menuId, event) {
            document.querySelectorAll('.content-section').forEach(s => s.classList.remove('active'));
            document.querySelectorAll('.menu-item').forEach(m => m.classList.remove('active'));
            
            document.getElementById(menuId).classList.add('active');
            if(event && event.currentTarget) {
                event.currentTarget.classList.add('active');
            }
            renderSemuaData();
        }

        // ==========================================
        // PROSES PEMBACAAN EXCEL DENGAN GENERATE DATA RANDOM STRATEGIS
        // ==========================================
        function prosesFileExcel(event) {
            const file = event.target.files[0];
            if (!file) return;

            const reader = new FileReader();
            reader.onload = function(e) {
                const data = new Uint8Array(e.target.result);
                const workbook = XLSX.read(data, { type: 'array' });
                const sheetName = workbook.SheetNames[0];
                const worksheet = workbook.Sheets[sheetName];
                
                const JSONData = XLSX.utils.sheet_to_json(worksheet);
                
                if (JSONData.length === 0) {
                    alert("File Excel kosong atau format kolom tidak sesuai!");
                    return;
                }

                const dataHasilImport = JSONData.map(item => {
                    const idPelanggan = item.id || item.ID || item['Id Pelanggan'] || item['ID Pelanggan'] || Math.floor(Math.random() * 100000000000);
                    const namaPelanggan = item.nama || item.Nama || item['Nama Pelanggan'] || "Tanpa Nama";
                    const alamatPelanggan = item.alamat || item.Alamat || item['Alamat Pelanggan'] || "Tidak Ada Alamat";
                    
                    const statusAwal = Math.random() > 0.2 ? "AKTIF" : "TERPUTUS";
                    const isAktif = statusAwal === "AKTIF";
                    
                    const kwhAcak = +(Math.random() * 520 + 30).toFixed(1);
                    const teganganAcak = isAktif ? +(216 + Math.random() * 6).toFixed(1) : 0.0;
                    const arusAcak = isAktif ? +(0.4 + Math.random() * 4.5).toFixed(1) : 0.0;
                    const dayaAcak = +(teganganAcak * arusAcak).toFixed(1);
                    
                    let tagihanAcak = 0;
                    let apakahLunas = true;
                    
                    if (!isAktif) {
                        tagihanAcak = Math.floor(Math.random() * 5 + 3) * 135000;
                        apakahLunas = false;
                    } else if (Math.random() > 0.7) {
                        tagihanAcak = Math.floor(Math.random() * 3 + 1) * 70000;
                        apakahLunas = false;
                    }

                    return {
                        id: String(idPelanggan).trim(),
                        nama: String(namaPelanggan).trim(),
                        alamat: String(alamatPelanggan).trim(),
                        kwh: kwhAcak,
                        tegangan: teganganAcak,
                        arus: arusAcak,
                        daya_watt: dayaAcak,
                        status: statusAwal,
                        tagihan: tagihanAcak,
                        lunas: apakahLunas
                    };
                });

                dataPelanggan = [...dataPelanggan, ...dataHasilImport];
                simpanDataKeStorage();
                alert(`Berhasil mengimpor ${dataHasilImport.length} pelanggan dari Excel dengan parameter random default!`);
                event.target.value = ''; 
                renderSemuaData();
            };
            reader.readAsArrayBuffer(file);
        }

        // ==========================================
        // FITUR BARU: EXPORT DATA KE FILE EXCEL UNTUK DI-DOWNLOAD
        // ==========================================
        function unduhLaporanExcel() {
            if (dataPelanggan.length === 0) {
                alert("Tidak ada data yang tersedia di sistem untuk diunduh!");
                return;
            }

            // Memetakan struktur data aplikasi ke dalam format baris & kolom laporan Excel
            const barisDataExcel = dataPelanggan.map(p => ({
                "ID Pelanggan": p.id,
                "Nama Pelanggan": p.nama,
                "Alamat": p.alamat,
                "Status Aliran Listrik": p.status,
                "Total Penggunaan (kWh)": p.kwh,
                "Tegangan Sensor (V)": p.tegangan,
                "Arus Beban (A)": p.arus,
                "Daya Aktif (W)": p.daya_watt,
                "Total Tunggakan (Rp)": p.tagihan,
                "Status Administrasi": p.lunas ? "Lunas" : "Ada Tunggakan"
            }));

            // Membuat worksheet baru dari JSON data di atas
            const worksheet = XLSX.utils.json_to_sheet(barisDataExcel);
            const workbook = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(workbook, worksheet, "Laporan Pelanggan");

            // Mengatur lebar kolom otomatis agar terlihat rapi saat dibuka
            const lebarKolom = Object.keys(barisDataExcel[0]).map(key => ({
                wch: Math.max(key.length, ...barisDataExcel.map(row => row[key] ? row[key].toString().length : 10)) + 3
            }));
            worksheet['!cols'] = lebarKolom;

            // Generate nama file dinamis menggunakan timestamp waktu saat ini
            const tanggalSekarang = new Date().toISOString().slice(0, 10);
            const namaFile = `Laporan_Sistem_IoT_PLN_${tanggalSekarang}.xlsx`;

            // Eksekusi download file ke device user
            XLSX.writeFile(workbook, namaFile);
        }

        function hapusSatuBaris(idx) {
            const namaPelanggan = dataPelanggan[idx].nama;
            if(confirm(`Apakah Anda yakin ingin menghapus pelanggan "${namaPelanggan}"?`)) {
                dataPelanggan.splice(idx, 1);
                simpanDataKeStorage();
                renderSemuaData();
            }
        }

        function hapusSemuaDataSimulasi() {
            if(confirm("PERINGATAN! Seluruh data pelanggan di sistem akan dibersihkan secara permanen. Lanjutkan?")) {
                dataPelanggan = [];
                logAktivitas = [];
                simpanDataKeStorage();
                renderSemuaData();
            }
        }

        // ==========================================
        // RENDERING TAMPILAN UI
        // ==========================================
        function renderSemuaData() {
            const skrg = new Date();
            const clockEl = document.getElementById('live-clock');
            if (clockEl) clockEl.innerText = skrg.toLocaleTimeString('id-ID') + " WIB";

            document.getElementById('dash-total-user').innerText = dataPelanggan.length;
            document.getElementById('dash-active-user').innerText = dataPelanggan.filter(p => p.status === "AKTIF").length;
            document.getElementById('dash-cut-user').innerText = dataPelanggan.filter(p => p.status === "TERPUTUS").length;

            document.getElementById('log-table-body').innerHTML = logAktivitas.map(log => `
                <tr>
                    <td>${log.waktu}</td>
                    <td><code style="background:#f1f5f9; padding:4px 8px; border-radius:6px;">${log.id}</code></td>
                    <td>${log.aksi}</td>
                    <td><span class='badge badge-active'>${log.status}</span></td>
                </tr>
            `).join('');

            document.getElementById('pemutusan-table-body').innerHTML = dataPelanggan.map((p, idx) => {
                const warnaTombol = p.status === 'AKTIF' ? 'btn-danger' : 'btn-success';
                const iconTombol = p.status === 'AKTIF' ? 'power_off' : 'bolt';
                const teksTombol = p.status === 'AKTIF' ? 'Putuskan Aliran' : 'Hubungkan Aliran';
                const badgeStatus = p.status === 'AKTIF' ? 'badge-active' : 'badge-cut';

                return `
                    <tr>
                        <td><code>${p.id}</code></td>
                        <td><strong>${p.nama}</strong></td>
                        <td><small>${p.alamat}</small></td>
                        <td><span class="badge ${badgeStatus}">${p.status}</span></td>
                        <td>
                            <button class="btn ${warnaTombol}" onclick="toggleListrik(${idx})">
                                <span class="material-icons-round" style="font-size:16px;">${iconTombol}</span>
                                ${teksTombol}
                            </button>
                        </td>
                    </tr>
                `;
            }).join('');

            document.getElementById('pembacaan-table-body').innerHTML = dataPelanggan.map(p => `
                <tr>
                    <td><code>${p.id}</code></td>
                    <td>${p.nama}</td>
                    <td><small>${p.alamat}</small></td>
                    <td><span style="color:var(--accent-color); font-weight:600">${p.kwh.toFixed(2)} kWh</span></td>
                    <td>${p.tegangan.toFixed(1)} V</td>
                    <td>${p.arus.toFixed(1)} A</td>
                    <td><span style="color:var(--warning); font-weight:600">${p.daya_watt.toFixed(1)} W</span></td>
                </tr>
            `).join('');

            document.getElementById('tagihan-table-body').innerHTML = dataPelanggan.map(p => `
                <tr>
                    <td><code>${p.id}</code></td>
                    <td>${p.nama}</td>
                    <td><small>${p.alamat}</small></td>
                    <td>${p.kwh.toFixed(1)} kWh</td>
                    <td><strong>Rp ${p.tagihan.toLocaleString('id-ID')}</strong></td>
                    <td><span class="badge ${p.lunas ? 'badge-active' : 'badge-cut'}">${p.lunas ? 'Lunas' : 'Ada Tunggakan'}</span></td>
                    <td><span style="font-weight:600; color:${p.lunas ? 'var(--success)' : 'var(--danger)'}">${p.lunas ? 'Sistem Aman' : 'Rekomendasi Putus'}</span></td>
                </tr>
            `).join('');

            const kelolaBody = document.getElementById('kelola-table-body');
            if(kelolaBody) {
                kelolaBody.innerHTML = dataPelanggan.map((p, idx) => `
                    <tr>
                        <td><code>${p.id}</code></td>
                        <td>${p.nama}</td>
                        <td><small>${p.alamat}</small></td>
                        <td><span class="badge ${p.status === 'AKTIF' ? 'badge-active' : 'badge-cut'}">${p.status}</span></td>
                        <td>Rp ${p.tagihan.toLocaleString('id-ID')}</td>
                        <td>
                            <button class="btn btn-danger" style="padding: 6px 12px; font-size:12px;" onclick="hapusSatuBaris(${idx})">
                                <span class="material-icons-round" style="font-size:14px;">delete</span> Hapus
                            </button>
                        </td>
                    </tr>
                `).join('');
            }
        }

        async function toggleListrik(idx) {
            const p = dataPelanggan[idx];
            const nilaiTarget = p.status === "AKTIF" ? 0 : 1;
            
            const sekarang = new Date();
            const tanggal = sekarang.toLocaleDateString('id-ID', { day: '2-digit', month: '2-digit', year: 'numeric' });
            const jam = sekarang.toLocaleTimeString('id-ID', { hour: '2-digit', minute: '2-digit' }).replace('.', ':');
            const waktuFull = `${tanggal} ${jam}`;
            
            const pesanKonfirmasi = p.status === "AKTIF" ? `Matikan listrik meteran ${p.id} (${p.nama})?` : `Hidupkan kembali listrik meteran ${p.id} (${p.nama})?`;
            
            if(!confirm(pesanKonfirmasi)) return;

            try {
                const respon = await fetch(`${BLYNK_API_URL}/update?token=${BLYNK_AUTH_TOKEN}&v1=${nilaiTarget}`);
                
                if(respon.ok) {
                    if(p.status === "AKTIF") {
                        p.status = "TERPUTUS"; p.tegangan = 0; p.arus = 0; p.daya_watt = 0;
                        logAktivitas.unshift({ waktu: waktuFull, id: p.id, aksi: "Relay Dimatikan via Blynk IoT API", status: "BERHASIL" });
                    } else {
                        p.status = "AKTIF"; p.tegangan = 220; p.arus = 1.2; p.daya_watt = 264;
                        logAktivitas.unshift({ waktu: waktuFull, id: p.id, aksi: "Relay Dihidupkan via Blynk IoT API", status: "BERHASIL" });
                    }
                    simpanDataKeStorage();
                    renderSemuaData();
                } else {
                    alert("Gagal terhubung ke Blynk. Periksa kembali AUTH TOKEN Anda.");
                }
            } catch (error) {
                console.error("Error Blynk API:", error);
                alert("Kesalahan Jaringan saat menghubungi Blynk IoT Cloud.");
            }
        }

        async function sinkronisasiDataBlynk() {
            try {
                const respon = await fetch(`${BLYNK_API_URL}/get?token=${BLYNK_AUTH_TOKEN}&v2`);
                if (respon.ok) {
                    const nilaiKwhDariSensor = await respon.text();
                    if(nilaiKwhDariSensor && !isNaN(nilaiKwhDariSensor) && dataPelanggan.length > 0) {
                        dataPelanggan[0].kwh = parseFloat(nilaiKwhDariSensor);
                        simpanDataKeStorage();
                        renderSemuaData();
                    }
                }
            } catch (error) {
                console.log("Menunggu koneksi hardware...", error);
            }
        }

        function simulasiKenaikanKwh() {
            if(dataPelanggan.length === 0) {
                alert("Silakan unggah data Excel terlebih dahulu!");
                return;
            }
            dataPelanggan.forEach(p => {
                if(p.status === "AKTIF") {
                    p.kwh += Math.random() * 0.8;
                    p.tegangan = +(218 + Math.random() * 5).toFixed(1);
                    p.arus = +(0.5 + Math.random() * 4).toFixed(1);
                    p.daya_watt = +(p.tegangan * p.arus).toFixed(1);
                }
            });
            simpanDataKeStorage();
            renderSemuaData();
        }

        // Sinkronisasi otomatis
        setInterval(() => {
            if(document.getElementById('main-layout').style.display === 'block') {
                sinkronisasiDataBlynk();
            }
        }, 5000);

        setInterval(() => {
            const clockEl = document.getElementById('live-clock');
            if (clockEl && document.getElementById('main-layout').style.display === 'block') {
                clockEl.innerText = new Date().toLocaleTimeString('id-ID') + " WIB";
            }
        }, 1000);
    </script>
</body>
</html>
