### Lampiran Screenshot Performance Tesing (JMeter)
![gui_1.png](img/gui_1.png)
Gambar 1: Penggunaan JMeter-GUI untuk Test Creation
![non_gui_1.png](img/non_gui_1.png)
Gambar 2: Penggunaan JMeter-CLI untuk Load Testing
![log_1.png](img/log_1.png)
Gambar 3: Hasil Load Testing

### Lampiran Screenshot Optimizing (Profiling Intellij)
![all_student_pre_profiling.png](img/all_student_pre_profiling.png)![all_student_post_profiling.png](img/all_student_post_profiling.png)
Gambar 4 & 5: Perbandingan pre-post refactor method GetAllStudentWithCourse 
![join_student_pre_profiling.png](img/join_student_pre_profiling.png)![join_student_post_profiling.png](img/join_student_post_profiling.png)
Gambar 6 & 7: Perbandingan pre-post refactor method joinStudentNames
![highest_gpa_pre_profiling.png](img/highest_gpa_pre_profiling.png)![highest_gpa_post_profiling.png](img/highest_gpa_post_profiling.png)
Gambar 8 & 9: Perbandingan pre-post refactor method joinStudentNames
<br /><br />Jika diperhatikan sekilas, performa post-optimize sudah lebih cepat sebanyak lebih dari 20% (CPU Time).
<br />
### Perbandingan Hasil Optimizing di JMeter
![compare_pre_post_optimizing.png](img/compare_pre_post_optimizing.png)
<br />Gambar 10: Perbandingan load test di CLI JMeter<br /><br />
Setelah melakukan *profiling* dan optimasi kode (refactoring), pengujian performa ulang dilakukan menggunakan JMeter dengan konfigurasi *load testing* yang sama persis. Hasilnya menunjukkan peningkatan performa yang sangat signifikan:

* **Total Waktu Eksekusi:** Turun drastis dari **2 menit 43 detik** menjadi hanya **13 detik**.
* **Throughput:** Meningkat tajam dari **0.2 requests/second** menjadi **2.3 requests/second**, menandakan kapasitas server melayani *user* naik lebih dari 10 kali lipat.
* **Average Response Time:** Waktu tunggu rata-rata membaik secara masif dari **~55,4 detik** menjadi hanya **~5,5 detik** per request.
* **Error Rate:** Turun dari **3.33%** (kemungkinan akibat *timeout* antrean query) menjadi **0.00%** (stabil).
