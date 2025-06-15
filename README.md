# ip-tracker
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Kiểm tra IP và vị trí</title>
</head>
<body>
  <h2>Đang xác định vị trí của bạn...</h2>
  <pre id="output"></pre>

  <script>
    fetch('https://ipapi.co/json/')
      .then(res => res.json())
      .then(data => {
        document.getElementById("output").textContent = JSON.stringify(data, null, 2);
      });
  </script>
</body>
</html>
