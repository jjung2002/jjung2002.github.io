<!DOCTYPE html>
<html lang="ko">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>정재윤 | Game Developer Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family:
                Pretendard,
                -apple-system,
                BlinkMacSystemFont,
                "Segoe UI",
                sans-serif;

            background: #0b1120;
            color: #f8fafc;
            line-height: 1.7;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .container {
            width: 90%;
            max-width: 1100px;
            margin: auto;
        }


        /* =========================
           NAVIGATION
        ========================== */

        nav {
            position: fixed;
            top: 0;
            left: 0;

            width: 100%;
            height: 70px;

            background: rgba(11, 17, 32, 0.9);
            backdrop-filter: blur(12px);

            border-bottom: 1px solid #1e293b;

            z-index: 1000;
        }

        .nav-inner {
            height: 100%;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 20px;
            font-weight: 800;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: #94a3b8;
            transition: 0.2s;
        }

        .nav-links a:hover {
            color: #38bdf8;
        }


        /* =========================
           HERO
        ========================== */

        .hero {
            min-height: 100vh;

            display: flex;
            flex-direction: column;
            justify-content: center;

            padding-top: 70px;
        }

        .hero-label {
            color: #38bdf8;

            font-size: 15px;
            font-weight: 700;

            letter-spacing: 2px;

            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: clamp(42px, 7vw, 78px);
            line-height: 1.15;

            max-width: 900px;

            margin-bottom: 30px;
        }

        .hero h1 span {
            color: #38bdf8;
        }

        .hero-description {
            max-width: 730px;

            color: #94a3b8;

            font-size: 18px;
        }

        .hero-buttons {
            margin-top: 35px;

            display: flex;
            gap: 15px;
        }

        .button {
            display: inline-block;

            padding: 13px 22px;

            border-radius: 8px;

            font-weight: 700;

            transition: 0.2s;
        }

        .button-primary {
            background: #38bdf8;
            color: #0f172a;
        }

        .button-primary:hover {
            background: #7dd3fc;
        }

        .button-outline {
            border: 1px solid #334155;
        }

        .button-outline:hover {
            border-color: #38bdf8;
        }


        /* =========================
           COMMON SECTION
        ========================== */

        section {
            padding: 110px 0;
        }

        .section-label {
            color: #38bdf8;

            font-size: 14px;
            font-weight: 700;

            letter-spacing: 2px;

            margin-bottom: 10px;
        }

        .section-title {
            font-size: 42px;
            margin-bottom: 50px;
        }


        /* =========================
           ABOUT
        ========================== */

        .about-content {
            max-width: 800px;

            color: #cbd5e1;

            font-size: 18px;
        }

        .about-content p + p {
            margin-top: 20px;
        }


        /* =========================
           PROJECT GRID
        ========================== */

        .project-grid {
            display: grid;

            grid-template-columns:
                repeat(2, minmax(0, 1fr));

            gap: 25px;
        }

        .project-card {
            position: relative;

            aspect-ratio: 1 / 1;

            overflow: hidden;

            border-radius: 18px;

            background: #1e293b;

            cursor: pointer;
        }

        .project-card img {
            width: 100%;
            height: 100%;

            object-fit: cover;

            transition:
                transform 0.5s,
                filter 0.5s;
        }

        .project-card:hover img {
            transform: scale(1.07);
        }

        .project-overlay {
            position: absolute;

            inset: 0;

            display: flex;
            flex-direction: column;
            justify-content: flex-end;

            padding: 30px;

            background:
                linear-gradient(
                    to top,
                    rgba(0, 0, 0, 0.92),
                    rgba(0, 0, 0, 0.1)
                );
        }

        .project-type {
            color: #38bdf8;

            font-size: 14px;
            font-weight: 700;
        }

        .project-overlay h3 {
            font-size: 30px;

            margin-top: 5px;
        }

        .project-overlay p {
            color: #cbd5e1;
        }


        /* =========================
           PROJECT DETAIL
        ========================== */

        .project-detail {
            border-top: 1px solid #1e293b;
        }

        .detail-header {
            display: flex;
            justify-content: space-between;
            gap: 30px;

            margin-bottom: 30px;
        }

        .detail-number {
            color: #38bdf8;
            font-weight: 700;
        }

        .detail-title {
            font-size: 38px;
        }

        .detail-subtitle {
            color: #94a3b8;

            font-size: 18px;
        }

        .detail-description {
            max-width: 800px;

            color: #cbd5e1;

            margin-bottom: 35px;
        }

        .detail-info {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 20px;

            margin-bottom: 30px;
        }

        .info-box {
            padding: 20px;

            background: #111827;

            border: 1px solid #1e293b;

            border-radius: 10px;
        }

        .info-box strong {
            color: #38bdf8;

            display: block;

            margin-bottom: 8px;
        }

        .project-buttons {
            display: flex;
            flex-wrap: wrap;

            gap: 10px;
        }


        /* =========================
           AI
        ========================== */

        .ai-box {
            padding: 45px;

            border-radius: 18px;

            background:
                linear-gradient(
                    135deg,
                    #111827,
                    #172554
                );

            border: 1px solid #1e3a5f;
        }

        .ai-box h3 {
            font-size: 30px;

            margin-bottom: 20px;
        }

        .ai-box p {
            color: #cbd5e1;

            max-width: 800px;
        }

        .ai-list {
            display: grid;

            grid-template-columns:
                repeat(2, 1fr);

            gap: 15px;

            margin-top: 30px;
        }

        .ai-item {
            background: rgba(255,255,255,0.04);

            padding: 18px;

            border-radius: 10px;
        }


        /* =========================
           SKILLS
        ========================== */

        .skill-list {
            display: flex;
            flex-wrap: wrap;

            gap: 12px;
        }

        .skill {
            padding: 10px 17px;

            border-radius: 100px;

            background: #111827;

            border: 1px solid #334155;

            color: #cbd5e1;
        }


        /* =========================
           FOOTER
        ========================== */

        footer {
            border-top: 1px solid #1e293b;

            padding: 50px 0;

            text-align: center;

            color: #64748b;
        }


        /* =========================
           MOBILE
        ========================== */

        @media (max-width: 750px) {

            .nav-links {
                display: none;
            }

            .project-grid {
                grid-template-columns: 1fr;
            }

            .detail-info {
                grid-template-columns: 1fr;
            }

            .ai-list {
                grid-template-columns: 1fr;
            }

            .detail-header {
                flex-direction: column;
            }
        }

    </style>
