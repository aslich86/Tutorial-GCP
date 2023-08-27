# Fundamental Cloud Computing

Cloud Computing? Penjelasan untuk Pemula

Anda mungkin tidak selalu menyadarinya, tetapi Anda menikmati banyak manfaat dari cloud hampir setiap jam setiap hari. Banyak kegembiraan (dan kengerian) dalam kehidupan modern tidak mungkin terjadi tanpanya.

Sebelum kita membicarakan apa yang dilakukannya dan ke mana arahnya, kita harus menjelaskan apa itu sebenarnya.

**Apa Itu Cloud?**
"Cloud" berkaitan dengan penggunaan komputer milik orang lain daripada milik Anda sendiri. Itu saja. Tidak, benar-benar.

Penyedia cloud menjalankan banyak server komputasi (yang hanyalah komputer yang ada untuk "melayani" aplikasi dan data sebagai respons terhadap permintaan eksternal), perangkat penyimpanan, dan perangkat keras jaringan. Kapan pun Anda mau, Anda bisa menyewa unit-unit dari server, perangkat, dan kapasitas jaringan tersebut untuk beban kerja Anda sendiri.

Ketika Anda menambahkan jutaan pengguna lain yang memiliki keinginan serupa, Anda mendapatkan cloud modern.

Untuk banyak aplikasi - meskipun tidak semuanya - ada manfaat besar dalam hal biaya dan kinerja yang bisa dicapai dengan mendeploy ke cloud. Dan banyak aplikasi - baik yang kecil, besar, atau sangat besar - telah menemukan tempat yang produktif di satu platform cloud atau yang lain.

Jadi mari kita lihat bagaimana semuanya bekerja dan apa yang mungkin Anda bisa lakukan dengannya.

**Model Penempatan Server Aplikasi**
Selama beberapa dekade, kita telah melalui sejumlah model untuk menjalankan beban kerja server. Secara umum, semua perubahan ini adalah hasil dari hanya dua teknologi:

1. Protokol jaringan yang memungkinkan komunikasi antara node yang terhubung.
2. Virtualisasi yang memungkinkan penggunaan sumber daya perangkat keras secara cepat, efisien, dan hemat biaya untuk penggunaan ganda dan paralel.

Jaringan, terutama karena sekarang menjadi teknologi yang stabil dan mapan, bukanlah sesuatu yang akan kita fokuskan di sini. Tapi kita akan kembali membahas virtualisasi sedikit lebih lanjut.

Bagaimana Pusat Data Lokal Bekerja
Di zaman dulu, jika Anda ingin menjalankan server baru untuk melakukan tugas komputasi, itu adalah proses yang cukup rumit.

Anda akan menghabiskan waktu seminggu atau lebih menghitung berapa banyak daya komputasi yang Anda butuhkan untuk pekerjaan Anda, menghubungi perwakilan penjualan beberapa vendor perangkat keras, menunggu mereka memberi Anda tawaran penawaran, dan kemudian membandingkan penawaran tersebut. Lalu, setelah Anda memilih satu, Anda akan menunggu beberapa minggu lain agar perangkat keras baru Anda dikirimkan. Kemudian Anda akan merangkai semua komponen, memasang semuanya, dan mulai memuat perangkat lunak.

Ruangan tempat server Anda berjalan akan memerlukan pasokan listrik yang andal dan tangguh serta sistem pendinginan: seperti anak-anak yang marah, server menghasilkan panas yang cukup banyak tetapi tidak menyukai kondisi panas. Anda mungkin tidak ingin melakukan pekerjaan lain di ruangan itu, karena suara kipas pendingin internal yang kuat dari server Anda akan sulit diabaikan.

Sementara server yang ditempatkan secara lokal memberi Anda kendali langsung dan manual atas perangkat keras Anda yang Anda butuhkan, hal ini datang dengan biaya.

Satu hal, peluang untuk redundansi infrastruktur (dan kehandalan yang datang bersamanya) terbatas. Terlepas dari segalanya, bahkan jika Anda secara teratur membackup data Anda (dan berasumsi backup Anda andal), mereka masih tidak akan melindungi Anda dari insiden yang melibatkan seluruh fasilitas seperti kebakaran yang menghancurkan.

Anda juga perlu mengelola jaringan Anda sendiri, sesuatu yang mungkin sangat sulit - dan berisiko - ketika klien jarak jauh memerlukan akses dari luar bangunan Anda.

Oh ya, jangan tertipu oleh penggunaan waktu lampau saya di sini ("terbatas," "dibackup"). Masih banyak beban kerja dari semua ukuran yang dengan senang hati berjalan di pusat data on-premises. Tapi trennya, tanpa keraguan, bergerak ke arah yang berbeda.


**Apa Itu Virtualisasi?**
Seperti yang saya sebutkan sebelumnya, virtualisasi adalah teknologi yang, lebih dari yang lain, mendefinisikan internet modern dan banyak layanan yang memungkinkannya.

