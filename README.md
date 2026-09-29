<!DOCTYPE html>
<html lang="fa" dir="rtl">

<head>

<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width, initial-scale=1.0">

<title>صرافی تبادل ارز</title>

<style>

/* =====================================================
   TABADOL EXCHANGE
   COMPLETE VERSION
===================================================== */

:root{
  --bg:#ffd600;
  --card:#111;
  --text:#fff;
  --green:#00e676;
  --orange:#ff9800;
  --red:#ff3b30;
  --blue:#2196f3;
}

*{
  box-sizing:border-box;
}

body{
  margin:0;
  min-height:100vh;
  background:var(--bg);
  color:#111;
  font-family:
    Tahoma,
    Arial,
    sans-serif;
  transition:.3s;
}

button,
input,
select{
  font-family:inherit;
}


/* =====================================================
   HEADER
===================================================== */

header{
  background:rgba(0,0,0,.92);
  color:white;
  padding:15px;
  text-align:center;
  position:sticky;
  top:0;
  z-index:100;
  box-shadow:0 3px 15px rgba(0,0,0,.3);
}

.header-title{
  font-size:27px;
  font-weight:bold;
}

.header-sub{
  font-size:12px;
  opacity:.75;
  margin-top:5px;
}


/* =====================================================
   LOGO
===================================================== */

.logo{
  width:70px;
  height:70px;
  margin:0 auto 8px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:42px;
  background:
    radial-gradient(
      circle,
      #fff 0%,
      #ffe600 35%,
      #ff9800 60%,
      #ff3d00 100%
    );
  box-shadow:
    0 0 15px #fff,
    0 0 35px #ff9800,
    0 0 55px #ff3d00;
  animation:logoGlow 1s infinite alternate;
}

@keyframes logoGlow{
  from{
    transform:scale(.96);
    box-shadow:
      0 0 10px #fff,
      0 0 25px #ff9800;
  }
  to{
    transform:scale(1.04);
    box-shadow:
      0 0 20px #fff,
      0 0 45px #ff9800,
      0 0 70px #ff3d00;
  }
}


/* =====================================================
   MAIN
===================================================== */

.container{
  width:94%;
  max-width:1150px;
  margin:22px auto;
}


/* =====================================================
   LIVE STATUS
===================================================== */

.live-status{
  background:#111;
  color:white;
  border-radius:15px;
  padding:12px;
  text-align:center;
  margin-bottom:15px;
  font-size:14px;
}


/* =====================================================
   COIN CARDS
===================================================== */

.coin-grid{
  display:grid;
  grid-template-columns:
    repeat(auto-fit,minmax(155px,1fr));
  gap:12px;
}

.coin-card{
  background:rgba(0,0,0,.84);
  color:white;
  padding:17px 10px;
  border-radius:20px;
  text-align:center;
  box-shadow:0 7px 18px rgba(0,0,0,.25);
}

.coin-led{
  width:13px;
  height:13px;
  background:#00ff55;
  border-radius:50%;
  margin:0 auto 9px;
  box-shadow:
    0 0 7px #00ff55,
    0 0 20px #00ff55;
  animation:ledBlink .7s infinite alternate;
}

@keyframes ledBlink{
  from{
    opacity:.25;
    transform:scale(.7);
  }
  to{
    opacity:1;
    transform:scale(1.25);
  }
}

.coin-name{
  font-weight:bold;
  font-size:16px;
}

.coin-price{
  font-size:19px;
  font-weight:bold;
  margin-top:8px;
  color:#fff;
}

.coin-time{
  font-size:10px;
  opacity:.55;
  margin-top:5px;
}


/* =====================================================
   PANELS
===================================================== */

.panel{
  background:rgba(0,0,0,.88);
  color:white;
  border-radius:22px;
  padding:22px;
  margin-top:20px;
  box-shadow:0 8px 25px rgba(0,0,0,.3);
}

.panel-title{
  text-align:center;
  font-size:23px;
  font-weight:bold;
  margin-bottom:18px;
}


/* =====================================================
   BUY SELL
===================================================== */

.trade-buttons{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
  margin-bottom:18px;
}

.trade-buttons button{
  padding:18px 10px;
  border:0;
  border-radius:16px;
  font-size:22px;
  font-weight:bold;
  cursor:pointer;
  transition:.2s;
}

.trade-buttons button:hover{
  transform:scale(1.02);
}

.buy-btn{
  background:#00e676;
  color:#000;
}

.sell-btn{
  background:#ffb300;
  color:#000;
}

.trade-buttons .active{
  box-shadow:
    0 0 0 4px #fff,
    0 0 25px currentColor;
}


/* =====================================================
   FORM
===================================================== */

.form-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:13px;
}

.field{
  margin-bottom:13px;
}

.field label{
  display:block;
  margin-bottom:7px;
  font-size:13px;
  opacity:.85;
}

.field input,
.field select{
  width:100%;
  padding:14px;
  border:0;
  border-radius:12px;
  font-size:16px;
  outline:none;
}

.full{
  grid-column:1/-1;
}


/* =====================================================
   RESULT
===================================================== */

.exchange-result{
  margin-top:15px;
  padding:18px;
  background:rgba(255,255,255,.08);
  border-radius:15px;
  text-align:center;
  line-height:2;
  font-size:17px;
}

