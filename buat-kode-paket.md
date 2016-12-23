## Buat Kode Paket

Untuk mebuat sebuah kode paket Anda bisa memakai metode `POST`, dan memakai 2 tipe request bersamaan yaitu POST dan GET, url untuk membuat paket adalah

##### ENDPOINT `[POST] http://paket.id/apis/v2/booking/`

Dan gunakan request dengan tipe POST dengan nama _field_ berikut

| **Nama Field** | **Tipe** | **Diperlukan** | **Deskripsi** |
| --- | --- | --- | --- |
| from\_name | String | Diperlukan | Nama Pengirim |
| from\_email | String \(email address format\) | Opsional | Email Pengirim, jika kosong maka menggunakan email user yang terdaftar |
| from\_address | String | Diperlukan | Alamat Pengirim |
| from\_phone | String | Diperlukan | Telefon Pengirim |
| from\_zip\_code | String | Opsional | Kode Pos Pengirim |
| to\_email | String \(email address format\) | Opsional | Email Penerima |
| to\_name | String | Diperlukan | Nama Penerima |
| to\_address | String | Diperlukan | Alamat Penerima |
| to\_phone | String | Diperlukan | Telefon Penerima |
| to\_zip\_code | String | Opsional | Pos Kode Penerima |
| note | String | Opsional | Catatan Pribadi \(Tidak dikirim ke penerima\) |
| content | String | Opsional | Konten barang |

##### CONTOH `[POST] http://paket.id/apis/v2/booking?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`

```
JSON RESPONSE

{

 "success": "1",

 "detail": {

 "booking_code": "GDTNF",

 "reference_code": "ID010116GDTNF"

 "to_name": "Andi",

 "to_phone": "0897678373728",

 "to_address": "Jln Rawa Belong no 21"

 }

}
```



