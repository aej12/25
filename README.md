<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>광고 시청 후 자료 보기</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding-top: 60px;
    }
    .btn {
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin: 10px;
    }
    .ad-button {
      background-color: #007aff;
      color: white;
    }
    .go-button {
      background-color: gray;
      color: white;
    }
    .go-button.active {
      background-color: #28a745;
    }
    .disclosure {
      font-size: 14px;
      color: #555;
      background-color: #f9f9f9;
      border: 1px solid #eee;
      border-radius: 8px;
      padding: 12px;
      width: fit-content;
      margin: 0 auto 40px auto;
      line-height: 1.5;
    }
  </style>
</head>
<body>

  <!-- ✅ 공정위 문구 (상단 고정) -->
  <div class="disclosure">
    본 페이지는 <strong>쿠팡파트너스 활동</strong>의 일환으로,<br>
    해당 링크를 통해 구매 시 <strong>일정액의 수수료를 제공받을 수 있습니다.</strong><br>
    이 내용은 <strong>공정거래위원회 ‘추천·보증 등에 관한 표시·광고 지침’</strong>을 준수합니다.
  </div>

  <h2>📢 광고를 먼저 봐주세요!</h2>
  <p>쿠팡 광고를 클릭하면 자료 다운로드 버튼이 활성화됩니다.</p>

  <!-- 쿠팡 광고 버튼 -->
  <button class="btn ad-button" onclick="handleAdClick()">✅ 쿠팡 인기 상품 보기</button>

  <!-- 구글 스프레드시트로 이동 버튼 (처음엔 비활성화) -->
  <button id="goBtn" class="btn go-button" disabled>📄 공유자료 보기</button>

  <script>
    function handleAdClick() {
      // 쿠팡 링크 새 탭으로 열기
      window.open("https://link.coupang.com/a/cGwzg1", "_blank");

      // 공유자료 버튼 활성화
      const goBtn = document.getElementById("goBtn");
      goBtn.disabled = false;
      goBtn.classList.add("active");

      // 클릭 시 구글 스프레드시트로 이동
      goBtn.onclick = function () {
        window.location.href = "https://docs.google.com/spreadsheets/d/1ZMnoCzsS4JZzUt5gQgiAyF0AtfBK0UKn7kp37umQ0M8/edit?usp=drivesdk";
      };
    }
  </script>

</body>
</html>
