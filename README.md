
![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/07dabd27-eff8-4c32-b8a5-f398669063d9)


# Tutorial Google Cloud Platform: Dari Nol Hingga Mahir dengan GCP

Selamat datang di tutorial Google Cloud Platform (GCP) dari nol hingga mahir! Artikel ini akan membimbing Anda dalam memahami konsep dasar dan mahir menggunakan Google Cloud Platform untuk berbagai kebutuhan, mulai dari desain platform analitik permainan mobile hingga pengelolaan sumber daya dan data besar. Mari kita mulai!

## Apa itu Google Cloud Platform (GCP)?

Google Cloud Platform (GCP) adalah rangkaian layanan komputasi awan yang ditawarkan oleh Google. GCP memungkinkan Anda untuk membangun, mengelola, dan mengoptimalkan berbagai jenis aplikasi dan layanan melalui infrastruktur Google yang aman dan skalabel.

### Mengapa GCP Penting?

GCP memiliki banyak keunggulan, seperti:

- **Biaya Fleksibel**: Anda hanya membayar untuk sumber daya yang digunakan.
- **Skalabilitas**: Mudah untuk menyesuaikan dengan kebutuhan Anda.
- **Layanan Analitik dan Machine Learning**: Mendukung pengembangan aplikasi cerdas dengan dukungan analitik data dan pembelajaran mesin.
- **Manajemen Sumber Daya**: Memungkinkan pengelolaan dan organisasi yang efisien.
- **Kinerja Tinggi**: GCP menawarkan kinerja komputasi dan jaringan yang andal.

## Bagian 1: Memulai dengan Google Cloud Platform

### Membuat Akun GCP Gratis

Anda dapat memulai perjalanan Anda di GCP dengan mendaftar untuk akun gratis dengan masa percobaan selama 3 bulan dan kredit sebesar $300. Ini memungkinkan Anda untuk mencoba layanan GCP tanpa biaya awal. Setelah masa percobaan selesai, Anda tidak akan dikenakan biaya kecuali Anda memutuskan untuk meningkatkan paket Anda.

Untuk memaksimalkan manfaat dari masa percobaan ini, Anda disarankan untuk:

- **Mencoba Sendiri**: Belajar dengan mencoba langsung, menghadapi masalah, dan memperbaikinya.
- **Praktik**: Menggunakan GCP untuk menjalankan aplikasi dan eksperimen.
- **Eksplorasi**: Mempelajari dokumentasi resmi dan mencoba berbagai layanan.

### Mengapa Migrasi ke GCP?

GCP menawarkan berbagai keuntungan bagi bisnis dan pengembang:

- **Biaya Rendah**: Tidak perlu investasi besar untuk perangkat keras.
- **Skalabilitas**: Dapat disesuaikan dengan permintaan, membayar hanya untuk yang Anda gunakan.
- **Proof of Concept**: Cepat membuat konsep baru dengan cepat.
- **Layanan Analitik dan Pembelajaran Mesin**: Mendukung pengembangan aplikasi cerdas.

## Bagian 2: Mengoptimalkan Biaya dengan GCP

### Menyusun Mesin Virtual (VM) dengan Efisien

Ada beberapa cara untuk mengoptimalkan biaya saat menggunakan mesin virtual di GCP:

- **Custom Machine Types**: Pilih tipe mesin yang sesuai dengan kebutuhan RAM dan CPU Anda.
- **Preemptible VM's**: Gunakan mesin virtual preemptible untuk menghemat biaya hingga 80%. Ini cocok untuk aplikasi yang tidak kritis.
- **Sustained Use Discounts**: Semakin lama Anda menggunakan VM atau Cloud SQL instances, semakin besar diskonnya.
- **Committed Use Discounts**: Dapatkan diskon hingga 57% dengan berkomitmen untuk CPU dan RAM dalam periode tertentu.

### Mengelola Sumber Daya di GCP

