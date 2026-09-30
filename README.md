صرافی انلاین

 
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
    min-height:100vh;
    color:#111;
    background:linear-gradient(135deg,#fff700,#ffae00);
    transition:.4s;
}

.container{
    width:94%;
    max-width:1250px;
    margin:auto;
    padding:18px 0 50px;
}

header,
.exchange,
.tracking,
.transactions{
    background:rgba(255,255,255,.97);
    border-radius:24px;
    box-shadow:0 8px 30px rgba(0,0,0,.14);
}

header{
    padding:25px;
    text-align:center;
}

.logo{
    font-size:32px;
    font-weight:bold;
}

.subtitle{
    margin-top:8px;
    color:#555;
}

.connection{
    margin-top:16px;
    display:flex;
    align-items:center;
    justify-content:center;
    gap:9px;
    font-weight:bold;
}

.dot{
    width:13px;
    height:13px;
    border-radius:50%;
    background:#16a34a;
    box-shadow:0 0 12px #16a34a;
    animation:pulse 1.2s infinite;
}

.dot.off{
    background:#dc2626;
    box-shadow:0 0 12px #dc2626;
}

@keyframes pulse{
    50%{opacity:.35}
}

.themes{
    display:flex;
    justify-content:center;
    gap:8px;
    margin-top:17px;
    flex-wrap:wrap;
}

.theme{
    border:2px solid #111;
    background:#fff;
    border-radius:12px;
    padding:8px 15px;
    cursor:pointer;
    font-weight:bold;
}

.title{
    text-align:center;
    font-size:25px;
    font-weight:bold;
    margin:25px 0 15px;
}

.market{
    display:grid;
    grid-template-columns:repeat(6,1fr);
    gap:12px;
}

.card{
    background:#fff;
    border-radius:18px;
    padding:17px 8px;
    text-align:center;
    box-shadow:0 5px 18px rgba(0,0,0,.12);
    transition:.2s;
}

.card:hover{
    transform:translateY(-3px);
}

.coin{
    font-size:19px;
    font-weight:bold;
}

.price{
    direction:ltr;
    font-size:18px;
    font-weight:bold;
    margin:13px 0 8px;
}

.status{
    font-size:12px;
    font-weight:bold;
    color:#16a34a;
}

.status.old{
    color:#d97706;
}

.status.wait{
    color:#777;
}

.source-info{
    margin-top:6px;
    font-size:10px;
    color:#777;
}

.exchange{
    padding:25px;
    margin-top:25px;
}

.exchange h2,
.tracking h2,
.transactions h2{
    text-align:center;
    margin-bottom:20px;
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
    padding:20px;
}

label{
    display:block;
    font-weight:bold;
    margin-bottom:9px;
}

select,
input{
    width:100%;
    padding:15px;
    border:2px solid #ddd;
    border-radius:14px;
    font-size:16px;
    outline:none;
    background:#fff;
}

select:focus,
input:focus{
    border-color:#f1b900;
}

.coin-current{
    margin-top:10px;
    padding:10px;
    background:#fff4bd;
    border-radius:12px;
    text-align:center;
    font-size:13px;
}

.result{
    margin-top:12px;
    padding:12px;
    background:#fff4bd;
    border-radius:12px;
    text-align:center;
    font-weight:bold;
}

.rate{
    margin-top:20px;
    background:#111;
    color:#fff;
    border-radius:17px;
    padding:18px;
    text-align:center;
    font-size:18px;
}

.rate strong{
    color:#ffe600;
}

.wallets{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
    margin-top:20px;
}

.wallet{
    background:#fff;
    border:2px solid #eee;
    border-radius:20px;
    padding:20px;
}

.wallet h3{
    margin-bottom:12px;
}

.address{
    direction:ltr;
    text-align:left;
    word-break:break-all;
    background:#f1f1f1;
    border-radius:12px;
    padding:13px;
    font-size:13px;
}

button{
    cursor:pointer;
}

.copy,
.submit,
.track{
    border:0;
    background:#111;
    color:#fff;
    border-radius:13px;
    padding:13px;
    font-weight:bold;
}

