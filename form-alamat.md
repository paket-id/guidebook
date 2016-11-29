## Format input label

Paket ID secara otomatis dapat mengidentifikasi Nama, Nomor Telepon dan Alamat dari sebuah label pengiriman, asal label tersebut mematuhi format berikut

1. Urutan label adalah Nama diikuti dengan Nomor Telepon dan diakhiri dengan alamat

2. Nomor Telepon harus diantara Nama dan Alamat

3. Nama tidak bisa diakhiri dengan nomor dan Alamat tidak bisa dimulai dengan nomor \(Jika ingin memakai nomor di nama, ikuti keterangan dibawah\)

4. Alamat tidak bisa terlalu pendek atau tidak memiliki nomor

5. Jika di dalam alamat mempunyai kodepos, akan terdeteksi secara otomatis


Dianjurkan untuk mempunyai kodepos di alamat untuk memudahkan petugas konter memvalidasi wilayah dan tariff pengiriman

Nomor Telepon bisa memakai karakter berikut: \(\)\/- dan spasi

_Contoh_

```

Andi Wijaya 0891-2912-1229 Jln Dukuh atas no 21, 11221

Andi Wijaya

0891 2212 1229

Jln Duku Atas no 21, Jakarta 11221

Andi Wijaya 089122121229

Jln Duku Atas No 21, Jakarta 11221

```

Jika ingin memakai nomor di nama ada 2 cara

1. Nomor disambung dengan nama, contoh Doni-111222

2. Nomor disambung dengan karakter lain seperti \#, contoh : Doni \#111222


_Contoh_

```

Andi Wijaya-111222 0891-2912-1229 Jln Dukuh atas no 21, 11221

Andi Wijaya #111222 0891 2212 1229 Jln Duku Atas no 21, Jakarta 11221

Andi Wijaya 089122121229 Jln Duku Atas No 21, Jakarta 11221

```

### Format marketplace

Paket ID juga bisa mendeteksi format beberapa marketplace di Indonesia

Untuk saat ini sudah ada 2 marketplace yang dapat digunakan langsung yaitu Bukalapak dan Shopee

Dengan fitur ini, membuat kode menjadi sangat mudah karena tinggal _copy paste_ dari aplikasi marketplace masing masing

**Bukalapak:**

Dari aplikasi Bukalapak -&gt; lanjut ke halaman Detil Transaksi -&gt; pilih tab “ALAMAT” -&gt; tekan dan tahan alamat tersebut -&gt; pilih “Salin”

**Shopee:**

Di aplikasi **Shopee** &gt; lanjut ke halaman Order Details &gt; tekan **COPY** bagian “**Delivery Address**”.


**Tokopedia**:

Copy alamat dari website Tokopedia.


Di Paket ID -&gt; tekan dan tahan di kotak penerima -&gt; pilih “Paste”, setelah data yang tersalin tertulis -&gt; tekan Book untuk langsung mendapatkan ID Paket

_Menyalin dari aplikasi marketplace_

![](/assets/bl1.png)

![](/assets/shp1.png)

![](/assets/tokopedia detail order_edited.jpg)

_Gambar Salinan di Paket ID_

![](/assets/paket1.png)

