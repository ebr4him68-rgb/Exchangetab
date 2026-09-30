


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
<!-- 🔧 دکمه تنظیمات دایره‌ای -->
<div id="kbSettingsButton" onclick="kbOpenSettings()" title="تنظیمات">
  🔧
</div>

<!-- 🎨 پنل تم‌ها -->
<div id="kbSettingsPanel">

  <div class="kbSettingsHeader">
    <span>⚙️ تنظیمات سایت</span>
    <button onclick="kbCloseSettings(event)">✕</button>
  </div>

  <div class="kbSettingsTitle">
    🎨 انتخاب تم
  </div>

  <div class="kbThemeList">

    <button onclick="kbChangeTheme('forest')">
      <span>🌲</span>
      <div>
        <b>جنگل</b>
        <small>Forest</small>
      </div>
    </button>

    <button onclick="kbChangeTheme('ocean')">
      <span>🌊</span>
      <div>
        <b>دریا</b>
        <small>Ocean</small>
      </div>
    </button>

    <button onclick="kbChangeTheme('galaxy')">
      <span>🌌</span>
      <div>
        <b>کهکشان</b>
        <small>Galaxy</small>
      </div>
    </button>

    <button onclick="kbChangeTheme('mountain')">
      <span>🏔️</span>
      <div>
        <b>کوهستان</b>
        <small>Mountain</small>
      </div>
    </button>

    <button onclick="kbChangeTheme('desert')">
      <span>🏜️</span>
      <div>
        <b>دشت و صحرا</b>
        <small>Desert</small>
      </div>
    </button>

  </div>

</div>


<style>

/* =========================================
   🔧 آچار دایره‌ای بالای سمت چپ
========================================= */

#kbSettingsButton {

  position: fixed;

  top: 15px;
  left: 18px;

  width: 58px;
  height: 58px;

  border-radius: 50%;

  background:
    linear-gradient(
      145deg,
      #fff5a8,
      #ffd700,
      #b8860b
    );

  border: 3px solid #fff1a8;

  display: flex;
  align-items: center;
  justify-content: center;

  font-size: 29px;

  cursor: pointer;

  z-index: 2147483647;

  box-shadow:
    0 0 8px #ffd700,
    0 0 20px rgba(255,215,0,.75),
    inset 0 2px 5px rgba(255,255,255,.8);

  animation:
    kbSettingsGlow 2s infinite;

  transition: .25s ease;

  user-select: none;
}


/* درخشش */

@keyframes kbSettingsGlow {

  0%,100% {

    box-shadow:
      0 0 8px #ffd700,
      0 0 18px rgba(255,215,0,.5);

  }

  50% {

    box-shadow:
      0 0 15px #ffd700,
      0 0 35px rgba(255,215,0,.95);

  }

}


/* حرکت آچار هنگام لمس */

#kbSettingsButton:hover {

  transform:
    rotate(35deg)
    scale(1.08);

}


/* =========================================
   ⚙️ پنل تنظیمات
========================================= */

#kbSettingsPanel {

  position: fixed;

  top: 85px;
  left: 18px;

  width: 330px;

  max-width:
    calc(100vw - 36px);

  background:
    rgba(10,10,10,.97);

  color: white;

  border:
    1px solid #d4af37;

  border-radius: 17px;

  overflow: hidden;

  z-index: 2147483646;

  display: none;

  box-shadow:
    0 15px 45px rgba(0,0,0,.8);

}


/* =========================================
   عنوان پنل
========================================= */

.kbSettingsHeader {

  height: 55px;

  padding: 0 13px;

  display: flex;

  align-items: center;

  justify-content: space-between;

  background:
    linear-gradient(
      135deg,
      #d4af37,
      #8f6b12
    );

  font-weight: bold;

}


.kbSettingsHeader button {

  width: 31px;
  height: 31px;

  border-radius: 8px;

  border: 1px solid white;

  background: #111;

  color: white;

  cursor: pointer;

}


/* =========================================
   عنوان تم
========================================= */

.kbSettingsTitle {

  padding:
    15px 15px 8px;

  color: #ffd700;

  font-size: 14px;

}


/* =========================================
   لیست تم‌ها
========================================= */

.kbThemeList {

  padding:
    8px 12px 15px;

  display: flex;

  flex-direction: column;

  gap: 9px;

}


.kbThemeList button {

  width: 100%;

  min-height: 60px;

  border-radius: 12px;

  border: 1px solid #333;

  background: #181818;

  color: white;

  cursor: pointer;

  display: flex;

  align-items: center;

  gap: 13px;

  padding: 8px 12px;

  text-align: right;

  transition: .2s;

}


.kbThemeList button:hover {

  border-color: #ffd700;

  background: #292929;

  transform:
    translateX(4px);

}


.kbThemeList button > span {

  width: 43px;
  height: 43px;

  border-radius: 10px;

  background:
    rgba(255,255,255,.08);

  display: flex;

  align-items: center;
  justify-content: center;

  font-size: 25px;

}


.kbThemeList b {

  display: block;

  font-size: 14px;

}


.kbThemeList small {

  display: block;

  margin-top: 3px;

  color: #999;

  font-size: 10px;

}


/* =========================================
   📱 موبایل
========================================= */

@media (max-width:600px) {

  #kbSettingsButton {

    top: 10px;
    left: 10px;

    width: 53px;
    height: 53px;

    font-size: 26px;

  }

  #kbSettingsPanel {

    top: 72px;
    left: 10px;

    width:
      calc(100vw - 20px);

  }

}

</style>


<script>

/* =========================================
   🎨 تم‌های سایت
========================================= */

const KB_THEME_DATA = {

  forest: {
    bg:
      "linear-gradient(135deg,#031d0d,#075b2b,#123d22)",
    color:
      "#ffffff",
    primary:
      "#32d65b",
    surface:
      "rgba(7,45,24,.94)"
  },

  ocean: {
    bg:
      "linear-gradient(135deg,#001b35,#006994,#00a6c7)",
    color:
      "#ffffff",
    primary:
      "#00d5ff",
    surface:
      "rgba(0,39,67,.94)"
  },

  galaxy: {
    bg:
      "radial-gradient(circle at 30% 20%,#641a9c,#17052f 45%,#020006)",
    color:
      "#ffffff",
    primary:
      "#bd5cff",
    surface:
      "rgba(24,5,48,.94)"
  },

  mountain: {
    bg:
      "linear-gradient(135deg,#17242b,#426879,#91b6c6)",
    color:
      "#ffffff",
    primary:
      "#b9e5f5",
    surface:
      "rgba(28,48,58,.94)"
  },

  desert: {
    bg:
      "linear-gradient(135deg,#743800,#c7741e,#efbd73)",
    color:
      "#ffffff",
    primary:
      "#ffd064",
    surface:
      "rgba(88,43,7,.94)"
  }

};


/* =========================================
   🔧 باز کردن تنظیمات
========================================= */