Pengelolaan sumber daya di GCP melibatkan hierarki sumber daya yang terdiri dari organisasi, proyek, folder, dan sumber daya itu sendiri. Pengaturan ini membantu dalam mengelola akses, konfigurasi, dan pengaturan sumber daya.

- **Resource Hierarchy**: Terdapat empat jenis sumber daya yang dapat dikelola melalui Resource Manager: organisasi, proyek, folder, dan sumber daya.
  ![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/4672c1d3-61e7-4d28-80b5-7db9d1f029c6)

  

- **Labels**: Labels adalah pasangan kunci-nilai yang membantu mengorganisir sumber daya Anda. Gunakan labels untuk mengelompokkan dan memfilter sumber daya.
- **Cloud IAM**: Cloud IAM mengontrol siapa yang dapat melakukan apa pada sumber daya. Pengaturan ini didasarkan pada peran dan izin.

  ![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/4ca17a58-f166-434a-9a7b-371cfc25b087)


**Identities**
Akun G Suite Domain adalah jenis akun yang dapat Anda gunakan untuk mengidentifikasi organisasi. Jika organisasi Anda sudah menggunakan Active Directory, Anda dapat menyinkronkannya dengan Cloud IAM menggunakan Cloud Identity.

`allAuthenticatedUsers` digunakan untuk mewakili pengguna yang diautentikasi dalam GCP.

`allUsers` digunakan untuk mewakili siapa pun, baik yang sudah diautentikasi maupun belum.

Terkait akun layanan, beberapa praktik terbaik dari Google meliputi:

1. **Tidak Menggunakan Akun Layanan Default**
2. **Menerapkan Prinsip Privilege yang Paling Rendah**
   - Memperbolehkan siapa saja yang dapat berperan sebagai akun layanan.
   - Memberikan hanya kumpulan izin minimum yang diperlukan oleh akun tersebut.
   - Membuat akun layanan untuk setiap layanan dengan izin yang diperlukan oleh akun tersebut.

**Roles (Peran)**
Peran adalah kumpulan izin. Ada tiga jenis peran:

1. **Primitive (Primitif)**: Peran GCP asli yang berlaku untuk seluruh proyek. Ada tiga peran dasar: Viewer, Editor, dan Owner. Editor berisi Viewer dan Owner berisi Editor.
2. **Predefined (Tersedia Awal)**: Memberikan akses ke layanan tertentu, misalnya, `storage.admin`.
3. **Custom (Kustom)**: Memungkinkan Anda membuat peran sendiri dengan menggabungkan izin tertentu yang Anda butuhkan.

Ketika memberikan peran, ikuti prinsip privilege yang paling rendah juga. Secara umum, lebih baik menggunakan peran yang tersedia awal daripada peran primitif.

**Cloud Deployment Manager**
Cloud Deployment Manager mengotomatisasi tugas yang dapat diulang seperti penyediaan, konfigurasi, dan penyebaran untuk banyak mesin.

Ini adalah layanan "Infrastructure as Code" Google, mirip dengan Terraform - meskipun Anda hanya dapat mendeploy sumber daya GCP. Ini digunakan oleh GCP Marketplace untuk membuat penyebaran yang telah dikonfigurasi sebelumnya.

Anda mendefinisikan konfigurasi Anda dalam file YAML, yang mencantumkan sumber daya yang ingin Anda buat (dibuat melalui panggilan API) dan properti mereka. Sumber daya didefinisikan oleh nama (VM-1, disk-1), tipe (compute.v1.disk, compute.v1.instance), dan properti (zone:europe-west4, boot:false).

Untuk meningkatkan kinerja, sumber daya dideploy secara paralel. Oleh karena itu, Anda perlu menentukan ketergantungan apa pun menggunakan referensi. Misalnya, jangan membuat mesin virtual VM-1 sampai persistent disk disk-1 telah dibuat. Sebaliknya, Terraform akan menentukan ketergantungan secara otomatis.

Anda dapat memodularkan file konfigurasi Anda menggunakan template sehingga dapat diperbarui dan dibagikan secara independen. Template dapat didefinisikan dalam Python atau Jinja2. Konten template Anda akan di-inline dalam file konfigurasi yang merujuk pada mereka.