</head>


<body>


<!-- =========================
     NAV
========================== -->

<nav>

    <div class="container nav-inner">

        <a class="logo" href="#">
            JY.
        </a>

        <div class="nav-links">

            <a href="#about">About</a>

            <a href="#projects">Projects</a>

            <a href="#ai">AI & Development</a>

            <a href="#skills">Skills</a>

        </div>

    </div>

</nav>



<!-- =========================
     HERO
========================== -->

<header class="container hero">

    <div class="hero-label">
        GAME DEVELOPER PORTFOLIO
    </div>

    <h1>
        게임을 직접 만들고,<br>
        <span>AI와 함께</span>
        더 빠르게 성장하는 개발자
    </h1>

    <p class="hero-description">

        안녕하세요. 게임 개발자 정재윤입니다.

        Unity와 Unreal Engine을 활용해
        다양한 장르의 게임을 제작하며

        플레이어 시스템, 전투, 인벤토리,
        AI, UI, 레벨 디자인 등
        게임 플레이 전반을 구현해 왔습니다.

    </p>

    <div class="hero-buttons">

        <a
            class="button button-primary"
            href="#projects">

            프로젝트 보기

        </a>

        <a
            class="button button-outline"
            href="#ai">

            개발 방식

        </a>

    </div>

</header>



<main>


<!-- =========================
     ABOUT
========================== -->

<section id="about">

    <div class="container">

        <div class="section-label">
            ABOUT
        </div>

        <h2 class="section-title">
            About Me
        </h2>

        <div class="about-content">

            <p>
                동국대학교 멀티미디어소프트웨어공학 전공으로,
                게임 개발자를 목표로 다양한 프로젝트를
                직접 기획하고 구현해 왔습니다.
            </p>

            <p>
                단순히 기능을 구현하는 것에서 그치지 않고,
                플레이어가 실제로 어떤 경험을 하게 되는지를
                고민하며 게임 시스템과 레벨을 설계합니다.
            </p>

            <p>
                또한 생성형 AI를
                아이디어 탐색, 코드 분석,
                디버깅, 기술 학습,
                빠른 프로토타이핑에 활용하며
                새로운 개발 방식을 적극적으로 익히고 있습니다.
            </p>

        </div>

    </div>

</section>



<!-- =========================
     PROJECT GRID
========================== -->