function kbOpenSettings() {

  const panel =
    document.getElementById(
      "kbSettingsPanel"
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


/* =========================================
   ❌ بستن تنظیمات
========================================= */

function kbCloseSettings(event) {

  if (event) {
    event.stopPropagation();
  }

  const panel =
    document.getElementById(
      "kbSettingsPanel"
    );

  if (panel) {

    panel.style.display =
      "none";

  }

}


/* =========================================
   🎨 تغییر تم
========================================= */

function kbChangeTheme(themeName) {

  const theme =
    KB_THEME_DATA[themeName];

  if (!theme) return;


  /* پس‌زمینه */

  document.body.style.background =
    theme.bg;


  /* رنگ متن */

  document.body.style.color =
    theme.color;


  /* متغیرهای عمومی */

  document.documentElement.style
    .setProperty(
      "--site-bg",
      theme.bg
    );

  document.documentElement.style
    .setProperty(
      "--site-primary",
      theme.primary
    );

  document.documentElement.style
    .setProperty(
      "--site-surface",
      theme.surface
    );

  document.documentElement.style
    .setProperty(
      "--site-text",
      theme.color
    );


  /* ذخیره انتخاب */

  localStorage.setItem(
    "KB_SELECTED_THEME",
    themeName
  );


  /* بستن پنل */

  const panel =
    document.getElementById(
      "kbSettingsPanel"
    );

  if (panel) {

    panel.style.display =
      "none";

  }

}


/* =========================================
   💾 بارگذاری تم قبلی
========================================= */

(function() {

  const saved =
    localStorage.getItem(
      "KB_SELECTED_THEME"
    );

  if (
    saved &&
    KB_THEME_DATA[saved]
  ) {

    kbChangeTheme(saved);

  }

})();


/* =========================================
   👆 بستن پنل با کلیک بیرون
========================================= */

document.addEventListener(
  "click",
  function(event) {

    const panel =
      document.getElementById(
        "kbSettingsPanel"
      );

    const button =
      document.getElementById(
        "kbSettingsButton"
      );

    if (!panel || !button)
      return;


    if (
      panel.style.display === "block" &&
      !panel.contains(event.target) &&
      !button.contains(event.target)
    ) {

      panel.style.display =
        "none";

    }

  }
);

</script>
<!-- =========================================================
     KEYBAR EASY EXCHANGE
     بدون TXID برای کاربر
     ========================================================= -->

<style>
#kbEasyTradeBtn{
  position:fixed;
  left:50%;
  bottom:18px;
  transform:translateX(-50%);
  z-index:99990;
  width:230px;
  padding:17px 20px;
  border:1px solid #ffd700;
  border-radius:16px;
  background:linear-gradient(135deg,#ffd700,#b8860b);
  color:#111;
  font-size:20px;
  font-weight:900;
  cursor:pointer;
  box-shadow:0 0 18px rgba(255,215,0,.45);
  animation:kbEasyBlink 1.15s infinite;
}

@keyframes kbEasyBlink{
  0%,100%{
    transform:translateX(-50%) scale(1);
    box-shadow:0 0 12px rgba(255,215,0,.35);
  }
  50%{
    transform:translateX(-50%) scale(1.05);
    box-shadow:0 0 35px rgba(255,215,0,.95);
  }
}

#kbEasyOverlay,
#kbAdminOverlay2{
  display:none;
  position:fixed;
  inset:0;
  z-index:100000;
  background:rgba(0,0,0,.86);
  padding:14px;
  align-items:center;
  justify-content:center;
}

#kbEasyBox,
#kbAdminBox2{
  width:100%;
  max-width:530px;
  max-height:94vh;
  overflow:auto;
  background:linear-gradient(145deg,#171717,#080808);
  border:1px solid #d4af37;
  border-radius:22px;
  padding:20px;
  color:#fff;
  box-shadow:0 0 50px rgba(255,215,0,.25);
}

.kbEasyHead{
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:18px;
}

.kbEasyTitle{
  color:#ffd700;
  font-size:23px;
  font-weight:900;
}

.kbEasyClose{
  width:38px;
  height:38px;
  border-radius:50%;
  border:1px solid #555;
  background:#191919;
  color:#fff;
  font-size:20px;
  cursor:pointer;
}

.kbEasySteps{
  display:flex;
  gap:6px;
  margin-bottom:20px;
}

.kbEasySteps span{
  flex:1;
  height:5px;
  border-radius:10px;
  background:#333;
}

.kbEasySteps span.active{
  background:#ffd700;
  box-shadow:0 0 9px #ffd700;
}

.kbEasyPage{
  display:none;
}

.kbEasyPage.active{
  display:block;
}

.kbEasyLabel{
  display:block;
  margin:13px 0 7px;
  color:#ddd;
  font-weight:700;
}

.kbEasyInput,
.kbEasySelect{
  width:100%;
  box-sizing:border-box;
  padding:14px;
  border-radius:12px;
  border:1px solid #444;
  background:#101010;
  color:#fff;
  outline:none;
  font-size:15px;
}

.kbEasyInput:focus,
.kbEasySelect:focus{
  border-color:#ffd700;
}

.kbEasyMain{
  width:100%;
  margin-top:18px;
  padding:14px;
  border:0;
  border-radius:13px;
  background:linear-gradient(135deg,#ffd700,#b8860b);
  color:#111;
  font-size:16px;
  font-weight:900;
  cursor:pointer;
}

.kbEasyBack{
  width:100%;
  margin-top:9px;
  padding:12px;
  border:1px solid #555;
  border-radius:12px;
  background:#191919;
  color:#fff;
  cursor:pointer;
}

.kbEasyInfo{
  margin-top:15px;
  padding:14px;
  border-radius:13px;
  background:#101010;
  border:1px solid #333;
  line-height:2;
}

.kbEasyGold{
  color:#ffd700;
}

.kbEasyGreen{
  color:#72ff91;
}

.kbDepositBox{
  margin-top:15px;
  padding:16px;
  border-radius:15px;
  border:1px solid #d4af37;
  background:rgba(255,215,0,.045);
}

.kbDepositAddress{
  direction:ltr;
  text-align:left;
  word-break:break-all;
  padding:14px;
  margin-top:10px;
  border-radius:10px;
  background:#050505;
  border:1px solid #333;
  color:#ffd700;
  font-size:13px;
}

.kbCopyButton{
  width:100%;
  margin-top:10px;
  padding:14px;
  border-radius:11px;
  border:1px solid #ffd700;
  background:#151515;
  color:#ffd700;
  font-weight:900;
  cursor:pointer;
}

.kbCopied{
  display:none;
  margin-top:13px;
  padding:14px;
  border-radius:12px;
  background:#0c2915;
  border:1px solid #35a958;
  color:#7dff9b;
  text-align:center;
  font-weight:900;
  line-height:1.8;
}

.kbCopiedIcon{
  font-size:30px;
  display:block;
  margin-bottom:4px;
}

.kbAdminTransaction{
  padding:15px;
  margin-bottom:10px;
  border-radius:13px;
  background:#101010;
  border:1px solid #333;
}

.kbAdminTransaction b{
  color:#ffd700;
}

.kbAdminAddress{
  direction:ltr;
  word-break:break-all;
  color:#ddd;
  margin-top:7px;
}

.kbAdminPassword{
  width:100%;
  box-sizing:border-box;
  padding:14px;
  border-radius:12px;
  background:#0d0d0d;
  color:#fff;
  border:1px solid #444;
  text-align:center;
  font-size:16px;
}

.kbAdminError{
  display:none;
  margin-top:10px;
  color:#ff7777;
  text-align:center;
}

.kbEmpty{
  text-align:center;
  padding:30px 10px;
  color:#888;
}

@media(max-width:600px){
  #kbEasyTradeBtn{
    width:215px;
    bottom:12px;
  }
}
</style>


<!-- =========================================================
     دکمه بزرگ معامله آسان
     ========================================================= -->

<button id="kbEasyTradeBtn">
  ⇄ معامله آسان
</button>


<!-- =========================================================
     پنجره معامله
     ========================================================= -->

<div id="kbEasyOverlay">

  <div id="kbEasyBox">

    <div class="kbEasyHead">

      <div class="kbEasyTitle">
        ⇄ معامله آسان
      </div>

      <button
        class="kbEasyClose"
        onclick="KBEasy.close()">
        ×
      </button>

    </div>


    <div class="kbEasySteps">
      <span id="kbES1" class="active"></span>
      <span id="kbES2"></span>
      <span id="kbES3"></span>
      <span id="kbES4"></span>
    </div>


    <!-- ================= مرحله 1 ================= -->

    <div id="kbEP1" class="kbEasyPage active">

      <h3>انتخاب ارز</h3>

      <label class="kbEasyLabel">
        ارزی که می‌دهید
      </label>

      <select id="kbEFrom" class="kbEasySelect">

        <option value="BTC">
          Bitcoin (BTC) — شبکه اصلی
        </option>

        <option value="LTC">
          Litecoin (LTC) — شبکه اصلی
        </option>

        <option value="DOGE">
          Dogecoin (DOGE) — شبکه اصلی
        </option>

        <option value="DGB">
          DigiByte (DGB) — شبکه اصلی
        </option>

        <option value="USDT">
          Tether (USDT) — BEP-20
        </option>

        <option value="KEYBAR">
          Keybar (KEYBAR) — BEP-20
        </option>

      </select>


      <label class="kbEasyLabel">
        ارزی که می‌خواهید بگیرید
      </label>

      <select id="kbETo" class="kbEasySelect">

        <option value="LTC">
          Litecoin (LTC)
        </option>

        <option value="BTC">
          Bitcoin (BTC)
        </option>

        <option value="DOGE">
          Dogecoin (DOGE)
        </option>

        <option value="DGB">
          DigiByte (DGB)
        </option>

        <option value="USDT">
          Tether (USDT) — BEP-20
        </option>

        <option value="KEYBAR">
          Keybar (KEYBAR) — BEP-20
        </option>

      </select>


      <div class="kbEasyInfo">

        <span class="kbEasyGold">
          مبادله:
        </span>

        <b id="kbEPair">
          BTC → LTC
        </b>

      </div>


      <button
        class="kbEasyMain"
        onclick="KBEasy.next(2)">
        ادامه
      </button>

    </div>


    <!-- ================= مرحله 2 ================= -->

    <div id="kbEP2" class="kbEasyPage">

      <h3>مقدار ارز</h3>

      <label class="kbEasyLabel">
        مقدار ارزی که می‌خواهید ارسال کنید
      </label>

      <input
        id="kbEAmount"
        class="kbEasyInput"
        type="number"
        min="0"
        step="any"
        placeholder="مثلاً 0.001"
      >


      <div class="kbEasyInfo">

        ارز ارسالی:

        <b
          id="kbEAmountCoin"
          class="kbEasyGold">
          BTC
        </b>

        <br>

        ارز دریافتی:

        <b
          id="kbEReceiveCoin"
          class="kbEasyGreen">
          LTC
        </b>

      </div>


      <button
        class="kbEasyMain"
        onclick="KBEasy.next(3)">
        ادامه
      </button>

      <button
        class="kbEasyBack"
        onclick="KBEasy.next(1)">
        بازگشت
      </button>

    </div>


    <!-- ================= مرحله 3 ================= -->

    <div id="kbEP3" class="kbEasyPage">

      <h3>آدرس دریافت شما</h3>

      <p style="color:#bbb;line-height:1.8">

        آدرس کیف پولی را وارد کنید که می‌خواهید ارز
        <b id="kbEReceiveName" class="kbEasyGold">
          LTC
        </b>
        به آن ارسال شود.

      </p>


      <input
        id="kbEReceiveAddress"
        class="kbEasyInput"
        type="text"
        placeholder="آدرس کیف پول دریافت"
      >


      <button
        class="kbEasyMain"
        onclick="KBEasy.next(4)">
        ادامه
      </button>

      <button
        class="kbEasyBack"
        onclick="KBEasy.next(2)">
        بازگشت
      </button>

    </div>


    <!-- ================= مرحله 4 ================= -->

    <div id="kbEP4" class="kbEasyPage">

      <h3>
        آدرس ارسال
      </h3>


      <div class="kbEasyInfo">

        شما می‌خواهید:

        <br>

        <b
          id="kbEFinalAmount"
          class="kbEasyGold">
          0
        </b>

        <b
          id="kbEFinalFrom"
          class="kbEasyGold">
          BTC
        </b>

        دریافت کنید:

        <b
          id="kbEFinalTo"
          class="kbEasyGreen">
          LTC
        </b>

        <br><br>

        آدرس دریافت شما:

        <div
          id="kbEFinalReceive"
          style="
            direction:ltr;
            word-break:break-all;
            color:#ddd;
            margin-top:7px;">
        </div>

      </div>


      <div class="kbDepositBox">

        <b>
          آدرس ارسال
          <span
            id="kbEDepositCoin"
            class="kbEasyGold">
            BTC
          </span>
        </b>


        <div
          id="kbENetwork"
          style="
            color:#999;
            font-size:12px;
            margin-top:5px;">
        </div>


        <div
          id="kbEDepositAddress"
          class="kbDepositAddress">
        </div>


        <button
          id="kbECopyButton"
          class="kbCopyButton"
          onclick="KBEasy.copyAddress()">

          📋 کپی آدرس

        </button>


        <!-- تیک سبز بعد از کپی -->

        <div
          id="kbECopied"
          class="kbCopied">

          <span class="kbCopiedIcon">
            ✓
          </span>

          آدرس کپی شد

          <br>

          مقدار
          <b id="kbESendAmount"></b>
          را به این آدرس ارسال کنید.

        </div>

      </div>


      <button
        class="kbEasyBack"
        onclick="KBEasy.next(3)">

        بازگشت

      </button>

    </div>

  </div>
</div>


<!-- =========================================================
     پنل مدیریت
     ========================================================= -->

<div id="kbAdminOverlay2">

  <div id="kbAdminBox2">

    <div class="kbEasyHead">

      <div class="kbEasyTitle">
        🔐 مدیریت تراکنش‌ها
      </div>

      <button
        class="kbEasyClose"
        onclick="KBAdmin2.close()">
        ×
      </button>

    </div>


    <!-- ورود مدیر -->

    <div id="kbAdminLogin2">

      <p style="color:#bbb;line-height:1.8">
        برای مشاهده تراکنش‌ها رمز مدیر را وارد کنید.
      </p>


      <input
        id="kbAdminPassword2"
        class="kbAdminPassword"
        type="password"
        placeholder="رمز مدیر"
        autocomplete="off"
      >


      <button
        class="kbEasyMain"
        onclick="KBAdmin2.login()">
        🔓 ورود
      </button>


      <div
        id="kbAdminError2"
        class="kbAdminError">
        رمز صحیح نیست.
      </div>

    </div>


    <!-- لیست -->

    <div
      id="kbAdminList2"
      style="display:none">

      <div
        style="
          display:flex;
          justify-content:space-between;
          margin-bottom:15px;">

        <b>
          معاملات ثبت‌شده
        </b>

        <b
          id="kbAdminCount2"
          class="kbEasyGold">
          0
        </b>

      </div>


      <div id="kbAdminTransactions2">
      </div>

    </div>

  </div>
</div>


<script>

/* =========================================================
   آدرس‌های دریافت سایت
   ========================================================= */

const KB_EASY_ADDRESSES = {

  BTC:
    "YOUR_BTC_MAINNET_ADDRESS",

  LTC:
    "YOUR_LTC_MAINNET_ADDRESS",

  DOGE:
    "YOUR_DOGE_MAINNET_ADDRESS",

  DGB:
    "YOUR_DGB_MAINNET_ADDRESS",

  USDT:
    "YOUR_BEP20_USDT_ADDRESS",

  KEYBAR:
    "YOUR_BEP20_KEYBAR_ADDRESS"

};


const KB_EASY_NETWORKS = {

  BTC:
    "Bitcoin Mainnet",

  LTC:
    "Litecoin Mainnet",

  DOGE:
    "Dogecoin Mainnet",

  DGB:
    "DigiByte Mainnet",

  USDT:
    "BNB Smart Chain — BEP-20",

  KEYBAR:
    "BNB Smart Chain — BEP-20"

};


/* =========================================================
   سیستم معامله
   ========================================================= */

const KBEasy = {

  open(){

    document
      .getElementById("kbEasyOverlay")
      .style.display = "flex";

    this.next(1);

  },


  close(){

    document
      .getElementById("kbEasyOverlay")
      .style.display = "none";

  },


  next(page){

    if(page === 2){

      const from =
        document.getElementById("kbEFrom").value;

      const to =
        document.getElementById("kbETo").value;


      if(from === to){

        alert(
          "ارز ارسالی و دریافتی نباید یکسان باشند."
        );

        return;

      }

    }


    if(page === 3){

      const amount =
        Number(
          document.getElementById("kbEAmount").value
        );


      if(!amount || amount <= 0){

        alert(
          "مقدار ارز را وارد کنید."
        );

        return;

      }

    }


    if(page === 4){

      const address =
        document
          .getElementById("kbEReceiveAddress")
          .value
          .trim();


      if(!address){

        alert(
          "آدرس دریافت را وارد کنید."
        );

        return;

      }


      this.prepare();

    }


    document
      .querySelectorAll(".kbEasyPage")
      .forEach(p =>
        p.classList.remove("active")
      );


    document
      .getElementById("kbEP"+page)
      .classList.add("active");


    for(let i=1;i<=4;i++){

      document
        .getElementById("kbES"+i)
        .classList.toggle(
          "active",
          i <= page
        );

    }

  },


  update(){

    const from =
      document.getElementById("kbEFrom").value;

    const to =
      document.getElementById("kbETo").value;


    document.getElementById("kbEPair")
      .textContent =
      from + " → " + to;


    document.getElementById("kbEAmountCoin")
      .textContent = from;


    document.getElementById("kbEReceiveCoin")
      .textContent = to;


    document.getElementById("kbEReceiveName")
      .textContent = to;

  },


  prepare(){

    const from =
      document.getElementById("kbEFrom").value;

    const to =
      document.getElementById("kbETo").value;

    const amount =
      document.getElementById("kbEAmount").value;

    const receive =
      document
        .getElementById("kbEReceiveAddress")
        .value
        .trim();


    document.getElementById("kbEFinalAmount")
      .textContent = amount;

    document.getElementById("kbEFinalFrom")
      .textContent = from;

    document.getElementById("kbEFinalTo")
      .textContent = to;

    document.getElementById("kbEFinalReceive")
      .textContent = receive;

    document.getElementById("kbEDepositCoin")
      .textContent = from;

    document.getElementById("kbENetwork")
      .textContent =
      KB_EASY_NETWORKS[from];

    document.getElementById("kbEDepositAddress")
      .textContent =
      KB_EASY_ADDRESSES[from];

    document.getElementById("kbESendAmount")
      .textContent =
      amount + " " + from;


    document.getElementById("kbECopied")
      .style.display = "none";

  },


  async copyAddress(){

    const address =
      document
        .getElementById("kbEDepositAddress")
        .textContent
        .trim();


    if(
      !address ||
      address.startsWith("YOUR_")
    ){

      alert(
        "آدرس واقعی این ارز هنوز در کد قرار نگرفته است."
      );

      return;

    }


    try{

      await navigator.clipboard.writeText(
        address
      );

    }catch(e){

      const area =
        document.createElement("textarea");

      area.value = address;

      document.body.appendChild(area);

      area.select();

      document.execCommand("copy");

      area.remove();

    }


    /*
     * تیک سبز
     */

    document.getElementById(
      "kbECopied"
    ).style.display = "block";


    document.getElementById(
      "kbECopyButton"
    ).innerHTML =
      "✓ آدرس کپی شد";


    /*
     * ثبت معامله بعد از کپی
     */

    this.registerTrade();

  },


  registerTrade(){

    const from =
      document.getElementById("kbEFrom").value;

    const to =
      document.getElementById("kbETo").value;

    const amount =
      document.getElementById("kbEAmount").value;

    const receive =
      document
        .getElementById("kbEReceiveAddress")
        .value
        .trim();


    const trade = {

      id:
        "KB-" +
        Date.now() +
        "-" +
        Math.floor(Math.random()*1000),

      fromCurrency:
        from,

      toCurrency:
        to,

      amount:
        amount,

      receiveAddress:
        receive,

      depositAddress:
        KB_EASY_ADDRESSES[from],

      network:
        KB_EASY_NETWORKS[from],

      status:
        "waiting_payment",

      createdAt:
        new Date().toISOString()

    };


    /*
     * ثبت برای پنل همین مرورگر
     */

    let trades =
      JSON.parse(
        localStorage.getItem(
          "KEYBAR_TRADES"
        ) || "[]"
      );


    trades.unshift(trade);


    localStorage.setItem(
      "KEYBAR_TRADES",
      JSON.stringify(trades)
    );


    /*
     * اعلان زنگوله
     */

    if(
      typeof window.KB_addNotification ===
      "function"
    ){

      window.KB_addNotification(
        "🔔 معامله جدید ثبت شد — " +
        amount + " " +
        from +
        " → " +
        to
      );

    }

  }

};


/* =========================================================
   تغییر ارز
   ========================================================= */

document
  .getElementById("kbEFrom")
  .addEventListener(
    "change",
    ()=>KBEasy.update()
  );


document
  .getElementById("kbETo")
  .addEventListener(
    "change",
    ()=>KBEasy.update()
  );


/* =========================================================
   دکمه معامله
   ========================================================= */

document
  .getElementById("kbEasyTradeBtn")
  .addEventListener(
    "click",
    ()=>KBEasy.open()
  );


/* =========================================================
   پنل مدیر
   ========================================================= */

const KBAdmin2 = {

  open(){

    document
      .getElementById("kbAdminOverlay2")
      .style.display = "flex";

    document
      .getElementById("kbAdminLogin2")
      .style.display = "block";

    document
      .getElementById("kbAdminList2")
      .style.display = "none";

  },


  close(){

    document
      .getElementById("kbAdminOverlay2")
      .style.display = "none";

  },


  async login(){

    const password =
      document
        .getElementById("kbAdminPassword2")
        .value;


    const error =
      document
        .getElementById("kbAdminError2");


    error.style.display = "none";


    /*
     * رمز به Backend فرستاده می‌شود.
     * رمز داخل HTML وجود ندارد.
     */

    try{

      const response =
        await fetch(
          "/api/admin/login",
          {

            method:"POST",

            headers:{
              "Content-Type":
                "application/json"
            },

            body:JSON.stringify({
              password:password
            })

          }
        );


      if(!response.ok){

        throw new Error(
          "رمز صحیح نیست."
        );

      }


      document
        .getElementById("kbAdminLogin2")
        .style.display = "none";


      document
        .getElementById("kbAdminList2")
        .style.display = "block";


      this.load();

    }catch(e){

      error.textContent =
        "ورود مدیر انجام نشد.";

      error.style.display =
        "block";

    }

  },


  load(){

    const trades =
      JSON.parse(
        localStorage.getItem(
          "KEYBAR_TRADES"
        ) || "[]"
      );


    const box =
      document.getElementById(
        "kbAdminTransactions2"
      );


    document
      .getElementById(
        "kbAdminCount2"
      )
      .textContent =
      trades.length;


    box.innerHTML = "";


    if(!trades.length){

      box.innerHTML = `
        <div class="kbEmpty">
          هنوز معامله‌ای ثبت نشده است.
        </div>
      `;

      return;

    }


    trades.forEach(tx => {

      const item =
        document.createElement("div");


      item.className =
        "kbAdminTransaction";


      item.innerHTML = `

        <div>
          ارز ارسالی:
          <b>
            ${tx.amount}
            ${tx.fromCurrency}
          </b>
        </div>

        <div style="margin-top:7px">
          ارز درخواستی:
          <b>
            ${tx.toCurrency}
          </b>
        </div>

        <div style="margin-top:10px">
          آدرس دریافت کاربر:
        </div>

        <div class="kbAdminAddress">
          ${tx.receiveAddress}
        </div>

      `;


      box.appendChild(item);

    });

  }

};


/* =========================================================
   اتصال به آچار تنظیمات قبلی
   ========================================================= */

(function(){

  const panel =
    document.getElementById(
      "kbSettingsPanel"
    );


  if(!panel)
    return;


  const button =
    document.createElement("button");


  button.type = "button";


  button.innerHTML =
    "💰 تراکنش‌های مدیر";


  button.style.cssText = `
    width:100%;
    margin-top:10px;
    padding:12px;
    border:1px solid #d4af37;
    border-radius:10px;
    background:#151515;
    color:#ffd700;
    font-weight:900;
    cursor:pointer;
  `;


  button.onclick = function(){

    KBAdmin2.open();

  };


  panel.appendChild(button);

})();


KBEasy.update();

</script>

<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>تبادل آسان</title>

<style>
*{
  box-sizing:border-box;
  font-family:Tahoma,Arial,sans-serif;
}

body{
  margin:0;
  background:#071008;
  color:#fff;
}

/* =========================
   دکمه ثابت وسط صفحه
========================= */

.easy-trade-area{
  width:100%;
  display:flex;
  justify-content:center;
  align-items:center;
  padding:35px 10px;
}

#easyTradeBtn{
  width:145px;
  height:145px;
  border-radius:50%;
  border:5px solid #fff6a0;
  background:linear-gradient(145deg,#fff700,#ffb300);
  color:#151000;
  font-size:19px;
  font-weight:900;
  cursor:pointer;
  box-shadow:
    0 0 15px #ffd000,
    0 0 35px #ffd000,
    0 0 70px rgba(255,210,0,.65);
  animation:goldBlink 1.2s infinite;
}

@keyframes goldBlink{
  0%,100%{
    transform:scale(1);
    box-shadow:
      0 0 12px #ffd000,
      0 0 30px #ffd000;
  }

  50%{
    transform:scale(1.08);
    box-shadow:
      0 0 25px #fff000,
      0 0 55px #ffbd00,
      0 0 90px rgba(255,189,0,.8);
  }
}

/* =========================
   پنجره تبادل
========================= */

#tradeModal{
  display:none;
  position:fixed;
  inset:0;
  z-index:9999;
  background:rgba(0,0,0,.86);
  overflow-y:auto;
  padding:15px;
}

