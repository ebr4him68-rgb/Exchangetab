
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0">
<meta name="theme-color" content="#07111f">
<title>ExchangeTab | صرافی دیجیتال</title>

<style>
:root{
 --bg:#07111f;
 --panel:#0d1b2e;
 --panel2:#10243b;
 --text:#f5f7fb;
 --muted:#8fa4bb;
 --line:rgba(255,255,255,.09);
 --primary:#00e5ff;
 --secondary:#00d084;
 --gold:#ffd400;
 --danger:#ff4d67;
 --shadow:0 20px 60px rgba(0,0,0,.28);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
 margin:0;
 background:
 radial-gradient(circle at 10% 10%,rgba(0,229,255,.10),transparent 28%),
 radial-gradient(circle at 90% 20%,rgba(0,208,132,.08),transparent 30%),
 var(--bg);
 color:var(--text);
 font-family:Tahoma,Arial,sans-serif;
 min-height:100vh;
}
button,input,select{font:inherit}
button{cursor:pointer}
a{color:inherit;text-decoration:none}

.app{
 width:min(1400px,100%);
 margin:auto;
 padding:16px;
}

.topbar{
 position:sticky;
 top:10px;
 z-index:1000;
 display:flex;
 align-items:center;
 justify-content:space-between;
 gap:12px;
 padding:12px 16px;
 background:rgba(7,17,31,.86);
 backdrop-filter:blur(18px);
 border:1px solid var(--line);
 border-radius:22px;
 box-shadow:var(--shadow);
}

.brand{
 display:flex;
 align-items:center;
 gap:11px;
 font-weight:900;
}
.logo{
 width:44px;
 height:44px;
 border-radius:14px;
 display:grid;
 place-items:center;
 background:linear-gradient(135deg,var(--primary),var(--secondary));
 color:#001018;
 font-size:23px;
 box-shadow:0 0 25px rgba(0,229,255,.25);
}
.brand small{
 display:block;
 color:var(--muted);
 font-size:10px;
 margin-top:3px;
}

.top-actions{
 display:flex;
 gap:8px;
}
.icon-btn{
 width:43px;
 height:43px;
 border:1px solid var(--line);
 border-radius:14px;
 background:var(--panel);
 color:var(--text);
 position:relative;
}
.icon-btn:hover{border-color:var(--primary)}
.badge{
 position:absolute;
 top:-4px;
 left:-4px;
 min-width:18px;
 height:18px;
 border-radius:20px;
 background:var(--danger);
 color:#fff;
 font-size:10px;
 display:grid;
 place-items:center;
}

.hero{
 margin-top:18px;
 display:grid;
 grid-template-columns:1.25fr .75fr;
 gap:18px;
}

.hero-main,.hero-side,.card{
 background:linear-gradient(145deg,rgba(16,36,59,.96),rgba(9,24,40,.96));
 border:1px solid var(--line);
 border-radius:28px;
 box-shadow:var(--shadow);
}

.hero-main{
 padding:30px;
 min-height:290px;
 display:flex;
 flex-direction:column;
 justify-content:center;
 overflow:hidden;
 position:relative;
}
.hero-main:after{
 content:"";
 position:absolute;
 width:300px;
 height:300px;
 border-radius:50%;
 background:rgba(0,229,255,.08);
 left:-80px;
 bottom:-140px;
}
.hero-main h1{
 font-size:clamp(28px,5vw,54px);
 margin:0 0 12px;
 line-height:1.15;
}
.gradient{
 background:linear-gradient(90deg,var(--primary),var(--secondary),var(--gold));
 -webkit-background-clip:text;
 color:transparent;
}
.hero-main p{
 color:var(--muted);
 max-width:700px;
 line-height:1.9;
 margin:0 0 22px;
}
.status{
 display:inline-flex;
 align-items:center;
 gap:8px;
 width:max-content;
 background:rgba(0,208,132,.09);
 border:1px solid rgba(0,208,132,.25);
 padding:8px 13px;
 border-radius:30px;
 color:#6dffc4;
 font-size:12px;
}
.dot{
 width:8px;height:8px;border-radius:50%;
 background:#00d084;
 box-shadow:0 0 12px #00d084;
 animation:pulse 1.3s infinite;
}
@keyframes pulse{50%{opacity:.3;transform:scale(.7)}}

.hero-side{
 padding:20px;
 display:flex;
 flex-direction:column;
 justify-content:space-between;
}
.balance-label{color:var(--muted);font-size:13px}
.balance{
 font-size:34px;
 font-weight:900;
 margin:8px 0;
}
.balance span{font-size:14px;color:var(--muted)}
.quick-row{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:9px;
}
.quick{
 border:1px solid var(--line);
 background:rgba(255,255,255,.03);
 border-radius:15px;
 padding:12px;
 color:var(--text);
}
.quick b{display:block;margin-bottom:4px}
.quick span{color:var(--muted);font-size:11px}

.market{
 margin-top:18px;
}
.section-title{
 display:flex;
 align-items:center;
 justify-content:space-between;
 margin-bottom:12px;
}
.section-title h2{margin:0;font-size:20px}
.section-title span{color:var(--muted);font-size:12px}

