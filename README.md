# API Cek Resi Cek Ongkir

API Cek Resi Cek Ongkir adalah sebuah layanan web yang memungkinkan Anda untuk melakukan pengecekan status pengiriman barang atau paket dari berbagai kurir di Indonesia, seperti JNE, TIKI, POS, J&T, Ninja Xpress, Sicepat, dan lain-lain. API ini disediakan oleh PT Web Solution melalui platform RapidAPI.

Untuk menggunakan API ini, Anda perlu melakukan beberapa langkah berikut:

1. Daftar akun di RapidAPI jika belum punya. Anda bisa menggunakan email, Google, atau GitHub untuk mendaftar.
2. Kunjungi halaman [API Cek Resi Cek Ongkir](https://rapidapi.com/ptwebsolution/api/cek-resi-cek-ongkir) dan klik tombol **Subscribe** untuk memilih rencana berlangganan yang sesuai dengan kebutuhan Anda. Ada rencana gratis dan berbayar dengan batasan jumlah permintaan per bulan.
3. Setelah berlangganan, Anda akan mendapatkan **X-RapidAPI-Key** yang merupakan kunci akses untuk menggunakan API ini. Simpan kunci ini dengan aman dan jangan bagikan kepada siapa pun.


Contoh permintaan List Logistik:
```shell
curl --request GET \
	--url https://cek-resi-cek-ongkir.p.rapidapi.com/general/logistics \
	--header 'X-RapidAPI-Host: cek-resi-cek-ongkir.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```
Contoh response List Logistik:
```json
{
  "success": true,
  "message": "success",
  "results": [
    {
      "id": "1",
      "name": "JNE"
    },
    ...
  ]
}
```

Contoh permintaan Autocomplete Lokasi:
```shell
curl --request GET \
	--url 'https://cek-resi-cek-ongkir.p.rapidapi.com/general/autocomplete?q=ancol' \
	--header 'X-RapidAPI-Host: cek-resi-cek-ongkir.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```

Contoh response Autocomplete Lokasi:
```json
{
  "success": true,
  "message": "success",
  "results": [
    {
      "value": "4616",
      "text": "Ancol, Pademangan, Jakarta Utara, DKI Jakarta"
    },
    ...
  ]
}
```

Contoh permintaan Cek Resi:
```shell
curl --request GET \
	--url 'https://cek-resi-cek-ongkir.p.rapidapi.com/tracking?logisticId=1&trackingNumber=TKP01-JGHKPWQ9' \
	--header 'X-RapidAPI-Host: cek-resi-cek-ongkir.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```

Contoh response Cek Resi:
```json
{
  "success": true,
  "message": "success",
  "results": {
    "logisticId": "1",
    "trackingNumber": "TKP01-JGHKPWQ9",
    "details": [
      {
        "dateTime": "2023-12-12T21:52:00+07:00",
        "status": "SHIPMENT RECEIVED BY JNE COUNTER OFFICER AT [BANDUNG BARAT KAB, NGAMPRAH]"
      },
      ...
    ]
  }
}
```

Contoh permintaan Cek Ongkir:
```shell
curl --request GET \
	--url 'https://cek-resi-cek-ongkir.p.rapidapi.com/shipping-cost?originAreaId=4616&destinationAreaId=685' \
	--header 'X-RapidAPI-Host: cek-resi-cek-ongkir.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```

Contoh response Cek Ongkir:
```json
{
  "success": true,
  "message": "success",
  "results": {
    "totalCount": 14,
    "items": [
      {
        "id": "66362848",
        "logistic": {
          "id": "38",
          "name": "Indah Cargo",
          "code": "IND",
          "status": true,
          "companyName": "PT Indah Logistic Cargo"
        },
        "rate": {
          "name": "Darat",
          "type": "Trucking"
        },
        "totalPrice": 15130,
        "minDay": 3,
        "maxDay": 4,
        "finalPrice": 15528,
        "discountedPrice": 15130,
        "insuranceFee": 398,
        "surchargeFee": 0,
        "discountValue": 0
      },
      ...
    ]
  }
}
```

Untuk mendapatkan API key, silahkan Coba GRATIS sekarang di [API Cek Resi Cek Ongkir](https://rapidapi.com/ptwebsolution/api/cek-resi-cek-ongkir)
