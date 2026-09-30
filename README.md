
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>صرافی آنلاین</title>

<style>
*{box-sizing:border-box}
body{
    margin:0;
    font-family:Tahoma,Arial,sans-serif;
    background:linear-gradient(135deg,#ffd600,#ffb300);
    color:#111;
    min-height:100vh;
}
header{
    background:rgba(255,255,255,.95);
    padding:18px;
    text-align:center;
    box-shadow:0 4px 20px #0002;
    position:sticky;
    top:0;
    z-index:10;
}
header h1{margin:0;font-size:27px}
header p{margin:8px 0 0;color:#555}

.container{
    width:min(1200px,94%);
    margin:25px auto;
}

.live-status{
    background:#111;
    color:#fff;
    padding:13px 18px;
    border-radius:14px;
    margin-bottom:18px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    flex-wrap:wrap;
    gap:10px;
}
.live-dot{
    width:10px;
    height:10px;
    display:inline-block;
    border-radius:50%;
    background:#20e070;
    box-shadow:0 0 10px #20e070;
    margin-left:7px;
}
#lastUpdate{color:#ddd;font-size:13px}

.card{
    background:rgba(255,255,255,.96);
    border-radius:20px;
    padding:22px;
    margin-bottom:22px;
    box-shadow:0 8px 30px #0002;
}

.card h2{
    margin-top:0;
    text-align:center;
}

.market-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:14px;
}

.market{
    background:#fff;
    border:2px solid #eee;
    border-radius:16px;
    padding:17px;
    position:relative;
}
.market .coin{
    font-size:21px;
    font-weight:bold;
}
.market .price{
    font-size:19px;
    margin-top:10px;
    font-weight:bold;
}
.market .toman{
    color:#555;
    margin-top:7px;
    font-size:14px;
}
.source{
    margin-top:10px;
    font-size:12px;
    color:#777;
}
.online{
    color:#0a9b43;
    font-size:12px;
}
.offline{
    color:#d00;
    font-size:12px;
}

.source-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:10px;
    margin-top:15px;
}
.source-box{
    background:#f7f7f7;
    border-radius:12px;
    padding:12px;
    text-align:center;
    border:1px solid #ddd;
}
.source-box strong{
    display:block;
    margin-bottom:7px;
}
.source-price{
    font-weight:bold;
    font-size:14px;
}
.source-status{
    font-size:11px;
    margin-top:5px;
}

.exchange-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
}

.select-box{
    background:#fafafa;
    border:3px solid #ddd;
    border-radius:18px;
    padding:18px;
}

.select-box h3{
    margin-top:0;
}

select,input{
    width:100%;
    padding:16px;
    border-radius:13px;
    border:2px solid #ccc;
    font-size:17px;
    outline:none;
    background:white;
}

select:focus,input:focus{
    border-color:#ffb000;
}

.toggle{
    width:100%;
    margin-top:12px;
    padding:13px;
    border:0;
    border-radius:12px;
    cursor:pointer;
    font-weight:bold;
    background:#111;
    color:white;
}

.toggle.active{
    background:#159447;
}

.amount-box{
    margin-top:20px;
}

.rate-box{
    background:#111;
    color:#fff;
    padding:18px;
    border-radius:16px;
    margin-top:20px;
    text-align:center;
}

.rate-box .big{
    font-size:21px;
    font-weight:bold;
    margin-top:8px;
}

.result{
    margin-top:20px;
    background:#fff8d9;
    border:2px solid #ffd000;
    border-radius:16px;
    padding:17px;
}

.result-row{
    display:flex;
    justify-content:space-between;
    padding:10px 0;
    border-bottom:1px solid #ddd;
    gap:10px;
}

.result-row:last-child{border-bottom:0}

.submit{
    width:100%;
    padding:18px;
    margin-top:18px;
    border:0;
    border-radius:15px;
    background:#111;
    color:#fff;
    font-size:18px;
    font-weight:bold;
    cursor:pointer;
}

.submit:hover{background:#222}

.wallet-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:14px;
}

.wallet{
    border:2px solid #eee;
    border-radius:15px;
    padding:15px;
    background:#fafafa;
}

.wallet-title{
    font-weight:bold;
    margin-bottom:8px;
}

