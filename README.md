# Uk
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tsunami Airdrop</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f0f8ff;
    }
    .container {
      margin-top: 50px;
    }
    .button {
      display: inline-block;
      padding: 10px 20px;
      font-size: 18px;
      color: white;
      background-color: #007bff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 20px;
    }
    .button:hover {
      background-color: #0056b3;
    }
    .coins {
      font-size: 24px;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Welcome to Tsunami Airdrop 🌊</h1>
    <div id="coins" class="coins">Coins: 0</div>
    <button class="button" id="collectCoins">Collect Coins</button>
    <button class="button" id="inviteFriends">Invite Friends</button>
  </div>

  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <script>
    Telegram.WebApp.ready();

    // دریافت اطلاعات کاربر از تلگرام
    let user = Telegram.WebApp.initDataUnsafe.user;
    let coins = 0;

    document.getElementById('collectCoins').addEventListener('click', () => {
      coins += 10;
      document.getElementById('coins').innerText = `Coins: ${coins}`;
      Telegram.WebApp.showAlert(`You collected 10 coins! Total: ${coins}`);
    });

    document.getElementById('inviteFriends').addEventListener('click', () => {
      Telegram.WebApp.showAlert('Invite your friends!');
    });

  </script>
</body>
</html>
