


<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Crypto </title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  font-family:Tahoma,Arial,sans-serif;
  background:#ffd900;
  min-height:100vh;
  color:#fff;
  transition:.4s;
}

body.blue{background:#087cf5}
body.purple{background:#7028c9}
body.orange{background:#ff7800}

.container{
  width:95%;
  max-width:1250px;
  margin:auto;
  padding:18px 0 40px;
}

.header{
  background:rgba(0,0,0,.94);
  border-radius:22px;
  padding:18px 20px;
  margin-bottom:15px;
  box-shadow:0 10px 30px rgba(0,0,0,.25);
}

.header-row{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
}

.logo{
  font-size:25px;
  font-weight:bold;
}

.status{
  display:flex;
  align-items:center;
  gap:8px;
  font-size:13px;
}

.status-light{
  width:13px;
  height:13px;
  border-radius:50%;
  background:#777;
}

.status-light.online{
  background:#00ff55;
  box-shadow:0 0 8px #00ff55,0 0 18px #00ff55;
  animation:blink 1s infinite;
}

.status-light.offline{
  background:#ff3030;
  box-shadow:0 0 10px #ff3030;
}

.status-light.warning{
  background:#ffd000;
  box-shadow:0 0 10px #ffd000;
}

@keyframes blink{
  0%,100%{opacity:1}
  50%{opacity:.25}
}

.themes{
  display:flex;
  justify-content:center;
  gap:10px;
  margin:15px 0;
}

.theme{
  width:40px;
  height:40px;
  border-radius:50%;
  border:3px solid #fff;
  cursor:pointer;
}

.theme-yellow{background:#ffd900}
.theme-blue{background:#087cf5}
.theme-purple{background:#7028c9}
.theme-orange{background:#ff7800}

.market{
  display:grid;
  grid-template-columns:repeat(6,1fr);
  gap:10px;
  margin-bottom:18px;
}

.coin{
  background:rgba(0,0,0,.93);
  border-radius:18px;
  padding:13px 8px;
  text-align:center;
  box-shadow:0 7px 22px rgba(0,0,0,.25);
}

.coin img{
  width:42px;
  height:42px;
  border-radius:50%;
  margin-bottom:6px;
}

.coin-name{
  font-size:14px;
  font-weight:bold;
}

.coin-price{
  direction:ltr;
  margin-top:7px;
  font-size:14px;
  font-weight:bold;
  white-space:nowrap;
}

.coin-state{
  margin-top:6px;
  font-size:10px;
  color:#00ff55;
}

.exchange{
  background:rgba(0,0,0,.95);
  border-radius:25px;
  padding:22px;
  box-shadow:0 12px 35px rgba(0,0,0,.3);
}

.exchange-title{
  text-align:center;
  font-size:25px;
  font-weight:bold;
  margin-bottom:20px;
}

.exchange-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:18px;
}

.card{
  background:#171717;
  border-radius:20px;
  padding:17px;
}

.card-title{
  font-size:15px;
  font-weight:bold;
  margin-bottom:10px;
}

select,
input{
  width:100%;
  border:0;
  outline:none;
  background:#292929;
  color:#fff;
  border-radius:13px;
  padding:14px;
  font-size:16px;
}

input{
  margin-top:10px;
  direction:ltr;
  text-align:left;
}

.result{
  margin-top:10px;
  background:#202020;
  border-radius:12px;
  padding:12px;
  direction:ltr;
  text-align:center;
  min-height:45px;
  font-weight:bold;
}

.trade-buttons{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:15px;
  margin-top:20px;
}

.trade{
  position:relative;
  overflow:hidden;
  border:0;
  border-radius:20px;
  padding:21px;
  color:#fff;
  font-size:25px;
  font-weight:bold;
  cursor:pointer;
  transition:.2s;
}

.trade:hover{
  transform:scale(1.02);
}

.trade:active{
  transform:scale(.97);
}

.buy{
  background:#08a842;
  box-shadow:0 0 15px rgba(0,255,80,.35);
}

.sell{
  background:#df1834;
  box-shadow:0 0 15px rgba(255,0,40,.35);
}

.trade::after{
  content:"";
  position:absolute;
  top:0;
  left:-100%;
  width:50%;
  height:100%;
  background:rgba(255,255,255,.18);
  transform:skewX(-25deg);
  animation:shine 2s infinite;
}

@keyframes shine{
  0%{left:-100%}
  45%,100%{left:150%}
}

.message{
  text-align:center;
  margin-top:15px;
  color:#ddd;
  font-size:13px;
  min-height:25px;
}

.info{
  margin-top:18px;
  background:#171717;
  border-radius:17px;
  padding:15px;
  color:#ddd;
  font-size:12px;
  line-height:2;
  text-align:center;
}

/* =========================
   TRANSACTIONS
========================= */

.transactions{
  margin-top:20px;
  background:rgba(0,0,0,.95);
  border-radius:25px;
  padding:22px;
  box-shadow:0 12px 35px rgba(0,0,0,.3);
}

.section-title{
  text-align:center;
  font-size:23px;
  font-weight:bold;
  margin-bottom:18px;
}

.address-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:12px;
}

.address-box{
  background:#171717;
  border-radius:17px;
  padding:15px;
}

.address-name{
  font-weight:bold;
  margin-bottom:8px;
}

.network{
  color:#aaa;
  font-size:11px;
  margin-bottom:8px;
}

.address-row{
  display:flex;
  gap:8px;
  align-items:center;
}

.address-value{
  flex:1;
  direction:ltr;
  text-align:left;
  background:#292929;
  border-radius:10px;
  padding:11px;
  font-size:11px;
  word-break:break-all;
}

.copy-btn{
  border:0;
  background:#087cf5;
  color:#fff;
  border-radius:10px;
  padding:11px 13px;
  cursor:pointer;
  font-weight:bold;
}

.copy-btn:active{
  transform:scale(.95);
}

.register-box{
  margin-top:20px;
  background:#171717;
  border-radius:20px;
  padding:18px;
}

.form-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:14px;
}

.form-item label{
  display:block;
  font-size:13px;
  margin-bottom:7px;
}

.form-item input,
.form-item select{
  margin-top:0;
}

.public-address{
  margin-top:10px;
  background:#202020;
  border-radius:12px;
  padding:12px;
  direction:ltr;
  text-align:left;
  word-break:break-all;
  font-size:12px;
}

.register-btn{
  width:100%;
  margin-top:15px;
  padding:17px;
  border:0;
  border-radius:15px;
  background:#08a842;
  color:#fff;
  font-size:19px;
  font-weight:bold;
  cursor:pointer;
}

.tracking-result{
  margin-top:15px;
  background:#202020;
  border-radius:14px;
  padding:15px;
  text-align:center;
  line-height:2;
  display:none;
}

.tracking-code{
  direction:ltr;
  font-size:20px;
  font-weight:bold;
  color:#ffd000;
  letter-spacing:1px;
}

.all-transactions{
  margin-top:20px;
  background:#171717;
  border-radius:20px;
  padding:18px;
}

.transaction-list{
  display:flex;
  flex-direction:column;
  gap:12px;
  max-height:650px;
  overflow:auto;
}

.transaction-item{
  background:#202020;
  border-radius:15px;
  padding:15px;
  border-right:5px solid #ffd000;
}

.transaction-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:10px;
  margin-bottom:10px;
}

.transaction-code{
  direction:ltr;
  font-weight:bold;
  color:#ffd000;
}

.buy-label{
  background:#08a842;
  padding:5px 9px;
  border-radius:8px;
  font-size:11px;
}

.sell-label{
  background:#df1834;
  padding:5px 9px;
  border-radius:8px;
  font-size:11px;
}

.transaction-details{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:7px;
  color:#ddd;
  font-size:12px;
}

.transaction-details div{
  background:#292929;
  padding:8px;
  border-radius:8px;
  word-break:break-all;
}

.empty-transactions{
  text-align:center;
  color:#aaa;
  padding:20px;
}

.status-pending{
  color:#ffd000;
  font-weight:bold;
}

.status-confirmed{
  color:#00ff55;
  font-weight:bold;
}

.notice{
  margin-top:12px;
  color:#aaa;
  font-size:11px;
  text-align:center;
  line-height:1.9;
}

@media(max-width:950px){
  .market{
    grid-template-columns:repeat(3,1fr);
  }

  .address-grid{
    grid-template-columns:1fr;
  }
}

@media(max-width:650px){

  .header-row{
    flex-direction:column;
  }

  .market{
    grid-template-columns:repeat(2,1fr);
  }

  .exchange-grid{
    grid-template-columns:1fr;
  }

  .trade-buttons{
    grid-template-columns:1fr;
  }

  .logo{
    font-size:21px;
  }

  .form-grid{
    grid-template-columns:1fr;
  }

  .transaction-details{
    grid-template-columns:1fr;
  }
}
</style>
</head>

<body>

<div class="container">

<div class="header">
  <div class="header-row">
    <div class="logo">₿ Crypto Exchange</div>

    <div class="status">
      <span id="globalLight" class="status-light offline"></span>
      <span id="globalStatus">در حال اتصال به بازار...</span>
    </div>
  </div>
</div>

<div class="themes">

  <button class="theme theme-yellow" onclick="setTheme('')"></button>
  <button class="theme theme-blue" onclick="setTheme('blue')"></button>
  <button class="theme theme-purple" onclick="setTheme('purple')"></button>
  <button class="theme theme-orange" onclick="setTheme('orange')"></button>

</div>

<div class="market">

<div class="coin">
<img src="https://assets.coingecko.com/coins/images/1/large/bitcoin.png" alt="Bitcoin">
<div class="coin-name">Bitcoin</div>
<div id="price-BTC" class="coin-price">در حال دریافت...</div>
<div id="state-BTC" class="coin-state">● اتصال</div>
</div>

<div class="coin">
<img src="https://assets.coingecko.com/coins/images/780/large/bitcoin-cash-circle.png" alt="Bitcoin Cash">
<div class="coin-name">Bitcoin Cash</div>
<div id="price-BCH" class="coin-price">در حال دریافت...</div>
<div id="state-BCH" class="coin-state">● اتصال</div>
</div>

<div class="coin">
<img src="https://assets.coingecko.com/coins/images/1094/large/tron-logo.png" alt="TRON">
<div class="coin-name">TRON</div>
<div id="price-TRX" class="coin-price">در حال دریافت...</div>
<div id="state-TRX" class="coin-state">● اتصال</div>
</div>

<div class="coin">
<img src="https://assets.coingecko.com/coins/images/2/large/litecoin.png" alt="Litecoin">
<div class="coin-name">Litecoin</div>
<div id="price-LTC" class="coin-price">در حال دریافت...</div>
<div id="state-LTC" class="coin-state">● اتصال</div>
</div>

<div class="coin">
<img src="https://assets.coingecko.com/coins/images/5/large/dogecoin.png" alt="Dogecoin">
<div class="coin-name">Dogecoin</div>
<div id="price-DOGE" class="coin-price">در حال دریافت...</div>
<div id="state-DOGE" class="coin-state">● اتصال</div>
</div>

<div class="coin">
<img src="https://assets.coingecko.com/coins/images/325/large/Tether.png" alt="USDT">
<div class="coin-name">Tether</div>
<div id="price-USDT" class="coin-price">$1.00</div>
<div class="coin-state" style="color:#00ff55">● فعال</div>
</div>

</div>

<div class="exchange">

<div class="exchange-title">تبدیل ارز</div>

<div class="exchange-grid">

<div class="card">

<div class="card-title">ارزی که می‌دهی</div>

<select id="fromCoin">

<option value="BTC">BTC - Bitcoin</option>
<option value="BCH">BCH - Bitcoin Cash</option>
<option value="TRX">TRX - TRON</option>
<option value="LTC">LTC - Litecoin</option>
<option value="DOGE">DOGE - Dogecoin</option>
<option value="USDT">USDT - Tether</option>

</select>

<input id="fromAmount"
       type="number"
       min="0"
       step="any"
       placeholder="مقدار">

</div>

<div class="card">

<div class="card-title">ارزی که می‌گیری</div>

<select id="toCoin">

<option value="USDT">USDT - Tether</option>
<option value="BTC">BTC - Bitcoin</option>
<option value="BCH">BCH - Bitcoin Cash</option>
<option value="TRX">TRX - TRON</option>
<option value="LTC">LTC - Litecoin</option>
<option value="DOGE">DOGE - Dogecoin</option>

</select>

<div id="toAmount" class="result">مقدار دریافتی</div>

</div>

</div>

<div class="trade-buttons">

<button class="trade buy" onclick="trade('BUY')">
🟢 BUY
</button>

<button class="trade sell" onclick="trade('SELL')">
🔴 SELL
</button>

</div>

<div id="message" class="message">
قیمت‌ها در حال دریافت هستند...
</div>

<div class="info">

قیمت‌ها از چندین منبع بازار بررسی می‌شوند.
اگر یک منبع قطع شود، منابع دیگر استفاده می‌شوند.
اگر تمام منابع موقتاً قطع شوند، آخرین قیمت معتبر
روی سایت باقی می‌ماند تا اتصال دوباره برقرار شود.

</div>

</div>


<!-- =====================================================
     TRANSACTION SECTION
===================================================== -->

<div class="transactions">

<div class="section-title">
ثبت معامله و آدرس‌های واریز
</div>


<!-- PUBLIC ADDRESSES -->

<div class="address-grid">

<div class="address-box">

<div class="address-name">₿ BTC</div>
<div class="network">شبکه Bitcoin</div>

<div class="address-row">
<div class="address-value">
1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV
</div>

<button class="copy-btn"
onclick="copyAddress('1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV',this)">
کپی
</button>
</div>

</div>


<div class="address-box">

<div class="address-name">₿ BCH</div>
<div class="network">شبکه Bitcoin Cash</div>

<div class="address-row">
<div class="address-value">
bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku
</div>

<button class="copy-btn"
onclick="copyAddress('bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku',this)">
کپی
</button>
</div>

</div>


<div class="address-box">

<div class="address-name">TRX</div>
<div class="network">شبکه TRON</div>

<div class="address-row">
<div class="address-value">
TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3
</div>

<button class="copy-btn"
onclick="copyAddress('TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3',this)">
کپی
</button>
</div>

</div>


<div class="address-box">

<div class="address-name">LTC</div>
<div class="network">شبکه Litecoin</div>

<div class="address-row">
<div class="address-value">
LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c
</div>

<button class="copy-btn"
onclick="copyAddress('LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c',this)">
کپی
</button>
</div>

</div>


<div class="address-box">

<div class="address-name">Ð DOGE</div>
<div class="network">شبکه Dogecoin</div>

<div class="address-row">
<div class="address-value">
DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk
</div>

<button class="copy-btn"
onclick="copyAddress('DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk',this)">
کپی
</button>
</div>

</div>


<div class="address-box">

<div class="address-name">₮ USDT</div>
<div class="network">شبکه BNB Smart Chain - BEP20</div>

<div class="address-row">
<div class="address-value">
0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6
</div>

<button class="copy-btn"
onclick="copyAddress('0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6',this)">
کپی
</button>
</div>

</div>

</div>


<!-- REGISTER -->

<div class="register-box">

<div class="section-title">
ثبت تراکنش
</div>

<div class="form-grid">


<div class="form-item">

<label>نوع معامله</label>

<select id="transactionType">

<option value="BUY">🟢 BUY - خرید</option>
<option value="SELL">🔴 SELL - فروش</option>

</select>

</div>


<div class="form-item">

<label>ارزی که می‌دهی</label>

<select id="transactionFrom">

<option value="BTC">BTC - Bitcoin</option>
<option value="BCH">BCH - Bitcoin Cash</option>
<option value="TRX">TRX - TRON</option>
<option value="LTC">LTC - Litecoin</option>
<option value="DOGE">DOGE - Dogecoin</option>
<option value="USDT">USDT - Tether BEP20</option>

</select>

</div>


<div class="form-item">

<label>مقدار معامله</label>

<input id="transactionAmount"
       type="number"
       min="0"
       step="any"
       placeholder="مقدار ارز">

</div>


<div class="form-item">

<label>ارزی که می‌گیری</label>

<select id="transactionTo">

<option value="USDT">USDT - Tether</option>
<option value="BTC">BTC - Bitcoin</option>
<option value="BCH">BCH - Bitcoin Cash</option>
<option value="TRX">TRX - TRON</option>
<option value="LTC">LTC - Litecoin</option>
<option value="DOGE">DOGE - Dogecoin</option>

</select>

</div>


<div class="form-item">

<label>آدرس کیف پول شما</label>

<input id="userWallet"
       type="text"
       placeholder="آدرس کیف پول دریافت شما">

</div>


<div class="form-item">

<label>TXID / هش تراکنش - اختیاری</label>

<input id="txid"
       type="text"
       placeholder="TXID تراکنش واریز">

</div>

</div>


<div style="margin-top:15px">

<div class="card-title">
آدرس عمومی برای واریز ارز انتخاب‌شده
</div>

<div id="selectedNetwork" class="network">
شبکه
</div>

<div class="public-address"
     id="selectedAddress">
آدرس
</div>

<button class="copy-btn"
        style="width:100%;margin-top:10px"
        onclick="copySelectedAddress()">
📋 کپی آدرس واریز
</button>

</div>


<button class="register-btn"
        onclick="registerTransaction()">
ثبت تراکنش و دریافت کد پیگیری
</button>


<div id="trackingResult" class="tracking-result">

<div>تراکنش شما ثبت شد</div>

<div style="margin-top:5px">
کد پیگیری:
</div>

<div id="newTrackingCode"
     class="tracking-code">
</div>

<div style="margin-top:8px;color:#ffd000">
وضعیت: در انتظار بررسی
</div>

</div>

<div class="notice">
ثبت این فرم به معنی ثبت درخواست معامله است.
تأیید نهایی تراکنش پس از بررسی واریز و تراکنش شبکه انجام می‌شود.
</div>

</div>


<!-- TRACKING -->

<div class="register-box">

<div class="section-title">
پیگیری تراکنش
</div>

<input id="trackingSearch"
       type="text"
       placeholder="کد پیگیری را وارد کنید">

<button class="register-btn"
        style="background:#087cf5"
        onclick="findTransaction()">
🔎 پیگیری
</button>

<div id="trackingSearchResult"
     class="tracking-result">
</div>

</div>


<!-- ALL TRANSACTIONS -->

<div class="all-transactions">

<div class="section-title">
همه تراکنش‌های ثبت‌شده
</div>

<div id="transactionList"
     class="transaction-list">

<div class="empty-transactions">
هنوز تراکنشی ثبت نشده است.
</div>

</div>

</div>

</div>

</div>


<script>

/* =====================================================
   COINS
===================================================== */

const COINS = [
  "BTC",
  "BCH",
  "TRX",
  "LTC",
  "DOGE"
];


/* =====================================================
   PRICES
===================================================== */

const prices = {
  BTC:null,
  BCH:null,
  TRX:null,
  LTC:null,
  DOGE:null,
  USDT:1
};


/* =====================================================
   BINANCE SYMBOL
===================================================== */

const binanceSymbols = {
  BTC:"BTCUSDT",
  BCH:"BCHUSDT",
  TRX:"TRXUSDT",
  LTC:"LTCUSDT",
  DOGE:"DOGEUSDT"
};


/* =====================================================
   FORMAT PRICE
===================================================== */

function formatPrice(value){

  if(!Number.isFinite(value)){
    return "قیمت در دسترس نیست";
  }

  let digits = 2;

  if(value < 1){
    digits = 6;
  }

  if(value < 0.01){
    digits = 8;
  }

  return "$" +
    Number(value).toLocaleString(
      "en-US",
      {
        minimumFractionDigits:digits,
        maximumFractionDigits:digits
      }
    );
}


/* =====================================================
   MEDIAN
===================================================== */

function median(list){

  const values = list
    .filter(
      x =>
        Number.isFinite(x) &&
        x > 0
    )
    .sort(
      (a,b)=>a-b
    );

  if(values.length === 0){
    return null;
  }

  const middle =
    Math.floor(values.length / 2);

  if(values.length % 2){
    return values[middle];
  }

  return (
    values[middle - 1] +
    values[middle]
  ) / 2;
}


/* =====================================================
   FETCH
===================================================== */

async function getJSON(url,timeout=7000){

  const controller =
    new AbortController();

  const timer =
    setTimeout(
      ()=>controller.abort(),
      timeout
    );

  try{

    const response =
      await fetch(
        url +
        (
          url.includes("?")
          ? "&"
          : "?"
        ) +
        "_=" +
        Date.now(),
        {
          cache:"no-store",
          signal:controller.signal
        }
      );

    if(!response.ok){
      throw new Error("HTTP "+response.status);
    }

    return await response.json();

  }finally{

    clearTimeout(timer);

  }
}


/* =====================================================
   BINANCE
===================================================== */

async function getBinance(coin){

  const data =
    await getJSON(
      "https://api.binance.com/api/v3/ticker/price?symbol="+
      binanceSymbols[coin]
    );

  const price =
    Number(data?.price);

  if(price > 0){
    return price;
  }

  throw new Error("Binance");
}


/* =====================================================
   COINBASE
===================================================== */

async function getCoinbase(coin){

  const data =
    await getJSON(
      "https://api.coinbase.com/v2/prices/"+
      coin+
      "-USD/spot"
    );

  const price =
    Number(data?.data?.amount);

  if(price > 0){
    return price;
  }

  throw new Error("Coinbase");
}


/* =====================================================
   KRAKEN
===================================================== */

async function getKraken(coin){

  const pairs = {
    BTC:"XBTUSD",
    BCH:"BCHUSD",
    TRX:"TRXUSD",
    LTC:"LTCUSD",
    DOGE:"DOGEUSD"
  };

  const data =
    await getJSON(
      "https://api.kraken.com/0/public/Ticker?pair="+
      pairs[coin]
    );

  const key =
    Object.keys(data?.result || {})[0];

  const price =
    Number(
      data?.result?.[key]?.c?.[0]
    );

  if(price > 0){
    return price;
  }

  throw new Error("Kraken");
}


/* =====================================================
   KUCOIN
===================================================== */

async function getKuCoin(coin){

  const data =
    await getJSON(
      "https://api.kucoin.com/api/v1/market/orderbook/level1?symbol="+
      coin+
      "-USDT"
    );

  const price =
    Number(data?.data?.price);

  if(price > 0){
    return price;
  }

  throw new Error("KuCoin");
}


/* =====================================================
   OKX
===================================================== */

async function getOKX(coin){

  const data =
    await getJSON(
      "https://www.okx.com/api/v5/market/ticker?instId="+
      coin+
      "-USDT"
    );

  const price =
    Number(data?.data?.[0]?.last);

  if(price > 0){
    return price;
  }

  throw new Error("OKX");
}


/* =====================================================
   BYBIT
===================================================== */

async function getBybit(coin){

  const data =
    await getJSON(
      "https://api.bybit.com/v5/market/tickers?category=spot&symbol="+
      coin+
      "USDT"
    );

  const price =
    Number(data?.result?.list?.[0]?.lastPrice);

  if(price > 0){
    return price;
  }

  throw new Error("Bybit");
}


/* =====================================================
   GATE
===================================================== */

async function getGate(coin){

  const data =
    await getJSON(
      "https://api.gateio.ws/api/v4/spot/tickers?currency_pair="+
      coin+
      "_USDT"
    );

  const price =
    Number(data?.[0]?.last);

  if(price > 0){
    return price;
  }

  throw new Error("Gate");
}


/* =====================================================
   BITGET
===================================================== */

async function getBitget(coin){

  const data =
    await getJSON(
      "https://api.bitget.com/api/v2/spot/market/tickers?symbol="+
      coin+
      "USDT"
    );

  const price =
    Number(data?.data?.[0]?.lastPr);

  if(price > 0){
    return price;
  }

  throw new Error("Bitget");
}


/* =====================================================
   MEXC
===================================================== */

async function getMexc(coin){

  const data =
    await getJSON(
      "https://api.mexc.com/api/v3/ticker/price?symbol="+
      coin+
      "USDT"
    );

  const price =
    Number(data?.price);

  if(price > 0){
    return price;
  }

  throw new Error("MEXC");
}


/* =====================================================
   HTX
===================================================== */

async function getHtx(coin){

  const data =
    await getJSON(
      "https://api.huobi.pro/market/detail/merged?symbol="+
      coin.toLowerCase()+
      "usdt"
    );

  const price =
    Number(data?.tick?.close);

  if(price > 0){
    return price;
  }

  throw new Error("HTX");
}


/* =====================================================
   LBANK
===================================================== */

async function getLbank(coin){

  const data =
    await getJSON(
      "https://api.lbkex.com/v2/ticker/24hr.do?symbol="+
      coin.toLowerCase()+
      "_usdt"
    );

  let price = null;

  if(Array.isArray(data?.data)){

    const item = data.data[0];

    price =
      Number(
        item?.latest ||
        item?.latestPrice ||
        item?.price ||
        item?.close
      );

  }else{

    price =
      Number(
        data?.data?.latest ||
        data?.data?.latestPrice ||
        data?.data?.price ||
        data?.data?.close
      );

  }

  if(price > 0){
    return price;
  }

  throw new Error("LBank");
}


/* =====================================================
   COINEX
===================================================== */

async function getCoinEx(coin){

  const data =
    await getJSON(
      "https://api.coinex.com/v2/spot/ticker?market="+
      coin.toLowerCase()+
      "usdt"
    );

  const item =
    data?.data?.[0];

  const price =
    Number(
      item?.last ||
      item?.last_price
    );

  if(price > 0){
    return price;
  }

  throw new Error("CoinEx");
}


/* =====================================================
   BITMART
===================================================== */

async function getBitMart(coin){

  const data =
    await getJSON(
      "https://api-cloud.bitmart.com/spot/v1/ticker?symbol="+
      coin+
      "_USDT"
    );

  const price =
    Number(
      data?.data?.tickers?.[0]?.last_price
    );

  if(price > 0){
    return price;
  }

  throw new Error("BitMart");
}


/* =====================================================
   CRYPTO.COM
===================================================== */

async function getCryptoCom(coin){

  const data =
    await getJSON(
      "https://api.crypto.com/exchange/v1/public/get-ticker?instrument_name="+
      coin+
      "_USDT"
    );

  const price =
    Number(
      data?.result?.data?.[0]?.a
    );

  if(price > 0){
    return price;
  }

  throw new Error("Crypto");
}


/* =====================================================
   GEMINI
===================================================== */

async function getGemini(coin){

  const data =
    await getJSON(
      "https://api.gemini.com/v1/pubticker/"+
      coin.toLowerCase()+
      "usd"
    );

  const price =
    Number(data?.last);

  if(price > 0){
    return price;
  }

  throw new Error("Gemini");
}


/* =====================================================
   BITSTAMP
===================================================== */

async function getBitstamp(coin){

  const data =
    await getJSON(
      "https://www.bitstamp.net/api/v2/ticker/"+
      coin.toLowerCase()+
      "usd/"
    );

  const price =
    Number(data?.last);

  if(price > 0){
    return price;
  }

  throw new Error("Bitstamp");
}


/* =====================================================
   WHITEBIT
===================================================== */

async function getWhiteBit(coin){

  const data =
    await getJSON(
      "https://whitebit.com/api/v4/public/ticker?market="+
      coin+
      "_USDT"
    );

  const price =
    Number(data?.last_price);

  if(price > 0){
    return price;
  }

  throw new Error("WhiteBit");
}


/* =====================================================
   PHEMEX
===================================================== */

async function getPhemex(coin){

  const data =
    await getJSON(
      "https://api.phemex.com/md/ticker/24hr?symbol="+
      coin+
      "USDT"
    );

  const price =
    Number(
      data?.result?.closeRp ||
      data?.result?.last
    );

  if(price > 0){
    return price;
  }

  throw new Error("Phemex");
}


/* =====================================================
   ASCENDEX
===================================================== */

async function getAscendEX(coin){

  const data =
    await getJSON(
      "https://ascendex.com/api/pro/v1/ticker?symbol="+
      coin+
      "/USDT"
    );

  const price =
    Number(data?.data?.close);

  if(price > 0){
    return price;
  }

  throw new Error("AscendEX");
}


/* =====================================================
   COINGECKO
===================================================== */

async function getCoinGecko(){

  const data =
    await getJSON(
      "https://api.coingecko.com/api/v3/simple/price"+
      "?ids=bitcoin,bitcoin-cash,tron,litecoin,dogecoin"+
      "&vs_currencies=usd"
    );

  return {

    BTC:Number(data?.bitcoin?.usd),

    BCH:Number(data?.["bitcoin-cash"]?.usd),

    TRX:Number(data?.tron?.usd),

    LTC:Number(data?.litecoin?.usd),

    DOGE:Number(data?.dogecoin?.usd)

  };

}


/* =====================================================
   ALL SOURCES
===================================================== */

function sourcesFor(coin){

  return [

    getBinance(coin),
    getCoinbase(coin),
    getKraken(coin),
    getKuCoin(coin),
    getOKX(coin),
    getBybit(coin),
    getGate(coin),
    getBitget(coin),
    getMexc(coin),
    getHtx(coin),
    getLbank(coin),
    getCoinEx(coin),
    getBitMart(coin),
    getCryptoCom(coin),
    getGemini(coin),
    getBitstamp(coin),
    getWhiteBit(coin),
    getPhemex(coin),
    getAscendEX(coin)

  ];

}


/* =====================================================
   UPDATE COIN
===================================================== */

async function updateCoin(coin){

  const results =
    await Promise.allSettled(
      sourcesFor(coin)
    );

  const validPrices = [];

  results.forEach(result=>{

    if(
      result.status === "fulfilled" &&
      Number.isFinite(result.value) &&
      result.value > 0
    ){

      validPrices.push(result.value);

    }

  });


  try{

    const gecko =
      await getCoinGecko();

    const gp =
      Number(gecko[coin]);

    if(
      Number.isFinite(gp) &&
      gp > 0
    ){

      validPrices.push(gp);

    }

  }catch(error){

    console.log("CoinGecko unavailable");

  }


  const finalPrice =
    median(validPrices);

  const priceElement =
    document.getElementById(
      "price-"+coin
    );

  const stateElement =
    document.getElementById(
      "state-"+coin
    );


  if(finalPrice !== null){

    prices[coin] =
      finalPrice;

    try{

      localStorage.setItem(
        "lastPrice_"+coin,
        String(finalPrice)
      );

    }catch(error){}

    priceElement.textContent =
      formatPrice(finalPrice);

    stateElement.textContent =
      "● آنلاین | "+
      validPrices.length+
      " منبع";

    stateElement.style.color =
      "#00ff55";

    return true;

  }


  if(prices[coin] === null){

    try{

      const saved =
        Number(
          localStorage.getItem(
            "lastPrice_"+coin
          )
        );

      if(
        Number.isFinite(saved) &&
        saved > 0
      ){

        prices[coin] =
          saved;

      }

    }catch(error){}

  }


  if(prices[coin] !== null){

    priceElement.textContent =
      formatPrice(prices[coin]);

    stateElement.textContent =
      "● آخرین قیمت معتبر";

    stateElement.style.color =
      "#ffd000";

  }else{

    priceElement.textContent =
      "قیمت در دسترس نیست";

    stateElement.textContent =
      "● قطع";

    stateElement.style.color =
      "#ff3030";

  }

  return false;

}


/* =====================================================
   UPDATE ALL
===================================================== */

async function updateAllPrices(){

  const results =
    await Promise.all(
      COINS.map(
        coin =>
          updateCoin(coin)
      )
    );

  let onlineCount = 0;

  results.forEach(ok=>{

    if(ok){
      onlineCount++;
    }

  });


  const light =
    document.getElementById(
      "globalLight"
    );

  const status =
    document.getElementById(
      "globalStatus"
    );


  if(onlineCount > 0){

    light.className =
      "status-light online";

    status.textContent =
      "بازار آنلاین | "+
      onlineCount+
      " ارز به‌روز شد";

  }else{

    light.className =
      "status-light warning";

    status.textContent =
      "اتصال موقتاً قطع | آخرین قیمت حفظ شد";

  }

  calculate();

}


/* =====================================================
   CALCULATE
===================================================== */

function calculate(){

  const from =
    document.getElementById(
      "fromCoin"
    ).value;

  const to =
    document.getElementById(
      "toCoin"
    ).value;

  const amount =
    Number(
      document.getElementById(
        "fromAmount"
      ).value
    );

  const output =
    document.getElementById(
      "toAmount"
    );

  const fromPrice =
    Number(prices[from]);

  const toPrice =
    Number(prices[to]);


  if(
    !Number.isFinite(amount) ||
    amount <= 0 ||
    !Number.isFinite(fromPrice) ||
    !Number.isFinite(toPrice) ||
    toPrice <= 0
  ){

    output.textContent =
      "مقدار دریافتی";

    return;

  }


  const usdValue =
    amount * fromPrice;

  const received =
    usdValue / toPrice;


  output.textContent =
    received.toLocaleString(
      "en-US",
      {
        maximumFractionDigits:10
      }
    )+
    " "+
    to;

}


/* =====================================================
   WALLET ADDRESSES
===================================================== */

const walletAddresses = {

  BTC:{
    network:"Bitcoin",
    address:"1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV"
  },

  BCH:{
    network:"Bitcoin Cash",
    address:"bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku"
  },

  TRX:{
    network:"TRON",
    address:"TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"
  },

  LTC:{
    network:"Litecoin",
    address:"LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c"
  },

  DOGE:{
    network:"Dogecoin",
    address:"DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk"
  },

  USDT:{
    network:"BNB Smart Chain - BEP20",
    address:"0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6"
  }

};


/* =====================================================
   UPDATE SELECTED ADDRESS
===================================================== */

function updateSelectedAddress(){

  const coin =
    document.getElementById(
      "transactionFrom"
    ).value;

  const data =
    walletAddresses[coin];

  document.getElementById(
    "selectedNetwork"
  ).textContent =
    "شبکه: "+data.network;

  document.getElementById(
    "selectedAddress"
  ).textContent =
    data.address;

}


/* =====================================================
   COPY ADDRESS
===================================================== */

function copyAddress(address,button){

  if(
    navigator.clipboard &&
    window.isSecureContext
  ){

    navigator.clipboard.writeText(address);

  }else{

    const area =
      document.createElement("textarea");

    area.value = address;
    document.body.appendChild(area);
    area.select();
    document.execCommand("copy");
    area.remove();

  }

  const oldText =
    button.textContent;

  button.textContent =
    "✓ کپی شد";

  setTimeout(
    ()=>{
      button.textContent =
        oldText;
    },
    1500
  );

}


/* =====================================================
   COPY SELECTED ADDRESS
===================================================== */

function copySelectedAddress(){

  const coin =
    document.getElementById(
      "transactionFrom"
    ).value;

  const address =
    walletAddresses[coin].address;

  copyAddress(
    address,
    document.querySelector(
      ".register-box .copy-btn"
    )
  );

}


/* =====================================================
   TRACKING CODE
===================================================== */

function createTrackingCode(){

  const now =
    new Date();

  const date =
    now.getFullYear()+
    String(now.getMonth()+1).padStart(2,"0")+
    String(now.getDate()).padStart(2,"0");

  const random =
    Math.random()
      .toString(36)
      .substring(2,8)
      .toUpperCase();

  return "TX-"+date+"-"+random;

}


/* =====================================================
   SAFE HTML
===================================================== */

function escapeHTML(value){

  return String(value ?? "")
    .replace(/&/g,"&amp;")
    .replace(/</g,"&lt;")
    .replace(/>/g,"&gt;")
    .replace(/"/g,"&quot;")
    .replace(/'/g,"&#039;");

}


/* =====================================================
   GET TRANSACTIONS
===================================================== */

function getTransactions(){

  try{

    return JSON.parse(
      localStorage.getItem(
        "exchangeTransactions"
      ) || "[]"
    );

  }catch(error){

    return [];

  }

}


/* =====================================================
   SAVE TRANSACTIONS
===================================================== */

function saveTransactions(list){

  localStorage.setItem(
    "exchangeTransactions",
    JSON.stringify(list)
  );

}


/* =====================================================
   REGISTER TRANSACTION
===================================================== */

function registerTransaction(){

  const type =
    document.getElementById(
      "transactionType"
    ).value;

  const from =
    document.getElementById(
      "transactionFrom"
    ).value;

  const to =
    document.getElementById(
      "transactionTo"
    ).value;

  const amount =
    Number(
      document.getElementById(
        "transactionAmount"
      ).value
    );

  const userWallet =
    document.getElementById(
      "userWallet"
    ).value.trim();

  const txid =
    document.getElementById(
      "txid"
    ).value.trim();


  if(
    !Number.isFinite(amount) ||
    amount <= 0
  ){

    alert("لطفاً مقدار معامله را وارد کنید.");
    return;

  }


  if(!userWallet){

    alert("لطفاً آدرس کیف پول خود را وارد کنید.");
    return;

  }


  const trackingCode =
    createTrackingCode();

  const publicAddress =
    walletAddresses[from].address;

  const network =
    walletAddresses[from].network;


  let receivedAmount =
    "";

  const fromPrice =
    Number(prices[from]);

  const toPrice =
    Number(prices[to]);


  if(
    Number.isFinite(fromPrice) &&
    Number.isFinite(toPrice) &&
    toPrice > 0
  ){

    receivedAmount =
      (
        amount *
        fromPrice /
        toPrice
      ).toLocaleString(
        "en-US",
        {
          maximumFractionDigits:10
        }
      );

  }


  const transaction = {

    trackingCode:trackingCode,

    type:type,

    from:from,

    to:to,

    amount:amount,

    receivedAmount:receivedAmount,

    publicAddress:publicAddress,

    network:network,

    userWallet:userWallet,

    txid:txid,

    status:"در انتظار بررسی",

    createdAt:new Date().toISOString()

  };


  const transactions =
    getTransactions();

  transactions.unshift(transaction);

  saveTransactions(transactions);


  document.getElementById(
    "newTrackingCode"
  ).textContent =
    trackingCode;


  document.getElementById(
    "trackingResult"
  ).style.display =
    "block";


  document.getElementById(
    "trackingSearch"
  ).value =
    trackingCode;


  renderTransactions();


  document.getElementById(
    "trackingResult"
  ).scrollIntoView({
    behavior:"smooth",
    block:"center"
  });

}


/* =====================================================
   RENDER ALL TRANSACTIONS
===================================================== */

function renderTransactions(){

  const list =
    document.getElementById(
      "transactionList"
    );

  const transactions =
    getTransactions();


  if(transactions.length === 0){

    list.innerHTML =
      '<div class="empty-transactions">'+
      'هنوز تراکنشی ثبت نشده است.'+
      '</div>';

    return;

  }


  list.innerHTML =
    transactions.map(tx=>{

      const typeClass =
        tx.type === "BUY"
        ? "buy-label"
        : "sell-label";

      const typeText =
        tx.type === "BUY"
        ? "🟢 BUY | خرید"
        : "🔴 SELL | فروش";


      const date =
        new Date(
          tx.createdAt
        ).toLocaleString(
          "fa-IR"
        );


      return `

<div class="transaction-item">

<div class="transaction-head">

<div class="transaction-code">
${escapeHTML(tx.trackingCode)}
</div>

<div class="${typeClass}">
${typeText}
</div>

</div>


<div class="transaction-details">

<div>
<b>ارز پرداختی:</b>
${escapeHTML(tx.from)}
</div>

<div>
<b>مقدار:</b>
${escapeHTML(tx.amount)}
${escapeHTML(tx.from)}
</div>

<div>
<b>ارز دریافتی:</b>
${escapeHTML(tx.to)}
</div>

<div>
<b>مقدار دریافتی:</b>
${escapeHTML(tx.receivedAmount || "در انتظار محاسبه")}
${escapeHTML(tx.to)}
</div>

<div>
<b>شبکه:</b>
${escapeHTML(tx.network)}
</div>

<div>
<b>وضعیت:</b>
<span class="status-pending">
${escapeHTML(tx.status)}
</span>
</div>

<div>
<b>آدرس عمومی واریز:</b>
${escapeHTML(tx.publicAddress)}
</div>

<div>
<b>آدرس کیف پول کاربر:</b>
${escapeHTML(tx.userWallet)}
</div>

<div>
<b>زمان ثبت:</b>
${escapeHTML(date)}
</div>

<div>
<b>TXID:</b>
${escapeHTML(tx.txid || "ثبت نشده")}
</div>

</div>

</div>

`;

    }).join("");

}


/* =====================================================
   FIND TRANSACTION
===================================================== */

function findTransaction(){

  const code =
    document.getElementById(
      "trackingSearch"
    ).value
    .trim()
    .toUpperCase();


  const result =
    document.getElementById(
      "trackingSearchResult"
    );


  if(!code){

    result.style.display =
      "block";

    result.innerHTML =
      "کد پیگیری را وارد کنید.";

    return;

  }


  const transactions =
    getTransactions();

  const tx =
    transactions.find(
      item =>
        String(
          item.trackingCode
        ).toUpperCase() === code
    );


  result.style.display =
    "block";


  if(!tx){

    result.innerHTML =
      "❌ تراکنشی با این کد پیگیری پیدا نشد.";

    return;

  }


  result.innerHTML = `

<div>
<b>کد پیگیری</b>
</div>

<div class="tracking-code">
${escapeHTML(tx.trackingCode)}
</div>

<div style="margin-top:8px">
نوع:
${tx.type === "BUY" ? "🟢 خرید" : "🔴 فروش"}
</div>

<div>
${escapeHTML(tx.amount)}
${escapeHTML(tx.from)}
→
${escapeHTML(tx.to)}
</div>

<div style="margin-top:8px">
وضعیت:
<span class="status-pending">
${escapeHTML(tx.status)}
</span>
</div>

`;

}


/* =====================================================
   BUY / SELL
===================================================== */

function trade(type){

  const from =
    document.getElementById(
      "fromCoin"
    ).value;

  const to =
    document.getElementById(
      "toCoin"
    ).value;

  const amount =
    Number(
      document.getElementById(
        "fromAmount"
      ).value
    );

  const message =
    document.getElementById(
      "message"
    );


  if(
    !Number.isFinite(amount) ||
    amount <= 0
  ){

    message.textContent =
      "ابتدا مقدار ارز را وارد کن.";

    return;

  }


  document.getElementById(
    "transactionType"
  ).value =
    type;

  document.getElementById(
    "transactionFrom"
  ).value =
    from;

  document.getElementById(
    "transactionTo"
  ).value =
    to;

  document.getElementById(
    "transactionAmount"
  ).value =
    amount;


  updateSelectedAddress();


  if(type === "BUY"){

    message.textContent =
      "🟢 BUY | خرید "+
      to+
      " با "+
      from+
      " | مقدار "+
      amount;

  }else{

    message.textContent =
      "🔴 SELL | فروش "+
      from+
      " برای دریافت "+
      to+
      " | مقدار "+
      amount;

  }


  document.querySelector(
    ".transactions"
  ).scrollIntoView({
    behavior:"smooth",
    block:"start"
  });

}


/* =====================================================
   INPUT EVENTS
===================================================== */

document
.getElementById("fromAmount")
.addEventListener(
  "input",
  calculate
);

document
.getElementById("fromCoin")
.addEventListener(
  "change",
  calculate
);

document
.getElementById("toCoin")
.addEventListener(
  "change",
  calculate
);

document
.getElementById("transactionFrom")
.addEventListener(
  "change",
  updateSelectedAddress
);


/* =====================================================
   THEMES
===================================================== */

function setTheme(theme){

  document.body.classList.remove(
    "blue",
    "purple",
    "orange"
  );

  if(theme){

    document.body.classList.add(
      theme
    );

  }

  try{

    localStorage.setItem(
      "theme",
      theme
    );

  }catch(error){}

}


try{

  const savedTheme =
    localStorage.getItem(
      "theme"
    );

  if(savedTheme){

    setTheme(savedTheme);

  }

}catch(error){}


/* =====================================================
   START
===================================================== */

updateSelectedAddress();

renderTransactions();

updateAllPrices();


/* Every 20 seconds */

setInterval(
  updateAllPrices,
  20000
);


/* Extra check after 5 seconds */

setTimeout(
  updateAllPrices,
  5000
);

</script>
<!-- ====== BANNER ====== -->
<style>
.crypto-banner{
width:100%;
box-sizing:border-box;
margin:20px 0;
padding:22px 15px;
border-radius:25px;
overflow:hidden;
position:relative;
background:linear-gradient(90deg,#006b2e,#00a83b,#72e000,#00a83b,#006b2e);
background-size:300% 100%;
animation:bgMove 6s linear infinite;
box-shadow:0 0 25px rgba(0,255,80,.45);
border:2px solid #b7ff00;
}

.crypto-banner-title{
text-align:center;
font-size:38px;
font-weight:900;
color:#ffe600;
text-shadow:0 0 8px #fff000,0 0 18px #ffb300;
white-space:nowrap;
animation:titleMove 4s ease-in-out infinite alternate;
}

.crypto-banner-sub{
text-align:center;
margin-top:10px;
font-size:22px;
font-weight:900;
color:white;
text-shadow:0 0 10px #000;
}

.crypto-coins{
display:flex;
justify-content:center;
align-items:center;
gap:14px;
margin-top:18px;
flex-wrap:wrap;
}

.crypto-coins span{
width:58px;
height:58px;
border-radius:50%;
display:flex;
align-items:center;
justify-content:center;
font-size:19px;
font-weight:900;
color:white;
background:linear-gradient(145deg,#222,#555);
border:3px solid #ffe600;
box-shadow:0 0 15px rgba(255,230,0,.7);
animation:coinFloat 2s ease-in-out infinite alternate;
}

.crypto-coins span:nth-child(2){animation-delay:.2s}
.crypto-coins span:nth-child(3){animation-delay:.4s}
.crypto-coins span:nth-child(4){animation-delay:.6s}
.crypto-coins span:nth-child(5){animation-delay:.8s}
.crypto-coins span:nth-child(6){animation-delay:1s}

@keyframes bgMove{
0%{background-position:0% 50%}
50%{background-position:100% 50%}
100%{background-position:0% 50%}
}

@keyframes titleMove{
from{transform:translateX(-25px)}
to{transform:translateX(25px)}
}

@keyframes coinFloat{
from{transform:translateY(0) rotate(-4deg)}
to{transform:translateY(-10px) rotate(4deg)}
}

@media(max-width:600px){
.crypto-banner-title{font-size:27px}
.crypto-banner-sub{font-size:17px}
.crypto-coins span{
width:48px;
height:48px;
font-size:15px;
}
}
</style>

<div class="crypto-banner">

<div class="crypto-banner-title">
🚀 صرافی تبادل 🚀
</div>

<div class="crypto-banner-sub">
تبادل ارز دیجیتال
</div>

<div class="crypto-coins">
<span>₿</span>
<span>₮</span>
<span>Ł</span>
<span>Ð</span>
<span>BCH</span>
<span>TRX</span>
</div>

</div>
<!-- ====== END BANNER ====== -->
<!-- =========================================================
     🔔 سیستم کامل زنگوله و اعلان‌ها
     محل قرار دادن: درست قبل از </body>
========================================================= -->

<div id="kbNotificationBell"
     onclick="KB_toggleNotifications()"
     aria-label="پیام‌ها">

  <span class="kbBellIcon">🔔</span>
  <span id="kbNotificationCount">0</span>

</div>


<!-- پنل پیام‌ها -->
<div id="kbNotificationPanel">

  <div class="kbNotificationHeader">

    <div class="kbNotificationTitle">
      🔔 پیام‌ها و تراکنش‌ها
    </div>

    <button onclick="KB_clearNotifications(event)">
      پاک کردن
    </button>

  </div>


  <div id="kbNotificationList">

    <div class="kbEmptyNotifications">
      پیام جدیدی وجود ندارد
    </div>

  </div>

</div>


<style>

/* ===============================
   🔔 زنگوله بالای سایت
================================ */

#kbNotificationBell {

  position: fixed;

  top: 15px;
  right: 18px;

  width: 58px;
  height: 58px;

  border-radius: 50%;

  background:
    linear-gradient(
      145deg,
      #fff3a0,
      #ffd700,
      #d99a00
    );

  display: flex;

  align-items: center;
  justify-content: center;

  cursor: pointer;

  z-index: 2147483647;

  box-shadow:
    0 0 8px #ffd700,
    0 0 20px rgba(255,215,0,.75),
    inset 0 2px 5px rgba(255,255,255,.8);

  border: 2px solid #fff2a8;

  animation:
    kbBellGlow 1.7s infinite;

  user-select: none;

}


/* آیکون زنگ */

.kbBellIcon {

  font-size: 31px;

  line-height: 1;

  display: block;

  animation:
    kbBellShake 2.5s infinite;

}


/* شماره پیام */

#kbNotificationCount {

  position: absolute;

  top: -5px;
  right: -5px;

  min-width: 22px;
  height: 22px;

  padding: 0 5px;

  background: #ff2020;

  color: white;

  border: 2px solid white;

  border-radius: 50px;

  font-size: 11px;

  font-weight: bold;

  display: none;

  align-items: center;
  justify-content: center;

  box-sizing: border-box;

  box-shadow:
    0 2px 8px rgba(0,0,0,.5);

}


/* درخشش زنگ */

@keyframes kbBellGlow {

  0% {
    transform: scale(1);
    box-shadow:
      0 0 8px #ffd700,
      0 0 15px rgba(255,215,0,.5);
  }

  50% {
    transform: scale(1.08);
    box-shadow:
      0 0 15px #ffd700,
      0 0 35px rgba(255,215,0,.95);
  }

  100% {
    transform: scale(1);
    box-shadow:
      0 0 8px #ffd700,
      0 0 15px rgba(255,215,0,.5);
  }

}


/* تکان خوردن زنگ */

@keyframes kbBellShake {

  0%, 70%, 100% {
    transform: rotate(0deg);
  }

  73% {
    transform: rotate(-15deg);
  }

  76% {
    transform: rotate(15deg);
  }

  79% {
    transform: rotate(-12deg);
  }

  82% {
    transform: rotate(12deg);
  }

  85% {
    transform: rotate(0deg);
  }

}


/* ===============================
   📋 پنل اعلان‌ها
================================ */

#kbNotificationPanel {

  position: fixed;

  top: 85px;
  right: 18px;

  width: 350px;

  max-width:
    calc(100vw - 36px);

  max-height: 520px;

  background: #101010;

  color: white;

  border: 1px solid #d4af37;

  border-radius: 16px;

  overflow: hidden;

  z-index: 2147483646;

  display: none;

  box-shadow:
    0 15px 45px rgba(0,0,0,.75),
    0 0 20px rgba(212,175,55,.25);

  animation:
    kbPanelOpen .2s ease;

}


@keyframes kbPanelOpen {

  from {
    opacity: 0;
    transform:
      translateY(-10px)
      scale(.96);
  }

  to {
    opacity: 1;
    transform:
      translateY(0)
      scale(1);
  }

}


/* ===============================
   عنوان پنل
================================ */

.kbNotificationHeader {

  background:
    linear-gradient(
      135deg,
      #d4af37,
      #9c7615
    );

  min-height: 55px;

  padding: 10px 12px;

  display: flex;

  align-items: center;

  justify-content: space-between;

  gap: 10px;

  box-sizing: border-box;

}


.kbNotificationTitle {

  font-weight: bold;

  font-size: 15px;

}


.kbNotificationHeader button {

  border: 1px solid white;

  background: #111;

  color: white;

  padding: 6px 9px;

  border-radius: 7px;

  cursor: pointer;

  font-size: 11px;

}


.kbNotificationHeader button:hover {

  background: #333;

}


/* ===============================
   لیست پیام‌ها
================================ */

#kbNotificationList {

  max-height: 450px;

  overflow-y: auto;

}


.kbNotificationItem {

  padding: 14px;

  border-bottom:
    1px solid #292929;

  background:
    rgba(255,255,255,.02);

  transition: .2s;

}


.kbNotificationItem:hover {

  background:
    rgba(255,215,0,.08);

}


.kbNotificationMessage {

  font-size: 14px;

  line-height: 1.8;

  word-break: break-word;

}


.kbNotificationTime {

  margin-top: 5px;

  color: #999;

  font-size: 10px;

}


/* پیام جدید */

.kbNotificationItem.new {

  border-right:
    3px solid #ffd700;

  background:
    rgba(255,215,0,.06);

}


/* ===============================
   وقتی پیام نداریم
================================ */

.kbEmptyNotifications {

  padding: 35px 15px;

  text-align: center;

  color: #999;

  font-size: 13px;

}


/* ===============================
   موبایل
================================ */

@media (max-width:600px) {

  #kbNotificationBell {

    top: 10px;
    right: 10px;

    width: 52px;
    height: 52px;

  }

  .kbBellIcon {

    font-size: 27px;

  }

  #kbNotificationPanel {

    top: 72px;
    right: 10px;

    width:
      calc(100vw - 20px);

  }

}


/* ===============================
   اسکرول زیبا
================================ */

#kbNotificationList::-webkit-scrollbar {

  width: 5px;

}

