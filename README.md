
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>صرافی آنلاین ارز دیجیتال</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  font-family:Tahoma,Arial,sans-serif;
  background:linear-gradient(135deg,#fff700,#ffb300);
  min-height:100vh;
  color:#111;
  transition:.4s;
}

.container{
  width:min(1200px,94%);
  margin:auto;
  padding:20px 0 50px;
}

header{
  background:rgba(255,255,255,.95);
  border-radius:22px;
  padding:22px;
  text-align:center;
  box-shadow:0 8px 30px rgba(0,0,0,.15);
  margin-bottom:20px;
}

.logo{
  font-size:32px;
  font-weight:bold;
}

.subtitle{
  margin-top:8px;
  color:#555;
}

.live-box{
  margin-top:15px;
  display:flex;
  justify-content:center;
  align-items:center;
  gap:8px;
  font-weight:bold;
}

.live-dot{
  width:12px;
  height:12px;
  background:#16a34a;
  border-radius:50%;
  box-shadow:0 0 12px #16a34a;
  animation:pulse 1.3s infinite;
}

.live-dot.off{
  background:#dc2626;
  box-shadow:0 0 12px #dc2626;
}

@keyframes pulse{
  50%{opacity:.35}
}

/* MARKET */

.market-title{
  text-align:center;
  font-size:25px;
  margin:20px 0 15px;
  font-weight:bold;
}

.market-grid{
  display:grid;
  grid-template-columns:repeat(6,1fr);
  gap:12px;
}

.coin-card{
  background:rgba(255,255,255,.96);
  border-radius:18px;
  padding:16px 10px;
  text-align:center;
  box-shadow:0 6px 20px rgba(0,0,0,.12);
  transition:.25s;
}

.coin-card:hover{
  transform:translateY(-4px);
}

.coin-name{
  font-size:18px;
  font-weight:bold;
}

.coin-price{
  font-size:19px;
  font-weight:bold;
  margin:12px 0 7px;
  direction:ltr;
}

.coin-toman{
  color:#555;
  font-size:13px;
  min-height:18px;
}

.status{
  margin-top:10px;
  font-size:12px;
  font-weight:bold;
  color:#16a34a;
}

.status.offline{
  color:#dc2626;
}

/* EXCHANGE */

.exchange{
  background:rgba(255,255,255,.97);
  border-radius:25px;
  padding:25px;
  margin-top:25px;
  box-shadow:0 10px 35px rgba(0,0,0,.15);
}

.exchange h2{
  text-align:center;
  margin-bottom:22px;
}

.exchange-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:20px;
}

.box{
  background:#fafafa;
  border:2px solid #eee;
  border-radius:20px;
  padding:18px;
}

.box label{
  display:block;
  font-weight:bold;
  margin-bottom:10px;
}

select,
input{
  width:100%;
  border:2px solid #ddd;
  border-radius:14px;
  padding:15px;
  font-size:17px;
  outline:none;
  background:white;
}

select:focus,
input:focus{
  border-color:#f5b400;
}

.rate{
  margin:20px 0;
  padding:18px;
  border-radius:18px;
  background:#111;
  color:white;
  text-align:center;
  font-size:18px;
}

.rate strong{
  color:#ffe600;
}

.result{
  margin-top:12px;
  background:#fff7cc;
  border-radius:15px;
  padding:14px;
  font-weight:bold;
  text-align:center;
}

.wallet-section{
  margin-top:25px;
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:20px;
}

.wallet{
  background:#fff;
  border-radius:20px;
  padding:20px;
  border:2px solid #eee;
}

.wallet h3{
  margin-bottom:12px;
}

.address{
  direction:ltr;
  text-align:left;
  word-break:break-all;
  background:#f3f3f3;
  padding:13px;
  border-radius:12px;
  font-size:13px;
}

.copy-btn{
  width:100%;
  margin-top:10px;
  border:0;
  border-radius:12px;
  padding:12px;
  background:#111;
  color:#fff;
  cursor:pointer;
  font-weight:bold;
}

.copy-btn:hover{
  opacity:.85;
}

.submit-btn{
  width:100%;
  margin-top:22px;
  padding:17px;
  border:0;
  border-radius:16px;
  background:#111;
  color:#fff;
  font-size:19px;
  font-weight:bold;
  cursor:pointer;
}

.submit-btn:hover{
  background:#222;
}

/* TRACKING */

.tracking{
  margin-top:25px;
  background:rgba(255,255,255,.97);
  border-radius:25px;
  padding:25px;
  box-shadow:0 10px 35px rgba(0,0,0,.12);
}

