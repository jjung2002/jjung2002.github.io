# jjung2002.github.io


<style>
  body {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #121212; /* 어두운 배경색 */
    color: #ffffff;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 40px 20px;
  }
  
  /* 유니티 캔버스를 감싸는 컨테이너 디자인 */
  #unity-container {
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.8);
    border-radius: 8px;
    overflow: hidden;
    background-color: #232323;
  }

  .game-title {
    font-size: 28px;
    font-weight: bold;
    margin-bottom: 10px;
  }

  .game-description {
    font-size: 16px;
    color: #b3b3b3;
    margin-bottom: 30px;
    text-align: center;
    max-width: 600px;
    line-height: 1.5;
  }
</style>

<body>
  <div class="game-title">게임 프로젝트 이름</div>
  <div class="game-description">
    여기에 게임의 간단한 설명과 조작법(예: WASD 이동, 마우스 좌클릭 사격 등)을 작성합니다.
  </div>
  
  <div id="unity-container" class="unity-desktop">
