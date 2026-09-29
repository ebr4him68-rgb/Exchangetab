


<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>تبادل | صرافی تبادل ارز</title>

<style>
:root{
  --bg1:#fff36b;
  --bg2:#ffae00;
  --card:rgba(255,255,255,.95);
  --text:#111;
  --accent:#087f23;
  --border:#ddd;
  --shadow:0 15px 40px rgba(0,0,0,.16);
}

*{box-sizing:border-box}

body{
  margin:0;
  min-height:100vh;
  font-family:Tahoma,Arial,sans-serif;
  color:var(--text);
  background:linear-gradient(135deg,var(--bg1),var(--bg2));
}

body.theme-green{
  --bg1:#c9ffd5;
  --bg2:#13a653;
}

body.theme-yellow{
  --bg1:#fff36b;
  --bg2:#ffae00;
}

body.theme-orange{
  --bg1:#ffe0a8;
  --bg2:#f57c00;
}

body.theme-blue{
  --bg1:#c9edff;
  --bg2:#1976d2;
}

body.theme-black{
  --bg1:#222;
  --bg2:#050505;
  --text:#fff;
  --card:rgba(28,28,28,.97);
  --border:#444;
}

.container{
  max-width:1200px;
  margin:auto;
  padding:18px;
}

.header{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
  padding:18px 20px;
  border-radius:24px;
  background:var(--card);
  box-shadow:var(--shadow);
  margin-bottom:18px;
}

.logo{
  font-size:27px;
  font-weight:900;
}

.subtitle{
  opacity:.7;
  margin-top:5px;
  font-size:13px;
}

.settings{
  border:0;
  background:#111;
  color:white;
  border-radius:15px;
  padding:12px 16px;
  cursor:pointer;
  font-size:21px;
}

.coin-grid{
  display:grid;
  grid-template-columns:repeat(6,1fr);
  gap:12px;
  margin-bottom:18px;
}

.coin-card{
  background:var(--card);
  border-radius:20px;
  padding:16px 10px;
  text-align:center;
  box-shadow:var(--shadow);
}

.led{
  width:22px;
  height:22px;
  margin:auto;
  border-radius:50%;
  background:#00ff3c;
  box-shadow:0 0 10px #00ff3c,0 0 25px #00ff3c;
  animation:blink .65s infinite alternate;
}

@keyframes blink{
  from{opacity:1;transform:scale(1)}
  to{opacity:.2;transform:scale(.72)}
}

.coin-name{
  margin-top:9px;
  font-weight:900;
  font-size:18px;
}

.coin-price{
  margin-top:7px;
  font-weight:900;
  font-size:14px;
  direction:ltr;
}

.panel{
  background:var(--card);
  border-radius:24px;
  padding:23px;
  box-shadow:var(--shadow);
  margin-bottom:18px;
}

.panel-title{
  font-size:22px;
  font-weight:900;
  margin-bottom:18px;
}

.buy-sell{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:14px;
  margin-bottom:18px;
}

.trade-button{
  border:0;
  border-radius:20px;
  padding:20px;
  font-size:27px;
  font-weight:900;
  cursor:pointer;
  animation:pulse 1s infinite alternate;
}

@keyframes pulse{
  to{transform:scale(1.025)}
}

.buy{
  background:#08b83d;
  color:white;
}

.sell{
  background:#ffc400;
  color:#111;
}

.selected{
  outline:5px solid white;
  box-shadow:0 0 0 4px #111;
}

.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:14px;
}

.field label{
  display:block;
  font-weight:900;
  margin-bottom:7px;
}

input,select{
  width:100%;
  padding:14px;
  border:2px solid var(--border);
  border-radius:14px;
  font-size:16px;
  outline:none;
  background:white;
  color:#111;
}

input:focus,select:focus{
  border-color:#087f23;
}

.wide{
  grid-column:1/-1;
}

.result-box{
  margin-top:15px;
  padding:17px;
  border-radius:16px;
  background:rgba(0,0,0,.07);
  font-weight:900;
  line-height:2;
}

