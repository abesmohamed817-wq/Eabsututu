<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>موقع الحب</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #ffe6e6;
      font-family: Arial, sans-serif;
      text-align: center;
      cursor: pointer;
    }
    h1 {
      font-size: 3em;
      color: #b30000;
    }
  </style>
</head>
<body id="body">
  <h1>مريم، أنتِ قلبي</h1>

  <audio id="music" loop>
    <source src="song.mp3" type="audio/mpeg">
  </audio>

  <script>
    const audio = document.getElementById("music");
    const body = document.getElementById("body");

    // أي ضغطة في الصفحة تشغل الموسيقى
    body.addEventListener("click", () => {
      audio.play();
    });

    // محاولة تشغيل تلقائي
    audio.play().catch(() => {
      console.log("الموسيقى ستبدأ بعد أول نقرة على الصفحة");
    });
  </script>
</body>
</html>