.tracking h2{
  text-align:center;
  margin-bottom:18px;
}

.track-row{
  display:flex;
  gap:10px;
}

.track-row input{
  flex:1;
}

.track-row button{
  width:150px;
  border:0;
  border-radius:14px;
  background:#111;
  color:white;
  font-weight:bold;
  cursor:pointer;
}

.track-result{
  margin-top:15px;
  padding:15px;
  border-radius:14px;
  background:#f5f5f5;
  display:none;
}

/* TRANSACTIONS */

.transactions{
  margin-top:25px;
  background:rgba(255,255,255,.97);
  border-radius:25px;
  padding:25px;
  box-shadow:0 10px 35px rgba(0,0,0,.12);
}

.transactions h2{
  text-align:center;
  margin-bottom:18px;
}

.table-wrap{
  overflow-x:auto;
}

table{
  width:100%;
  border-collapse:collapse;
  min-width:850px;
}

th,td{
  padding:13px;
  border-bottom:1px solid #ddd;
  text-align:center;
}

th{
  background:#111;
  color:#fff;
}

.pending{
  color:#d97706;
  font-weight:bold;
}

.done{
  color:#16a34a;
  font-weight:bold;
}

footer{
  text-align:center;
  color:#333;
  margin-top:30px;
  font-size:13px;
}

/* THEMES */

.themes{
  display:flex;
  justify-content:center;
  gap:10px;
  margin-top:15px;
}

.theme{
  border:2px solid #111;
  border-radius:12px;
  padding:8px 13px;
  cursor:pointer;
  background:#fff;
}

/* MOBILE */

@media(max-width:900px){
  .market-grid{
    grid-template-columns:repeat(3,1fr);
  }
}

@media(max-width:600px){
  .market-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .exchange-grid,
  .wallet-section{
    grid-template-columns:1fr;
  }

  .track-row{
    flex-direction:column;
  }

  .track-row button{
    width:100%;
    padding:14px;
  }

  .logo{
    font-size:25px;
  }
}
</style>
</head>

<body>

<div class="container">

<header>
  <div class="logo">صرافی آنلاین</div>
  <div class="subtitle">
    خرید، فروش و تبدیل ارزهای دیجیتال
  </div>

  <div class="live-box">
    <span class="live-dot" id="globalDot"></span>
    <span id="globalStatus">در حال دریافت قیمت آنلاین...</span>
  </div>

  <div class="themes">
    <button class="theme" onclick="setTheme('yellow')">زرد</button>
    <button class="theme" onclick="setTheme('blue')">آبی</button>
    <button class="theme" onclick="setTheme('purple')">بنفش</button>
    <button class="theme" onclick="setTheme('orange')">نارنجی</button>
  </div>
</header>


<div class="market-title">
  قیمت لحظه‌ای ارزها
</div>

<div class="market-grid" id="marketGrid"></div>


<section class="exchange">

<h2>تبدیل ارز دیجیتال</h2>

<div class="exchange-grid">

  <div class="box">

    <label>ارزی که ارسال می‌کنید</label>

    <select id="fromCoin" onchange="calculate()">
      <option value="BTC">BTC</option>
      <option value="BCH">BCH</option>
      <option value="TRX">TRX</option>
      <option value="LTC">LTC</option>
      <option value="DOGE">DOGE</option>
      <option value="USDT">USDT</option>
    </select>

    <br><br>

    <label>مقدار ارسال</label>

    <input
      id="amount"
      type="number"
      min="0"
      step="any"
      placeholder="مثلاً 0.01"
      oninput="calculate()"
    >

    <div class="result">
      ارزش تقریبی:
      <span id="sendUsd">0</span> USDT
    </div>

  </div>


  <div class="box">

    <label>ارزی که دریافت می‌کنید</label>

    <select id="toCoin" onchange="calculate()">
      <option value="DOGE">DOGE</option>
      <option value="BTC">BTC</option>
      <option value="BCH">BCH</option>
      <option value="TRX">TRX</option>
      <option value="LTC">LTC</option>
      <option value="USDT">USDT</option>
    </select>

    <br><br>

    <label>مقدار دریافت</label>

    <input
      id="receive"
      type="text"
      readonly
      placeholder="محاسبه خودکار"
    >

    <div class="result">
      ارزش دریافتی:
      <span id="receiveUsd">0</span> USDT
    </div>

  </div>

</div>


<div class="rate">
  نرخ تبدیل:
  <strong id="rateText">در انتظار قیمت آنلاین...</strong>
</div>


