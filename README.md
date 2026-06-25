# jjung2002.github.io

<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="utf-8">
    <title>Unity WebGL Player | jjung2002.github.io</title>
    <link rel="shortcut icon" href="TemplateData/favicon.ico">
    <link rel="stylesheet" href="TemplateData/style.css">
    
    <style>
      body {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: #121212;
        color: #ffffff;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        margin: 0;
        padding: 40px 20px;
      }
      
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
  </head>
  <body>
    <div class="game-title">타워 디펜스 & FPS 하이브리드 프로젝트</div>
    <div class="game-description">
      타워를 배치하여 방어선을 구축하고, 1인칭 시점으로 직접 전투에 참여하는 하이브리드 게임입니다.<br>
      조작법: WASD 이동, 마우스 좌클릭 사격, 숫자 키로 타워 선택
    </div>
    
    <div id="unity-container" class="unity-desktop">
      <canvas id="unity-canvas" width=960 height=600 tabindex="-1"></canvas>
      <div id="unity-loading-bar">
        <div id="unity-logo"></div>
        <div id="unity-progress-bar-empty">
          <div id="unity-progress-bar-full"></div>
        </div>
      </div>
      <div id="unity-warning"> </div>
      <div id="unity-footer">
        <div id="unity-webgl-logo"></div>
        <div id="unity-fullscreen-button"></div>
        <div id="unity-build-title">Project Name</div>
      </div>
    </div>
    
    <script>
      // ... (유니티가 생성한 긴 자바스크립트 코드들) ...
    </script>
  </body>
</html>