.copy{
    width:100%;
    margin-top:10px;
}

.submit{
    width:100%;
    margin-top:20px;
    padding:17px;
    font-size:18px;
}

.tracking,
.transactions{
    margin-top:25px;
    padding:25px;
}

.track-row{
    display:flex;
    gap:10px;
}

.track-row input{
    flex:1;
}

.track{
    width:150px;
}

.track-result{
    display:none;
    margin-top:15px;
    background:#f4f4f4;
    border-radius:14px;
    padding:17px;
    line-height:2;
}

.table-wrap{
    overflow-x:auto;
}

table{
    width:100%;
    min-width:900px;
    border-collapse:collapse;
}

th,
td{
    padding:12px 7px;
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
    margin-top:30px;
    font-size:13px;
    color:#333;
}

@media(max-width:950px){
    .market{
        grid-template-columns:repeat(3,1fr);
    }
}

@media(max-width:650px){
    .market{
        grid-template-columns:repeat(2,1fr);
    }

    .exchange-grid,
    .wallets{
        grid-template-columns:1fr;
    }

    .track-row{
        flex-direction:column;
    }

    .track{
        width:100%;
    }

    .logo{
        font-size:26px;
    }
}
</style>
</head>

<body>

<div class="container">

<header>

    <div class="logo">
        صرافی آنلاین
    </div>

    <div class="subtitle">
        خرید، فروش و تبدیل ارز دیجیتال
    </div>

    <div class="connection">

        <span id="dot" class="dot"></span>

        <span id="connectionText">
            در حال دریافت قیمت...
        </span>

    </div>

    <div class="themes">

        <button class="theme"
                onclick="setTheme('yellow')">
            زرد
        </button>

        <button class="theme"
                onclick="setTheme('blue')">
            آبی
        </button>

        <button class="theme"
                onclick="setTheme('purple')">
            بنفش
        </button>

        <button class="theme"
                onclick="setTheme('orange')">
            نارنجی
        </button>

    </div>

</header>


<div class="title">
    قیمت آنلاین ارزها
</div>

<div id="market" class="market"></div>


<section class="exchange">

<h2>
    تبدیل ارز دیجیتال
</h2>

<div class="exchange-grid">

<div class="box">

<label>
    ارزی که ارسال می‌کنید
</label>

<select id="fromCoin">
    <option value="BTC">BTC</option>
    <option value="BCH">BCH</option>
    <option value="TRX">TRX</option>
    <option value="LTC">LTC</option>
    <option value="DOGE">DOGE</option>
    <option value="USDT">USDT</option>
</select>

<div id="fromPrice"
     class="coin-current">
    قیمت: در انتظار...
</div>

<br>

<label>
    مقدار ارسال
</label>

<input
    id="amount"
    type="number"
    min="0"
    step="any"
    placeholder="مثلاً 0.01"
>

<div class="result">
    ارزش ارسال:
    <span id="sendUsd">0</span>
    USDT
</div>

</div>


<div class="box">

<label>
    ارزی که دریافت می‌کنید
</label>

<select id="toCoin">
    <option value="DOGE">DOGE</option>
    <option value="BTC">BTC</option>
    <option value="BCH">BCH</option>
    <option value="TRX">TRX</option>
    <option value="LTC">LTC</option>
    <option value="USDT">USDT</option>
</select>

<div id="toPrice"
     class="coin-current">
    قیمت: در انتظار...
</div>

<br>

<label>
    مقدار دریافت
</label>

<input
    id="receive"
    type="text"
    readonly
    placeholder="محاسبه خودکار"
>

<div class="result">
    ارزش دریافت:
    <span id="receiveUsd">0</span>
    USDT
</div>

</div>

</div>


<div class="rate">

    نرخ تبدیل:

    <strong id="rateText">
        در انتظار قیمت...
    </strong>

</div>


<div class="wallets">

<div class="wallet">

<h3>
    آدرس واریز ارز ارسالی
</h3>

<div
    id="depositAddress"
    class="address"
>
    در انتظار انتخاب ارز
</div>

<button
    class="copy"
    onclick="copyAddress()"
