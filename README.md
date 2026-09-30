Exchange tab

<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>صرافی آنلاین</title>

<style>
:root{
  --main:#00c853;
  --main2:#00a844;
  --bg:#07130d;
  --card:#0d2116;
  --text:#fff;
  --muted:#9bb0a2;
  --border:#183b26;
  --danger:#ff5252;
  --warning:#ffb300;
}

*{box-sizing:border-box}

body{
  margin:0;
  font-family:Tahoma,Arial,sans-serif;
  background:
    radial-gradient(circle at top,#12351e 0,#07130d 45%,#030805 100%);
  color:var(--text);
  min-height:100vh;
}

header{
  position:sticky;
  top:0;
  z-index:50;
  background:rgba(4,12,7,.92);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
  padding:15px;
}

.header{
  max-width:1100px;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
}

.logo{
  font-size:22px;
  font-weight:bold;
  color:var(--main);
}

.logo span{
  color:white;
}

.settings{
  background:#10261a;
  border:1px solid var(--border);
  color:white;
  padding:10px 14px;
  border-radius:12px;
  cursor:pointer;
}

.container{
  width:min(1100px,94%);
  margin:25px auto 60px;
}

.hero{
  text-align:center;
  padding:25px 10px;
}

.hero h1{
  margin:0 0 10px;
  font-size:30px;
}

.hero p{
  color:var(--muted);
  margin:0;
}

.section-title{
  margin:28px 0 14px;
  font-size:20px;
}

.market-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:14px;
}