Pada intinya, virtualisasi adalah trik perangkat lunak cerdas yang memungkinkan Anda meyakinkan sistem operasi bahwa ia sendirian di atas komputer fisik yang kosong, padahal sebenarnya ia hanya satu dari banyak sistem operasi yang berbagi satu set sumber daya fisik.

Sistem operasi virtual akan diberikan ruang pada disk penyimpanan virtual, bandwidth melalui antarmuka jaringan virtual, dan memori dari modul RAM virtual.

Inilah mengapa itu sangat penting. Misalkan disk penyimpanan pada server host Anda memiliki kapasitas total dua terabyte dan Anda memiliki 64GB RAM. Anda mungkin membutuhkan 10GB penyimpanan dan 10GB RAM untuk sistem operasi host (atau hypervisor seperti yang disebut beberapa host virtualisasi).

Ini meninggalkan Anda banyak ruang untuk instance sistem operasi virtual Anda. Anda dapat dengan mudah menjalankan beberapa instance virtual, masing-masing dialokasikan sumber daya yang cukup untuk menyelesaikan pekerjaan individunya.

Ketika suatu instance tidak lagi diperlukan, Anda dapat mematikannya, melepaskan sumber daya sehingga mereka akan langsung tersedia untuk instance lain yang menjalankan tugas lain.

Namun, manfaat sebenarnya datang dari cara virtualisasi dapat sangat efisien dengan sumber daya Anda. Satu instance bisa, katakanlah, diberikan RAM dan penyimpanan yang kemudian terbukti tidak mencukupi. Anda dapat dengan mudah mengalokasikan lebih banyak dari masing-masing dari pool tersebut - seringkali tanpa harus mematikan instance Anda. Demikian pula, Anda dapat mengurangi alokasi untuk instance saat kebutuhannya menurun.

Ini menghilangkan semua spekulasi dalam perencanaan server. Anda hanya perlu membeli (atau menyewa) sumber daya perangkat keras generik dan menetapkan mereka dalam unit inkremental sesuai kebutuhan. Tidak lagi perlu melihat ke masa depan jauh ketika Anda mencoba untuk memperkirakan apa yang akan Anda lakukan dalam lima tahun. Lima menit sudah lebih dari cukup untuk perencanaan.

Bayangkan semua ini terjadi dalam skala yang jauh lebih besar: Misalkan Anda memiliki ribuan server yang berjalan di gudang suatu tempat yang melayani beban kerja untuk ribuan pelanggan. Mungkin satu pelanggan tiba-tiba meminta terabyte penyimpanan tambahan.

Bahkan jika disk yang digunakan pelanggan tersebut sudah penuh, Anda dengan mudah dapat menambahkan terabyte lain dari disk lain, mungkin yang terpasang beberapa ratus meter di seberang gudang. Pelanggan tidak akan pernah tahu perbedaannya, tetapi perubahan itu bisa hampir instan.

**Cattle vs Pets**
Virtualisasi server telah mengubah cara kita melihat komputasi dan bahkan pengembangan perangkat lunak.

Tidak lagi penting untuk membangun antarmuka konfigurasi ke dalam aplikasi Anda yang akan memungkinkan Anda untuk mengatur dan memperbaiki hal-hal secara cepat. Seringkali lebih efektif bagi pengembang dan administrator sistem Anda untuk membangun citra sistem operasi khusus (biasanya berbasis Linux) dengan semua perangkat lunak yang telah diatur sebelumnya. Anda kemudian dapat meluncurkan instance virtual baru berdasarkan citra Anda setiap kali perlu ada pembaruan.

Jika ada yang salah atau Anda perlu menerapkan perubahan, Anda hanya perlu membuat citra baru, mematikan instance Anda, dan kemudian menggantinya dengan instance yang menjalankan citra baru Anda.

Pada dasarnya, Anda memperlakukan server virtual Anda seperti peternak susu memperlakukan sapi: ketika waktunya tiba (seperti yang pasti akan terjadi), Anda menggantikan sapi tua atau sakit, dan kemudian membawa sapi (lebih muda) yang lain untuk menggantikannya.

Siapa pun yang pernah terlibat dalam administrasi ruang server warisan pasti akan terkejut dengan pemikiran seperti itu! Mesin fisik tua kami diperlakukan seperti hewan peliharaan yang dicintai. Pada tanda ketidaknyamanan sekecil apapun, kami akan berdiri di sisinya dengan cemas, mencoba mendiagnosis masalahnya dan bagaimana itu bisa diperbaiki.

Jika segala cara gagal, kita harus memaksa me-reboot server, berharap-harap cemas agar server tersebut bisa hidup kembali. Jika itu saja tidak cukup, kita harus rela mengganti perangkat kerasnya.

Namun modularitas yang kita dapatkan dari virtualisasi memberi kita berbagai fleksibilitas baru. Sekarang setelah pertimbangan perangkat keras telah sebagian besar diabstraksikan, fokus utama kita adalah pada perangkat lunak (baik itu seluruh sistem operasi atau aplikasi individual). Dan perangkat lunak, berkat bahasa pemrograman skrip, bisa diotomatisasi.