.result-big{
  font-size:22px;
  font-weight:bold;
  color:#00e676;
}


/* =====================================================
   PRIMARY BUTTON
===================================================== */

.primary{
  width:100%;
  padding:15px;
  border:0;
  border-radius:13px;
  background:#2196f3;
  color:white;
  font-size:18px;
  font-weight:bold;
  cursor:pointer;
}

.primary:hover{
  filter:brightness(1.1);
}


/* =====================================================
   DEPOSIT BOX
===================================================== */

.deposit-box{
  display:none;
  margin-top:18px;
  background:#fff;
  color:#111;
  padding:18px;
  border-radius:16px;
}

.deposit-address{
  direction:ltr;
  word-break:break-all;
  background:#eee;
  padding:13px;
  border-radius:10px;
  margin:10px 0;
  font-family:monospace;
}

.copy-btn{
  background:#111;
  color:#fff;
  border:0;
  border-radius:10px;
  padding:11px 15px;
  cursor:pointer;
}


/* =====================================================
   TRACK
===================================================== */

.track-input{
  display:flex;
  gap:10px;
}

.track-input input{
  flex:1;
  padding:14px;
  border:0;
  border-radius:12px;
  font-size:16px;
}

.track-result{
  margin-top:15px;
  display:none;
  background:#fff;
  color:#111;
  border-radius:15px;
  padding:18px;
  line-height:2;
}

.status{
  display:inline-block;
  padding:6px 12px;
  border-radius:20px;
  font-weight:bold;
}

.status-pending{
  background:#fff3cd;
  color:#856404;
}

.status-received{
  background:#cce5ff;
  color:#004085;
}

.status-completed{
  background:#d4edda;
  color:#155724;
}

.status-cancelled{
  background:#f8d7da;
  color:#721c24;
}


/* =====================================================
   TXID
===================================================== */

.txid-row{
  display:flex;
  gap:8px;
  margin-top:10px;
}

.txid-row input{
  flex:1;
  padding:12px;
  border:1px solid #ddd;
  border-radius:10px;
  direction:ltr;
}


/* =====================================================
   SETTINGS
===================================================== */

.settings-btn{
  position:fixed;
  left:15px;
  bottom:15px;
  width:55px;
  height:55px;
  border-radius:50%;
  border:0;
  background:#111;
  color:#fff;
  font-size:25px;
  cursor:pointer;
  z-index:500;
  box-shadow:0 4px 15px rgba(0,0,0,.35);
}


/* =====================================================
   MODAL
===================================================== */

.modal{
  display:none;
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.75);
  z-index:1000;
  overflow:auto;
  padding:25px 10px;
}

.modal-box{
  width:96%;
  max-width:1000px;
  margin:20px auto;
  background:#fff;
  color:#111;
  border-radius:20px;
  padding:22px;
}

.modal-title{
  font-size:23px;
  font-weight:bold;
  margin-bottom:18px;
}

.close{
  float:left;
  background:#e53935;
  color:#fff;
  border:0;
  border-radius:9px;
  padding:8px 13px;
  cursor:pointer;
}


/* =====================================================
   THEME
===================================================== */

.theme-grid{
  display:grid;
  grid-template-columns:
    repeat(auto-fit,minmax(100px,1fr));
  gap:10px;
}

.theme-grid button{
  padding:15px;
  border:0;
  border-radius:12px;
  cursor:pointer;
  font-weight:bold;
}

.theme-green{
  background:#16a34a;
  color:#fff;
}

.theme-yellow{
  background:#ffd600;
}

.theme-orange{
  background:#ff9800;
}

.theme-blue{
  background:#1976d2;
  color:#fff;
}

.theme-black{
  background:#111;
  color:#fff;
}


/* =====================================================
   ADMIN
===================================================== */

.admin-stats{
  display:grid;
  grid-template-columns:
    repeat(3,1fr);
  gap:10px;
  margin-bottom:20px;
}

.stat{
  background:#111;
  color:#fff;
  padding:15px;
  text-align:center;
  border-radius:13px;
}

.stat-number{
  display:block;
  font-size:25px;
  font-weight:bold;
  margin-top:5px;
}

.admin-table-wrap{
  overflow-x:auto;
}

.admin-table{
  width:100%;
  border-collapse:collapse;
  min-width:900px;
}

.admin-table th,
.admin-table td{
  border:1px solid #ddd;
  padding:8px;
  text-align:center;
  font-size:12px;
}

.admin-table th{
  background:#111;
  color:#fff;
}

.admin-actions{
  display:flex;
  gap:5px;
  flex-wrap:wrap;
}

.admin-actions button{
  border:0;
  border-radius:7px;
  padding:6px 8px;
  cursor:pointer;
  font-size:11px;
}

.btn-green{
  background:#00c853;
  color:#fff;
}

.btn-blue{
  background:#1976d2;
  color:#fff;
}

.btn-red{
  background:#e53935;
  color:#fff;
}

.btn-gray{
  background:#555;
  color:#fff;
}


/* =====================================================
   LOGIN
===================================================== */

.login-box{
  max-width:420px;
  margin:70px auto;
}