>
    کپی آدرس
</button>

</div>


<div class="wallet">

<h3>
    آدرس کیف پول دریافت‌کننده
</h3>

<input
    id="receiveWallet"
    type="text"
    dir="ltr"
    placeholder="آدرس کیف پول خود را وارد کنید"
>

</div>

</div>


<button
    class="submit"
    onclick="submitExchange()"
>
    ثبت درخواست تبدیل
</button>

</section>


<section class="tracking">

<h2>
    پیگیری تراکنش
</h2>

<div class="track-row">

<input
    id="trackInput"
    type="text"
    dir="ltr"
    placeholder="کد پیگیری"
>

<button
    class="track"
    onclick="trackTransaction()"
>
    پیگیری
</button>

</div>

<div
    id="trackResult"
    class="track-result"
></div>

</section>


<section class="transactions">

<h2>
    تراکنش‌های ثبت‌شده
</h2>

<div class="table-wrap">

<table>

<thead>
<tr>
    <th>کد</th>
    <th>ارسال</th>
    <th>دریافت</th>
    <th>مقدار ارسال</th>
    <th>مقدار دریافت</th>
    <th>USDT</th>
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
    قیمت‌ها از دو منبع بازار دریافت می‌شوند و در صورت قطعی موقت، آخرین قیمت معتبر حفظ می‌شود.
</footer>

</div>


<script>

/* ==========================================
   API ها
========================================== */

const COINGECKO_API =
"https://api.coingecko.com/api/v3/simple/price";

const LBANK_API =
"https://api.lbkex.com/v2/ticker/24hr.do";


/* ==========================================
   CoinGecko IDs
========================================== */

const cgIds = {

    BTC:"bitcoin",
    BCH:"bitcoin-cash",
    TRX:"tron",
    LTC:"litecoin",
    DOGE:"dogecoin"

};


/* ==========================================
   ارزها
========================================== */

const coins = [
    "BTC",
    "BCH",
    "TRX",
    "LTC",
    "DOGE",
    "USDT"
];


/* ==========================================
   آدرس‌ها
========================================== */

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


/* ==========================================
   آخرین قیمت معتبر
========================================== */

let prices = {

    BTC:null,
    BCH:null,
    TRX:null,
    LTC:null,
    DOGE:null,
    USDT:1

};


/* ==========================================
   زمان آخرین بروزرسانی
========================================== */

let lastUpdate = {

    BTC:null,
    BCH:null,
    TRX:null,
    LTC:null,
    DOGE:null,
    USDT:Date.now()

};


/* ==========================================
   وضعیت منابع
========================================== */

let sourceStatus = {

    coingecko:false,
    lbank:false

};


/* ==========================================
   CoinGecko
========================================== */

async function getCoinGeckoPrices(){

    try{

        const ids =
            Object.values(cgIds)
            .join(",");

        const url =
            COINGECKO_API +
            "?ids=" +
            encodeURIComponent(ids) +
            "&vs_currencies=usd" +
            "&include_last_updated_at=true" +
            "&_=" +
            Date.now();


        const response =
            await fetch(
                url,
                {
                    cache:"no-store"
                }
            );


        if(!response.ok){

            throw new Error(
                "CoinGecko HTTP " +
                response.status
            );

        }


        const data =
            await response.json();


        const result = {};


        for(const coin of coins){

            if(coin === "USDT"){
                continue;
            }


            const id =
                cgIds[coin];


            const value =
                Number(
                    data?.[id]?.usd
                );


            if(
                Number.isFinite(value) &&
                value > 0
            ){

                result[coin] =
                    value;

            }

        }


        sourceStatus.coingecko =
            Object.keys(result).length > 0;


        return result;


    }catch(error){

        console.error(
            "CoinGecko:",
            error
        );

        sourceStatus.coingecko =
            false;

        return {};

    }

}


/* ==========================================
   LBank
========================================== */

