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

</script>```html
<!-- ================================
     LIVE CRYPTO PRICE BAR
     این بخش فقط نمایش قیمت است
     و به بخش مبادله دست نمی‌زند
================================ -->

<style>

.live-market{
    width:100%;
    padding:14px 10px;
    background:
        linear-gradient(180deg,#07111f,#0b1627);
    border-bottom:1px solid rgba(255,255,255,.08);
    overflow:hidden;
}

.live-market-title{
    text-align:center;
    color:#facc15;
    font-size:15px;
    font-weight:bold;
    margin-bottom:12px;
}

.live-coins{
    width:100%;
    max-width:1400px;
    margin:auto;
    display:grid;
    grid-template-columns:
        repeat(6,minmax(140px,1fr));
    gap:10px;
}

.live-coin{
    min-width:0;
    padding:12px;
    border-radius:15px;
    background:#111c2d;
    border:1px solid rgba(255,255,255,.07);
    text-align:center;
    transition:.25s;
}

.live-coin:hover{
    transform:translateY(-2px);
    border-color:#38bdf8;
}

.coin-top{
    display:flex;
    align-items:center;
    justify-content:center;
    gap:7px;
}

.coin-logo{
    width:30px;
    height:30px;
    border-radius:50%;
}

.coin-name{
    font-weight:bold;
    font-size:14px;
}

.coin-symbol{
    color:#94a3b8;
    font-size:11px;
}

.coin-price{
    margin-top:8px;
    font-size:16px;
    font-weight:bold;
    direction:ltr;
}

.coin-change{
    margin-top:5px;
    font-size:11px;
}

.price-status{
    margin-top:7px;
    font-size:11px;
    color:#86efac;
    display:flex;
    justify-content:center;
    align-items:center;
    gap:5px;
}

/* چراغ سبز */
.live-light{
    width:8px;
    height:8px;
    border-radius:50%;
    background:#22c55e;
    box-shadow:
        0 0 5px #22c55e,
        0 0 10px #22c55e;
    animation:liveBlink .9s infinite;
}

@keyframes liveBlink{
    0%,100%{
        opacity:1;
    }

    50%{
        opacity:.25;
    }
}

.price-up{
    color:#4ade80;
}

.price-down{
    color:#f87171;
}

.price-neutral{
    color:#cbd5e1;
}

/* موبایل */
@media(max-width:950px){

    .live-coins{
        display:flex;
        overflow-x:auto;
        justify-content:flex-start;
        padding-bottom:5px;
        scrollbar-width:none;
    }

    .live-coins::-webkit-scrollbar{
        display:none;
    }

    .live-coin{
        min-width:145px;
        flex:0 0 145px;
    }

}

</style>


<div class="live-market">

    <div class="live-market-title">
        🟢 بازار آنلاین ارزها
    </div>

    <div class="live-coins">

        <!-- BTC -->
        <div class="live-coin">

            <div class="coin-top">

                <img
                    class="coin-logo"
                    src="https://s2.coinmarketcap.com/static/img/coins/64x64/1.png"
                    alt="Bitcoin">

                <div>
                    <div class="coin-name">
                        Bitcoin
                    </div>

                    <div class="coin-symbol">
                        BTC
                    </div>
                </div>

            </div>

            <div
                id="price-BTC"
                class="coin-price">
                در حال دریافت...
            </div>

            <div
                id="change-BTC"
                class="coin-change price-neutral">
                --
            </div>

            <div class="price-status">

                <span class="live-light"></span>

                آنلاین

            </div>

        </div>


        <!-- DOGE -->
        <div class="live-coin">

            <div class="coin-top">

                <img
                    class="coin-logo"
                    src="https://s2.coinmarketcap.com/static/img/coins/64x64/74.png"
                    alt="Dogecoin">

                <div>

                    <div class="coin-name">
                        Dogecoin
                    </div>

                    <div class="coin-symbol">
                        DOGE
                    </div>

                </div>

            </div>

            <div
                id="price-DOGE"
                class="coin-price">
                در حال دریافت...
            </div>

            <div
                id="change-DOGE"
                class="coin-change price-neutral">
                --
            </div>

            <div class="price-status">

                <span class="live-light"></span>

                آنلاین

            </div>

        </div>


        <!-- BCH -->
        <div class="live-coin">

            <div class="coin-top">

                <img
                    class="coin-logo"
                    src="https://s2.coinmarketcap.com/static/img/coins/64x64/1831.png"
                    alt="Bitcoin Cash">

                <div>

                    <div class="coin-name">
                        Bitcoin Cash
                    </div>

                    <div class="coin-symbol">
                        BCH
                    </div>

                </div>

            </div>

            <div
                id="price-BCH"
                class="coin-price">
                در حال دریافت...
            </div>

            <div
                id="change-BCH"
                class="coin-change price-neutral">
                --
            </div>

            <div class="price-status">

                <span class="live-light"></span>

                آنلاین

            </div>

        </div>


        <!-- LTC -->
        <div class="live-coin">

            <div class="coin-top">

                <img
                    class="coin-logo"
                    src="https://s2.coinmarketcap.com/static/img/coins/64x64/2.png"
                    alt="Litecoin">

                <div>

                    <div class="coin-name">
                        Litecoin
                    </div>

                    <div class="coin-symbol">
                        LTC
                    </div>

                </div>

            </div>

            <div
                id="price-LTC"
                class="coin-price">
                در حال دریافت...
            </div>

            <div
                id="change-LTC"
                class="coin-change price-neutral">
                --
            </div>

            <div class="price-status">

                <span class="live-light"></span>

                آنلاین

            </div>

        </div>


        <!-- USDT -->
        <div class="live-coin">

            <div class="coin-top">

                <img
                    class="coin-logo"
                    src="https://s2.coinmarketcap.com/static/img/coins/64x64/825.png"
                    alt="Tether">

                <div>

                    <div class="coin-name">
                        Tether

                    </div>

                    <div class="coin-symbol">
                        USDT
                    </div>

                </div>

            </div>

            <div
                id="price-USDT"
                class="coin-price">
                در حال دریافت...
            </div>

            <div
                id="change-USDT"
                class="coin-change price-neutral">
                --
            </div>

            <div class="price-status">

                <span class="live-light"></span>

                آنلاین

            </div>

        </div>


        <!-- BNB -->
        <div class="live-coin">

            <div class="coin-top">

                <img
                    class="coin-logo"
                    src="https://s2.coinmarketcap.com/static/img/coins/64x64/1839.png"
                    alt="BNB">

                <div>

                    <div class="coin-name">
                        BNB
                    </div>

                    <div class="coin-symbol">
                        BNB
                    </div>

                </div>

            </div>

            <div
                id="price-BNB"
                class="coin-price">
                در حال دریافت...
            </div>

            <div
                id="change-BNB"
                class="coin-change price-neutral">
                --
            </div>

            <div class="price-status">

                <span class="live-light"></span>

                آنلاین

            </div>

        </div>

    </div>

</div>


<script>

/* =====================================
   LIVE PRICE ENGINE
   فقط قیمت‌ها را به‌روزرسانی می‌کند
   و به بخش مبادله کاری ندارد
===================================== */

const liveCoins = {

    BTC: 1,

    DOGE: 74,

    BCH: 1831,

    LTC: 2,

    USDT: 825,

    BNB: 1839

};


/*
   دریافت قیمت‌ها از CoinMarketCap
   همه ۶ ارز در یک درخواست
*/

async function updateLivePrices(){

    try{

        const ids =
            Object.values(liveCoins).join(",");

        const url =
            "https://pro-api.coinmarketcap.com/public-api/v3/cryptocurrency/quotes/latest"
            + "?id="
            + ids
            + "&convert=USD";


        const response =
            await fetch(url);


        if(!response.ok){

            throw new Error(
                "Price API error"
            );

        }


        const result =
            await response.json();


        if(
            !result ||
            !result.data
        ){

            throw new Error(
                "Invalid price data"
            );

        }


        /*
           تبدیل ID به نماد
        */

        const idToSymbol = {

            1:"BTC",

            74:"DOGE",

            1831:"BCH",

            2:"LTC",

            825:"USDT",

            1839:"BNB"

        };


        Object.entries(
            result.data
        ).forEach(
            ([id,coin]) => {

                const symbol =
                    idToSymbol[id];


                if(!symbol){

                    return;

                }


                const quote =
                    coin.quote.USD;


                const price =
                    Number(
                        quote.price
                    );


                const change =
                    Number(
                        quote.percent_change_24h
                    );


                /*
                   فرمت قیمت
                */

                let formattedPrice;


                if(price >= 1000){

                    formattedPrice =
                        "$" +
                        price.toLocaleString(
                            "en-US",
                            {
                                maximumFractionDigits:2
                            }
                        );

                }
                else if(price >= 1){

                    formattedPrice =
                        "$" +
                        price.toLocaleString(
                            "en-US",
                            {
                                minimumFractionDigits:2,
                                maximumFractionDigits:4
                            }
                        );

                }
                else{

                    formattedPrice =
                        "$" +
                        price.toLocaleString(
                            "en-US",
                            {
                                minimumFractionDigits:4,
                                maximumFractionDigits:8
                            }
                        );

                }


                const priceElement =
                    document.getElementById(
                        "price-" + symbol
                    );


                const changeElement =
                    document.getElementById(
                        "change-" + symbol
                    );


                if(priceElement){

                    priceElement.textContent =
                        formattedPrice;

                }


                if(changeElement){

                    const sign =
                        change >= 0
                        ? "+"
                        : "";

                    changeElement.textContent =
                        sign +
                        change.toFixed(2) +
                        "% (24h)";


                    changeElement.className =
                        "coin-change " +
                        (
                            change > 0
                            ? "price-up"
                            : change < 0
                            ? "price-down"
                            : "price-neutral"
                        );

                }

            }
        );


    }catch(error){

        console.log(
            "Live price error:",
            error
        );

        /*
           اگر API موقتاً پاسخ نداد،
           بخش مبادله همچنان بدون تغییر کار می‌کند.
        */

    }

}


/*
   قیمت‌ها هنگام باز شدن سایت
*/

updateLivePrices();


/*
   به‌روزرسانی دوره‌ای
   هر 30 ثانیه
*/

setInterval(
    updateLivePrices,
    30000
);

</script>
```


</body>
</html>
```