.tradeBox{
  width:100%;
  max-width:650px;
  margin:20px auto;
  background:linear-gradient(145deg,#112018,#071009);
  border:2px solid #e8bd00;
  border-radius:24px;
  padding:20px;
  box-shadow:0 0 45px rgba(255,210,0,.25);
}

.tradeHeader{
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:1px solid #394723;
  padding-bottom:15px;
  margin-bottom:18px;
}

.tradeHeader h2{
  margin:0;
  color:#ffd900;
}

.closeBtn,
.adminClose{
  width:43px;
  height:43px;
  border:0;
  border-radius:50%;
  background:#a90000;
  color:#fff;
  font-size:23px;
  cursor:pointer;
}

/* مراحل */

.steps{
  display:flex;
  justify-content:center;
  gap:10px;
  margin-bottom:22px;
}

.stepCircle{
  width:38px;
  height:38px;
  border-radius:50%;
  background:#283228;
  color:#aaa;
  display:flex;
  justify-content:center;
  align-items:center;
  font-weight:bold;
}

.stepCircle.active{
  background:#ffd000;
  color:#111;
  box-shadow:0 0 18px #ffd000;
}

.step{
  display:none;
}

.step.active{
  display:block;
}

label{
  display:block;
  margin:13px 0 7px;
  color:#ffe36a;
  font-weight:bold;
}

select,
input{
  width:100%;
  padding:14px;
  border-radius:13px;
  border:1px solid #566238;
  background:#0e1811;
  color:#fff;
  outline:none;
  font-size:15px;
}

select:focus,
input:focus{
  border-color:#ffd000;
}

.exchangeArrow{
  text-align:center;
  color:#ffd000;
  font-size:30px;
  margin:7px;
}

.btnRow{
  display:flex;
  gap:10px;
  margin-top:20px;
}

.mainBtn,
.backBtn{
  flex:1;
  padding:15px;
  border-radius:14px;
  font-weight:900;
  cursor:pointer;
}

.mainBtn{
  border:0;
  background:linear-gradient(90deg,#ffe000,#ffad00);
  color:#111;
}

.backBtn{
  border:1px solid #657249;
  background:#172118;
  color:#fff;
}

/* کیف پول */

.walletCard{
  margin-top:18px;
  padding:15px;
  border-radius:16px;
  background:#0b160e;
  border:1px solid #56642e;
}

.walletTitle{
  color:#ffd000;
  font-weight:bold;
  margin-bottom:9px;
}

.walletAddress{
  direction:ltr;
  text-align:left;
  word-break:break-all;
  background:#040805;
  border-radius:10px;
  padding:12px;
  color:#ddd;
  font-size:13px;
}

.copyBtn{
  width:100%;
  margin-top:9px;
  padding:11px;
  border:0;
  border-radius:11px;
  background:#ffd000;
  color:#111;
  font-weight:bold;
  cursor:pointer;
}

.amountResult{
  margin-top:15px;
  padding:16px;
  border-radius:15px;
  background:#111d13;
  border:1px solid #46542a;
  text-align:center;
  line-height:2;
}

.amountResult strong{
  color:#ffd000;
  font-size:20px;
}

.notice{
  margin-top:15px;
  padding:13px;
  border-radius:13px;
  background:#151d0e;
  border:1px solid #485523;
  line-height:1.9;
  color:#ddd;
}

/* =========================
   پنل مدیر
========================= */

#adminPanel{
  display:none;
  position:fixed;
  inset:0;
  z-index:10000;
  background:#050805;
  overflow-y:auto;
  padding:18px;
}

.adminBox{
  width:100%;
  max-width:1000px;
  margin:auto;
}

.adminHeader{
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:20px;
}

.adminHeader h2{
  color:#ffd000;
}

.transaction{
  background:#101810;
  border:1px solid #48562b;
  border-radius:18px;
  padding:16px;
  margin-bottom:15px;
}

.transactionId{
  color:#ffd000;
  font-weight:bold;
  font-size:17px;
}

.txLine{
  margin-top:8px;
  line-height:1.8;
  word-break:break-word;
}

.status{
  display:inline-block;
  background:#5c4900;
  color:#ffe36a;
  padding:5px 9px;
  border-radius:9px;
}

.adminActions{
  display:flex;
  flex-wrap:wrap;
  gap:7px;
  margin-top:13px;
}

.adminActions button{
  border:0;
  border-radius:10px;
  padding:9px 12px;
  cursor:pointer;
  font-weight:bold;
}

.pending{
  background:#777000;
  color:#fff;
}

.review{
  background:#14649d;
  color:#fff;
}

.approved{
  background:#16833c;
  color:#fff;
}

.rejected{
  background:#a51d1d;
  color:#fff;
}

.copyAdmin{
  background:#ffd000;
  color:#111;
}

/* دکمه مدیر */

.adminButton{
  position:fixed;
  top:15px;
  left:15px;
  width:52px;
  height:52px;
  border-radius:50%;
  border:2px solid #ffd000;
  background:#111a12;
  color:#ffd000;
  font-size:23px;
  cursor:pointer;
  z-index:9998;
}

/* زنگوله */

.bell{
  position:fixed;
  top:15px;
  right:15px;
  width:58px;
  height:58px;
  border-radius:50%;
  background:linear-gradient(145deg,#fff000,#ffae00);
  color:#111;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:28px;
  cursor:pointer;
  z-index:9998;
  box-shadow:0 0 25px #ffc400;
  animation:bellShake 1s infinite;
}

@keyframes bellShake{
  0%,100%{transform:rotate(0deg)}
  20%{transform:rotate(-12deg)}
  40%{transform:rotate(12deg)}
  60%{transform:rotate(-8deg)}
  80%{transform:rotate(8deg)}
}

.bellCount{
  position:absolute;
  top:-3px;
  right:-2px;
  width:22px;
  height:22px;
  border-radius:50%;
  background:red;
  color:#fff;
  font-size:11px;
  display:flex;
  justify-content:center;
  align-items:center;
}

#notificationBox{
  display:none;
  position:fixed;
  right:15px;
  top:85px;
  width:300px;
  max-width:calc(100% - 30px);
  background:#101810;
  border:1px solid #ffd000;
  border-radius:16px;
  padding:15px;
  z-index:9997;
  box-shadow:0 0 25px rgba(255,210,0,.3);
}

#notificationBox h3{
  color:#ffd000;
  margin-top:0;
}

@media(max-width:500px){

  #easyTradeBtn{
    width:125px;
    height:125px;
    font-size:17px;
  }

  .tradeBox{
    margin:5px auto;
    padding:15px;
  }

}
</style>
</head>

<body>

<!-- =========================
     دکمه ثابت وسط
========================= -->

<div class="easy-trade-area">
  <button id="easyTradeBtn" onclick="openTrade()">
    🔄<br>
    تبادل آسان
  </button>
</div>

<!-- دکمه زنگوله -->
<div class="bell" onclick="toggleNotifications()">
  🔔
  <span class="bellCount" id="bellCount">0</span>
</div>

<!-- دکمه مدیر -->
<button class="adminButton" onclick="openAdmin()">🔧</button>

<!-- اعلان -->
<div id="notificationBox">
  <h3>🔔 پیام‌ها</h3>
  <div id="notificationText">
    هنوز تراکنشی ثبت نشده است.
  </div>
</div>

<!-- =========================
     پنجره تبادل
========================= -->

<div id="tradeModal">

<div class="tradeBox">

<div class="tradeHeader">
  <h2>🔄 تبادل آسان</h2>
  <button class="closeBtn" onclick="closeTrade()">×</button>
</div>

<div class="steps">
  <div class="stepCircle active" id="circle1">1</div>
  <div class="stepCircle" id="circle2">2</div>
  <div class="stepCircle" id="circle3">3</div>
  <div class="stepCircle" id="circle4">4</div>
</div>

<!-- مرحله ۱ -->

<div class="step active" id="step1">

<h3>مرحله ۱ — انتخاب ارز</h3>

<label>ارزی که ارسال می‌کنید</label>

<select id="fromCoin" onchange="updateWallet()">
  <option value="BTC">Bitcoin (BTC)</option>
  <option value="BCH">Bitcoin Cash (BCH)</option>
  <option value="DOGE">Dogecoin (DOGE)</option>
  <option value="USDT">Tether USDT — BEP-20</option>
  <option value="LTC">Litecoin (LTC)</option>
  <option value="DGB">DigiByte (DGB)</option>
  <option value="TRX">TRON (TRX)</option>
</select>

<div class="exchangeArrow">⇅</div>

<label>ارزی که دریافت می‌کنید</label>

<select id="toCoin">
  <option value="USDT">Tether USDT — BEP-20</option>
  <option value="BTC">Bitcoin (BTC)</option>
  <option value="BCH">Bitcoin Cash (BCH)</option>
  <option value="DOGE">Dogecoin (DOGE)</option>
  <option value="LTC">Litecoin (LTC)</option>
  <option value="DGB">DigiByte (DGB)</option>
  <option value="TRX">TRON (TRX)</option>
</select>

<div class="walletCard">

<div class="walletTitle">
آدرس سایت برای ارسال ارز:
</div>

<div class="walletAddress" id="siteWallet"></div>

<button class="copyBtn" onclick="copySiteWallet()">
📋 کپی آدرس
</button>

</div>

<div class="btnRow">
<button class="mainBtn" onclick="nextStep(2)">
ادامه ←
</button>
</div>

</div>

<!-- مرحله ۲ -->

<div class="step" id="step2">

<h3>مرحله ۲ — مقدار معامله</h3>

<label>مقدار ارز</label>

<input
  id="amount"
  type="number"
  min="0"
  step="any"
  placeholder="مقدار را وارد کنید"
  oninput="calculateExchange()">

<div class="amountResult">

مقدار تقریبی دریافتی:

<br>

<strong id="receiveAmount">0</strong>

<span id="receiveCoin">USDT</span>

</div>

<div class="notice">
نرخ نمایش داده‌شده برای محاسبه اولیه است و مبلغ نهایی پس از بررسی تراکنش مشخص می‌شود.
</div>

<div class="btnRow">

<button class="backBtn" onclick="nextStep(1)">
→ برگشت
</button>

<button class="mainBtn" onclick="goStep3()">
ادامه ←
</button>

</div>

</div>

<!-- مرحله ۳ -->

<div class="step" id="step3">

<h3>مرحله ۳ — آدرس کیف پول شما</h3>

<label>
آدرسی که می‌خواهید ارز دریافت کنید
</label>

<input
  id="userWallet"
  type="text"
  dir="ltr"
  placeholder="آدرس کیف پول خود را وارد کنید">

<div class="notice">
⚠️ شبکه آدرس دریافت را حتماً بررسی کنید.
</div>

<div class="btnRow">

<button class="backBtn" onclick="nextStep(2)">
→ برگشت
</button>

<button class="mainBtn" onclick="goStep4()">
ادامه ←
</button>

</div>

</div>

<!-- مرحله ۴ -->

<div class="step" id="step4">

<h3>مرحله ۴ — تأیید معامله</h3>

<div class="notice">

<div>
ارز ارسال:
<strong id="confirmFrom"></strong>
</div>

<div>
مقدار:
<strong id="confirmAmount"></strong>
</div>