.login-box input{
  width:100%;
  padding:14px;
  border:1px solid #ddd;
  border-radius:10px;
  margin:10px 0;
  font-size:17px;
}


/* =====================================================
   FOOTER
===================================================== */

footer{
  text-align:center;
  padding:25px;
  font-size:12px;
  opacity:.7;
}


/* =====================================================
   MOBILE
===================================================== */

@media(max-width:650px){

  .form-grid{
    grid-template-columns:1fr;
  }

  .full{
    grid-column:auto;
  }

  .trade-buttons{
    grid-template-columns:1fr 1fr;
  }

  .trade-buttons button{
    font-size:18px;
  }

  .admin-stats{
    grid-template-columns:1fr;
  }

  .track-input{
    flex-direction:column;
  }

}

</style>

</head>


<body>


<!-- =====================================================
 HEADER
===================================================== -->

<header>

  <div class="logo">💡</div>

  <div class="header-title">
    صرافی تبادل ارز
  </div>

  <div class="header-sub">
    تبادل مستقیم ارزهای دیجیتال
  </div>

</header>


<div class="container">


<!-- =====================================================
 LIVE STATUS
===================================================== -->

<div class="live-status"
     id="priceStatus">

  🟡 در حال دریافت قیمت آنلاین از CoinMarketCap...

</div>


<!-- =====================================================
 COINS
===================================================== -->

<div class="coin-grid">


  <div class="coin-card">

    <div class="coin-led"></div>

    <div class="coin-name">
      Bitcoin BTC
    </div>

    <div class="coin-price"
         id="price-btc">
      ---
    </div>

    <div class="coin-time"
         id="time-btc">
      ---
    </div>

  </div>


  <div class="coin-card">

    <div class="coin-led"></div>

    <div class="coin-name">
      Litecoin LTC
    </div>

    <div class="coin-price"
         id="price-ltc">
      ---
    </div>

    <div class="coin-time"
         id="time-ltc">
      ---
    </div>

  </div>


  <div class="coin-card">

    <div class="coin-led"></div>

    <div class="coin-name">
      Bitcoin Cash BCH
    </div>

    <div class="coin-price"
         id="price-bch">
      ---
    </div>

    <div class="coin-time"
         id="time-bch">
      ---
    </div>

  </div>


  <div class="coin-card">

    <div class="coin-led"></div>

    <div class="coin-name">
      Dogecoin DOGE
    </div>

    <div class="coin-price"
         id="price-doge">
      ---
    </div>

    <div class="coin-time"
         id="time-doge">
      ---
    </div>

  </div>


  <div class="coin-card">

    <div class="coin-led"></div>

    <div class="coin-name">
      Tether USDT
    </div>

    <div class="coin-price"
         id="price-usdt">
      ---
    </div>

    <div class="coin-time"
         id="time-usdt">
      ---
    </div>

  </div>


  <div class="coin-card">

    <div class="coin-led"></div>

    <div class="coin-name">
      TRON TRX
    </div>

    <div class="coin-price"
         id="price-trx">
      ---
    </div>

    <div class="coin-time"
         id="time-trx">
      ---
    </div>

  </div>


</div>


<!-- =====================================================
 EXCHANGE
===================================================== -->

<div class="panel">

  <div class="panel-title">
    🔄 تبادل ارز
  </div>


  <div class="trade-buttons">

    <button
      id="buyButton"
      class="buy-btn active"
      onclick="setTradeType('BUY')">

      🟢 خرید

    </button>


    <button
      id="sellButton"
      class="sell-btn"
      onclick="setTradeType('SELL')">

      🟠 فروش

    </button>

  </div>


  <div class="form-grid">


    <div class="field">

      <label>
        ارز مبدا
      </label>

      <select id="fromCoin"
              onchange="calculateExchange()">

        <option value="btc">
          BTC - Bitcoin
        </option>

        <option value="ltc">
          LTC - Litecoin
        </option>

        <option value="bch">
          BCH - Bitcoin Cash
        </option>

        <option value="doge">
          DOGE - Dogecoin
        </option>

        <option value="usdt">
          USDT - Tether
        </option>

        <option value="trx">
          TRX - TRON
        </option>

      </select>

    </div>


    <div class="field">

      <label>
        ارز مقصد
      </label>

      <select id="toCoin"
              onchange="calculateExchange()">

        <option value="usdt">
          USDT - Tether
        </option>

        <option value="btc">
          BTC - Bitcoin
        </option>

        <option value="ltc">
          LTC - Litecoin
        </option>

        <option value="bch">
          BCH - Bitcoin Cash
        </option>

        <option value="doge">
          DOGE - Dogecoin
        </option>

        <option value="trx">
          TRX - TRON
        </option>

      </select>

    </div>


    <div class="field full">

      <label>
        مقدار ارز
      </label>

      <input
        id="exchangeAmount"
        type="number"
        step="any"
        min="0"
        placeholder="مثلاً 0.1"
        oninput="calculateExchange()">

    </div>


    <div class="field full">

      <div class="exchange-result"
           id="exchangeResult">

        مقدار ارز را وارد کنید

      </div>

    </div>


    <div class="field full">

      <label>
        آدرس کیف پول مقصد شما
      </label>

      <input
        id="destinationAddress"
        type="text"
        placeholder="آدرس کیف پولی که می‌خواهید ارز به آن ارسال شود"
        dir="ltr">

    </div>


  </div>


  <button
    class="primary"
    onclick="prepareTrade()">

    ثبت معامله و دریافت آدرس واریز

  </button>


  <!-- DEPOSIT -->

  <div class="deposit-box"
       id="depositBox">

    <h3>
      📥 آدرس واریز
    </h3>

    <p>
      برای ثبت معامله، ارز مبدا را به آدرس زیر ارسال کنید:
    </p>

    <div class="deposit-address"
         id="depositAddress">

    </div>

    <button
      class="copy-btn"
      onclick="copyDepositAddress()">

      📋 کپی آدرس

    </button>


    <div style="margin-top:15px">

      <b>
        کد معامله:
      </b>

      <div id="tradeCodeDisplay"
           style="
             font-size:22px;
             font-weight:bold;
             margin-top:8px;
             direction:ltr;
           ">

      </div>

    </div>


    <div style="margin-top:15px">

      پس از ارسال تراکنش، TXID را می‌توانید در بخش پیگیری ثبت کنید.

    </div>

  </div>


