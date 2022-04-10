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
   ![image](https://user-images.githubusercontent.com/80016547/162620391-84d15bbe-2d51-49c5-9a5a-30cbaa85169c.png)
   
   
   b. Mean Distribusi Geometrik dengan 10.000 data random, prob = 0.20 dimana Distribusi Geometrik acak tersebut x = 3  
   
   ```
   set.seed(1); mean(rgeom(10000,0.20)==3)
   ```  
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620490-c64a7ccd-f6d6-4f9f-a19e-ee77880468bb.png)
   
   
   c. Bandingkan hasil poin a dan b, apa kesimpulan yang bisa didapatkan?  
   
   ```
   a = 0.1024, b = 0.0993, hasil a menunjukkan peluang kegagalan sebanyak tiga kali sebelum berhasil, sedangkan b menunjukkan rata-rata kegagalan yang terjadi sebelum berhasil.
   ```
   
   d. Histogram Distribusi Geometrik, peluang x = 3 gagal sebelum sukses pertama  
      
   
   ```
   hist(dgeom(3, 0.20))
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620575-670b7020-15c5-47ac-8852-8bbef20cbf3b.png)
   
   
   e. Nilai rataan (μ) dan varian (σ²) dari Distribusi Geometrik  
      
   
   ```
   rataan <- (1-0.2)/0.2
   rataan
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620517-45ee6370-50c2-4415-b936-6d79657b5eb0.png)
   
   ```
   varian <- (1-0.2)/(0.2^2)
   varian
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620541-05a204f0-0a2b-4dc8-8b74-39d3e6ed4606.png)   
   
2. Terdapat 20 pasien menderita Covid19 dengan peluang sembuh sebesar 0.2. Tentukan:  
   a. Peluang terdapat 4 pasien yang sembuh  
         
   
   ```
   dbinom(4, 20, 0.2)
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620689-bd8468bb-50bf-4193-9436-68792e5fb378.png)

   
   b. Gambarkan grafik histogram berdasarkan kasus tersebut  
            
   
   ```
   hist(dbinom(4, 20, 0.2))
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620748-2255c45b-5efe-4cfc-a1a3-8d75c51db80e.png)

   
   c. Nilai rataan (μ) dan varian (σ²) dari Distribusi Binomial  
      
   
   ```
   rataan <- 20*0.2
   rataan
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620709-098c97cd-7ef7-4633-b5e0-9735fff3eadb.png)

   
   ```
   varian <- 20*0.2*0.8
   varian
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620724-3685fb72-9c77-4423-9af2-df449bd0f5a5.png)

   
3. Diketahui data dari sebuah tempat bersalin di rumah sakit tertentu menunjukkan rata-rata historis 4,5 bayi lahir di rumah sakit ini setiap hari  
   a. Berapa peluang bahwa 6 bayi akan lahir di rumah sakit ini besok?  
            
   
   ```
   dpois(6, 4.5)
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620980-80885923-0893-43d5-aad7-5018da021748.png)

   
   b. Simulasikan dan buatlah histogram kelahiran 6 bayi akan lahir di rumah sakit ini selama setahun (n = 365)  
            
   
   ```
   set.seed(1); hist(rpois(365,4.5), xlim=c(6.01, 6.99)
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162620952-06b32c3b-df46-4fce-8922-0db8429a97bb.png)

   
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
   ![image](https://user-images.githubusercontent.com/80016547/162621000-fe249082-32da-44d1-9cd6-b51a9b5a0c8e.png)

   
   ```
   varian <- 4.5
   varian
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621012-f3b5a7b6-2b6a-4dd2-9154-e941a57a48fb.png)

   
4. Diketahui nilai x = 2 dan v = 10. Tentukan:  
   a. Fungsi probabilitas dari Distribusi Chi-Square  
            
   
   ```
   dchisq(2, 10)
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621098-98f20865-9a7d-4e6a-9635-44437d38c1cd.png)

   
   b. Histogram dari Distribusi Chi-Square dengan 100 data random  
            
   
   ```
   set.seed(1); hist(rchisq(100, 10))
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621072-080d7e5a-6378-4f6a-a36b-8c8c0c8a1a2d.png)

   
   c. Nilai rataan (μ) dan varian (σ²) dari Distribusi Chi-Square  
        
   
   ```
   rataan <- 10
   rataan
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621105-1360909e-18cb-4992-8240-ee5e81fc009d.png)

   
   ```
   varian <- 10^2
   varian
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621112-524c6e64-6461-49dd-b7d1-4ffba2337768.png)

   
5. Diketahui bilangan acak (*random variable*) berdistribusi Eksponensial (λ = 3). Tentukan:  
   a. Fungsi Probabilitas dari Distribusi Eksponensial  
            
   
   ```
   set.seed(1); rexp(1,3)
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621531-0564c02b-81b3-471f-a8f2-5313155268e6.png)

   
   b. Histogram dari Distribusi Eksponensial untuk 10, 100, 1000 dan 10000 bilangan random  
            
   
   ```
   set.seed(1); hist(rexp(10, 3))
   set.seed(1); hist(rexp(100, 3))
   set.seed(1); hist(rexp(1000, 3))
   set.seed(1); hist(rexp(10000, 3))
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621981-332125d9-183f-4cec-a421-ceece950c344.png)  
   ![image](https://user-images.githubusercontent.com/80016547/162622493-d68d8493-8ab0-45a0-86ed-83095ef8a314.png)  
   ![image](https://user-images.githubusercontent.com/80016547/162622669-c165a712-36af-40d2-9b37-8371ba6f9266.png)
   ![image](https://user-images.githubusercontent.com/80016547/162622804-f8eb2f48-03da-4e6b-97e6-4eb98e122c61.png)

   
   c.  Nilai rataan (μ) dan varian (σ²) dari Distribusi Eksponensial untuk n = 100 dan λ = 3  
      
   
   ```
   rataan <- 1/3
   rataan
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621748-b3955840-1ee1-4ae5-a82d-7c785f775709.png)

   
   ```
   varian <- 1/(3^2)
   varian
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621794-cfc19018-706f-4405-bc13-dbeb90d6abef.png)

   
6. Diketahui generate random nilai sebanyak 100 data, mean = 50, sd = 8. Tentukan:  
   a. Fungsi Probabilitas dari Distribusi Normal P(X1 ≤ x ≤ X2), hitung Z-Score Nya dan plot data generate randomnya dalam bentuk grafik  
            
   
   ```
   set.seed(1)
   a <- rnorm(100, 50, 8)
   a.z <- (a - 50)/8
   plot(a.z, type="o")
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621161-1efafa74-f3af-4910-8378-67ac6e454416.png)

   
   b. Generate Histogram dari Distribusi Normal dengan breaks 50 dan format penamaan: NRP_Nama_Probstat_{Nama Kelas}_DNhistogram  
            
   
   ```
   library(rcompanion)
   plotNormalHistogram(a, main="5025201174_Selfira Ayu Sheehan_Probstat_D_DNHistogram", breaks = 50)
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621316-a7559e3e-7dc8-4a57-a3a2-d856b7fae9cc.png)

   
   c. Nilai Varian (σ²) dari hasil generate random nilai Distribusi Normal  
      
   
   ```
   rataan <- 8^2
   rataan
   ```
   Hasil:  
   ![image](https://user-images.githubusercontent.com/80016547/162621361-a3a1844d-e1b0-4f38-a8bb-c5692e3fbeeb.png)
