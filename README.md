<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Bilal Faisal Arain · GitHub Profile</title>
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <style>
        /* ── Reset & Base ── */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;
            font-family: 'Segoe UI', 'Inter', system-ui, -apple-system, sans-serif;
            display: flex;
            justify-content: center;
            padding: 2rem 1rem;
            color: #e6edf3;
            line-height: 1.6;
        }

        .card {
            max-width: 900px;
            width: 100%;
            background: #161b22;
            border-radius: 32px;
            padding: 2.5rem 2.8rem;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8);
            border: 1px solid #30363d;
            transition: all 0.2s ease;
        }

        /* ── Typography ── */
        h1,
        h2,
        h3 {
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        h1 {
            font-size: 2.4rem;
            background: linear-gradient(135deg, #f0f6fc 0%, #58a6ff 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: inline-block;
        }

        h2 {
            font-size: 1.2rem;
            color: #8b949e;
            font-weight: 400;
            margin-top: 0.2rem;
        }

        h3 {
            font-size: 1.1rem;
            color: #f0f6fc;
            margin-bottom: 0.75rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        h3 i {
            color: #58a6ff;
            font-size: 1.1rem;
            width: 1.6rem;
            text-align: center;
        }

        /* ── Divider ── */
        .divider {
            border: 0;
            height: 1px;
            background: linear-gradient(90deg, #30363d, #58a6ff55, #30363d);
            margin: 1.8rem 0;
        }

        /* ── Header Section ── */
        .header-wrap {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 1.5rem;
        }

        .avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: linear-gradient(135deg, #238636, #2ea043);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.8rem;
            font-weight: 700;
            color: #0d1117;
            box-shadow: 0 0 0 3px #30363d, 0 0 0 6px #161b22;
            flex-shrink: 0;
            user-select: none;
        }

        .badge-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin-top: 0.6rem;
        }

        .badge-row a {
            text-decoration: none;
        }

        /* ── Badge style (shields.io look) ── */
        .badge {
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            background: #21262d;
            color: #c9d1d9;
            padding: 0.3rem 0.9rem;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 500;
            border: 1px solid #30363d;
            transition: 0.15s;
            text-decoration: none;
        }

        .badge i {
            font-size: 0.8rem;
            color: #58a6ff;
        }

        .badge:hover {
            background: #30363d;
            border-color: #58a6ff;
            transform: translateY(-1px);
        }

        .badge-blue {
            background: #1f6feb33;
            border-color: #1f6feb55;
            color: #58a6ff;
        }
        .badge-green {
            background: #23863633;
            border-color: #23863655;
            color: #3fb950;
        }
        .badge-purple {
            background: #8957e533;
            border-color: #8957e555;
            color: #d2a8ff;
        }
        .badge-orange {
            background: #d2992233;
            border-color: #d2992255;
            color: #e3b341;
        }
        .badge-pink {
            background: #f778ba33;
            border-color: #f778ba55;
            color: #f778ba;
        }
        .badge-cyan {
            background: #39d2c033;
            border-color: #39d2c055;
            color: #39d2c0;
        }

        /* ── Grid Layout for Skills ── */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
            gap: 0.8rem;
            margin-top: 0.2rem;
        }

        .skill-tag {
            background: #21262d;
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 0.5rem 1rem;
            font-size: 0.85rem;
            font-weight: 450;
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: #e6edf3;
            transition: 0.15s;
        }

        .skill-tag i {
            color: #58a6ff;
            width: 1.2rem;
            text-align: center;
            font-size: 0.95rem;
        }

        .skill-tag:hover {
            background: #30363d;
            border-color: #58a6ff55;
            transform: translateX(3px);
        }

        /* ── Contact list ── */
        .contact-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.8rem;
            margin-top: 0.2rem;
        }

        .contact-list a {
            color: #8b949e;
            text-decoration: none;
            font-size: 0.95rem;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.15s;
            border-bottom: 1px solid transparent;
        }

        .contact-list a i {
            color: #58a6ff;
            font-size: 1rem;
            width: 1.2rem;
            text-align: center;
        }

        .contact-list a:hover {
            color: #f0f6fc;
            border-bottom-color: #58a6ff;
        }

        /* ── Responsive ── */
        @media (max-width: 600px) {
            .card {
                padding: 1.5rem;
            }
            h1 {
                font-size: 1.8rem;
            }
            .header-wrap {
                flex-direction: column;
                align-items: flex-start;
            }
            .avatar {
                width: 76px;
                height: 76px;
                font-size: 2rem;
            }
            .skills-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 420px) {
            .skills-grid {
                grid-template-columns: 1fr;
            }
            .contact-list {
                flex-direction: column;
                gap: 0.4rem;
            }
        }

        /* ── Glow for the name ── */
        .glow {
            text-shadow: 0 0 20px #58a6ff33;
        }

        /* small tagline */
        .tagline {
            color: #8b949e;
            font-size: 0.95rem;
            margin-top: 0.1rem;
        }

        .tagline span {
            color: #f0f6fc;
            font-weight: 500;
        }

        /* ── GitHub stats placeholder ── */
        .stats-wrap {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin-top: 1.2rem;
        }

        .stats-wrap img {
            border-radius: 12px;
            border: 1px solid #30363d;
            max-width: 100%;
            height: auto;
            background: #0d1117;
            transition: 0.2s;
        }

        .stats-wrap img:hover {
            border-color: #58a6ff55;
            transform: scale(1.01);
        }

        /* small footnote */
        .footnote {
            text-align: center;
            font-size: 0.75rem;
            color: #484f58;
            margin-top: 1.8rem;
            letter-spacing: 0.3px;
        }
        .footnote i {
            color: #da3633;
        }
    </style>
</head>
<body>

    <div class="card">

        <!-- ═══ HEADER ═══ -->
        <div class="header-wrap">
            <div>
                <h1 class="glow">Bilal Faisal Arain</h1>
                <h2>
                    <i class="fas fa-code" style="color:#58a6ff; margin-right:6px;"></i>
                    Full‑Stack Developer &amp; Laravel Expert
                </h2>
                <div class="tagline">
                    <i class="fas fa-map-pin" style="color:#58a6ff; margin-right:4px;"></i>
                    <span>PHP · JavaScript</span> &nbsp;|&nbsp; QA Tester · AI Enthusiast
                </div>
                <div class="badge-row">
                    <a href="#"><span class="badge"><i class="fas fa-bolt"></i> Laravel</span></a>
                    <a href="#"><span class="badge badge-blue"><i class="fab fa-react"></i> React</span></a>
                    <a href="#"><span class="badge badge-green"><i class="fab fa-vuejs"></i> Vue.js</span></a>
                    <a href="#"><span class="badge badge-purple"><i class="fab fa-docker"></i> Docker</span></a>
                    <a href="#"><span class="badge badge-orange"><i class="fab fa-aws"></i> AWS</span></a>
                </div>
            </div>
            <div class="avatar">BF</div>
        </div>

        <hr class="divider" />

        <!-- ═══ ABOUT ═══ -->
        <div style="margin-bottom: 1.4rem;">
            <h3><i class="fas fa-user-astronaut"></i> About Me</h3>
            <p style="color:#b1bac4; max-width: 700px;">
                I'm a passionate Full‑Stack Web Developer and QA Tester with a strong focus on
                <strong style="color:#f0f6fc;">Laravel</strong> and <strong style="color:#f0f6fc;">JavaScript</strong>.
                I love building clean, scalable applications and ensuring they perform flawlessly.
                Currently crafting digital experiences at <strong style="color:#f0f6fc;">CodeCreatives Agency</strong>.
            </p>
        </div>

        <!-- ═══ CURRENT WORK ═══ -->
        <div style="margin-bottom: 1.4rem;">
            <h3><i class="fas fa-briefcase"></i> Current Work</h3>
            <div style="background:#0d1117; border-radius:16px; padding:0.8rem 1.2rem; border:1px solid #21262d;">
                <span style="font-weight:600; color:#f0f6fc;">
                    <i class="fas fa-building" style="color:#58a6ff; margin-right:8px;"></i>
                    CodeCreatives Agency
                </span>
                <span style="color:#8b949e; margin-left:0.8rem;">
                    — Full‑Stack Developer &amp; QA Engineer
                </span>
                <div style="margin-top:0.4rem; font-size:0.9rem; color:#8b949e;">
                    <i class="fas fa-code" style="color:#3fb950; margin-right:6px;"></i>
                    Building high‑performance web apps · Laravel · Vue · Tailwind
                </div>
            </div>
        </div>

        <!-- ═══ TECH STACK ═══ -->
        <div style="margin-bottom: 1.4rem;">
            <h3><i class="fas fa-cubes"></i> Tech Stack</h3>
            <div class="skills-grid">

                <!-- Backend -->
                <div class="skill-tag"><i class="fab fa-laravel"></i> Laravel</div>
                <div class="skill-tag"><i class="fab fa-php"></i> PHP</div>

                <!-- Frontend -->
                <div class="skill-tag"><i class="fab fa-html5"></i> HTML5</div>
                <div class="skill-tag"><i class="fab fa-css3-alt"></i> CSS3</div>
                <div class="skill-tag"><i class="fab fa-js"></i> JavaScript</div>
                <div class="skill-tag"><i class="fab fa-bootstrap"></i> Bootstrap</div>
                <div class="skill-tag"><i class="fab fa-tailwind"></i> Tailwind</div>

                <!-- Databases -->
                <div class="skill-tag"><i class="fas fa-database"></i> MySQL</div>
                <div class="skill-tag"><i class="fas fa-database"></i> MongoDB</div>
                <div class="skill-tag"><i class="fas fa-fire"></i> Firebase</div>

                <!-- Tools & Platforms -->
                <div class="skill-tag"><i class="fab fa-git-alt"></i> Git</div>
                <div class="skill-tag"><i class="fab fa-github"></i> GitHub</div>
                <div class="skill-tag"><i class="fas fa-flask"></i> Postman</div>
                <div class="skill-tag"><i class="fab fa-linux"></i> Linux</div>
                <div class="skill-tag"><i class="fas fa-robot"></i> AI Tools</div>
                <div class="skill-tag"><i class="fas fa-paint-brush"></i> Photoshop</div>
                <div class="skill-tag"><i class="fas fa-cube"></i> Unity</div>

            </div>
        </div>

        <!-- ═══ LEARNING ═══ -->
        <div style="margin-bottom: 1.4rem;">
            <h3><i class="fas fa-graduation-cap"></i> Currently Learning</h3>
            <div style="display:flex; flex-wrap:wrap; gap:0.6rem;">
                <span class="badge badge-blue"><i class="fab fa-laravel"></i> Laravel Advanced</span>
                <span class="badge badge-green"><i class="fab fa-vuejs"></i> Vue.js</span>
                <span class="badge badge-cyan"><i class="fab fa-react"></i> React</span>
                <span class="badge badge-orange"><i class="fab fa-docker"></i> Docker</span>
                <span class="badge badge-purple"><i class="fab fa-aws"></i> AWS</span>
            </div>
        </div>

        <!-- ═══ CONTACT ═══ -->
        <div style="margin-bottom: 0.6rem;">
            <h3><i class="fas fa-paper-plane"></i> Connect With Me</h3>
            <div class="contact-list">
                <a href="mailto:bilalfaisalarain@gmail.com">
                    <i class="fas fa-envelope"></i> bilalfaisalarain@gmail.com
                </a>
                <a href="https://instagram.com/bilal.faisalarain" target="_blank">
                    <i class="fab fa-instagram"></i> @bilal.faisalarain
                </a>
                <a href="https://github.com/bilalfaisaldev" target="_blank">
                    <i class="fab fa-github"></i> bilalfaisaldev
                </a>
                <a href="#">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="#">
                    <i class="fab fa-twitter"></i> Twitter
                </a>
            </div>
        </div>

        <hr class="divider" />

        <!-- ═══ GITHUB STATS ═══ -->
        <div>
            <h3 style="justify-content:center; gap:0.8rem; font-size:1rem; color:#8b949e;">
                <i class="fas fa-chart-line" style="color:#58a6ff;"></i>
                GitHub Activity
            </h3>
            <div class="stats-wrap">
                <img
                src="https://github-readme-stats.vercel.app/api?username=bilalfaisaldev&show_icons=true&theme=dark&bg_color=0d1117&border_color=30363d&icon_color=58a6ff&title_color=f0f6fc&text_color=8b949e"
                alt="GitHub Stats"
                width="400"
                />
                <img
                src="https://github-readme-stats.vercel.app/api/top-langs/?username=bilalfaisaldev&layout=compact&theme=dark&bg_color=0d1117&border_color=30363d&title_color=f0f6fc&text_color=8b949e"
                alt="Top Languages"
                width="340"
                />
            </div>
        </div>

        <!-- ═══ FOOTER ═══ -->
        <div class="footnote">
            <i class="fas fa-heart"></i> &nbsp; built with &nbsp; <i class="fas fa-code"></i> &nbsp; · &nbsp; © 2026 Bilal Faisal Arain
        </div>

    </div>

</body>
</html>
