# HR Analytics: Solving Employee Retention Problems with Employee Clustering

Tantangan utama adalah memahami tingkat attrition yang tinggi (25%) dan mengidentifikasi di mana dan mengapa hal itu terjadi. Proyek ini bertujuan untuk memetakan distribusi karyawan, menganalisis pola gaji dan kinerja, serta mengidentifikasi kelompok-kelompok karyawan yang paling berisiko untuk membantu tim HR membuat keputusan yang berbasis data.

## Data and Tools
- Dataset: Data HR berisi 2 juta catatan dari sebuah perusahaan multinasional, termasuk informasi gaji, kinerja, status pekerjaan, dan lainnya.
- Alat: Python (pandas, matplotlib, seaborn, scikit-learn, squarify, dan machine learning clustering K-Means

## Metodologi
1. Melakukan proses data cleaning dengan menghilangkan kolom index Unnamed
   <img width="399" height="36" alt="image" src="https://github.com/user-attachments/assets/edb5ff9f-b3ce-49f6-80ce-b557a010c3d3" />

3. Mengidentifikasi nilai yang hilang dengan mengisi nilai yang hilang di Salary INR
   <img width="664" height="21" alt="image" src="https://github.com/user-attachments/assets/3dc8ffd8-7314-4538-b3ff-1f75db638162" />

5. Analisis Kluster:
   
   <img width="437" height="165" alt="image" src="https://github.com/user-attachments/assets/2897184e-6c52-45e1-8e24-abef057872cf" />

   - dengan menggunakan StandardScaler dari scikit-learn untuk menormalisasi data numerik (Salary_INR, Experience_Years, Performance_Rating). Ini adalah langkah yang krusial untuk memastikan bahwa semua fitur memiliki bobot yang sama dalam algoritma K-Means, mencegah fitur dengan nilai besar mendominasi.
   - kemudian menerapkan algoritma K-Means dengan tiga klaster (n_clusters=3) dan menetapkan random_state=42 untuk memastikan hasilnya dapat direplikasi.
   - selanjutnya hasil klasterisasi disimpan kembali ke DataFrame utama dalam kolom baru bernama Cluster

## Temuan 
<img width="465" height="95" alt="image" src="https://github.com/user-attachments/assets/7122f0d0-35d5-4fcc-8f36-9f7e102038c9" />

Berdasarkan nilai rata-rata yang telah dibuat, kita bisa memberikan makna pada setiap klaster:
1. Klaster 0: Karyawan Berpengalaman & Bergaji Tinggi
   - Karakteristik: Ini adalah kelompok dengan gaji tertinggi (rata-rata ₹1,69 juta) dan pengalaman paling tinggi (rata-rata 4,96 tahun). Rating kinerja mereka berada di level rata-rata (3.02).
   - Temuan: Kelompok ini kemungkinan besar terdiri dari para spesialis senior dan talenta kunci di perusahaan. Mereka adalah pilar dari organisasi, dan mempertahankan mereka harus menjadi prioritas utama.

2. Klaster 1: Karyawan Berkinerja Rendah & Berpengalaman Sedang
   - Karakteristik: Kelompok ini memiliki gaji terendah (rata-rata ₹780 ribu) dan rating kinerja terburuk (1.74). Pengalaman mereka berada di tengah (rata-rata 5,66 tahun), yang menunjukkan bahwa mereka bukan karyawan baru.
   - Temuan: Klaster ini bisa menjadi "talenta yang berisiko" atau "talenta yang underperform". Meskipun mereka memiliki pengalaman, kinerja mereka di bawah standar. Mereka mungkin tidak puas dengan kompensasi atau tidak memiliki keterampilan yang relevan.

3. Klaster 2: Karyawan Berkinerja Tinggi & Gaji Standar
   - Karakteristik: Kelompok ini memiliki rating kinerja tertinggi (4.17) tetapi gaji rata-rata yang mirip dengan Klaster 1 (rata-rata ₹777 ribu). Pengalaman mereka paling sedikit (rata-rata 4,42 tahun).
   - Temuan: Klaster ini kemungkinan besar adalah "bintang baru" yang sangat produktif tetapi mungkin merasa kompensasinya belum setara dengan kontribusi mereka. Mereka adalah kelompok yang berisiko tinggi untuk mengalami attrition jika tidak diperhatikan.

<img width="965" height="885" alt="image" src="https://github.com/user-attachments/assets/3932ac7e-0d86-4c4f-ae73-fdc30733829e" />

## Kontributor
- Nama :  Rizka Hasna Nabila
- Email : rizkahasna94@gmail.com
- Github : @rizkaa-hn
- Linkedin : https://www.linkedin.com/in/rizkahasnanabila/ 