.market{
  background:linear-gradient(145deg,#10271a,#09170e);
  border:1px solid var(--border);
  border-radius:18px;
  padding:18px;
  box-shadow:0 8px 30px rgba(0,0,0,.2);
}

.market-top{
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.coin{
  font-size:18px;
  font-weight:bold;
}

.live{
  display:flex;
  align-items:center;
  gap:6px;
  color:#64ff91;
  font-size:11px;
}

.dot{
  width:8px;
  height:8px;
  border-radius:50%;
  background:#00e676;
  box-shadow:0 0 10px #00e676;
  animation:blink 1.2s infinite;
}

@keyframes blink{
  50%{opacity:.25}
}

.price{
  margin-top:16px;
  font-size:20px;
  font-weight:bold;
}

.usdt,.toman{
  margin-top:7px;
  color:var(--muted);
  font-size:13px;
}

.card{
  background:rgba(10,29,17,.94);
  border:1px solid var(--border);
  border-radius:20px;
  padding:20px;
  margin-top:20px;
  box-shadow:0 10px 35px rgba(0,0,0,.25);
}

.form-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:14px;
}

.field{
  margin-bottom:14px;
}

label{
  display:block;
  margin-bottom:7px;
  font-size:13px;
  color:#b9c9bf;
}

input,select{
  width:100%;
  background:#06100a;
  color:white;
  border:1px solid #244a31;
  border-radius:12px;
  padding:13px;
  outline:none;
}

input:focus,select:focus{
  border-color:var(--main);
}

button{
  border:0;
  cursor:pointer;
  font-family:inherit;
}

.primary{
  width:100%;
  padding:14px;
  border-radius:13px;
  color:#001c0a;
  font-weight:bold;
  background:linear-gradient(135deg,var(--main),#72ff9b);
  margin-top:5px;
}

.result{
  display:none;
  margin-top:15px;
  background:#07170d;
  border:1px solid #205f34;
  border-radius:15px;
  padding:15px;
}

.result-row{
  display:flex;
  justify-content:space-between;
  gap:15px;
  padding:7px 0;
  border-bottom:1px solid #14311e;
}

.result-row:last-child{
  border-bottom:0;
}

.wallet-box{
  background:#06100a;
  border:1px dashed #2d633c;
  padding:14px;
  border-radius:13px;
  word-break:break-all;
  line-height:1.8;
}

.copy{
  background:#163c24;
  color:white;
  padding:8px 12px;
  border-radius:9px;
  margin-top:8px;
}

.track{
  display:flex;
  gap:10px;
}

.track input{
  flex:1;
}

.track button{
  background:var(--main);
  color:#001c0a;
  padding:0 20px;
  border-radius:12px;
  font-weight:bold;
}

/* transactions */

.transactions{
  margin-top:35px;
}

.transaction{
  background:linear-gradient(145deg,#0c2014,#07140c);
  border:1px solid var(--border);
  border-radius:17px;
  padding:16px;
  margin-bottom:12px;
}

.tx-top{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:10px;
  margin-bottom:12px;
}

.tx-code{
  font-weight:bold;
  color:var(--main);
}

.status{
  padding:6px 10px;
  border-radius:30px;
  font-size:11px;
}

.pending{
  background:rgba(255,179,0,.13);
  color:#ffc107;
  border:1px solid rgba(255,179,0,.35);
}

.done{
  background:rgba(0,230,118,.12);
  color:#00e676;
  border:1px solid rgba(0,230,118,.35);
}

.tx-info{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:8px;
  color:#b9c9bf;
  font-size:13px;
}

.address{
  word-break:break-all;
  color:#fff;
}

.empty{
  text-align:center;
  padding:25px;
  color:#7f9687;
}

.modal{
  display:none;
  position:fixed;
  inset:0;
  z-index:100;
  background:rgba(0,0,0,.72);
  align-items:center;
  justify-content:center;
  padding:20px;
}

.modal-box{
  width:min(430px,100%);
  background:#0a1b10;
  border:1px solid var(--border);
  border-radius:20px;
  padding:20px;
}

.theme-list{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin-top:15px;
}

.theme-btn{
  padding:13px;
  border-radius:12px;
  color:white;
  background:#14251a;
  border:1px solid #284c33;
}

.close{
  background:#222;
  color:white;
  padding:10px;
  border-radius:10px;
  width:100%;
  margin-top:15px;
}

.notice{
  margin-top:12px;
  color:#8ea796;
  font-size:12px;
  line-height:1.8;
}

@media(max-width:650px){
  .form-grid,
  .tx-info{
    grid-template-columns:1fr;
  }

  .track{
    flex-direction:column;
  }

  .track button{
    padding:13px;
  }

  .hero h1{
    font-size:25px;
  }
}
</style>
</head>

<body>

<header>
  <div class="header">
    <div class="logo">صرافی <span>آنلاین</span></div>
    <button class="settings" onclick="openSettings()">⚙ تنظیمات</button>
  </div>
</header>

<div class="container">

<section class="hero">
  <h1>تبادل سریع ارزهای دیجیتال</h1>
  <p>تبدیل ارز، ثبت درخواست و پیگیری تراکنش</p>
</section>

<h2 class="section-title">قیمت لحظه‌ای</h2>

<div class="market-grid">

  <div class="market">
    <div class="market-top">
      <div class="coin">₿ BTC</div>
      <div class="live"><span class="dot"></span> آنلاین</div>
    </div>
    <div class="price" id="btcPrice">در حال دریافت...</div>
    <div class="usdt" id="btcUsdt">USDT: --</div>
    <div class="toman" id="btcToman">تومان: --</div>
  </div>

  <div class="market">
    <div class="market-top">
      <div class="coin">Ð DOGE</div>
      <div class="live"><span class="dot"></span> آنلاین</div>
    </div>
    <div class="price" id="dogePrice">در حال دریافت...</div>
    <div class="usdt" id="dogeUsdt">USDT: --</div>
    <div class="toman" id="dogeToman">تومان: --</div>
  </div>

  <div class="market">
    <div class="market-top">
      <div class="coin">Ł LTC</div>
      <div class="live"><span class="dot"></span> آنلاین</div>
    </div>
    <div class="price" id="ltcPrice">در حال دریافت...</div>
    <div class="usdt" id="ltcUsdt">USDT: --</div>
    <div class="toman" id="ltcToman">تومان: --</div>
  </div>

  <div class="market">
    <div class="market-top">
      <div class="coin">₮ USDT</div>
      <div class="live"><span class="dot"></span> آنلاین</div>
    </div>
    <div class="price" id="usdtPrice">1 USDT</div>
    <div class="usdt">USDT: 1</div>
    <div class="toman" id="usdtToman">تومان: --</div>
  </div>

</div>

<h2 class="section-title">تبادل ارز</h2>

<div class="card">

  <div class="form-grid">

    <div class="field">
      <label>ارزی که می‌فرستید</label>
      <select id="fromCoin" onchange="calculate()">
        <option value="BTC">BTC</option>
        <option value="DOGE">DOGE</option>
        <option value="LTC">LTC</option>
        <option value="USDT">USDT</option>
        <option value="TRX">TRX</option>
        <option value="BCH">BCH</option>
      </select>
    </div>

    <div class="field">
      <label>ارزی که دریافت می‌کنید</label>
      <select id="toCoin" onchange="calculate()">
        <option value="DOGE">DOGE</option>
        <option value="BTC">BTC</option>
        <option value="LTC">LTC</option>
        <option value="USDT">USDT</option>
        <option value="TRX">TRX</option>
        <option value="BCH">BCH</option>
      </select>
    </div>

  </div>

  <div class="field">
    <label>مقدار ارز</label>
    <input id="amount" type="number" step="any" placeholder="مثلاً 100" oninput="calculate()">
  </div>

  <div class="result" id="result">
    <div class="result-row">
      <span>مقدار دریافتی</span>
      <strong id="receiveAmount">--</strong>
    </div>

    <div class="result-row">
      <span>ارزش دلاری</span>
      <strong id="receiveUsdt">-- USDT</strong>
    </div>

    <div class="result-row">
      <span>ارزش تومانی</span>
      <strong id="receiveToman">-- تومان</strong>
    </div>
  </div>

  <div class="field" style="margin-top:15px">
    <label>آدرس کیف پول دریافت‌کننده شما</label>
    <input id="userAddress" placeholder="آدرس کیف پول خود را وارد کنید">
  </div>

  <button class="primary" onclick="submitTransaction()">
    ثبت درخواست تبادل
  </button>

</div>

<h2 class="section-title">آدرس‌های واریز صرافی</h2>

<div class="card">

  <div class="field">
    <label>ارز انتخابی برای واریز</label>

    <select id="depositCoin" onchange="showDepositAddress()">
      <option value="BTC">BTC</option>
      <option value="BCH">BCH</option>
      <option value="TRX">TRX</option>
      <option value="LTC">LTC</option>
      <option value="DOGE">DOGE</option>
      <option value="USDT">USDT BEP20</option>
    </select>
  </div>

  <div class="wallet-box">
    <div id="depositAddress"></div>
    <button class="copy" onclick="copyDeposit()">کپی آدرس</button>
  </div>

  <div class="notice">
    پس از ارسال ارز، درخواست خود را ثبت کنید تا تراکنش در پنل پایین سایت نمایش داده شود.
  </div>

</div>

<h2 class="section-title">پیگیری تراکنش</h2>

<div class="card">

  <div class="track">
    <input id="trackingInput" placeholder="کد پیگیری را وارد کنید">
    <button onclick="trackTransaction()">پیگیری</button>
  </div>

  <div id="trackResult" class="result"></div>

</div>

<!-- پنل عمومی تراکنش‌ها -->

<section class="transactions">

  <h2 class="section-title">
    تراکنش‌های صرافی
  </h2>

  <div id="transactionList">
    <div class="empty">
      هنوز تراکنشی ثبت نشده است.
    </div>
  </div>

</section>

</div>

<!-- تنظیمات -->

<div class="modal" id="settingsModal">

  <div class="modal-box">

    <h3>تنظیمات سایت</h3>

    <p style="color:#9bb0a2;font-size:13px">
      انتخاب رنگ سایت
    </p>

    <div class="theme-list">

      <button class="theme-btn" onclick="setTheme('green')">
        🟢 سبز
      </button>

      <button class="theme-btn" onclick="setTheme('blue')">
        🔵 آبی
      </button>

      <button class="theme-btn" onclick="setTheme('purple')">
        🟣 بنفش
      </button>

      <button class="theme-btn" onclick="setTheme('orange')">
        🟠 نارنجی
      </button>

    </div>

    <button class="close" onclick="closeSettings()">بستن</button>

  </div>

</div>

<script>

/* =========================
   آدرس‌های صرافی
========================= */

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


/* =========================
   قیمت‌ها
   این مقادیر موقت هستند.
   برای قیمت زنده بیت برگ باید
   API واقعی آن سرویس وصل شود.
========================= */

let prices = {

  BTC: 110000,
  DOGE: 0.25,
  LTC: 100,
  USDT: 1,
  TRX: 0.34,
  BCH: 500

};

let tomanUSDT = 100000;


/* =========================
   نمایش آدرس واریز
========================= */

function showDepositAddress(){

  const coin =
    document.getElementById("depositCoin").value;

  document.getElementById("depositAddress").innerText =
    wallets[coin];

}

showDepositAddress();


function copyDeposit(){

  const text =
    document.getElementById("depositAddress").innerText;

  navigator.clipboard.writeText(text);

  alert("آدرس کپی شد");

}


/* =========================
   محاسبه تبدیل
========================= */

function calculate(){

  const amount =
    parseFloat(document.getElementById("amount").value);

  const from =
    document.getElementById("fromCoin").value;

  const to =
    document.getElementById("toCoin").value;

  const result =
    document.getElementById("result");

  if(!amount || amount <= 0){

    result.style.display = "none";

    return;
  }

  const usdValue =
    amount * prices[from];

  const receive =
    usdValue / prices[to];

  const toman =
    usdValue * tomanUSDT;

  result.style.display = "block";

  document.getElementById("receiveAmount").innerText =
    receive.toLocaleString(undefined,{
      maximumFractionDigits:8
    }) + " " + to;

  document.getElementById("receiveUsdt").innerText =
    usdValue.toLocaleString(undefined,{
      maximumFractionDigits:2
    }) + " USDT";

  document.getElementById("receiveToman").innerText =
    toman.toLocaleString() + " تومان";

}


/* =========================
   کد پیگیری
========================= */

function generateTracking(){

  const random =
    Math.random().toString(36)
    .substring(2,8)
    .toUpperCase();

  return "EX-" +
    Date.now().toString().slice(-6) +
    "-" +
    random;

}


/* =========================
   ثبت تراکنش
========================= */

function submitTransaction(){

  const amount =
    parseFloat(document.getElementById("amount").value);

  const from =
    document.getElementById("fromCoin").value;

  const to =
    document.getElementById("toCoin").value;

  const address =
    document.getElementById("userAddress").value.trim();

  if(!amount || amount <= 0){

    alert("مقدار ارز را وارد کنید");

    return;
  }

  if(!address){

    alert("آدرس دریافت‌کننده را وارد کنید");

    return;
  }

  if(from === to){

    alert("ارز مبدا و مقصد نباید یکسان باشند");

    return;
  }

  const usd =
    amount * prices[from];

  const receive =
    usd / prices[to];

  const tx = {

    id:generateTracking(),

    from:from,

    to:to,

    amount:amount,

    receive:receive,

    usdt:usd,

    toman:usd * tomanUSDT,

    address:address,

    status:"در حال بررسی",

    time:new Date().toLocaleString("fa-IR")

  };


  /*
     ثبت محلی برای نمایش فوری.
     
     توجه:
     localStorage فقط در همین مرورگر ذخیره می‌کند.
     برای نمایش مشترک بین تمام کاربران،
     باید API ذخیره‌سازی مشترک وصل شود.
  */

  const list =
    JSON.parse(
      localStorage.getItem("exchangeTransactions") || "[]"
    );

  list.unshift(tx);

  localStorage.setItem(
    "exchangeTransactions",
    JSON.stringify(list)
  );

  renderTransactions();

  alert(
    "درخواست شما ثبت شد.\n\n" +
    "کد پیگیری:\n" +
    tx.id
  );

  document.getElementById("trackingInput").value =
    tx.id;

}


/* =========================
   نمایش تراکنش‌ها
========================= */

function renderTransactions(){

  const list =
    JSON.parse(
      localStorage.getItem("exchangeTransactions") || "[]"
    );

  const box =
    document.getElementById("transactionList");

  if(!list.length){

    box.innerHTML =
      '<div class="empty">هنوز تراکنشی ثبت نشده است.</div>';

    return;
  }

  box.innerHTML =
    list.map(tx => {

      const statusClass =
        tx.status === "انجام شد"
        ? "done"
        : "pending";

      return `

        <div class="transaction">

          <div class="tx-top">

            <div class="tx-code">
              ${tx.id}
            </div>

            <div class="status ${statusClass}">
              ${tx.status}
            </div>

          </div>

          <div class="tx-info">

            <div>
              نوع:
              <strong>
                تبادل
              </strong>
            </div>

            <div>
              ارز:
              <strong>
                ${tx.from} → ${tx.to}
              </strong>
            </div>

            <div>
              مقدار:
              <strong>
                ${Number(tx.amount).toLocaleString()}
                ${tx.from}
              </strong>
            </div>

            <div>
              دریافتی:
              <strong>
                ${Number(tx.receive).toLocaleString(undefined,{
                  maximumFractionDigits:8
                })}
                ${tx.to}
              </strong>
            </div>

            <div>
              ارزش:
              <strong>
                ${Number(tx.usdt).toLocaleString(undefined,{
                  maximumFractionDigits:2
                })}
                USDT
              </strong>
            </div>

            <div>
              زمان:
              ${tx.time}
            </div>

          </div>

          <div style="margin-top:12px">

            <div style="font-size:12px;color:#899f90">
              آدرس دریافت‌کننده
            </div>

            <div class="address">
              ${tx.address}
            </div>

          </div>

        </div>

      `;

    }).join("");

}


/* =========================
   پیگیری
========================= */

function trackTransaction(){

  const code =
    document.getElementById("trackingInput")
    .value
    .trim()
    .toUpperCase();

  const list =
    JSON.parse(
      localStorage.getItem("exchangeTransactions") || "[]"
    );

  const tx =
    list.find(x => x.id === code);

  const box =
    document.getElementById("trackResult");

  box.style.display = "block";

  if(!tx){

    box.innerHTML =
      "❌ تراکنشی با این کد پیدا نشد.";

    return;
  }

  box.innerHTML = `

    <div class="result-row">
      <span>کد پیگیری</span>
      <strong>${tx.id}</strong>
    </div>

    <div class="result-row">
      <span>وضعیت</span>
      <strong>${tx.status}</strong>
    </div>

    <div class="result-row">
      <span>تبادل</span>
      <strong>${tx.from} → ${tx.to}</strong>
    </div>

    <div class="result-row">
      <span>مقدار دریافتی</span>
      <strong>
        ${Number(tx.receive).toLocaleString(undefined,{
          maximumFractionDigits:8
        })} ${tx.to}
      </strong>
    </div>

  `;

}


/* =========================
   تنظیمات رنگ
========================= */

function openSettings(){

  document.getElementById("settingsModal")
    .style.display = "flex";

}

function closeSettings(){

  document.getElementById("settingsModal")
    .style.display = "none";

}

function setTheme(theme){

  const root =
    document.documentElement;

  if(theme === "green"){

    root.style.setProperty("--main","#00c853");
    root.style.setProperty("--main2","#00a844");

  }

  if(theme === "blue"){

    root.style.setProperty("--main","#2196f3");
    root.style.setProperty("--main2","#1976d2");

  }

  if(theme === "purple"){

    root.style.setProperty("--main","#9c27b0");
    root.style.setProperty("--main2","#7b1fa2");

  }

  if(theme === "orange"){

    root.style.setProperty("--main","#ff9800");
    root.style.setProperty("--main2","#f57c00");

  }

  localStorage.setItem("siteTheme",theme);

}


/* =========================
   بارگذاری رنگ ذخیره شده
========================= */

const savedTheme =
  localStorage.getItem("siteTheme");

if(savedTheme){

  setTheme(savedTheme);

}


/* =========================
   قیمت‌های نمایشی
========================= */

function updatePrices(){

  document.getElementById("btcPrice").innerText =
    "$" + prices.BTC.toLocaleString();

  document.getElementById("dogePrice").innerText =
    "$" + prices.DOGE;

  document.getElementById("ltcPrice").innerText =
    "$" + prices.LTC;

  document.getElementById("btcUsdt").innerText =
    "USDT: " + prices.BTC.toLocaleString();

  document.getElementById("dogeUsdt").innerText =
    "USDT: " + prices.DOGE;

  document.getElementById("ltcUsdt").innerText =
    "USDT: " + prices.LTC;

  document.getElementById("btcToman").innerText =
    "تومان: " +
    (prices.BTC * tomanUSDT).toLocaleString();

  document.getElementById("dogeToman").innerText =
    "تومان: " +
    (prices.DOGE * tomanUSDT).toLocaleString();

  document.getElementById("ltcToman").innerText =
    "تومان: " +
    (prices.LTC * tomanUSDT).toLocaleString();

  document.getElementById("usdtToman").innerText =
    "تومان: " +
    tomanUSDT.toLocaleString();

}

updatePrices();

renderTransactions();


/*
=====================================================
محل اتصال API واقعی قیمت بیت برگ
=====================================================

وقتی endpoint رسمی API بیت برگ مشخص شد،
فقط همین تابع باید به API وصل شود:

async function getBitbargPrices(){

   const response =
      await fetch("BITBARG_API_URL");

   const data =
      await response.json();

   // قیمت‌های BTC / DOGE / LTC / ...
   // از پاسخ بیت برگ خوانده می‌شوند.

}

=====================================================
*/


</script>

</body>
</html>