Cloud Deployment Manager akan membuat manifest yang berisi konfigurasi asli Anda, semua template yang telah Anda impor, dan daftar diperluas dari semua sumber daya yang ingin Anda buat.

**Cloud Operations (dahulu Stackdriver)**
![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/2652e37a-b9cb-4401-8f1a-8d212a880f66)

Cloud Operations menyediakan seperangkat alat untuk memantau, mengelola log, debugging, pelaporan kesalahan, profil, dan pelacakan sumber daya di GCP, AWS, dan bahkan on-premise.

**Cloud Logging**
Cloud Logging adalah solusi terpusat GCP untuk manajemen log secara real-time. Untuk setiap proyek Anda, itu memungkinkan Anda untuk menyimpan, mencari, menganalisis, memantau, dan memberikan peringatan pada data logging:

Secara default, data akan disimpan selama periode waktu tertentu. Periode retensi bervariasi tergantung pada jenis log. Anda tidak dapat mengambil log setelah melewati periode retensi ini.
Log dapat diekspor untuk tujuan yang berbeda. Untuk melakukannya, Anda membuat sink, yang terdiri dari filter (untuk memilih apa yang ingin Anda log) dan tujuan: Google Cloud Storage (GCS) untuk retensi jangka panjang, BigQuery untuk analisis, atau Pub/Sub untuk streaming ke aplikasi lain.
Anda dapat membuat metrik berbasis log di Cloud Monitoring dan bahkan mendapatkan peringatan ketika ada masalah.
Log adalah kumpulan entri log. Entri log mencatat status atau acara dan mencakup nama log-nya, misalnya, `compute.googleapis.com/activity`. Ada dua jenis utama log:

- User Logs: Dibuat oleh aplikasi dan layanan Anda. Mereka ditulis ke Cloud Logging menggunakan API Cloud Logging, pustaka klien, atau agen logging yang diinstal pada mesin virtual Anda.
- Security logs: Dibagi menjadi:

  - Audit logs, untuk perubahan administratif****


## Bagian 3: Penyimpanan Data di GCP

### Menggunakan Google Cloud Storage (GCS)

Google Cloud Storage adalah layanan penyimpanan Google untuk data tak terstruktur seperti gambar, video, berkas, dan lainnya. Data ditempatkan dalam "buckets" dan dapat dikelola dengan perizinan dan kelas penyimpanan tertentu.
![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/f00190b7-621f-4a99-9462-5b3694c99f9e)

- **Objects dan Buckets**: Data disimpan dalam "objects" yang ditempatkan dalam "buckets".
- **Storage Classes**: Penyimpanan kelas memungkinkan Anda memilih SLA penyimpanan yang sesuai dengan kebutuhan Anda.
- **Object Lifecycle Management**: Anda dapat menentukan aturan yang mengatur tindakan pada suatu objek saat kondisi tertentu terpenuhi.

Dalam tutorial ini, Anda akan mempelajari langkah-langkah awal dalam memulai dengan Google Cloud Platform, mengoptimalkan biaya dengan bijak, serta mengelola dan menyimpan data secara efisien.

``
{
   "lifecycle":{
      "rule":[
         {
            "action":{
               "type":"Delete"
            },
            "condition":{
               "age":30,
               "isLive":true
            }
         },
         {
            "action":{
               "type":"Delete"
            },
            "condition":{
               "numNewerVersions":2
            }
         },
         {
            "action":{
               "type":"Delete"
            },
            "condition":{
               "age":180,
               "isLive":false
            }
         }
      ]
   }
}
``

Permissions in GCS (Lanjutan)
Selain peran IAM, Anda juga dapat menggunakan Access Control Lists (ACLs) untuk mengelola akses ke sumber daya dalam sebuah bucket.