async function getLBankPrice(symbol){

    try{

        const pair =
            symbol.toLowerCase() +
            "_usdt";


        const url =
            LBANK_API +
            "?symbol=" +
            encodeURIComponent(pair) +
            "&_=" +
            Date.now();


        const response =
            await fetch(
                url,
                {
                    cache:"no-store"
                }
            );


        if(!response.ok){

            throw new Error(
                "LBank HTTP " +
                response.status
            );

        }


        const json =
            await response.json();


        let value = null;


        if(
            json?.data &&
            Array.isArray(json.data)
        ){

            const item =
                json.data[0];


            value =
                Number(
                    item?.latest ??
                    item?.latestPrice ??
                    item?.price ??
                    item?.close
                );

        }
        else if(json?.data){

            value =
                Number(
                    json.data.latest ??
                    json.data.latestPrice ??
                    json.data.price ??
                    json.data.close
                );

        }


        if(
            !Number.isFinite(value) ||
            value <= 0
        ){

            throw new Error(
                "LBank price invalid"
            );

        }


        return value;


    }catch(error){

        console.error(
            "LBank:",
            symbol,
            error
        );

        return null;

    }

}


/* ==========================================
   دریافت قیمت‌های LBank
========================================== */

async function getAllLBankPrices(){

    const result = {};

    const responses =
        await Promise.all(
            coins
                .filter(
                    coin =>
                    coin !== "USDT"
                )
                .map(
                    async coin => {

                        return {
                            coin,
                            price:
                            await getLBankPrice(
                                coin
                            )
                        };

                    }
                )
        );


    responses.forEach(item => {

        if(
            item.price !== null &&
            Number.isFinite(item.price) &&
            item.price > 0
        ){

            result[item.coin] =
                item.price;

        }

    });


    sourceStatus.lbank =
        Object.keys(result).length > 0;


    return result;

}


/* ==========================================
   دریافت همزمان دو منبع
========================================== */

async function updatePrices(){

    setConnection(
        "در حال دریافت قیمت‌های آنلاین...",
        true
    );


    const [
        gecko,
        lbank
    ] =
    await Promise.all([
        getCoinGeckoPrices(),
        getAllLBankPrices()
    ]);


    let updated = 0;


    /*
       اگر هر دو قیمت موجود باشند،
       میانگین آن دو استفاده می‌شود.

       اگر فقط یکی موجود باشد،
       همان استفاده می‌شود.

       اگر هیچ‌کدام موجود نباشد،
       قیمت قبلی حفظ می‌شود.
    */

    for(const coin of coins){

        if(coin === "USDT"){
            continue;
        }


        const a =
            Number(gecko[coin]);


        const b =
            Number(lbank[coin]);


        let newPrice = null;


        const validA =
            Number.isFinite(a) &&
            a > 0;


        const validB =
            Number.isFinite(b) &&
            b > 0;


        if(validA && validB){

            /*
              میانگین دو منبع
            */

            newPrice =
                (a + b) / 2;

        }
        else if(validA){

            newPrice = a;

        }
        else if(validB){

            newPrice = b;

        }


        if(
            newPrice !== null &&
            Number.isFinite(newPrice) &&
            newPrice > 0
        ){

            prices[coin] =
                newPrice;

            lastUpdate[coin] =
                Date.now();

            updated++;

        }

    }


    prices.USDT = 1;


    renderMarket();

    calculate();

    updateDepositAddress();


    /*
       وضعیت اتصال
    */

    if(
        sourceStatus.coingecko &&
        sourceStatus.lbank
    ){

        setConnection(
            "قیمت‌ها آنلاین هستند • هر ۲۰ ثانیه بررسی می‌شوند",
            true
        );

    }
    else if(
        sourceStatus.coingecko ||
        sourceStatus.lbank
    ){

        setConnection(
            "یک منبع قیمت فعال است • قیمت‌ها به‌روز می‌شوند",
            true
        );

    }
    else if(
        updated === 0
    ){

        setConnection(
            "اتصال موقتاً قطع است • آخرین قیمت حفظ شده",
            false
        );

    }

}


/* ==========================================
   وضعیت اتصال
========================================== */

