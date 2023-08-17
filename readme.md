# Fast Paymax


# 🎈 Images 🎈

![image](https://user-images.githubusercontent.com/63351166/215289937-b27e1a25-5eaa-473c-bef0-bb9e1136182f.png)

# 🌱 Example Create Link Paymax 🌱

```
const paymax = require('fast-paymax');

const data = {
    referer: 'localhost', // Referer Domain example.com
    hash: 'xxxx', // Api Hash Anahtarı
    userName: 'xxxx', // Apı User
    password: 'xxxxxxxxxxx', // Api Key
    shopCode: 'xxx', // Api Mağaza Kodu
    productName: 'productName',
    productData: 'productData',
    productType: 'DIJITAL_URUN',
    productsTotalPrice: 21,
    orderPrice: 20.00,
    currency: 'TRY',
    orderId: '20',
    locale: 'locale',
    conversationId: 'DIJITAL_URUN',
    buyerName: 'buyerName',
    buyerSurName: 'buyerSurName',
    buyerGsmNo: 'buyerGsmNo',
    buyerMail: 'buyerEmail@gmail.com',
    buyerIp: '124.432.423',
    buyerAdress: 'buyerAdress',
    BuyerCountry: 'BuyerCountry',
    BuyerCity: 'BuyerCity',
    buyerDistrict: 'buyerDistrict',
    callbackOkUrl: 'http://localhost/callbackOkUrl',
    callbackFailUrl: 'http://localhost/callbackFailUrl',
};

paymax.createPaymentLink(data, (err, res) => {
    console.log(err, res);
});

```
# 🎏 Example Express Fast-Paymax 🎏

```js
const express = require('express');
const app = express();
const paymax = require('fast-paymax');

app.get('/createPaymentLink', (req, res) => {
    const data = {
        referer: 'localhost', // Referer Domain example.com
        hash: 'xxxx', // Api Hash Anahtarı
        userName: 'xxxx', // Apı User
        password: 'xxxxxxxxxxx', // Api Key
        shopCode: 'xxx', // Api Mağaza Kodu
        productName: 'productName',
        productData: 'productData',
        productType: 'DIJITAL_URUN',
        productsTotalPrice: 21,
        orderPrice: 20.00,
        currency: 'TRY',
        orderId: '20',
        locale: 'locale',
        conversationId: 'DIJITAL_URUN',
        buyerName: 'buyerName',
        buyerSurName: 'buyerSurName',
        buyerGsmNo: 'buyerGsmNo',
        buyerMail: 'buyerEmail@gmail.com',
        buyerIp: '124.432.423',
        buyerAdress: 'buyerAdress',
        BuyerCountry: 'BuyerCountry',
        BuyerCity: 'BuyerCity',
        buyerDistrict: 'buyerDistrict',
        callbackOkUrl: 'http://localhost/callbackOkUrl',
        callbackFailUrl: 'http://localhost/callbackFailUrl',
    };

    paymax.createPaymentLink(data, (response) => {
        //console.log(response);
        if (response.status === 'error') return res.send(response.message);
        res.redirect(response.url);
    });
});

app.get('/callbackOkUrl', (req, res) => {
    res.send('Ödeme Başarılı');
});

app.get('/callbackFailUrl', (req, res) => {
    res.send('Ödeme Başarısız');
});

app.get('/callback', async (req, res) => {
    let data = {
        status: req.body.status,
        paymentStatus: req.body.paymentStatus,
        hash: req.body.hash,
        paymentAmount: req.body.paymentAmount,
        paymentType: req.body.paymentType,
        conversationId: req.body.conversationId,
        orderId: req.body.orderId,
    };

    if (data.status !== 'success') return res.send('Ödeme Başarısız');

    // Veritabanı işlemleri
    res.send('ok');
});


app.listen(80, () => {
    console.log('Server Started');
});

```


# 🌘 Example Response Fast-Paymax 🌘

```js
{
  status: 'success',
  data: {
    status: 'success',
    errorMessage: '',
    payment_page_url: 'https://www.vallet.com.tr/payment-center/en/copay/XXXXXXXXX',
    payment_page_url_domestic_card: 'https://www.vallet.com.tr/payment-center/en/copay/XXXXXXXXX/kredi-karti',
    payment_page_url_bank_transfer_card: 'https://www.vallet.com.tr/payment-center/en/copay/XXXXXXXXX/banka-havale',
    payment_page_url_international_card: 'https://www.vallet.com.tr/payment-center/en/copay/XXXXXXXXX/kredi-karti-dunya',
    ValletOrderNumber: '111111111',
    ValletOrderId: '1111111113',
    conversationId: 'DIJITAL_URUN'
  },
  url: 'https://www.vallet.com.tr/payment-center/en/copay/XXXXXXXXX'
}
```

# 🛠️ Installation 🛠️

- `npm i fast-paymax`

- https://www.vallet.com.tr/merchant/api-manager/api-information.html

## ⛳Tech Stack ⛳

**🗄️ Server:** Node, Axios, form-data, crypto, buffer

---
- ✨ [For Support](https://github.com/sponsors/fastuptime) <br>
- 💕 [Discord](https://fastuptime.com/discord)<br>
- 🏓 [Fast Uptime](https://fastuptime.com/)<br>
- 🪄 All kinds of projects are made <br>
- 🧨 You can contact us to make a paid project<br>
- 💸 You can contact for paid installation<br>
- ☄️ [Click For Contact](mailto:fastuptime@gmail.com)<br>

# 🎯 License 🎯
- ⚖️ Its protected by Creative Commons ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))

<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" title="BYNCSA40"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png"></a>
