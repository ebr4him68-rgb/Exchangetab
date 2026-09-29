# Exchangetab

<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>صرافی تبادل ارز | تبادل</title>

<style>
*{box-sizing:border-box}

body{
    margin:0;
    font-family:Tahoma,Arial,sans-serif;
    color:#171717;
    background:
      radial-gradient(circle at 10% 10%,#fff8ad 0,transparent 30%),
      radial-gradient(circle at 90% 90%,#ffda29 0,transparent 35%),
      linear-gradient(135deg,#eab800,#ffe66b);
    min-height:100vh;
}

.container{
    width:94%;
    max-width:1050px;
    margin:auto;
    padding:22px 0 50px;
}

/* HEADER */

.header{
    text-align:center;
    padding:20px 10px 25px;
}

.logo{
    display:inline-flex;
    align-items:center;
    gap:12px;
    direction:rtl;
}

.fire{
    position:relative;
    width:64px;
    height:78px;
}

.flame{
    position:absolute;
    width:55px;
    height:68px;
    bottom:0;
    left:4px;
    background:linear-gradient(145deg,#ff5b00,#ffb300 70%,#ffe66b);
    border-radius:55% 45% 55% 45%;
    transform:rotate(-8deg);
    box-shadow:0 0 25px rgba(255,104,0,.65);
}

.flame:before{
    content:"";
    position:absolute;
    width:32px;
    height:42px;
    background:#ffe66b;
    left:12px;
    bottom:8px;
    border-radius:50% 50% 45% 45%;
}

.bulb{
    position:absolute;
    z-index:3;
    width:29px;
    height:29px;
    border-radius:50%;
    background:#fff;
    left:17px;
    top:17px;
    box-shadow:
      0 0 8px #fff,
      0 0 18px #fff,
      0 0 30px #ffd21a;
}

.bulb:after{
    content:"";
    position:absolute;
    width:16px;
    height:10px;
    background:#333;
    left:6px;
    top:25px;
    border-radius:0 0 5px 5px;
}

.brand{
    font-size:44px;
    font-weight:1000;
    letter-spacing:-2px;
}

.brand small{
    display:block;
    font-size:14px;
    letter-spacing:0;
    margin-top:3px;
    color:#444;
}

.header h1{
    margin:15px 0 5px;
    font-size:27px;
    font-weight:900;
}

.header p{
    margin:0;
    color:#555;
    font-size:13px;
}

/* COINS */

.coins{
    display:grid;
    grid-template-columns:repeat(6,1fr);
    gap:9px;
    margin-bottom:20px;
}

.coin{
    background:rgba(255,255,255,.91);
    border:1px solid rgba(0,0,0,.12);
    border-radius:17px;
    padding:13px 6px;
    text-align:center;
    box-shadow:0 5px 18px rgba(0,0,0,.09);
}

.led{
    display:inline-block;
    width:9px;
    height:9px;
    border-radius:50%;
    background:#16c45a;
    margin-left:4px;
    box-shadow:0 0 9px #16c45a;
    animation:blink 1s infinite;
}

@keyframes blink{
    0%,100%{opacity:1}
    50%{opacity:.25}
}

.coin b{
    font-size:15px;
}

.coin-price{
    margin-top:6px;
    font-size:11px;
    color:#555;
    direction:ltr;
}

/* MAIN */

.card{
    background:rgba(255,255,255,.97);
    border-radius:25px;
    padding:24px;
    box-shadow:0 18px 50px rgba(0,0,0,.2);
}

.title{
    text-align:center;
    font-size:23px;
    font-weight:900;
    margin-bottom:20px;
}

.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:14px;
}

label{
    display:block;
    font-size:13px;
    font-weight:bold;
    margin-bottom:7px;
}

input,select{
    width:100%;
    padding:14px;
    border:1px solid #ccc;
    border-radius:13px;
    background:#fff;
    font-size:16px;
    outline:none;
}

input:focus,select:focus{
    border-color:#e4b900;
    box-shadow:0 0 0 3px rgba(245,196,0,.2);
}

.field{
    margin-top:14px;
}

.result{
    margin-top:17px;
    background:#fff8ce;
    border:1px solid #e1c33c;
    border-radius:15px;
    padding:15px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:10px;
}

.result strong{
    direction:ltr;
    font-size:19px;
}

.rate{
    margin-top:9px;
    text-align:center;
    font-size:11px;
    color:#777;
}

.button{
    width:100%;
    border:0;
    border-radius:14px;
    margin-top:19px;
    padding:16px;
    background:#111;
    color:#fff;
    font-size:17px;
    font-weight:900;
    cursor:pointer;
}

.button:hover{
    background:#252525;
}

/* DEPOSIT */

.message{
    display:none;
    margin-top:15px;
    padding:13px;
    border-radius:12px;
    background:#f2f2f2;
    font-size:13px;
    line-height:1.8;
}

.deposit{
    display:none;
    margin-top:18px;
    background:#151515;
    color:#fff;
    border-radius:18px;
    padding:19px;
}

.deposit h3{
    color:#ffd21a;
    margin:0 0 9px;
}

.deposit-address{
    background:#fff;
    color:#111;
    padding:14px;
    border-radius:10px;
    margin-top:10px;
    direction:ltr;
    text-align:left;
    word-break:break-all;
    font-family:monospace;
}

.copy{
    width:100%;
    border:0;
    border-radius:10px;
    margin-top:10px;
    padding:13px;
    background:#16a34a;
    color:#fff;
    font-weight:bold;
    cursor:pointer;
}

.warning{
    color:#ffd86b;
    font-size:11px;
    line-height:1.8;
    margin-top:11px;
}

.trade-id{
    color:#aaa;
    font-size:11px;
    margin-top:9px;
}

/* FOOTER */

.footer{
    text-align:center;
    margin-top:18px;
    font-size:11px;
    color:#555;
}

@media(max-width:760px){
    .coins{
        grid-template-columns:repeat(3,1fr);
    }

    .grid{
        grid-template-columns:1fr;
    }

    .brand{
        font-size:37px;
    }
}

@media(max-width:430px){
    .coins{
        grid-template-columns:repeat(2,1fr);
    }

    .card{
        padding:17px;
    }
}
</style>
</head>

<body>

<div class="container">

<header class="header">

    <div class="logo">

        <div class="fire">
            <div class="flame"></div>
            <div class="bulb"></div>
        </div>

        <div class="brand">
            تبادل
            <small>TA B A D O L</small>
        </div>

    </div>

    <h1>صرافی تبادل ارز</h1>

    <p>تبادل مستقیم رمزارز به رمزارز</p>

</header>


<!-- ارزها -->

<section class="coins">

    <div class="coin">
        <span class="led"></span>
        <b>BTC</b>
        <div class="coin-price" id="BTCprice">$65,000</div>
    </div>

    <div class="coin">
        <span class="led"></span>
        <b>LTC</b>
        <div class="coin-price" id="LTCprice">$70</div>
    </div>

    <div class="coin">
        <span class="led"></span>
        <b>BCH</b>
        <div class="coin-price" id="BCHprice">$520</div>
    </div>

    <div class="coin">
        <span class="led"></span>
        <b>DOGE</b>
        <div class="coin-price" id="DOGEprice">$0.12</div>
    </div>

    <div class="coin">
        <span class="led"></span>
        <b>USDT</b>
        <div class="coin-price" id="USDTprice">$1</div>
    </div>

    <div class="coin">
        <span class="led"></span>
        <b>TRX</b>
        <div class="coin-price" id="TRXprice">$0.25</div>
    </div>

</section>


<!-- EXCHANGE -->

<section class="card">

    <div class="title">
        🔄 تبادل ارز
    </div>

    <div class="grid">

        <div>
            <labe1>افروش sell</label>

            <select id="fromCoin">
                <option value="BTC">Bitcoin (BTC)</option>
                <option value="LTC">Litecoin (LTC)</option>
                <option value="BCH">Bitcoin Cash (BCH)</option>
                <option value="DOGE" selected>Dogecoin (DOGE)</option>
                <option value="USDT">Tether USDT (BSC)</option>
                <option value="TRX">TRON (TRX)</option>
            </select>
        </div>

        <div>
            <label>اخرید buy</label>

            <select id="toCoin">
                <option value="BTC" selected>Bitcoin (BTC)</option>
                <option value="LTC">Litecoin (LTC)</option>
                <option value="BCH">Bitcoin Cash (BCH)</option>
                <option value="DOGE">Dogecoin (DOGE)</option>
                <option value="USDT">Tether USDT (BSC)</option>
                <option value="TRX">TRON (TRX)</option>
            </select>
        </div>

    </div>


    <div class="field">

        <label>مقدار ارز</label>

        <input
            id="amount"
            type="number"
            min="0"
            step="any"
            placeholder="مثلاً 100"
        >

    </div>


    <div class="result">

        <span>مقدار دریافتی:</span>

        <strong id="receive">
            0 BTC
        </strong>

    </div>

    <div class="rate" id="rate">
        نرخ تبدیل را وارد کنید
    </div>


    <div class="field">

        <label>
            آدرس کیف پول شما برای دریافت
        </label>

        <input
            id="destination"
            type="text"
            placeholder="آدرس ارز مقصد خود را وارد کنید"
            dir="ltr"
        >

    </div>


    <button class="button" id="createTrade">
        ایجاد درخواست تبدیل
    </button>


    <div class="message" id="message"></div>


    <!-- آدرس واریز -->

    <div class="deposit" id="deposit">

        <h3>📥 آدرس واریز شما</h3>

        <div id="depositText">
            لطفاً ارز مبدأ را به آدرس زیر ارسال کنید:
        </div>

        <div
            class="deposit-address"
            id="depositAddress"
        ></div>

        <button
            class="copy"
            id="copyButton"
        >
            📋 کپی آدرس
        </button>

        <div class="warning">
            ⚠️ فقط ارز و شبکه مشخص‌شده را به این آدرس ارسال کنید.
            پس از ارسال، TXID تراکنش را برای بررسی ثبت کنید.
        </div>

        <div
            class="trade-id"
            id="tradeId"
        ></div>

    </div>

</section>


<div class="footer">
    تبادل © Crypto Exchange
</div>

</div>


<script>

/* =========================
   PRICE DATA
   ========================= */

const prices = {

    BTC:65000,
    LTC:70,
    BCH:520,
    DOGE:0.12,
    USDT:1,
    TRX:0.25

};


/* =========================
   YOUR DEPOSIT ADDRESSES
   ========================= */

const depositAddresses = {

    BTC:
    "1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

    LTC:
    "LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

    BCH:
    "bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

    DOGE:
    "DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

    USDT:
    "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6",

    TRX:
    "TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"

};


/* =========================
   ELEMENTS
   ========================= */

const fromCoin =
document.getElementById("fromCoin");

const toCoin =
document.getElementById("toCoin");

const amount =
document.getElementById("amount");

const receive =
document.getElementById("receive");

const rate =
document.getElementById("rate");

const destination =
document.getElementById("destination");

const message =
document.getElementById("message");

const deposit =
document.getElementById("deposit");

const depositAddress =
document.getElementById("depositAddress");

const depositText =
document.getElementById("depositText");

const tradeId =
document.getElementById("tradeId");


/* =========================
   CALCULATE
   ========================= */

function calculate(){

    const from =
    fromCoin.value;

    const to =
    toCoin.value;

    const value =
    Number(amount.value);

    if(!value || value <= 0){

        receive.textContent =
        "0 " + to;

        rate.textContent =
        "مقدار را وارد کنید";

        return;
    }

    if(from === to){

        receive.textContent =
        "ارز یکسان";

        rate.textContent =
        "ارز مبدأ و مقصد باید متفاوت باشند";

        return;
    }

    const dollarValue =
    value * prices[from];

    const result =
    dollarValue / prices[to];

    receive.textContent =
    result.toLocaleString(
        "en-US",
        {
            maximumFractionDigits:12
        }
    ) + " " + to;

    rate.textContent =
    "1 " + from +
    " ≈ " +
    (prices[from] / prices[to])
    .toLocaleString(
        "en-US",
        {
            maximumFractionDigits:12
        }
    ) +
    " " + to;

}


amount.addEventListener(
    "input",
    calculate
);

fromCoin.addEventListener(
    "change",
    calculate
);

toCoin.addEventListener(
    "change",
    calculate
);


/* =========================
   CREATE TRADE
   ========================= */

document
.getElementById("createTrade")
.addEventListener(
"click",
function(){

    const from =
    fromCoin.value;

    const to =
    toCoin.value;

    const value =
    Number(amount.value);

    const userAddress =
    destination.value.trim();


    message.style.display =
    "block";

    deposit.style.display =
    "none";


    if(!value || value <= 0){

        message.textContent =
        "❌ مقدار ارز را وارد کنید.";

        return;
    }


    if(from === to){

        message.textContent =
        "❌ ارز مبدأ و مقصد یکسان است.";

        return;
    }


    if(!userAddress){

        message.textContent =
        "❌ آدرس کیف پول مقصد خود را وارد کنید.";

        return;
    }


    /*
      در نسخه واقعی این اطلاعات باید
      به سرور ارسال و در دیتابیس ثبت شود.
    */


    const id =
    "TB-" +
    Date.now()
    .toString()
    .slice(-10);


    message.textContent =
    "✅ درخواست تبدیل ایجاد شد. آدرس واریز ارز مبدأ را در پایین مشاهده کنید.";


    depositText.textContent =
    "لطفاً " +
    from +
    " را به آدرس زیر ارسال کنید:";


    depositAddress.textContent =
    depositAddresses[from];


    tradeId.textContent =
    "شناسه معامله: " + id;


    deposit.style.display =
    "block";


    deposit.scrollIntoView({
        behavior:"smooth",
        block:"nearest"
    });

});


/* =========================
   COPY
   ========================= */

document
.getElementById("copyButton")
.addEventListener(
"click",
async function(){

    const text =
    depositAddress.textContent;

    try{

        await navigator.clipboard.writeText(text);

        this.textContent =
        "✅ آدرس کپی شد";

        setTimeout(
        ()=>{
            this.textContent =
            "📋 کپی آدرس";
        },
        1800);

    }catch(error){

        const area =
        document.createElement("textarea");

        area.value = text;

        document.body.appendChild(area);

        area.select();

        document.execCommand("copy");

        area.remove();

        this.textContent =
        "✅ آدرس کپی شد";

    }

});


/* =========================
   INITIAL
   ========================= */

calculate();

</script>
<!-- ==============================
     TABADOL - TRANSACTION SYSTEM
     این کد را پایین HTML فعلی قرار بده
================================ -->

<style>
#tabadolTxSystem{
  direction:rtl;
  font-family:Tahoma,Arial,sans-serif;
  max-width:1000px;
  margin:25px auto;
}

.tx-box{
  background:rgba(255,255,255,.96);
  border-radius:18px;
  padding:20px;
  margin:15px 0;
  box-shadow:0 8px 30px rgba(0,0,0,.12);
}

.tx-box h2{
  margin-top:0;
  color:#222;
}

.tx-input{
  width:100%;
  box-sizing:border-box;
  padding:13px;
  border:1px solid #ddd;
  border-radius:10px;
  margin:7px 0;
  font-size:15px;
}

.tx-btn{
  border:0;
  border-radius:10px;
  padding:12px 18px;
  cursor:pointer;
  font-weight:bold;
  margin:5px;
}

.tx-btn-main{
  background:#111;
  color:white;
}

.tx-btn-green{
  background:#159447;
  color:white;
}

.tx-btn-red{
  background:#d33;
  color:white;
}

.tx-btn-blue{
  background:#1877d2;
  color:white;
}

.tx-result{
  background:#f7f7f7;
  border-radius:12px;
  padding:15px;
  margin-top:15px;
  line-height:2;
  word-break:break-word;
}

.tx-status{
  display:inline-block;
  padding:5px 10px;
  border-radius:20px;
  background:#eee;
  font-weight:bold;
}

.tx-status.pending{
  background:#fff0b3;
  color:#8a6500;
}

.tx-status.received{
  background:#d9f4df;
  color:#146b2d;
}

.tx-status.completed{
  background:#bdecc8;
  color:#075c1c;
}

.tx-status.cancelled{
  background:#ffd5d5;
  color:#9b1111;
}

.tx-admin{
  display:none;
}

.tx-admin-table{
  width:100%;
  border-collapse:collapse;
  margin-top:15px;
  font-size:13px;
}

.tx-admin-table th,
.tx-admin-table td{
  border:1px solid #ddd;
  padding:9px;
  text-align:right;
  vertical-align:top;
}

.tx-admin-table th{
  background:#222;
  color:white;
}

.tx-admin-table tr:nth-child(even){
  background:#fafafa;
}

.tx-small{
  font-size:12px;
  color:#777;
}

.tx-copy{
  background:#1877d2;
  color:#fff;
  border:0;
  padding:8px 12px;
  border-radius:7px;
  cursor:pointer;
}

.tx-search-row{
  display:flex;
  gap:8px;
}

.tx-search-row input{
  flex:1;
}

@media(max-width:700px){
  .tx-admin-table{
    display:block;
    overflow-x:auto;
    white-space:nowrap;
  }

  .tx-search-row{
    flex-direction:column;
  }
}
</style>


<div id="tabadolTxSystem">

  <!-- =========================
       پیگیری معامله کاربر
  ========================== -->
  <div class="tx-box">

    <h2>🔎 پیگیری معامله</h2>

    <div class="tx-search-row">
      <input
        id="txSearchCode"
        class="tx-input"
        placeholder="کد معامله را وارد کنید"
      >

      <button
        class="tx-btn tx-btn-blue"
        onclick="tabadolFindTransaction()"
      >
        مشاهده معامله
      </button>
    </div>

    <div id="txUserResult"></div>

  </div>


  <!-- =========================
       پنل مدیریت
       عمداً در صفحه اصلی مخفی است
  ========================== -->

  <div id="tabadolAdminPanel" class="tx-admin">

    <div class="tx-box">

      <h2>🔐 پنل مدیریت تبادل</h2>

      <button
        class="tx-btn tx-btn-red"
        onclick="tabadolAdminLogout()"
      >
        خروج از پنل
      </button>

      <div id="txAdminStats"></div>

      <div style="overflow-x:auto;">
        <table class="tx-admin-table">

          <thead>
            <tr>
              <th>کد</th>
              <th>مبدأ</th>
              <th>مقصد</th>
              <th>آدرس مقصد</th>
              <th>آدرس واریز</th>
              <th>TXID</th>
              <th>زمان</th>
              <th>وضعیت</th>
              <th>عملیات</th>
            </tr>
          </thead>

          <tbody id="txAdminList"></tbody>

        </table>
      </div>

    </div>

  </div>

</div>


<script>
/* ==========================================
   TABADOL TRANSACTION SYSTEM
========================================== */


/* -------------------------------
   تنظیمات
-------------------------------- */

const TABADOL_ADMIN_PASSWORD = "Admin321";

const TABADOL_STORAGE_KEY =
  "TABADOL_TRANSACTIONS_V2";


/* -------------------------------
   آدرس‌های واریز
-------------------------------- */

const TABADOL_DEPOSIT_ADDRESSES = {

  BTC:
    "1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

  LTC:
    "LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

  BCH:
    "bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

  DOGE:
    "DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

  USDT:
    "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6",

  TRX:
    "TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"

};


/* -------------------------------
   خواندن معاملات
-------------------------------- */

function tabadolGetTransactions(){

  try{

    const data =
      localStorage.getItem(TABADOL_STORAGE_KEY);

    if(!data) return [];

    const parsed = JSON.parse(data);

    return Array.isArray(parsed)
      ? parsed
      : [];

  }catch(e){

    return [];

  }

}


/* -------------------------------
   ذخیره معاملات
-------------------------------- */

function tabadolSaveTransactions(list){

  localStorage.setItem(
    TABADOL_STORAGE_KEY,
    JSON.stringify(list)
  );

}


/* -------------------------------
   ساخت کد معامله
-------------------------------- */

function tabadolGenerateTradeCode(){

  const now = new Date();

  const date =
    now.getFullYear().toString().slice(-2) +
    String(now.getMonth()+1).padStart(2,"0") +
    String(now.getDate()).padStart(2,"0");

  const random =
    Math.floor(100000 + Math.random()*900000);

  return "TB-" + date + "-" + random;

}


/* -------------------------------
   مخفی کردن اطلاعات
-------------------------------- */

function tabadolMask(value){

  if(!value) return "••••";

  value = String(value);

  if(value.length <= 10){

    return value.substring(0,3) +
      "••••" +
      value.substring(value.length-3);

  }

  return value.substring(0,6) +
    "••••••••" +
    value.substring(value.length-6);

}


/* -------------------------------
   فرار از HTML
-------------------------------- */

function tabadolEscape(value){

  if(value === undefined || value === null)
    return "";

  return String(value)
    .replace(/&/g,"&amp;")
    .replace(/</g,"&lt;")
    .replace(/>/g,"&gt;")
    .replace(/"/g,"&quot;")
    .replace(/'/g,"&#039;");

}


/* -------------------------------
   زمان
-------------------------------- */

function tabadolTime(){

  return new Date().toLocaleString(
    "fa-IR",
    {
      year:"numeric",
      month:"2-digit",
      day:"2-digit",
      hour:"2-digit",
      minute:"2-digit",
      second:"2-digit"
    }
  );

}


/* =================================================
   این تابع را از دکمه «کپی آدرس واریز» فعلی سایت
   صدا بزن
================================================= */

function tabadolRegisterAfterCopy(
  sourceCoin,
  sourceAmount,
  destinationCoin,
  destinationAmount,
  userDestinationAddress
){

  if(!sourceCoin ||
     !sourceAmount ||
     !destinationCoin ||
     !destinationAmount ||
     !userDestinationAddress){

    alert("اطلاعات معامله کامل نیست.");
    return null;

  }


  const depositAddress =
    TABADOL_DEPOSIT_ADDRESSES[sourceCoin];

  if(!depositAddress){

    alert("آدرس واریز این ارز تنظیم نشده است.");
    return null;

  }


  let transactions =
    tabadolGetTransactions();


  let tradeCode =
    tabadolGenerateTradeCode();


  /* جلوگیری از تکراری شدن کد */

  while(
    transactions.some(
      t => t.code === tradeCode
    )
  ){

    tradeCode =
      tabadolGenerateTradeCode();

  }


  const transaction = {

    code: tradeCode,

    sourceCoin: sourceCoin,

    sourceAmount: String(sourceAmount),

    destinationCoin: destinationCoin,

    destinationAmount:
      String(destinationAmount),

    userDestinationAddress:
      String(userDestinationAddress),

    depositAddress:
      String(depositAddress),

    txid: "",

    status: "در انتظار پرداخت",

    createdAt: tabadolTime(),

    updatedAt: tabadolTime()

  };


  transactions.unshift(transaction);

  tabadolSaveTransactions(transactions);


  /* کد معامله را برای کاربر نگه می‌داریم */

  try{

    sessionStorage.setItem(
      "TABADOL_LAST_TRADE",
      tradeCode
    );

  }catch(e){}


  alert(
    "معامله با موفقیت ثبت شد.\n\n" +
    "کد معامله: " +
    tradeCode
  );


  return transaction;

}


/* =================================================
   کپی آدرس + ثبت معامله در یک تابع
================================================= */

function tabadolCopyDepositAndRegister(

  sourceCoin,
  sourceAmount,
  destinationCoin,
  destinationAmount,
  userDestinationAddress

){

  const address =
    TABADOL_DEPOSIT_ADDRESSES[sourceCoin];

  if(!address){

    alert("آدرس واریز پیدا نشد.");
    return;

  }


  /* ثبت معامله */

  const transaction =
    tabadolRegisterAfterCopy(

      sourceCoin,
      sourceAmount,
      destinationCoin,
      destinationAmount,
      userDestinationAddress

    );


  if(!transaction) return;


  /* کپی آدرس */

  if(navigator.clipboard){

    navigator.clipboard.writeText(address)
      .then(()=>{

        alert(
          "آدرس واریز کپی شد.\n\n" +
          "کد معامله: " +
          transaction.code
        );

      })
      .catch(()=>{

        prompt(
          "آدرس واریز را کپی کنید:",
          address
        );

      });

  }else{

    prompt(
      "آدرس واریز را کپی کنید:",
      address
    );

  }

}


/* =================================================
   ثبت TXID
================================================= */

function tabadolSaveTxid(code, txid){

  if(!code || !txid){

    alert("کد معامله و TXID را وارد کنید.");
    return;

  }


  let transactions =
    tabadolGetTransactions();


  const index =
    transactions.findIndex(
      t => t.code === code
    );


  if(index === -1){

    alert("معامله پیدا نشد.");
    return;

  }


  transactions[index].txid =
    String(txid).trim();

  transactions[index].updatedAt =
    tabadolTime();


  tabadolSaveTransactions(
    transactions
  );


  alert("TXID ثبت شد.");

}


/* =================================================
   نمایش معامله برای کاربر
================================================= */

function tabadolFindTransaction(){

  const code =
    document.getElementById(
      "txSearchCode"
    ).value.trim();


  const result =
    document.getElementById(
      "txUserResult"
    );


  if(!code){

    result.innerHTML =
      '<div class="tx-result">کد معامله را وارد کنید.</div>';

    return;

  }


  const transactions =
    tabadolGetTransactions();


  const trade =
    transactions.find(
      t =>
        t.code.toUpperCase() ===
        code.toUpperCase()
    );


  if(!trade){

    result.innerHTML =
      '<div class="tx-result">' +
      '❌ معامله‌ای با این کد پیدا نشد.' +
      '</div>';

    return;

  }


  let statusClass =
    "pending";


  if(trade.status === "ارز مقصد ارسال شد" ||
     trade.status === "تکمیل شد"){

    statusClass = "completed";

  }


  if(trade.status === "دریافت شد"){

    statusClass = "received";

  }


  if(trade.status === "لغو شد"){

    statusClass = "cancelled";

  }


  result.innerHTML = `

    <div class="tx-result">

      <h3>📄 اطلاعات معامله</h3>

      <b>کد معامله:</b>
      ${tabadolEscape(trade.code)}
      <br>

      <b>ارز ارسالی:</b>
      ${tabadolEscape(trade.sourceAmount)}
      ${tabadolEscape(trade.sourceCoin)}
      <br>

      <b>ارز درخواستی:</b>
      ${tabadolEscape(trade.destinationAmount)}
      ${tabadolEscape(trade.destinationCoin)}
      <br>

      <b>آدرس دریافت:</b>
      ${tabadolMask(trade.userDestinationAddress)}
      <br>

      <b>آدرس واریز:</b>
      ${tabadolMask(trade.depositAddress)}
      <br>

      <b>TXID:</b>
      ${
        trade.txid
        ? tabadolMask(trade.txid)
        : "هنوز ثبت نشده"
      }
      <br>

      <b>زمان ثبت:</b>
      ${tabadolEscape(trade.createdAt)}
      <br>

      <b>آخرین بروزرسانی:</b>
      ${tabadolEscape(trade.updatedAt)}
      <br><br>

      <b>وضعیت:</b>
      <span class="tx-status ${statusClass}">
        ${tabadolEscape(trade.status)}
      </span>

      ${
        trade.status === "تکمیل شد"
        ? `
          <hr>
          <strong>✅ معامله با موفقیت تکمیل شده است.</strong>
        `
        : ""
      }

    </div>

  `;

}


/* =================================================
   ورود مدیر
   برای استفاده، این تابع را از یک دکمه مخفی/اختصاصی
   یا URL داخلی خودت اجرا کن
================================================= */

function tabadolAdminLogin(){

  const password =
    prompt("رمز ورود پنل مدیریت را وارد کنید:");

  if(password !== TABADOL_ADMIN_PASSWORD){

    alert("رمز ورود اشتباه است.");
    return;

  }


  sessionStorage.setItem(
    "TABADOL_ADMIN_SESSION",
    "1"
  );


  document.getElementById(
    "tabadolAdminPanel"
  ).style.display = "block";


  tabadolRenderAdmin();

}


/* =================================================
   خروج مدیر
================================================= */

function tabadolAdminLogout(){

  sessionStorage.removeItem(
    "TABADOL_ADMIN_SESSION"
  );


  document.getElementById(
    "tabadolAdminPanel"
  ).style.display = "none";

}


/* =================================================
   بررسی ورود مدیر
================================================= */

function tabadolCheckAdmin(){

  const logged =
    sessionStorage.getItem(
      "TABADOL_ADMIN_SESSION"
    );


  if(logged === "1"){

    document.getElementById(
      "tabadolAdminPanel"
    ).style.display = "block";


    tabadolRenderAdmin();

  }

}


/* =================================================
   نمایش پنل مدیریت
================================================= */

function tabadolRenderAdmin(){

  const list =
    document.getElementById(
      "txAdminList"
    );


  const stats =
    document.getElementById(
      "txAdminStats"
    );


  if(!list || !stats) return;


  const transactions =
    tabadolGetTransactions();


  const total =
    transactions.length;


  const pending =
    transactions.filter(
      t => t.status === "در انتظار پرداخت"
    ).length;


  const completed =
    transactions.filter(
      t => t.status === "تکمیل شد"
    ).length;


  stats.innerHTML = `

    <div class="tx-result">

      <b>کل معاملات:</b> ${total}
      &nbsp;&nbsp;

      <b>در انتظار:</b> ${pending}
      &nbsp;&nbsp;

      <b>تکمیل شده:</b> ${completed}

    </div>

  `;


  if(!transactions.length){

    list.innerHTML = `
      <tr>
        <td colspan="9">
          هنوز معامله‌ای ثبت نشده است.
        </td>
      </tr>
    `;

    return;

  }


  list.innerHTML =
    transactions.map(
      trade => `

      <tr>

        <td>
          <b>${tabadolEscape(trade.code)}</b>
        </td>

        <td>
          ${tabadolEscape(trade.sourceAmount)}
          ${tabadolEscape(trade.sourceCoin)}
        </td>

        <td>
          ${tabadolEscape(trade.destinationAmount)}
          ${tabadolEscape(trade.destinationCoin)}
        </td>

        <td>
          ${tabadolEscape(
            trade.userDestinationAddress
          )}
        </td>

        <td>
          ${tabadolEscape(
            trade.depositAddress
          )}
        </td>

        <td>
          ${
            trade.txid
            ? tabadolEscape(trade.txid)
            : "—"
          }
        </td>

        <td>
          ${tabadolEscape(trade.createdAt)}
        </td>

        <td>

          <span class="tx-status">
            ${tabadolEscape(trade.status)}
          </span>

        </td>

        <td>

          <button
            class="tx-btn tx-btn-green"
            onclick="tabadolSetStatus(
              '${trade.code}',
              'دریافت شد'
            )"
          >
            دریافت شد
          </button>

          <button
            class="tx-btn tx-btn-green"
            onclick="tabadolSetStatus(
              '${trade.code}',
              'تکمیل شد'
            )"
          >
            تکمیل شد
          </button>

          <button
            class="tx-btn tx-btn-red"
            onclick="tabadolSetStatus(
              '${trade.code}',
              'لغو شد'
            )"
          >
            لغو
          </button>

        </td>

      </tr>

    `
    ).join("");

}


/* =================================================
   تغییر وضعیت
================================================= */

function tabadolSetStatus(code,status){

  let transactions =
    tabadolGetTransactions();


  const index =
    transactions.findIndex(
      t => t.code === code
    );


  if(index === -1){

    alert("معامله پیدا نشد.");
    return;

  }


  transactions[index].status =
    status;


  transactions[index].updatedAt =
    tabadolTime();


  tabadolSaveTransactions(
    transactions
  );


  tabadolRenderAdmin();


  /* اگر همان معامله توسط کاربر باز باشد */

  tabadolFindTransaction();

}


/* =================================================
   ایجاد پنل مدیریت با کلید مخفی
   کلید: Ctrl + Shift + A
================================================= */

document.addEventListener(
  "keydown",
  function(event){

    if(
      event.ctrlKey &&
      event.shiftKey &&
      event.key.toLowerCase() === "a"
    ){

      event.preventDefault();

      tabadolAdminLogin();

    }

  }
);


/* =================================================
   بارگذاری اولیه
================================================= */

document.addEventListener(
  "DOMContentLoaded",
  function(){

    tabadolCheckAdmin();

  }
);

</script>
</body>
</html>
