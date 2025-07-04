
# ❤️ Arduino Heart Rate Monitor using MAX30102

> Sistem pendeteksi dan pemantau **Target Heart Rate (THR)** pada manusia secara real-time menggunakan **sensor MAX30102** dan **Arduino Uno**. Proyek ini bertujuan untuk membantu pengguna menjaga intensitas latihan agar tetap dalam zona aman dan optimal berdasarkan perhitungan metode Karvonen.

## 🧠 Deskripsi Singkat

Sistem ini memungkinkan pengguna:
- Mendeteksi detak jantung secara real-time menggunakan sensor optik MAX30102
- Menampilkan nilai BPM (beats per minute)
- Menghitung dan membandingkan dengan Target Heart Rate berdasarkan usia dan RHR
- Membantu menilai apakah aktivitas fisik sudah cukup intens atau belum

## 🎯 Tujuan

Membantu pengguna memantau denyut jantung saat berolahraga agar tidak melebihi batas aman atau justru terlalu rendah, yang dapat menyebabkan latihan menjadi tidak efektif.

## 🔧 Komponen Hardware

| Komponen         | Fungsi                                                                 |
|------------------|------------------------------------------------------------------------|
| Arduino Uno      | Mikrokontroler utama                                                    |
| Sensor MAX30102  | Sensor detak jantung dan oksigen (SpO2) berbasis cahaya inframerah      |
| Kabel Jumper     | Menghubungkan komponen ke Arduino                                       |
| Breadboard       | Media penyusunan rangkaian tanpa solder (opsional)                     |

## 💡 Cara Kerja Sistem

1. MAX30102 membaca data denyut jantung secara real-time.
2. Arduino memproses sinyal dan mendeteksi denyut jantung (bpm).
3. Sistem menghitung nilai **Target Heart Rate** dengan rumus metode Karvonen:
   ```
   HRmax = 206.9 - (0.67 × usia)
   THR = ((HRmax - RHR) × intensitas) + RHR
   ```
4. BPM dan rata-ratanya ditampilkan di Serial Monitor.
5. Jika tidak ada jari, sistem akan menampilkan notifikasi "No finger?"

## 📊 Hasil Pengujian

- Orang pertama (Usia 20, RHR 78 bpm) → THR = 158.22 bpm
- Orang kedua (Usia 20, RHR 64 bpm) → THR = 154.02 bpm
- Hasil pengukuran setelah jogging menunjukkan bahwa BPM aktual masih di bawah THR, menandakan bahwa intensitas latihan masih kurang.

## 🧑‍💻 Tim Proyek

| Nama                      | Peran                |
|---------------------------|----------------------|
| Wahyu Widihansyah         | Project Manager      |
| Azriel Darmawan           | Hardware Developer   |
| **Daffa Aprilian Herdika**| Data Analyst         |
| Lefry Ariyo Mandang       | Report Writer        |


## 📚 Referensi

- Febrida, M. (2013). [Pelari Jakarta Marathon Meninggal karena Serangan Jantung](https://www.liputan6.com)
- ACSM’s Guidelines for Exercise Testing and Prescription
- Musayyanah, P. et al. (2018). *Monitoring THR untuk Optimalisasi Latihan Lari*