Gunakan peran IAM jika memungkinkan, tetapi ingatlah bahwa ACL memberikan akses ke bucket dan objek individu, sementara peran IAM adalah izin yang berlaku di seluruh proyek atau bucket. Kedua metode ini bekerja bersamaan.

Untuk memberikan akses sementara kepada pengguna di luar GCP, Anda dapat menggunakan Signed URLs.

Bucket Lock (Kunci Bucket)
Bucket lock memungkinkan Anda menerapkan periode retensi minimum untuk objek dalam sebuah bucket. Anda mungkin memerlukan ini untuk tujuan audit atau hukum.

Setelah bucket dikunci, itu tidak dapat dibuka kembali. Untuk menghapusnya, Anda harus terlebih dahulu menghapus semua objek dalam bucket, yang hanya dapat Anda lakukan setelah semua objek mencapai periode retensi yang ditentukan oleh kebijakan retensi. Hanya setelah itu, Anda dapat menghapus bucket.

Anda dapat menyertakan kebijakan retensi saat Anda membuat bucket atau menambahkan kebijakan retensi ke bucket yang sudah ada (ini juga berlaku secara retrospektif untuk objek yang sudah ada dalam bucket).

Fakta menarik: periode retensi maksimum adalah 100 tahun.

Relational Managed Databases in GCP
Cloud SQL dan Cloud Spanner adalah dua layanan database yang dikelola yang tersedia di GCP. Jika Anda tidak ingin berurusan dengan semua pekerjaan yang diperlukan untuk menjaga database online, mereka adalah pilihan yang bagus. Anda selalu dapat membuat mesin virtual dan mengelola database Anda sendiri.

Cloud SQL
Cloud SQL memberikan akses ke instans database MySQL atau PostgreSQL yang dikelola di GCP. Setiap instans terbatas pada satu wilayah (region) dan memiliki kapasitas maksimum 30 TB.

Google akan mengurus instalasi, cadangan, skalabilitas, pemantauan, failover, dan replika baca. Untuk alasan ketersediaan, replika harus didefinisikan di wilayah yang sama tetapi zona yang berbeda dari instans utama.

Data dapat dengan mudah diimpor (dengan mengunggah data ke Google Cloud Storage terlebih dahulu, kemudian ke instans) dan diekspor menggunakan SQL dumps atau format file CSV. Data dapat dikompres untuk mengurangi biaya (Anda dapat mengimpor file .gz secara langsung). Untuk migrasi "lift and shift," ini adalah pilihan yang bagus.

Jika Anda memerlukan ketersediaan global atau lebih banyak kapasitas, pertimbangkan menggunakan Cloud Spanner.

Cloud Spanner
Cloud Spanner tersedia secara global dan dapat dengan baik meliputi skala (horizontal).

Dua fitur ini membuatnya mampu mendukung kasus penggunaan yang berbeda dari Cloud SQL dan juga lebih mahal. Cloud Spanner bukanlah pilihan untuk migrasi "lift and shift."

NoSQL Managed Databases in GCP
Demikian pula, GCP menyediakan dua database NoSQL yang dikelola, Bigtable dan Datastore, serta layanan database in-memory, Memorystore.

Datastore
Datastore adalah database dokumen yang sangat skalabel yang tidak memerlukan operasi yang rumit, ideal untuk aplikasi web dan mobile: status permainan, katalog produk, persediaan real-time, dan sebagainya. Cocok untuk:

Profil pengguna - aplikasi mobile
Status simpan permainan
Secara default, Datastore memiliki indeks bawaan yang meningkatkan kinerja pada kueri sederhana. Anda dapat membuat indeks Anda sendiri, disebut indeks komposit, yang didefinisikan dalam format YAML.

Jika Anda memerlukan throughput ekstrim (jumlah besar baca/tulis per detik), gunakan Bigtable sebagai gantinya.

Bigtable
Bigtable adalah database NoSQL yang ideal untuk beban kerja analitis di mana Anda dapat mengharapkan volume tulis yang sangat tinggi, baca dalam hitungan milidetik, dan kemampuan untuk menyimpan informasi dalam terabyte hingga petabyte. Cocok untuk:

