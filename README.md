# P1_Probstat_D_5025201174

Nama: Selfira Ayu Sheehan  
NRP: 5025201174  
Kelas: Probabilitas dan Statistik D

# Praktikum 1 - Distribusi Probabilitas

1. Seorang penyurvei secara acak memilih orang-orang di jalan sampai dia bertemu dengan seseorang yang menghadiri acara vaksinasi sebelumnya, tentukan:  
   a. Berapa peluang penyurvei bertemu x = 3 orang yang tidak menghadiri acara vaksinasi sebelum keberhasilan pertama ketika p = 0,20 dari populasi menghadiri acara vaksinasi?  
   
   ```
   dgeom(3,0.20)
   ```
   Hasil:
   
   
   
   b. Mean Distribusi Geometrik dengan 10.000 data random, prob = 0.20 dimana Distribusi Geometrik acak tersebut x = 3  
   
   
   ```
   set.seed(1); mean(rgeom(10000,0.20)==3)
   ```
   Hasil:
   
   
   
   c. Bandingkan hasil poin a dan b, apa kesimpulan yang bisa didapatkan?  
   
   ```
   a = 0.1024, b = 0.0993, hasil a menunjukkan peluang kegagalan sebanyak tiga kali sebelum berhasil, sedangkan b menunjukkan rata-rata kegagalan yang terjadi sebelum berhasil.
   ```
   
   d. Histogram Distribusi Geometrik, peluang x = 3 gagal sebelum sukses pertama  
      
   
   ```
   hist(dgeom(3, 0.20))
   ```
   Hasil:
   
   
   
   e. Nilai rataan (μ) dan varian (σ²) dari Distribusi Geometrik  
      
   
   ```
   rataan <- (1-0.2)/0.2
   rataan
   ```
   Hasil:
   
   
   ```
   varian <- (1-0.2)/(0.2^2)
   varian
   ```
   Hasil:
   
   
2. Terdapat 20 pasien menderita Covid19 dengan peluang sembuh sebesar 0.2. Tentukan:  
   a. Peluang terdapat 4 pasien yang sembuh  
         
   
   ```
   dbinom(4, 20, 0.2)
   ```
   Hasil:
   
   
   b. Gambarkan grafik histogram berdasarkan kasus tersebut  
            
   
   ```
   hist(dbinom(4, 20, 0.2))
   ```
   Hasil:
   
   
   c. Nilai rataan (μ) dan varian (σ²) dari Distribusi Binomial  
      
   
   ```
   rataan <- 20*0.2
   rataan
   ```
   Hasil:
   
   
   ```
   varian <- 20*0.2*0.8
   varian
   ```
   Hasil:
   
   
3. Diketahui data dari sebuah tempat bersalin di rumah sakit tertentu menunjukkan rata-rata historis 4,5 bayi lahir di rumah sakit ini setiap hari  
   a. Berapa peluang bahwa 6 bayi akan lahir di rumah sakit ini besok?  
            
   
   ```
   dpois(6, 4.5)
   ```
   Hasil:
   
   
   b. Simulasikan dan buatlah histogram kelahiran 6 bayi akan lahir di rumah sakit ini selama setahun (n = 365)  
            
   
   ```
   set.seed(1);hist(rpois(365,4.5), xlim=c(6.01, 6.99)
   ```
   Hasil:
   
   
   c. Bandingkan hasil poin a dan b, apa kesimpulan yang bisa didapatkan?  
            
   
   ```
   a merupakan peluang bayi berjumlah 6 yang akan lahir di rumah sakit ini, sedangkan histogram pada b menujukkan banyaknya hari dimana pada hari itu terdapat 6 bayi yang lahir
   ```

   d. Nilai rataan (μ) dan varian (σ²) dari Distribusi Poisson  
          
   
   ```
   rataan <- 4.5
   rataan
   ```
   Hasil:
   
   
   ```
   varian <- 4.5
   varian
   ```
   Hasil:
   
   
4. Diketahui nilai x = 2 dan v = 10. Tentukan:  
   a. Fungsi probabilitas dari Distribusi Chi-Square  
            
   
   ```
   dchisq(2, 10)
   ```
   Hasil:
   
   
   b. Histogram dari Distribusi Chi-Square dengan 100 data random  
            
   
   ```
   set.seed(1);hist(rchisq(100, 10))
   ```
   Hasil:
   
   
   c. Nilai rataan (μ) dan varian (σ²) dari Distribusi Chi-Square  
        
   
   ```
   rataan <- 10
   rataan
   ```
   Hasil:
   
   
   ```
   varian <- 10^2
   varian
   ```
   Hasil:
   
   
5. Diketahui bilangan acak (*random variable*) berdistribusi Eksponensial (λ = 3). Tentukan:  
   a. Fungsi Probabilitas dari Distribusi Eksponensial  
            
   
   ```
   set.seed(1); rexp(1,3)
   ```
   Hasil:
   
   
   b. Histogram dari Distribusi Eksponensial untuk 10, 100, 1000 dan 10000 bilangan random  
            
   
   ```
   set.seed(1); hist(rexp(10, 3))
   set.seed(1); hist(rexp(100, 3))
   set.seed(1); hist(rexp(1000, 3))
   set.seed(1); hist(rexp(10000, 3))
   ```
   Hasil:
   
   
   c.  Nilai rataan (μ) dan varian (σ²) dari Distribusi Eksponensial untuk n = 100 dan λ = 3  
      
   
   ```
   rataan <- 1/3
   rataan
   ```
   Hasil:
   
   
   ```
   varian <- 1/(3^2)
   varian
   ```
   Hasil:
   
   
6. Diketahui generate random nilai sebanyak 100 data, mean = 50, sd = 8. Tentukan:  
   a. Fungsi Probabilitas dari Distribusi Normal P(X1 ≤ x ≤ X2), hitung Z-Score Nya dan plot data generate randomnya dalam bentuk grafik  
            
   
   ```
   dbinom(4, 20, 0.2)
   ```
   Hasil:
   
   
   b. Generate Histogram dari Distribusi Normal dengan breaks 50 dan format penamaan: NRP_Nama_Probstat_{Nama Kelas}_DNhistogram  
            
   
   ```
   set.seed(1)
   a <- rnorm(100, 50, 8)
   a.z <- (a - 50)/8
   plot(a.z, type="o")  
   ```
   Hasil:
   
   
   c. Nilai Varian (σ²) dari hasil generate random nilai Distribusi Normal  
      
   
   ```
   rataan <- 8^2
   rataan
   ```
   Hasil:
   
   