<section id="projects">

    <div class="container">

        <div class="section-label">
            PROJECTS
        </div>

        <h2 class="section-title">
            Game Projects
        </h2>


        <div class="project-grid">


            <!-- RetroDash -->

            <a
                class="project-card"
                href="#retrodash">

                <img
                    src="images/retrodash.jpg"
                    alt="RetroDash">

                <div class="project-overlay">

                    <span class="project-type">
                        3인 팀 프로젝트
                    </span>

                    <h3>
                        RetroDash
                    </h3>

                    <p>
                        Rhythm Bullet Hell
                    </p>

                </div>

            </a>



            <!-- Shopping List -->

            <a
                class="project-card"
                href="#shoppinglist">

                <img
                    src="images/shoppinglist.jpg"
                    alt="Today's Shopping List">

                <div class="project-overlay">

                    <span class="project-type">
                        4인 팀 프로젝트
                    </span>

                    <h3>
                        Today's Shopping List
                    </h3>

                    <p>
                        First Person Horror
                    </p>

                </div>

            </a>



            <!-- T-Bot -->

            <a
                class="project-card"
                href="#tbot">

                <img
                    src="images/tbot.jpg"
                    alt="T-Bot">

                <div class="project-overlay">

                    <span class="project-type">
                        개인 프로젝트
                    </span>

                    <h3>
                        T-Bot
                    </h3>

                    <p>
                        FPS × Tower Defense
                    </p>

                </div>

            </a>



            <!-- Keepmove -->

            <a
                class="project-card"
                href="#keepmove">

                <img
                    src="images/keepmove.jpg"
                    alt="Keepmove">

                <div class="project-overlay">

                    <span class="project-type">
                        개인 프로젝트 · 2 Day Prototype
                    </span>

                    <h3>
                        Keepmove
                    </h3>

                    <p>
                        Survivors-like × Tower Defense
                    </p>

                </div>

            </a>


        </div>

    </div>

</section>



<!-- =========================
     RETRODASH
========================== -->

<section
    id="retrodash"
    class="project-detail">

    <div class="container">

        <div class="detail-header">

            <div>

                <div class="detail-number">
                    PROJECT 01
                </div>

                <h2 class="detail-title">
                    RetroDash
                </h2>

                <p class="detail-subtitle">
                    2D 리듬 탄막 회피 게임
                </p>

            </div>

        </div>


        <p class="detail-description">

            음악의 비트에 맞춰 다양한 장애물과
            공격 패턴이 등장하는 리듬 기반 회피 게임입니다.

            플레이어는 이동과 대시를 활용하여
            공격을 피하고 음악이 끝날 때까지
            생존해야 합니다.

        </p>


        <div class="detail-info">

            <div class="info-box">

                <strong>
                    Team
                </strong>

                3인 제작

            </div>


            <div class="info-box">

                <strong>
                    Role
                </strong>

                플레이어 · 아이템 · 맵 구성 ·
                애니메이션 배치 · 레벨 디자인

            </div>


            <div class="info-box">

                <strong>
                    Tech
                </strong>

                Unity · C#

            </div>

        </div>


        <div class="project-buttons">

            <a
                class="button button-primary"
                href="https://drive.google.com/file/d/1560znRkFTS2F37V-TcSqW4QyVaBG0k-8/view?usp=drive_link"
                target="_blank">

                게임 보기

            </a>

        </div>

    </div>

</section>



<!-- =========================
     SHOPPING LIST
========================== -->

<section
    id="shoppinglist"
    class="project-detail">

    <div class="container">

        <div class="detail-number">
            PROJECT 02
        </div>

        <h2 class="detail-title">
            Today's Shopping List
        </h2>

        <p class="detail-subtitle">
            3D 1인칭 공포 게임
        </p>


        <br>


        <p class="detail-description">

            나폴리탄 괴담을 기반으로 제작한
            1인칭 공포 게임입니다.

            대형 마트에서 진실과 거짓이
            동적으로 변하는 안전수칙을 해석하면서
            쇼핑 리스트에 있는 물건들을 수집합니다.

        </p>


        <div class="detail-info">

            <div class="info-box">

                <strong>
                    Team
                </strong>

                4인 제작

            </div>


            <div class="info-box">

                <strong>
                    Role
                </strong>

                플레이어 · 인벤토리 · 아이템 ·
                맵 구조 · 몬스터 · 기믹

            </div>


            <div class="info-box">

                <strong>
                    Tech
                </strong>

                Unreal Engine 5 ·
                C++ · Blueprint

            </div>

        </div>


        <div class="project-buttons">

            <a
                class="button button-primary"
                href="https://drive.google.com/file/d/16V-nXyjkaAxpwjUAmK5hyJ511gE2Eq_T/view?usp=drive_link"
                target="_blank">

                게임 보기

            </a>


            <a
                class="button button-outline"
                href="https://docs.google.com/presentation/d/1zKhrEZib4bScawb8hLI1ZOU2NQZLduu8/edit?usp=drive_link&ouid=102295740409891925672&rtpof=true&sd=true"
                target="_blank">

                프로젝트 PPT

            </a>

        </div>

    </div>

</section>



<!-- =========================
     T-BOT
========================== -->

