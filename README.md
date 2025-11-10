
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
      background-color: #ffe500;
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
    <!-- 將下面 src 換成你的 YouTube 影片 ID，例如 https://www.youtube.com/watch?v=dQw4w9WgXcQ -->
    <iframe src="https://www.youtube.com/watch?v=VoIBecCM34U&mute=1" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    <div class="note">⇈ 點擊上方影片觀看投資班 ⇈</div>
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

  <h2>倒數結束後</h2>

  <script>
    // 設定倒數計時（例如 1 小時後結束）
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
        document.querySelector('.countdown').innerHTML = '<h3>時間到！</h3>';
      }
    }, 1000);
  </script>

</body>
</html>