<div class="wallet-section">

  <div class="wallet">
    <h3>آدرس واریز ارز ارسالی</h3>

    <div class="address" id="depositAddress">
      ابتدا ارز را انتخاب کنید
    </div>

    <button class="copy-btn" onclick="copyDeposit()">
      کپی آدرس
    </button>
  </div>


  <div class="wallet">
    <h3>آدرس کیف پول دریافت‌کننده</h3>

    <input
      id="receiveWallet"
      type="text"
      placeholder="آدرس کیف پول خود را وارد کنید"
      dir="ltr"
    >
  </div>

</div>


<button class="submit-btn" onclick="submitExchange()">
  ثبت درخواست تبدیل
</button>

</section>


<section class="tracking">

<h2>پیگیری تراکنش</h2>

<div class="track-row">

<input
  id="trackInput"
  placeholder="کد پیگیری را وارد کنید"
  dir="ltr"
>

<button onclick="trackTransaction()">
  پیگیری
</button>

</div>

<div class="track-result" id="trackResult"></div>

</section>


<section class="transactions">

<h2>تراکنش‌های ثبت‌شده</h2>

<div class="table-wrap">

<table>

<thead>
<tr>
  <th>کد پیگیری</th>
  <th>ارسال</th>
  <th>دریافت</th>
  <th>مقدار ارسال</th>
  <th>مقدار دریافت</th>
  <th>ارزش USDT</th>
  <th>کیف پول</th>
  <th>زمان</th>
  <th>وضعیت</th>
</tr>
</thead>

<tbody id="transactionsBody"></tbody>

</table>

</div>

</section>


<footer>
  قیمت‌ها به صورت آنلاین دریافت می‌شوند و هر ۲۰ ثانیه به‌روزرسانی می‌شوند.
</footer>

</div>


<script>

/* =========================
   تنظیمات
========================= */

const API =
"https://api.lbkex.com/v2/ticker/24hr.do";


const coins = [
  "BTC",
  "BCH",
  "TRX",
  "LTC",
  "DOGE",
  "USDT"
];


const wallets = {

  BTC:
  "1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

  BCH:
  "bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

  TRX:
  "TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3",

  LTC:
  "LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

  DOGE:
  "DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

  USDT:
  "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6"

};


let prices = {
  BTC:null,
  BCH:null,
  TRX:null,
  LTC:null,
  DOGE:null,
  USDT:1
};


/* =========================
   دریافت قیمت LBank
========================= */

async function getLBankPrice(symbol){

  if(symbol === "USDT"){
    return 1;
  }

  const pair =
    symbol.toLowerCase() + "_usdt";

  try{

    const response =
      await fetch(
        API +
        "?symbol=" +
        encodeURIComponent(pair) +
        "&_=" +
        Date.now(),
        {
          cache:"no-store"
        }
      );

    if(!response.ok){
      throw new Error("HTTP " + response.status);
    }

    const json =
      await response.json();

    /*
      ساختار API ممکن است بسته به نسخه
      کمی متفاوت باشد، بنابراین چند حالت
      رایج بررسی می‌شود.
    */

    let price = null;

    if(json && json.data){

      if(Array.isArray(json.data)){

        const item = json.data[0];

        if(item){

          price =
            Number(
              item.latest ??
              item.latestPrice ??
              item.price ??
              item.close
            );

        }

      }else{

        price =
          Number(
            json.data.latest ??
            json.data.latestPrice ??
            json.data.price ??
            json.data.close
          );

      }

    }

    if(!Number.isFinite(price) || price <= 0){

      if(json && json.data && Array.isArray(json.data.ticker)){

        price =
          Number(
            json.data.ticker[0]?.latest
          );

      }

    }

    if(!Number.isFinite(price) || price <= 0){

      throw new Error("قیمت معتبر دریافت نشد");

    }

    return price;

  }catch(error){

    console.error(
      "LBank " + symbol,
      error
    );

    return null;
  }
}


/* =========================
   دریافت تمام قیمت‌ها
========================= */

async function updatePrices(){

  setGlobalStatus(
    "در حال دریافت قیمت آنلاین...",
    false
  );

  const results =
    await Promise.all(
      coins
        .filter(c => c !== "USDT")
        .map(async coin => {

          const price =
            await getLBankPrice(coin);

          return {
            coin,
            price
          };

        })
    );


  let onlineCount = 0;


  results.forEach(item => {

    if(
      item.price !== null &&
      Number.isFinite(item.price)
    ){

      prices[item.coin] =
        item.price;

      onlineCount++;

    }else{

      prices[item.coin] =
        null;

    }

  });


  prices.USDT = 1;


  renderMarket();
  calculate();
  updateDepositAddress();


  if(onlineCount === 5){

    setGlobalStatus(
      "قیمت‌ها آنلاین هستند • بروزرسانی هر ۲۰ ثانیه",
      true
    );

  }else if(onlineCount > 0){

    setGlobalStatus(
      onlineCount +
      " ارز آنلاین است • بعضی قیمت‌ها در دسترس نیست",
      true
    );

  }else{

    setGlobalStatus(
      "اتصال قیمت‌ها قطع است",
      false
    );

  }

}


