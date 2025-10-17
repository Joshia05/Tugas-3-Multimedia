# Tugas Multimedia 3: Pemrosesan Audio

## Deskripsi
Repository ini berisi proyek untuk tugas multimedia dengan fokus pada pemrosesan audio. Dalam tugas ini, dua lagu diproses untuk disesuaikan dalam tempo, kunci, dan transisi yang mulus menggunakan teknik audio processing. Lagu pertama memiliki tempo lebih lambat dan nuansa sedih, sementara lagu kedua lebih cepat dan ceria. Proyek ini mencakup beberapa tahapan pemrosesan seperti **time-stretching**, **pitch shifting**, **crossfading**, dan **filtering**.
Lagu_1_Lambat.wav # Lagu pertama dengan tempo lambat
Lagu_2_Cepat.wav # Lagu kedua dengan tempo cepat
Soal_1.wav # Audio untuk Soal 1
Soal_2.wav # Audio untuk Soal 2
Soal_1_pitch12.wav # Pitch-shifted Soal 1 (+12 semitone)
Soal_1_pitch7.wav # Pitch-shifted Soal 1 (+7 semitone)
Soal_2_pitch12.wav # Pitch-shifted Soal 2 (+12 semitone)
Soal_2_pitch7.wav # Pitch-shifted Soal 2 (+7 semitone)
Tugas Multimedia 3.html # File HTML dengan penjelasan proses dan hasil
Tugas Multimedia 3.pdf # Dokumen PDF hasil akhir tugas
combined_audio.wav # Hasil gabungan audio (Lagu 1 & 2)
final_processed_audio.wav # Hasil akhir pemrosesan audio
final_remix_with_crossfade.wav # Hasil remix dengan efek crossfade
lagu_1_processed.wav # Lagu 1 yang telah diproses
lagu_2_processed.wav # Lagu 2 yang telah diproses


## Instalasi dan Persyaratan
Pastikan Anda sudah menginstal semua dependensi berikut:

1. **Librosa**: Digunakan untuk pemrosesan audio dan analisis.
2. **Pydub**: Digunakan untuk manipulasi audio, termasuk crossfading.
3. **Soundfile**: Digunakan untuk membaca dan menulis file audio.
4. **Matplotlib**: Digunakan untuk visualisasi **waveform** dan **spectrogram**.

Instalasi dependensi menggunakan `pip`:

```bash
pip install librosa pydub soundfile matplotlib


## Struktur Repository
Berikut adalah struktur direktori dalam repository ini:
Cara Menjalankan Kode
1. Memuat dan Memvisualisasikan Audio
Pertama, pastikan Anda memuat file audio dengan benar menggunakan librosa.load().
Visualisasikan waveform dan spectrogram menggunakan librosa.display.
2. Deteksi Tempo dan Kunci
Lakukan deteksi tempo (BPM) dan estimasi kunci (key) menggunakan librosa.beat.beat_track() dan librosa.feature.chroma_cens().
3. Proses Time Stretch
Untuk menyamakan tempo antara dua lagu, gunakan scipy.signal.resample untuk merubah durasi lagu kedua agar sesuai dengan lagu pertama.
4. Proses Pitch Shift
Lakukan pitch shifting pada Lagu 2 agar kunci (key) sama dengan Lagu 1. Gunakan librosa.effects.pitch_shift().
5. Proses Crossfading
Gabungkan kedua lagu menggunakan efek crossfading untuk transisi yang halus antara kedua lagu.
6. Filter Tambahan (Opsional)
Anda dapat menambahkan filter seperti low-pass, high-pass, atau band-pass sesuai kebutuhan.
7. Hasil Akhir
Setelah proses selesai, file hasil gabungan akan disimpan sebagai final_remix_with_crossfade.wav. Anda dapat memvisualisasikan hasil remix ini.
Penjelasan Proses
Time Stretching: Dihitung dengan perbandingan tempo antara Lagu 1 dan Lagu 2, diterapkan untuk menyesuaikan durasi Lagu 2.
Pitch Shift: Menggunakan perbedaan semitone antara kunci Lagu 1 dan Lagu 2 untuk menyesuaikan pitch.
Crossfade: Digunakan untuk menggabungkan kedua lagu secara mulus, dengan transisi volume yang halus.
Spectrogram: Menampilkan perubahan frekuensi sepanjang durasi lagu untuk menunjukkan hasil dari proses audio.
Hasil Remix
Waveform dan Spectrogram menunjukkan bahwa kedua lagu sekarang berada pada tempo dan kunci yang sama, dengan transisi halus di antara keduanya berkat efek crossfading.
Pitch shifting memberikan perubahan yang terlihat pada spectrogram dengan pergeseran frekuensi, sementara time-stretching memperpanjang durasi Lagu 2 untuk mencocokkan tempo Lagu 1.
Kelebihan dan Kekurangan dari Remix
Kelebihan:
Harmoni antara kedua lagu: Proses time-stretching dan pitch-shifting memungkinkan kedua lagu disesuaikan agar berbaur lebih harmonis.
Transisi mulus: Crossfading memastikan transisi antara kedua lagu menjadi halus, tanpa ada jeda yang mencolok.
Kekurangan:
Penyimpangan kualitas suara: Proses time-stretching yang berlebihan atau pitch-shifting yang ekstrem dapat mengubah karakter suara dan menghasilkan distorsi.
Keterbatasan dalam perubahan besar: Jika perbedaan tempo atau kunci terlalu besar, kualitas suara bisa terganggu.
Secara keseluruhan, proses remix ini berhasil menyatukan dua lagu dengan cara yang harmonis, namun tentunya ada batasan terkait kualitas suara yang bisa dicapai tergantung pada seberapa besar perubahan yang diterapkan.
