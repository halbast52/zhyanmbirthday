<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Birthday Eman 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom right, #ffe6f0, #fff5fa);
      font-family: 'Segoe UI', sans-serif;
      color: #333;
      text-align: center;
    }
    .container {
      padding: 40px 20px;
      max-width: 600px;
      margin: auto;
    }
    h1 {
      font-size: 2.5em;
      color: #d63384;
    }
    .message {
      margin-top: 20px;
      font-size: 1.2em;
      white-space: pre-wrap;
      line-height: 1.6;
    }
    .button {
      margin-top: 30px;
      padding: 15px 30px;
      font-size: 1em;
      background-color: #ff69b4;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .button:hover {
      background-color: #ff1493;
    }
    .hidden-content {
      margin-top: 20px;
      display: none;
    }
    iframe {
      margin-top: 20px;
      border-radius: 10px;
    }
    .image-wrapper {
      margin-top: 20px;
    }
    img {
      width: 100%;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Happy Birthday to My Beautiful Eman 💖</h1>
    <div class="message">
      Emany 🥺💖 mn qwrbāni daqa ba daqay tamany tw bm...<br>
      Amn bmbwra, hich hadyakm nabw lōt namtani law rozhā jwanay.<br>
      Shtakt pesh kāsh kam, bas datanm pr ba dl blem... xoshmdāweyy hamw kasm atw.<br>
      Hadyay xwday labo mn rābē, xwa labo mnt bēly.<br>
      <strong>Muahhhh 😘</strong><br>
      Sārt zor zor’m xoshdāweyy 😭💕<br>
      Taqān’m — jazhny la dayk bunt peroza, taqāni dli mn. 🎂🌹
    </div>

    <button class="button" onclick="showGiftAndPlayAudio()">
      Click here for your gift 🎁
    </button>

    <div class="hidden-content">
      <div class="image-wrapper">
        <img src="https://i.postimg.cc/yk9Zmp2j/your-image.jpg" alt="Birthday Image" />
      </div>
    </div>
  </div>

  <script>
    function showGiftAndPlayAudio() {
      document.querySelector('.hidden-content').style.display = 'block';
      document.querySelector('.button').style.display = 'none';

      // Create an iframe to play the audio
      const audioIframe = document.createElement('iframe');
      audioIframe.width = 0;
      audioIframe.height = 0;
      audioIframe.src = "https://www.youtube.com/embed/nyuo9-OjNNg?autoplay=1&loop=1&playlist=nyuo9-OjNNg";
      audioIframe.frameBorder = 0;
      audioIframe.allow = "autoplay; encrypted-media";  // Allow autoplay and encrypted media
      audioIframe.style.display = "none";  // Hide iframe as it's just for playing audio
      
      document.body.appendChild(audioIframe);

      // Ensure the audio starts when the iframe is loaded
      audioIframe.onload = function() {
        const iframeWindow = audioIframe.contentWindow;
        iframeWindow.postMessage('{"event":"command","func":"playVideo","args":""}', '*');
      };
    }
  </script>
</body>
</html>