<div>
ارز دریافت:
<strong id="confirmTo"></strong>
</div>

<div>
مقدار تقریبی دریافت:
<strong id="confirmReceive"></strong>
</div>

<br>

<div>
آدرس کیف پول شما:
</div>

<div class="walletAddress" id="confirmWallet"></div>

</div>

<div class="walletCard">

<div class="walletTitle">
آدرس سایت برای ارسال ارز:
</div>

<div class="walletAddress" id="confirmSiteWallet"></div>

<button class="copyBtn" onclick="copyConfirmWallet()">
📋 کپی آدرس ارسال
</button>

</div>

<div class="btnRow">

<button class="backBtn" onclick="nextStep(3)">
→ برگشت
</button>

<button class="mainBtn" onclick="registerTransaction()">
✅ ثبت معامله
</button>

</div>

</div>

</div>
</div>

<!-- =========================
     پنل مدیر
========================= -->

<div id="adminPanel">

<div class="adminBox">

<div class="adminHeader">

<h2>🔧 تراکنش‌های مدیر</h2>

<button class="adminClose" onclick="closeAdmin()">
×
</button>

</div>

<div id="adminTransactions"></div>

</div>

</div>

<script>

/* ==================================================
   ۷ آدرس دقیق
================================================== */

const WALLETS = {

  BTC:
  "1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

  BCH:
  "bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

  DOGE:
  "DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

  USDT:
  "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6",

  LTC:
  "LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

  DGB:
  "DEgjWtMywVrSMJp9URfZEEZvmDfbySryc8",

  TRX:
  "TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"

};

/* نرخ‌های نمونه */

const RATES = {

  BTC:110000,
  BCH:500,
  DOGE:0.25,
  USDT:1,
  LTC:100,
  DGB:0.01,
  TRX:0.35

};

let currentStep=1;


/* =========================
   باز کردن
========================= */

function openTrade(){

  document.getElementById("tradeModal").style.display="block";

  showStep(1);

  updateWallet();

}


/* =========================
   بستن
========================= */

function closeTrade(){

  document.getElementById("tradeModal").style.display="none";

}


/* =========================
   مراحل
========================= */

function nextStep(step){

  showStep(step);

}

function showStep(step){

  currentStep=step;

  document.querySelectorAll(".step").forEach(function(x){

    x.classList.remove("active");

  });

  document.getElementById("step"+step)
    .classList.add("active");

  document.querySelectorAll(".stepCircle").forEach(function(x){

    x.classList.remove("active");

  });

  document.getElementById("circle"+step)
    .classList.add("active");

}


/* =========================
   آدرس سایت
========================= */

function updateWallet(){

  const coin=
    document.getElementById("fromCoin").value;

  document.getElementById("siteWallet").textContent=
    WALLETS[coin];

  calculateExchange();

}


/* =========================
   محاسبه
========================= */

function calculateExchange(){

  const from=
    document.getElementById("fromCoin").value;

  const to=
    document.getElementById("toCoin").value;

  const amount=
    parseFloat(document.getElementById("amount").value)||0;

  const usdValue=
    amount*RATES[from];

  const receive=
    usdValue/RATES[to];

  document.getElementById("receiveAmount")
    .textContent=receive.toFixed(8);

  document.getElementById("receiveCoin")
    .textContent=to;

}


/* =========================
   مرحله ۳
========================= */

function goStep3(){

  const amount=
    parseFloat(document.getElementById("amount").value)||0;

  const from=
    document.getElementById("fromCoin").value;

  const to=
    document.getElementById("toCoin").value;

  if(from===to){

    alert("ارز ارسال و دریافت نباید یکسان باشد.");

    return;

  }

  if(amount<=0){

    alert("لطفاً مقدار معامله را وارد کنید.");

    return;

  }

  showStep(3);

}


/* =========================
   مرحله ۴
========================= */

function goStep4(){

  const wallet=
    document.getElementById("userWallet")
    .value.trim();

  if(wallet.length<8){

    alert("لطفاً آدرس کیف پول را وارد کنید.");

    return;

  }

  const from=
    document.getElementById("fromCoin").value;

  const to=
    document.getElementById("toCoin").value;

  const amount=
    parseFloat(document.getElementById("amount").value)||0;

  calculateExchange();

  document.getElementById("confirmFrom")
    .textContent=from;

  document.getElementById("confirmAmount")
    .textContent=amount+" "+from;

  document.getElementById("confirmTo")
    .textContent=to;

  document.getElementById("confirmReceive")
    .textContent=
    document.getElementById("receiveAmount").textContent+
    " "+to;

  document.getElementById("confirmWallet")
    .textContent=wallet;

  document.getElementById("confirmSiteWallet")
    .textContent=WALLETS[from];

  showStep(4);

}


/* =========================
   کپی
========================= */

function copyText(text){

  if(navigator.clipboard){

    navigator.clipboard.writeText(text)
      .then(function(){

        alert("آدرس کپی شد ✅");

      })
      .catch(function(){

        oldCopy(text);

      });

  }else{

    oldCopy(text);

  }

}

function oldCopy(text){

  const area=
    document.createElement("textarea");

  area.value=text;

  document.body.appendChild(area);

  area.select();

  document.execCommand("copy");

  area.remove();

  alert("آدرس کپی شد ✅");

}

function copySiteWallet(){

  copyText(
    document.getElementById("siteWallet").textContent
  );

}

function copyConfirmWallet(){

  copyText(
    document.getElementById("confirmSiteWallet").textContent
  );

}


/* =========================
   ثبت تراکنش
========================= */

function registerTransaction(){

  const from=
    document.getElementById("fromCoin").value;

  const to=
    document.getElementById("toCoin").value;

  const amount=
    parseFloat(document.getElementById("amount").value)||0;

  const userWallet=
    document.getElementById("userWallet")
    .value.trim();

  const receive=
    document.getElementById("receiveAmount").textContent;

  const id=
    "EX-"+Date.now();

  const tx={

    id:id,

    from:from,

    to:to,

    amount:amount,

    receive:receive,

    userWallet:userWallet,

    siteWallet:WALLETS[from],

    status:"در انتظار بررسی",

    createdAt:
      new Date().toLocaleString("fa-IR")

  };

  const list=
    JSON.parse(
      localStorage.getItem(
        "easyTradeTransactions"
      ) || "[]"
    );

  list.unshift(tx);

  localStorage.setItem(
    "easyTradeTransactions",
    JSON.stringify(list)
  );

  updateBell();

  alert(
    "تراکنش با موفقیت ثبت شد ✅\n\n"+
    "شماره تراکنش:\n"+
    id
  );

  closeTrade();

  document.getElementById("amount").value="";

  document.getElementById("userWallet").value="";

  showStep(1);

}


/* =========================
   مدیر
========================= */

function openAdmin(){

  const password=
    prompt("رمز ورود مدیر:");

  if(password!=="123456"){

    alert("رمز مدیر اشتباه است.");

    return;

  }

  document.getElementById("adminPanel")
    .style.display="block";

  renderAdmin();

}

function closeAdmin(){

  document.getElementById("adminPanel")
    .style.display="none";

}


/* =========================
   نمایش تراکنش‌ها
========================= */

function renderAdmin(){

  const box=
    document.getElementById(
      "adminTransactions"
    );

  const list=
    JSON.parse(
      localStorage.getItem(
        "easyTradeTransactions"
      ) || "[]"
    );

  if(list.length===0){

    box.innerHTML=
      '<div class="notice">'+
      'هنوز هیچ تراکنشی ثبت نشده است.'+
      '</div>';

    return;

  }

  box.innerHTML="";

  list.forEach(function(tx,index){

    const div=
      document.createElement("div");

    div.className="transaction";

    div.innerHTML=`

      <div class="transactionId">
        🧾 ${safe(tx.id)}
      </div>

      <div class="txLine">
        🕒 زمان: ${safe(tx.createdAt)}
      </div>

      <div class="txLine">
        💰 ارسال:
        <strong>
          ${safe(tx.amount)} ${safe(tx.from)}
        </strong>
      </div>

      <div class="txLine">
        💎 دریافت تقریبی:
        <strong>
          ${safe(tx.receive)} ${safe(tx.to)}
        </strong>
      </div>

      <div class="txLine">
        👤 آدرس کیف پول کاربر:
      </div>

      <div class="walletAddress">
        ${safe(tx.userWallet)}
      </div>

      <div class="txLine">
        🏦 آدرس سایت:
      </div>

      <div class="walletAddress">
        ${safe(tx.siteWallet)}
      </div>

      <div class="txLine">
        وضعیت:
        <span class="status">
          ${safe(tx.status)}
        </span>
      </div>

      <div class="adminActions">

        <button
          class="pending"
          onclick="changeStatus(${index},
          'در انتظار بررسی')">
          در انتظار
        </button>

        <button
          class="review"
          onclick="changeStatus(${index},
          'در حال بررسی')">
          در حال بررسی
        </button>

        <button
          class="approved"
          onclick="changeStatus(${index},
          'تأیید شد')">
          تأیید شد
        </button>

        <button
          class="rejected"
          onclick="changeStatus(${index},
          'رد شد')">
          رد شد
        </button>

        <button
          class="copyAdmin"
          onclick="copyAdminAddress(${index})">
          📋 کپی آدرس
        </button>

      </div>
    `;

    box.appendChild(div);

  });

}


/* =========================
   وضعیت
========================= */

function changeStatus(index,status){

  const list=
    JSON.parse(
      localStorage.getItem(
        "easyTradeTransactions"
      ) || "[]"
    );

  if(!list[index]) return;

  list[index].status=status;

  localStorage.setItem(
    "easyTradeTransactions",
    JSON.stringify(list)
  );

  renderAdmin();

  updateBell();

}


/* =========================
   کپی آدرس مدیر
========================= */

function copyAdminAddress(index){

  const list=
    JSON.parse(
      localStorage.getItem(
        "easyTradeTransactions"
      ) || "[]"
    );

  if(!list[index]) return;

  copyText(list[index].userWallet);

}


/* =========================
   زنگوله
========================= */

function updateBell(){

  const list=
    JSON.parse(
      localStorage.getItem(
        "easyTradeTransactions"
      ) || "[]"
    );

  const count=
    list.filter(function(x){

      return x.status==="در انتظار بررسی";

    }).length;

  document.getElementById("bellCount")
    .textContent=count;

  if(count>0){

    document.getElementById("notificationText")
      .innerHTML=
      "🔔 تعداد <strong>"+
      count+
      "</strong> تراکنش در انتظار بررسی مدیر است.";

  }else{

    document.getElementById("notificationText")
      .textContent=
      "تراکنش جدیدی در انتظار بررسی نیست.";

  }

}


/* =========================
   اعلان
========================= */

function toggleNotifications(){

  const box=
    document.getElementById(
      "notificationBox"
    );

  if(box.style.display==="block"){

    box.style.display="none";

  }else{

    updateBell();

    box.style.display="block";

  }

}


/* =========================
   امنیت نمایش متن
========================= */

function safe(value){

  return String(value)
    .replaceAll("&","&amp;")
    .replaceAll("<","&lt;")
    .replaceAll(">","&gt;")
    .replaceAll('"',"&quot;")
    .replaceAll("'","&#039;");

}


/* شروع */

updateWallet();
updateBell();

</script>
<!-- ================================
 FIX تبادل آسان - نمایش صحیح ارز
================================ -->

<style>
/* نمایش نتیجه واقعی تبادل */
.easy-exchange-fix{
  margin-top:15px;
  padding:16px;
  border-radius:15px;
  background:#101a12;
  border:1px solid #ffd000;
  text-align:center;
}

.easy-exchange-fix .exchange-line{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:10px;
  margin:8px 0;
  padding:10px;
  border-radius:10px;
  background:#071008;
}

.easy-exchange-fix .coin-name{
  color:#ffd000;
  font-weight:bold;
}

.easy-exchange-fix .coin-value{
  direction:ltr;
  font-weight:bold;
  color:#fff;
  word-break:break-all;
}

.easy-exchange-fix .arrow{
  color:#ffd000;
  font-size:25px;
}

#fixReceiveAmount{
  color:#00ff88;
  font-size:21px;
  font-weight:900;
}

#fixReceiveCoin{
  color:#ffd000;
  font-size:18px;
  font-weight:900;
}
</style>

