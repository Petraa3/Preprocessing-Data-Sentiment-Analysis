# Belajar Analisis Sentimen: Membersihkan Data TikTok ‘mbg’

Proyek ini memberikan informasi untuk **tahapan preprocessing** atau **pembersihan data teks** agar data siap digunakan untuk proses analisis sentimen. Dataset dikumpulkan menggunakan **Apify** dengan kata kunci "mbg", lalu melalui serangkaian proses pembersihan hingga menjadi teks siap olah.

---

## Alur Preprocessing Data

Berikut urutan tahapan preprocessing yang dilakukan:

<img src="Desain%20tanpa%20judul.png" width="400">

1. **Data Asli**  
   Data hasil scraping dari TikTok, berisi komentar mentah dengan berbagai karakter, emoji, mention, dan simbol.

2. **Cleaning**  
   Menghapus elemen yang tidak relevan seperti emoji, URL, mention (@username), dan tanda baca berlebih agar data lebih bersih.

3. **Case Folding**  
   Mengubah seluruh teks menjadi huruf kecil (lowercase) agar tidak terjadi perbedaan makna antara huruf besar dan kecil.

4. **Normalisasi**  
   Mengubah kata tidak baku menjadi kata baku menggunakan kamus normalisasi, misalnya:
   - “gk” → “tidak”  
   - “jd” → “jadi”  
   - “servis” → “layanan”  

5. **Tokenisasi**  
   Memecah kalimat menjadi daftar kata agar lebih mudah diproses dalam tahap berikutnya.

6. **Stopword Removal**  
   Menghapus kata umum yang tidak memiliki makna signifikan dalam analisis, seperti *dan*, *yang*, *di*, *ke*, dll.

7. **Stemming**  
   Mengembalikan kata ke bentuk dasarnya menggunakan library **Sastrawi**, misalnya:
   - “bermain” → “main”  
   - “menulis” → “tulis”

8. **Data Bersih**  
   Hasil akhir berupa teks yang siap digunakan untuk analisis sentimen.