</div>


<!-- =====================================================
 TRACK
===================================================== -->

<div class="panel">

  <div class="panel-title">
    🔎 پیگیری معامله
  </div>


  <div class="track-input">

    <input
      id="trackCode"
      placeholder="کد معامله مثل TB-260930-123456"
      dir="ltr">

    <button
      class="primary"
      onclick="trackTrade()">

      پیگیری

    </button>

  </div>


  <div class="track-result"
       id="trackResult">

  </div>

</div>


</div>


<!-- =====================================================
 SETTINGS BUTTON
===================================================== -->

<button
  class="settings-btn"
  onclick="openSettings()">

  ⚙️

</button>


<!-- =====================================================
 SETTINGS MODAL
===================================================== -->

<div class="modal"
     id="settingsModal">

  <div class="modal-box">

    <button
      class="close"
      onclick="closeModal('settingsModal')">

      ×

    </button>

    <div class="modal-title">
      ⚙️ تنظیمات
    </div>


    <h3>
      رنگ پس‌زمینه
    </h3>


    <div class="theme-grid">

      <button
        class="theme-green"
        onclick="changeTheme('#16a34a')">

        سبز

      </button>


      <button
        class="theme-yellow"
        onclick="changeTheme('#ffd600')">

        زرد

      </button>


      <button
        class="theme-orange"
        onclick="changeTheme('#ff9800')">

        نارنجی

      </button>


      <button
        class="theme-blue"
        onclick="changeTheme('#1976d2')">

        آبی

      </button>


      <button
        class="theme-black"
        onclick="changeTheme('#111')">

        مشکی

      </button>

    </div>


    <hr style="margin:25px 0">


    <button
      class="primary"
      onclick="openAdminLogin()">

      🔐 ورود به پنل مدیریت

    </button>

  </div>

</div>


<!-- =====================================================
 ADMIN LOGIN
===================================================== -->

<div class="modal"
     id="loginModal">

  <div class="modal-box login-box">

    <button
      class="close"
      onclick="closeModal('loginModal')">

      ×

    </button>

    <div class="modal-title">
      🔐 ورود مدیریت
    </div>


    <input
      id="adminPassword"
      type="password"
      placeholder="رمز مدیریت">


    <button
      class="primary"
      onclick="adminLogin()">

      ورود

    </button>


    <div id="loginError"
         style="
           color:red;
           text-align:center;
           margin-top:12px;
         ">

    </div>

  </div>

</div>


<!-- =====================================================
 ADMIN PANEL
===================================================== -->

<div class="modal"
     id="adminModal">

  <div class="modal-box">

    <button
      class="close"
      onclick="closeModal('adminModal')">

      خروج

    </button>


    <div class="modal-title">
      🛠 پنل مدیریت صرافی تبادل
    </div>


    <div class="admin-stats">

      <div class="stat">

        کل معاملات

        <span
          class="stat-number"
          id="statTotal">

          0

        </span>

      </div>


      <div class="stat">

        در انتظار

        <span
          class="stat-number"
          id="statPending">

          0

        </span>

      </div>


      <div class="stat">

        تکمیل شده

        <span
          class="stat-number"
          id="statCompleted">

          0

        </span>

      </div>

    </div>


    <div class="admin-table-wrap">

      <table class="admin-table">

        <thead>

          <tr>

            <th>
              کد
            </th>

            <th>
              نوع
            </th>

            <th>
              مبدا
            </th>

            <th>
              مقدار
            </th>

            <th>
              مقصد
            </th>

            <th>
              دریافتی
            </th>

            <th>
              آدرس کاربر
            </th>

            <th>
              آدرس واریز
            </th>

            <th>
              TXID
            </th>

            <th>
              وضعیت
            </th>

            <th>
              عملیات
            </th>

          </tr>

        </thead>

        <tbody id="adminTableBody">

        </tbody>

      </table>

    </div>

  </div>

</div>


<footer>

  صرافی تبادل — Crypto Exchange

  <br>

  نرخ بازار از CoinMarketCap