/* =========================
   وضعیت کلی
========================= */

function setGlobalStatus(text, online){

  document.getElementById(
    "globalStatus"
  ).textContent = text;

  const dot =
    document.getElementById(
      "globalDot"
    );

  if(online){

    dot.classList.remove("off");

  }else{

    dot.classList.add("off");

  }

}


/* =========================
   نمایش بازار
========================= */

function renderMarket(){

  const grid =
    document.getElementById(
      "marketGrid"
    );

  grid.innerHTML = "";

  coins.forEach(coin => {

    const price =
      prices[coin];

    const online =
      price !== null &&
      Number.isFinite(price);

    const card =
      document.createElement("div");

    card.className =
      "coin-card";

    card.innerHTML = `

      <div class="coin-name">
        ${coin}
      </div>

      <div class="coin-price">
        ${
          online
          ? formatPrice(price) + " USDT"
          : "در انتظار..."
        }
      </div>

      <div class="coin-toman">
        ارزش تومانی از API قیمت تومانی دریافت نمی‌شود
      </div>

      <div class="status ${online ? "" : "offline"}">
        ${online ? "● آنلاین" : "● قطع"}
      </div>

    `;

    grid.appendChild(card);

  });

}


/* =========================
   فرمت قیمت
========================= */

function formatPrice(value){

  if(value === null ||
     !Number.isFinite(value))
    return "—";

  if(value >= 1000){

    return value.toLocaleString(
      "en-US",
      {
        maximumFractionDigits:2
      }
    );

  }

  if(value >= 1){

    return value.toLocaleString(
      "en-US",
      {
        maximumFractionDigits:6
      }
    );

  }

  return value.toLocaleString(
    "en-US",
    {
      maximumFractionDigits:10
    }
  );

}


/* =========================
   محاسبه تبدیل
========================= */

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
        "amount"
      ).value
    );


  const fromPrice =
    prices[from];

  const toPrice =
    prices[to];


  if(
    fromPrice === null ||
    toPrice === null ||
    !Number.isFinite(amount) ||
    amount <= 0
  ){

    document.getElementById(
      "receive"
    ).value = "";

    document.getElementById(
      "sendUsd"
    ).textContent = "0";

    document.getElementById(
      "receiveUsd"
    ).textContent = "0";

    document.getElementById(
      "rateText"
    ).textContent =
      "در انتظار قیمت آنلاین...";

    return;

  }


  const sendUsd =
    amount * fromPrice;


  const receiveAmount =
    sendUsd / toPrice;


  document.getElementById(
    "receive"
  ).value =
    receiveAmount.toLocaleString(
      "en-US",
      {
        maximumFractionDigits:12
      }
    );


  document.getElementById(
    "sendUsd"
  ).textContent =
    formatPrice(sendUsd);


  document.getElementById(
    "receiveUsd"
  ).textContent =
    formatPrice(
      receiveAmount * toPrice
    );


  const rate =
    fromPrice / toPrice;


  document.getElementById(
    "rateText"
  ).innerHTML =
    `1 ${from} = <strong>${
      formatPrice(rate)
    }</strong> ${to}`;

}


/* =========================
   آدرس واریز
========================= */

function updateDepositAddress(){

  const coin =
    document.getElementById(
      "fromCoin"
    ).value;

  document.getElementById(
    "depositAddress"
  ).textContent =
    wallets[coin] ||
    "آدرس موجود نیست";

}


document.getElementById(
  "fromCoin"
).addEventListener(
  "change",
  updateDepositAddress
);


/* =========================
   کپی آدرس
========================= */

async function copyDeposit(){

  const address =
    document.getElementById(
      "depositAddress"
    ).textContent;

  if(
    !address ||
    address.includes("انتخاب")
  ){

    alert("ابتدا ارز را انتخاب کنید");
    return;

  }

  try{

    await navigator.clipboard.writeText(
      address
    );

    alert("آدرس کپی شد");

  }catch(e){

    const temp =
      document.createElement("textarea");

    temp.value = address;

    document.body.appendChild(temp);

    temp.select();

    document.execCommand("copy");

    temp.remove();

    alert("آدرس کپی شد");

  }

}


