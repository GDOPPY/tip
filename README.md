hai help me up fellass
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Support Doppy</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background-image: url('https://source.unsplash.com/1600x900/?abstract,light');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      position: relative;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      z-index: 0;
    }

    .container {
      position: relative;
      z-index: 2;
      background-color: rgba(255, 255, 255, 0.95);
      padding: 24px;
      border-radius: 12px;
      text-align: center;
      box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.2);
      max-width: 360px;
      width: 90%;
    }

    h1 {
      color: #4CAF50;
      margin-bottom: 10px;
    }

    p {
      color: #555;
      font-size: 1em;
      margin-bottom: 20px;
    }

    .donate-button {
      display: inline-block;
      background-color: #4CAF50;
      color: #fff;
      padding: 14px 28px;
      text-decoration: none;
      border-radius: 6px;
      font-size: 1.1em;
      transition: background-color 0.3s ease;
    }

    .donate-button:hover {
      background-color: #45a049;
    }

    .qr-code {
      display: none;
      margin: 20px 0;
    }

    .qr-code img {
      width: 200px;
      height: 200px;
    }

    @media (min-width: 768px) {
      .qr-code {
        display: block;
      }

      .donate-button {
        display: none;
      }
    }

    /* Bird shadow animation */
    .bird-shadow {
      position: absolute;
      top: 20%;
      left: -100px;
      width: 80px;
      height: 40px;
      background: radial-gradient(ellipse at center, rgba(0, 0, 0, 0.2) 0%, transparent 70%);
      border-radius: 50%;
      transform: scaleX(2) rotate(15deg);
      animation: flyAcross 12s linear infinite;
      z-index: 1;
    }

    @keyframes flyAcross {
      0% {
        left: -100px;
        top: 20%;
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      50% {
        top: 30%;
        transform: scaleX(2) rotate(10deg);
      }
      90% {
        opacity: 1;
      }
      100% {
        left: 110%;
        top: 25%;
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="overlay"></div>
  <div class="bird-shadow"></div>

  <div class="container">
    <h1>Support Doppy</h1>
    <p>If you enjoy my work, feel free to support me with a tip via UPI.</p>

    <a href="upi://pay?pa=7510960026@fam&pn=Doppy&cu=INR" class="donate-button">Tip via UPI</a>

    <div class="qr-code">
      <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=upi://pay?pa=7510960026@fam&pn=Doppy&cu=INR" alt="Scan to pay via UPI" />
      <p style="margin-top: 10px;">Scan with your UPI app</p>
    </div>
  </div>
</body>
</html>
