<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Crypto Exchange</title>

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

/* HEADER */

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
  box-shadow:
    0 0 8px #00ff55,
    0 0 18px #00ff55;
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

/* THEMES */

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

/* MARKET */

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

/* EXCHANGE */

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

/* BUY SELL */

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
  box-shadow:
    0 0 15px rgba(0,255,80,.35);
}

.sell{
  background:#df1834;
  box-shadow:
    0 0 15px rgba(255,0,40,.35);
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

/* MESSAGE */

.message{
  text-align:center;
  margin-top:15px;
  color:#ddd;
  font-size:13px;
  min-height:25px;
}

/* INFO */

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

/* RESPONSIVE */

@media(max-width:950px){

  .market{
    grid-template-columns:repeat(3,1fr);
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

}
</style>
</head>

<body>

<div class="container">

  <!-- HEADER -->

  <div class="header">

    <div class="header-row">

      <div class="logo">
        ₿ Crypto Exchange
      </div>

      <div class="status">

        <span id="globalLight"
              class="status-light offline"></span>

        <span id="globalStatus">
          در حال اتصال به بازار...
        </span>

      </div>

    </div>

  </div>


  <!-- THEMES -->

  <div class="themes">

    <button
      class="theme theme-yellow"
      onclick="setTheme('')">
    </button>

    <button
      class="theme theme-blue"
      onclick="setTheme('blue')">
    </button>

    <button
      class="theme theme-purple"
      onclick="setTheme('purple')">
    </button>

    <button
      class="theme theme-orange"
      onclick="setTheme('orange')">
    </button>

  </div>


  <!-- MARKET -->

  <div class="market">

    <!-- BTC -->

    <div class="coin">

      <img
        src="https://assets.coingecko.com/coins/images/1/large/bitcoin.png"
        alt="Bitcoin">

      <div class="coin-name">
        Bitcoin
      </div>

      <div
        id="price-BTC"
        class="coin-price">
        در حال دریافت...
      </div>

      <div
        id="state-BTC"
        class="coin-state">
        ● اتصال
      </div>

    </div>


    <!-- BCH -->

    <div class="coin">

      <img
        src="https://assets.coingecko.com/coins/images/780/large/bitcoin-cash-circle.png"
        alt="Bitcoin Cash">

      <div class="coin-name">
        Bitcoin Cash
      </div>

      <div
        id="price-BCH"
        class="coin-price">
        در حال دریافت...
      </div>

      <div
        id="state-BCH"
        class="coin-state">
        ● اتصال
      </div>

    </div>


    <!-- TRX -->

    <div class="coin">

      <img
        src="https://assets.coingecko.com/coins/images/1094/large/tron-logo.png"
        alt="TRON">

      <div class="coin-name">
        TRON
      </div>

      <div
        id="price-TRX"
        class="coin-price">
        در حال دریافت...
      </div>

      <div
        id="state-TRX"
        class="coin-state">
        ● اتصال
      </div>

    </div>


    <!-- LTC -->

    <div class="coin">

      <img
        src="https://assets.coingecko.com/coins/images/2/large/litecoin.png"
        alt="Litecoin">

      <div class="coin-name">
        Litecoin
      </div>

      <div
        id="price-LTC"
        class="coin-price">
        در حال دریافت...
      </div>

      <div
        id="state-LTC"
        class="coin-state">
        ● اتصال
      </div>

    </div>


    <!-- DOGE -->

    <div class="coin">

      <img
        src="https://assets.coingecko.com/coins/images/5/large/dogecoin.png"
        alt="Dogecoin">

      <div class="coin-name">
        Dogecoin
      </div>

      <div
        id="price-DOGE"
        class="coin-price">
        در حال دریافت...
      </div>

      <div
        id="state-DOGE"
        class="coin-state">
        ● اتصال
      </div>

    </div>


    <!-- USDT -->

    <div class="coin">

      <img
        src="https://assets.coingecko.com/coins/images/325/large/Tether.png"
        alt="USDT">

      <div class="coin-name">
        Tether
      </div>

      <div
        id="price-USDT"
        class="coin-price">
        $1.00
      </div>

      <div
        class="coin-state"
        style="color:#00ff55">
        ● فعال
      </div>

    </div>

  </div>


  <!-- EXCHANGE -->

  <div class="exchange">

    <div class="exchange-title">
      تبدیل ارز
    </div>


    <div class="exchange-grid">


      <!-- FROM -->

      <div class="card">

        <div class="card-title">
          ارزی که می‌دهی
        </div>

        <select id="fromCoin">

          <option value="BTC">
            BTC - Bitcoin
          </option>

          <option value="BCH">
            BCH - Bitcoin Cash
          </option>

          <option value="TRX">
            TRX - TRON
          </option>

          <option value="LTC">
            LTC - Litecoin
          </option>

          <option value="DOGE">
            DOGE - Dogecoin
          </option>

          <option value="USDT">
            USDT - Tether
          </option>

        </select>


        <input
          id="fromAmount"
          type="number"
          min="0"
          step="any"
          placeholder="مقدار">

      </div>


      <!-- TO -->

      <div class="card">

        <div class="card-title">
          ارزی که می‌گیری
        </div>

        <select id="toCoin">

          <option value="USDT">
            USDT - Tether
          </option>

          <option value="BTC">
            BTC - Bitcoin
          </option>

          <option value="BCH">
            BCH - Bitcoin Cash
          </option>

          <option value="TRX">
            TRX - TRON
          </option>

          <option value="LTC">
            LTC - Litecoin
          </option>

          <option value="DOGE">
            DOGE - Dogecoin
          </option>

        </select>


        <div
          id="toAmount"
          class="result">
          مقدار دریافتی
        </div>

      </div>

    </div>


    <!-- BUY SELL -->

    <div class="trade-buttons">

      <button
        class="trade buy"
        onclick="trade('BUY')">

        🟢 BUY

      </button>


      <button
        class="trade sell"
        onclick="trade('SELL')">

        🔴 SELL

      </button>

    </div>


    <div
      id="message"
      class="message">

      قیمت‌ها در حال دریافت هستند...

    </div>


    <div class="info">

      قیمت‌ها از چندین منبع بازار بررسی می‌شوند.
      اگر یک منبع قطع شود، منابع دیگر استفاده می‌شوند.
      اگر تمام منابع موقتاً قطع شوند، آخرین قیمت معتبر
      روی سایت باقی می‌ماند تا اتصال دوباره برقرار شود.

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

async function getJSON(
  url,
  timeout = 7000
){

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
      throw new Error(
        "HTTP " +
        response.status
      );
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
      "https://api.binance.com/api/v3/ticker/price?symbol=" +
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
      "https://api.coinbase.com/v2/prices/" +
      coin +
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
      "https://api.kraken.com/0/public/Ticker?pair=" +
      pairs[coin]
    );

  const key =
    Object.keys(
      data?.result || {}
    )[0];

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
      "https://api.kucoin.com/api/v1/market/orderbook/level1?symbol=" +
      coin +
      "-USDT"
    );

  const price =
    Number(
      data?.data?.price
    );

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
      "https://www.okx.com/api/v5/market/ticker?instId=" +
      coin +
      "-USDT"
    );

  const price =
    Number(
      data?.data?.[0]?.last
    );

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
      "https://api.bybit.com/v5/market/tickers?category=spot&symbol=" +
      coin +
      "USDT"
    );

  const price =
    Number(
      data?.result?.list?.[0]?.lastPrice
    );

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
      "https://api.gateio.ws/api/v4/spot/tickers?currency_pair=" +
      coin +
      "_USDT"
    );

  const price =
    Number(
      data?.[0]?.last
    );

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
      "https://api.bitget.com/api/v2/spot/market/tickers?symbol=" +
      coin +
      "USDT"
    );

  const price =
    Number(
      data?.data?.[0]?.lastPr
    );

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
      "https://api.mexc.com/api/v3/ticker/price?symbol=" +
      coin +
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
      "https://api.huobi.pro/market/detail/merged?symbol=" +
      coin.toLowerCase() +
      "usdt"
    );

  const price =
    Number(
      data?.tick?.close
    );

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
      "https://api.lbkex.com/v2/ticker/24hr.do?symbol=" +
      coin.toLowerCase() +
      "_usdt"
    );

  let price = null;

  if(Array.isArray(data?.data)){

    const item =
      data.data[0];

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
      "https://api.coinex.com/v2/spot/ticker?market=" +
      coin.toLowerCase() +
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
      "https://api-cloud.bitmart.com/spot/v1/ticker?symbol=" +
      coin +
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
      "https://api.crypto.com/exchange/v1/public/get-ticker?instrument_name=" +
      coin +
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
      "https://api.gemini.com/v1/pubticker/" +
      coin.toLowerCase() +
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
      "https://www.bitstamp.net/api/v2/ticker/" +
      coin.toLowerCase() +
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
      "https://whitebit.com/api/v4/public/ticker?market=" +
      coin +
      "_USDT"
    );

  const price =
    Number(
      data?.last_price
    );

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
      "https://api.phemex.com/md/ticker/24hr?symbol=" +
      coin +
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
      "https://ascendex.com/api/pro/v1/ticker?symbol=" +
      coin +
      "/USDT"
    );

  const price =
    Number(
      data?.data?.close
    );

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
      "https://api.coingecko.com/api/v3/simple/price" +
      "?ids=bitcoin,bitcoin-cash,tron,litecoin,dogecoin" +
      "&vs_currencies=usd"
    );

  return {

    BTC:
      Number(
        data?.bitcoin?.usd
      ),

    BCH:
      Number(
        data?.["bitcoin-cash"]?.usd
      ),

    TRX:
      Number(
        data?.tron?.usd
      ),

    LTC:
      Number(
        data?.litecoin?.usd
      ),

    DOGE:
      Number(
        data?.dogecoin?.usd
      )

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

      validPrices.push(
        result.value
      );

    }

  });


  /*
    CoinGecko separately checked.
  */

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

    console.log(
      "CoinGecko unavailable"
    );

  }


  const finalPrice =
    median(validPrices);


  const priceElement =
    document.getElementById(
      "price-" + coin
    );

  const stateElement =
    document.getElementById(
      "state-" + coin
    );


  if(finalPrice !== null){

    prices[coin] =
      finalPrice;


    /*
      Save last valid price.
    */

    try{

      localStorage.setItem(
        "lastPrice_" + coin,
        String(finalPrice)
      );

    }catch(error){}


    priceElement.textContent =
      formatPrice(finalPrice);


    stateElement.textContent =
      "● آنلاین | " +
      validPrices.length +
      " منبع";


    stateElement.style.color =
      "#00ff55";


    return true;

  }


  /*
    No current source.
    Load last valid price.
  */

  if(prices[coin] === null){

    try{

      const saved =
        Number(
          localStorage.getItem(
            "lastPrice_" + coin
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
      formatPrice(
        prices[coin]
      );

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
      "بازار آنلاین | " +
      onlineCount +
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
    Number(
      prices[from]
    );

  const toPrice =
    Number(
      prices[to]
    );


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
    amount *
    fromPrice;


  const received =
    usdValue /
    toPrice;


  output.textContent =
    received.toLocaleString(
      "en-US",
      {
        maximumFractionDigits:10
      }
    ) +
    " " +
    to;


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


  if(type === "BUY"){

    message.textContent =
      "🟢 BUY | خرید " +
      to +
      " با " +
      from +
      " | مقدار " +
      amount;

  }else{

    message.textContent =
      "🔴 SELL | فروش " +
      from +
      " برای دریافت " +
      to +
      " | مقدار " +
      amount;

  }

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

updateAllPrices();


/*
  Every 20 seconds
*/

setInterval(
  updateAllPrices,
  20000
);


/*
  Extra check after 5 seconds
*/

setTimeout(
  updateAllPrices,
  5000
);

</script>

</body>
</html>
