<!-- DIGIFLAZZ -->

## <center>Digiflazz</center>

### Instalasi

`npm install lutzstore`

### Dokumentasi

```js
const Digiflazz = require("lutzstore/digiflazz");
const digiflazz = new Digiflazz("username", "apikey");
```

#### Buyer Area

##### Cek Saldo

```js
let saldo = await digiflazz.cekSaldo();
```

##### Daftar Harga

```js
let harga = await digiflazz.daftarHarga();
```

##### Tiket Deposit

```js
let deposit = await digiflazz.deposit(nominal, "BANK", "Nama Pemilik Rekening");
```

##### Topup & Status Topup

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id");
```

##### Inquiry Pascabayar

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id", "CEK");
```

##### Bayar Pascabayar

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id", "BAYAR");
```

##### Status Pascabayar

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id", "STATUS");
```

##### Webhook

```js
const Digiflazz = require("lutzstore/digiflazz");
const digiflazz = new Digiflazz("username", "apikey", "webhookkey");

app.post("/hook", Digiflazz.webhook(digiflazz), (req) => {
  // Anda dapat memproses hasilnya disini
  // result webhook dapat diakses di req.digiwebhooks
});
```

<!-- APIGAMES -->

## <center>Apigames</center>

## Instalasi

```bash
npm install lutzstore
```

## Dokumentasi

```js
const Apigames = require("lutzstore/apigames");
const client = new Apigames("YOUR MERCHANT ID", "YOUR SECRET");
```

### Cek Saldo

```js
let saldo = await client.cekSaldo();
```

### Cek Akun Game

```js
let saldo = await client.cekAkunGame(gameCode, userId);
```

> Game yang tersedia : mobilelegend , freefire, higgs

### Cek Status Koneksi

```js
Coming Soon
```

### Transaksi Versi 1

```js
let transaksi = await client.transaksi(refId, productCode, tujuan);
```

> Note:
> RefID adalah kode transaksi unik kamu yang di generate secara acak

### Transaksi Versi 2

```js
let transaksi = await client.transaksiv2(refId, productCode, tujuan, serverId);
```

> Note:
> RefID adalah kode transaksi unik kamu yang di generate secara acak

### Cek Status Transaksi

```js
Coming Soon
```

### Radeem Kiosgamer Garena Shell Bulk

```js
Coming Soon
```

### Cek Status Radeem Kiosgamer Garena Shell Bulk

```js
Coming Soon
```

<!-- TOKOPAY -->

## <center>Tokopay</center>

## Instalasi

```bash
npm install lutzstore
```

## Dokumentasi

```js
const tokopay = require("lutzstore/tokopay");
const client = new tokopay("YOUR MERCHANT ID", "YOUR SECRET");
```

### Informasi Akun

```js
const createOrder = await client.info();
```

### Membuat Simple Order

```js
const createOrder = await client.simpleOrder(refId, metode, nominal);
```

### Tarik Saldo

```js
const createOrder = await client.tarikSaldo(nominal);
```
