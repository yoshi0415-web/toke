<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>秒数表示アプリ</title>
</head>
<body>

  <h1>秒数表示アプリ</h1>

  <div id="seconds">0秒</div>

  <button onclick="startTimer()">開始</button>
  <button onclick="stopTimer()">停止</button>
  <button onclick="resetTimer()">リセット</button>

  <script>
    let count = 0;
    let timer = null;

    function startTimer() {
      if (timer !== null) return;

      timer = setInterval(function() {
        count++;
        document.getElementById("seconds").textContent = count + "秒";
      }, 1000);
    }

    function stopTimer() {
      clearInterval(timer);
      timer = null;
    }

    function resetTimer() {
      clearInterval(timer);
      timer = null;
      count = 0;
      document.getElementById("seconds").textContent = "0秒";
    }
  </script>

</body>
</html>