Analisis keuangan
Data IoT
Data pemasaran
Bigtable memerlukan pembuatan dan konfigurasi node Anda sendiri (berbeda dengan Datastore atau BigQuery yang sepenuhnya dikelola). Anda dapat menambahkan atau menghapus node dari kluster Anda tanpa waktu henti. Cara paling sederhana untuk berinteraksi dengan Bigtable adalah dengan perangkat baris perintah cbt.

Kinerja Bigtable akan tergantung pada desain skema database Anda.

Anda hanya dapat mendefinisikan satu kunci per baris dan harus menyimpan semua informasi yang terkait dengan entitas dalam baris yang sama. Pikirkan ini seperti tabel hash.
Tabel adalah langka: jika tidak ada informasi yang terkait dengan kolom, tidak ada ruang yang diperlukan.
Untuk membuat pembacaan lebih efisien, coba simpan entitas terkait dalam baris yang berdekatan.

Karena topik ini sepadan dengan artikel tersendiri, saya sarankan Anda membaca dokumentasinya.

Memorystore
Memorystore menyediakan versi yang dikelola dari Redis dan Memcache (database in-memory), menghasilkan kinerja yang sangat cepat. Instans bersifat regional, seperti Cloud SQL, dan memiliki kapasitas hingga 300 GB.

Bagaimana Memilih Database Anda
Google menyukai pohon keputusan. Ini akan membantu Anda memilih database yang tepat untuk proyek Anda. Untuk data yang tidak terstruktur, pertimbangkan GCS atau prosesnya menggunakan Dataflow (akan dibahas nanti).

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/33e347cd-9a31-4b3e-bd48-c89fa5cad241)


**Jaringan di GCP**

**Virtual Private Cloud (VPC)**

Infrastruktur jaringan GCP dibagi menjadi wilayah (regions), zona (zones), dan titik akses tepi (edge points of presence). Komponen-komponen ini menyediakan jaringan yang tangguh dan efisien untuk menjalankan layanan.

- **Wilayah (Regions):** Ini adalah area geografis independen di mana Google meng-host pusat data. Setiap wilayah terdiri dari tiga atau lebih zona, dan setiap wilayah didesain untuk berjarak setidaknya 100 mil dari wilayah lainnya. Contohnya, "us-central1."

- **Zona (Zones):** Zona-zona adalah pusat data individu di dalam sebuah wilayah. Mereka dirancang untuk memberikan redundansi dan failover. Sebagai contoh, "us-central1-a."

- **Titik Akses Tepi (Edge Points of Presence):** Ini adalah titik-titik di mana jaringan Google terhubung dengan internet, memastikan pertukaran data yang efisien.

**Virtual Private Cloud (VPC)** memungkinkan Anda membangun jaringan Anda di atas infrastruktur Google. VPC adalah jaringan yang didefinisikan oleh perangkat lunak di mana konsep-konsep jaringan tradisional berlaku.

- **Subnet:** Subnet adalah partisi logis dari sebuah jaringan, yang didefinisikan menggunakan notasi CIDR. Mereka hanya berada di satu wilayah, tetapi bisa melintasi beberapa zona. Pastikan rentang CIDR tidak tumpang tindih di antara subnet.

- **Alamat IP:** Alamat IP bisa internal (untuk komunikasi pribadi di dalam GCP) atau eksternal (untuk komunikasi dengan internet). Alamat IP eksternal dapat bersifat sementara (ephemeral) atau tetap (static). Secara umum, Anda memerlukan alamat IP eksternal untuk terhubung ke layanan GCP. Namun, dalam beberapa kasus, Anda dapat mengonfigurasi akses privat untuk instansi yang hanya memiliki alamat IP internal.

