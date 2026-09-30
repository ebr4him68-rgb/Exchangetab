``
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Exchange | مبادله ارز</title>

<style>
*{
  box-sizing:border-box;
}

body{
  margin:0;
  font-family:Tahoma,Arial,sans-serif;
  color:#fff;
  min-height:100vh;
  background:
    radial-gradient(circle at 20% 20%,rgba(0,200,255,.15),transparent 30%),
    radial-gradient(circle at 80% 80%,rgba(140,0,255,.15),transparent 30%),
    linear-gradient(135deg,#050816,#0b1022,#050816);
}

.container{
  width:100%;
  max-width:600px;
  margin:auto;
  padding:25px 15px 50px;
}

.logo{
  text-align:center;
  font-size:30px;
  font-weight:bold;
  margin:15px 0 5px;
}

.subtitle{
  text-align:center;
  color:#aeb8d0;
  margin-bottom:25px;
}

.exchange-box{
  background:rgba(15,23,42,.92);
  border:1px solid rgba(255,255,255,.08);
  border-radius:24px;
  padding:22px;
  box-shadow:0 20px 60px rgba(0,0,0,.45);
  backdrop-filter:blur(12px);
}

h2{
  text-align:center;
  margin:0 0 25px;
}

label{
  display:block;
  margin:15px 0 8px;
  font-weight:bold;
}

select,
input{
  width:100%;
  padding:15px;
  border-radius:13px;
  border:1px solid #334155;
  background:#111827;
  color:#fff;
  font-size:15px;
  outline:none;
}

select:focus,
input:focus{
  border-color:#38bdf8;
}

.amount-box{
  margin-top:5px;
}

.address-title{
  margin-top:22px;
  padding:12px;
  border-radius:12px;
  background:#172033;
  color:#facc15;
  text-align:center;
}

button{
  border:0;
  cursor:pointer;
  font-family:inherit;
}

.main-btn{
  width:100%;
  padding:16px;
  margin-top:22px;
  border-radius:14px;
  background:linear-gradient(90deg,#f59e0b,#facc15);
  color:#111827;
  font-size:17px;
  font-weight:bold;
}

.main-btn:hover{
  filter:brightness(1.08);
}

.swap{
  display:block;
  margin:10px auto;
  width:44px;
  height:44px;
  border-radius:50%;
  background:#1e293b;
  color:#38bdf8;
  font-size:22px;
}

.message{
  display:none;
  margin-top:15px;
  padding:13px;
  border-radius:12px;
  text-align:center;
}

.error{
  display:block;
  background:#450a0a;
  color:#fecaca;
}

.success{
  display:block;
  background:#052e16;
  color:#bbf7d0;
}

.deposit-box{
  display:none;
  margin-top:25px;
  padding:20px;
  border-radius:18px;
  background:#0b1220;
  border:1px solid #334155;
}

.deposit-box h3{
  margin-top:0;
  text-align:center;
  color:#facc15;
}

.info{
  color:#94a3b8;
  font-size:13px;
  line-height:1.8;
}

.address-display{
  margin-top:12px;
  padding:14px;
  background:#020617;
  border:1px solid #334155;
  border-radius:12px;
  direction:ltr;
  text-align:left;
  word-break:break-all;
  color:#67e8f9;
  font-size:14px;
}

.copy-btn{
  width:100%;
  padding:13px;
  margin-top:10px;
  border-radius:11px;
  background:#1e40af;
  color:white;
  font-weight:bold;
}

.copy-btn:hover{
  background:#2563eb;
}

.trade-info{
  margin-top:18px;
  padding:14px;
  border-radius:12px;
  background:#111827;
  line-height:2;
}

.trade-info span{
  color:#facc15;
}

.warning{
  margin-top:15px;
  padding:12px;
  border-radius:10px;
  background:#3f2a00;
  color:#fde68a;
  font-size:13px;
  line-height:1.8;
}

@media(max-width:480px){
  .exchange-box{
    padding:17px;
  }
}
</style>
</head>

<body>

<div class="container">

  <div class="logo">🔄 EXCHANGE</div>

  <div class="subtitle">
    مبادله مستقیم ارز دیجیتال با ارز دیجیتال
  </div>

  <div class="exchange-box">

    <h2>ثبت معامله</h2>

    <!-- ارز پرداختی -->
    <label>ارزی که می‌دهید</label>

    <select id="giveCoin">
      <option value="BTC">Bitcoin (BTC)</option>
      <option value="DOGE">Dogecoin (DOGE)</option>
      <option value="BCH">Bitcoin Cash (BCH)</option>
      <option value="LTC">Litecoin (LTC)</option>
      <option value="USDT">Tether (USDT - BEP20)</option>
      <option value="BNB">BNB</option>
    </select>


    <!-- دکمه جابه‌جایی -->
    <button class="swap" onclick="swapCoins()">⇅</button>


    <!-- ارز دریافتی -->
    <label>ارزی که می‌خواهید دریافت کنید</label>

    <select id="receiveCoin">
      <option value="BTC">Bitcoin (BTC)</option>
      <option value="DOGE">Dogecoin (DOGE)</option>
      <option value="BCH">Bitcoin Cash (BCH)</option>
      <option value="LTC">Litecoin (LTC)</option>
      <option value="USDT">Tether (USDT - BEP20)</option>
      <option value="BNB">BNB</option>
    </select>


    <!-- مقدار -->
    <label>مقدار ارز</label>

    <input
      id="amount"
      type="number"
      min="0"
      step="any"
      placeholder="مثلاً 100"
    >


    <!-- آدرس دریافت کاربر -->
    <div class="address-title">
      📥 آدرس کیف پول شما برای دریافت
    </div>

    <label id="receiveAddressLabel">
      آدرس BTC خود را وارد کنید
    </label>

    <input
      id="receiveAddress"
      type="text"
      dir="ltr"
      autocomplete="off"
      placeholder="آدرس کیف پول خود را وارد کنید"
    >


    <button
      class="main-btn"
      onclick="createTrade()">
      ثبت معامله
    </button>


    <div id="message" class="message"></div>


    <!-- نتیجه معامله -->
    <div id="depositBox" class="deposit-box">

      <h3>✅ معامله ثبت شد</h3>

      <div class="trade-info">

        <div>
          شماره معامله:
          <span id="tradeId"></span>
        </div>

        <div>
          شما می‌دهید:
          <span id="tradeGive"></span>
        </div>

        <div>
          شما دریافت می‌کنید:
          <span id="tradeReceive"></span>
        </div>

        <div>
          آدرس دریافت شما:
          <span id="userReceiveAddress"
                style="direction:ltr;display:block;word-break:break-all;">
          </span>
        </div>

      </div>


      <h3 style="margin-top:25px;">
        📤 آدرس واریز صرافی
      </h3>

      <div class="info">
        لطفاً ارز پرداختی خود را به آدرس زیر ارسال کنید:
      </div>

      <div id="depositAddress"
           class="address-display">
      </div>

      <button
        class="copy-btn"
        onclick="copyDepositAddress()">
        📋 کپی آدرس واریز
      </button>


      <div class="warning">
        ⚠️ فقط ارز و شبکه مشخص‌شده را به این آدرس ارسال کنید.
        ارسال ارز یا شبکه اشتباه ممکن است باعث از دست رفتن دارایی شود.
      </div>

    </div>

  </div>

</div>


<script>

/* =========================================
   آدرس‌های صرافی
========================================= */

const exchangeAddresses = {

  BTC:
    "1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

  DOGE:
    "DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

  BCH:
    "bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

  LTC:
    "LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

  USDT:
    "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6",

  BNB:
    "0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6"

};


/* =========================================
   نام ارزها
========================================= */

const coinNames = {

  BTC:"Bitcoin (BTC)",

  DOGE:"Dogecoin (DOGE)",

  BCH:"Bitcoin Cash (BCH)",

  LTC:"Litecoin (LTC)",

  USDT:"Tether (USDT - BEP20)",

  BNB:"BNB"

};


/* =========================================
   تغییر متن آدرس
========================================= */

document
.getElementById("receiveCoin")
.addEventListener("change", updateAddressLabel);


function updateAddressLabel(){

  const coin =
    document.getElementById("receiveCoin").value;

  document
  .getElementById("receiveAddressLabel")
  .textContent =
    "آدرس " + coin + " خود را وارد کنید";

  document
  .getElementById("receiveAddress")
  .placeholder =
    "آدرس کیف پول " + coin + " خود را وارد کنید";

}


/* =========================================
   جابه‌جایی ارزها
========================================= */

function swapCoins(){

  const give =
    document.getElementById("giveCoin");

  const receive =
    document.getElementById("receiveCoin");

  const temp = give.value;

  give.value = receive.value;

  receive.value = temp;

  updateAddressLabel();

}


/* =========================================
   بررسی اولیه آدرس
========================================= */

function validateAddress(address,coin){

  if(!address){
    return false;
  }

  address = address.trim();


  if(coin === "BTC"){

    return /^(1|3|bc1)[a-zA-Z0-9]{20,100}$/.test(address);

  }


  if(coin === "DOGE"){

    return /^D[a-zA-Z0-9]{20,40}$/.test(address);

  }


  if(coin === "BCH"){

    return /^(bitcoincash:)?[qp][a-z0-9]{20,100}$/i.test(address);

  }


  if(coin === "LTC"){

    return /^(L|M|3|ltc1)[a-zA-Z0-9]{20,100}$/i.test(address);

  }


  if(coin === "USDT" || coin === "BNB"){

    return /^0x[a-fA-F0-9]{40}$/.test(address);

  }


  return address.length >= 10;

}


/* =========================================
   ثبت معامله
========================================= */

function createTrade(){

  const give =
    document.getElementById("giveCoin").value;

  const receive =
    document.getElementById("receiveCoin").value;

  const amount =
    document.getElementById("amount").value.trim();

  const userAddress =
    document.getElementById("receiveAddress").value.trim();


  /* ارزها نباید یکسان باشند */

  if(give === receive){

    showMessage(
      "ارز پرداختی و دریافتی باید متفاوت باشند.",
      "error"
    );

    return;
  }


  /* مقدار */

  if(!amount || Number(amount) <= 0){

    showMessage(
      "لطفاً مقدار معامله را وارد کنید.",
      "error"
    );

    return;
  }


  /* آدرس کاربر */

  if(!userAddress){

    showMessage(
      "ابتدا آدرس کیف پول خود را برای دریافت وارد کنید.",
      "error"
    );

    return;
  }


  /* بررسی آدرس */

  if(!validateAddress(userAddress,receive)){

    showMessage(
      "فرمت آدرس واردشده با ارز دریافتی مطابقت ندارد.",
      "error"
    );

    return;
  }


  /* ساخت شماره معامله */

  const tradeId =
    "EX-" +
    Date.now().toString().slice(-10);


  /* نمایش اطلاعات */

  document.getElementById("tradeId")
    .textContent = tradeId;

  document.getElementById("tradeGive")
    .textContent =
    amount + " " + give;

  document.getElementById("tradeReceive")
    .textContent =
    coinNames[receive];

  document.getElementById("userReceiveAddress")
    .textContent =
    userAddress;


  /* آدرس صرافی برای واریز ارز پرداختی */

  document.getElementById("depositAddress")
    .textContent =
    exchangeAddresses[give];


  document.getElementById("depositBox")
    .style.display = "block";


  showMessage(
    "معامله با موفقیت ثبت شد. آدرس واریز صرافی نمایش داده شد.",
    "success"
  );


  /* ذخیره معامله در مرورگر */

  const trade = {

    id:tradeId,

    giveCoin:give,

    receiveCoin:receive,

    amount:amount,

    userReceiveAddress:userAddress,

    exchangeDepositAddress:
      exchangeAddresses[give],

    status:"در انتظار واریز",

    createdAt:
      new Date().toISOString()

  };


  let trades =
    JSON.parse(
      localStorage.getItem("exchangeTrades") || "[]"
    );


  trades.push(trade);


  localStorage.setItem(
    "exchangeTrades",
    JSON.stringify(trades)
  );


  /* رفتن به قسمت آدرس واریز */

  document.getElementById("depositBox")
    .scrollIntoView({
      behavior:"smooth",
      block:"start"
    });

}


/* =========================================
   کپی آدرس صرافی
========================================= */

async function copyDepositAddress(){

  const address =
    document.getElementById("depositAddress")
    .textContent;

  try{

    await navigator.clipboard.writeText(address);

    showMessage(
      "✅ آدرس واریز کپی شد.",
      "success"
    );

  }catch(error){

    const temp =
      document.createElement("textarea");

    temp.value = address;

    document.body.appendChild(temp);

    temp.select();

    document.execCommand("copy");

    temp.remove();

    showMessage(
      "✅ آدرس واریز کپی شد.",
      "success"
    );

  }

}


/* =========================================
   پیام
========================================= */

function showMessage(text,type){

  const message =
    document.getElementById("message");

  message.textContent = text;

  message.className =
    "message " + type;

}


/* اجرای اولیه */

updateAddressLabel();

</script>

</body>
</html>
```
