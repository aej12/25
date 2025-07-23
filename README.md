<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>광고 시청 후 자료 보기</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding-top: 100px;
    }
    a.ad-button {
      display: inline-block;
      padding: 15px 30px;
      background-color: #007aff;
      color: white;
      text-decoration: none;
      font-size: 18px;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <h2>광고를 먼저 봐주세요 😊</h2>
  <p>👉 광고를 클릭하면 공유자료로 이동합니다!</p>

  <!-- 쿠팡 광고 클릭 시 새 창으로 열고, 현재 페이지는 구글 스프레드시트로 이동 -->
  <a class="ad-button" href="#" onclick="goToCoupangAndThenSpreadsheet()">✅ 쿠팡 인기 상품 보기</a>

  <script>
    function goToCoupangAndThenSpreadsheet() {
      // 쿠팡 링크 새 창으로 열기
      window.open("https://link.coupang.com/a/cGwzg1", "_blank");

      // 0.5초 뒤에 구글 스프레드시트로 이동
      setTimeout(function() {
        window.location.href = "https://docs.google.com/spreadsheets/d/1ZMnoCzsS4JZzUt5gQgiAyF0AtfBK0UKn7kp37umQ0M8/edit?gid=1500292523";
      }, 500);
    }
  </script>

</body>
</html>