#kbNotificationList::-webkit-scrollbar-track {

  background: #111;

}

#kbNotificationList::-webkit-scrollbar-thumb {

  background: #b58b20;

  border-radius: 10px;

}

</style>


<script>

/* =========================================================
   🔔 سیستم اعلان KEYBAR
========================================================= */


/* دریافت پیام‌های قبلی */

let KB_notifications = [];

try {

  KB_notifications =
    JSON.parse(
      localStorage.getItem(
        "KEYBAR_notifications"
      ) || "[]"
    );

  if (!Array.isArray(KB_notifications)) {

    KB_notifications = [];

  }

} catch (error) {

  KB_notifications = [];

}


/* =========================================================
   ذخیره پیام‌ها
========================================================= */

function KB_saveNotifications() {

  try {

    localStorage.setItem(
      "KEYBAR_notifications",
      JSON.stringify(
        KB_notifications
      )
    );

  } catch (error) {

    console.log(
      "خطا در ذخیره اعلان‌ها",
      error
    );

  }

}


/* =========================================================
   نمایش تعداد پیام
========================================================= */

function KB_updateNotificationCount() {

  const count =
    document.getElementById(
      "kbNotificationCount"
    );

  if (!count) return;


  if (KB_notifications.length > 0) {

    count.textContent =
      KB_notifications.length > 99
        ? "99+"
        : KB_notifications.length;

    count.style.display =
      "flex";

  } else {

    count.style.display =
      "none";

  }

}


