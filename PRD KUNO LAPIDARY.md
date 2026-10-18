# PRD — Website KUNO LAPIDARY

**Versi:** 1.1  
**Status:** Draf produk untuk ditinjau  
**Pemilik produk dan koleksi:** KUNO LAPIDARY  
**Pasar awal:** Indonesia dan pembeli internasional pada negara yang dapat dilayani  
**Bahasa:** Indonesia dan Inggris

> Dokumen ini menetapkan kebutuhan produk dan perilaku sistem. Vendor pembayaran, kurir, tarif, daftar negara, serta beberapa kebijakan operasional masih harus dipilih sebelum peluncuran.

## 1. Ringkasan produk

Website e-commerce untuk memamerkan dan menjual koleksi batu alam pribadi milik KUNO LAPIDARY. Pembeli dapat menelusuri koleksi, membaca informasi produk, melihat foto dan video, membeli produk satuan atau bundel, membayar, dan mengikuti status pesanan.

Website ditujukan kepada kolektor dan pembeli baru di Indonesia maupun negara lain yang dapat dilayani. Website menyediakan bahasa Indonesia dan Inggris. Aturan awal yang diminta pemilik adalah IDR ketika bahasa Indonesia dipilih dan USD ketika bahasa Inggris dipilih.

## 2. Latar belakang dan masalah

Batu koleksi memiliki pola, bentuk, kondisi, dan karakter yang berbeda. Pembeli perlu informasi yang cukup untuk memahami potongan yang akan diterima, sedangkan KUNO LAPIDARY memerlukan satu tempat untuk menampilkan koleksi dan mengelola produk serta pesanan.

**Asumsi yang perlu divalidasi:** katalog dengan media asli dan informasi batu yang terstruktur akan membantu pembeli menilai produk serta menyelesaikan pembelian. Belum ada data riset pelanggan atau data penjualan yang menjadi dasar target numerik.

## 3. Pengguna dan kebutuhan

### Kolektor batu

Ingin menemukan batu berdasarkan nama, asal, kategori, bentuk, pola, atau harga; melihat potongan spesifik; dan mengetahui apakah produk tersedia sebagai satuan atau bundel.

### Pembeli baru

Ingin memahami kondisi, ukuran, berat, foto, video, biaya total, pengiriman, dan kebijakan toko sebelum membeli.

### Admin KUNO LAPIDARY

Ingin menambah serta memperbarui produk, menghubungkan produk dengan batu asalnya, mengelola stok satuan dan bundel, serta memproses dan memperbarui pesanan.

## 4. Tujuan dan bukan tujuan

### Tujuan

- Menampilkan koleksi KUNO LAPIDARY secara jelas kepada pembeli di pasar yang dilayani.
- Memberikan informasi produk yang akurat dan foto/video dari produk yang benar-benar dijual.
- Mendukung pembelian produk tunggal dan bundel tanpa penjualan ganda.
- Membantu pembeli menyelesaikan checkout tanpa wajib membuat akun.
- Menyediakan pengalaman bahasa Indonesia dan Inggris.

### Bukan tujuan versi pertama

- Menjadi marketplace bagi banyak penjual.
- Menyediakan penawaran harga atau negosiasi.
- Menjamin pengiriman ke setiap negara tanpa pengecualian.
- Menyediakan sertifikasi gemologi untuk semua produk.
- Menyimpan kartu pembayaran pembeli di sistem KUNO LAPIDARY.

## 5. Ukuran keberhasilan

Target angka ditetapkan setelah periode pengumpulan data awal. Definisi pengukuran awal:

1. **Pesanan berhasil:** jumlah order unik berstatus pembayaran berhasil dalam periode laporan. Order yang kemudian direfund tetap dilaporkan terpisah.
2. **Tingkat penyelesaian checkout:** jumlah checkout yang menghasilkan pembayaran berhasil dibagi jumlah checkout yang dimulai dalam periode yang sama. Checkout duplikat dan transaksi uji dikecualikan.
3. **Tingkat keluhan ketidaksesuaian produk:** jumlah pesanan terkirim dengan keluhan bahwa barang berbeda secara material dari foto/deskripsi dibagi jumlah pesanan yang terkirim. Laporkan jumlah absolut dan persentasenya.

Metrik operasional tambahan yang disarankan untuk dipantau: pembayaran gagal, pembatalan, pesanan yang belum memiliki nomor pelacakan, dan pertanyaan terkait ongkos kirim/bea impor.

## 6. Ruang lingkup versi pertama

### Termasuk

