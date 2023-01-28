# Fast Paymax
---

![image](https://user-images.githubusercontent.com/63351166/215289937-b27e1a25-5eaa-473c-bef0-bb9e1136182f.png)

# Örnek Kullanımı

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

- Sadece link oluşturmak içindir.

---
- ✨ [Destek İçin](https://fastuptime.com) <br>
- 💕 [Discord](https://fastuptime.com/discord)<br>
- 🎖️ [FasterHost Technology](https://fasterhost.tech/)<br>
- ✨ İletişim için [Tıkla!](mailto:fastuptime@gmail.com)<br>

# License
- Its protected by Creative Commons ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))

<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" title="BYNCSA40"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png"></a>
