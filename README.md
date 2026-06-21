# TicktingTimeBomb

🚨 TICKING TIME BOMB - Peringatan Kenaikan Muka Air Laut

TICKING TIME BOMB adalah Dashboard Spasial Pesisir & Kelautan yang dirancang untuk mensimulasikan ancaman ganda mematikan: Kenaikan Muka Air Laut Global (Sea Level Rise) dan Laju Penurunan Muka Tanah (Land Subsidence).
Sistem ini bertindak sebagai "Kalkulator Waktu Mundur" yang memproyeksikan tahun ke berapa sebuah wilayah pesisir akan tertelan genangan air laut secara permanen (inundasi total).

📋 Petunjuk Instalasi & Cara Menjalankan Program
Sistem ini dibangun dengan arsitektur Client-Side murni. Anda tidak perlu menginstal database, Node.js, atau backend server apapun. Program dapat langsung diuji dengan mudah.

Prasyarat:
1. Komputer / Laptop dengan sistem operasi Windows, macOS, atau Linux.
2. Peramban Web Modern (Google Chrome, Mozilla Firefox, Microsoft Edge, atau Safari).
3. Koneksi Internet Aktif (Wajib, untuk memuat Peta Satelit, Library Tailwind/Chart.js, dan Data API Oseanografi).

Langkah-langkah Instalasi:
Anda bisa mendapatkan source code program ini melalui dua cara:

Opsi A: Mengunduh File ZIP (Cara Termudah)
1. Klik tombol <> Code berwarna hijau di bagian atas repositori GitHub ini.
2. Pilih Download ZIP.
3. Ekstrak (Unzip) file yang telah diunduh ke dalam sebuah folder di laptop Anda (misal: di folder Desktop atau Documents).

Opsi B: Menggunakan Git Clone (Via Terminal/CMD)
1. Buka Terminal atau Command Prompt.
2. Jalankan perintah berikut:
3. git clone https://github.com/USERNAME_ANDA/NAMA_REPOSITORI.git

Masuk ke direktori proyek:
cd NAMA_REPOSITORI


Cara Menjalankan Program (Eksekusi Dashboard):
Pilih salah satu metode di bawah ini untuk menjalankan dashboard:

Metode 1: Buka Langsung (Direct Open)
1. Buka folder proyek yang telah Anda ekstrak atau clone.
2. Cari file bernama index.html.
3. Klik ganda (Double-Click) file tersebut. Aplikasi akan langsung terbuka dan berjalan di browser default Anda.

Metode 2: Menggunakan Visual Studio Code & Live Server 
1. Buka aplikasi Visual Studio Code (VS Code).
2. Tarik dan lepas (drag-and-drop) folder proyek ke dalam VS Code.
3. Pastikan Anda telah menginstal ekstensi Live Server 
4. Klik kanan pada file index.html lalu pilih "Open with Live Server".
5. Dashboard akan terbuka otomatis di browser pada alamat http://127.0.0.1:5500/index.html.

🌊 Cara Menggunakan Dashboard (Pengujian Fungsionalitas)
Untuk memverifikasi bahwa seluruh fungsi berjalan dengan baik, ikuti panduan pengujian berikut:

1.Saat program terbuka, Anda akan melihat Landing Page "Ticking Time Bomb". Klik tombol "Hitung Waktu Mundur" / "Inisialisasi Workspace".
2. Di dalam Workspace, Anda bisa:
a. Menggunakan Search Bar: Ketik nama kota (contoh: "Demak" atau "Muara Baru") lalu klik "Cari Target". Peta akan terbang (fly-to) ke lokasi tersebut otomatis.
b. Klik Peta Langsung: Klik titik manapun di atas peta Indonesia/Dunia.
c. Perhatikan indikator "LIVE SENSOR". Sistem sedang menarik data topografi, tinggi gelombang laut, dan amblesan.
d. Grafik Proyeksi: Perhatikan grafik garis. Titik perpotongan antara garis Elevasi Tanah (Oranye) dan Kenaikan Muka Air Laut (Biru) adalah tahun di mana wilayah     tersebut diprediksi tenggelam permanen.
e. Panel Evaluasi (Bawah): Sistem akan otomatis merakit laporan penilaian bahaya wilayah tersebut.
f. Eksport & Cetak:
1. Uji tombol "Eksport CSV" di pojok kanan atas untuk mengunduh data proyeksi ke format Excel.
2. Uji tombol "Cetak Laporan" untuk menyimpan tampilan dashboard menjadi PDF yang bersih (print-ready).
g. Simulasi CMEMS (Opsional): Pada panel kanan, isikan sembarang teks pada Username & Password Copernicus, lalu klik "Ekstrak Raster SLA" untuk mensimulasikan penyesuaian parameter air laut secara dinamis.

✨ Fitur Unggulan
🗺️ Peta Spasial Multi-Layer: Integrasi Leaflet.js dengan berbagai peta dasar (Satelit Esri, Topografi) dan overlay Rute Kelautan OpenSeaMap.
📈 Simulasi Inundasi Interaktif: Grafik time-series interaktif (2026 - 2100) yang memproyeksikan persilangan elevasi daratan dan kenaikan laut (MSL).
🌊 Dinamika Kelautan WMO: Ekstraksi Wave Height dan Storm Surge real-time, lengkap dengan klasifikasi Sea State WMO (Tenang, Berombak, Ekstrem).
📄 Sistem Pelaporan Mandiri: Generator kesimpulan teknis yang diolah secara otomatis berdasarkan kalkulator numerik.
🖨️ Print & Export Ready: Fitur ekstraksi data spasial ke format CSV dan PDF.
⚙️ Sumber Data API (Real-Time)

Dashboard ini mengambil data spasial secara live dari layanan terbuka berikut:

a. Open-Meteo Elevation API (Topografi Daratan)

b. Open-Meteo Marine API (Hidrodinamika Laut)

c. Nominatim OpenStreetMap (Reverse & Forward Geocoding / Search)

d. Wikimedia API (Ekstraksi representasi gambar visual lokasi)

Catatan:

Program ini dikembangkan untuk tujuan simulasi prototipe, edukasi, dan proyek akademik. Simulasi data penurunan tanah (subsidence) menggunakan kombinasi data API publik dan konstanta aproksimasi zona rentan Indonesia.