- Beranda yang mengenalkan KUNO LAPIDARY dan koleksi.
- Katalog, kategori, pencarian atau filter dasar.
- Halaman detail produk dengan informasi, foto, video jika tersedia, harga, dan stok.
- Produk satuan, pair, dan bundel.
- Keranjang dan checkout tamu tanpa akun.
- Bahasa Indonesia dan Inggris.
- Harga tampilan IDR untuk bahasa Indonesia dan USD untuk bahasa Inggris.
- Pilihan negara tujuan yang hanya mencakup negara yang telah dikonfigurasi untuk pengiriman.
- Informasi pengiriman, retur, FAQ, kontak, konfirmasi order, dan pelacakan.
- Area admin untuk katalog, stok, bundel, dan pesanan.

### Di luar ruang lingkup atau belum diputuskan

- Platform e-commerce dan vendor pembayaran.
- Vendor kurir, tarif, metode tarif langsung atau tarif tetap, dan daftar negara peluncuran.
- Sertifikasi pihak ketiga untuk setiap batu.
- Akun pelanggan dan daftar favorit; akun hanya opsional jika kelak ditambahkan.
- Multi-vendor, promosi kompleks, dan negosiasi harga.

## 7. Model katalog dan data produk

Sistem harus membedakan tiga konsep berikut:

1. **Batu asal/koleksi asal:** batu atau material sumber yang dapat menghasilkan beberapa potongan. Menyimpan nama batu, informasi lokasi asal, catatan identifikasi, serta tingkat kepastian asal.
2. **Produk jual:** potongan fisik tertentu yang mempunyai ID/SKU unik, foto/video sendiri, ukuran, berat, kondisi, harga, dan status stok.
3. **Paket penjualan:** pair atau bundel yang merujuk ke satu atau lebih produk jual tertentu.

Kategori/kondisi produk yang direncanakan: **cabochon, rough, slab, specimen**. **Pair** adalah format paket dua potong, bukan kondisi batu. Cara penjualan dapat berupa produk tunggal atau bundel. Satu produk dapat mempunyai kategori kondisi sekaligus menjadi bagian dari sebuah paket.

Setiap produk jual harus memiliki identitas yang membedakannya dari potongan lain, terutama bila berasal dari batu asal yang sama.

### Informasi produk

Halaman produk menampilkan:

- Nama batu dan nama/label produk.
- Daerah asal di Indonesia pada tingkat detail yang dapat dipertanggungjawabkan.
- Catatan apakah identifikasi atau asal telah diverifikasi, belum pasti, atau tidak diketahui.
- Kategori/kondisi: cabochon, rough, slab, atau specimen; pair ditampilkan sebagai format paket.
- Foto asli dari beberapa sisi yang menampilkan produk yang akan dikirim.
- Video produk jika tersedia.
- Ukuran, berat, kondisi, dan jenis pengerjaan jika relevan.
- Deskripsi pola dan karakter yang terlihat.
- Harga, mata uang, dan status ketersediaan.
- Semua potongan yang termasuk dalam pair/bundel.
- Sertifikat atau hasil identifikasi hanya jika benar-benar tersedia.

Untuk mengurangi risiko perbedaan persepsi, foto sebaiknya menyertakan skala atau objek pembanding. Ini adalah rekomendasi konten produk; alat pembanding dan format foto dapat dipilih kemudian.

## 8. Aturan inventaris dan bundel

- Setiap potongan fisik unik mempunyai stok maksimum satu, kecuali admin secara eksplisit mencatat beberapa unit identik.
- Pair/bundel menyimpan daftar ID produk yang termasuk di dalamnya.
- Produk tunggal yang sudah terjual tidak dapat dibeli lagi.
- Jika salah satu produk dalam bundel terjual terpisah, bundel terkait otomatis tidak tersedia.
- Jika satu bundel terjual, semua produk yang menjadi bagiannya tidak tersedia untuk penjualan tunggal atau bundel lain.
- Sistem memvalidasi stok lagi saat pembeli memulai pembayaran dan sebelum pembayaran dianggap berhasil.
- Jika stok berubah ketika checkout berjalan, pembeli diberi tahu, tidak ditagih untuk produk yang tidak tersedia, dan keranjang diperbarui.
- Mekanisme reservasi stok selama pembayaran dan lama reservasi **perlu diputuskan saat memilih platform/vendor**. Sistem tidak boleh mengonfirmasi dua order berbayar untuk produk fisik yang sama.

## 9. Bahasa, negara, dan mata uang

