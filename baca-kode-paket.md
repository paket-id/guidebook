## Baca Kode Paket

Untuk membaca info dari sebuah kode paket Anda bisa memakai _node_

##### ENDPOINT `[GET] http://paket.id/apis/v2/booking/{kode}`

Bila tidak bisa mendapatkan info dari kode paket, cek beberapa hal ini

* Kunci Api Anda valid

* Anda mempunyai akses untuk kode paket tersebut \(sebagai jasa kurir atau pemilik kode paket\)

* Kode paket benar

* Kode paket masih dalam keadaan aktif dan belum dihapus atau sudah kadaluarsa

Bila masih tidak bisa mendapatkan info untuk kode paket anda, silahkan kirim email ke cs@paket.id

##### CONTOH `[GET] http://paket.id/apis/v2/booking/ABCDE?auth-user-email=test@paket.id&auth-api-key=API_KEY_ANDA`

```
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
```