function setConnection(text, online){

    document.getElementById(
        "connectionText"
    ).textContent = text;


    const dot =
        document.getElementById(
            "dot"
        );


    if(online){

        dot.classList.remove(
            "off"
        );

    }else{

        dot.classList.add(
            "off"
        );

    }

}


/* ==========================================
   نمایش قیمت‌ها
========================================== */

function renderMarket(){

    const market =
        document.getElementById(
            "market"
        );


    market.innerHTML = "";


    coins.forEach(coin => {

        const price =
            prices[coin];


        const valid =
            price !== null &&
            Number.isFinite(price);


        let status =
            "در انتظار قیمت";

        let cls =
            "status wait";


        if(valid){

            if(
                coin === "USDT" ||
                sourceStatus.coingecko ||
                sourceStatus.lbank
            ){

                status =
                    "● آنلاین";

                cls =
                    "status";

            }
            else{

                status =
                    "● آخرین قیمت";

                cls =
                    "status old";

            }

        }


        const card =
            document.createElement(
                "div"
            );


        card.className =
            "card";


        card.innerHTML = `

            <div class="coin">
                ${coin}
            </div>

            <div class="price">
                ${
                    valid
                    ? formatPrice(price) +
                      " USDT"
                    : "در انتظار..."
                }
            </div>

            <div class="${cls}">
                ${status}
            </div>

            <div class="source-info">
                ${getSourceText(coin)}
            </div>

        `;


        market.appendChild(card);

    });

}


/* ==========================================
   منبع قیمت
========================================== */

function getSourceText(coin){

    if(coin === "USDT"){
        return "قیمت پایه";
    }


    const gecko =
        sourceStatus.coingecko;

    const lbank =
        sourceStatus.lbank;


    if(gecko && lbank){
        return "۲ منبع فعال";
    }

    if(gecko){
        return "۱ منبع فعال";
    }

    if(lbank){
        return "۱ منبع فعال";
    }

    if(prices[coin] !== null){
        return "آخرین قیمت معتبر";
    }

    return "بدون قیمت";

}


/* ==========================================
   فرمت
========================================== */

function formatPrice(value){

    if(
        value === null ||
        !Number.isFinite(value)
    ){

        return "—";

    }


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


/* ==========================================
   محاسبه تبدیل
========================================== */

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


    document.getElementById(
        "fromPrice"
    ).textContent =
        fromPrice !== null
        ? "قیمت: " +
          formatPrice(fromPrice) +
          " USDT"
        : "قیمت: در انتظار...";


    document.getElementById(
        "toPrice"
    ).textContent =
        toPrice !== null
        ? "قیمت: " +
          formatPrice(toPrice) +
          " USDT"
        : "قیمت: در انتظار...";


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
        amount *
        fromPrice;


    const receiveAmount =
        sendUsd /
        toPrice;


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
            receiveAmount *
            toPrice
        );


    const rate =
        fromPrice /
        toPrice;


    document.getElementById(
        "rateText"
    ).innerHTML =
        `1 ${from} = <strong>${formatPrice(rate)}</strong> ${to}`;

}


/* ==========================================
   آدرس
========================================== */

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


/* ==========================================
   کپی
========================================== */

async function copyAddress(){

    const address =
        document.getElementById(
            "depositAddress"
        ).textContent;


    try{

        await navigator.clipboard.writeText(
            address
        );

        alert(
            "آدرس کپی شد"
        );

    }catch(e){

        const textarea =
            document.createElement(
                "textarea"
            );

        textarea.value =
            address;

        document.body.appendChild(
            textarea
        );

        textarea.select();

        document.execCommand(
            "copy"
        );

        textarea.remove();

        alert(
            "آدرس کپی شد"
        );

    }

}