</footer>


<script>

/* =====================================================
   TABADOL COMPLETE JAVASCRIPT
===================================================== */

"use strict";


/* =====================================================
   CONFIG
===================================================== */

const ADMIN_PASSWORD =
  "Admin321";


const STORAGE_KEY =
  "TABADOL_TRANSACTIONS_FINAL_V1";


const FEE =
  0.01;


/* =====================================================
   COINS
===================================================== */

const COINS = {

  btc:{
    symbol:"BTC",
    name:"Bitcoin",
    cmcId:1,
    address:"1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV"
  },

  ltc:{
    symbol:"LTC",
    name:"Litecoin",
    cmcId:2,
    address:"LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c"
  },

  bch:{
    symbol:"BCH",
    name:"Bitcoin Cash",
    cmcId:1831,
    address:"bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku"
  },

  doge:{
    symbol:"DOGE",
    name:"Dogecoin",
    cmcId:74,
    address:"DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk"
  },

  usdt:{
    symbol:"USDT",
    name:"USDT BEP-20",
    cmcId:825,
    address:"0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6"
  },

  trx:{
    symbol:"TRX",
    name:"TRON",
    cmcId:1958,
    address:"TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"
  }

};


/* =====================================================
   PRICE DATA
===================================================== */

let livePrices = {};

let tradeType = "BUY";


/* =====================================================
   COINMARKETCAP KEYLESS API
===================================================== */

const CMC_URL =
  "https://pro-api.coinmarketcap.com/public-api/v1/cryptocurrency/quotes/latest" +
  "?id=1,2,1831,74,825,1958&convert=USD";


/* =====================================================
   STORAGE
===================================================== */

function getTrades(){

  try{

    const data =
      localStorage.getItem(
        STORAGE_KEY
      );

    if(!data){
      return [];
    }

    const parsed =
      JSON.parse(data);

    return Array.isArray(parsed)
      ? parsed
      : [];

  }
  catch(e){

    console.error(e);

    return [];

  }

}


function saveTrades(trades){

  localStorage.setItem(
    STORAGE_KEY,
    JSON.stringify(trades)
  );

}


/* =====================================================
   PRICE FORMAT
===================================================== */

function formatUSD(value){

  if(
    value === undefined ||
    value === null ||
    !isFinite(value)
  ){

    return "---";

  }


  if(value >= 1000){

    return "$" +
      value.toLocaleString(
        "en-US",
        {
          minimumFractionDigits:2,
          maximumFractionDigits:2
        }
      );

  }


  if(value >= 1){

    return "$" +
      value.toLocaleString(
        "en-US",
        {
          minimumFractionDigits:2,
          maximumFractionDigits:8
        }
      );

  }


  return "$" +
    value.toLocaleString(
      "en-US",
      {
        minimumFractionDigits:4,
        maximumFractionDigits:10
      }
    );

}


function formatNumber(value){

  if(!isFinite(value)){
    return "---";
  }

  return value.toLocaleString(
    "en-US",
    {
      maximumFractionDigits:8
    }
  );

}


/* =====================================================
   GET LIVE PRICE
===================================================== */

function getPrice(symbol){

  const coin =
    COINS[symbol];

  if(!coin){
    return null;
  }

  const item =
    livePrices[coin.cmcId];

  if(!item){
    return null;
  }

  if(
    !item.quote ||
    !item.quote.USD
  ){

    return null;

  }

  return item.quote.USD.price;

}


/* =====================================================
   LOAD LIVE PRICES
===================================================== */

async function loadPrices(){

  const status =
    document.getElementById(
      "priceStatus"
    );


  status.innerHTML =
    "🟡 دریافت قیمت آنلاین از CoinMarketCap...";


  try{

    const controller =
      new AbortController();


    const timeout =
      setTimeout(
        function(){

          controller.abort();

        },
        15000
      );


    const response =
      await fetch(
        CMC_URL,
        {
          method:"GET",
          cache:"no-store",
          signal:controller.signal,
          headers:{
            "Accept":"application/json"
          }
        }
      );


    clearTimeout(timeout);


    if(!response.ok){

      throw new Error(
        "HTTP " +
        response.status
      );

    }


    const json =
      await response.json();


    if(
      !json.data ||
      !json.status
    ){

      throw new Error(
        "Invalid CMC response"
      );

    }


    if(
      json.status.error_code &&
      json.status.error_code !== 0
    ){

      throw new Error(
        json.status.error_message ||
        "CoinMarketCap API error"
      );

    }


    livePrices =
      json.data;


    renderPrices();

    calculateExchange();


    status.innerHTML =
      "🟢 قیمت آنلاین فعال است — CoinMarketCap — " +
      new Date().toLocaleTimeString();


  }
  catch(error){

    console.error(
      "CoinMarketCap error:",
      error
    );


    status.innerHTML =
      "🔴 دریافت قیمت آنلاین ناموفق بود — تلاش مجدد خودکار فعال است";

  }

}


/* =====================================================
   RENDER PRICES
===================================================== */