/* =========================================================
   نمایش پیام‌ها
========================================================= */

function KB_renderNotifications() {

  const list =
    document.getElementById(
      "kbNotificationList"
    );

  if (!list) return;


  if (KB_notifications.length === 0) {

    list.innerHTML = `
      <div class="kbEmptyNotifications">
        🔔 پیام جدیدی وجود ندارد
      </div>
    `;

    KB_updateNotificationCount();

    return;

  }


  list.innerHTML =
    KB_notifications.map(
      function(item) {

        return `
          <div class="kbNotificationItem new">

            <div class="kbNotificationMessage">
              ${KB_escapeHTML(item.message)}
            </div>

            <div class="kbNotificationTime">
              ${KB_escapeHTML(item.time)}
            </div>

          </div>
        `;

      }
    ).join("");


  KB_updateNotificationCount();

}


/* =========================================================
   جلوگیری از HTML خطرناک داخل پیام
========================================================= */

function KB_escapeHTML(text) {

  const div =
    document.createElement("div");

  div.textContent =
    String(text);

  return div.innerHTML;

}


/* =========================================================
   باز و بسته کردن پنل
========================================================= */

function KB_toggleNotifications() {

  const panel =
    document.getElementById(
      "kbNotificationPanel"
    );

  if (!panel) return;


  if (
    panel.style.display === "block"
  ) {

    panel.style.display =
      "none";

  } else {

    panel.style.display =
      "block";

  }

}


