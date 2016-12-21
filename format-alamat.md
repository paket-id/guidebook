## Format Alamat

Paket ID secara otomatis dapat mengidentifikasi Nama, Nomor Telepon dan Alamat dari sebuah label pengiriman, asal label tersebut mematuhi format berikut

1. Urutan label adalah Nama diikuti dengan Nomor Telepon dan diakhiri dengan alamat

2. Nomor Telepon harus diantara Nama dan Alamat

3. Nama tidak bisa diakhiri dengan nomor dan Alamat tidak bisa dimulai dengan nomor \(Jika ingin memakai nomor di nama, ikuti keterangan dibawah\)

4. Alamat tidak bisa terlalu pendek atau tidak memiliki nomor

5. Jika di dalam alamat mempunyai kodepos, akan terdeteksi secara otomatis

Dianjurkan untuk mempunyai kodepos di alamat untuk memudahkan petugas konter memvalidasi wilayah dan tariff pengiriman

Nomor Telepon bisa memakai karakter berikut: \(\) / - dan spasi

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

Klik link "Example" pada website paket.id

![](/assets/example format button.png)

Akan muncul pop-up dialog seperti ini:

### ![](/assets/example format.png)