function renderPrices(){

  Object.keys(COINS)
    .forEach(
      function(symbol){

        const price =
          getPrice(symbol);


        const priceElement =
          document.getElementById(
            "price-" + symbol
          );


        const timeElement =
          document.getElementById(
            "time-" + symbol
          );


        if(priceElement){

          priceElement.textContent =
            formatUSD(price);

        }


        if(
          timeElement &&
          livePrices[
            COINS[symbol].cmcId
          ]
        ){

          const updated =
            livePrices[
              COINS[symbol].cmcId
            ].last_updated;


          if(updated){

            timeElement.textContent =
              new Date(
                updated
              ).toLocaleTimeString();

          }

        }

      }
    );

}


/* =====================================================
   TRADE TYPE
===================================================== */

function setTradeType(type){

  tradeType =
    type;


  const buy =
    document.getElementById(
      "buyButton"
    );


  const sell =
    document.getElementById(
      "sellButton"
    );


  buy.classList.remove(
    "active"
  );


  sell.classList.remove(
    "active"
  );


  if(type === "BUY"){

    buy.classList.add(
      "active"
    );

  }
  else{

    sell.classList.add(
      "active"
    );

  }


  calculateExchange();

}


/* =====================================================
   CALCULATE EXCHANGE
===================================================== */

function calculateExchange(){

  const from =
    document.getElementById(
      "fromCoin"
    ).value;


  const to =
    document.getElementById(
      "toCoin"
    ).value;


  const amount =
    parseFloat(
      document.getElementById(
        "exchangeAmount"
      ).value
    );


  const result =
    document.getElementById(
      "exchangeResult"
    );


  if(
    !amount ||
    amount <= 0
  ){

    result.innerHTML =
      "مقدار ارز را وارد کنید";

    return;

  }


  const fromPrice =
    getPrice(from);


  const toPrice =
    getPrice(to);


  if(
    fromPrice === null ||
    toPrice === null
  ){

    result.innerHTML =
      "🟡 در حال دریافت قیمت آنلاین...";

    return;

  }


  /*
     ارزش دلاری ارز ورودی
  */

  const dollarValue =
    amount *
    fromPrice;


  /*
     مقدار مقصد قبل از کارمزد
  */

  const beforeFee =
    dollarValue /
    toPrice;


  /*
     فقط 1 درصد کارمزد
  */

  const fee =
    beforeFee *
    FEE;


  /*
     مقدار نهایی
  */

  const finalAmount =
    beforeFee -
    fee;


  result.innerHTML =

    "<div>" +

    (tradeType === "BUY"
      ? "🟢 <b>خرید</b>"
      : "🟠 <b>فروش</b>") +

    "</div>" +

    "<div>" +

    formatNumber(amount) +
    " " +
    COINS[from].symbol +

    " ≈ " +

    "<span class='result-big'>" +

    formatNumber(
      finalAmount
    ) +

    " " +
    COINS[to].symbol +

    "</span>" +

    "</div>" +

    "<div>" +

    "قیمت بازار " +
    COINS[from].symbol +
    ": " +
    "<b>" +
    formatUSD(fromPrice) +
    "</b>" +

    "</div>" +

    "<div>" +

    "قیمت بازار " +
    COINS[to].symbol +
    ": " +
    "<b>" +
    formatUSD(toPrice) +
    "</b>" +

    "</div>" +

    "<div>" +

    "کارمزد سایت: <b>1%</b>" +

    " — " +

    formatNumber(fee) +
    " " +
    COINS[to].symbol +

    "</div>";

}


/* =====================================================
   PREPARE TRADE
===================================================== */

function prepareTrade(){

  const from =
    document.getElementById(
      "fromCoin"
    ).value;


  const to =
    document.getElementById(
      "toCoin"
    ).value;


  const amount =
    parseFloat(
      document.getElementById(
        "exchangeAmount"
      ).value
    );


  const destination =
    document.getElementById(
      "destinationAddress"
    ).value.trim();


  if(
    !amount ||
    amount <= 0
  ){

    alert(
      "مقدار ارز را وارد کنید"
    );

    return;

  }


  if(!destination){

    alert(
      "آدرس کیف پول مقصد را وارد کنید"
    );

    return;

  }


  if(
    from === to
  ){

    alert(
      "ارز مبدا و مقصد نباید یکسان باشند"
    );

    return;

  }


  const fromPrice =
    getPrice(from);


  const toPrice =
    getPrice(to);


  if(
    fromPrice === null ||
    toPrice === null
  ){

    alert(
      "قیمت آنلاین هنوز دریافت نشده است"
    );

    return;

  }


  const beforeFee =
    (
      amount *
      fromPrice
    ) /
    toPrice;


  const fee =
    beforeFee *
    FEE;


  const finalAmount =
    beforeFee -
    fee;


  const code =
    generateTradeCode();


  const trade = {

    id:code,

    type:tradeType,

    from:from,

    fromAmount:amount,

    to:to,

    toAmount:finalAmount,

    fee:fee,

    fromPrice:fromPrice,

    toPrice:toPrice,

    destinationAddress:destination,

    depositAddress:
      COINS[from].address,

    txid:"",

    status:"در انتظار واریز",

    createdAt:
      new Date().toISOString(),

    updatedAt:
      new Date().toISOString()

  };


  const trades =
    getTrades();


  trades.unshift(
    trade
  );


  saveTrades(
    trades
  );


  document.getElementById(
    "depositAddress"
  ).textContent =
    COINS[from].address;


  document.getElementById(
    "tradeCodeDisplay"
  ).textContent =
    code;


  document.getElementById(
    "depositBox"
  ).style.display =
    "block";


  alert(
    "معامله ثبت شد\nکد معامله: " +
    code
  );


}