<script>
(function(){

  /* ==========================================
     نرخ‌ها فقط برای محاسبه داخلی هستند.
     دلار به کاربر نمایش داده نمی‌شود.
  ========================================== */

  const FIX_RATES = {
    BTC: 110000,
    BCH: 500,
    DOGE: 0.25,
    USDT: 1,
    LTC: 100,
    DGB: 0.01,
    TRX: 0.35
  };

  const FIX_NAMES = {
    BTC: "Bitcoin (BTC)",
    BCH: "Bitcoin Cash (BCH)",
    DOGE: "Dogecoin (DOGE)",
    USDT: "Tether (USDT BEP-20)",
    LTC: "Litecoin (LTC)",
    DGB: "DigiByte (DGB)",
    TRX: "TRON (TRX)"
  };

  /*
    پیدا کردن select های قبلی سایت
  */
  function getFrom(){
    return document.getElementById("fromCoin");
  }

  function getTo(){
    return document.getElementById("toCoin");
  }

  function getAmount(){
    return document.getElementById("amount");
  }

  /*
    نتیجه مرحله دوم را کاملاً با ارز واقعی
    ارسال و دریافت بازسازی می‌کنیم.
  */
  function fixExchangeResult(){

    const fromSelect=getFrom();
    const toSelect=getTo();
    const amountInput=getAmount();

    if(!fromSelect || !toSelect || !amountInput){
      return;
    }

    const from=fromSelect.value;
    const to=toSelect.value;

    const amount=parseFloat(amountInput.value)||0;

    let receive=0;

    if(amount>0 && FIX_RATES[from] && FIX_RATES[to]){

      /*
        تبدیل داخلی:
        مقدار ارز ارسال × نرخ آن
        سپس تقسیم بر نرخ ارز دریافت

        دلار فقط واحد محاسبات داخلی است
        و هیچ‌وقت به کاربر نمایش داده نمی‌شود.
      */
      receive=
        (amount * FIX_RATES[from]) /
        FIX_RATES[to];
    }

    const oldAmount=
      document.getElementById("receiveAmount");

    const oldCoin=
      document.getElementById("receiveCoin");

    /*
      اگر عناصر قبلی وجود دارند،
      نتیجه آنها را هم اصلاح می‌کنیم.
    */
    if(oldAmount){

      oldAmount.textContent=
        receive>0
        ? formatCoinAmount(receive)
        : "0";
    }

    if(oldCoin){

      oldCoin.textContent=to;
    }

    /*
      نتیجه بصری جدید
    */
    let result=
      document.getElementById("easyExchangeFixResult");

    if(!result){

      result=
        document.createElement("div");

      result.id="easyExchangeFixResult";

      result.className="easy-exchange-fix";

      /*
        بعد از amountResult قرار می‌گیرد
      */
      const amountResult=
        document.querySelector(".amountResult");

      if(amountResult){

        amountResult.parentNode.insertBefore(
          result,
          amountResult.nextSibling
        );

      }else{

        amountInput.parentNode.appendChild(result);

      }
    }

    result.innerHTML=`

      <div class="exchange-line">

        <span class="coin-name">
          ارز ارسالی
        </span>

        <span class="coin-value">
          ${escapeFix(amount)} ${escapeFix(from)}
        </span>

      </div>

      <div class="arrow">
        ↓
      </div>

      <div class="exchange-line">

        <span class="coin-name">
          ارز دریافتی
        </span>

        <span class="coin-value">
          <span id="fixReceiveAmount">
            ${receive>0 ? formatCoinAmount(receive) : "0"}
          </span>

          <span id="fixReceiveCoin">
            ${escapeFix(to)}
          </span>
        </span>

      </div>

      <div style="
        margin-top:10px;
        color:#aaa;
        font-size:12px;
      ">
        ${escapeFix(FIX_NAMES[from])}
        →
        ${escapeFix(FIX_NAMES[to])}
      </div>
    `;
  }


  /*
    تعداد اعشار مناسب
  */
  function formatCoinAmount(value){

    if(value===0){
      return "0";
    }

    if(value>=1){
      return value.toFixed(8)
        .replace(/\.?0+$/,"");
    }

    return value.toFixed(12)
      .replace(/\.?0+$/,"");
  }


  /*
    جلوگیری از ورود HTML
  */
  function escapeFix(value){

    return String(value)
      .replaceAll("&","&amp;")
      .replaceAll("<","&lt;")
      .replaceAll(">","&gt;")
      .replaceAll('"',"&quot;")
      .replaceAll("'","&#039;");
  }


  /*
    وقتی ارز ارسالی تغییر کند
  */
  function fixFromChange(){

    fixExchangeResult();

    /*
      آدرس کیف پول سایت نیز مطابق ارز
      ارسالی قبلی تغییر می‌کند.
    */

    if(
      typeof updateWallet==="function"
    ){

      updateWallet();

    }
  }


  /*
    وقتی ارز دریافتی تغییر کند
  */
  function fixToChange(){

    fixExchangeResult();
  }


  /*
    وقتی مقدار تغییر کند
  */
  function fixAmountChange(){

    fixExchangeResult();
  }


  /*
    اتصال به select های قبلی
  */
  function installFix(){

    const from=getFrom();
    const to=getTo();
    const amount=getAmount();

    if(!from || !to || !amount){

      return;
    }

    /*
      حذف listenerهای قبلی با clone
      تا محاسبه قدیمی مزاحم نشود.
    */

    const newFrom=from.cloneNode(true);
    from.parentNode.replaceChild(newFrom,from);

    const newTo=to.cloneNode(true);
    to.parentNode.replaceChild(newTo,to);

    const newAmount=amount.cloneNode(true);
    amount.parentNode.replaceChild(newAmount,amount);

    newFrom.removeAttribute("onchange");
    newTo.removeAttribute("onchange");
    newAmount.removeAttribute("oninput");

    newFrom.addEventListener(
      "change",
      fixFromChange
    );

    newTo.addEventListener(
      "change",
      fixToChange
    );

    newAmount.addEventListener(
      "input",
      fixAmountChange
    );

    /*
      یک بار در شروع
    */
    fixExchangeResult();
  }


  /*
    چون ممکن است کد قبلی دیرتر اجرا شود،
    چند بار بررسی می‌کنیم.
  */

  function startFix(){

    if(
      getFrom() &&
      getTo() &&
      getAmount()
    ){

      installFix();

    }else{

      setTimeout(startFix,300);

    }
  }


  /*
    اگر مرحله دوم باز شد،
    نتیجه را دوباره تازه می‌کنیم.
  */

  const oldShowStep=
    window.showStep;

  if(typeof oldShowStep==="function"){

    window.showStep=function(step){

      oldShowStep(step);

      if(step===2){

        setTimeout(
          fixExchangeResult,
          50
        );

      }
    };
  }


  startFix();

})();
</script>
<!-- =========================================================
     نسخه نهایی «تبادل آسان»
     این کد را آخر کد سایت و قبل از </body> قرار بده
========================================================= -->

<style>
/* حذف دکمه/پنجره قدیمی */
#easyTradeBtn,
#easyTradeModal,
#tradeModal,
.easyTradeOld,
.tradeOld {
  display:none !important;
}

/* دکمه جدید تبادل آسان - ثابت وسط صفحه */
#NEW_EASY_EXCHANGE_BUTTON{
  width:175px;
  height:175px;
  border-radius:50%;
  border:6px solid #fff6a0;
  background:linear-gradient(145deg,#fff900,#ffb000);
  color:#171200;
  font-size:21px;
  font-weight:900;
  cursor:pointer;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  gap:7px;
  margin:35px auto;
  box-shadow:
    0 0 15px #ffd000,
    0 0 35px #ffd000,
    0 0 70px rgba(255,200,0,.7);
  animation:NEW_EASY_BLINK 1.15s infinite;
}

#NEW_EASY_BUTTON_ICON{
  font-size:42px;
}

@keyframes NEW_EASY_BLINK{
  0%,100%{
    transform:scale(1);
    box-shadow:0 0 15px #ffd000,0 0 35px #ffd000;
  }
  50%{
    transform:scale(1.08);
    box-shadow:
      0 0 25px #fff700,
      0 0 60px #ffb900,
      0 0 100px rgba(255,180,0,.7);
  }
}

/* زمینه پنجره */
#NEW_EASY_MODAL{
  display:none;
  position:fixed;
  inset:0;
  z-index:999999;
  background:rgba(0,0,0,.88);
  overflow-y:auto;
  padding:15px;
}

/* پنجره اصلی */
#NEW_EASY_BOX{
  width:100%;
  max-width:650px;
  margin:20px auto;
  background:linear-gradient(145deg,#122119,#060d08);
  border:2px solid #ffd000;
  border-radius:25px;
  padding:20px;
  box-shadow:0 0 50px rgba(255,208,0,.3);
  color:#fff;
}

/* هدر */
#NEW_EASY_HEADER{
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:1px solid #405027;
  padding-bottom:15px;
  margin-bottom:18px;
}

#NEW_EASY_HEADER h2{
  margin:0;
  color:#ffd000;
  font-size:22px;
}

#NEW_EASY_CLOSE{
  width:44px;
  height:44px;
  border:0;
  border-radius:50%;
  background:#a80000;
  color:#fff;
  font-size:25px;
  cursor:pointer;
}

/* مراحل */
.NEW_EASY_STEPS{
  display:flex;
  justify-content:center;
  gap:10px;
  margin-bottom:20px;
}

.NEW_EASY_STEP_CIRCLE{
  width:38px;
  height:38px;
  border-radius:50%;
  background:#273229;
  color:#aaa;
  display:flex;
  align-items:center;
  justify-content:center;
  font-weight:bold;
}

.NEW_EASY_STEP_CIRCLE.active{
  background:#ffd000;
  color:#111;
  box-shadow:0 0 17px #ffd000;
}

/* صفحات */
.NEW_EASY_PAGE{
  display:none;
}

.NEW_EASY_PAGE.active{
  display:block;
}

/* عنوان */
.NEW_EASY_PAGE h3{
  color:#ffd000;
}

/* برچسب */
.NEW_EASY_LABEL{
  display:block;
  color:#ffe36b;
  font-weight:bold;
  margin:13px 0 7px;
}

/* انتخاب ارز */
.NEW_EASY_SELECT{
  width:100%;
  padding:15px;
  border-radius:14px;
  border:1px solid #53622e;
  background:#0b150e;
  color:#fff;
  font-size:16px;
  outline:none;
}

.NEW_EASY_SELECT:focus{
  border-color:#ffd000;
}

/* جفت ارز */
#NEW_EASY_PAIR_BOX{
  margin-top:18px;
  padding:16px;
  border:1px solid #59662f;
  border-radius:17px;
  background:#09130c;
  text-align:center;
}

.NEW_EASY_PAIR_TITLE{
  color:#aaa;
  font-size:13px;
  margin-bottom:12px;
}

#NEW_EASY_PAIR{
  display:flex;
  justify-content:center;
  align-items:center;
  gap:10px;
  flex-wrap:wrap;
}

.NEW_EASY_COIN{
  min-width:105px;
  padding:11px 14px;
  border-radius:13px;
  background:#182519;
  border:1px solid #68783a;
  color:#ffd000;
  font-weight:bold;
}

.NEW_EASY_ARROW{
  color:#ffd000;
  font-size:25px;
}

/* مقدار */
.NEW_EASY_INPUT{
  width:100%;
  padding:15px;
  border-radius:14px;
  border:1px solid #53622e;
  background:#0b150e;
  color:#fff;
  font-size:16px;
  outline:none;
  direction:ltr;
  text-align:left;
}

.NEW_EASY_INPUT:focus{
  border-color:#ffd000;
}

/* نتیجه */
#NEW_EASY_RESULT{
  margin-top:17px;
  border-radius:17px;
  background:#09140d;
  border:1px solid #ffd000;
  padding:16px;
}

.NEW_EASY_RESULT_ROW{
  display:flex;
  justify-content:space-between;
  gap:10px;
  align-items:center;
  padding:11px;
  margin:6px 0;
  border-radius:11px;
  background:#101c13;
}

.NEW_EASY_RESULT_LABEL{
  color:#aaa;
}

.NEW_EASY_RESULT_VALUE{
  color:#fff;
  font-weight:bold;
  direction:ltr;
}

.NEW_EASY_RECEIVE{
  color:#00ff88 !important;
  font-size:20px;
}

/* کیف پول */
.NEW_EASY_WALLET{
  margin-top:17px;
  padding:15px;
  background:#09130c;
  border:1px solid #4e5e2b;
  border-radius:16px;
}

.NEW_EASY_WALLET_TITLE{
  color:#ffd000;
  font-weight:bold;
  margin-bottom:9px;
}

.NEW_EASY_ADDRESS{
  direction:ltr;
  text-align:left;
  word-break:break-all;
  padding:12px;
  border-radius:10px;
  background:#030604;
  color:#ddd;
  font-size:13px;
  line-height:1.7;
}

.NEW_EASY_COPY{
  width:100%;
  margin-top:9px;
  padding:11px;
  border:0;
  border-radius:11px;
  background:#ffd000;
  color:#111;
  font-weight:bold;
  cursor:pointer;
}

/* هشدار */
.NEW_EASY_NOTICE{
  margin-top:15px;
  padding:13px;
  border-radius:13px;
  background:#151d0f;
  border:1px solid #46542a;
  color:#ddd;
  line-height:1.9;
}

/* دکمه‌ها */
.NEW_EASY_BUTTONS{
  display:flex;
  gap:10px;
  margin-top:20px;
}

.NEW_EASY_MAIN,
.NEW_EASY_BACK{
  flex:1;
  padding:15px;
  border-radius:14px;
  cursor:pointer;
  font-weight:900;
}

.NEW_EASY_MAIN{
  border:0;
  background:linear-gradient(90deg,#ffe000,#ffad00);
  color:#111;
}

.NEW_EASY_BACK{
  border:1px solid #5b6934;
  background:#172118;
  color:#fff;
}

/* موبایل */
@media(max-width:500px){

  #NEW_EASY_EXCHANGE_BUTTON{
    width:155px;
    height:155px;
    font-size:19px;
  }

  #NEW_EASY_BOX{
    margin:5px auto;
    padding:15px;
  }

}
</style>


<!-- =========================================================
     دکمه جدید
========================================================= -->

<div id="NEW_EASY_BUTTON_AREA">
  <button id="NEW_EASY_EXCHANGE_BUTTON" onclick="NEW_EASY_OPEN()">
    <span id="NEW_EASY_BUTTON_ICON">⇄</span>
    <span>تبادل آسان</span>
  </button>
</div>


<!-- =========================================================
     پنجره جدید تبادل آسان
========================================================= -->