.coins{
 display:grid;
 grid-template-columns:repeat(6,1fr);
 gap:10px;
}
.coin{
 padding:15px;
 border-radius:19px;
 background:var(--panel);
 border:1px solid var(--line);
 transition:.2s;
}
.coin:hover{transform:translateY(-3px);border-color:rgba(0,229,255,.35)}
.coin-head{
 display:flex;
 justify-content:space-between;
 align-items:center;
 gap:5px;
}
.coin-icon{
 width:35px;height:35px;border-radius:12px;
 display:grid;place-items:center;
 background:linear-gradient(135deg,var(--primary),var(--secondary));
 color:#001018;font-weight:900;
}
.coin-symbol{font-weight:900}
.coin-name{color:var(--muted);font-size:10px;margin-top:7px}
.coin-price{font-weight:900;margin-top:12px;font-size:16px}
.up{color:#42e6a4;font-size:11px;margin-top:5px}
.down{color:#ff7185;font-size:11px;margin-top:5px}

.main-grid{
 margin-top:18px;
 display:grid;
 grid-template-columns:1fr 1fr;
 gap:18px;
}

.card{padding:22px}

.tabs{
 display:flex;
 gap:8px;
 margin-bottom:18px;
}
.tab{
 flex:1;
 border:1px solid var(--line);
 background:rgba(255,255,255,.03);
 color:var(--muted);
 border-radius:13px;
 padding:11px;
}
.tab.active{
 background:linear-gradient(135deg,var(--primary),var(--secondary));
 color:#001018;
 font-weight:900;
}

.field{
 margin-bottom:13px;
}
.field label{
 display:block;
 color:var(--muted);
 font-size:12px;
 margin-bottom:7px;
}
.field input,.field select{
 width:100%;
 border:1px solid var(--line);
 border-radius:14px;
 background:#081625;
 color:#fff;
 padding:13px;
 outline:none;
}
.field input:focus,.field select:focus{
 border-color:var(--primary);
 box-shadow:0 0 0 3px rgba(0,229,255,.08);
}

.amount-row{
 display:grid;
 grid-template-columns:1fr 120px;
 gap:8px;
}
.swap{
 width:42px;
 height:42px;
 border-radius:50%;
 border:1px solid var(--line);
 background:var(--panel2);
 color:var(--primary);
 display:block;
 margin:-4px auto 9px;
}

.primary{
 width:100%;
 border:0;
 border-radius:15px;
 padding:14px;
 background:linear-gradient(135deg,var(--primary),var(--secondary));
 color:#001018;
 font-weight:900;
 box-shadow:0 10px 30px rgba(0,229,255,.12);
}
.primary:hover{filter:brightness(1.08)}

.secondary{
 border:1px solid var(--line);
 background:rgba(255,255,255,.04);
 color:#fff;
 border-radius:13px;
 padding:11px 14px;
}

.result{
 margin-top:14px;
 padding:15px;
 border-radius:16px;
 background:rgba(0,229,255,.05);
 border:1px solid rgba(0,229,255,.13);
}
.result-line{
 display:flex;
 justify-content:space-between;
 gap:10px;
 padding:6px 0;
 color:var(--muted);
}
.result-line strong{color:#fff}

.tx-list{
 display:flex;
 flex-direction:column;
 gap:10px;
 max-height:360px;
 overflow:auto;
}
.tx{
 display:grid;
 grid-template-columns:auto 1fr auto;
 gap:11px;
 align-items:center;
 padding:13px;
 border:1px solid var(--line);
 border-radius:15px;
 background:rgba(255,255,255,.025);
}
.tx-icon{
 width:40px;height:40px;
 border-radius:13px;
 display:grid;place-items:center;
 background:rgba(0,229,255,.08);
 color:var(--primary);
}
.tx b{font-size:13px}
.tx small{display:block;color:var(--muted);margin-top:4px}
.pending{color:#ffd65c;font-size:11px}
.confirmed{color:#42e6a4;font-size:11px}

.exchange-panel{
 margin-top:18px;
 padding:24px;
 border-radius:25px;
 background:
 linear-gradient(135deg,rgba(255,212,0,.07),rgba(0,229,255,.05)),
 var(--panel);
 border:1px solid var(--line);
}
.exchange-head{
 display:flex;
 justify-content:space-between;
 gap:15px;
 align-items:center;
 margin-bottom:18px;
}
.exchange-head h2{margin:0}
.exchange-head p{margin:5px 0 0;color:var(--muted);font-size:12px}

.addresses{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:10px;
 margin-top:15px;
}
.address{
 border:1px solid var(--line);
 border-radius:15px;
 padding:13px;
 background:rgba(255,255,255,.025);
}
.address-head{
 display:flex;
 justify-content:space-between;
 margin-bottom:8px;
}
.address code{
 display:block;
 direction:ltr;
 text-align:left;
 word-break:break-all;
 color:#a9bdd0;
 font-size:10px;
 line-height:1.6;
}
.copy{
 border:0;
 border-radius:9px;
 padding:6px 9px;
 background:rgba(0,229,255,.1);
 color:var(--primary);
 font-size:10px;
}

.news{
 margin-top:18px;
}
.news-box{
 background:#fff;
 color:#111827;
 border-radius:26px;
 padding:20px;
 box-shadow:var(--shadow);
}
.news-grid{
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:15px;
}
.news-card{
 overflow:hidden;
 border:1px solid #e5e7eb;
 border-radius:17px;
 background:#fff;
}
.news-card img{
 width:100%;
 height:160px;
 object-fit:cover;
 background:#eef2f7;
}
.news-body{padding:14px}
.news-source{
 color:#2563eb;
 font-size:11px;
 font-weight:900;
}
.news-card h3{
 font-size:15px;
 line-height:1.6;
 margin:8px 0;
}
.news-card p{
 color:#6b7280;
 font-size:12px;
 line-height:1.7;
 margin:0 0 10px;
}
.news-card a{
 color:#0891b2;
 font-size:12px;
 font-weight:900;
}

.footer{
 text-align:center;
 color:var(--muted);
 padding:35px 10px 100px;
 font-size:11px;
}

.modal{
 position:fixed;
 inset:0;
 background:rgba(0,0,0,.7);
 backdrop-filter:blur(8px);
 display:none;
 align-items:center;
 justify-content:center;
 padding:15px;
 z-index:5000;
}
.modal.show{display:flex}
.modal-box{
 width:min(650px,100%);
 max-height:90vh;
 overflow:auto;
 background:var(--panel);
 border:1px solid var(--line);
 border-radius:25px;
 padding:22px;
 box-shadow:var(--shadow);
}
.modal-head{
 display:flex;
 justify-content:space-between;
 align-items:center;
 margin-bottom:18px;
}
.close{
 width:38px;height:38px;border-radius:12px;
 border:1px solid var(--line);
 background:transparent;color:#fff;
}

.settings-grid{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:10px;
}
.setting{
 padding:14px;
 border-radius:15px;
 border:1px solid var(--line);
 background:rgba(255,255,255,.03);
}
.setting b{display:block;margin-bottom:7px}
.setting small{color:var(--muted)}

.themes{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:10px;
 margin-top:10px;
}
.theme{
 min-height:75px;
 border-radius:16px;
 border:2px solid transparent;
 padding:12px;
 color:#fff;
 text-align:right;
}
.theme.active{border-color:#fff}
.theme-dark{background:linear-gradient(135deg,#07111f,#102b45)}
.theme-neon{background:linear-gradient(135deg,#12002f,#002d35)}
.theme-gold{background:linear-gradient(135deg,#241400,#5a3a00)}
.theme-lady{
 background:
 radial-gradient(circle at 75% 35%,rgba(255,125,190,.55),transparent 18%),
 radial-gradient(ellipse at 73% 65%,rgba(255,180,215,.25),transparent 30%),
 linear-gradient(135deg,#1b0717,#48152e 55%,#12040d);
}

.notice{
 padding:13px;
 border-radius:14px;
 background:rgba(255,212,0,.07);
 border:1px solid rgba(255,212,0,.18);
 color:#ffe27b;
 font-size:11px;
 line-height:1.8;
 margin-top:12px;
}

.toast{
 position:fixed;
 left:50%;
 bottom:22px;
 transform:translate(-50%,120px);
 opacity:0;
 z-index:99999;
 background:#101f30;
 border:1px solid var(--line);
 color:#fff;
 padding:12px 18px;
 border-radius:14px;
 box-shadow:var(--shadow);
 transition:.3s;
 font-size:12px;
}
.toast.show{
 transform:translate(-50%,0);
 opacity:1;
}

@media(max-width:1050px){
 .coins{grid-template-columns:repeat(3,1fr)}
 .hero{grid-template-columns:1fr}
}
@media(max-width:800px){
 .main-grid{grid-template-columns:1fr}
 .news-grid{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:600px){
 .app{padding:9px}
 .topbar{top:5px;padding:10px}
 .brand small{display:none}
 .hero-main{padding:22px}
 .coins{grid-template-columns:repeat(2,1fr)}
 .coin{padding:12px}
 .main-grid{gap:12px}
 .card{padding:16px}
 .addresses{grid-template-columns:1fr}
 .news-grid{grid-template-columns:1fr}
 .amount-row{grid-template-columns:1fr 100px}
 .settings-grid{grid-template-columns:1fr}
}
</style>
</head>

<body>

<div class="app">

<header class="topbar">
 <div class="brand">
   <div class="logo">⇄</div>
   <div>
     <div>ExchangeTab</div>
     <small data-i18n="digitalExchange">صرافی دیجیتال</small>
   </div>
 </div>

 <div class="top-actions">
   <button class="icon-btn" onclick="openModal('messages')">
     🔔
     <span class="badge" id="notificationCount">3</span>
   </button>
   <button class="icon-btn" onclick="openModal('settings')">⚙️</button>
 </div>
</header>


<section class="hero">

 <div class="hero-main">
   <div class="status">
     <span class="dot"></span>
     <span data-i18n="online">بازار آنلاین</span>
   </div>

   <h1>
     <span data-i18n="welcome">تبادل سریع و آسان</span>
     <br>
     <span class="gradient">Crypto Exchange</span>
   </h1>

   <p data-i18n="heroText">
     خرید، فروش و تبدیل ارزهای دیجیتال در یک محیط سریع،
     ساده و مدرن.
   </p>

   <button class="primary" style="max-width:240px" onclick="scrollToExchange()">
     ⚡ <span data-i18n="startExchange">شروع تبادل</span>
   </button>
 </div>


 <div class="hero-side">
   <div>
     <div class="balance-label" data-i18n="portfolio">ارزش تقریبی سبد</div>
     <div class="balance">$0.00 <span>USD</span></div>
     <div class="balance-label" data-i18n="demoBalance">
       موجودی برای نمایش در پنل
     </div>
   </div>

   <div class="quick-row">
     <button class="quick" onclick="setExchange('BTC')">
       <b>BTC</b>
       <span data-i18n="bitcoin">Bitcoin</span>
     </button>
     <button class="quick" onclick="setExchange('USDT')">
       <b>USDT</b>
       <span>Tether</span>
     </button>
     <button class="quick" onclick="setExchange('DOGE')">
       <b>DOGE</b>
       <span>Dogecoin</span>
     </button>
     <button class="quick" onclick="setExchange('LTC')">
       <b>LTC</b>
       <span>Litecoin</span>
     </button>
   </div>
 </div>

</section>


<section class="market">

 <div class="section-title">
   <h2 data-i18n="market">بازار ارزهای دیجیتال</h2>
   <span id="marketUpdated">در حال بروزرسانی...</span>
 </div>

 <div class="coins" id="coins"></div>

</section>


<section class="main-grid">

 <div class="card" id="exchange">

   <div class="section-title">
     <h2 data-i18n="exchange">تبادل آسان</h2>
     <span>LIVE</span>
   </div>

   <div class="tabs">
     <button class="tab active" onclick="setTradeMode('exchange',this)" data-i18n="convert">
       تبدیل
     </button>
     <button class="tab" onclick="setTradeMode('buy',this)" data-i18n="buy">
       خرید
     </button>
     <button class="tab" onclick="setTradeMode('sell',this)" data-i18n="sell">
       فروش
     </button>
   </div>

   <div class="field">
     <label data-i18n="send">می‌فرستم</label>
     <div class="amount-row">
       <input id="sendAmount" type="number" min="0" step="any" value="0.01"
              oninput="calculate()">
       <select id="fromCoin" onchange="calculate()"></select>
     </div>
   </div>

   <button class="swap" onclick="swapCoins()">⇅</button>

   <div class="field">
     <label data-i18n="receive">دریافت می‌کنم</label>
     <div class="amount-row">
       <input id="receiveAmount" readonly>
       <select id="toCoin" onchange="calculate()"></select>
     </div>
   </div>

   <div class="result">
     <div class="result-line">
       <span data-i18n="rate">نرخ تبدیل</span>
       <strong id="rate">-</strong>
     </div>
     <div class="result-line">
       <span data-i18n="fee">کارمزد</span>
       <strong id="fee">0.00%</strong>
     </div>
     <div class="result-line">
       <span data-i18n="estimated">مقدار تقریبی</span>
       <strong id="estimated">$0.00</strong>
     </div>
   </div>

   <button class="primary" style="margin-top:14px" onclick="createTransaction()">
     ⚡ <span data-i18n="createTransaction">ایجاد تراکنش</span>
   </button>

 </div>


 <div class="card">

   <div class="section-title">
     <h2 data-i18n="transactions">تراکنش‌های اخیر</h2>
     <button class="secondary" onclick="openModal('transactions')" data-i18n="all">
       همه
     </button>
   </div>

   <div class="tx-list" id="txList"></div>

 </div>

</section>


<section class="exchange-panel" id="addresses">

 <div class="exchange-head">
   <div>
     <h2 data-i18n="depositAddresses">آدرس‌های واریز</h2>
     <p data-i18n="depositText">
       آدرس ارز موردنظر را کپی کنید. قبل از ارسال، شبکه را بررسی کنید.
     </p>
   </div>
 </div>

 <div class="addresses" id="addressList"></div>

 <div class="notice" data-i18n="networkWarning">
   ⚠️ قبل از واریز حتماً شبکه و نوع ارز را بررسی کنید.
   ارسال روی شبکه اشتباه ممکن است باعث از دست رفتن دارایی شود.
 </div>

</section>


<section class="news">

 <div class="section-title">
   <h2 data-i18n="cryptoNews">اخبار ارزهای دیجیتال</h2>
   <span>LIVE NEWS</span>
 </div>

 <div class="news-box">
   <div class="news-grid" id="newsGrid">
     <div style="padding:30px;text-align:center;color:#6b7280">
       در حال دریافت اخبار...
     </div>
   </div>
 </div>

</section>


<footer class="footer">
  <div>ExchangeTab © 2026</div>
  <div style="margin-top:7px" data-i18n="footerText">
    پلتفرم تبادل دارایی‌های دیجیتال
  </div>
</footer>

</div>


<!-- SETTINGS MODAL -->
<div class="modal" id="settingsModal">
 <div class="modal-box">

  <div class="modal-head">
   <h2 data-i18n="settings">⚙️ تنظیمات</h2>
   <button class="close" onclick="closeModal('settings')">×</button>
  </div>

  <div class="settings-grid">

   <div class="setting">
    <b data-i18n="language">زبان</b>
    <select id="languageSelect" onchange="changeLanguage(this.value)"
            style="width:100%;padding:10px;border-radius:10px;background:#081625;color:#fff;border:1px solid var(--line)">
      <option value="fa">فارسی</option>
      <option value="en">English</option>
      <option value="ru">Русский</option>
    </select>
   </div>

   <div class="setting">
    <b data-i18n="theme">تم سایت</b>
    <small data-i18n="themeText">ظاهر موردنظر خود را انتخاب کنید.</small>
   </div>

  </div>

  <div class="themes">

   <button class="theme theme-dark active" onclick="setTheme('dark',this)">
     🌌 Dark
   </button>

   <button class="theme theme-neon" onclick="setTheme('neon',this)">
     💠 Neon
   </button>

   <button class="theme theme-gold" onclick="setTheme('gold',this)">
     🟡 Gold
   </button>

   <button class="theme theme-lady" onclick="setTheme('lady',this)">
     🌹 بانوی شب
   </button>

  </div>

  <div class="notice">
    🌹 <span data-i18n="ladyText">
    تم بانوی شب با طراحی هنری و غیرصریح برای تغییر فضای ظاهری سایت.
    </span>
  </div>

  <div style="margin-top:15px">
    <button class="primary" onclick="closeModal('settings')" data-i18n="save">
      ذخیره
    </button>
  </div>

 </div>
</div>


<!-- MESSAGES MODAL -->
<div class="modal" id="messagesModal">
 <div class="modal-box">

  <div class="modal-head">
   <h2 data-i18n="messages">🔔 پیام‌ها</h2>
   <button class="close" onclick="closeModal('messages')">×</button>
  </div>

  <div class="tx-list">

   <div class="tx">
    <div class="tx-icon">✓</div>
    <div>
     <b data-i18n="welcomeMessage">به ExchangeTab خوش آمدید</b>
     <small data-i18n="welcomeMessageText">
      پنل جدید شما آماده استفاده است.
     </small>
    </div>
    <span class="confirmed">NEW</span>
   </div>

   <div class="tx">
    <div class="tx-icon">₿</div>
    <div>
     <b>BTC</b>
     <small data-i18n="priceMessage">
      اطلاعات قیمت بازار بروزرسانی شد.
     </small>
    </div>
    <span class="confirmed">LIVE</span>
   </div>

   <div class="tx">
    <div class="tx-icon">⚡</div>
    <div>
     <b data-i18n="security">امنیت</b>
     <small data-i18n="securityText">
      قبل از هر تراکنش آدرس و شبکه را بررسی کنید.
     </small>
    </div>
    <span class="pending">INFO</span>
   </div>

  </div>

 </div>
</div>


<!-- TRANSACTIONS MODAL -->
<div class="modal" id="transactionsModal">
 <div class="modal-box">

  <div class="modal-head">
   <h2 data-i18n="allTransactions">📋 همه تراکنش‌ها</h2>
   <button class="close" onclick="closeModal('transactions')">×</button>
  </div>

  <div class="tx-list" id="allTxList"></div>

 </div>
</div>


<div class="toast" id="toast"></div>


<script>
/* =========================================================
   DATA
========================================================= */

const COINS = {

 BTC:{
   name:"Bitcoin",
   symbol:"BTC",
   icon:"₿",
   price:65000
 },

 BCH:{
   name:"Bitcoin Cash",
   symbol:"BCH",
   icon:"B",
   price:520
 },

 TRX:{
   name:"TRON",
   symbol:"TRX",
   icon:"T",
   price:.25
 },

 LTC:{
   name:"Litecoin",
   symbol:"LTC",
   icon:"Ł",
   price:80
 },

 DOGE:{
   name:"Dogecoin",
   symbol:"DOGE",
   icon:"Ð",
   price:.12
 },

 USDT:{
   name:"Tether",
   symbol:"USDT",
   icon:"₮",
   price:1
 }

};


/*
 آدرس‌هایی که در نسخه قبلی سایت وجود داشتند.
*/

const ADDRESSES = {

 BTC:"1Q99GpYnEU9yELNLjiJUWopNT1HatRYQrV",

 BCH:"bitcoincash:qrj64uh0xlah2wzksudq3g5eeg2ewdyg6urq5kywku",

 LTC:"LZeRDFWbPLpuqeAw7m5i5YcYiu32KRAM6c",

 DOGE:"DA9b1AqJqgsdFNuJNjzRo2g5wFj1rEeQLk",

 TRX:"TRb33idZSi7svRyBTRsEKq8BfL54ADYMh3",

 USDT:"0x3765C083F36B7D874d3a6249436a84C9e9bDAbA6"

};


/* =========================================================
   TRANSLATIONS
========================================================= */

const LANG = {

 fa:{
  digitalExchange:"صرافی دیجیتال",
  online:"بازار آنلاین",
  welcome:"تبادل سریع و آسان",
  heroText:"خرید، فروش و تبدیل ارزهای دیجیتال در یک محیط سریع، ساده و مدرن.",
  startExchange:"شروع تبادل",
  portfolio:"ارزش تقریبی سبد",
  demoBalance:"موجودی برای نمایش در پنل",
  bitcoin:"Bitcoin",
  market:"بازار ارزهای دیجیتال",
  exchange:"تبادل آسان",
  convert:"تبدیل",
  buy:"خرید",
  sell:"فروش",
  send:"می‌فرستم",
  receive:"دریافت می‌کنم",
  rate:"نرخ تبدیل",
  fee:"کارمزد",
  estimated:"مقدار تقریبی",
  createTransaction:"ایجاد تراکنش",
  transactions:"تراکنش‌های اخیر",
  all:"همه",
  depositAddresses:"آدرس‌های واریز",
  depositText:"آدرس ارز موردنظر را کپی کنید. قبل از ارسال، شبکه را بررسی کنید.",
  networkWarning:"⚠️ قبل از واریز حتماً شبکه و نوع ارز را بررسی کنید. ارسال روی شبکه اشتباه ممکن است باعث از دست رفتن دارایی شود.",
  cryptoNews:"اخبار ارزهای دیجیتال",
  footerText:"پلتفرم تبادل دارایی‌های دیجیتال",
  settings:"⚙️ تنظیمات",
  language:"زبان",
  theme:"تم سایت",
  themeText:"ظاهر موردنظر خود را انتخاب کنید.",
  ladyText:"تم بانوی شب با طراحی هنری و غیرصریح برای تغییر فضای ظاهری سایت.",
  save:"ذخیره",
  messages:"🔔 پیام‌ها",
  welcomeMessage:"به ExchangeTab خوش آمدید",
  welcomeMessageText:"پنل جدید شما آماده استفاده است.",
  priceMessage:"اطلاعات قیمت بازار بروزرسانی شد.",
  security:"امنیت",
  securityText:"قبل از هر تراکنش آدرس و شبکه را بررسی کنید.",
  allTransactions:"📋 همه تراکنش‌ها",
  copied:"آدرس کپی شد",
  transactionCreated:"تراکنش ایجاد شد",
  selectDifferent:"دو ارز متفاوت انتخاب کنید.",
  noTransactions:"هنوز تراکنشی ثبت نشده است."
 },

 en:{
  digitalExchange:"Digital Exchange",
  online:"Market Online",
  welcome:"Fast & Easy Exchange",
  heroText:"Buy, sell and exchange digital assets in a fast, simple and modern environment.",
  startExchange:"Start Exchange",
  portfolio:"Estimated Portfolio",
  demoBalance:"Balance shown in the panel",
  bitcoin:"Bitcoin",
  market:"Crypto Market",
  exchange:"Easy Exchange",
  convert:"Convert",
  buy:"Buy",
  sell:"Sell",
  send:"I send",
  receive:"I receive",
  rate:"Exchange Rate",
  fee:"Fee",
  estimated:"Estimated Value",
  createTransaction:"Create Transaction",
  transactions:"Recent Transactions",
  all:"All",
  depositAddresses:"Deposit Addresses",
  depositText:"Copy the address for the selected asset. Check the network before sending.",
  networkWarning:"⚠️ Always verify the asset and network before depositing.",
  cryptoNews:"Crypto News",
  footerText:"Digital asset exchange platform",
  settings:"⚙️ Settings",
  language:"Language",
  theme:"Website Theme",
  themeText:"Choose your preferred appearance.",
  ladyText:"Lady Night theme with an artistic, non-explicit visual style.",
  save:"Save",
  messages:"🔔 Messages",
  welcomeMessage:"Welcome to ExchangeTab",
  welcomeMessageText:"Your new exchange panel is ready.",
  priceMessage:"Market price information was updated.",
  security:"Security",
  securityText:"Always verify the address and network before a transaction.",
  allTransactions:"📋 All Transactions",
  copied:"Address copied",
  transactionCreated:"Transaction created",
  selectDifferent:"Choose two different assets.",
  noTransactions:"No transactions yet."
 },

 ru:{
  digitalExchange:"Криптообменник",
  online:"Рынок онлайн",
  welcome:"Быстрый обмен",
  heroText:"Покупайте, продавайте и обменивайте цифровые активы быстро и удобно.",
  startExchange:"Начать обмен",
  portfolio:"Примерная стоимость",
  demoBalance:"Баланс в панели",
  bitcoin:"Bitcoin",
  market:"Крипторынок",
  exchange:"Быстрый обмен",
  convert:"Обмен",
  buy:"Покупка",
  sell:"Продажа",
  send:"Отправляю",
  receive:"Получаю",
  rate:"Курс обмена",
  fee:"Комиссия",
  estimated:"Примерная сумма",
  createTransaction:"Создать транзакцию",
  transactions:"Последние операции",
  all:"Все",
  depositAddresses:"Адреса пополнения",
  depositText:"Скопируйте адрес выбранного актива. Проверьте сеть перед отправкой.",
  networkWarning:"⚠️ Перед пополнением обязательно проверьте актив и сеть.",
  cryptoNews:"Новости криптовалют",
  footerText:"Платформа обмена цифровых активов",
  settings:"⚙️ Настройки",
  language:"Язык",
  theme:"Тема сайта",
  themeText:"Выберите внешний вид сайта.",
  ladyText:"Тема Lady Night с художественным, неэксплицитным оформлением.",
  save:"Сохранить",
  messages:"🔔 Сообщения",
  welcomeMessage:"Добро пожаловать в ExchangeTab",
  welcomeMessageText:"Ваша новая панель обмена готова.",
  priceMessage:"Информация о рынке обновлена.",
  security:"Безопасность",
  securityText:"Проверяйте адрес и сеть перед каждой транзакцией.",
  allTransactions:"📋 Все транзакции",
  copied:"Адрес скопирован",
  transactionCreated:"Транзакция создана",
  selectDifferent:"Выберите два разных актива.",
  noTransactions:"Транзакций пока нет."
 }

};


/* =========================================================
   INIT
========================================================= */

let currentLang =
 localStorage.getItem("exchangeLang") || "fa";

let currentTheme =
 localStorage.getItem("exchangeTheme") || "dark";

let tradeMode="exchange";

let transactions =
 JSON.parse(
   localStorage.getItem("exchangeTransactions") || "[]"
 );


document.documentElement.lang=currentLang;
document.documentElement.dir=
 currentLang==="fa" ? "rtl":"ltr";


function applyTranslations(){

 const lang=LANG[currentLang];

 document.querySelectorAll("[data-i18n]")
 .forEach(el=>{

   const key=el.getAttribute("data-i18n");

   if(lang[key]){
     el.textContent=lang[key];
   }

 });

 document.documentElement.lang=currentLang;

 document.documentElement.dir=
   currentLang==="fa" ? "rtl":"ltr";

 document.getElementById("languageSelect").value=currentLang;
}


function changeLanguage(lang){

 currentLang=lang;

 localStorage.setItem(
   "exchangeLang",
   lang
 );

 applyTranslations();

 renderCoins();
 renderAddresses();
 renderTransactions();

 toast(
   lang==="fa"
    ?"زبان فارسی فعال شد"
    :lang==="en"
      ?"English enabled"
      :"Русский включён"
 );
}


/* =========================================================
   THEME
========================================================= */

function setTheme(theme,button){

 currentTheme=theme;

 localStorage.setItem(
   "exchangeTheme",
   theme
 );

 document.body.classList.remove(
   "theme-neon-active",
   "theme-gold-active",
   "theme-lady-active"
 );

 if(theme==="neon")
   document.body.classList.add("theme-neon-active");

 if(theme==="gold")
   document.body.classList.add("theme-gold-active");

 if(theme==="lady")
   document.body.classList.add("theme-lady-active");

 document.querySelectorAll(".theme")
 .forEach(x=>x.classList.remove("active"));

 if(button)
   button.classList.add("active");

 applyThemeColors();

 toast(
   currentLang==="fa"
    ?"تم تغییر کرد"
    :currentLang==="en"
      ?"Theme changed"
      :"Тема изменена"
 );
}


function applyThemeColors(){

 const root=document.documentElement;

 if(currentTheme==="neon"){

   root.style.setProperty("--primary","#b66cff");
   root.style.setProperty("--secondary","#00e5ff");
   root.style.setProperty("--gold","#ff44c7");

 }

 else if(currentTheme==="gold"){

   root.style.setProperty("--primary","#ffd400");
   root.style.setProperty("--secondary","#ff9d00");
   root.style.setProperty("--gold","#ffe56b");

 }

 else if(currentTheme==="lady"){

   root.style.setProperty("--primary","#ff6eae");
   root.style.setProperty("--secondary","#d946ef");
   root.style.setProperty("--gold","#ffd1e6");

 }

 else{

   root.style.setProperty("--primary","#00e5ff");
   root.style.setProperty("--secondary","#00d084");
   root.style.setProperty("--gold","#ffd400");

 }
}


/* =========================================================
   COINS
========================================================= */

function renderCoins(){

 const container=
 document.getElementById("coins");

 container.innerHTML="";

 Object.values(COINS).forEach(coin=>{

   const change=
    (Math.random()*5-2.5);

   const card=
   document.createElement("div");

   card.className="coin";

   card.innerHTML=`
     <div class="coin-head">
       <div class="coin-icon">${coin.icon}</div>
       <div class="coin-symbol">${coin.symbol}</div>
     </div>

     <div class="coin-name">${coin.name}</div>

     <div class="coin-price" id="price-${coin.symbol}">
       $${formatPrice(coin.price)}
     </div>

     <div class="${change>=0?'up':'down'}">
       ${change>=0?'▲':'▼'}
       ${Math.abs(change).toFixed(2)}%
     </div>
   `;

   container.appendChild(card);

 });

}


function formatPrice(price){

 if(price>=1000)
   return price.toLocaleString("en-US",{
     maximumFractionDigits:2
   });

 if(price>=1)
   return price.toFixed(2);

 return price.toFixed(4);

}


/* =========================================================
   LIVE PRICES
========================================================= */

async function updatePrices(){

 try{

   const ids=
    "bitcoin,bitcoin-cash,tron,litecoin,dogecoin,tether";

   const response=
    await fetch(
      "https://api.coingecko.com/api/v3/simple/price"+
      "?ids="+ids+
      "&vs_currencies=usd",
      {cache:"no-store"}
    );

   if(!response.ok)
     throw new Error();

   const data=await response.json();

   if(data.bitcoin)
     COINS.BTC.price=data.bitcoin.usd;

   if(data["bitcoin-cash"])
     COINS.BCH.price=data["bitcoin-cash"].usd;

   if(data.tron)
     COINS.TRX.price=data.tron.usd;

   if(data.litecoin)
     COINS.LTC.price=data.litecoin.usd;

   if(data.dogecoin)
     COINS.DOGE.price=data.dogecoin.usd;

   if(data.tether)
     COINS.USDT.price=data.tether.usd;

   renderCoins();

   document.getElementById("marketUpdated").textContent=
     new Date().toLocaleTimeString(
       currentLang==="fa"?"fa-IR":
       currentLang==="ru"?"ru-RU":"en-US"
     );

   calculate();

 }catch(e){

   document.getElementById("marketUpdated").textContent=
     currentLang==="fa"
       ?"قیمت پیش‌فرض"
       :"Fallback prices";

 }

}


/* =========================================================
   SELECTS
========================================================= */

function fillCoinSelects(){

 const from=
  document.getElementById("fromCoin");

 const to=
  document.getElementById("toCoin");

 from.innerHTML="";
 to.innerHTML="";

 Object.values(COINS).forEach(coin=>{

   from.innerHTML+=
    `<option value="${coin.symbol}">
       ${coin.symbol} — ${coin.name}
     </option>`;

   to.innerHTML+=
    `<option value="${coin.symbol}">
       ${coin.symbol} — ${coin.name}
     </option>`;

 });

 from.value="BTC";
 to.value="USDT";

 calculate();
}


function setExchange(symbol){

 document.getElementById("fromCoin").value=symbol;

 if(symbol==="USDT")
   document.getElementById("toCoin").value="BTC";
 else
   document.getElementById("toCoin").value="USDT";

 calculate();

 scrollToExchange();
}


function swapCoins(){

 const from=
  document.getElementById("fromCoin");

 const to=
  document.getElementById("toCoin");

 const temp=from.value;

 from.value=to.value;
 to.value=temp;

 calculate();
}


function calculate(){

 const amount=
  Number(document.getElementById("sendAmount").value)||0;

 const from=
  document.getElementById("fromCoin").value;

 const to=
  document.getElementById("toCoin").value;

 if(!COINS[from]||!COINS[to])
   return;

 if(from===to){

   document.getElementById("receiveAmount").value="0";

   document.getElementById("rate").textContent="1:1";

   document.getElementById("estimated").textContent="$0.00";

   return;
 }

 const gross=
  amount*
  COINS[from].price/
  COINS[to].price;

 const feeRate=.005;

 const net=
  gross*(1-feeRate);

 document.getElementById("receiveAmount").value=
  net.toFixed(8);

 document.getElementById("rate").textContent=
  `1 ${from} ≈ ${(COINS[from].price/COINS[to].price).toFixed(6)} ${to}`;

 document.getElementById("fee").textContent=
  "0.50%";

 document.getElementById("estimated").textContent=
  "$"+(amount*COINS[from].price).toFixed(2);
}


/* =========================================================
   TRADE MODE
========================================================= */

function setTradeMode(mode,button){

 tradeMode=mode;

 document.querySelectorAll(".tab")
 .forEach(t=>t.classList.remove("active"));

 button.classList.add("active");

}


function createTransaction(){

 const amount=
  Number(document.getElementById("sendAmount").value)||0;

 const from=
  document.getElementById("fromCoin").value;

 const to=
  document.getElementById("toCoin").value;

 const receive=
  document.getElementById("receiveAmount").value;

 if(!amount){

   toast(
     currentLang==="fa"
       ?"مقدار را وارد کنید"
       :"Enter an amount"
   );

   return;
 }

 if(from===to){

   toast(LANG[currentLang].selectDifferent);

   return;
 }

 const id=
  "EX"+
  Date.now().toString().slice(-10);

 const tx={

   id:id,

   from:from,

   to:to,

   amount:amount,

   receive:receive,

   mode:tradeMode,

   status:"Pending",

   date:new Date().toISOString()

 };

 transactions.unshift(tx);

 transactions=
  transactions.slice(0,50);

 localStorage.setItem(
   "exchangeTransactions",
   JSON.stringify(transactions)
 );

 renderTransactions();

 toast(
   LANG[currentLang].transactionCreated+
   " • "+id
 );

}


/* =========================================================
   TRANSACTIONS
========================================================= */

function renderTransactions(){

 const list=
  document.getElementById("txList");

 const all=
  document.getElementById("allTxList");

 if(!transactions.length){

   list.innerHTML=
    `<div style="padding:30px;text-align:center;color:var(--muted)">
       ${LANG[currentLang].noTransactions}
     </div>`;

   if(all)
     all.innerHTML=list.innerHTML;

   return;
 }


 const html=
 transactions.map(tx=>{

   const status=
    tx.status==="Confirmed"
      ? `<span class="confirmed">Confirmed</span>`
      : `<span class="pending">Pending</span>`;

   return `
    <div class="tx">

      <div class="tx-icon">
        ⇄
      </div>

      <div>
        <b>${tx.amount} ${tx.from} → ${tx.receive} ${tx.to}</b>
        <small>${tx.id}</small>
      </div>

      <div>
        ${status}
        <small>
          ${new Date(tx.date).toLocaleDateString(
            currentLang==="fa"?"fa-IR":
            currentLang==="ru"?"ru-RU":"en-US"
          )}
        </small>
      </div>

    </div>
   `;

 }).join("");

 list.innerHTML=html;

 if(all)
   all.innerHTML=html;

}


/* =========================================================
   ADDRESSES
========================================================= */

function renderAddresses(){

 const box=
  document.getElementById("addressList");

 box.innerHTML="";

 Object.entries(ADDRESSES).forEach(([symbol,address])=>{

   const coin=COINS[symbol];

   const div=
    document.createElement("div");

   div.className="address";

   div.innerHTML=`

     <div class="address-head">

       <strong>
         ${coin.icon} ${symbol}
       </strong>

       <button
         class="copy"
         onclick="copyAddress('${escapeAttr(address)}')"
       >
         📋
       </button>

     </div>

     <code>${address}</code>

   `;

   box.appendChild(div);

 });

}


function escapeAttr(text){

 return text
  .replace(/&/g,"&amp;")
  .replace(/'/g,"&#39;")
  .replace(/"/g,"&quot;");

}


async function copyAddress(address){

 try{

   await navigator.clipboard.writeText(address);

 }catch(e){

   const textarea=
    document.createElement("textarea");

   textarea.value=address;

   document.body.appendChild(textarea);

   textarea.select();

   document.execCommand("copy");

   textarea.remove();

 }

 toast(LANG[currentLang].copied);

}


/* =========================================================
   NEWS
========================================================= */

const NEWS_FEEDS=[

 {
   name:"CoinDesk",
   url:"https://www.coindesk.com/arc/outboundfeeds/rss/"
 },

 {
   name:"Cointelegraph",
   url:"https://cointelegraph.com/rss"
 },

 {
   name:"Decrypt",
   url:"https://decrypt.co/feed"
 },

 {
   name:"CryptoSlate",
   url:"https://cryptoslate.com/feed/"
 },

 {
   name:"NewsBTC",
   url:"https://www.newsbtc.com/feed/"
 },

 {
   name:"Bitcoinist",
   url:"https://bitcoinist.com/feed/"
 },

 {
   name:"CryptoPotato",
   url:"https://cryptopotato.com/feed/"
 },

 {
   name:"U.Today",
   url:"https://u.today/rss"
 },

 {
   name:"Bitcoin Magazine",
   url:"https://bitcoinmagazine.com/.rss/full/"
 },

 {
   name:"Google News Crypto",
   url:
   "https://news.google.com/rss/search?q=bitcoin%20OR%20ethereum%20OR%20cryptocurrency&hl=en-US&gl=US&ceid=US:en"
 }

];


async function getFeed(feed){


</script>
<!-- =========================
     ثبت معامله + آدرس دریافت
========================= -->

<style>
.trade-box{
  max-width:520px;
  margin:25px auto;
  padding:25px;
  border-radius:18px;
  background:#111827;
  color:white;
  box-shadow:0 10px 35px rgba(0,0,0,.35);
  font-family:Arial,sans-serif;
}

.trade-box h2{
  text-align:center;
  margin-bottom:20px;
}

.trade-box label{
  display:block;
  margin:12px 0 7px;
  font-weight:bold;
}

.trade-box select,
.trade-box input{
  width:100%;
  box-sizing:border-box;
  padding:13px;
  border-radius:10px;
  border:1px solid #374151;
  background:#1f2937;
  color:white;
  outline:none;
  font-size:15px;
}

.trade-box select:focus,
.trade-box input:focus{
  border-color:#f59e0b;
}

.receive-title{
  margin-top:18px;
  padding:12px;
  background:#172033;
  border-radius:10px;
  color:#fbbf24;
  text-align:center;
}

.address-row{
  display:flex;
  gap:8px;
}

.address-row input{
  flex:1;
}

.copy-btn{
  width:90px;
  border:0;
  border-radius:10px;
  background:#374151;
  color:white;
  cursor:pointer;
}

.trade-btn{
  width:100%;
  margin-top:20px;
  padding:15px;
  border:0;
  border-radius:12px;
  background:#f59e0b;
  color:#111827;
  font-size:17px;
  font-weight:bold;
  cursor:pointer;
}

.trade-btn:hover{
  background:#fbbf24;
}

.message{
  margin-top:15px;
  padding:12px;
  border-radius:10px;
  display:none;
  text-align:center;
}

.success{
  display:block;
  background:#064e3b;
  color:#a7f3d0;
}

.error{
  display:block;
  background:#7f1d1d;
  color:#fecaca;
}

.trade-result{
  display:none;
  margin-top:20px;
  padding:15px;
  border-radius:12px;
  background:#0f172a;
  border:1px solid #374151;
}

.trade-result div{
  margin:8px 0;
  word-break:break-all;
}

.public-address{
  color:#fbbf24;
}
</style>


<div class="trade-box">

  <h2>🔄 ثبت معامله</h2>

  <label>ارزی که می‌دهید</label>

  <select id="giveCoin">
    <option value="DOGE">DOGE</option>
    <option value="BTC">BTC</option>
    <option value="BCH">BCH</option>
    <option value="LTC">LTC</option>
    <option value="USDT">USDT</option>
    <option value="ETH">ETH</option>
  </select>


  <label>ارزی که می‌خواهید دریافت کنید</label>

  <select id="receiveCoin">
    <option value="BTC">BTC</option>
    <option value="DOGE">DOGE</option>
    <option value="BCH">BCH</option>
    <option value="LTC">LTC</option>
    <option value="USDT">USDT</option>
    <option value="ETH">ETH</option>
  </select>


  <label>مقدار ارز</label>

  <input
    type="number"
    id="amount"
    placeholder="مثلاً 100"
    min="0"
    step="any"
  >


  <div class="receive-title">
    📥 آدرس کیف پول برای دریافت ارز
  </div>


  <label id="addressLabel">
    آدرس کیف پول BTC
  </label>

  <div class="address-row">

    <input
      type="text"
      id="receiveAddress"
      placeholder="آدرس کیف پول خود را وارد کنید"
      autocomplete="off"
    >

    <button
      type="button"
      class="copy-btn"
      onclick="pasteAddress()">
      Paste
    </button>

  </div>


  <button
    type="button"
    class="trade-btn"
    onclick="createTrade()">

    ثبت معامله

  </button>


  <div id="message" class="message"></div>


  <div id="tradeResult" class="trade-result">

    <div>
      <strong>شماره معامله:</strong>
      <span id="tradeId"></span>
    </div>

    <div>
      <strong>پرداختی:</strong>
      <span id="resultGive"></span>
    </div>

    <div>
      <strong>دریافتی:</strong>
      <span id="resultReceive"></span>
    </div>

    <div>
      <strong>آدرس دریافت:</strong><br>
      <span
        id="resultAddress"
        class="public-address">
      </span>
    </div>

    <div>
      <strong>وضعیت:</strong>
      <span>⏳ در انتظار پرداخت</span>
    </div>

  </div>

</div>


<script>

const receiveCoin = document.getElementById("receiveCoin");

const addressLabel = document.getElementById("addressLabel");

const receiveAddress = document.getElementById("receiveAddress");


// تغییر نام ارز کنار قسمت آدرس
receiveCoin.addEventListener("change", function(){

  addressLabel.textContent =
    "آدرس کیف پول " + this.value;

  receiveAddress.placeholder =
    "آدرس کیف پول " + this.value + " را وارد کنید";

});


// Paste
async function pasteAddress(){

  try{

    const text =
      await navigator.clipboard.readText();

    receiveAddress.value = text.trim();

  }catch(e){

    showMessage(
      "امکان Paste خودکار وجود ندارد؛ آدرس را دستی وارد کنید.",
      "error"
    );

  }

}


// بررسی ساده فرمت آدرس
function checkAddress(address, coin){

  address = address.trim();

  if(!address){
    return false;
  }

  // BTC
  if(coin === "BTC"){

    return /^(bc1|[13])[a-zA-HJ-NP-Z0-9]{25,90}$/i.test(address);

  }


  // DOGE
  if(coin === "DOGE"){

    return /^D[a-zA-Z0-9]{25,34}$/.test(address);

  }


  // BCH
  if(coin === "BCH"){

    return /^(bitcoincash:)?(q|p)[a-z0-9]{40,60}$/i.test(address);

  }


  // LTC
  if(coin === "LTC"){

    return /^(ltc1|[LM3])[a-zA-Z0-9]{20,90}$/i.test(address);

  }


  // ETH / USDT ERC20
  if(coin === "ETH" || coin === "USDT"){

    return /^0x[a-fA-F0-9]{40}$/.test(address);

  }


  return address.length >= 10;

}


// ثبت معامله
function createTrade(){

  const give =
    document.getElementById("giveCoin").value;

  const receive =
    document.getElementById("receiveCoin").value;

  const amount =
    document.getElementById("amount").value.trim();

  const address =
    receiveAddress.value.trim();


  // جلوگیری از یکسان بودن ارزها
  if(give === receive){

    showMessage(
      "ارز پرداختی و دریافتی نمی‌توانند یکسان باشند.",
      "error"
    );

    return;
  }


  // مقدار
  if(!amount || Number(amount) <= 0){

    showMessage(
      "لطفاً مقدار معامله را وارد کنید.",
      "error"
    );

    return;
  }


  // آدرس
  if(!address){

    showMessage(
      "لطفاً آدرس کیف پول دریافت‌کننده را وارد کنید.",
      "error"
    );

    receiveAddress.focus();

    return;
  }


  // اعتبارسنجی آدرس
  if(!checkAddress(address, receive)){

    showMessage(
      "فرمت آدرس کیف پول با ارز انتخاب‌شده مطابقت ندارد.",
      "error"
    );

    receiveAddress.focus();

    return;
  }


  // شماره معامله
  const tradeId =
    "TR-" +
    Date.now().toString().slice(-10);


  // نمایش معامله
  document.getElementById("tradeId").textContent =
    tradeId;

  document.getElementById("resultGive").textContent =
    amount + " " + give;

  document.getElementById("resultReceive").textContent =
    receive;

  document.getElementById("resultAddress").textContent =
    address;


  document.getElementById("tradeResult").style.display =
    "block";


  showMessage(
    "✅ معامله با موفقیت ثبت شد.",
    "success"
  );


  // ذخیره موقت معامله در مرورگر
  const trade = {

    id: tradeId,

    giveCoin: give,

    receiveCoin: receive,

    amount: amount,

    receiveAddress: address,

    status: "pending",

    createdAt: new Date().toISOString()

  };


  localStorage.setItem(
    "trade_" + tradeId,
    JSON.stringify(trade)
  );


  // ذخیره در لیست معاملات
  let trades =
    JSON.parse(
      localStorage.getItem("trades") || "[]"
    );

  trades.push(trade);

  localStorage.setItem(
    "trades",
    JSON.stringify(trades)
  );

}


// پیام
function showMessage(text,type){

  const message =
    document.getElementById("message");

  message.textContent = text;

  message.className =
    "message " + type;

}

</script>
</body>
</html>
```
