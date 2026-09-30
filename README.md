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