<div id="NEW_EASY_MODAL">

  <div id="NEW_EASY_BOX">

    <div id="NEW_EASY_HEADER">
      <h2>🔄 تبادل آسان</h2>
      <button id="NEW_EASY_CLOSE" onclick="NEW_EASY_CLOSE()">×</button>
    </div>


    <!-- مراحل -->

    <div class="NEW_EASY_STEPS">

      <div
        class="NEW_EASY_STEP_CIRCLE active"
        id="NEW_EASY_C1">
        1
      </div>

      <div
        class="NEW_EASY_STEP_CIRCLE"
        id="NEW_EASY_C2">
        2
      </div>

      <div
        class="NEW_EASY_STEP_CIRCLE"
        id="NEW_EASY_C3">
        3
      </div>

      <div
        class="NEW_EASY_STEP_CIRCLE"
        id="NEW_EASY_C4">
        4
      </div>

    </div>


    <!-- =====================================================
         مرحله ۱
    ====================================================== -->

    <div
      class="NEW_EASY_PAGE active"
      id="NEW_EASY_PAGE1">

      <h3>مرحله ۱ — انتخاب جفت ارز</h3>

      <label class="NEW_EASY_LABEL">
        ارز ارسالی
      </label>

      <select
        id="NEW_EASY_FROM"
        class="NEW_EASY_SELECT"
        onchange="NEW_EASY_UPDATE()">

        <option value="BTC">
          Bitcoin (BTC)
        </option>

        <option value="BCH">
          Bitcoin Cash (BCH)
        </option>

        <option value="DOGE">
          Dogecoin (DOGE)
        </option>

        <option value="USDT">
          Tether (USDT BEP-20)
        </option>

        <option value="LTC">
          Litecoin (LTC)
        </option>

        <option value="DGB">
          DigiByte (DGB)
        </option>

        <option value="TRX">
          TRON (TRX)
        </option>

      </select>


      <div style="
        text-align:center;
        color:#ffd000;
        font-size:30px;
        padding:9px;
      ">
        ↓
      </div>


      <label class="NEW_EASY_LABEL">
        ارز دریافتی
      </label>

      <select
        id="NEW_EASY_TO"
        class="NEW_EASY_SELECT"
        onchange="NEW_EASY_UPDATE()">

        <option value="BCH">
          Bitcoin Cash (BCH)
        </option>

        <option value="BTC">
          Bitcoin (BTC)
        </option>

        <option value="DOGE">
          Dogecoin (DOGE)
        </option>

        <option value="USDT">
          Tether (USDT BEP-20)
        </option>

        <option value="LTC">
          Litecoin (LTC)
        </option>

        <option value="DGB">
          DigiByte (DGB)
        </option>

        <option value="TRX">
          TRON (TRX)
        </option>

      </select>


      <!-- جفت ارز واقعی انتخاب‌شده -->

      <div id="NEW_EASY_PAIR_BOX">

        <div class="NEW_EASY_PAIR_TITLE">
          جفت ارز انتخاب‌شده
        </div>

        <div id="NEW_EASY_PAIR">

          <div
            class="NEW_EASY_COIN"
            id="NEW_EASY_PAIR_FROM">
            BTC
          </div>

          <div class="NEW_EASY_ARROW">
            ⇄
          </div>

          <div
            class="NEW_EASY_COIN"
            id="NEW_EASY_PAIR_TO">
            BCH
          </div>

        </div>

      </div>


      <div class="NEW_EASY_BUTTONS">

        <button
          class="NEW_EASY_MAIN"
          onclick="NEW_EASY_NEXT(2)">
          ادامه ←
        </button>

      </div>

    </div>


    <!-- =====================================================
         مرحله ۲
    ====================================================== -->

    <div
      class="NEW_EASY_PAGE"
      id="NEW_EASY_PAGE2">

      <h3>مرحله ۲ — مقدار تبادل</h3>


      <div class="NEW_EASY_NOTICE">

        <div>
          ارز ارسالی:
          <strong id="NEW_EASY_SEND_NAME">
            BTC
          </strong>
        </div>

        <div>
          ارز دریافتی:
          <strong id="NEW_EASY_GET_NAME">
            BCH
          </strong>
        </div>

      </div>


      <label class="NEW_EASY_LABEL">
        مقدار ارز ارسالی
      </label>

      <input
        id="NEW_EASY_AMOUNT"
        class="NEW_EASY_INPUT"
        type="number"
        min="0"
        step="any"
        placeholder="مثلاً 0.01"
        oninput="NEW_EASY_CALCULATE()">


      <!-- نتیجه واقعی -->
      <div id="NEW_EASY_RESULT">

        <div class="NEW_EASY_RESULT_ROW">

          <span class="NEW_EASY_RESULT_LABEL">
            ارسال
          </span>

          <span
            class="NEW_EASY_RESULT_VALUE"
            id="NEW_EASY_SEND_RESULT">
            0 BTC
          </span>

        </div>


        <div
          style="
            text-align:center;
            color:#ffd000;
            font-size:25px;
          ">
          ↓
        </div>


        <div class="NEW_EASY_RESULT_ROW">

          <span class="NEW_EASY_RESULT_LABEL">
            دریافت
          </span>

          <span
            class="NEW_EASY_RESULT_VALUE NEW_EASY_RECEIVE"
            id="NEW_EASY_GET_RESULT">
            0 BCH
          </span>

        </div>

      </div>


      <div class="NEW_EASY_NOTICE">
        ارز دریافتی بر اساس همان ارز انتخاب‌شده در مرحله اول نمایش داده می‌شود؛
        دلار به‌عنوان ارز دریافتی نمایش داده نمی‌شود.
      </div>


      <div class="NEW_EASY_BUTTONS">

        <button
          class="NEW_EASY_BACK"
          onclick="NEW_EASY_NEXT(1)">
          → برگشت
        </button>

        <button
          class="NEW_EASY_MAIN"
          onclick="NEW_EASY_GO3()">
          ادامه ←
        </button>

      </div>

    </div>


    <!-- =====================================================
         مرحله ۳
    ====================================================== -->

    <div
      class="NEW_EASY_PAGE"
      id="NEW_EASY_PAGE3">

      <h3>مرحله ۳ — آدرس کیف پول دریافت</h3>


      <div class="NEW_EASY_NOTICE">

        شما در حال تبدیل:

        <strong id="NEW_EASY_CONFIRM_PAIR">
          BTC → BCH
        </strong>

      </div>


      <label class="NEW_EASY_LABEL">
        آدرس کیف پول برای دریافت ارز
      </label>

      <input
        id="NEW_EASY_USER_WALLET"
        class="NEW_EASY_INPUT"
        type="text"
        placeholder="آدرس کیف پول خود را وارد کنید">


      <div class="NEW_EASY_BUTTONS">

        <button
          class="NEW_EASY_BACK"
          onclick="NEW_EASY_NEXT(2)">
          → برگشت
        </button>

        <button
          class="NEW_EASY_MAIN"
          onclick="NEW_EASY_GO4()">
          ادامه ←
        </button>

      </div>

    </div>


    <!-- =====================================================
         مرحله ۴
    ====================================================== -->

    <div
      class="NEW_EASY_PAGE"
      id="NEW_EASY_PAGE4">

      <h3>مرحله ۴ — تأیید تبادل</h3>


      <div class="NEW_EASY_NOTICE">

        <div>
          ارز ارسالی:
          <strong id="NEW_EASY_FINAL_FROM"></strong>
        </div>

        <div>
          مقدار ارسالی:
          <strong id="NEW_EASY_FINAL_AMOUNT"></strong>
        </div>

        <div>
          ارز دریافتی:
          <strong id="NEW_EASY_FINAL_TO"></strong>
        </div>

        <div>
          مقدار تقریبی دریافتی:
          <strong id="NEW_EASY_FINAL_RECEIVE"></strong>
        </div>

        <br>

        <div>
          آدرس دریافت شما:
        </div>

        <div
          class="NEW_EASY_ADDRESS"
          id="NEW_EASY_FINAL_USER_WALLET">
        </div>

      </div>


      <div class="NEW_EASY_WALLET">

        <div class="NEW_EASY_WALLET_TITLE">
          🏦 آدرس سایت برای ارسال ارز
        </div>

        <div
          class="NEW_EASY_ADDRESS"
          id="NEW_EASY_SITE_WALLET">
        </div>

        <button
          class="NEW_EASY_COPY"
          onclick="NEW_EASY_COPY_SITE()">
          📋 کپی آدرس
        </button>

      </div>


      <div class="NEW_EASY_BUTTONS">

        <button
          class="NEW_EASY_BACK"
          onclick="NEW_EASY_NEXT(3)">
          → برگشت
        </button>

        <button
          class="NEW_EASY_MAIN"
          onclick="NEW_EASY_REGISTER()">
          ✅ ثبت تبادل
        </button>

      </div>

    </div>

  </div>

</div>


<script>
/* =========================================================
   اطلاعات اصلی
========================================================= */

const NEW_EASY_WALLETS = {

  BTC:
  "1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

  BCH:
  "bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

  DOGE:
  "DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

  USDT:
  "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6",

  LTC:
  "LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

  DGB:
  "DEgjWtMywVrSMJp9URfZEEZvmDfbySryc8",

  TRX:
  "TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"

};


/* نام ارزها */

const NEW_EASY_NAMES = {

  BTC:"Bitcoin (BTC)",
  BCH:"Bitcoin Cash (BCH)",
  DOGE:"Dogecoin (DOGE)",
  USDT:"Tether (USDT BEP-20)",
  LTC:"Litecoin (LTC)",
  DGB:"DigiByte (DGB)",
  TRX:"TRON (TRX)"

};


/* نرخ‌ها برای محاسبه داخلی */

const NEW_EASY_RATES = {

  BTC:110000,
  BCH:500,
  DOGE:0.25,
  USDT:1,
  LTC:100,
  DGB:0.01,
  TRX:0.35

};


/* =========================================================
   باز کردن
========================================================= */

function NEW_EASY_OPEN(){

  document.getElementById(
    "NEW_EASY_MODAL"
  ).style.display="block";

  NEW_EASY_NEXT(1);

  NEW_EASY_UPDATE();

}


/* =========================================================
   بستن
========================================================= */

function NEW_EASY_CLOSE(){

  document.getElementById(
    "NEW_EASY_MODAL"
  ).style.display="none";

}


/* =========================================================
   تغییر مرحله
========================================================= */

function NEW_EASY_NEXT(step){

  document.querySelectorAll(
    ".NEW_EASY_PAGE"
  ).forEach(function(page){

    page.classList.remove("active");

  });


  document.getElementById(
    "NEW_EASY_PAGE"+step
  ).classList.add("active");


  for(let i=1;i<=4;i++){

    document.getElementById(
      "NEW_EASY_C"+i
    ).classList.remove("active");

  }


  document.getElementById(
    "NEW_EASY_C"+step
  ).classList.add("active");


  if(step===2){

    NEW_EASY_UPDATE();
    NEW_EASY_CALCULATE();

  }

}


/* =========================================================
   تغییر جفت ارز
========================================================= */

function NEW_EASY_UPDATE(){

  const from=
    document.getElementById(
      "NEW_EASY_FROM"
    ).value;

  const to=
    document.getElementById(
      "NEW_EASY_TO"
    ).value;


  /* نمایش جفت ارز */

  document.getElementById(
    "NEW_EASY_PAIR_FROM"
  ).textContent=from;


  document.getElementById(
    "NEW_EASY_PAIR_TO"
  ).textContent=to;


  /* نمایش در مرحله دوم */

  document.getElementById(
    "NEW_EASY_SEND_NAME"
  ).textContent=
    NEW_EASY_NAMES[from];


  document.getElementById(
    "NEW_EASY_GET_NAME"
  ).textContent=
    NEW_EASY_NAMES[to];


  NEW_EASY_CALCULATE();

}


/* =========================================================
   محاسبه
========================================================= */

function NEW_EASY_CALCULATE(){

  const from=
    document.getElementById(
      "NEW_EASY_FROM"
    ).value;

  const to=
    document.getElementById(
      "NEW_EASY_TO"
    ).value;

  const input=
    document.getElementById(
      "NEW_EASY_AMOUNT"
    );

  const amount=
    parseFloat(input.value)||0;


  let receive=0;


  if(
    amount>0 &&
    NEW_EASY_RATES[from] &&
    NEW_EASY_RATES[to]
  ){

    receive=
      (amount*NEW_EASY_RATES[from]) /
      NEW_EASY_RATES[to];

  }


  /* مهم:
     هیچ USD / USDT اجباری در اینجا نیست.
     ارز خروجی دقیقاً همان to است.
  */

  document.getElementById(
    "NEW_EASY_SEND_RESULT"
  ).textContent=
    formatNEW(amount)+" "+from;


  document.getElementById(
    "NEW_EASY_GET_RESULT"
  ).textContent=
    formatNEW(receive)+" "+to;


  document.getElementById(
    "NEW_EASY_PAIR_FROM"
  ).textContent=from;


  document.getElementById(
    "NEW_EASY_PAIR_TO"
  ).textContent=to;

}


/* =========================================================
   مرحله سوم
========================================================= */

function NEW_EASY_GO3(){

  const from=
    document.getElementById(
      "NEW_EASY_FROM"
    ).value;

  const to=
    document.getElementById(
      "NEW_EASY_TO"
    ).value;

  const amount=
    parseFloat(
      document.getElementById(
        "NEW_EASY_AMOUNT"
      ).value
    )||0;


  if(from===to){

    alert(
      "ارز ارسالی و دریافتی نباید یکسان باشد."
    );

    return;

  }


  if(amount<=0){

    alert(
      "لطفاً مقدار ارز ارسالی را وارد کنید."
    );

    return;

  }


  document.getElementById(
    "NEW_EASY_CONFIRM_PAIR"
  ).textContent=
    from+" → "+to;


  NEW_EASY_NEXT(3);

}


/* =========================================================
   مرحله چهار
========================================================= */

function NEW_EASY_GO4(){

  const wallet=
    document.getElementById(
      "NEW_EASY_USER_WALLET"
    ).value.trim();


  if(wallet.length<8){

    alert(
      "لطفاً آدرس کیف پول دریافت را وارد کنید."
    );

    return;

  }


  const from=
    document.getElementById(
      "NEW_EASY_FROM"
    ).value;

  const to=
    document.getElementById(
      "NEW_EASY_TO"
    ).value;

  const amount=
    parseFloat(
      document.getElementById(
        "NEW_EASY_AMOUNT"
      ).value
    )||0;


  let receive=
    (amount*NEW_EASY_RATES[from]) /
    NEW_EASY_RATES[to];


  document.getElementById(
    "NEW_EASY_FINAL_FROM"
  ).textContent=
    NEW_EASY_NAMES[from];


  document.getElementById(
    "NEW_EASY_FINAL_AMOUNT"
  ).textContent=
    formatNEW(amount)+" "+from;


  document.getElementById(
    "NEW_EASY_FINAL_TO"
  ).textContent=
    NEW_EASY_NAMES[to];


  document.getElementById(
    "NEW_EASY_FINAL_RECEIVE"
  ).textContent=
    formatNEW(receive)+" "+to;


  document.getElementById(
    "NEW_EASY_FINAL_USER_WALLET"
  ).textContent=wallet;


  /*
    آدرس سایت بر اساس ارز ارسالی
    انتخاب می‌شود.
  */

  document.getElementById(
    "NEW_EASY_SITE_WALLET"
  ).textContent=
    NEW_EASY_WALLETS[from];


  NEW_EASY_NEXT(4);

}


/* =========================================================
   ثبت تراکنش
========================================================= */

function NEW_EASY_REGISTER(){

  const from=
    document.getElementById(
      "NEW_EASY_FROM"
    ).value;

  const to=
    document.getElementById(
      "NEW_EASY_TO"
    ).value;

  const amount=
    parseFloat(
      document.getElementById(
        "NEW_EASY_AMOUNT"
      ).value
    )||0;

  const wallet=
    document.getElementById(
      "NEW_EASY_USER_WALLET"
    ).value.trim();


  const receive=
    (amount*NEW_EASY_RATES[from]) /
    NEW_EASY_RATES[to];


  const id=
    "EX-"+Date.now();


  const transaction={

    id:id,

    from:from,

    fromName:
      NEW_EASY_NAMES[from],

    to:to,

    toName:
      NEW_EASY_NAMES[to],

    amount:amount,

    receive:
      formatNEW(receive),

    userWallet:wallet,

    siteWallet:
      NEW_EASY_WALLETS[from],

    pair:
      from+" → "+to,

    status:
      "در انتظار بررسی",

    createdAt:
      new Date().toLocaleString("fa-IR")

  };


  /*
    ذخیره برای پنل مدیر
  */

  let list=[];

  try{

    list=JSON.parse(
      localStorage.getItem(
        "easyTradeTransactions"
      )||"[]"
    );

  }catch(e){

    list=[];

  }


  list.unshift(transaction);


  localStorage.setItem(
    "easyTradeTransactions",
    JSON.stringify(list)
  );


  alert(
    "تبادل با موفقیت ثبت شد ✅\n\n"+
    "شماره تراکنش:\n"+
    id+"\n\n"+
    "جفت ارز:\n"+
    from+" → "+to
  );


  NEW_EASY_CLOSE();


  /* پاک کردن فرم */

  document.getElementById(
    "NEW_EASY_AMOUNT"
  ).value="";


  document.getElementById(
    "NEW_EASY_USER_WALLET"
  ).value="";


  NEW_EASY_NEXT(1);

}


