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