/* ==========================================
   ثبت درخواست
========================================== */

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


    if(
        !Number.isFinite(amount) ||
        amount <= 0
    ){

        alert(
            "مقدار ارسال را وارد کنید"
        );

        return;

    }


    if(!receive){

        alert(
            "قیمت هنوز دریافت نشده است"
        );

        return;

    }


    if(!wallet){

        alert(
            "آدرس کیف پول دریافت‌کننده را وارد کنید"
        );

        return;

    }


    const id =
        "EX" +
        Date.now()
        .toString()
        .slice(-10);


    const item = {

        id:id,

        from:from,

        to:to,

        amount:amount,

        receive:receive,

        usd:
            formatPrice(
                amount *
                prices[from]
            ),

        wallet:wallet,

        time:
            new Date()
            .toLocaleString(
                "fa-IR"
            ),

        status:
            "در حال بررسی"

    };


    const list =
        JSON.parse(
            localStorage.getItem(
                "exchangeTransactions"
            ) ||
            "[]"
        );


    list.unshift(item);


    localStorage.setItem(
        "exchangeTransactions",
        JSON.stringify(list)
    );


    renderTransactions();


    document.getElementById(
        "trackInput"
    ).value = id;


    alert(
        "درخواست ثبت شد\n\nکد پیگیری: " +
        id
    );

}


/* ==========================================
   تراکنش‌ها
========================================== */