/* =========================================================
   اضافه کردن پیام جدید
========================================================= */

function KB_addNotification(message) {

  const now =
    new Date();


  let time;

  try {

    time =
      now.toLocaleString(
        "fa-IR",
        {
          dateStyle: "short",
          timeStyle: "short"
        }
      );

  } catch (error) {

    time =
      now.toLocaleString();

  }


  KB_notifications.unshift({

    message:
      String(message),

    time:
      time

  });


  /* فقط 50 پیام آخر */

  KB_notifications =
    KB_notifications.slice(
      0,
      50
    );


  KB_saveNotifications();

  KB_renderNotifications();


  /* =====================================================
     🔔 تکان شدید زنگ هنگام پیام جدید
  ===================================================== */

  const bell =
    document.getElementById(
      "kbNotificationBell"
    );


  if (bell) {

    bell.animate(

      [
        {
          transform:
            "rotate(0deg) scale(1)"
        },

        {
          transform:
            "rotate(-20deg) scale(1.15)"
        },

        {
          transform:
            "rotate(20deg) scale(1.15)"
        },

        {
          transform:
            "rotate(-15deg) scale(1.1)"
        },

        {
          transform:
            "rotate(15deg) scale(1.1)"
        },

        {
          transform:
            "rotate(0deg) scale(1)"
        }

      ],

      {
        duration: 800
      }

    );

  }


}


