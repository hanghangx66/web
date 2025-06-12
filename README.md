<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <title>行行行贊助頁</title>
  <script async src="https://js.stripe.com/v3/buy-button.js"></script>
  <style>
    body {
      background-color: #111;
      color: white;
      font-family: sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }
    h1 {
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <h1>行行行贊助頁</h1>
  <stripe-buy-button
    buy-button-id="buy_btn_1RZ5sAGATWi8yAKo8j7Us82x"
    publishable-key="pk_live_51JQQ0h9GATWi8yAKoTLYAZp9ko478LYn7N04wWbo9wHZAXtDus5YLY8EEqbXT5porUvVRc9txtKANzJMoUSJmoQPMsVb0y0VzFc0p">
  </stripe-buy-button>
</body>
</html>