/* =========================================================
   کپی آدرس
========================================================= */

function NEW_EASY_COPY_SITE(){

  const address=
    document.getElementById(
      "NEW_EASY_SITE_WALLET"
    ).textContent;


  if(navigator.clipboard){

    navigator.clipboard.writeText(address)
      .then(function(){

        alert("آدرس کپی شد ✅");

      })
      .catch(function(){

        NEW_EASY_OLD_COPY(address);

      });

  }else{

    NEW_EASY_OLD_COPY(address);

  }

}


function NEW_EASY_OLD_COPY(text){

  const area=
    document.createElement("textarea");

  area.value=text;

  document.body.appendChild(area);

  area.select();

  document.execCommand("copy");

  area.remove();

  alert("آدرس کپی شد ✅");

}


/* =========================================================
   فرمت عدد
========================================================= */

function formatNEW(value){

  if(!value || value===0){

    return "0";

  }


  if(value>=1){

    return value
      .toFixed(8)
      .replace(/\.?0+$/,"");

  }


  return value
    .toFixed(12)
    .replace(/\.?0+$/,"");

}


/* =========================================================
   جلوگیری از نمایش HTML ناخواسته
========================================================= */

function NEW_EASY_ESCAPE(value){

  return String(value)
    .replaceAll("&","&amp;")
    .replaceAll("<","&lt;")
    .replaceAll(">","&gt;")
    .replaceAll('"',"&quot;")
    .replaceAll("'","&#039;");

}


/* =========================================================
   جلوگیری از نمایش دکمه قبلی
========================================================= */

(function(){

  function removeOldExchange(){

    const oldIds=[
      "easyTradeBtn",
      "tradeModal",
      "easyTradeModal"
    ];


    oldIds.forEach(function(id){

      const el=document.getElementById(id);

      if(el){

        el.style.display="none";

      }

    });


    /*
      اگر دکمه قدیمی متن «معامله آسان» داشته باشد،
      آن را هم پنهان می‌کنیم.
    */

    document
      .querySelectorAll("button")
      .forEach(function(btn){

        const text=
          (btn.textContent||"").trim();

        if(
          text.includes("معامله آسان") &&
          !text.includes("تبادل آسان")
        ){

          btn.style.display="none";

        }

      });

  }


  removeOldExchange();

  setTimeout(
    removeOldExchange,
    300
  );

  setTimeout(
    removeOldExchange,
    1000
  );

})();


/* =========================================================
   شروع
========================================================= */

document.addEventListener(
  "DOMContentLoaded",
  function(){

    NEW_EASY_UPDATE();

  }
);

</script>
<style>
/* فقط استایل دکمه تبادل آسان */
#NEW_EASY_EXCHANGE_BUTTON {
    position: fixed !important;
    top: 50% !important;
    left: 50% !important;
    right: auto !important;
    bottom: auto !important;

    transform: translate(-50%, -50%) !important;

    width: 230px !important;
    height: 230px !important;
    min-width: 230px !important;
    min-height: 230px !important;

    border-radius: 50% !important;
    border: 6px solid rgba(255,255,255,0.9) !important;

    display: flex !important;
    align-items: center !important;
    justify-content: center !important;

    font-size: 30px !important;
    font-weight: 900 !important;
    color: #111 !important;

    cursor: pointer !important;
    z-index: 999999 !important;

    animation: easyExchangeGreenYellow 1.2s infinite alternate !important;

    box-shadow:
        0 0 20px rgba(255,215,0,0.9),
        0 0 45px rgba(0,255,100,0.6),
        0 15px 40px rgba(0,0,0,0.35) !important;
}

@keyframes easyExchangeGreenYellow {
    0% {
        background: #ffd900 !important;
        box-shadow:
            0 0 20px #ffd900,
            0 0 45px rgba(255,217,0,0.8),
            0 15px 40px rgba(0,0,0,0.35);
    }

    100% {
        background: #00e676 !important;
        box-shadow:
            0 0 20px #00e676,
            0 0 55px rgba(0,230,118,0.9),
            0 15px 40px rgba(0,0,0,0.35);
    }
}

/* موبایل */
@media (max-width: 600px) {
    #NEW_EASY_EXCHANGE_BUTTON {
        width: 190px !important;
        height: 190px !important;
        min-width: 190px !important;
        min-height: 190px !important;
        font-size: 25px !important;
    }
}
</style>
<!-- دکمه ثابت تبادل آسان -->
<style>
  .easy-exchange-fixed {
    position: fixed;
    left: 50%;
    bottom: 18px;
    transform: translateX(-50%);
    z-index: 9999;

    padding: 15px 42px;
    border: 2px solid #00eaff;
    border-radius: 50px;

    background: linear-gradient(135deg, #00c853, #00b0ff);
    color: #ffffff;

    font-size: 20px;
    font-weight: 800;
    text-decoration: none;
    text-align: center;

    box-shadow:
      0 0 12px rgba(0, 234, 255, 0.8),
      0 0 25px rgba(0, 200, 83, 0.6);

    animation: easyExchangeBlink 1.5s infinite;
    transition: transform 0.2s ease;
  }

  .easy-exchange-fixed:hover {
    transform: translateX(-50%) scale(1.05);
  }

  @keyframes easyExchangeBlink {
    0%, 100% {
      opacity: 1;
      box-shadow:
        0 0 12px rgba(0, 234, 255, 0.8),
        0 0 25px rgba(0, 200, 83, 0.6);
    }

    50% {
      opacity: 0.65;
      box-shadow:
        0 0 25px rgba(0, 234, 255, 1),
        0 0 45px rgba(0, 200, 83, 0.9);
    }
  }

  @media (max-width: 600px) {
    .easy-exchange-fixed {
      bottom: 14px;
      padding: 13px 30px;
      font-size: 18px;
    }
  }
</style>

<a href="#exchange" class="easy-exchange-fixed">
  ⚡ تبادل آسان
</a>
```
```html
<!-- ===============================
     اخبار لحظه‌ای ارزهای دیجیتال
     =============================== -->

<style>
  .crypto-news-section {
    width: 100%;
    max-width: 1200px;
    margin: 60px auto 30px;
    padding: 0 15px;
    box-sizing: border-box;
  }

  .crypto-news-title {
    text-align: center;
    margin-bottom: 25px;
  }

  .crypto-news-title h2 {
    margin: 0;
    font-size: 28px;
    font-weight: 900;
    color: #111827;
  }

  .crypto-news-title p {
    margin: 8px 0 0;
    color: #6b7280;
    font-size: 14px;
  }

  .live-news-status {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    margin-top: 12px;
    padding: 7px 14px;
    border-radius: 20px;
    background: #f0fdf4;
    color: #15803d;
    font-size: 13px;
    font-weight: 700;
  }

  .live-news-dot {
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: #22c55e;
    animation: newsLiveBlink 1s infinite;
  }

  @keyframes newsLiveBlink {
    0%,100% {
      opacity: 1;
      transform: scale(1);
    }
    50% {
      opacity: .35;
      transform: scale(.75);
    }
  }

  .crypto-news-box {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 22px;
    padding: 20px;
    box-shadow: 0 8px 30px rgba(0,0,0,.08);
  }

  .crypto-news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
  }

  .crypto-news-card {
    overflow: hidden;
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 16px;
    transition: .25s ease;
  }

  .crypto-news-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 25px rgba(0,0,0,.10);
  }

  .crypto-news-image {
    width: 100%;
    height: 180px;
    object-fit: cover;
    display: block;
    background: #f3f4f6;
  }

  .crypto-news-content {
    padding: 16px;
  }

  .crypto-news-source {
    font-size: 12px;
    color: #2563eb;
    font-weight: 800;
    margin-bottom: 8px;
  }

  .crypto-news-card h3 {
    margin: 0 0 10px;
    font-size: 17px;
    line-height: 1.55;
    color: #111827;
  }

  .crypto-news-card p {
    margin: 0 0 12px;
    color: #6b7280;
    font-size: 13px;
    line-height: 1.7;
  }

  .crypto-news-card a {
    display: inline-block;
    color: #0891b2;
    font-size: 13px;
    font-weight: 800;
    text-decoration: none;
  }

  .crypto-news-time {
    margin-top: 10px;
    font-size: 11px;
    color: #9ca3af;
  }

  .news-loading {
    text-align: center;
    padding: 40px 10px;
    color: #6b7280;
    font-size: 15px;
  }

  .news-error {
    text-align: center;
    padding: 35px 15px;
    color: #6b7280;
    line-height: 1.8;
  }

  @media (max-width: 900px) {
    .crypto-news-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 600px) {
    .crypto-news-section {
      margin-top: 40px;
    }

    .crypto-news-title h2 {
      font-size: 23px;
    }

    .crypto-news-box {
      padding: 12px;
      border-radius: 18px;
    }

    .crypto-news-grid {
      grid-template-columns: 1fr;
      gap: 14px;
    }

    .crypto-news-image {
      height: 190px;
    }
  }
</style>


<section class="crypto-news-section" id="crypto-news">

  <div class="crypto-news-title">

    <h2>📰 اخبار لحظه‌ای ارزهای دیجیتال</h2>

    <p>
      آخرین اخبار و رویدادهای بازار رمزارزها
    </p>

    <div class="live-news-status">
      <span class="live-news-dot"></span>
      اخبار در حال به‌روزرسانی
    </div>

  </div>


  <div class="crypto-news-box">

    <div id="cryptoNewsGrid" class="crypto-news-grid">

      <div class="news-loading">
        در حال دریافت آخرین اخبار ارزهای دیجیتال...
      </div>

    </div>

  </div>

</section>


<script>
(function () {

  const newsGrid = document.getElementById("cryptoNewsGrid");

  const fallbackNews = [
    {
      title: "آخرین تحولات بازار ارزهای دیجیتال",
      description: "برای مشاهده آخرین اخبار و تحلیل‌های بازار رمزارزها، خبرهای جدید را دنبال کنید.",
      image: "https://images.unsplash.com/photo-1621761191319-c6fb62004040?auto=format&fit=crop&w=900&q=80",
      source: "Crypto News",
      link: "https://www.google.com/search?q=crypto+news"
    },
    {
      title: "تحولات جدید بازار بیت‌کوین",
      description: "آخرین اطلاعات و اخبار مرتبط با بیت‌کوین و بازار رمزارزها.",
      image: "https://images.unsplash.com/photo-1518546305927-5a555bb7020d?auto=format&fit=crop&w=900&q=80",
      source: "Crypto Market",
      link: "https://www.google.com/search?q=bitcoin+news"
    },
    {
      title: "اخبار مهم بازار رمزارزها",
      description: "جدیدترین رویدادهای مهم بازار ارزهای دیجیتال را دنبال کنید.",
      image: "https://images.unsplash.com/photo-1621416894569-0f39ed31d247?auto=format&fit=crop&w=900&q=80",
      source: "Crypto World",
      link: "https://www.google.com/search?q=cryptocurrency+news"
    }
  ];


  function escapeHTML(text) {

    const div = document.createElement("div");

    div.textContent = text || "";

    return div.innerHTML;

  }


  function renderNews(news) {

    newsGrid.innerHTML = "";

    news.slice(0, 6).forEach(function (item) {

      const card = document.createElement("article");

      card.className = "crypto-news-card";

      card.innerHTML = `
        <img
          class="crypto-news-image"
          src="${escapeHTML(item.image)}"
          alt="اخبار ارزهای دیجیتال"
          loading="lazy"
          onerror="this.style.display='none'"
        >

        <div class="crypto-news-content">

          <div class="crypto-news-source">
            ${escapeHTML(item.source || "اخبار رمزارز")}
          </div>

          <h3>
            ${escapeHTML(item.title)}
          </h3>

          <p>
            ${escapeHTML(item.description || "برای مشاهده جزئیات خبر کلیک کنید.")}
          </p>

          <a
            href="${escapeHTML(item.link || "#")}"
            target="_blank"
            rel="noopener noreferrer"
          >
            مشاهده خبر ←
          </a>

          <div class="crypto-news-time">
            آخرین به‌روزرسانی: ${new Date().toLocaleTimeString("fa-IR")}
          </div>

        </div>
      `;

      newsGrid.appendChild(card);

    });

  }


  async function loadCryptoNews() {

    try {

      /*
       * RSS2JSON خبرهای RSS را به JSON تبدیل می‌کند.
       * در صورت محدودیت سرویس، اخبار نمونه نمایش داده می‌شوند.
       */

      const rssURL =
        "https://api.rss2json.com/v1/api.json?rss_url=" +
        encodeURIComponent(
          "https://news.google.com/rss/search?q=cryptocurrency%20OR%20bitcoin%20OR%20ethereum&hl=en-US&gl=US&ceid=US:en"
        );

      const response = await fetch(rssURL, {
        cache: "no-store"
      });

      if (!response.ok) {
        throw new Error("News API error");
      }

      const data = await response.json();

      if (!data.items || !data.items.length) {
        throw new Error("No news");
      }

      const news = data.items.map(function (item) {

        return {
          title: item.title,
          description: item.description
            ? item.description.replace(/<[^>]*>/g, "").slice(0, 180)
            : "آخرین اخبار بازار ارزهای دیجیتال.",
          image:
            item.thumbnail ||
            "https://images.unsplash.com/photo-1621761191319-c6fb62004040?auto=format&fit=crop&w=900&q=80",
          source: item.author || "Crypto News",
          link: item.link
        };

      });

      renderNews(news);

    } catch (error) {

      console.log("Crypto news:", error);

      renderNews(fallbackNews);

    }

  }


  // بارگذاری اولیه
  loadCryptoNews();


  // به‌روزرسانی خودکار هر 5 دقیقه
  setInterval(function () {

    loadCryptoNews();

  }, 5 * 60 * 1000);


})();
</script>
``
<style>
/* دکمه تبادل آسان - پایین و ثابت */
.easy-exchange-fixed,
.easy-exchange-button,
.exchange-easy-button {
  position: fixed !important;
  left: 50% !important;
  bottom: 18px !important;
  top: auto !important;
  right: auto !important;
  transform: translateX(-50%) !important;

  z-index: 99999 !important;

  background: linear-gradient(135deg, #ffd600, #ffb300) !important;
  color: #111 !important;

  padding: 14px 38px !important;
  border-radius: 50px !important;
  border: 2px solid #fff !important;

  font-size: 19px !important;
  font-weight: 900 !important;
  white-space: nowrap !important;

  box-shadow:
    0 0 12px rgba(255, 214, 0, .8),
    0 0 28px rgba(255, 179, 0, .55) !important;

  animation: easyExchangeGlow 1.5s infinite !important;
}

@keyframes easyExchangeGlow {
  0%, 100% {
    opacity: 1;
    box-shadow:
      0 0 12px rgba(255, 214, 0, .8),
      0 0 28px rgba(255, 179, 0, .55);
  }

  50% {
    opacity: .72;
    box-shadow:
      0 0 25px rgba(255, 214, 0, 1),
      0 0 45px rgba(255, 179, 0, .9);
  }
}

/* موبایل */
@media (max-width: 600px) {
  .easy-exchange-fixed,
  .easy-exchange-button,
  .exchange-easy-button {
    bottom: 12px !important;
    padding: 12px 28px !important;
    font-size: 17px !important;
  }
}
</style>
<style>
/* فقط دکمه تبادل آسان */
#easy-exchange-bottom-button {
  position: fixed !important;
  top: auto !important;
  bottom: 20px !important;
  left: 50% !important;
  right: auto !important;

  transform: translateX(-50%) !important;

  width: auto !important;
  height: auto !important;

  margin: 0 !important;

  z-index: 2147483647 !important;
}
</style>