/* =====================================================
   TRADE CODE
===================================================== */

function generateTradeCode(){

  const d =
    new Date();


  const date =
    String(
      d.getFullYear()
    ).slice(-2) +

    String(
      d.getMonth()+1
    ).padStart(2,"0") +

    String(
      d.getDate()
    ).padStart(2,"0");


  const random =
    Math.floor(
      100000 +
      Math.random()*900000
    );


  return(
    "TB-" +
    date +
    "-" +
    random
  );

}


/* =====================================================
   COPY DEPOSIT
===================================================== */

function copyDepositAddress(){

  const address =
    document.getElementById(
      "depositAddress"
    ).textContent;


  navigator.clipboard
    .writeText(address)
    .then(
      function(){

        alert(
          "آدرس کپی شد"
        );

      }
    )
    .catch(
      function(){

        alert(
          "کپی خودکار انجام نشد؛ آدرس را دستی کپی کنید"
        );

      }
    );

}


/* =====================================================
   MASK
===================================================== */

function maskText(value){

  if(!value){
    return "---";
  }


  if(value.length <= 12){

    return value;

  }


  return(
    value.substring(0,6) +
    "••••••••••" +
    value.substring(
      value.length-6
    )
  );

}


/* =====================================================
   TRACK TRADE
===================================================== */

function trackTrade(){

  const code =
    document.getElementById(
      "trackCode"
    ).value
    .trim()
    .toUpperCase();


  const result =
    document.getElementById(
      "trackResult"
    );


  const trades =
    getTrades();


  const trade =
    trades.find(
      function(t){

        return(
          t.id.toUpperCase() ===
          code
        );

      }
    );


  if(!trade){

    result.style.display =
      "block";

    result.innerHTML =
      "❌ معامله‌ای با این کد پیدا نشد";

    return;

  }


  let statusClass =
    "status-pending";


  if(
    trade.status ===
    "دریافت شد"
  ){

    statusClass =
      "status-received";

  }


  if(
    trade.status ===
    "تکمیل شد"
  ){

    statusClass =
      "status-completed";

  }


  if(
    trade.status ===
    "لغو شد"
  ){

    statusClass =
      "status-cancelled";

  }


  result.style.display =
    "block";


  result.innerHTML =

    "<b>کد معامله:</b> " +
    trade.id +

    "<br>" +

    "<b>نوع:</b> " +
    trade.type +

    "<br>" +

    "<b>مبادله:</b> " +
    COINS[trade.from].symbol +
    " → " +
    COINS[trade.to].symbol +

    "<br>" +

    "<b>مقدار:</b> " +
    formatNumber(
      trade.fromAmount
    ) +
    " " +
    COINS[trade.from].symbol +

    "<br>" +

    "<b>مقدار دریافتی:</b> " +
    formatNumber(
      trade.toAmount
    ) +
    " " +
    COINS[trade.to].symbol +

    "<br>" +

    "<b>آدرس مقصد:</b> " +
    maskText(
      trade.destinationAddress
    ) +

    "<br>" +

    "<b>TXID:</b> " +
    maskText(
      trade.txid
    ) +

    "<br>" +

    "<b>وضعیت:</b> " +

    "<span class='status " +
    statusClass +
    "'>" +

    trade.status +

    "</span>" +

    "<br><br>" +

    "<div class='txid-row'>" +

    "<input " +
    "id='txid-" +
    trade.id +
    "' " +
    "placeholder='TXID تراکنش را وارد کنید' " +
    "dir='ltr'>" +

    "<button " +
    "class='copy-btn' " +
    "onclick=\"saveTXID('" +
    trade.id +
    "')\">" +

    "ثبت TXID" +

    "</button>" +

    "</div>";

}


/* =====================================================
   SAVE TXID
===================================================== */

function saveTXID(code){

  const input =
    document.getElementById(
      "txid-" + code
    );


  if(!input){
    return;
  }


  const txid =
    input.value.trim();


  if(!txid){

    alert(
      "TXID را وارد کنید"
    );

    return;

  }


  const trades =
    getTrades();


  const index =
    trades.findIndex(
      function(t){

        return t.id === code;

      }
    );


  if(index === -1){

    alert(
      "معامله پیدا نشد"
    );

    return;

  }


  trades[index].txid =
    txid;


  trades[index].status =
    "دریافت شد";


  trades[index].updatedAt =
    new Date().toISOString();


  saveTrades(
    trades
  );


  alert(
    "TXID ثبت شد"
  );


  trackTrade();

}


/* =====================================================
   SETTINGS
===================================================== */

function openSettings(){

  document.getElementById(
    "settingsModal"
  ).style.display =
    "block";

}


function openAdminLogin(){

  closeModal(
    "settingsModal"
  );


  document.getElementById(
    "loginModal"
  ).style.display =
    "block";

}