function renderTransactions(){

    const body =
        document.getElementById(
            "transactionsBody"
        );


    const list =
        JSON.parse(
            localStorage.getItem(
                "exchangeTransactions"
            ) ||
            "[]"
        );


    body.innerHTML = "";


    list.forEach(item => {

        const tr =
            document.createElement(
                "tr"
            );


        const cls =
            item.status ===
            "انجام شد"
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

            <td class="${cls}">
                ${item.status}
            </td>

        `;


        body.appendChild(tr);

    });

}


/* ==========================================
   پیگیری
========================================== */

function trackTransaction(){

    const id =
        document.getElementById(
            "trackInput"
        ).value.trim();


    const result =
        document.getElementById(
            "trackResult"
        );


    result.style.display =
        "block";


    const list =
        JSON.parse(
            localStorage.getItem(
                "exchangeTransactions"
            ) ||
            "[]"
        );


    const item =
        list.find(
            x =>
            x.id === id
        );


    if(!item){

        result.innerHTML =
            "<b>تراکنش پیدا نشد.</b>";

        return;

    }


    result.innerHTML = `

        <b>کد پیگیری:</b>
        ${item.id}

        <br>

        <b>ارسال:</b>
        ${item.amount} ${item.from}

        <br>

        <b>دریافت:</b>
        ${item.receive} ${item.to}

        <br>

        <b>ارزش:</b>
        ${item.usd} USDT

        <br>

        <b>کیف پول:</b>
        <span dir="ltr">
            ${item.wallet}
        </span>

        <br>

        <b>وضعیت:</b>
        ${item.status}

    `;

}


/* ==========================================
   تم
========================================== */

function setTheme(theme){

    if(theme === "yellow"){

        document.body.style.background =
            "linear-gradient(135deg,#fff700,#ffae00)";

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


/* ==========================================
   رویدادها
========================================== */

document.getElementById(
    "fromCoin"
).addEventListener(
    "change",
    function(){

        updateDepositAddress();
        calculate();

    }
);


document.getElementById(
    "toCoin"
).addEventListener(
    "change",
    calculate
);


document.getElementById(
    "amount"
).addEventListener(
    "input",
    calculate
);


/* ==========================================
   شروع سایت
========================================== */

updateDepositAddress();

renderMarket();

renderTransactions();

updatePrices();


/*
   هر 20 ثانیه دوباره از
   CoinGecko و LBank درخواست می‌شود.
*/

setInterval(
    updatePrices,
    20000
);

</script>
<!-- ===== Bitcoin Live Price Widget ===== -->
<div id="btc-live-widget">
  <div class="btc-box">

    <div class="btc-left">
      <img
        src="https://assets.coingecko.com/coins/images/1/large/bitcoin.png"
        class="btc-logo"
        alt="Bitcoin"
      >

      <div>
        <div class="btc-title">Bitcoin</div>
        <div class="btc-symbol">BTC / USD</div>
      </div>
    </div>

    <div class="btc-center">
      <div id="btc-price">در حال دریافت...</div>
      <div id="btc-status">
        <span id="btc-light"></span>
        <span id="btc-status-text">در حال اتصال...</span>
      </div>
    </div>

  </div>
</div>

<style>
#btc-live-widget{
  width:100%;
  max-width:650px;
  margin:18px auto;
  font-family:Arial,Tahoma,sans-serif;
}

.btc-box{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
  padding:18px 20px;
  border-radius:18px;
  background:rgba(20,20,20,.94);
  box-shadow:0 8px 30px rgba(0,0,0,.25);
  color:white;
  border:1px solid rgba(255,255,255,.12);
}

.btc-left{
  display:flex;
  align-items:center;
  gap:12px;
}

.btc-logo{
  width:55px;
  height:55px;
  border-radius:50%;
  display:block;
}

.btc-title{
  font-size:20px;
  font-weight:bold;
}

.btc-symbol{
  margin-top:5px;
  font-size:13px;
  opacity:.65;
}

.btc-center{
  text-align:right;
}

#btc-price{
  font-size:25px;
  font-weight:bold;
  direction:ltr;
  white-space:nowrap;
}

#btc-status{
  margin-top:7px;
  font-size:12px;
  display:flex;
  align-items:center;
  justify-content:flex-end;
  gap:6px;
}

#btc-light{
  width:9px;
  height:9px;
  border-radius:50%;
  background:#777;
  display:inline-block;
}

/* چراغ روشن */
#btc-light.online{
  background:#00ff66;
  box-shadow:0 0 8px #00ff66,0 0 16px #00ff66;
  animation:btcBlink 1.2s infinite;
}

/* چراغ خاموش */
#btc-light.offline{
  background:#ff3030;
  box-shadow:0 0 7px #ff3030;
}

@keyframes btcBlink{
  0%,100%{
    opacity:1;
  }
  50%{
    opacity:.25;
  }
}

@media(max-width:500px){
  .btc-box{
    padding:14px;
  }

  .btc-logo{
    width:45px;
    height:45px;
  }

  .btc-title{
    font-size:17px;
  }

  #btc-price{
    font-size:18px;
  }
}
</style>

<script>
(function(){

  const BTC_API =
    "https://api.coingecko.com/api/v3/simple/price" +
    "?ids=bitcoin&vs_currencies=usd&include_last_updated_at=true";

  let lastBTCPrice = null;

  const priceElement = document.getElementById("btc-price");
  const lightElement = document.getElementById("btc-light");
  const statusElement = document.getElementById("btc-status-text");

  function showOnline(price){

    lastBTCPrice = price;

    priceElement.textContent =
      "$" + Number(price).toLocaleString("en-US", {
        minimumFractionDigits: 2,
        maximumFractionDigits: 2
      });

    lightElement.className = "online";
    statusElement.textContent = "آنلاین";
    statusElement.style.color = "#00ff66";
  }

  function showOffline(){

    lightElement.className = "offline";

    if(lastBTCPrice !== null){

      priceElement.textContent =
        "$" + Number(lastBTCPrice).toLocaleString("en-US", {
          minimumFractionDigits: 2,
          maximumFractionDigits: 2
        });

      statusElement.textContent = "آخرین قیمت";
      statusElement.style.color = "#ffcc00";

    }else{

      priceElement.textContent = "قیمت در دسترس نیست";
      statusElement.textContent = "قطع";
      statusElement.style.color = "#ff3030";
    }
  }

  async function getBitcoinPrice(){

    try{

      const response = await fetch(
        BTC_API + "&_=" + Date.now(),
        {
          method:"GET",
          cache:"no-store"
        }
      );

      if(!response.ok){
        throw new Error("API Error");
      }

      const data = await response.json();

      const price = Number(data?.bitcoin?.usd);

      if(!Number.isFinite(price) || price <= 0){
        throw new Error("Invalid BTC price");
      }

      showOnline(price);

    }catch(error){

      console.log("Bitcoin price API error:", error);

      showOffline();
    }
  }

  // بار اول
  getBitcoinPrice();

  // بررسی دوباره هر 60 ثانیه
  setInterval(getBitcoinPrice, 60000);

})();
</script>
<!-- ===== End Bitcoin Live Price Widget ===== -->
</body>
</html>
