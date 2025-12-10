<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Open Letter</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f3f3f3;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      text-align: center;
      max-width: 350px;
    }
    button {
      padding: 10px 20px;
      border: none;
      background: #ff7ea5;
      color: white;
      border-radius: 10px;
      cursor: pointer;
      font-size: 18px;
      margin-top: 15px;
      transition: 0.2s;
    }
    button:hover {
      background: #ff5c8d;
    }
    #letterScreen {
      display: none;
      flex-direction: column;
      gap: 15px;
      max-width: 500px;
      width: 90%;
    }
    textarea {
      width: 100%;
      height: 300px;
      padding: 15px;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 16px;
      resize: none;
    }
    .letter-container {
      display: none;
      flex-direction: column;
      align-items: center;
      width: 100%;
    }

    .letter-paper {
      background: #fffaf0;
      padding: 30px;
      border-radius: 15px;
      border: 2px solid #e7d7c1;
      box-shadow: 0 6px 20px rgba(0,0,0,0.1);
      max-width: 600px;
      width: 90%;
      position: relative;
    }

    .letter-paper::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 40px;
      background: repeating-linear-gradient(
        to bottom,
        #f5e6cc 0px,
        #f5e6cc 4px,
        transparent 4px,
        transparent 8px
      );
      border-top-left-radius: 15px;
      border-top-right-radius: 15px;
      opacity: 0.6;
      pointer-events: none;
    }

    .letter-text {
      width: 100%;
      height: 350px;
      padding: 15px;
      border-radius: 10px;
      border: 1px solid #d6c3a1;
      background: #fffdf7;
      font-size: 17px;
      line-height: 1.5;
      resize: none;
      font-family: "Georgia", serif;
    }
  </style>
</head>
<body>

  <div id="homeScreen" class="card">
    <h2>A Letter for You</h2>
    <p>Click below to open it.</p>
    <button onclick="openLetter()">Open Me</button>
  </div>

  <div id="letterScreen" class="letter-container">
    <div class="letter-paper">
      <h2>💌 Your Letter</h2>
      <textarea id="letterText" class="letter-text">Write your letter here...</textarea>
    </div>
  </div>

  <script>
    function openLetter() {
      document.getElementById('homeScreen').style.display = 'none';
      document.getElementById('letterScreen').style.display = 'flex';
    }
  </script>

</body>
</html>
