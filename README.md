<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>行行股票心法班</title>
  <style>
    body {
      margin: 0;
      font-family: 'Noto Sans TC', sans-serif;
      background-color: #fff;
      text-align: center;
    }

    .header {
      background-color: #ffeb00;
      color: #000;
      font-weight: 700;
      padding: 20px 0;
      font-size: 1.5em;
    }

    iframe {
      width: 80%;
      max-width: 800px;
      height: 450px;
      border-radius: 10px;
      border: none;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .video-section {
      background: #000;
      padding: 40px 0;
    }

    .note {
      color: red;
      font-weight: bold;
      margin-top: 10px;
    }

    .countdown {
      margin-top: 40px;
      display: flex;
      justify-content: center;
      gap: 20px;
    }

    .count-box {
      background-color: #d11a1a;
      color: white;
      font-weight: bold;
      padding: 20px;
      border-radius: 8px;
      min-width: 80px;
    }

    .label {
      font-size: 0.8em;
      color: #222;
      margin-top: 5px;
    }

    h2 {
      margin-top: 20px;
      font-weight: 700;
    }
  </style>
</head>
<body>

  <div class="header">⇊行行股票心法班⇊</div>

  <div class="video-section">
    <!-- 把下面的 YouTube 影片 ID 換成你自己的 -->
    <iframe src="https://www.youtube.com/watch?v=VoIBecCM34U?autoplay=1&mute=1" 
      allow="autoplay; encrypted-media" allowfullscreen></iframe>
    <div class="note">⇈ 點擊上方影片框觀看課程 ⇈</div>
  </div>

  <div class="countdown">
    <div class="count-box">
      <div id="hours">00</div>
      <div class="label">HOUR</div>
    </div>
    <div class="count-box">
      <div id="minutes">00</div>
      <div class="label">MINUTES</div>
    </div>
    <div class="count-box">
      <div id="seconds">00</div>
      <div class="label">SECONDS</div>
    </div>
  </div>

  <h2>倒計時結束後</h2>
<h3 style="color:red; font-weight:700; margin-top:5px;">優惠將結束！</h3>


  <script>
    // 倒數一小時後自動跳轉
    const countdownTime = new Date().getTime() + (1 * 60 * 60 * 1000);

    const timer = setInterval(() => {
      const now = new Date().getTime();
      const distance = countdownTime - now;

      const hours = Math.floor((distance / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((distance / (1000 * 60)) % 60);
      const seconds = Math.floor((distance / 1000) % 60);

      document.getElementById('hours').textContent = String(hours).padStart(2, '0');
      document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
      document.getElementById('seconds').textContent = String(seconds).padStart(2, '0');

      if (distance < 0) {
        clearInterval(timer);
        // 倒數結束後自動跳轉下一頁（改成你自己的頁面名稱或網址）
        window.location.href = "offer.html";
      }
    }, 1000);
  </script>

</body>
</html>
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>限時優惠頁 - 掃地僧股票投資班</title>
  <style>
    body {
      margin: 0;
      font-family: 'Noto Sans TC', sans-serif;
      background-color: #e6d8f5;
      color: #000;
      text-align: center;
    }

    h1 {
      font-size: 1.8em;
      font-weight: 700;
      margin: 40px 0 20px;
    }

    h1 span {
      color: red;
    }

    .container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 30px;
      padding: 20px;
    }

    @media(min-width: 900px) {
      .container {
        flex-direction: row;
        align-items: flex-start;
        justify-content: center;
      }
    }

    .left img {
      width: 350px;
      max-width: 90vw;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .right {
      text-align: left;
      max-width: 400px;
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    ul {
      list-style: none;
      padding: 0;
    }

    ul li::before {
      content: '✔';
      color: green;
      margin-right: 8px;
    }

    .price {
      margin-top: 10px;
      font-size: 1.2em;
    }

    .price del {
      color: gray;
      margin-right: 10px;
    }

    .highlight {
      color: red;
      font-weight: 700;
    }

    .btn {
      background-color: #e62222;
      color: #fff;
      font-weight: bold;
      border: none;
      padding: 15px 25px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 10px;
      animation: swing 2s infinite ease-in-out;
    }

    @keyframes swing {
      0%, 100% { transform: translateX(0); }
      50% { transform: translateX(5px); }
    }

    .progress-section {
      margin-top: 40px;
      text-align: center;
    }

    .progress-bar {
      width: 80%;
      max-width: 500px;
      height: 25px;
      background-color: #ddd;
      border-radius: 20px;
      overflow: hidden;
      margin: 0 auto;
      box-shadow: inset 0 0 5px rgba(0,0,0,0.3);
    }

    .progress-fill {
      height: 100%;
      width: 95%; /* 假設238/250 */
      background: linear-gradient(90deg, #ff4b2b, #ff0000);
      text-align: right;
      color: white;
      padding-right: 10px;
      font-size: 0.8em;
      line-height: 25px;
    }

    .bottom-btn {
      background-color: #ff2c2c;
      color: #fff;
      font-weight: bold;
      padding: 18px 30px;
      border: none;
      border-radius: 8px;
      margin-top: 30px;
      animation: swing 2s infinite ease-in-out;
    }

  </style>
</head>
<body>

  <h1>如何在<span>3個月內</span>建立一個自動化年賺<span>六位數</span>的投資系統？</h1>

  <div class="container">
    <div class="left">
      <!-- 放置圖片的地方 -->
      <img src="assets/course-placeholder.jpg" alt="投資課程示意圖">
    </div>
    <div class="right">
      <ul>
        <li>資金不大</li>
        <li>英數不好</li>
        <li>不會專業的金融知識</li>
        <li>一直在股市虧錢</li>
      </ul>
      <div class="price">
        <del>原價：1888 USD</del>
        <span class="highlight">限時優惠價：1488 USD</span>
      </div>
      <button class="btn">立即領取優惠 21% OFF</button>
      <p style="font-size: 0.8em; color: #333;">一次付費，終身會員，永久觀看</p>
    </div>
  </div>

  <div class="progress-section">
    <p>優惠名額只有<span class="highlight">250</span>名<br>滿額後價格將回到原價：1,888 USD</p>
    <div class="progress-bar">
      <div class="progress-fill">238 / 250</div>
    </div>
    <button class="bottom-btn">把握機會，立即使用優惠</button>
  </div>

</body>
</html>