**Peraturan Firewall:** Peraturan firewall digunakan untuk mengizinkan atau melarang lalu lintas ke mesin virtual Anda, baik masuk (ingress) maupun keluar (egress). Secara default, semua lalu lintas masuk diblokir dan semua lalu lintas keluar diizinkan. Peraturan firewall didefinisikan pada tingkat VPC, tetapi berlaku untuk instansi-individu atau kelompok instansi dengan menggunakan label jaringan (network tags) atau rentang IP.

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/d516fada-d090-419b-a59f-c2e56319ef9b)


**Shared VPC dan VPC Network Peering**

- **Shared VPC:** Shared VPC adalah cara untuk berbagi sumber daya antara proyek-proyek yang berbeda dalam satu organisasi. Ini memungkinkan Anda mengendalikan faktur dan mengelola akses ke sumber daya di berbagai proyek, mengikuti prinsip kebijakan paling sedikit. Tanpa Shared VPC, Anda harus menempatkan semua sumber daya di satu proyek tunggal. Shared VPC terdiri dari proyek tuan rumah (host project), proyek layanan (service project), dan proyek mandiri (standalone project).

- **VPC Network Peering:** VPC Network Peering bukanlah layanan GCP, tetapi Anda dapat menggunakannya untuk menghubungkan jaringan Anda ke jaringan Google dan mengakses layanan seperti Youtube, Drive, atau layanan GCP lainnya. Ini berguna saat Anda perlu menghubungkan ke Google tetapi tidak ingin melakukannya melalui internet publik. Dalam VPC Network Peering, Anda perlu memetakan alamat IP antara VPC yang terhubung.

**Menghubungkan Infrastruktur On-Premise dan GCP**

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/fed2f77e-29d3-4b39-a6b0-86d0eed1d494)


Ada tiga opsi untuk menghubungkan infrastruktur on-premise Anda ke GCP:

- **Cloud VPN:** Dengan Cloud VPN, lalu lintas Anda berjalan melalui internet publik melalui sebuah terowongan terenkripsi. Setiap terowongan memiliki kapasitas maksimum 3 Gbps dan Anda dapat menggunakan hingga 8 terowongan untuk kinerja yang lebih baik. Anda dapat mendefinisikan rute statis atau dinamis antara VPC Anda dan jaringan on-premise Anda.

- **Cloud Interconnect:** Dengan Cloud Interconnect, ada koneksi fisik langsung antara jaringan on-premise Anda dan VPC Anda. Ada dua jenis interkoneksi yang tersedia: Dedicated Interconnect dan Partner Interconnect. Dedicated Interconnect adalah koneksi langsung dengan kapasitas 10 hingga 200 Gbps, sedangkan Partner Interconnect melalui penyedia layanan dengan kecepatan 50 Mbps hingga 10 Gbps.

- **Cloud Peering:** Cloud Peering bukan layanan GCP, tetapi Anda dapat menggunakannya untuk menghubungkan jaringan Anda ke jaringan Google dan mengakses layanan seperti Youtube, Drive, atau layanan GCP lainnya. Ini berguna saat Anda perlu menghubungkan ke Google tetapi tidak ingin melakukannya melalui internet publik.

Dalam bagian berikutnya, saya akan membahas layanan database yang tersedia di Google Cloud Platform (GCP).

**Bagian 3 - Layanan Jaringan Lainnya dan Pemrosesan Data Besar di Google Cloud Platform (GCP)**

**Load Balancers di GCP**

Di GCP, load balancer adalah perangkat lunak yang mendistribusikan permintaan pengguna di antara sekelompok instance. Load balancer dapat memiliki beberapa backend yang terkait dengannya, dengan aturan untuk memutuskan backend yang sesuai untuk permintaan tertentu.

Ada berbagai jenis load balancer. Perbedaannya terletak pada jenis lalu lintas (HTTP vs TCP/UDP - Layer 7 atau Layer 4), apakah mereka menangani lalu lintas eksternal atau internal, dan apakah lingkupnya regional atau global:

