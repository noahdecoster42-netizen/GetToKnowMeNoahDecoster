
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Noah Decoster — Get to know me</title>
    <style>
        :root{
            --bg1:#0f1724;
            --bg2:#0b1020;
            --accent:#7c5cff;
            --accent-2:#24d3b5;
            --glass: rgba(255,255,255,0.06);
            --glass-2: rgba(255,255,255,0.04);
            --card-radius:16px;
            --max-w:980px;
            --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", "Segoe UI Mono", monospace;
            --ui: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
        }

        *{box-sizing:border-box}
        html,body{height:100%}
        body{
            margin:0;
            font-family:var(--ui);
            background: radial-gradient(1200px 600px at 10% 10%, rgba(124,92,255,0.12), transparent 10%),
                                    radial-gradient(1000px 500px at 90% 90%, rgba(36,211,181,0.08), transparent 10%),
                                    linear-gradient(180deg,var(--bg1),var(--bg2));
            color:#e6eef8;
            -webkit-font-smoothing:antialiased;
            -moz-osx-font-smoothing:grayscale;
            padding:40px 20px;
            display:flex;
            align-items:center;
            justify-content:center;
        }

        .wrap{
            width:100%;
            max-width:var(--max-w);
            backdrop-filter: blur(6px) saturate(120%);
            border-radius:20px;
            padding:28px;
            background: linear-gradient(180deg,var(--glass), var(--glass-2));
            box-shadow: 0 8px 30px rgba(2,6,23,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
            display:grid;
            grid-template-columns: 360px 1fr;
            gap:28px;
        }

        /* LEFT PANEL */
        .profile{
            border-radius:var(--card-radius);
            padding:22px;
            background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
            display:flex;
            flex-direction:column;
            gap:18px;
            align-items:center;
            text-align:center;
        }

        .avatar{
            width:140px;
            height:140px;
            border-radius:50%;
            display:flex;
            align-items:center;
            justify-content:center;
            font-size:64px;
            background: linear-gradient(135deg,var(--accent),var(--accent-2));
            box-shadow: 0 8px 30px rgba(124,92,255,0.12);
            transform-origin:center;
            animation: float 3.6s ease-in-out infinite;
        }
        @keyframes float{
            0%{transform:translateY(0) rotate(-4deg)}
            50%{transform:translateY(-10px) rotate(4deg)}
            100%{transform:translateY(0) rotate(-4deg)}
        }

        h1{
            margin:0;
            font-size:20px;
            letter-spacing:0.2px;
        }
        .sub{
            font-size:13px;
            color:rgba(230,238,248,0.7);
        }

        .quick{
            width:100%;
            display:grid;
            grid-template-columns:repeat(2,1fr);
            gap:10px;
        }
        .chip{
            background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
            padding:10px;
            border-radius:10px;
            font-size:13px;
        }

        .skills{
            width:100%;
            display:flex;
            flex-direction:column;
            gap:8px;
            align-items:stretch;
        }
        .skill{
            font-size:13px;
            display:flex;
            justify-content:space-between;
            gap:10px;
            align-items:center;
        }
        .bar{
            height:8px;
            background:rgba(255,255,255,0.04);
            border-radius:6px;
            overflow:hidden;
        }
        .bar > i{
            display:block;
            height:100%;
            background: linear-gradient(90deg,var(--accent),var(--accent-2));
            width:0;
            border-radius:6px;
            transition:width 1s cubic-bezier(.2,.9,.3,1);
        }

        /* RIGHT PANEL */
        .content{
            padding:18px;
            border-radius:var(--card-radius);
            background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
            display:flex;
            flex-direction:column;
            gap:18px;
        }

        .hero{
            display:flex;
            align-items:flex-start;
            gap:16px;
            justify-content:space-between;
        }
        .intro{
            flex:1;
        }
        .intro h2{
            margin:0;
            font-size:20px;
        }
        .intro p{
            margin:6px 0 0 0;
            color:rgba(230,238,248,0.78);
            font-size:14px;
        }

        .cta{
            display:flex;
            gap:10px;
            align-items:center;
        }
        .btn{
            padding:10px 14px;
            border-radius:10px;
            background:linear-gradient(90deg,var(--accent),var(--accent-2));
            color:#041226;
            font-weight:600;
            text-decoration:none;
            box-shadow: 0 6px 18px rgba(36,211,181,0.08);
            transition:transform .18s ease, box-shadow .18s ease;
        }
        .btn:active{transform:translateY(1px)}
        .ghost{
            padding:10px 14px;
            border-radius:10px;
            background:transparent;
            color:rgba(230,238,248,0.9);
            border:1px solid rgba(255,255,255,0.04);
            font-weight:600;
        }

        .cards{
            display:grid;
            grid-template-columns:repeat(2,1fr);
            gap:12px;
        }
        .card{
            padding:12px;
            border-radius:12px;
            background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));
        }
        .card h3{margin:0 0 6px 0;font-size:14px}
        .card p{margin:0;color:rgba(230,238,248,0.78);font-size:13px}

        .goals{display:flex;flex-direction:column;gap:10px}
        .goal{display:flex;align-items:center;gap:12px}
        .dot{width:10px;height:10px;border-radius:50%;background:linear-gradient(90deg,var(--accent),var(--accent-2))}

        .fun{
            margin-top:6px;
            display:flex;
            gap:10px;
            align-items:center;
        }

        /* CSS-only toggle for fun fact */
        .reveal{
            display:flex;
            gap:8px;
            align-items:center;
        }
        .reveal input{display:none}
        .reveal label{
            padding:8px 12px;border-radius:10px;background:transparent;border:1px solid rgba(255,255,255,0.04);cursor:pointer;font-size:13px;
        }
        .fact{max-height:0;overflow:hidden;transition:max-height .5s ease, padding .3s ease;opacity:0;padding:0 8px}
        .reveal input:checked ~ .fact{
            max-height:120px;opacity:1;padding:10px 8px;
        }

        footer{font-size:12px;color:rgba(230,238,248,0.6);text-align:center;padding-top:8px}

        /* Responsive */
        @media (max-width:880px){
            .wrap{grid-template-columns:1fr; padding:18px}
            .avatar{width:110px;height:110px;font-size:52px}
        }

        /* Animate bars on load via keyframe trick */
        body.loaded .bar > i[data-width="80"]{width:80%}
        body.loaded .bar > i[data-width="60"]{width:60%}
        body.loaded .bar > i[data-width="25"]{width:25%}
    </style>
