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
            <label>ارزی که ارسال می‌کنید</label>

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
            <label>ارزی که دریافت می‌کنید</label>

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

</body>
</html>