function closeModal(id){

  document.getElementById(
    id
  ).style.display =
    "none";

}


/* =====================================================
   THEME
===================================================== */

function changeTheme(color){

  document.documentElement
    .style.setProperty(
      "--bg",
      color
    );


  localStorage.setItem(
    "TABADOL_THEME",
    color
  );

}


function loadTheme(){

  const theme =
    localStorage.getItem(
      "TABADOL_THEME"
    );


  if(theme){

    document.documentElement
      .style.setProperty(
        "--bg",
        theme
      );

  }

}


/* =====================================================
   ADMIN LOGIN
===================================================== */

function adminLogin(){

  const password =
    document.getElementById(
      "adminPassword"
    ).value;


  const error =
    document.getElementById(
      "loginError"
    );


  if(
    password !==
    ADMIN_PASSWORD
  ){

    error.textContent =
      "رمز مدیریت اشتباه است";

    return;

  }


  error.textContent =
    "";


  document.getElementById(
    "adminPassword"
  ).value =
    "";


  closeModal(
    "loginModal"
  );


  document.getElementById(
    "adminModal"
  ).style.display =
    "block";


  renderAdmin();

}


/* =====================================================
   ADMIN RENDER
===================================================== */

function renderAdmin(){

  const trades =
    getTrades();


  const total =
    trades.length;


  const pending =
    trades.filter(
      function(t){

        return(
          t.status ===
          "در انتظار واریز"
        );

      }
    ).length;


  const completed =
    trades.filter(
      function(t){

        return(
          t.status ===
          "تکمیل شد"
        );

      }
    ).length;


  document.getElementById(
    "statTotal"
  ).textContent =
    total;


  document.getElementById(
    "statPending"
  ).textContent =
    pending;


  document.getElementById(
    "statCompleted"
  ).textContent =
    completed;


  const body =
    document.getElementById(
      "adminTableBody"
    );


  if(!trades.length){

    body.innerHTML =
      "<tr>" +
      "<td colspan='11'>" +
      "هنوز معامله‌ای ثبت نشده است" +
      "</td>" +
      "</tr>";

    return;

  }


  body.innerHTML =
    trades.map(
      function(t){

        return `

<tr>

<td dir="ltr">
${t.id}
</td>

<td>
${t.type}
</td>

<td>
${COINS[t.from].symbol}
</td>

<td>
${formatNumber(t.fromAmount)}
</td>

<td>
${COINS[t.to].symbol}
</td>

<td>
${formatNumber(t.toAmount)}
</td>

<td dir="ltr"
    style="max-width:160px;word-break:break-all">
${t.destinationAddress}
</td>

<td dir="ltr"
    style="max-width:160px;word-break:break-all">
${t.depositAddress}
</td>

<td dir="ltr"
    style="max-width:180px;word-break:break-all">
${t.txid || "---"}
</td>

<td>
${t.status}
</td>

<td>

<div class="admin-actions">

<button
class="btn-green"
onclick="changeStatus('${t.id}','تکمیل شد')">

تکمیل

</button>

<button
class="btn-blue"
onclick="changeStatus('${t.id}','دریافت شد')">

دریافت

</button>

<button
class="btn-gray"
onclick="changeStatus('${t.id}','در انتظار واریز')">

انتظار

</button>

<button
class="btn-red"
onclick="changeStatus('${t.id}','لغو شد')">

لغو

</button>

<button
class="btn-red"
onclick="deleteTrade('${t.id}')">

حذف

</button>

</div>

</td>

</tr>

`;

      }
    )
    .join("");

}


/* =====================================================
   CHANGE STATUS
===================================================== */

function changeStatus(
  code,
  newStatus
){

  const trades =
    getTrades();


  const index =
    trades.findIndex(
      function(t){

        return(
          t.id === code
        );

      }
    );


  if(index === -1){
    return;
  }


  trades[index].status =
    newStatus;


  trades[index].updatedAt =
    new Date().toISOString();


  saveTrades(
    trades
  );


  renderAdmin();

}


/* =====================================================
   DELETE
===================================================== */

function deleteTrade(code){

  if(
    !confirm(
      "این معامله حذف شود؟"
    )
  ){

    return;

  }


  const trades =
    getTrades();


  const filtered =
    trades.filter(
      function(t){

        return(
          t.id !== code
        );

      }
    );


  saveTrades(
    filtered
  );


  renderAdmin();

}


/* =====================================================
   CLOSE MODAL BY CLICK OUTSIDE
===================================================== */

document
.addEventListener(
  "click",
  function(event){

    if(
      event.target.classList
        .contains("modal")
    ){

      event.target.style.display =
        "none";

    }

  }
);


/* =====================================================
   START
===================================================== */

loadTheme();

loadPrices();


/*
   قیمت‌ها هر 60 ثانیه
   مجدداً از CoinMarketCap گرفته می‌شوند.
*/

setInterval(
  loadPrices,
  60000
);


/* =====================================================
   EXPOSE PRICE DATA
===================================================== */

window.TABADOL_GET_PRICE =
function(symbol){

  return getPrice(symbol);

};


window.TABADOL_GET_ALL_PRICES =
function(){

  return livePrices;

};


</script>


</body>

</html>