Jadi dengan menggunakan alat-alat orkestrasi seperti Ansible, Terraform, dan Puppet, Anda dapat mengotomatiskan pembuatan, penyediaan, dan manajemen siklus hidup penuh dari instance layanan aplikasi. Bahkan penanganan kesalahan pun dapat diintegrasikan ke dalam orkestrasi Anda, sehingga aplikasi Anda bisa dirancang untuk secara ajaib memperbaiki masalah mereka sendiri.

**Mesin Virtual vs Kontainer**
Instance virtual datang dalam dua varian. Mesin virtual (atau VM) adalah sistem operasi lengkap yang berjalan di atas mesin host - namun dengan derajat independensi terhadap - perangkat keras dasar.

Inilah jenis virtualisasi yang menggunakan hypervisor untuk mengadministrasi akses masing-masing VM ke sumber daya perangkat keras yang mendasarinya, tetapi VM semacam itu umumnya dibiarkan hidup dengan cara mereka sendiri.

Contoh lingkungan hypervisor meliputi proyek open source Xen, VMware ESXi, Oracle's VirtualBox, dan Microsoft Hypver-V.

Kontainer, di sisi lain, tidak hanya berbagi perangkat keras, tetapi juga kernel perangkat Bagian lunak dari sistem operasi host mereka. Ini membuat instance kontainer jauh lebih cepat dan lebih ringan (karena gambar mereka tidak perlu menyertakan kernel).

Tidak hanya ini berarti bahwa kontainer dapat diluncurkan hampir seketika, tetapi juga bahwa sistem file mereka dapat dipindahkan antara host dan berbagi. Portabilitas berarti bahwa lingkungan instance dapat direproduksi dengan andal di mana saja, membuat kolaborasi dan implementasi otomatis tidak hanya mungkin, tetapi mudah.

Contoh teknologi kontainer meliputi LXD dan Docker. Dan implementasi kontainer perusahaan meliputi sistem orkestrasi Kubernetes yang open source dari Google.

**Bagaimana Cloud Publik Bekerja**
Platform cloud publik telah mengangkat abstraksi dan alokasi dinamis sumber daya komputasi menjadi seni. Penyedia cloud besar memanfaatkan jaringan luas dari ratusan ribu server dan jumlah perangkat penyimpanan yang sulit dibayangkan tersebar di pusat data di seluruh dunia.

Siapa saja, di mana saja, dapat membuat akun pengguna dengan penyedia, meminta instance dengan kapasitas yang ditentukan sendiri, dan memiliki server web yang berfungsi sepenuhnya dan menghadap ke publik berjalan dalam waktu beberapa menit. Dan karena Anda hanya membayar untuk apa yang Anda gunakan, biaya Anda akan mencerminkan kebutuhan dunia nyata Anda dengan cermat.

Server web yang saya jalankan di Amazon Web Services (AWS) untuk menyimpan dua atau tiga situs web saya yang cukup sibuk hanya menghabiskan sekitar $50 per tahun. Dan server tersebut memiliki cukup daya yang tersisa untuk menangani lalu lintas yang lebih besar.

Sumber daya AWS yang digunakan oleh perusahaan streaming video Netflix mungkin akan lebih mahal - mungkin dalam jutaan dolar per tahun. Tetapi jelas mereka berpikir bahwa mereka mendapatkan penawaran yang baik dan lebih suka menggunakan AWS daripada menjalankan infrastrukturnya sendiri.

Jadi, siapa saja penyedia cloud publik tersebut, saya yakin Anda bertanya-tanya? Nah, percakapan itu harus dimulai (dan, seringkali, berakhir) dengan AWS. Mereka adalah gajah di setiap ruangan. Jutaan beban kerja yang berjalan di pusat data Amazon yang besar dan tersebar, bersama dengan laju inovasi mereka yang luar biasa, menjadikan mereka pemain yang harus dikalahkan dalam perlombaan ini. Dan itu belum termasuk miliaran dolar laba bersih yang mereka kantongi setiap kuartal.

Pada titik ini, satu-satunya pesaing serius untuk AWS adalah Microsoft's Azure yang cukup baik dalam menjaga kategori layanan dan, menurut semua laporan, menghasilkan uang dengan baik dalam proses tersebut. Ada juga Alibaba Cloud yang sebagian besar berfokus pada pasar Asia saat ini. Google Cloud turut serta dalam permainan ini, tetapi tampaknya fokus pada satu set layanan yang lebih sempit di mana mereka dapat bersaing secara realistis.

Karena hambatan masuk ke pasar tersebut kuat, hanya ada beberapa yang lain yang diperhatikan, termasuk Oracle Cloud, IBM Cloud, dan, dengan konvensi penamaan yang menyenangkan, Digital Ocean.
