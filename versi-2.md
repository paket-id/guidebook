## API Versi 2



API Versi 2 menggunakan otorisasi universal, untuk memakai fungsi fungsi daripada API ini silahkan memakai field \(GET\) sebagai berikut:



| **Nama Field** | **Keterangan** |

| --- | --- |

| `auth-user-email` | user email akun anda |

| `auth-api-key` | Api key yang diberikan kepada anda, bisa didapatkan di halaman [API](https://paket.id/settings/apikeyuser) |



## Baca Kode Paket



Untuk membaca info dari sebuah kode paket anda bisa memakai node



##### ENDPOINT `[GET] http://paket.id/apis/v2/booking/{kode}`



Bila tidak bisa mendapatkan info dari kode paket, cek beberapa hal ini



* Kunci Api anda valid

* Anda mempunyai akses untuk kode paket tersebut \(sebagai jasa kurir atau pemilik kode paket\)

* Kode paket benar

* Kode paket masih dalam keadaan aktif dan belum di delete atau sudah expirasi



Bila masih tidak bisa mendapatkan info untuk kode paket anda, silahkan kirim email ke cs@paket.id



##### CONTOH `[GET] http://paket.id/apis/v2/booking/ABCDE?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`



{

 "status": {

 "success": 1

 },

 "from\_detail": {

 "name": "Dika",

 "address": "Jln Rawa Kepa Raya No 50",

 "area": null,

 "state": null,

 "zip\_code": "",

 "country": null,

 "country\_code": "ID",

 "phone": "089622245655"

 },

 "to\_detail": {

 "name": "Desiana",

 "address": "Jl Pegangsaan 12 Komp. Gading Arcadia Blok A No. 222",

 "area": null,

 "state": null,

 "zip\_code": "",

 "country": null,

 "country\_code": "ID",

 "phone": "081619422272339"

 },

 "additional\_info": {

 "message": "",

 "content": "",

 "value": null,

 "insurance": null,

 "max\_cost": null,

 "note": ""

 },

 "booking\_detail": {

 "booking\_code": "DCYBE",

 "booking\_date": "2016-01-27",

 "expiry\_date": "2016-02-26",

 "reference\_code": "ID270116DCYBE",

 "status": "1",

 "status\_msg": "sent",

 "created\_from": "PaketIDWeb"

 },

 "shipment": {

 "vendor": {

 "code": "tiki",

 "name": "Tiki"

 },

 "service": {

 "code": null,

 "name": null

 },

 "detail": {

 "airway\_bill": "310155454612",

 "weight": null,

 "dimension": null,

 "volume": null,

 "volumetric\_weight": "10",

 "eta": null

 },

 "tariff": {

 "value": "10000.00",

 "unit\_code": "Rp",

 "unit\_name": "Rupiah",

 "unit\_symbol": "Rp"

 }

 },

 "tracking\_history": \[

 {

 "datetime": "2016-09-13 13:17:13",

 "status": "Package has been processed!"

 },

 {

 "datetime": "2016-09-13 14:16:18",

 "status": "With delivery courier"

 },

 {

 "datetime": "2016-09-13 15:20:00",

 "status": "Packaged with PL\#1823"

 }

 \]

}



## Buat Kode Paket



Untuk mebuat sebuah kode paket anda bisa memakai metode `POST`, dan memakai 2 tipe request bersamaan yaitu POST dan GET, url untuk membuat paket adalah



##### ENDPOINT `[POST] http://paket.id/apis/v2/booking/`



Dan gunakan request dengan tipe POST dengan nama field berikut



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



## Tarif



Untuk melihat daftar tarif yang dimiliki oleh Paket ID bisa memakai API `tarif`, API `tarif` memakai area yang terdapat pada API area



##### ENDPOINT `[POST/GET] http://paket.id/apis/v2/tarif/{kode-vendor}/{area-pengirim}/{area-penerima}/{berat}`



| **Nama** | **Deskripsi** | **Default** |

| --- | --- | --- |

| kode-vendor | Dipakai untuk mengambil kode spesifik sebuah vendor | tiki |

| area-pengirim | Area darimana barang dikirim, bisa didapat dari API "AREA" | Jakarta |

| area-penerima | Area tujuan pengiriman barang, bisa didapat dari API "AREA" | Jakarta |

| Berat | Berat barang dalam kilogram | 1 |



##### CONTOH `[GET/POST] http://paket.id/apis/v2/tariff/tiki/Jakarta/Surabaya/1?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`



```

JSON RESPONSE

{

 "tariff": {

 "TIKI": [

 {

 "SERVICE": "SDS",

 "DESCRIPTION": "SAMEDAY SERVICE",

 "TARIFF": 256000,

 "EST_DAY": "0",

 "FROM_AREA": "JAKARTA",

 "TO_AREA": "SURABAYA"

 },

 {

 "SERVICE": "HDS",

 "DESCRIPTION": "HOLIDAY SERVICE",

 "TARIFF": 46000,

 "EST_DAY": "1",

 "FROM_AREA": "JAKARTA",

 "TO_AREA": "SURABAYA"

 },

 {

 "SERVICE": "ONS",

 "DESCRIPTION": "ONE NIGHT SERVICE",

 "TARIFF": 25000,

 "EST_DAY": "1",

 "FROM_AREA": "JAKARTA",

 "TO_AREA": "SURABAYA"

 },

 {

 "SERVICE": "REG",

 "DESCRIPTION": "REGULAR SERVICE",

 "TARIFF": 17000,

 "EST_DAY": "3",

 "FROM_AREA": "JAKARTA",

 "TO_AREA": "SURABAYA"

 },

 {

 "SERVICE": "ECO",

 "DESCRIPTION": "ECONOMY SERVICE",

 "TARIFF": 12000,

 "EST_DAY": "5",

 "FROM_AREA": "JAKARTA",

 "TO_AREA": "SURABAYA"

 }

 ]

 },

 "success": 1,

}



```



## Area untuk Tarif



Untuk melihat daftar area yang dimiliki oleh Paket ID bisa memakai API `area`, API `area` dipakai untuk keperluan tarif



##### ENDPOINT `[POST/GET] http://paket.id/apis/v2/area/{tipe}`



| **Tipe** | **Deskripsi** |

| --- | --- |

| list | list dipakai untuk mengambil nama semua area terdaftar, list adalah tipe default |

| full | full dipakai untuk mengambil detail semua area |



##### CONTOH `[GET/POST] http://paket.id/apis/v2/area?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`



```

JSON RESPONSE

{

 "Penajam Paser Utara",

 "Tana Tidung",

 "Balikpapan",

 "Bontang",

 "Samarinda",

 "Tarakan",

 "Boalemo",

 "Bone Bolango",

 "Gorontalo",

 "Gorontalo Utara",

 "Pohuwato",

 "Bantaeng",

 "Barru",

 ....

}



```



##### CONTOH `[GET/POST] http://paket.id/apis/v2/area/full?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`



```

JSON RESPONSE

{

 {

 "area_id": "117",

 "area": "Ogan Komering Ulu",

 "state": "Sumatera Selatan",

 "country": "Indonesia",

 "country_code": "ID",

 "importance": "1",

 "timestamp": "2014-12-17 03:21:02"

 },

 {

 "area_id": "118",

 "area": "Ogan Komering Ulu Selatan",

 "state": "Sumatera Selatan",

 "country": "Indonesia",

 "country_code": "ID",

 "importance": "1",

 "timestamp": "2014-12-17 03:21:02"

 }, ....

}



```



## Vendor



API Vendor diapakai untuk melihat daftar para vendor yang telah memakai Paket ID



##### ENDPOINT `[POST/GET] http://paket.id/apis/v2/vendor`



##### CONTOH `[GET/POST] http://paket.id/apis/v2/vendor?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`



```

JSON RESPONSE

{

 "success": 1,

 "vendor": [

 "tiki"

 ]

}

```