</head>
<body>
    <div class="wrap" role="main" aria-label="Noah Decoster profile card">
        <aside class="profile" aria-labelledby="name">
            <div class="avatar" aria-hidden="true">🕺</div>
            <div>
                <h1 id="name">Noah Decoster</h1>
                <div class="sub">16 jaar oud • lerende web designer • danser</div>
            </div>

            <div class="quick" aria-hidden="false">
                <div class="chip">Location: België</div>
                <div class="chip">School: secundair onderwijs 5de Jaar</div>
            </div>

            <div style="width:100%;">
                <h3 style="margin:10px 0 8px 0;font-size:13px;color:rgba(230,238,248,0.85)">Skills</h3>
                <div class="skills">
                    <div class="skill"><span>Dansen</span><strong>80%</strong></div>
                    <div class="bar"><i data-width="80"></i></div>

                    <div class="skill"><span>HTML & CSS</span><strong>60%</strong></div>
                    <div class="bar"><i data-width="60"></i></div>

                    <div class="skill"><span>JavaScript (starting)</span><strong>25%</strong></div>
                    <div class="bar"><i data-width="25"></i></div>
                </div>
            </div>

            <div style="width:100%;display:flex;gap:10px;justify-content:center">
                <a class="btn" href="#" onclick="alert('Keep practicing and build small projects!');return false">Start learning</a>
                <a class="ghost" href="#" onclick="alert('Say hi to Noah!');return false">Say hi</a>
            </div>
        </aside>

        <section class="content">
            <div class="hero">
                <div class="intro">
                    <h2>Hi — I'm Noah</h2>
                    <p>Ik hou van dansen, muziek en creatief bezig zijn. Ik ben 15 jaar oud en enthousiast om webdesign te leren, zodat ik coole websites voor mezelf en mijn vrienden kan bouwen.</p>
                </div>
                <div class="cta" aria-hidden="true">
                    <div style="font-size:28px;opacity:0.95">💫</div>
                </div>
            </div>

            <div class="cards" role="region" aria-label="About and Interests">
                <div class="card">
                    <h3>About me</h3>
                    <p>Creative, curious, and energetic. I practice different dance styles and enjoy choreographing small routines. On the web side, I love seeing how designs come together.</p>
                </div>

                <div class="card">
                    <h3>Interests</h3>
                    <p>Dance, music production, visual design, and experimenting with code to turn ideas into interactive pages.</p>
                </div>
            </div>

            <div class="goals" role="list" aria-label="Goals">
                <div class="goal" role="listitem"><div class="dot"></div><div><strong>Short term:</strong> Learn HTML & CSS thoroughly and build a personal portfolio.</div></div>
                <div class="goal" role="listitem"><div class="dot"></div><div><strong>Medium term:</strong> Learn responsive design and basic JavaScript interactions.</div></div>
                <div class="goal" role="listitem"><div class="dot"></div><div><strong>Fun project:</strong> A small website showcasing dance videos and choreography ideas.</div></div>
            </div>

            <div class="fun" aria-label="Fun and interactive">
                <div class="reveal">
                    <input type="checkbox" id="toggle" />
                    <label for="toggle">Reveal a fun fact</label>
                    <div class="fact">I sometimes choreograph moves to my favorite songs and record them on my phone — then I try to make a short website to show them off!</div>
                </div>
                <div style="margin-left:auto;color:rgba(230,238,248,0.75);font-size:13px">Want to learn with me? Start a small project and try one page at a time.</div>
            </div>

            <footer>
                Built by Noah — a simple, stylish starter page to introduce yourself. Tip: open this file, edit the text, colors, or emoji to make it yours.
            </footer>
        </section>
    </div>

    <script>
        // small enhancement: animate bars when loaded
        window.addEventListener('load', function(){
            document.body.classList.add('loaded');
        });
    </script>
</body>
</html></div>