- **HTTP(s) Load Balancer:** Load balancer global yang menangani permintaan HTTP(s), mendistribusikan lalu lintas ke berbagai wilayah berdasarkan lokasi pengguna (ke wilayah terdekat dengan instance yang tersedia) atau pemetaan URL (load balancer dapat dikonfigurasi untuk meneruskan permintaan ke URL/news ke layanan backend tertentu dan URL/videos ke yang lain). Load balancer ini dapat menerima lalu lintas IPv4 dan IPv6 (IPv6 dihentikan di tingkat load balancer dan diteruskan sebagai IPv4 ke backend) dan memiliki dukungan asli untuk WebSockets.
- **SSL Proxy Load Balancer:** Load balancer global yang menangani lalu lintas TCP yang dienkripsi, mengelola sertifikat SSL untuk Anda.
- **TCP Proxy Load Balancer:** Load balancer global yang menangani lalu lintas TCP yang tidak dienkripsi. Secara default, tidak akan mempertahankan alamat IP klien, tetapi ini bisa diubah.
- **Network Load Balancer:** Load balancer regional yang menangani lalu lintas eksternal TCP/UDP, berdasarkan alamat IP dan port.
- **Internal Load Balancer:** Mirip dengan Network LB, tetapi untuk lalu lintas internal.

**Cloud DNS**

**Cloud DNS** adalah layanan Domain Name System (DNS) yang dikelola oleh Google, baik untuk lalu lintas internal maupun eksternal (publik). Ini akan memetakan URL seperti https://www.freecodecamp.org/ ke alamat IP. Ini adalah satu-satunya layanan di GCP dengan SLA 100% - tersedia sepanjang waktu.

**Google Cloud CDN**

**Google Cloud CDN** adalah Jaringan Pengiriman Konten Google. Jika Anda memiliki data yang tidak sering berubah (gambar, video, CSS, dll.), Masuk akal untuk menyimpannya dekat dengan pengguna Anda. Cloud CDN menyediakan 90 Edge Point of Presence (POP) untuk menyimpan data dekat dengan pengguna akhir Anda.

Setelah permintaan pertama, data statis dapat disimpan di POP, biasanya jauh lebih dekat dengan pengguna Anda daripada server utama Anda. Dengan demikian, dalam permintaan berikutnya, Anda dapat mengambil data lebih cepat dari POP dan mengurangi beban pada server backend Anda.

**Tempat Anda Dapat Menjalankan Aplikasi di GCP**

Saya akan menyajikan 4 tempat di mana kode Anda dapat dijalankan di GCP:

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/fa9662f2-9d77-4232-8eae-c23565e90a71)


- **Google Compute Engine (GCE):** Mengizinkan Anda membuat mesin virtual di GCP. Ini adalah tempat di mana GKE dan GAE berjalan.
- **Google Kubernetes Engine (GKE):** Memudahkan Anda untuk menjalankan dan mengelola kluster Kubernetes di GCP.
- **App Engine:** Pilihan yang baik ketika Anda ingin fokus pada kode dan membiarkan Google mengelola infrastruktur Anda.
- **Cloud Functions:** Fungsi serverless yang memungkinkan Anda fokus pada kode tanpa khawatir tentang infrastruktur tempat kode akan dijalankan.

**Google Compute Engine (GCE)**

**Google Compute Engine** memungkinkan Anda membuat mesin virtual di GCP. GCE menyediakan infrastruktur tempat GKE dan GAE berjalan.

- **Disks:** Anda dapat menyimpan data VM Anda di Persistent disks, Local SSDs, atau Cloud Storage.
- **Snapshots:** Snapshots adalah cadangan disk Anda.
- **Images:** Images mengacu pada gambar sistem operasi yang diperlukan untuk membuat disk boot untuk instance Anda.
- **Instance Groups:** Instance groups memungkinkan Anda memperlakukan sekelompok instance sebagai satu kesatuan.
- **Security Best Practices:** Meliputi aspek keamanan untuk GCE, seperti Shielded VMs, menghindari akses dari internet publik, menggunakan gambar yang terpercaya, dan lainnya.

**App Engine**

