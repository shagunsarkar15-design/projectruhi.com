<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>रूhī — Giving every child a chance to dream</title>

    <meta
        name="description"
        content="रूhī is working to give every child a chance to learn, grow, dream and make mistakes."
    >

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link
        href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,500;1,600&display=swap"
        rel="stylesheet"
    >

    <style>

        /* =====================================================
           R U H I — GLOBAL DESIGN
        ===================================================== */

        :root {
            --cream: #fff8ec;
            --vanilla: #f8e8bd;
            --soft-pink: #f5b3b9;
            --pink: #dc617c;
            --raspberry: #b92f55;
            --lemon: #f5c84c;
            --lime: #b9bb4a;
            --sage: #9da77b;
            --earth: #39271f;
            --earth-soft: #634b3f;
            --white: #fffdf8;

            --serif: "Playfair Display", Georgia, serif;
            --sans: "DM Sans", Arial, sans-serif;

            --radius: 28px;
            --max-width: 1180px;
        }


        /* =====================================================
           RESET
        ===================================================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: var(--cream);
            color: var(--earth);
            font-family: var(--sans);
            line-height: 1.7;
            overflow-x: hidden;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        button {
            font: inherit;
        }


        /* =====================================================
           ETHNIC DECORATIVE PATTERN
        ===================================================== */

        .pattern-line {
            width: 100%;
            height: 26px;
            margin: 20px 0;

            background-image:
                radial-gradient(
                    circle at center,
                    transparent 5px,
                    var(--raspberry) 6px,
                    var(--raspberry) 7px,
                    transparent 8px
                );

            background-size: 32px 18px;
            opacity: 0.45;
        }

        .pattern-line::after {
            content: "✦  ❋  ✦  ❋  ✦  ❋  ✦";
            display: block;
            text-align: center;
            font-size: 13px;
            letter-spacing: 8px;
            color: var(--earth-soft);
            transform: translateY(-2px);
        }


        /* =====================================================
           NAVIGATION
        ===================================================== */

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;

            padding: 20px 5%;

            background: rgba(255, 248, 236, 0.78);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);

            border-bottom: 1px solid rgba(57, 39, 31, 0.08);
        }

        .nav-inner {
            max-width: var(--max-width);
            margin: auto;

            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
        }

        .logo {
            font-family: var(--serif);
            font-size: 30px;
            font-weight: 600;
            letter-spacing: -1px;
        }

        .logo span {
            color: var(--raspberry);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 30px;
        }

        .nav-links a {
            font-size: 14px;
            font-weight: 600;
            position: relative;
        }

        .nav-links a::after {
            content: "";
            position: absolute;
            left: 0;
            bottom: -6px;
            width: 0;
            height: 2px;
            background: var(--pink);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-cta {
            padding: 12px 20px;
            border-radius: 999px;

            background: var(--pink);
            color: white !important;

            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .nav-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(185, 47, 85, 0.2);
        }


        /* =====================================================
           HERO
        ===================================================== */

        .hero {
            min-height: 100vh;
            padding: 150px 5% 90px;

            display: flex;
            align-items: center;

            background:
                radial-gradient(
                    circle at 15% 15%,
                    rgba(245, 200, 76, 0.55),
                    transparent 32%
                ),

                radial-gradient(
                    circle at 85% 25%,
                    rgba(245, 179, 185, 0.7),
                    transparent 38%
                ),

                radial-gradient(
                    circle at 60% 90%,
                    rgba(185, 187, 74, 0.18),
                    transparent 32%
                ),

                var(--cream);
        }

        .hero-inner {
            width: 100%;
            max-width: var(--max-width);
            margin: auto;

            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 70px;
            align-items: center;
        }

        .eyebrow {
            display: inline-flex;
            align-items: center;
            gap: 10px;

            margin-bottom: 24px;

            font-size: 13px;
            font-weight: 700;
            letter-spacing: 3px;
            text-transform: uppercase;

            color: var(--raspberry);
        }

        .eyebrow::before {
            content: "";
            width: 38px;
            height: 2px;
            background: var(--raspberry);
        }

        .hero h1 {
            font-family: var(--serif);
            font-size: clamp(52px, 7vw, 92px);
            line-height: 0.98;
            letter-spacing: -4px;
            max-width: 800px;
        }

        .hero h1 em {
            color: var(--raspberry);
            font-weight: 500;
        }

        .hero-intro {
            margin-top: 30px;
            max-width: 680px;

            font-size: 19px;
            line-height: 1.8;
            color: var(--earth-soft);
        }

        .hero-tagline {
            margin-top: 24px;

            font-family: var(--serif);
            font-style: italic;
            font-size: 22px;
        }

        .hero-buttons {
            margin-top: 38px;

            display: flex;
            flex-wrap: wrap;
            gap: 14px;
        }

        .button {
            display: inline-flex;
            align-items: center;
            justify-content: center;

            padding: 15px 25px;

            border-radius: 999px;

            font-weight: 700;
            font-size: 14px;

            transition:
                transform 0.3s ease,
                box-shadow 0.3s ease,
                background 0.3s ease;
        }

        .button-primary {
            background: var(--pink);
            color: white;

            box-shadow: 0 12px 25px rgba(220, 97, 124, 0.18);
        }

        .button-secondary {
            border: 1px solid var(--earth);
            background: transparent;
        }

        .button:hover {
            transform: translateY(-3px);
        }

        .button-primary:hover {
            box-shadow: 0 18px 35px rgba(220, 97, 124, 0.25);
        }


        /* =====================================================
           HERO ART
        ===================================================== */

        .hero-art {
            position: relative;
            min-height: 480px;

            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero-circle {
            width: 390px;
            height: 390px;

            border-radius: 50%;

            background:
                radial-gradient(
                    circle at 35% 25%,
                    #fff3b6,
                    transparent 30%
                ),

                linear-gradient(
                    145deg,
                    var(--lemon),
                    var(--soft-pink),
                    var(--pink)
                );

            position: relative;

            box-shadow:
                0 35px 70px rgba(57, 39, 31, 0.13);
        }

        .hero-circle::before {
            content: "";
            position: absolute;

            inset: 35px;

            border: 2px dashed rgba(57, 39, 31, 0.35);
            border-radius: 50%;
        }

        .hero-message {
            position: absolute;

            width: 245px;
            padding: 25px;

            bottom: 20px;
            left: 0;

            background: rgba(255, 253, 248, 0.93);

            border-radius: 24px;

            box-shadow:
                0 20px 45px rgba(57, 39, 31, 0.13);

            transform: rotate(-3deg);
        }

        .hero-message strong {
            display: block;

            font-family: var(--serif);
            font-size: 35px;

            color: var(--raspberry);
        }

        .hero-message p {
            margin-top: 7px;

            font-size: 14px;
            line-height: 1.5;
        }

        .hero-sun {
            position: absolute;

            width: 115px;
            height: 115px;

            top: 15px;
            right: 15px;

            border-radius: 50%;

            background:
                repeating-radial-gradient(
                    circle,
                    rgba(57, 39, 31, 0.3) 0 2px,
                    transparent 3px 14px
                );

            opacity: 0.5;
        }


        /* =====================================================
           GENERAL SECTION
        ===================================================== */

        section {
            padding: 110px 5%;
        }

        .section-inner {
            max-width: var(--max-width);
            margin: auto;
        }

        .section-label {
            display: flex;
            align-items: center;
            gap: 12px;

            color: var(--raspberry);

            font-size: 13px;
            font-weight: 700;
            letter-spacing: 3px;
            text-transform: uppercase;

            margin-bottom: 20px;
        }

        .section-label::before {
            content: "";
            width: 35px;
            height: 2px;
            background: var(--raspberry);
        }

        .section-title {
            font-family: var(--serif);

            font-size: clamp(40px, 5vw, 67px);
            line-height: 1.05;

            letter-spacing: -2px;
        }

        .section-title em {
            font-weight: 500;
        }

        .section-text {
            margin-top: 22px;

            max-width: 700px;

            color: var(--earth-soft);
            font-size: 17px;
            line-height: 1.85;
        }


        /* =====================================================
           INTRO
        ===================================================== */

        .intro {
            background:
                linear-gradient(
                    120deg,
                    #fffaf0,
                    #fff3dc,
                    #fff8ec
                );
        }

        .intro-grid {
            display: grid;

            grid-template-columns: 1fr 0.8fr;

            gap: 80px;
            align-items: center;
        }

        .intro-card {
            padding: 45px;

            border-radius: var(--radius);

            background:
                linear-gradient(
                    145deg,
                    rgba(245, 200, 76, 0.55),
                    rgba(245, 179, 185, 0.65)
                );

            border: 1px solid rgba(57, 39, 31, 0.08);

            box-shadow:
                0 25px 60px rgba(57, 39, 31, 0.08);
        }

        .intro-card p {
            font-family: var(--serif);
            font-size: 28px;
            line-height: 1.45;
        }


        /* =====================================================
           INDIA SECTION
        ===================================================== */

        .world {
            background:
                radial-gradient(
                    circle at 85% 15%,
                    rgba(185, 187, 74, 0.2),
                    transparent 25%
                ),

                radial-gradient(
                    circle at 10% 80%,
                    rgba(220, 97, 124, 0.15),
                    transparent 25%
                ),

                var(--cream);
        }

        .world-heading {
            max-width: 800px;
        }

        .map-wrapper {
            margin-top: 70px;

            display: grid;
            grid-template-columns: 1fr 0.75fr;

            gap: 50px;
            align-items: center;
        }

        .map-card {
            min-height: 560px;

            position: relative;

            display: flex;
            align-items: center;
            justify-content: center;

            overflow: hidden;

            border-radius: 40px;

            background:
                linear-gradient(
                    145deg,
                    #f7df9c,
                    #f5b3b9,
                    #e77991
                );

            border: 1px solid rgba(57, 39, 31, 0.08);
        }

        /*
           Stylised India silhouette placeholder.
           We intentionally keep this as a decorative shape
           until real project locations are added.
        */

        .india-shape {
            width: 300px;
            height: 390px;

            position: relative;

            background:
                linear-gradient(
                    150deg,
                    #b9bb4a,
                    #9da77b
                );

            clip-path: polygon(
                45% 0%,
                65% 8%,
                80% 20%,
                76% 35%,
                92% 48%,
                78% 62%,
                72% 80%,
                55% 100%,
                42% 83%,
                35% 68%,
                22% 55%,
                28% 40%,
                14% 27%,
                30% 15%
            );

            filter: drop-shadow(
                15px 20px 18px rgba(57, 39, 31, 0.15)
            );
        }

        .map-dot {
            position: absolute;

            width: 17px;
            height: 17px;

            border-radius: 50%;

            background: var(--raspberry);

            border: 3px solid var(--cream);

            box-shadow:
                0 5px 15px rgba(185, 47, 85, 0.35);

            cursor: pointer;

            transition: transform 0.25s ease;
        }

        .map-dot:hover {
            transform: scale(1.5);
        }

        .dot-delhi {
            top: 22%;
            left: 55%;
        }

        .dot-jaipur {
            top: 31%;
            left: 40%;
        }

        .dot-mumbai {
            top: 58%;
            left: 38%;
        }

        .dot-kolkata {
            top: 46%;
            left: 69%;
        }

        .dot-bengaluru {
            top: 74%;
            left: 49%;
        }

        .dot-chennai {
            top: 76%;
            left: 61%;
        }

        .map-caption {
            position: absolute;

            bottom: 25px;
            left: 30px;
            right: 30px;

            padding: 15px 20px;

            background: rgba(255, 253, 248, 0.86);

            border-radius: 18px;

            font-size: 13px;
            text-align: center;
        }

        .issue-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .issue {
            padding: 25px;

            border: 1px solid rgba(57, 39, 31, 0.13);
            border-radius: 22px;

            background: rgba(255, 253, 248, 0.7);

            transition:
                transform 0.3s ease,
                background 0.3s ease;
        }

        .issue:hover {
            transform: translateX(8px);

            background: #fffdf8;
        }

        .issue-number {
            color: var(--raspberry);

            font-size: 12px;
            font-weight: 700;
            letter-spacing: 2px;
        }

        .issue h3 {
            margin-top: 6px;

            font-family: var(--serif);
            font-size: 24px;
        }

        .issue p {
            margin-top: 7px;

            font-size: 14px;
            color: var(--earth-soft);
        }


        /* =====================================================
           APPROACH
        ===================================================== */

        .approach {
            background:
                linear-gradient(
                    125deg,
                    #f8e8bd,
                    #f5d6c9,
                    #e8e4bb
                );
        }

        .approach-grid {
            margin-top: 55px;

            display: grid;
            grid-template-columns: repeat(3, 1fr);

            gap: 20px;
        }

        .approach-card {
            min-height: 310px;

            padding: 35px;

            border-radius: var(--radius);

            background: rgba(255, 253, 248, 0.65);

            border: 1px solid rgba(57, 39, 31, 0.1);

            transition:
                transform 0.35s ease,
                box-shadow 0.35s ease;
        }

        .approach-card:hover {
            transform: translateY(-8px);

            box-shadow:
                0 25px 45px rgba(57, 39, 31, 0.1);
        }

        .approach-number {
            font-family: var(--serif);
            font-size: 52px;
            color: var(--raspberry);
        }

        .approach-card h3 {
            margin-top: 15px;

            font-family: var(--serif);
            font-size: 28px;
        }

        .approach-card p {
            margin-top: 12px;

            font-size: 15px;
            color: var(--earth-soft);
        }


        /* =====================================================
           PROJECTS
        ===================================================== */

        .projects {
            background: #fffaf1;
        }

        .projects-header {
            display: flex;
            align-items: end;
            justify-content: space-between;
            gap: 30px;
        }

        .project-grid {
            margin-top: 55px;

            display: grid;
            grid-template-columns: repeat(2, 1fr);

            gap: 25px;
        }

        .project-card {
            overflow: hidden;

            border-radius: 30px;

            background: white;

            border: 1px solid rgba(57, 39, 31, 0.1);

            transition:
                transform 0.35s ease,
                box-shadow 0.35s ease;
        }

        .project-card:hover {
            transform: translateY(-7px);

            box-shadow:
                0 25px 55px rgba(57, 39, 31, 0.12);
        }

        .project-image {
            height: 300px;

            display: flex;
            align-items: center;
            justify-content: center;

            background:
                linear-gradient(
                    135deg,
                    var(--vanilla),
                    var(--soft-pink)
                );

            font-family: var(--serif);
            font-size: 26px;

            color: var(--earth-soft);
        }

        .project-card:nth-child(2) .project-image {
            background:
                linear-gradient(
                    135deg,
                    #d9dfac,
                    #f3c2c3
                );
        }

        .project-content {
            padding: 30px;
        }

        .project-number {
            font-size: 12px;
            font-weight: 700;
            letter-spacing: 2px;
            color: var(--raspberry);
        }

        .project-content h3 {
            margin-top: 8px;

            font-family: var(--serif);
            font-size: 31px;
        }

        .project-content p {
            margin-top: 10px;

            font-size: 15px;
            color: var(--earth-soft);
        }

        .project-link {
            display: inline-block;

            margin-top: 20px;

            font-size: 13px;
            font-weight: 700;

            color: var(--raspberry);
        }


        /* =====================================================
           STORY
        ===================================================== */

        .story {
            background:
                radial-gradient(
                    circle at 20% 20%,
                    rgba(245, 200, 76, 0.22),
                    transparent 28%
                ),

                radial-gradient(
                    circle at 80% 80%,
                    rgba(220, 97, 124, 0.2),
                    transparent 30%
                ),

                var(--cream);
        }

        .story-grid {
            display: grid;

            grid-template-columns: 0.8fr 1fr;

            gap: 80px;
            align-items: center;
        }

        .story-art {
            min-height: 500px;

            border-radius: 40px;

            background:
                linear-gradient(
                    145deg,
                    #f4d77f,
                    #d7a5a9,
                    #9da77b
                );

            position: relative;

            overflow: hidden;
        }

        .story-art::before {
            content: "रूhī";

            position: absolute;

            top: 50%;
            left: 50%;

            transform:
                translate(-50%, -50%)
                rotate(-7deg);

            font-family: var(--serif);

            font-size: 100px;
            font-weight: 600;

            color: rgba(255, 253, 248, 0.8);
        }

        .story-text p {
            margin-top: 22px;

            color: var(--earth-soft);

            font-size: 17px;
            line-height: 1.9;
        }


        /* =====================================================
           FINAL CTA
        ===================================================== */

        .final-cta {
            padding: 120px 5%;

            text-align: center;

            background:
                linear-gradient(
                    135deg,
                    #dc617c,
                    #c84b68,
                    #aeb45c
                );

            color: white;
        }

        .final-cta h2 {
            max-width: 800px;

            margin: auto;

            font-family: var(--serif);

            font-size: clamp(45px, 6vw, 76px);

            line-height: 1.05;
        }

        .final-cta p {
            margin-top: 20px;

            font-size: 17px;
            opacity: 0.9;
        }

        .final-cta .button {
            margin-top: 30px;

            background: var(--cream);
            color: var(--earth);
        }


        /* =====================================================
           FOOTER
        ===================================================== */

        footer {
            padding: 60px 5% 30px;

            background: var(--earth);
            color: #fff4df;
        }

        .footer-inner {
            max-width: var(--max-width);
            margin: auto;

            display: flex;
            justify-content: space-between;
            align-items: start;

            gap: 40px;
        }

        .footer-logo {
            font-family: var(--serif);
            font-size: 40px;
        }

        .footer-tagline {
            margin-top: 10px;

            color: #d8c4b7;
            font-size: 14px;
        }

        .footer-links {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }

        .footer-links a {
            font-size: 14px;
            color: #f8e8d8;
        }

        .footer-bottom {
            max-width: var(--max-width);

            margin: 50px auto 0;
            padding-top: 20px;

            border-top: 1px solid rgba(255,255,255,0.15);

            font-size: 12px;
            color: #cdb8aa;
        }


        /* =====================================================
           SCROLL ANIMATION
        ===================================================== */

        .reveal {
            opacity: 0;
            transform: translateY(35px);

            transition:
                opacity 0.8s ease,
                transform 0.8s ease;
        }

        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }


        /* =====================================================
           MOBILE
        ===================================================== */

        @media (max-width: 900px) {

            .nav-links {
                display: none;
            }

            .hero-inner,
            .intro-grid,
            .map-wrapper,
            .story-grid {
                grid-template-columns: 1fr;
            }

            .hero {
                padding-top: 130px;
            }

            .hero-art {
                min-height: 420px;
            }

            .hero-circle {
                width: 320px;
                height: 320px;
            }

            .approach-grid {
                grid-template-columns: 1fr;
            }

            .project-grid {
                grid-template-columns: 1fr;
            }

            .projects-header {
                align-items: start;
                flex-direction: column;
            }

            .footer-inner {
                flex-direction: column;
            }
        }


        @media (max-width: 600px) {

            section {
                padding: 80px 6%;
            }

            .hero {
                padding-left: 6%;
                padding-right: 6%;
            }

            .hero h1 {
                font-size: 54px;
                letter-spacing: -2px;
            }

            .hero-intro {
                font-size: 16px;
            }

            .hero-art {
                min-height: 350px;
            }

            .hero-circle {
                width: 280px;
                height: 280px;
            }

            .hero-message {
                width: 210px;
                left: 0;
            }

            .map-card {
                min-height: 450px;
            }

            .india-shape {
                width: 230px;
                height: 310px;
            }

            .intro-card {
                padding: 30px;
            }

            .intro-card p {
                font-size: 23px;
            }

            .project-image {
                height: 230px;
            }

            .final-cta {
                padding: 90px 6%;
            }

        }

    </style>
</head>


<body>


    <!-- =====================================================
         NAVIGATION
    ====================================================== -->

    <nav>

        <div class="nav-inner">

            <a href="#home" class="logo">
                रू<span>hī</span>
            </a>

            <div class="nav-links">

                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#world">Our Work</a>
                <a href="#projects">Projects</a>
                <a href="#story">Our Story</a>

                <a href="#get-involved" class="nav-cta">
                    Get Involved
                </a>

            </div>

        </div>

    </nav>



    <!-- =====================================================
         HERO
    ====================================================== -->

    <main>

        <section class="hero" id="home">

            <div class="hero-inner">

                <div class="hero-content reveal">

                    <div class="eyebrow">
                        A little space to dream
                    </div>

                    <h1>
                        Come along,<br>
                        to <em>learn,</em><br>
                        grow & dream.
                    </h1>

                    <p class="hero-intro">
                        रूhī works towards creating spaces where
                        underprivileged children can learn, explore,
                        understand the world around them and imagine
                        something bigger for themselves.
                    </p>

                    <p class="hero-tagline">
                        Giving every child a chance to dream.
                    </p>

                    <div class="hero-buttons">

                        <a href="#story" class="button button-primary">
                            Our Story
                        </a>

                        <a href="#get-involved" class="button button-secondary">
                            Get Involved
                        </a>

                    </div>

                </div>


                <div class="hero-art reveal">

                    <div class="hero-circle">

                        <div class="hero-sun"></div>

                    </div>

                    <div class="hero-message">

                        <strong>learn.</strong>

                        <p>
                            To ask questions.
                            To make mistakes.
                            To try again.
                        </p>

                    </div>

                </div>

            </div>

        </section>



        <div class="pattern-line"></div>



        <!-- =====================================================
             ABOUT / INTRO
        ====================================================== -->

        <section class="intro" id="about">

            <div class="section-inner intro-grid">

                <div class="reveal">

                    <div class="section-label">
                        A little about us
                    </div>

                    <h2 class="section-title">
                        We believe childhood
                        should leave room
                        for <em>curiosity.</em>
                    </h2>

                    <p class="section-text">
                        रूhī is a youth-led initiative working towards
                        the welfare of underprivileged children.
                        Our focus is simple: create opportunities for
                        children to build basic literacy, understand
                        the world around them and feel empowered to
                        imagine a future of their own.
                    </p>

                    <div class="hero-buttons">

                        <a href="#story" class="button button-primary">
                            Read Our Story
                        </a>

                    </div>

                </div>


                <div class="intro-card reveal">

                    <p>
                        "Maybe we don't have to know exactly
                        where we're going. Maybe we can just
                        start by walking together."
                    </p>

                    <div class="pattern-line"></div>

                    <span>
                        — रूhī
                    </span>

                </div>

            </div>

        </section>



        <!-- =====================================================
             THE WORLD WE SEE
        ====================================================== -->

        <section class="world" id="world">

            <div class="section-inner">

                <div class="world-heading reveal">

                    <div class="section-label">
                        The world we see
                    </div>

                    <h2 class="section-title">
                        Every place tells
                        a different <em>story.</em>
                    </h2>

                    <p class="section-text">
                        Children's lives are shaped by where they
                        grow up, what opportunities surround them,
                        and whether someone is there to listen.
                        As रूhī grows, we want to understand these
                        stories — not just from numbers, but from
                        people and communities themselves.
                    </p>

                </div>


                <div class="map-wrapper">

                    <!-- Stylised map -->

                    <div class="map-card reveal">

                        <div class="india-shape">

                            <div class="map-dot dot-delhi"
                                 title="Delhi"></div>

                            <div class="map-dot dot-jaipur"
                                 title="Jaipur"></div>

                            <div class="map-dot dot-mumbai"
                                 title="Mumbai"></div>

                            <div class="map-dot dot-kolkata"
                                 title="Kolkata"></div>

                            <div class="map-dot dot-bengaluru"
                                 title="Bengaluru"></div>

                            <div class="map-dot dot-chennai"
                                 title="Chennai"></div>

                        </div>


                        <div class="map-caption">

                            A growing map of the places,
                            communities and stories we hope
                            to learn from.

                        </div>

                    </div>


                    <!-- Issues -->

                    <div class="issue-list reveal">

                        <div class="issue">

                            <div class="issue-number">
                                01 — LEARNING
                            </div>

                            <h3>
                                Access to basic literacy
                            </h3>

                            <p>
                                Every child deserves the chance
                                to read, understand and express
                                themselves.
                            </p>

                        </div>


                        <div class="issue">

                            <div class="issue-number">
                                02 — AWARENESS
                            </div>

                            <h3>
                                Understanding the world
                            </h3>

                            <p>
                                Social knowledge helps children
                                understand their rights, communities
                                and the world around them.
                            </p>

                        </div>


                        <div class="issue">

                            <div class="issue-number">
                                03 — OPPORTUNITY
                            </div>

                            <h3>
                                Room to imagine
                            </h3>

                            <p>
                                Empowerment begins when a child
                                feels that their ideas and dreams
                                matter.
                            </p>

                        </div>


                        <div class="issue">

                            <div class="issue-number">
                                04 — DIGNITY
                            </div>

                            <h3>
                                Being seen and heard
                            </h3>

                            <p>
                                We believe welfare should never
                                take away a child's voice or dignity.
                            </p>

                        </div>

                    </div>

                </div>

            </div>

        </section>



        <!-- =====================================================
             APPROACH
        ====================================================== -->

        <section class="approach" id="approach">

            <div class="section-inner">

                <div class="reveal">

                    <div class="section-label">
                        Our approach
                    </div>

                    <h2 class="section-title">
                        Learn. Grow.
                        <em>Keep going.</em>
                    </h2>

                    <p class="section-text">
                        This section is intentionally simple so
                        you can edit the three cards later as
                        रूhī's approach develops.
                    </p>

                </div>


                <div class="approach-grid">

                    <div class="approach-card reveal">

                        <div class="approach-number">
                            01
                        </div>

                        <h3>
                            Learn
                        </h3>

                        <p>
                            Add your approach, philosophy or
                            educational model here.
                        </p>

                    </div>


                    <div class="approach-card reveal">

                        <div class="approach-number">
                            02
                        </div>

                        <h3>
                            Grow
                        </h3>

                        <p>
                            Add your second principle here.
                        </p>

                    </div>


                    <div class="approach-card reveal">

                        <div class="approach-number">
                            03
                        </div>

                        <h3>
                            Empower
                        </h3>

                        <p>
                            Add your third principle here.
                        </p>

                    </div>

                </div>

            </div>

        </section>



        <!-- =====================================================
             PROJECTS
        ====================================================== -->

        <section class="projects" id="projects">

            <div class="section-inner">

                <div class="projects-header reveal">

                    <div>

                        <div class="section-label">
                            What we've done
                        </div>

                        <h2 class="section-title">
                            Little projects,
                            <em>real moments.</em>
                        </h2>

                    </div>

                </div>


                <div class="project-grid">

                    <!-- PROJECT 01 -->

                    <article class="project-card reveal">

                        <div class="project-image">

                            PROJECT 01

                        </div>

                        <div class="project-content">

                            <div class="project-number">
                                PROJECT 01
                            </div>

                            <h3>
                                Project Name
                            </h3>

                            <p>
                                A short description of what
                                happened during the project.
                                This will eventually connect
                                to the full project story and
                                gallery.
                            </p>

                            <a href="#" class="project-link">
                                VIEW PROJECT →
                            </a>

                        </div>

                    </article>


                    <!-- PROJECT 02 -->

                    <article class="project-card reveal">

                        <div class="project-image">

                            PROJECT 02

                        </div>

                        <div class="project-content">

                            <div class="project-number">
                                PROJECT 02
                            </div>

                            <h3>
                                Project Name
                            </h3>

                            <p>
                                A short description of your
                                second project can go here.
                            </p>

                            <a href="#" class="project-link">
                                VIEW PROJECT →
                            </a>

                        </div>

                    </article>

                </div>

            </div>

        </section>



        <!-- =====================================================
             OUR STORY
        ====================================================== -->

        <section class="story" id="story">

            <div class="section-inner story-grid">

                <div class="story-art reveal">
                </div>


                <div class="story-text reveal">

                    <div class="section-label">
                        Our story
                    </div>

                    <h2 class="section-title">
                        Why <em>रूhī</em> exists.
                    </h2>

                    <p>
                        रूhī began with a simple belief:
                        that a child's circumstances should not
                        decide how far their dreams are allowed
                        to go.
                    </p>

                    <p>
                        We are a youth-led initiative trying to
                        learn, listen and act — beginning with
                        basic literacy and social awareness,
                        and slowly building spaces where children
                        can discover their own voices.
                    </p>

                    <p>
                        This is only the beginning.
                    </p>

                    <div class="hero-buttons">

                        <a href="#get-involved"
                           class="button button-primary">

                            Come Along

                        </a>

                    </div>

                </div>

            </div>

        </section>



        <!-- =====================================================
             FINAL CTA
        ====================================================== -->

        <section class="final-cta" id="get-involved">

            <div class="reveal">

                <h2>
                    Giving every child
                    a chance to dream.
                </h2>

                <p>
                    Come along. Learn. Grow. Make mistakes.
                    Make something meaningful.
                </p>

                <a href="#home" class="button">
                    Back to the beginning ↑
                </a>

            </div>

        </section>

    </main>



    <!-- =====================================================
         FOOTER
    ====================================================== -->

    <footer>

        <div class="footer-inner">

            <div>

                <div class="footer-logo">
                    रूhī
                </div>

                <div class="footer-tagline">
                    Giving every child a chance to dream.
                </div>

            </div>


            <div class="footer-links">

                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#projects">Projects</a>
                <a href="#story">Our Story</a>
                <a href="#get-involved">Get Involved</a>

            </div>

        </div>


        <div class="footer-bottom">

            © 2026 रूhī. Built with hope, curiosity and a
            willingness to make mistakes.

        </div>

    </footer>



    <!-- =====================================================
         JAVASCRIPT
    ====================================================== -->

    <script>

        /*
         * Simple reveal animation.
         * Sections fade upward as you scroll.
         */

        const revealElements =
            document.querySelectorAll(".reveal");

        const observer =
            new IntersectionObserver(

                (entries) => {

                    entries.forEach((entry) => {

                        if (entry.isIntersecting) {

                            entry.target.classList.add("visible");

                        }

                    });

                },

                {
                    threshold: 0.12
                }

            );


        revealElements.forEach((element) => {

            observer.observe(element);

        });


        /*
         * Small interaction for map locations.
         */

        const mapDots =
            document.querySelectorAll(".map-dot");

        mapDots.forEach((dot) => {

            dot.addEventListener("click", () => {

                const city =
                    dot.getAttribute("title");

                alert(
                    city +
                    " — project information coming soon."
                );

            });

        });

    </script>

</body>
</html>