/* =========================
   ثبت تراکنش
========================= */

function submitExchange(){

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
        "amount"
      ).value
    );

  const receive =
    document.getElementById(
      "receive"
    ).value;

  const wallet =
    document.getElementById(
      "receiveWallet"
    ).value.trim();


  if(!amount || amount <= 0){

    alert("مقدار ارسال را وارد کنید");
    return;

  }

  if(!receive){

    alert("قیمت آنلاین هنوز دریافت نشده");
    return;

  }

  if(!wallet){

    alert("آدرس کیف پول دریافت‌کننده را وارد کنید");
    return;

  }


  const id =
    "EX" +
    Date.now()
      .toString()
      .slice(-10);


  const item = {

    id,

    from,

    to,

    amount,

    receive,

    usd:
      formatPrice(
        amount * prices[from]
      ),

    wallet,

    time:
      new Date().toLocaleString(
        "fa-IR"
      ),

    status:
      "در حال بررسی"

  };


  const list =
    JSON.parse(
      localStorage.getItem(
        "exchangeTransactions"
      ) || "[]"
    );


  list.unshift(item);


  localStorage.setItem(
    "exchangeTransactions",
    JSON.stringify(list)
  );


  document.getElementById(
    "trackInput"
  ).value = id;


  renderTransactions();


  alert(
    "درخواست ثبت شد\nکد پیگیری: " +
    id
  );

}


/* =========================
   تراکنش‌ها
========================= */

function renderTransactions(){

  const body =
    document.getElementById(
      "transactionsBody"
    );

  const list =
    JSON.parse(
      localStorage.getItem(
        "exchangeTransactions"
      ) || "[]"
    );


  body.innerHTML = "";


  list.forEach(item => {

    const tr =
      document.createElement("tr");


    const statusClass =
      item.status === "انجام شد"
      ? "done"
      : "pending";


    tr.innerHTML = `

      <td dir="ltr">
        ${item.id}
      </td>

      <td>
        ${item.from}
      </td>

      <td>
        ${item.to}
      </td>

      <td dir="ltr">
        ${item.amount}
      </td>

      <td dir="ltr">
        ${item.receive}
      </td>

      <td dir="ltr">
        ${item.usd}
      </td>

      <td dir="ltr">
        ${item.wallet}
      </td>

      <td>
        ${item.time}
      </td>

      <td class="${statusClass}">
        ${item.status}
      </td>

    `;


    body.appendChild(tr);

  });

}


/* =========================
   پیگیری
========================= */

function trackTransaction(){

  const id =
    document.getElementById(
      "trackInput"
    ).value.trim();


  const result =
    document.getElementById(
      "trackResult"
    );


  if(!id){

    alert("کد پیگیری را وارد کنید");
    return;

  }


  const list =
    JSON.parse(
      localStorage.getItem(
        "exchangeTransactions"
      ) || "[]"
    );


  const item =
    list.find(
      x => x.id === id
    );


  result.style.display =
    "block";


  if(!item){

    result.innerHTML =
      "<b>تراکنشی با این کد پیدا نشد.</b>";

    return;

  }


  result.innerHTML = `

    <div>
      <b>کد پیگیری:</b>
      ${item.id}
    </div>

    <br>

    <div>
      <b>ارسال:</b>
      ${item.amount} ${item.from}
    </div>

    <br>

    <div>
      <b>دریافت:</b>
      ${item.receive} ${item.to}
    </div>

    <br>

    <div>
      <b>ارزش:</b>
      ${item.usd} USDT
    </div>

    <br>

    <div>
      <b>وضعیت:</b>
      ${item.status}
    </div>

  `;

}


/* =========================
   تغییر رنگ
========================= */

function setTheme(theme){

  if(theme === "yellow"){

    document.body.style.background =
      "linear-gradient(135deg,#fff700,#ffb300)";

  }

  if(theme === "blue"){

    document.body.style.background =
      "linear-gradient(135deg,#60a5fa,#2563eb)";

  }

  if(theme === "purple"){

    document.body.style.background =
      "linear-gradient(135deg,#c084fc,#7e22ce)";

  }

  if(theme === "orange"){

    document.body.style.background =
      "linear-gradient(135deg,#fb923c,#ea580c)";

  }

}


/* =========================
   شروع سایت
========================= */

updateDepositAddress();

renderTransactions();

updatePrices();


/*
  بروزرسانی قیمت هر 20 ثانیه
*/

setInterval(
  updatePrices,
  20000
);

</script>

</body>
</html>
