<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>부자 카톡</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #111;
      margin: 0;
      padding: 40px 0;
      display: flex;
      justify-content: center;
    }

    /* 📱 스마트폰 프레임 */
    .phone-frame {
      width: 420px;
      max-width: 100%;
      background-color: #222;
      border-radius: 30px;
      overflow: hidden;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
    }

    /* 🟨 상단 헤더 */
    .chat-header {
      background-color: #f5f5f5;
      color: #000;
      text-align: center;
      padding: 15px 10px;
      font-weight: bold;
      font-size: 18px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
      position: sticky;
      top: 0;
      z-index: 999;
    }

    .chat-container {
      padding: 20px;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .chat-item {
      display: none;
      flex-direction: column;
      align-items: flex-start;
    }

    .chat-item.dad {
      align-items: flex-end;
    }

    .bubble {
      padding: 10px 15px;
      border-radius: 15px;
      max-width: 80%;
      line-height: 1.5;
      word-break: break-word;
    }

    .user .bubble {
      background-color: #3b5998;
      border-top-left-radius: 0;
      color: #fff;
    }

    .dad .bubble {
      background-color: #ffeb3b;
      color: #000;
      border-top-right-radius: 0;
    }

    .timestamp {
      font-size: 0.75em;
      color: #aaa;
      margin-top: 3px;
    }

    .unread {
      color: #1e90ff;
      font-weight: bold;
      margin-left: 5px;
    }
  </style>
</head>
<body>

  <!-- 📱 스마트폰 본체 -->
  <div class="phone-frame">
    <!-- 🟨 상단 채팅방 제목 -->
    <div class="chat-header">사랑하는 울 아들</div>

    <!-- 💬 대화 영역 -->
    <div class="chat-container" onclick="showNextMessage()">
      <div class="chat-item user"><div class="bubble">아빠</div><div class="timestamp">오전 8:57</div></div>
      <div class="chat-item user"><div class="bubble">사랑하는 막내 아들♥</div><div class="timestamp">오전 8:59</div></div>
      <div class="chat-item user"><div class="bubble">아ㅍ</div><div class="timestamp">오전 8:59</div></div>
      <div class="chat-item user"><div class="bubble">아빠 사랑해</div><div class="timestamp">오전 8:59</div></div>
      <div class="chat-item user"><div class="bubble">사랑해요</div><div class="timestamp">오전 9:00</div></div>

      <div class="chat-item dad"><div class="bubble">왜~ 사랑 고백!<br>아빠도 사랑한다 ♥♥♥<br>날씨가 꿀꿀.. 신나게 놀다 와라<br>도착하면 엄마한테 문자 주고</div><div class="timestamp">오전 9:07<span class="unread">1</span></div></div>

      <div class="chat-item dad"><div class="bubble">아들</div><div class="timestamp">오전 9:26<span class="unread">1</span></div></div>
      <div class="chat-item dad"><div class="bubble">전화 주라</div><div class="timestamp">오전 9:34<span class="unread">1</span></div></div>
      <div class="chat-item dad"><div class="bubble">사랑한다<br>아들아<br>제발... 무사히 살아만 있어다오...</div><div class="timestamp">오전 10:03<span class="unread">1</span></div></div>
    </div>
  </div>

  <script>
    const chatItems = document.querySelectorAll('.chat-item');
    let index = 0;

    function showNextMessage() {
      if (index < chatItems.length) {
        chatItems[index].style.display = 'flex';
        index++;
      }
    }

    // 첫 메시지 표시
    showNextMessage();
  </script>
</body>
</html>