.wallet-address{
    word-break:break-all;
    background:#fff;
    border:1px solid #ddd;
    padding:11px;
    border-radius:10px;
    font-size:13px;
}

.copy{
    width:100%;
    padding:11px;
    margin-top:9px;
    border:0;
    border-radius:10px;
    background:#ffbd00;
    cursor:pointer;
    font-weight:bold;
}

.track{
    display:flex;
    gap:10px;
}

.track input{flex:1}

.track button{
    width:150px;
    border:0;
    border-radius:12px;
    background:#111;
    color:white;
    font-weight:bold;
}

.transaction{
    background:#fafafa;
    border:2px solid #eee;
    padding:15px;
    border-radius:15px;
    margin-top:12px;
}

.status{
    display:inline-block;
    padding:6px 10px;
    border-radius:8px;
    font-size:12px;
    font-weight:bold;
}

.pending{
    background:#fff0a8;
    color:#765900;
}

.done{
    background:#bdf5d1;
    color:#087331;
}

.settings{
    text-align:center;
}

.theme-btn{
    border:0;
    padding:12px 18px;
    border-radius:10px;
    margin:5px;
    cursor:pointer;
    font-weight:bold;
}

.yellow{background:#ffd000}
.blue{background:#56a8ff}
.purple{background:#b77aff}
.orange{background:#ff8b32}

.note{
    background:#fff8d9;
    border-right:5px solid #ffb000;
    padding:14px;
    border-radius:10px;
    line-height:1.8;
}

footer{
    text-align:center;
    padding:25px;
    color:#333;
}

@media(max-width:800px){
    .market-grid{
        grid-template-columns:repeat(2,1fr);
    }
    .exchange-grid{
        grid-template-columns:1fr;
    }
    .wallet-grid{
        grid-template-columns:1fr;
    }
    .source-grid{
        grid-template-columns:repeat(2,1fr);
    }
}

@media(max-width:500px){
    .market-grid{
        grid-template-columns:1fr;
    }
    .track{
        flex-direction:column;
    }
    .track button{
        width:100%;
        padding:15px;
    }
}
</style>
</head>

<body>

<header>
    <h1>💱 صرافی آنلاین</h1>
    <p>قیمت لحظه‌ای ارزهای دیجیتال</p>
</header>

<div class="container">

    <div class="live-status">
        <div>
            <span class="live-dot"></span>
            قیمت‌ها آنلاین هستند
        </div>
        <div id="lastUpdate">در حال دریافت قیمت...</div>
    </div>

    <!-- بازار -->
    <section class="card">
        <h2>📊 قیمت آنلاین ارزها</h2>

        <div id="marketGrid" class="market-grid"></div>

        <div class="source-grid">

            <div class="source-box">
                <strong>Binance</strong>
                <div id="binanceStatus" class="source-status">در حال اتصال...</div>
            </div>

            <div class="source-box">
                <strong>LBank</strong>
                <div id="lbankStatus" class="source-status">در حال اتصال...</div>
            </div>

            <div class="source-box">
                <strong>Bitbarg</strong>
                <div id="bitbargStatus" class="source-status">API نیاز دارد</div>
            </div>

            <div class="source-box">
                <strong>Tabdeal</strong>
                <div id="tabdealStatus" class="source-status">API نیاز دارد</div>
            </div>

        </div>
    </section>


    <!-- تبدیل -->
    <section class="card">

        <h2>🔄 تبدیل ارز</h2>

        <div class="exchange-grid">

            <div class="select-box">
                <h3>ارزی که ارسال می‌کنید</h3>

                <select id="sendCoin"></select>

                <button id="sendToggle"
                        class="toggle active"
                        onclick="toggleSend()">
                    فعال است
                </button>
            </div>

            <div class="select-box">
                <h3>ارزی که دریافت می‌کنید</h3>

                <select id="receiveCoin"></select>

                <button id="receiveToggle"
                        class="toggle active"
                        onclick="toggleReceive()">
                    فعال است
                </button>
            </div>

        </div>

        <div class="amount-box">
            <label>مقدار ارز ارسالی</label>
            <input
                id="amount"
                type="number"
                step="any"
                placeholder="مثلاً 0.01"
                oninput="calculate()">
        </div>

        <div class="rate-box">

            <div>نرخ لحظه‌ای تبدیل</div>

            <div id="exchangeRate" class="big">
                در انتظار قیمت...
            </div>

            <div id="rateSource" style="margin-top:8px;color:#bbb">
                منابع قیمت: Binance + LBank
            </div>

        </div>

        <div class="result">

            <div class="result-row">
                <span>مقدار دریافتی</span>
                <strong id="receiveAmount">0</strong>
            </div>

            <div class="result-row">
                <span>ارزش ارسالی به USDT</span>
                <strong id="sendUSDT">0 USDT</strong>
            </div>

            <div class="result-row">
                <span>ارزش دریافتی به USDT</span>
                <strong id="receiveUSDT">0 USDT</strong>
            </div>

            <div class="result-row">
                <span>ارزش ارسالی به تومان</span>
                <strong id="sendToman">0 تومان</strong>
            </div>

            <div class="result-row">
                <span>ارزش دریافتی به تومان</span>
                <strong id="receiveToman">0 تومان</strong>
            </div>

        </div>

        <div style="margin-top:20px">
            <label>آدرس کیف پول دریافت‌کننده</label>
            <input
                id="recipient"
                type="text"
                placeholder="آدرس کیف پول خود را وارد کنید">
        </div>

        <button class="submit" onclick="submitTransaction()">
            ثبت درخواست تبدیل
        </button>

    </section>


    <!-- آدرس‌ها -->
    <section class="card">

        <h2>💰 آدرس‌های واریز</h2>

        <div class="wallet-grid" id="walletGrid"></div>

    </section>


    <!-- پیگیری -->
    <section class="card">

        <h2>🔎 پیگیری تراکنش</h2>

        <div class="track">

            <input
                id="trackingInput"
                placeholder="کد پیگیری را وارد کنید">

            <button onclick="trackTransaction()">
                پیگیری
            </button>

        </div>

        <div id="trackResult"></div>

    </section>


    <!-- تراکنش‌ها -->
    <section class="card">

        <h2>📋 تراکنش‌های اخیر</h2>

        <div id="transactions"></div>

    </section>


    <!-- تنظیمات -->
    <section class="card settings">

        <h2>🎨 تنظیمات ظاهر</h2>

        <button class="theme-btn yellow"
                onclick="setTheme('yellow')">
            زرد
        </button>

        <button class="theme-btn blue"
                onclick="setTheme('blue')">
            آبی
        </button>

        <button class="theme-btn purple"
                onclick="setTheme('purple')">
            بنفش
        </button>

        <button class="theme-btn orange"
                onclick="setTheme('orange')">
            نارنجی
        </button>

    </section>

</div>

<footer>
    صرافی آنلاین © 2026
</footer>


<script>

/* =========================================================
   تنظیمات
========================================================= */

const REFRESH_SECONDS = 20;


/*
  Binance:
  API عمومی قیمت بازار
*/
const BINANCE_API =
    "https://data-api.binance.vision/api/v3/ticker/price";


/*
  LBank:
  API عمومی بازار
*/
const LBANK_API =
    "https://api.lbkex.com/v2/ticker/24hr.do";


/*
  مهم:
  برای Bitbarg و Tabdeal عمداً URL ساختگی قرار نداده‌ایم.

  وقتی API رسمی آنها مشخص شد فقط این دو مقدار را تغییر می‌دهیم.
*/
const BITBARG_API_URL = "";

const TABDEAL_API_URL = "";


/* =========================================================
   کیف پول‌ها
========================================================= */

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


/* =========================================================
   اطلاعات ارزها
========================================================= */

const coins = {

    BTC:{
        name:"Bitcoin",
        icon:"₿"
    },

    BCH:{
        name:"Bitcoin Cash",
        icon:"₿"
    },

    TRX:{
        name:"TRON",
        icon:"TRX"
    },

    LTC:{
        name:"Litecoin",
        icon:"Ł"
    },

    DOGE:{
        name:"Dogecoin",
        icon:"Ð"
    },

    USDT:{
        name:"Tether",
        icon:"₮"
    }

};


/* =========================================================
   قیمت‌ها
========================================================= */

let prices = {
    BTC:null,
    BCH:null,
    TRX:null,
    LTC:null,
    DOGE:null,
    USDT:1
};


/*
  قیمت هر منبع جداگانه نگهداری می‌شود
*/
let sourcePrices = {

    Binance:{},
    LBank:{},
    Bitbarg:{},
    Tabdeal:{}

};


let tomanUSDT = null;

let sendActive = true;
let receiveActive = true;


/* =========================================================
   ساخت لیست‌ها
========================================================= */

function buildLists(){

    const send =
        document.getElementById("sendCoin");

    const receive =
        document.getElementById("receiveCoin");

    send.innerHTML = "";
    receive.innerHTML = "";

    Object.keys(coins).forEach(symbol => {

        const a =
            document.createElement("option");

        a.value = symbol;
        a.textContent =
            `${coins[symbol].icon} ${symbol} - ${coins[symbol].name}`;

        send.appendChild(a);


        const b =
            document.createElement("option");

        b.value = symbol;
        b.textContent =
            `${coins[symbol].icon} ${symbol} - ${coins[symbol].name}`;

        receive.appendChild(b);

    });

    send.value = "BTC";
    receive.value = "DOGE";

    send.addEventListener("change",calculate);
    receive.addEventListener("change",calculate);
}


/* =========================================================
   نمایش بازار
========================================================= */

function renderMarkets(){

    const grid =
        document.getElementById("marketGrid");

    grid.innerHTML = "";

    Object.keys(coins).forEach(symbol => {

        const price = prices[symbol];

        let priceText =
            price !== null
            ? formatUSD(price)
            : "در انتظار قیمت";

        let tomanText =
            price !== null && tomanUSDT
            ? formatToman(price * tomanUSDT)
            : "در انتظار نرخ تومان";


        const div =
            document.createElement("div");

        div.className = "market";

        div.innerHTML = `

            <div class="coin">
                ${coins[symbol].icon}
                ${symbol}
            </div>

            <div class="price">
                ${priceText} USDT
            </div>

            <div class="toman">
                ${tomanText}
            </div>

            <div class="source">
                قیمت تجمیعی از منابع آنلاین
            </div>

        `;

        grid.appendChild(div);

    });

}


/* =========================================================
   Binance
========================================================= */

async function getBinancePrices(){

    const symbols = [
        "BTCUSDT",
        "BCHUSDT",
        "TRXUSDT",
        "LTCUSDT",
        "DOGEUSDT"
    ];

    try{

        const url =
            BINANCE_API +
            "?symbols=" +
            encodeURIComponent(
                JSON.stringify(symbols)
            );

        const response =
            await fetch(url,{
                cache:"no-store"
            });

        if(!response.ok)
            throw new Error("Binance error");

        const data =
            await response.json();


        sourcePrices.Binance = {};

        data.forEach(item => {

            const symbol =
                item.symbol.replace("USDT","");

            sourcePrices.Binance[symbol] =
                Number(item.price);

        });


        document.getElementById(
            "binanceStatus"
        ).innerHTML =
            '<span class="online">● آنلاین</span>';

        return true;

    }catch(error){

        console.error(
            "Binance:",
            error
        );

        document.getElementById(
            "binanceStatus"
        ).innerHTML =
            '<span class="offline">● خطا</span>';

        return false;
    }

}


/* =========================================================
   LBank
========================================================= */

async function getLBankPrices(){

    const symbols = [
        "btc_usdt",
        "bch_usdt",
        "trx_usdt",
        "ltc_usdt",
        "doge_usdt"
    ];

    try{

        const requests =
            symbols.map(symbol =>

                fetch(
                    LBANK_API +
                    "?symbol=" +
                    symbol,
                    {
                        cache:"no-store"
                    }
                )
                .then(r => r.json())

            );


        const results =
            await Promise.all(requests);


        sourcePrices.LBank = {};


        results.forEach((data,index) => {

            let item = null;

            if(Array.isArray(data))
                item = data[0];

            else if(data.data)
                item =
                    Array.isArray(data.data)
                    ? data.data[0]
                    : data.data;


            if(!item)
                return;


            const latest =
                item?.ticker?.latest ??
                item?.latest ??
                item?.price;


            if(latest){

                const symbol =
                    symbols[index]
                    .split("_")[0]
                    .toUpperCase();

                sourcePrices.LBank[symbol] =
                    Number(latest);

            }

        });


        document.getElementById(
            "lbankStatus"
        ).innerHTML =
            '<span class="online">● آنلاین</span>';

        return true;

    }catch(error){

        console.error(
            "LBank:",
            error
        );

        document.getElementById(
            "lbankStatus"
        ).innerHTML =
            '<span class="offline">● خطا</span>';

        return false;
    }

}


/* =========================================================
   Bitbarg
========================================================= */

async function getBitbargPrices(){

    /*
      تا زمانی که API رسمی عمومی Bitbarg
      مشخص نباشد، این قسمت قیمت جعلی تولید نمی‌کند.
    */

    if(!BITBARG_API_URL){

        document.getElementById(
            "bitbargStatus"
        ).innerHTML =
            '<span class="offline">API رسمی وارد نشده</span>';

        return false;
    }


    try{

        const response =
            await fetch(
                BITBARG_API_URL,
                {
                    cache:"no-store"
                }
            );

        if(!response.ok)
            throw new Error("Bitbarg error");

        const data =
            await response.json();


        /*
          این قسمت را مطابق JSON واقعی API
          Bitbarg تنظیم می‌کنیم.
        */

        console.log(
            "Bitbarg data:",
            data
        );


        document.getElementById(
            "bitbargStatus"
        ).innerHTML =
            '<span class="online">● آنلاین</span>';

        return true;

    }catch(error){

        console.error(
            "Bitbarg:",
            error
        );

        document.getElementById(
            "bitbargStatus"
        ).innerHTML =
            '<span class="offline">● خطا</span>';

        return false;

    }

}


/* =========================================================
   Tabdeal
========================================================= */

async function getTabdealPrices(){

    if(!TABDEAL_API_URL){

        document.getElementById(
            "tabdealStatus"
        ).innerHTML =
            '<span class="offline">API رسمی وارد نشده</span>';

        return false;
    }


    try{

        const response =
            await fetch(
                TABDEAL_API_URL,
                {
                    cache:"no-store"
                }
            );

        if(!response.ok)
            throw new Error("Tabdeal error");


        const data =
            await response.json();


        console.log(
            "Tabdeal data:",
            data
        );


        document.getElementById(
            "tabdealStatus"
        ).innerHTML =
            '<span class="online">● آنلاین</span>';

        return true;


    }catch(error){

        console.error(
            "Tabdeal:",
            error
        );

        document.getElementById(
            "tabdealStatus"
        ).innerHTML =
            '<span class="offline">● خطا</span>';

        return false;

    }

}


/* =========================================================
   محاسبه قیمت نهایی
========================================================= */

function calculateAveragePrice(symbol){

    const values = [];

    if(
        sourcePrices.Binance[symbol] &&
        isFinite(sourcePrices.Binance[symbol])
    ){
        values.push(
            sourcePrices.Binance[symbol]
        );
    }


    if(
        sourcePrices.LBank[symbol] &&
        isFinite(sourcePrices.LBank[symbol])
    ){
        values.push(
            sourcePrices.LBank[symbol]
        );
    }


    if(
        sourcePrices.Bitbarg[symbol] &&
        isFinite(sourcePrices.Bitbarg[symbol])
    ){
        values.push(
            sourcePrices.Bitbarg[symbol]
        );
    }


    if(
        sourcePrices.Tabdeal[symbol] &&
        isFinite(sourcePrices.Tabdeal[symbol])
    ){
        values.push(
            sourcePrices.Tabdeal[symbol]
        );
    }


    if(!values.length)
        return null;


    const total =
        values.reduce(
            (a,b) => a+b,
            0
        );


    return total / values.length;
}


/* =========================================================
   بروزرسانی قیمت‌ها
========================================================= */

async function updateOnlinePrices(){

    document.getElementById(
        "lastUpdate"
    ).textContent =
        "در حال بروزرسانی قیمت‌ها...";


    /*
      منابع را همزمان دریافت می‌کنیم
    */

    await Promise.allSettled([

        getBinancePrices(),

        getLBankPrices(),

        getBitbargPrices(),

        getTabdealPrices()

    ]);


    /*
      میانگین قیمت منابعی که واقعا
      جواب داده‌اند
    */

    Object.keys(coins).forEach(symbol => {

        if(symbol === "USDT"){

            prices.USDT = 1;
            return;

        }


        const average =
            calculateAveragePrice(symbol);


        if(average !== null)
            prices[symbol] = average;

    });


    /*
      نرخ USDT به تومان
      اگر API تومان جداگانه نداشته باشیم،
      فعلاً قیمت تومان در انتظار API می‌ماند.
    */

    renderMarkets();

    calculate();


    const now =
        new Date();


    document.getElementById(
        "lastUpdate"
    ).textContent =
        "آخرین بروزرسانی: " +
        now.toLocaleTimeString("fa-IR") +
        " | بروزرسانی بعدی: " +
        REFRESH_SECONDS +
        " ثانیه";


}


/* =========================================================
   نرخ تبدیل
========================================================= */

function updateRate(){

    const send =
        document.getElementById("sendCoin").value;

    const receive =
        document.getElementById("receiveCoin").value;


    const sendPrice =
        prices[send];

    const receivePrice =
        prices[receive];


    if(
        sendPrice === null ||
        receivePrice === null
    ){

        document.getElementById(
            "exchangeRate"
        ).textContent =
            "در انتظار قیمت آنلاین...";

        return null;
    }


    if(receivePrice === 0)
        return null;


    const rate =
        sendPrice / receivePrice;


    document.getElementById(
        "exchangeRate"
    ).textContent =
        `1 ${send} = ${formatCoin(rate)} ${receive}`;


    return rate;
}


/* =========================================================
   محاسبه کامل
========================================================= */

function calculate(){

    const rate =
        updateRate();


    const amount =
        Number(
            document.getElementById(
                "amount"
            ).value
        ) || 0;


    const send =
        document.getElementById(
            "sendCoin"
        ).value;


    const receive =
        document.getElementById(
            "receiveCoin"
        ).value;


    if(
        !rate ||
        prices[send] === null ||
        prices[receive] === null
    ){

        document.getElementById(
            "receiveAmount"
        ).textContent = "0";

        document.getElementById(
            "sendUSDT"
        ).textContent = "0 USDT";

        document.getElementById(
            "receiveUSDT"
        ).textContent = "0 USDT";

        document.getElementById(
            "sendToman"
        ).textContent = "0 تومان";

        document.getElementById(
            "receiveToman"
        ).textContent = "0 تومان";

        return;
    }


    const received =
        amount * rate;


    const sendValue =
        amount * prices[send];


    const receiveValue =
        received * prices[receive];


    document.getElementById(
        "receiveAmount"
    ).textContent =
        formatCoin(received) +
        " " +
        receive;


    document.getElementById(
        "sendUSDT"
    ).textContent =
        formatUSD(sendValue) +
        " USDT";


    document.getElementById(
        "receiveUSDT"
    ).textContent =
        formatUSD(receiveValue) +
        " USDT";


    if(tomanUSDT){

        document.getElementById(
            "sendToman"
        ).textContent =
            formatToman(
                sendValue * tomanUSDT
            );


        document.getElementById(
            "receiveToman"
        ).textContent =
            formatToman(
                receiveValue * tomanUSDT
            );

    }else{

        document.getElementById(
            "sendToman"
        ).textContent =
            "نرخ تومان وارد نشده";


        document.getElementById(
            "receiveToman"
        ).textContent =
            "نرخ تومان وارد نشده";

    }

}


/* =========================================================
   فعال / غیرفعال
========================================================= */

function toggleSend(){

    sendActive =
        !sendActive;


    const btn =
        document.getElementById(
            "sendToggle"
        );


    if(sendActive){

        btn.textContent =
            "فعال است";

        btn.classList.add("active");

    }else{

        btn.textContent =
            "غیرفعال است";

        btn.classList.remove("active");

    }

}


function toggleReceive(){

    receiveActive =
        !receiveActive;


    const btn =
        document.getElementById(
            "receiveToggle"
        );


    if(receiveActive){

        btn.textContent =
            "فعال است";

        btn.classList.add("active");

    }else{

        btn.textContent =
            "غیرفعال است";

        btn.classList.remove("active");

    }

}


/* =========================================================
   کیف پول‌ها
========================================================= */

function renderWallets(){

    const grid =
        document.getElementById(
            "walletGrid"
        );


    grid.innerHTML = "";


    Object.keys(wallets).forEach(symbol => {

        const div =
            document.createElement("div");

        div.className =
            "wallet";


        div.innerHTML = `

            <div class="wallet-title">
                ${coins[symbol].icon}
                ${symbol}
            </div>

            <div
                id="wallet-${symbol}"
                class="wallet-address">
                ${wallets[symbol]}
            </div>

            <button
                class="copy"
                onclick="copyWallet('${symbol}')">
                کپی آدرس
            </button>

        `;


        grid.appendChild(div);

    });

}


function copyWallet(symbol){

    navigator.clipboard
        .writeText(
            wallets[symbol]
        )
        .then(() => {

            alert(
                "آدرس " +
                symbol +
                " کپی شد"
            );

        });

}


/* =========================================================
   ثبت تراکنش
========================================================= */

function submitTransaction(){

    if(!sendActive || !receiveActive){

        alert(
            "ارسال یا دریافت غیرفعال است."
        );

        return;
    }


    const send =
        document.getElementById(
            "sendCoin"
        ).value;


    const receive =
        document.getElementById(
            "receiveCoin"
        ).value;


    const amount =
        Number(
            document.getElementById(
                "amount"
            ).value
        );


    const recipient =
        document.getElementById(
            "recipient"
        ).value.trim();


    if(!amount || amount <= 0){

        alert(
            "مقدار ارز را وارد کنید."
        );

        return;
    }


    if(!recipient){

        alert(
            "آدرس کیف پول دریافت‌کننده را وارد کنید."
        );

        return;
    }


    const rate =
        updateRate();


    if(!rate){

        alert(
            "قیمت آنلاین هنوز دریافت نشده است."
        );

        return;
    }


    const received =
        amount * rate;


    const valueUSDT =
        amount * prices[send];


    const tracking =
        "EX" +
        Date.now()
        .toString()
        .slice(-8);


    const transaction = {

        tracking,

        send,

        receive,

        amount,

        received,

        valueUSDT,

        recipient,

        time:
            new Date().toLocaleString(
                "fa-IR"
            ),

        status:
            "در حال بررسی"

    };


    /*
      این بخش فقط روی همین مرورگر ذخیره می‌شود.
      برای نمایش مشترک بین همه کاربران،
      بعداً باید backend/shared storage متصل شود.
    */

    const list =
        JSON.parse(
            localStorage.getItem(
                "transactions"
            ) || "[]"
        );


    list.unshift(transaction);


    localStorage.setItem(
        "transactions",
        JSON.stringify(
            list.slice(0,50)
        )
    );


    renderTransactions();


    alert(
        "درخواست ثبت شد.\n\nکد پیگیری: " +
        tracking
    );

}


/* =========================================================
   نمایش تراکنش‌ها
========================================================= */

function renderTransactions(){

    const box =
        document.getElementById(
            "transactions"
        );


    const list =
        JSON.parse(
            localStorage.getItem(
                "transactions"
            ) || "[]"
        );


    if(!list.length){

        box.innerHTML =
            "<p>هنوز تراکنشی ثبت نشده است.</p>";

        return;
    }


    box.innerHTML = "";


    list.forEach(tx => {

        const div =
            document.createElement("div");

        div.className =
            "transaction";


        const statusClass =
            tx.status === "انجام شد"
            ? "done"
            : "pending";


        div.innerHTML = `

            <div>
                <strong>
                    کد پیگیری:
                </strong>
                ${tx.tracking}
            </div>

            <div style="margin-top:7px">
                ${tx.send}
                →
                ${tx.receive}
            </div>

            <div style="margin-top:7px">
                مقدار ارسال:
                ${formatCoin(tx.amount)}
                ${tx.send}
            </div>

            <div style="margin-top:7px">
                مقدار دریافت:
                ${formatCoin(tx.received)}
                ${tx.receive}
            </div>

            <div style="margin-top:7px">
                ارزش:
                ${formatUSD(tx.valueUSDT)}
                USDT
            </div>

            <div style="margin-top:7px">
                آدرس:
                ${tx.recipient}
            </div>

            <div style="margin-top:7px">
                زمان:
                ${tx.time}
            </div>

            <div style="margin-top:9px">
                <span class="status ${statusClass}">
                    ${tx.status}
                </span>
            </div>

        `;


        box.appendChild(div);

    });

}


/* =========================================================
   پیگیری
========================================================= */

function trackTransaction(){

    const code =
        document.getElementById(
            "trackingInput"
        ).value.trim();


    const result =
        document.getElementById(
            "trackResult"
        );


    if(!code){

        result.innerHTML =
            "<p>کد پیگیری را وارد کنید.</p>";

        return;
    }


    const list =
        JSON.parse(
            localStorage.getItem(
                "transactions"
            ) || "[]"
        );


    const tx =
        list.find(
            x => x.tracking === code
        );


    if(!tx){

        result.innerHTML =
            `
            <div class="note" style="margin-top:15px">
                تراکنشی با این کد پیدا نشد.
            </div>
            `;

        return;
    }


    result.innerHTML =
        `

        <div class="transaction">

            <strong>
                ${tx.send}
                →
                ${tx.receive}
            </strong>

            <div style="margin-top:10px">
                مقدار:
                ${formatCoin(tx.amount)}
                ${tx.send}
            </div>

            <div style="margin-top:7px">
                دریافت:
                ${formatCoin(tx.received)}
                ${tx.receive}
            </div>

            <div style="margin-top:7px">
                وضعیت:
                <span class="status ${
                    tx.status === "انجام شد"
                    ? "done"
                    : "pending"
                }">
                    ${tx.status}
                </span>
            </div>

        </div>

        `;

}


/* =========================================================
   قالب قیمت
========================================================= */

function formatUSD(value){

    if(
        value === null ||
        value === undefined ||
        !isFinite(value)
    )
        return "در انتظار";


    if(value >= 1000)
        return Number(value)
            .toLocaleString(
                "en-US",
                {
                    maximumFractionDigits:2
                }
            );


    if(value >= 1)
        return Number(value)
            .toLocaleString(
                "en-US",
                {
                    maximumFractionDigits:6
                }
            );


    return Number(value)
        .toLocaleString(
            "en-US",
            {
                maximumFractionDigits:10
            }
        );

}


function formatCoin(value){

    if(
        value === null ||
        value === undefined ||
        !isFinite(value)
    )
        return "0";


    return Number(value)
        .toLocaleString(
            "en-US",
            {
                maximumFractionDigits:12
            }
        );

}


function formatToman(value){

    if(
        value === null ||
        value === undefined ||
        !isFinite(value)
    )
        return "در انتظار";


    return Number(value)
        .toLocaleString(
            "fa-IR",
            {
                maximumFractionDigits:0
            }
        ) +
        " تومان";

}


/* =========================================================
   تم‌ها
========================================================= */

function setTheme(theme){

    if(theme === "yellow"){

        document.body.style.background =
            "linear-gradient(135deg,#ffd600,#ffb300)";

    }

    if(theme === "blue"){

        document.body.style.background =
            "linear-gradient(135deg,#5ab0ff,#2478d8)";

    }

    if(theme === "purple"){

        document.body.style.background =
            "linear-gradient(135deg,#c17cff,#7137d9)";

    }

    if(theme === "orange"){

        document.body.style.background =
            "linear-gradient(135deg,#ffad4a,#ff5d22)";

    }

    localStorage.setItem(
        "theme",
        theme
    );

}


/* =========================================================
   شروع سایت
========================================================= */

buildLists();

renderWallets();

renderTransactions();

renderMarkets();


const savedTheme =
    localStorage.getItem("theme");


if(savedTheme)
    setTheme(savedTheme);


/*
  اولین دریافت قیمت
*/

updateOnlinePrices();


/*
  بروزرسانی دقیقاً هر ۲۰ ثانیه
*/

setInterval(
    updateOnlinePrices,
    REFRESH_SECONDS * 1000
);

</script>

</body>
</html>