**App Engine** merupakan pilihan yang baik ketika Anda ingin fokus pada kode dan membiarkan Google mengelola infrastruktur Anda. Ini cocok untuk berbagai penggunaan seperti website, aplikasi seluler, dan backend game.

- **Standard Environment:** Cepat dalam skalabilitas, namun hanya mendukung beberapa bahasa pemrograman.
- **Flexible Environment:** Lebih fleksibel daripada Standard Environment, cocok untuk lalu lintas yang lebih konsisten.

**Google Kubernetes Engine (GKE)**

**Google Kubernetes Engine** adalah layanan yang memudahkan Anda untuk menjalankan dan mengelola kluster Kubernetes di GCP.

**Cloud Functions**

**Cloud Functions** adalah fungsi serverless yang memungkinkan Anda fokus pada kode dan tidak perlu khawatir tentang infrastruktur.

**Big Data di GCP**

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/a809f27b-554b-4dec-96e3-dcd2ca9bfa00)


**BigQuery:** BigQuery adalah data warehousing berbasis serverless yang menyediakan kemampuan analitik untuk database skala petabyte.

**Pub/Sub:** Pub/Sub adalah antrian pesan yang dikelola sepenuhnya, memungkinkan Anda untuk mengontrol akses aplikasi GCP melalui HTTPs tanpa menginstal perangkat lunak VPN.

**Cloud Dataflow:** Cloud Dataflow adalah layanan dikelola untuk pemrosesan data stream dan batch, berbasis Apache Beam.

**Cloud Dataproc:** Cloud Dataproc adalah ekosistem Hadoop dan Spark yang dikelola oleh Google.

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/aae1b79f-284d-4ccf-886d-9cc2e6f9ae0e)

**Cloud Composer:** Cloud Composer adalah layanan manajemen alur kerja berbasis Apache Airflow.

**AI dan Machine Learning di GCP**

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/d60edf29-379d-4e54-b1a7-9063b0b146d1)


- **AI Platform:** AI Platform menyediakan platform yang dikelola sepenuhnya untuk menggunakan perpustakaan pembelajaran mesin seperti TensorFlow.
- **Cloud AutoML:** Google memungkinkan Anda menggunakan data Anda untuk melatih model mereka.
  
**Eksplorasi dan Visualisasi Data di GCP**

- **Cloud Data Studio:** Data Studio memungkinkan Anda membuat visualisasi dan dasbor berdasarkan data yang ada di layanan Google dan GCP.
- **Cloud Datalab:**

 Datalab memungkinkan Anda menjelajahi, menganalisis, dan memvisualisasikan data di berbagai layanan GCP.
  
**Keamanan di GCP**

![image](https://github.com/aslich86/Tutorial-GCP/assets/74340158/ad78384a-effd-481a-98ee-7903f1e622d5)


- **Enkripsi di Google Cloud Platform:** Data di GCP dienkripsi baik saat beristirahat (data yang disimpan di disk) maupun saat transit (data yang bergerak di jaringan).
- **Cloud Key Management Service (KMS):** KMS adalah layanan yang memungkinkan Anda mengelola kunci enkripsi Anda.
- **Identity-Aware Proxy (IAP):** IAP memungkinkan Anda mengontrol akses aplikasi GCP melalui HTTPs tanpa instalasi perangkat lunak VPN.
- **Cloud Armor:** Cloud Armor melindungi infrastruktur Anda dari serangan DDoS.
- **Cloud Data Loss Prevention:** Data Loss Prevention adalah layanan yang dirancang untuk membantu Anda menemukan, mengklasifikasikan, dan melindungi data sensitif.
- **VPC Service Control:** VPC Service Control membantu mencegah eksfiltrasi data dengan mendefinisikan batas di sekitar sumber daya yang ingin Anda lindungi.
- **Cloud Web Security Scanner:** Cloud Web Security Scanner memindai aplikasi yang berjalan di GCP untuk kerentanannya.

**Sumber Daya Tambahan di GCP**

- Google Cloud Solutions Architecture Reference
- GCP solutions by industry
- GCP Youtube channel
- GCP Labs