/* =========================================================
   پاک کردن پیام‌ها
========================================================= */

function KB_clearNotifications(event) {

  if (event) {

    event.stopPropagation();

  }


  KB_notifications = [];

  KB_saveNotifications();

  KB_renderNotifications();

}


/* =========================================================
   کلیک بیرون پنل
========================================================= */

document.addEventListener(
  "click",
  function(event) {

    const panel =
      document.getElementById(
        "kbNotificationPanel"
      );

    const bell =
      document.getElementById(
        "kbNotificationBell"
      );


    if (!panel || !bell) return;


    if (
      panel.style.display === "block" &&
      !panel.contains(event.target) &&
      !bell.contains(event.target)
    ) {

      panel.style.display =
        "none";

    }

  }
);


/* =========================================================
   پیام‌های نمونه
   این قسمت اجرا نمی‌شود؛ فقط برای استفاده در کد سایت است.
========================================================= */

/*

KB_addNotification(
  "💰 واریز جدید 50 USDT ثبت شد"
);


KB_addNotification(
  "📤 درخواست برداشت جدید ثبت شد"
);


KB_addNotification(
  "⚠️ مشکل در تراکنش کاربر ایجاد شد"
);


KB_addNotification(
  "🔄 تراکنش جدید در انتظار بررسی است"
);

*/


/* =========================================================
   شروع سیستم
========================================================= */

KB_renderNotifications();

</script>

<!-- =========================================================
     پایان سیستم زنگوله
========================================================= -->
</body>
</html>
