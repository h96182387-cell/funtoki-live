<!DOCTYPE html>
<html>
<head>
  <title>FunToki Live</title>
  <style>
    body {
      margin: 0;
      background: black;
      color: white;
      font-family: Arial;
      text-align: center;
    }

    h1 {
      padding: 10px;
    }

    video {
      width: 100%;
      height: 80vh;
      object-fit: cover;
    }

    .live {
      position: absolute;
      top: 15px;
      left: 15px;
      background: red;
      padding: 5px 10px;
      font-weight: bold;
      border-radius: 5px;
    }
  </style>
</head>

<body>

<div class="live">LIVE</div>

<h1>FunToki Live</h1>

<video id="video" autoplay muted playsinline></video>

<script>
  navigator.mediaDevices.getUserMedia({ video: true, audio: true })
    .then(stream => {
      document.getElementById("video").srcObject = stream;
    })
    .catch(error => {
      alert("Camera access denied!");
    });
</script>

</body>
</html>