.address-box{
  margin-top:15px;
  padding:18px;
  border-radius:17px;
  background:#edf8ff;
  color:#111;
  word-break:break-all;
  direction:ltr;
  text-align:left;
  display:none;
}

.main-button{
  border:0;
  border-radius:15px;
  padding:15px 22px;
  background:#111;
  color:white;
  font-size:17px;
  font-weight:900;
  cursor:pointer;
  margin-top:14px;
}

.copy-button{
  background:#087f23;
  display:none;
}

.success{
  display:none;
  margin-top:15px;
  padding:18px;
  border-radius:17px;
  background:#d8ffe2;
  color:#075d20;
  font-weight:900;
  line-height:2;
}

.track{
  display:flex;
  gap:10px;
}

.track input{
  flex:1;
}

.status{
  display:inline-block;
  padding:5px 11px;
  border-radius:9px;
  background:#eee;
  color:#111;
  font-weight:900;
}

.footer{
  text-align:center;
  padding:18px;
  opacity:.7;
  font-size:12px;
}

.modal{
  display:none;
  position:fixed;
  inset:0;
  z-index:100;
  background:rgba(0,0,0,.75);
  padding:20px;
  overflow:auto;
}

.modal-box{
  max-width:1150px;
  margin:auto;
  background:var(--card);
  color:var(--text);
  border-radius:24px;
  padding:22px;
}

.small-modal{
  max-width:430px;
}

.close{
  float:left;
  border:0;
  border-radius:10px;
  padding:8px 12px;
  cursor:pointer;
}

.theme-grid{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:9px;
}

.theme-grid button{
  border:0;
  border-radius:13px;
  height:50px;
  font-weight:900;
  cursor:pointer;
}