<section
    id="tbot"
    class="project-detail">

    <div class="container">

        <div class="detail-number">
            PROJECT 03
        </div>

        <h2 class="detail-title">
            T-Bot
        </h2>

        <p class="detail-subtitle">
            FPS × Tower Defense
        </p>


        <br>


        <p class="detail-description">

            타워 디펜스의 전략적인 포탑 배치와
            FPS 방식의 직접 전투를 결합한
            개인 제작 게임입니다.

            웨이브 시작 전 포탑을 배치하고,
            전투가 시작되면 FPS 시점으로 전환하여
            플레이어가 직접 적과 싸웁니다.

        </p>


        <div class="detail-info">

            <div class="info-box">

                <strong>
                    Team
                </strong>

                개인 제작

            </div>


            <div class="info-box">

                <strong>
                    Role
                </strong>

                기획 · 시스템 · 전투 ·
                적 · UI · 레벨 구현

            </div>


            <div class="info-box">

                <strong>
                    Tech
                </strong>

                Unity · C#

            </div>

        </div>


        <div class="project-buttons">

            <a
                class="button button-primary"
                href="https://yoonyyun.itch.io/t-bot?secret=rKUlsPWSNJy8BAh52h0DFeOIU"
                target="_blank">

                itch.io

            </a>

        </div>

    </div>

</section>



<!-- =========================
     KEEPMOVE
========================== -->

<section
    id="keepmove"
    class="project-detail">

    <div class="container">

        <div class="detail-number">
            PROJECT 04
        </div>

        <h2 class="detail-title">
            Keepmove
        </h2>

        <p class="detail-subtitle">
            Survivors-like × Tower Defense
        </p>


        <br>


        <p class="detail-description">

            뱀서라이크 스타일의 전투와
            타워 디펜스 요소를 결합해 제작한
            Unity 개인 프로젝트입니다.

            제한된 시간 안에서
            아이디어를 실제 플레이 가능한 게임으로
            구현하는 것을 목표로
            2일 동안 개발한 프로토타입입니다.

        </p>


        <div class="detail-info">

            <div class="info-box">

                <strong>
                    Team
                </strong>

                개인 제작

            </div>


            <div class="info-box">

                <strong>
                    Development
                </strong>

                2 Days

            </div>


            <div class="info-box">

                <strong>
                    Tech
                </strong>

                Unity · C#

            </div>

        </div>


        <div class="project-buttons">

            <a
                class="button button-primary"
                href="https://drive.google.com/file/d/1l2K6rDjb6jW5CVa8MG-XB_c-m5D4GFho/view?usp=drive_link"
                target="_blank">

                게임 보기

            </a>


            <a
                class="button button-outline"
                href="https://drive.google.com/file/d/1LFKtwrAdAXq8AY13b8G6LTfKEV1jhnmT/view?usp=drive_link"
                target="_blank">

                플레이 영상

            </a>

        </div>

    </div>

</section>



<!-- =========================
     AI
========================== -->

<section id="ai">

    <div class="container">

        <div class="section-label">
            DEVELOPMENT
        </div>

        <h2 class="section-title">
            AI-Assisted Development
        </h2>


        <div class="ai-box">

            <h3>
                AI를 사용해 코드를 만드는 것보다,<br>
                AI와 함께 문제를 해결합니다.
            </h3>


            <p>

                생성형 AI를 새로운 기술을 탐색하고
                문제를 분석하는 개발 보조 도구로 활용합니다.

                AI가 제안한 결과를 그대로 적용하지 않고,
                코드의 동작 원리를 확인한 뒤
                프로젝트에 맞게 수정하고 검증하는 것을
                중요하게 생각합니다.

            </p>


            <div class="ai-list">

                <div class="ai-item">
                    게임 시스템 아이디어 탐색
                </div>

                <div class="ai-item">
                    C# / C++ 코드 분석
                </div>

                <div class="ai-item">
                    디버깅 및 오류 원인 탐색
                </div>

                <div class="ai-item">
                    빠른 프로토타이핑
                </div>

                <div class="ai-item">
                    새로운 기술 학습
                </div>

                <div class="ai-item">
                    게임 로직 개선안 탐색
                </div>

            </div>

        </div>

    </div>

</section>



<!-- =========================
     SKILLS
========================== -->

<section id="skills">

    <div class="container">

        <div class="section-label">
            SKILLS
        </div>

        <h2 class="section-title">
            Tech Stack
        </h2>


        <div class="skill-list">

            <span class="skill">
                Unity
            </span>

            <span class="skill">
                Unreal Engine 5
            </span>

            <span class="skill">
                C#
            </span>

            <span class="skill">
                C++
            </span>

            <span class="skill">
                Blueprint
            </span>

            <span class="skill">
                Python
            </span>

            <span class="skill">
                Game AI
            </span>

            <span class="skill">
                Level Design
            </span>

            <span class="skill">
                UI / UX
            </span>

            <span class="skill">
                GitHub
            </span>

        </div>

    </div>

</section>


</main>



<footer>

    © 2026 Jae-Yun Jeong
    · Game Developer Portfolio

</footer>


</body>

</html>