- Halaman beranda, katalog, detail produk, checkout, pesan sistem, dan informasi bantuan tersedia dalam bahasa Indonesia dan Inggris.
- Aturan awal: pilihan bahasa Indonesia menampilkan IDR; pilihan bahasa Inggris menampilkan USD.
- Negara tujuan dipilih secara terpisah dari bahasa, dan negara yang tidak dapat dilayani tidak tersedia di checkout.
- Jika metode pembayaran tidak dapat memproses mata uang yang sedang ditampilkan, sistem harus menjelaskan mata uang pembayaran sebelum order dikonfirmasi; tidak boleh mengganti mata uang diam-diam.
- Harga produk, keranjang, ongkir, total, konfirmasi, dan refund harus menyatakan mata uang secara konsisten.
- Perlu dipastikan apakah harga USD dikonversi otomatis dari IDR atau ditetapkan manual per produk. Keputusan ini masih terbuka.

## 10. Alur pembelian

1. Pembeli membuka website dan memilih bahasa.
2. Pembeli menelusuri atau memfilter katalog.
3. Pembeli membuka detail produk dan memeriksa media, informasi, harga, serta ketersediaan.
4. Pembeli menambahkan produk tunggal atau bundel ke keranjang.
5. Sistem memvalidasi bahwa seluruh produk fisik dalam keranjang masih tersedia.
6. Pembeli mengisi nama penerima, email, nomor telepon, alamat lengkap, dan negara tujuan.
7. Sistem menampilkan pilihan pengiriman, ongkos kirim, estimasi waktu, serta pemberitahuan tentang kemungkinan bea/pajak impor.
8. Pembeli memeriksa ringkasan akhir dan menyelesaikan pembayaran.
9. Jika pembayaran berhasil, sistem membuat konfirmasi order dan mengirim email berisi nomor order.
10. Setelah barang dikirim, admin memasukkan atau menyinkronkan nomor pelacakan dan pembeli menerima pembaruan.

Checkout tidak mewajibkan akun. Akun pelanggan, bila dibuat kemudian, bersifat opsional.

## 11. Pembayaran, pengiriman, bea, dan pajak

### Pembayaran

Vendor dan metode pembayaran belum dipilih. Kebutuhan produk:

- Mendukung transaksi dalam mata uang yang ditampilkan, sesuai negara yang dilayani.
- Menyampaikan hasil pembayaran berhasil/gagal dengan status order yang benar.
- Menangani pembayaran gagal atau tertunda tanpa menandai order sebagai lunas.
- Tidak menyimpan data kartu di sistem KUNO LAPIDARY; pemrosesan dilakukan oleh penyedia pembayaran yang dipilih.
- Mendukung pembatalan/refund ketika diperlukan oleh kebijakan atau hukum yang berlaku.

### Pengiriman

- Gunakan layanan yang menyediakan pelacakan dan cakupan perlindungan yang sesuai dengan nilai produk.
- Ongkos kirim dan estimasi ditampilkan sebelum pembayaran.
- Untuk model awal, pembeli membayar ongkos kirim di checkout.
- Negara tujuan hanya dibuka setelah kemampuan kurir dan persyaratan ekspor/impor diperiksa.
- Jika tarif tidak dapat dihitung atau pengiriman tidak tersedia, sistem tidak boleh membiarkan order dibayar tanpa penjelasan dan persetujuan admin.
- Vendor, tarif, waktu proses, kemasan, serta batas nilai/berat masih belum diputuskan.

### Bea dan pajak impor

Model awal yang direncanakan adalah DAP: pembeli mungkin harus membayar bea/pajak impor di negara tujuan. Informasi ini harus terlihat sebelum checkout selesai. Penghitungan dan pembayaran di muka (misalnya DDP) dapat dipertimbangkan kemudian. Ketentuan final bergantung pada negara, produk, kurir, dan hukum yang berlaku.

## 12. Retur, kerusakan, dan ketidaksesuaian

Preferensi awal KUNO LAPIDARY adalah tidak menerima pengembalian karena pembeli berubah pikiran. Ketentuan ini tidak mengesampingkan hak wajib konsumen di negara tujuan.

PRD menetapkan kebutuhan berikut, sementara detail operasional masih harus disepakati:

- Kebijakan retur ditampilkan sebelum pembelian dan tersedia dalam kedua bahasa.
- Pembeli memiliki cara untuk melaporkan barang rusak, salah kirim, atau berbeda secara material dari deskripsi.
- Proses penanganan, bukti yang diminta, batas waktu pelaporan, pihak yang membayar ongkos retur, dan bentuk penyelesaian (penggantian/refund/opsi lain) **belum diputuskan**.
- Kebijakan final harus ditinjau untuk pasar yang benar-benar dilayani.

## 13. Privasi dan keamanan

- Data checkout dibatasi pada data yang diperlukan untuk pembayaran, pengiriman, dukungan pesanan, dan kewajiban hukum.
- Data pelanggan dan order hanya dapat dilihat oleh petugas yang memerlukan akses untuk memproses pesanan.
- Situs menggunakan koneksi aman dan penyedia pembayaran yang menangani data pembayaran.
- Website menjelaskan penggunaan data dan menyediakan kebijakan privasi dalam bahasa Indonesia dan Inggris.
- Lama penyimpanan data, proses permintaan penghapusan, serta kewajiban privasi untuk tiap pasar harus dikonfirmasi sebelum peluncuran.