.green-theme{background:#20a85a}
.yellow-theme{background:#ffd400}
.orange-theme{background:#f57c00}
.blue-theme{background:#1976d2;color:white}
.black-theme{background:#111;color:white}

.stats{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:12px;
  margin:17px 0;
}

.stat{
  padding:18px;
  border-radius:15px;
  background:rgba(0,0,0,.07);
  text-align:center;
  font-weight:900;
}

.stat-number{
  display:block;
  font-size:25px;
  margin-top:6px;
}

.table-wrapper{
  overflow:auto;
}

table{
  width:100%;
  min-width:1200px;
  border-collapse:collapse;
}

th,td{
  padding:10px;
  border-bottom:1px solid var(--border);
  text-align:right;
  vertical-align:top;
}

th{
  background:rgba(0,0,0,.08);
}

.action-btn{
  border:0;
  border-radius:8px;
  padding:7px 9px;
  margin:2px;
  cursor:pointer;
  font-weight:700;
}

.edit-btn{background:#ffc400}
.done-btn{background:#50d878}
.wait-btn{background:#ddd}
.delete-btn{background:#e53935;color:white}

.notice{
  font-size:12px;
  opacity:.7;
  line-height:1.8;
  margin-top:12px;
}

@media(max-width:950px){
  .coin-grid{
    grid-template-columns:repeat(3,1fr);
  }
}

@media(max-width:650px){
  .container{padding:10px}

  .coin-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .grid{
    grid-template-columns:1fr;
  }

  .wide{
    grid-column:auto;
  }

  .buy-sell{
    grid-template-columns:1fr;
  }

  .track{
    flex-direction:column;
  }

  .stats{
    grid-template-columns:1fr;
  }

  .theme-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .logo{
    font-size:21px;
  }
}
</style>
</head>

<body>

<div class="container">

<header class="header">
  <div>
    <div class="logo">💡 صرافی تبادل ارز</div>
    <div class="subtitle">
      تبادل مستقیم ارزهای دیجیتال — بدون نگهداری موجودی کاربران
    </div>
  </div>

  <button class="settings" onclick="openSettings()">⚙️</button>
</header>


<!-- COINS -->

<section class="coin-grid" id="coinGrid"></section>


<!-- EXCHANGE -->

<section class="panel">

<div class="panel-title">
  🔄 ایجاد معامله
</div>

<div class="buy-sell">

<button id="buyButton"
        class="trade-button buy"
        onclick="setSide('BUY')">
  BUY
</button>

<button id="sellButton"
        class="trade-button sell"
        onclick="setSide('SELL')">
  SELL
</button>

</div>


<div class="grid">

<div class="field">
<label>ارز مبدأ</label>

<select id="fromCoin" onchange="calculateExchange()"></select>
</div>


<div class="field">
<label>مبلغ مبدأ</label>

<input
id="fromAmount"
type="number"
min="0"
step="any"
placeholder="مبلغ را وارد کنید"
oninput="calculateExchange()">
</div>


<div class="field">
<label>ارز مقصد</label>

<select id="toCoin" onchange="calculateExchange()"></select>
</div>


<div class="field">
<label>مبلغ تقریبی دریافتی</label>

<input id="toAmount" readonly>
</div>


<div class="field wide">

<label>
آدرس کیف پول شما برای دریافت ارز مقصد
</label>

<input
id="userAddress"
dir="ltr"
placeholder="آدرس کیف پول خود را وارد کنید">

</div>

</div>


<div class="result-box" id="calculation">
در حال دریافت قیمت آنلاین...
</div>


<button class="main-button"
        onclick="prepareTrade()">
ایجاد معامله
</button>


<div class="address-box" id="depositBox"></div>


<button
id="copyRegisterButton"
class="main-button copy-button"
onclick="copyDepositAndRegister()">

📋 کپی آدرس و ثبت معامله

</button>


<div id="successBox" class="success"></div>

</section>


<!-- TRACK -->

<section class="panel">

<div class="panel-title">
🔎 پیگیری معامله
</div>

<div class="track">

<input
id="trackingCode"
dir="ltr"
placeholder="کد معامله مثل TB-260930-483921">

<button
class="main-button"
onclick="trackTrade()">

پیگیری

</button>

</div>

<div id="trackingResult"></div>

</section>


<div class="footer">
قیمت‌ها از CoinGecko دریافت می‌شوند.
</div>

</div>


<!-- SETTINGS -->

<div id="settingsModal" class="modal">

<div class="modal-box small-modal">

<button class="close"
onclick="closeModal('settingsModal')">
✕
</button>

<h2>⚙️ تنظیمات سایت</h2>

<p>
انتخاب رنگ ظاهر سایت:
</p>

<div class="theme-grid">

<button class="green-theme"
onclick="setTheme('green')">
سبز
</button>

<button class="yellow-theme"
onclick="setTheme('yellow')">
زرد
</button>

<button class="orange-theme"
onclick="setTheme('orange')">
نارنجی
</button>

<button class="blue-theme"
onclick="setTheme('blue')">
آبی
</button>

<button class="black-theme"
onclick="setTheme('black')">
مشکی
</button>

</div>


<button
class="main-button"
onclick="openAdminLogin()">

🔐 ورود به پنل مدیریت

</button>

</div>

</div>


<!-- ADMIN LOGIN -->

<div id="loginModal" class="modal">

<div class="modal-box small-modal">

<button class="close"
onclick="closeModal('loginModal')">
✕
</button>

<h2>🔐 ورود مدیریت</h2>

<input
id="adminPassword"
type="password"
placeholder="رمز مدیریت">

<button
class="main-button"
onclick="loginAdmin()">

ورود به پنل

</button>

<div id="loginMessage"></div>

</div>

</div>


<!-- ADMIN -->

<div id="adminModal" class="modal">

<div class="modal-box">

<button class="close"
onclick="closeModal('adminModal')">
✕
</button>

<h2>🛠 پنل مدیریت صرافی تبادل</h2>


<div class="stats">

<div class="stat">
کل معاملات
<span id="totalTrades" class="stat-number">0</span>
</div>

<div class="stat">
در انتظار پرداخت
<span id="pendingTrades" class="stat-number">0</span>
</div>

<div class="stat">
تکمیل شده
<span id="completedTrades" class="stat-number">0</span>
</div>

</div>


<div class="table-wrapper">

<table>

<thead>

<tr>

<th>کد</th>
<th>نوع</th>
<th>مبدأ</th>
<th>مبلغ</th>
<th>مقصد</th>
<th>دریافتی</th>
<th>آدرس کاربر</th>
<th>آدرس واریز</th>
<th>TXID</th>
<th>وضعیت</th>
<th>زمان</th>
<th>عملیات</th>

</tr>

</thead>

<tbody id="adminTable"></tbody>

</table>

</div>

</div>

</div>


<!-- EDIT -->

<div id="editModal" class="modal">

<div class="modal-box">

<button class="close"
onclick="closeModal('editModal')">
✕
</button>

<h2>✏️ ویرایش معامله</h2>

<input type="hidden" id="editId">

<div class="grid">

<div class="field">
<label>ارز مبدأ</label>
<select id="editFrom"></select>
</div>

<div class="field">
<label>مبلغ مبدأ</label>
<input id="editFromAmount" type="number" step="any">
</div>

<div class="field">
<label>ارز مقصد</label>
<select id="editTo"></select>
</div>

<div class="field">
<label>مبلغ مقصد</label>
<input id="editToAmount" type="number" step="any">
</div>

<div class="field wide">
<label>آدرس کاربر</label>
<input id="editUserAddress" dir="ltr">
</div>

<div class="field wide">
<label>TXID</label>
<input id="editTxid" dir="ltr">
</div>

<div class="field">
<label>وضعیت</label>

<select id="editStatus">

<option value="در انتظار پرداخت">
در انتظار پرداخت
</option>

<option value="دریافت شد">
دریافت شد
</option>

<option value="تکمیل شد">
تکمیل شد
</option>

<option value="لغو شد">
لغو شد
</option>

</select>

</div>

</div>

<button
class="main-button"
onclick="saveEditedTrade()">

💾 ذخیره تغییرات

</button>

</div>

</div>


<script>

/* =========================
   COINS
========================= */

const COINS = {

BTC:{
 name:"BTC",
 cg:"bitcoin",
 address:"1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV"
},

LTC:{
 name:"LTC",
 cg:"litecoin",
 address:"LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c"
},

BCH:{
 name:"BCH",
 cg:"bitcoin-cash",
 address:"bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku"
},

DOGE:{
 name:"DOGE",
 cg:"dogecoin",
 address:"DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk"
},

USDT:{
 name:"USDT",
 cg:"tether",
 address:"0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6"
},

TRX:{
 name:"TRX",
 cg:"tron",
 address:"TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3"
}

};


const ADMIN_PASSWORD="Admin321";

const STORAGE_KEY="TABADOL_TRANSACTIONS_V4";

let prices={};

let currentSide="BUY";

let preparedTrade=null;


/* =========================
   HELPERS
========================= */

function $(id){
 return document.getElementById(id);
}


/* =========================
   INITIALIZE
========================= */

function initialize(){

 const options=Object.keys(COINS)
 .map(c=>`<option value="${c}">${c}</option>`)
 .join("");

 $("fromCoin").innerHTML=options;
 $("toCoin").innerHTML=options;

 $("editFrom").innerHTML=options;
 $("editTo").innerHTML=options;

 $("fromCoin").value="BTC";
 $("toCoin").value="USDT";

 renderCoinCards();

 setSide("BUY");

 const savedTheme=
 localStorage.getItem("TABADOL_THEME") || "yellow";

 setTheme(savedTheme);

 fetchPrices();

 setInterval(fetchPrices,60000);

}


/* =========================
   COIN CARDS
========================= */

function renderCoinCards(){

 $("coinGrid").innerHTML=
 Object.keys(COINS).map(c=>{

 let price=
 prices[c] !== undefined
 ? "$"+Number(prices[c]).toLocaleString(
   "en-US",
   {maximumFractionDigits:8}
 )
 : "در حال دریافت...";

 return `

 <div class="coin-card">

   <div class="led"></div>

   <div class="coin-name">
     ${c}
   </div>

   <div class="coin-price">
     ${price}
   </div>

 </div>

 `;

 }).join("");

}


/* =========================
   LIVE PRICES
========================= */

async function fetchPrices(){

 try{

 const ids=
 Object.values(COINS)
 .map(x=>x.cg)
 .join(",");

 const response=
 await fetch(
 `https://api.coingecko.com/api/v3/simple/price?ids=${ids}&vs_currencies=usd`
 );

 const data=await response.json();

 Object.keys(COINS).forEach(c=>{

   const value=data[COINS[c].cg]?.usd;

   if(value !== undefined){
     prices[c]=value;
   }

 });

 renderCoinCards();

 calculateExchange();

 }

 catch(error){

 $("calculation").innerHTML=
 "⚠️ دریافت قیمت آنلاین ناموفق بود. اتصال اینترنت یا محدودیت API را بررسی کنید.";

 }

}


/* =========================
   BUY / SELL
========================= */

function setSide(side){

 currentSide=side;

 $("buyButton").classList.toggle(
 "selected",
 side==="BUY"
 );

 $("sellButton").classList.toggle(
 "selected",
 side==="SELL"
 );

 calculateExchange();

}


/* =========================
   CALCULATE
========================= */

function calculateExchange(){

 const from=$("fromCoin").value;

 const to=$("toCoin").value;

 const amount=
 Number($("fromAmount").value)||0;

 if(!prices[from] || !prices[to]){

 $("calculation").innerHTML=
 "در حال دریافت قیمت آنلاین...";

 return;

 }

 if(from===to){

 $("calculation").innerHTML=
 "⚠️ ارز مبدأ و مقصد باید متفاوت باشند.";

 $("toAmount").value="";

 return;

 }

 const result=
 amount * prices[from] / prices[to];

 $("toAmount").value=
 result ? result.toFixed(8) : "";

 $("calculation").innerHTML=

 `${currentSide}
 | ${from}: $${prices[from].toLocaleString()}
 | ${to}: $${prices[to].toLocaleString()}
 | مبلغ تقریبی دریافتی:
 <b>${result.toLocaleString(
 "en-US",
 {maximumFractionDigits:8}
 )} ${to}</b>`;

}


/* =========================
   PREPARE TRADE
========================= */

function prepareTrade(){

 const from=$("fromCoin").value;

 const to=$("toCoin").value;

 const amount=
 Number($("fromAmount").value);

 const userAddress=
 $("userAddress").value.trim();


 if(from===to){

 alert("ارز مبدأ و مقصد نباید یکسان باشند.");

 return;

 }


 if(!amount || amount<=0){

 alert("مبلغ مبدأ را وارد کنید.");

 return;

 }


 if(!userAddress){

 alert("آدرس کیف پول مقصد را وارد کنید.");

 return;

 }


 if(!prices[from] || !prices[to]){

 alert("قیمت آنلاین هنوز دریافت نشده است.");

 return;

 }


 const received=
 amount * prices[from] / prices[to];


 preparedTrade={

 side:currentSide,

 from,

 fromAmount:amount,

 to,

 toAmount:received,

 userAddress,

 depositAddress:COINS[from].address

 };


 $("depositBox").style.display="block";

 $("depositBox").innerHTML=

 `<b>آدرس واریز ${from}</b>
 <br><br>
 ${COINS[from].address}`;

 $("copyRegisterButton").style.display="block";

 $("successBox").style.display="none";

}


/* =========================
   REGISTER
========================= */

async function copyDepositAndRegister(){

 if(!preparedTrade) return;


 try{

 await navigator.clipboard.writeText(
 preparedTrade.depositAddress
 );

 }catch(e){}


 const now=new Date();

 const date=
 now.toISOString()
 .slice(0,10)
 .replaceAll("-","");


 const code=
 `TB-${date.slice(2)}-${Math.floor(
 100000+Math.random()*900000
 )}`;


 const trade={

 id:
 window.crypto?.randomUUID
 ? crypto.randomUUID()
 : String(Date.now()),

 code,

 ...preparedTrade,

 txid:"",

 status:"در انتظار پرداخت",

 createdAt:
 now.toLocaleString("fa-IR"),

 updatedAt:
 now.toLocaleString("fa-IR")

 };


 const trades=getTrades();

 trades.unshift(trade);

 saveTrades(trades);


 $("successBox").style.display="block";

 $("successBox").innerHTML=

 `

 معامله با موفقیت ثبت شد ✅

 <br>

 کد معامله:

 <b dir="ltr">${code}</b>

 <br>

 این کد را برای پیگیری معامله نگهداری کنید.

 <br>

 <button
 class="main-button"
 onclick="copyText('${code}')">

 📋 کپی کد معامله

 </button>

 `;


 $("copyRegisterButton").style.display="none";

}


/* =========================
   COPY
========================= */

function copyText(text){

 navigator.clipboard?.writeText(text);

}


/* =========================
   STORAGE
========================= */

function getTrades(){

 try{

 return JSON.parse(
 localStorage.getItem(STORAGE_KEY)||"[]"
 );

 }catch(e){

 return [];

 }

}


function saveTrades(trades){

 localStorage.setItem(
 STORAGE_KEY,
 JSON.stringify(trades)
 );

}


/* =========================
   MASK
========================= */

function maskValue(value){

 if(!value) return "—";

 if(value.length<12){

 return value.slice(0,4)+
 "••••"+
 value.slice(-3);

 }

 return value.slice(0,5)+
 "••••••••••"+
 value.slice(-5);

}


/* =========================
   TRACK
========================= */

function trackTrade(){

 const code=
 $("trackingCode")
 .value
 .trim()
 .toUpperCase();


 const trade=
 getTrades()
 .find(t=>t.code===code);


 if(!trade){

 $("trackingResult").innerHTML=

 `<div class="address-box"
 style="display:block">

 معامله‌ای با این کد پیدا نشد.

 </div>`;

 return;

 }


 $("trackingResult").innerHTML=

 `

 <div class="result-box">

 <b>کد معامله:</b>
 ${trade.code}

 <br>

 <b>نوع:</b>
 ${trade.side}

 <br>

 <b>مبدأ:</b>
 ${trade.from}
 —
 ${trade.fromAmount}

 <br>

 <b>مقصد:</b>
 ${trade.to}
 —
 ${trade.toAmount}

 <br>

 <b>آدرس دریافت:</b>
 <span dir="ltr">
 ${maskValue(trade.userAddress)}
 </span>

 <br>

 <b>آدرس واریز:</b>
 <span dir="ltr">
 ${maskValue(trade.depositAddress)}
 </span>

 <br>

 <b>TXID:</b>
 <span dir="ltr">
 ${maskValue(trade.txid)}
 </span>

 <br>

 <b>وضعیت:</b>

 <span class="status">
 ${trade.status}
 </span>

 <br>

 <b>آخرین بروزرسانی:</b>
 ${trade.updatedAt}

 </div>

 `;

}


/* =========================
   SETTINGS
========================= */

function openSettings(){

 $("settingsModal").style.display="block";

}


function openAdminLogin(){

 closeModal("settingsModal");

 $("adminPassword").value="";

 $("loginMessage").innerHTML="";

 $("loginModal").style.display="block";

}


function closeModal(id){

 $(id).style.display="none";

}


/* =========================
   THEME
========================= */

function setTheme(theme){

 document.body.className="";

 if(theme!=="yellow"){

 document.body.classList.add(
 "theme-"+theme
 );

 }

 localStorage.setItem(
 "TABADOL_THEME",
 theme
 );

}


/* =========================
   ADMIN LOGIN
========================= */

function loginAdmin(){

 if(
 $("adminPassword").value===
 ADMIN_PASSWORD
 ){

 closeModal("loginModal");

 renderAdmin();

 $("adminModal").style.display="block";

 }

 else{

 $("loginMessage").innerHTML=
 `<p style="color:red">
 رمز مدیریت اشتباه است.
 </p>`;

 }

}


/* =========================
   ADMIN PANEL
========================= */

function renderAdmin(){

 const trades=getTrades();


 $("totalTrades").textContent=
 trades.length;


 $("pendingTrades").textContent=
 trades.filter(
 t=>t.status==="در انتظار پرداخت"
 ).length;


 $("completedTrades").textContent=
 trades.filter(
 t=>t.status==="تکمیل شد"
 ).length;


 $("adminTable").innerHTML=
 trades.map(trade=>`

 <tr>

 <td dir="ltr">
 ${trade.code}
 </td>

 <td>
 ${trade.side}
 </td>

 <td>
 ${trade.from}
 </td>

 <td>
 ${trade.fromAmount}
 </td>

 <td>
 ${trade.to}
 </td>

 <td>
 ${trade.toAmount}
 </td>

 <td dir="ltr">
 ${trade.userAddress}
 </td>

 <td dir="ltr">
 ${trade.depositAddress}
 </td>

 <td dir="ltr">
 ${trade.txid || "—"}
 </td>

 <td>
 ${trade.status}
 </td>

 <td>
 ${trade.updatedAt}
 </td>

 <td>

 <button
 class="action-btn edit-btn"
 onclick="openEdit('${trade.id}')">

 ویرایش

 </button>

 <button
 class="action-btn done-btn"
 onclick="changeStatus(
 '${trade.id}',
 'تکمیل شد'
 )">

 تکمیل

 </button>

 <button
 class="action-btn wait-btn"
 onclick="changeStatus(
 '${trade.id}',
 'در انتظار پرداخت'
 )">

 انتظار

 </button>

 <button
 class="action-btn delete-btn"
 onclick="deleteTrade('${trade.id}')">

 حذف

 </button>

 </td>

 </tr>

 `).join("");

}


/* =========================
   EDIT
========================= */

function openEdit(id){

 const trade=
 getTrades().find(t=>t.id===id);

 if(!trade) return;


 $("editId").value=trade.id;

 $("editFrom").value=trade.from;

 $("editFromAmount").value=
 trade.fromAmount;

 $("editTo").value=trade.to;

 $("editToAmount").value=
 trade.toAmount;

 $("editUserAddress").value=
 trade.userAddress;

 $("editTxid").value=
 trade.txid;

 $("editStatus").value=
 trade.status;


 $("editModal").style.display="block";

}


/* =========================
   SAVE EDIT
========================= */

function saveEditedTrade(){

 const trades=getTrades();

 const index=
 trades.findIndex(
 t=>t.id===$("editId").value
 );


 if(index<0)return;


 trades[index].from=
 $("editFrom").value;

 trades[index].fromAmount=
 Number($("editFromAmount").value);

 trades[index].to=
 $("editTo").value;

 trades[index].toAmount=
 Number($("editToAmount").value);

 trades[index].userAddress=
 $("editUserAddress").value.trim();

 trades[index].txid=
 $("editTxid").value.trim();

 trades[index].status=
 $("editStatus").value;

 trades[index].updatedAt=
 new Date().toLocaleString("fa-IR");


 saveTrades(trades);

 closeModal("editModal");

 renderAdmin();

}


/* =========================
   CHANGE STATUS
========================= */

function changeStatus(id,status){

 const trades=getTrades();

 const trade=
 trades.find(t=>t.id===id);

 if(!trade)return;


 trade.status=status;

 trade.updatedAt=
 new Date().toLocaleString("fa-IR");


 saveTrades(trades);

 renderAdmin();

}


/* =========================
   DELETE
========================= */

function deleteTrade(id){

 if(!confirm(
 "آیا از حذف این معامله مطمئن هستید؟"
 ))return;


 const trades=
 getTrades().filter(t=>t.id!==id);


 saveTrades(trades);

 renderAdmin();

}


/* =========================
   START
========================= */

initialize();

</script>

</body>
</html>
```
