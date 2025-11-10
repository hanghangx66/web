<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>行行股票心法班</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Noto Sans TC', sans-serif;
      background-color: #e8d8f5; /* 整體底色（下半部淡紫） */
    }

    .top-section {
      background-color: #ffffff; /* 上半部白底 */
      text-align: center;
      padding-bottom: 40px;
    }

    .header {
      background-color: #ffeb00;
      color: #000;
      font-weight: 700;
      padding: 20px 0;
      font-size: 1.5em;
    }

    .video-section {
      background: #000;
      padding: 40px 0;
    }

    iframe {
      width: 80%;
      max-width: 800px;
      height: 450px;
      border-radius: 10px;
      border: none;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .note {
      color: red;
      font-weight: bold;
      margin-top: 10px;
    }

    .bottom-section {
      text-align: center;
      padding: 50px 0;
      background-color: #e8d8f5;
    }

    .countdown {
      margin-top: 20px;
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
      color: #fff;
      margin-top: 5px;
    }

    h2 {
      margin-top: 30px;
      font-weight: 700;
    }

    h3 {
      margin-top: 10px;
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="top-section">
    <div class="header">⇊行行股票心法班⇊</div>

    <div class="video-section">
      <!-- 換成你的 YouTube 影片 ID -->
      <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1&mute=1" 
        allow="autoplay; encrypted-media" allowfullscreen></iframe>
      <div class="note">⇈ 點擊上方影片框觀看課程 ⇈</div>
    </div>
  </div>

  <div class="bottom-section">
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
    <h3>優惠將結束！</h3>
  </div>

  <script>
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
        window.location.href = "offer.html"; // 自動跳轉到下一頁
      }
    }, 1000);
  </script>

</body>
</html>