<script>
(function () {

  function findAndMoveExchangeButton() {

    const all = document.querySelectorAll('button, a');

    for (const el of all) {

      const text = (el.innerText || el.textContent || '')
        .replace(/\s+/g, ' ')
        .trim();

      if (
        text === 'تبادل آسان' ||
        text === '⚡ تبادل آسان' ||
        text === '🔄 تبادل آسان' ||
        text.includes('تبادل آسان')
      ) {

        /*
         * فقط خود دکمه را انتخاب می‌کنیم.
         * محتوای داخل آن، لینک‌ها و ۷ آدرس تغییر نمی‌کنند.
         */
        el.id = 'easy-exchange-bottom-button';

        return;
      }
    }
  }

  findAndMoveExchangeButton();

  window.addEventListener('load', findAndMoveExchangeButton);

  setTimeout(findAndMoveExchangeButton, 500);
  setTimeout(findAndMoveExchangeButton, 1500);
  setTimeout(findAndMoveExchangeButton, 3000);

})();
</script>
<!-- =========================================================
     FIX: انتقال خودکار دکمه «تبادل آسان / تبادل سریع» به پایین
     بدون تغییر محتویات، لینک‌ها یا آدرس‌های داخل آن
========================================================= -->

<style>
  #exchange-bottom-fixed {
    position: fixed !important;
    left: 50% !important;
    top: auto !important;
    right: auto !important;
    bottom: 18px !important;
    transform: translateX(-50%) !important;
    z-index: 2147483647 !important;

    width: 82px !important;
    height: 82px !important;
    min-width: 82px !important;
    min-height: 82px !important;

    border-radius: 50% !important;
    margin: 0 !important;
  }

  @media (max-width:600px) {
    #exchange-bottom-fixed {
      width: 70px !important;
      height: 70px !important;
      min-width: 70px !important;
      min-height: 70px !important;
      bottom: 12px !important;
    }
  }

  /* ================= اخبار ================= */

  #crypto-live-news {
    width: calc(100% - 24px);
    max-width: 1250px;
    margin: 70px auto 40px;
    box-sizing: border-box;
    font-family: inherit;
  }

  #crypto-live-news .news-title {
    text-align: center;
    margin-bottom: 22px;
  }

  #crypto-live-news .news-title h2 {
    margin: 0;
    color: #111827;
    font-size: 28px;
    font-weight: 900;
  }

  #crypto-live-news .news-title p {
    margin: 8px 0;
    color: #6b7280;
  }

  #crypto-live-news .live-label {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 7px 14px;
    border-radius: 20px;
    background: #ecfdf5;
    color: #15803d;
    font-size: 13px;
    font-weight: 800;
  }

  #crypto-live-news .live-dot {
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: #22c55e;
    animation: cryptoNewsPulse 1s infinite;
  }

  @keyframes cryptoNewsPulse {
    50% {
      opacity: .3;
      transform: scale(.75);
    }
  }

  #crypto-live-news .news-box {
    background: #fff;
    border: 1px solid #e5e7eb;
    border-radius: 22px;
    padding: 20px;
    box-shadow: 0 8px 30px rgba(0,0,0,.08);
  }

  #crypto-live-news .news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
  }

  #crypto-live-news .news-card {
    background: #fff;
    border: 1px solid #e5e7eb;
    border-radius: 16px;
    overflow: hidden;
    transition: transform .2s, box-shadow .2s;
  }

  #crypto-live-news .news-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 25px rgba(0,0,0,.1);
  }

  #crypto-live-news .news-card img {
    width: 100%;
    height: 175px;
    object-fit: cover;
    display: block;
  }

  #crypto-live-news .news-content {
    padding: 15px;
  }

  #crypto-live-news .news-source {
    color: #2563eb;
    font-size: 12px;
    font-weight: 900;
    margin-bottom: 8px;
  }

  #crypto-live-news .news-card h3 {
    margin: 0 0 9px;
    color: #111827;
    font-size: 17px;
    line-height: 1.6;
  }

  #crypto-live-news .news-card p {
    margin: 0 0 12px;
    color: #6b7280;
    font-size: 13px;
    line-height: 1.7;
  }

  #crypto-live-news .news-card a {
    color: #0891b2;
    text-decoration: none;
    font-size: 13px;
    font-weight: 900;
  }

  #crypto-live-news .news-date {
    margin-top: 10px;
    color: #9ca3af;
    font-size: 11px;
  }

  #crypto-live-news .loading {
    text-align: center;
    padding: 45px 10px;
    color: #6b7280;
  }

  @media (max-width:900px) {
    #crypto-live-news .news-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width:600px) {
    #crypto-live-news .news-grid {
      grid-template-columns: 1fr;
    }

    #crypto-live-news .news-box {
      padding: 12px;
    }

    #crypto-live-news .news-title h2 {
      font-size: 23px;
    }
  }
</style>


<script>
(function () {

  /* ======================================================
     پیدا کردن دکمه موجود
     فقط موقعیت خود دکمه تغییر می‌کند
  ====================================================== */

  function findExchangeButton() {

    if (document.getElementById('exchange-bottom-fixed')) {
      return;
    }

    const items = document.querySelectorAll(
      'button, a, [role="button"]'
    );

    for (const item of items) {

      const text = (
        item.innerText ||
        item.textContent ||
        ''
      ).replace(/\s+/g, ' ').trim();

      if (
        text === 'تبادل آسان' ||
        text === 'تبادل سریع' ||
        text.includes('تبادل آسان') ||
        text.includes('تبادل سریع')
      ) {

        item.id = 'exchange-bottom-fixed';

        return;
      }
    }
  }


  findExchangeButton();

  window.addEventListener(
    'load',
    findExchangeButton
  );

  setTimeout(findExchangeButton, 300);
  setTimeout(findExchangeButton, 1000);
  setTimeout(findExchangeButton, 2500);
  setTimeout(findExchangeButton, 5000);


  /* اگر سایت دکمه را بعداً ایجاد کند */
  const observer = new MutationObserver(
    findExchangeButton
  );

  observer.observe(document.body, {
    childList: true,
    subtree: true
  });


  /* ======================================================
     ساخت بخش اخبار در انتهای سایت
  ====================================================== */

  const newsSection =
    document.createElement('section');

  newsSection.id = 'crypto-live-news';

  newsSection.innerHTML = `
    <div class="news-title">

      <h2>📰 اخبار لحظه‌ای ارزهای دیجیتال</h2>

      <p>
        جدیدترین اخبار بازار رمزارزها از منابع مختلف
      </p>

      <div class="live-label">
        <span class="live-dot"></span>
        بروزرسانی خودکار
      </div>

    </div>

    <div class="news-box">

      <div id="cryptoNewsGrid" class="news-grid">

        <div class="loading">
          در حال دریافت آخرین اخبار...
        </div>

      </div>

    </div>
  `;

  document.body.appendChild(newsSection);


  /* ======================================================
     10 منبع خبری
  ====================================================== */

  const feeds = [

    {
      name: 'CoinDesk',
      url:
      'https://www.coindesk.com/arc/outboundfeeds/rss/'
    },

    {
      name: 'Cointelegraph',
      url:
      'https://cointelegraph.com/rss'
    },

    {
      name: 'Bitcoin Magazine',
      url:
      'https://bitcoinmagazine.com/.rss/full/'
    },

    {
      name: 'Decrypt',
      url:
      'https://decrypt.co/feed'
    },

    {
      name: 'CryptoSlate',
      url:
      'https://cryptoslate.com/feed/'
    },

    {
      name: 'NewsBTC',
      url:
      'https://www.newsbtc.com/feed/'
    },

    {
      name: 'Bitcoinist',
      url:
      'https://bitcoinist.com/feed/'
    },

    {
      name: 'CryptoPotato',
      url:
      'https://cryptopotato.com/feed/'
    },

    {
      name: 'U.Today',
      url:
      'https://u.today/rss'
    },

    {
      name: 'Google News Crypto',
      url:
      'https://news.google.com/rss/search?q=cryptocurrency%20bitcoin%20ethereum&hl=en-US&gl=US&ceid=US:en'
    }

  ];


  const grid =
    document.getElementById('cryptoNewsGrid');


  function clean(text) {

    const div =
      document.createElement('div');

    div.innerHTML = text || '';

    return (
      div.textContent ||
      div.innerText ||
      ''
    )
    .replace(/\s+/g, ' ')
    .trim();

  }


  async function loadFeed(feed) {

    try {

      const api =
        'https://api.rss2json.com/v1/api.json?rss_url=' +
        encodeURIComponent(feed.url);

      const response =
        await fetch(api, {
          cache: 'no-store'
        });

      if (!response.ok) {
        return [];
      }

      const data =
        await response.json();

      if (
        !data.items ||
        !Array.isArray(data.items)
      ) {
        return [];
      }


      return data.items.slice(0, 5).map(
        function (item) {

          return {

            title:
              clean(item.title) ||
              'خبر جدید ارز دیجیتال',

            description:
              clean(item.description)
              .slice(0, 190) ||
              'آخرین اخبار بازار رمزارزها.',

            link:
              item.link || '#',

            image:
              item.thumbnail ||
              'https://images.unsplash.com/photo-1621761191319-c6fb62004040?auto=format&fit=crop&w=900&q=80',

            source:
              feed.name,

            date:
              item.pubDate || ''

          };

        }
      );

    } catch (e) {

      return [];

    }

  }


  async function loadNews() {

    grid.innerHTML = `
      <div class="loading">
        در حال دریافت اخبار از منابع مختلف...
      </div>
    `;


    const responses =
      await Promise.all(
        feeds.map(loadFeed)
      );


    let all = [];

    responses.forEach(function (items) {
      all = all.concat(items);
    });


    /* حذف خبرهای کاملاً تکراری */

    const seen = new Set();

    all = all.filter(function (item) {

      const key =
        item.title
          .toLowerCase()
          .replace(/[^a-z0-9\u0600-\u06ff]+/g, ' ')
          .trim();

      if (seen.has(key)) {
        return false;
      }

      seen.add(key);

      return true;

    });


    /* مرتب‌سازی جدیدترین خبرها */

    all.sort(function (a, b) {

      return (
        new Date(b.date || 0) -
        new Date(a.date || 0)
      );

    });


    /* نمایش چندین خبر */

    const news =
      all.slice(0, 18);


    if (!news.length) {

      grid.innerHTML = `
        <div class="loading">
          در حال حاضر خبر جدیدی دریافت نشد.
        </div>
      `;

      return;

    }


    grid.innerHTML = '';


    news.forEach(function (item) {

      const card =
        document.createElement('article');

      card.className = 'news-card';


      const date =
        item.date
          ? new Date(item.date)
              .toLocaleString('fa-IR')
          : 'به‌تازگی';


      card.innerHTML = `

        <img
          src="${item.image}"
          alt="خبر ارز دیجیتال"
          loading="lazy"
        >

        <div class="news-content">

          <div class="news-source">
            ${item.source}
          </div>

          <h3>
            ${escapeHTML(item.title)}
          </h3>

          <p>
            ${escapeHTML(item.description)}
          </p>

          <a
            href="${item.link}"
            target="_blank"
            rel="noopener noreferrer"
          >
            مشاهده خبر ←
          </a>

          <div class="news-date">
            ${date}
          </div>

        </div>
      `;


      grid.appendChild(card);

    });

  }


  function escapeHTML(text) {

    const div =
      document.createElement('div');

    div.textContent =
      text || '';

    return div.innerHTML;

  }


  loadNews();


  /* بروزرسانی هر 5 دقیقه */

  setInterval(
    loadNews,
    5 * 60 * 1000
  );

})();
</script>
```
```
<script>
(function () {
    function moveExchangeButtonIntoSettings() {
        // پیدا کردن عنوان تنظیمات
        const settingsTitle = [...document.querySelectorAll('*')].find(el => {
            const t = (el.textContent || '').replace(/\s+/g, ' ').trim();
            return t === '⚙️ تنظیمات سایت';
        });

        if (!settingsTitle) return;

        // پیدا کردن دکمه اصلی معامله آسان
        const exchangeButton = [...document.querySelectorAll('button')].find(btn => {
            const t = (btn.textContent || '').replace(/\s+/g, ' ').trim();
            return t === '⇄ معامله آسان' || t === 'معامله آسان';
        });

        if (!exchangeButton) return;

        // پیدا کردن پنل واقعی تنظیمات
        let settingsPanel = settingsTitle.parentElement;

        // اگر والد مستقیم فقط عنوان بود، چند مرحله بالاتر را بررسی کن
        for (let i = 0; i < 5 && settingsPanel; i++) {
            if (
                settingsPanel.contains(settingsTitle) &&
                settingsPanel.querySelectorAll('button').length >= 1
            ) {
                break;
            }
            settingsPanel = settingsPanel.parentElement;
        }

        if (!settingsPanel) return;

        // انتقال خود دکمه به داخل تنظیمات
        if (!settingsPanel.contains(exchangeButton)) {
            settingsPanel.appendChild(exchangeButton);
        }

        // ظاهر دکمه را دست نمی‌زنیم
        // فقط جای آن داخل تنظیمات است
        exchangeButton.style.removeProperty('position');
        exchangeButton.style.removeProperty('left');
        exchangeButton.style.removeProperty('right');
        exchangeButton.style.removeProperty('top');
        exchangeButton.style.removeProperty('bottom');
        exchangeButton.style.removeProperty('transform');
    }

    moveExchangeButtonIntoSettings();

    window.addEventListener('load', moveExchangeButtonIntoSettings);

    const observer = new MutationObserver(function () {
        moveExchangeButtonIntoSettings();
    });

    observer.observe(document.body, {
        childList: true,
        subtree: true
    });
})();
</script>
```

</body>
</html>
</body>
</html>