## 14. Persyaratan kualitas layanan

- Website dapat digunakan pada ponsel dan desktop.
- Informasi penting seperti harga, mata uang, stok, ongkir, dan total order tidak boleh ambigu.
- Halaman produk harus tetap dapat dibaca saat video tidak tersedia atau gagal dimuat; foto dan teks tetap ditampilkan.
- Status order harus dapat dibedakan: menunggu pembayaran, pembayaran gagal/berhasil, diproses, dikirim, selesai, dibatalkan, atau direfund sesuai dukungan platform.
- Seluruh konten checkout dan pemberitahuan penting tersedia dalam bahasa yang dipilih.

## 15. Kriteria penerimaan

1. Pembeli dapat melihat foto asli, nama batu, asal (atau keterangan belum diketahui), kondisi/kategori, ukuran, berat, harga, dan status stok pada halaman produk.
2. Pembeli dapat memilih satu produk atau paket yang tersedia; isi paket terlihat sebelum dimasukkan ke keranjang.
3. Setelah potongan terjual dalam transaksi tunggal, paket yang memuat potongan itu tidak dapat dibeli.
4. Jika dua checkout bersaing atas potongan fisik yang sama, hanya satu pembayaran yang dapat menghasilkan order terkonfirmasi untuk potongan tersebut.
5. Pembeli dapat menyelesaikan checkout tanpa membuat akun.
6. Pembeli harus memasukkan nama, email, nomor telepon, alamat, dan negara tujuan sebelum membuat order.
7. Ongkir, estimasi, mata uang, total, dan pemberitahuan bea/pajak ditampilkan sebelum langkah pembayaran akhir.
8. Kegagalan pembayaran tidak membuat order berstatus lunas dan tidak mengirim konfirmasi pembayaran berhasil.
9. Negara yang tidak dikonfigurasi untuk pengiriman tidak dapat dipilih sebagai tujuan checkout.
10. Setelah pembayaran berhasil, pembeli menerima email konfirmasi dan nomor order.
11. Setelah nomor pelacakan ditambahkan, pembeli menerima pembaruan berisi nomor tersebut.
12. Teks dan pesan penting pada alur utama tersedia dalam bahasa Indonesia dan Inggris.
13. Jika video tidak tersedia, halaman tetap menampilkan foto dan detail produk.
14. Produk dengan asal atau identifikasi belum terverifikasi diberi label yang tidak menyatakan kepastian.

## 16. Risiko dan asumsi

- **Asumsi:** foto dan video produk nyata membantu pembeli memahami barang unik sebelum membeli.
- **Risiko stok:** hubungan produk tunggal dengan beberapa bundel dapat menyebabkan overselling jika stok tidak dikunci dengan benar.
- **Risiko mata uang:** bahasa dan negara pembeli tidak selalu sama; aturan IDR/Indonesia dan USD/Inggris perlu diuji pada checkout dan metode pembayaran.
- **Risiko pengiriman:** layanan, tarif, aturan ekspor, bea/pajak, dan pembatasan impor berbeda menurut tujuan.
- **Risiko kebijakan:** aturan retur dan perlindungan konsumen dapat berbeda antarnegara.
- **Risiko klaim produk:** nama batu dan asal geografis harus disampaikan sesuai tingkat verifikasi yang benar.

## 17. Keputusan terbuka sebelum peluncuran

1. Platform website dan vendor pembayaran.
2. Daftar metode pembayaran serta mata uang yang benar-benar dapat ditagihkan.
3. Apakah harga USD dikonversi otomatis atau ditetapkan manual.
4. Kurir, tarif, estimasi, pelacakan, perlindungan paket, dan negara peluncuran.
5. Persyaratan ekspor produk serta dokumen yang diperlukan.
6. Prosedur retur/komplain, batas waktu, dan bentuk penyelesaian sesuai pasar.
7. Lama penyimpanan data dan ketentuan privasi per pasar.
8. Lama reservasi stok saat pembayaran.
9. Apakah bundel dapat berisi potongan dari batu asal yang berbeda.
10. Target numerik untuk metrik setelah data awal tersedia.

## 18. Status dokumen

PRD ini telah mencatat kebutuhan produk yang disepakati dan asumsi yang diketahui. Dokumen dapat digunakan untuk diskusi desain dan pemilihan platform. Keputusan terbuka pada bagian 17 harus ditutup sebelum peluncuran; vendor dan tarif dapat ditambahkan setelah riset operasional.
