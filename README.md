<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="theme-color" content="#f6d6df" />
  <title>LOVECHAIN — Love, but forever.</title>
  <meta name="description" content="LOVECHAIN — A place to store human love on-chain. Every memory. Every sacrifice. Recorded for eternity." />

  <style>
    :root{
      --bg1:#fff7f9;
      --bg2:#fff1f6;
      --ink:#2b2a2e;
      --muted:#6b6670;
      --card:#ffffffcc;
      --stroke:#f0d4dd;
      --accent:#ff5aa5;
      --accent2:#b07cff;
      --gold:#caa76a;
      --shadow: 0 16px 60px rgba(20,16,24,.10);
      --radius: 22px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;
      color:var(--ink);
      background:
        radial-gradient(1200px 600px at 20% -10%, #ffe2ef 0%, transparent 60%),
        radial-gradient(900px 600px at 110% 30%, #eadbff 0%, transparent 55%),
        linear-gradient(180deg, var(--bg1), var(--bg2));
    }
    a{color:inherit; text-decoration:none}
    .wrap{max-width:1120px; margin:0 auto; padding:24px}
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      gap:16px;
      position:sticky; top:0;
      padding:14px 0;
      backdrop-filter: blur(10px);
      background: linear-gradient(180deg, rgba(255,247,249,.85), rgba(255,247,249,.45));
      border-bottom:1px solid rgba(240,212,221,.65);
      z-index:10;
    }
    .brand{
      display:flex; align-items:center; gap:10px;
      font-weight:800; letter-spacing:.3px;
    }
    .mark{
      width:40px; height:40px; border-radius:14px;
      background:
        radial-gradient(14px 14px at 30% 30%, #fff 0%, rgba(255,255,255,.45) 55%, transparent 60%),
        linear-gradient(135deg, #ff5aa5, #b07cff);
      box-shadow: 0 12px 30px rgba(255,90,165,.25);
      position:relative;
    }
    .mark:before{
      content:"";
      position:absolute; inset:9px 11px 13px 11px;
      border-radius:999px 999px 16px 16px;
      transform: rotate(-6deg);
      background: rgba(255,255,255,.85);
      clip-path: polygon(50% 0%, 62% 10%, 75% 24%, 86% 40%, 90% 58%, 84% 76%, 70% 90%, 50% 100%, 30% 90%, 16% 76%, 10% 58%, 14% 40%, 25% 24%, 38% 10%);
      opacity:.9;
      filter: drop-shadow(0 6px 10px rgba(0,0,0,.06));
    }
    .navlinks{
      display:flex; gap:10px; align-items:center; flex-wrap:wrap; justify-content:flex-end;
    }
    .pill{
      display:inline-flex; align-items:center; gap:8px;
      padding:10px 12px; border-radius:999px;
      border:1px solid rgba(240,212,221,.95);
      background: rgba(255,255,255,.65);
      box-shadow: 0 10px 25px rgba(20,16,24,.06);
      font-weight:650; color:var(--ink);
      transition:.18s transform ease, .18s box-shadow ease, .18s background ease;
    }
    .pill:hover{transform: translateY(-1px); box-shadow: 0 14px 28px rgba(20,16,24,.10); background: rgba(255,255,255,.82)}
    .hero{
      padding:44px 0 24px;
      display:grid; grid-template-columns: 1.2fr .8fr;
      gap:22px;
      align-items:stretch;
    }
    @media (max-width: 900px){ .hero{grid-template-columns:1fr; padding-top:26px;} }
    .card{
      border:1px solid rgba(240,212,221,.92);
      background: var(--card);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding:22px;
    }
    .headline{
      font-size: clamp(34px, 4.2vw, 54px);
      line-height:1.02;
      margin:0 0 10px;
      letter-spacing:-.8px;
    }
    .sub{
      margin:0 0 18px;
      font-size: 16.5px;
      line-height:1.6;
      color:var(--muted);
      max-width: 60ch;
    }
    .badge{
      display:inline-flex; gap:8px; align-items:center;
      padding:8px 10px; border-radius:999px;
      border:1px solid rgba(240,212,221,.95);
      background: rgba(255,255,255,.72);
      font-weight:700;
      color: #4a3e49;
    }
    .gradient-text{
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      -webkit-background-clip:text; background-clip:text;
      color:transparent;
    }
    .ctaRow{display:flex; gap:10px; flex-wrap:wrap; margin-top:14px}
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      gap:10px;
      padding:12px 14px;
      border-radius:14px;
      border:1px solid rgba(240,212,221,.95);
      background: rgba(255,255,255,.75);
      font-weight:800;
      cursor:pointer;
      transition:.18s transform ease, .18s box-shadow ease, .18s background ease;
      box-shadow: 0 12px 28px rgba(20,16,24,.08);
    }
    .btn:hover{transform: translateY(-1px); box-shadow: 0 16px 32px rgba(20,16,24,.12); background: rgba(255,255,255,.92)}
    .btn.primary{
      border-color: rgba(255,90,165,.35);
      background: linear-gradient(135deg, rgba(255,90,165,.22), rgba(176,124,255,.18));
    }
    .btn small{font-weight:750; color:var(--muted)}
    .kpis{display:grid; grid-template-columns: repeat(3, 1fr); gap:10px; margin-top:14px}
    @media (max-width: 520px){ .kpis{grid-template-columns:1fr} }
    .kpi{
      padding:14px;
      border-radius:16px;
      border:1px solid rgba(240,212,221,.95);
      background: rgba(255,255,255,.70);
    }
    .kpi b{display:block; font-size:14px}
    .kpi span{display:block; color:var(--muted); margin-top:6px; font-size:13px; line-height:1.45}
    .asideTop{
      display:flex; flex-direction:column; gap:12px; height:100%;
    }
    .miniTitle{margin:0 0 8px; font-size:14px; letter-spacing:.2px; color:#4a3e49}
    .mono{
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      font-size: 13px;
      color:#3d3640;
      word-break: break-all;
      line-height:1.5;
    }
    .walletBox{
      padding:14px;
      border-radius:18px;
      border:1px dashed rgba(202,167,106,.55);
      background: rgba(255,255,255,.72);
    }
    .row{
      display:flex; align-items:center; justify-content:space-between; gap:10px; flex-wrap:wrap;
    }
    .copy{
      border:1px solid rgba(240,212,221,.95);
      background: rgba(255,255,255,.80);
      padding:10px 12px;
      border-radius:12px;
      font-weight:800;
      cursor:pointer;
      user-select:none;
    }
    .copy:active{transform: translateY(1px)}
    .section{padding:18px 0}
    .section h2{
      margin:0 0 10px;
      font-size: 22px;
      letter-spacing:-.3px;
    }
    .grid{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:12px;
    }
    @media (max-width: 900px){ .grid{grid-template-columns:1fr} }
    .tile{
      padding:16px;
      border-radius:20px;
      border:1px solid rgba(240,212,221,.95);
      background: rgba(255,255,255,.70);
    }
    .tile b{display:block; margin-bottom:6px}
    .tile p{margin:0; color:var(--muted); line-height:1.55; font-size:14px}
    .divider{
      height:1px; background: rgba(240,212,221,.85);
      margin:18px 0;
      border-radius:999px;
    }
    .footer{
      padding:26px 0 36px;
      color:var(--muted);
      font-size:13px;
      line-height:1.6;
    }
    .toast{
      position: fixed;
      left:50%; bottom:18px;
      transform: translateX(-50%);
      background: rgba(30,26,35,.92);
      color:#fff;
      padding:10px 12px;
      border-radius:999px;
      font-weight:800;
      font-size:13px;
      opacity:0;
      pointer-events:none;
      transition: opacity .2s ease, transform .2s ease;
      box-shadow: 0 16px 40px rgba(0,0,0,.25);
      z-index:99;
    }
    .toast.show{opacity:1; transform: translateX(-50%) translateY(-4px);}
    .heartline{
      height:8px; border-radius:999px;
      background: linear-gradient(90deg, rgba(255,90,165,.0), rgba(255,90,165,.55), rgba(176,124,255,.55), rgba(255,90,165,.0));
      filter: blur(.2px);
      margin-top:12px;
    }
    .smallmuted{color:var(--muted); font-size:13px; line-height:1.55; margin:0}
  </style>
</head>

<body>
  <div class="wrap">
    <header class="nav">
      <div class="brand" aria-label="LoveChain">
        <div class="mark" aria-hidden="true"></div>
        <div>
          <div style="font-size:14px; opacity:.9;">LOVECHAIN</div>
          <div style="font-size:12px; color:var(--muted); font-weight:700;">Love, but forever.</div>
        </div>
      </div>

      <nav class="navlinks" aria-label="Primary">
        <a class="pill" href="https://t.me/lovechainportal" target="_blank" rel="noopener noreferrer">Telegram</a>
        <a class="pill" href="https://x.com/LoveChainWorld" target="_blank" rel="noopener noreferrer">X (Twitter)</a>
        <a class="pill" href="#burn">Burn Wallet</a>
      </nav>
    </header>

    <main>
      <section class="hero" aria-label="Hero">
        <div class="card">
          <span class="badge">💗 Emotional Blockchain</span>
          <h1 class="headline">
            Store <span class="gradient-text">human love</span><br/>
            on-chain—forever.
          </h1>
          <p class="sub">
            LOVECHAIN is a place to preserve love as an eternal legacy.
            Every memory. Every sacrifice. Recorded for eternity.
          </p>

          <div class="ctaRow">
            <a class="btn primary" href="https://t.me/lovechainportal" target="_blank" rel="noopener noreferrer">
              Join Telegram <small>t.me/lovechainportal</small>
            </a>
            <a class="btn" href="https://x.com/LoveChainWorld" target="_blank" rel="noopener noreferrer">
              Follow on X <small>@LoveChainWorld</small>
            </a>
            <button class="btn" id="copyBurnTop" type="button">Copy Burn Wallet</button>
          </div>

          <div class="kpis" aria-label="Key points">
            <div class="kpi">
              <b>Love Proof</b>
              <span>Record devotion as a permanent on-chain trace.</span>
            </div>
            <div class="kpi">
              <b>Sacrifice Burn</b>
              <span>Burn $LOVE as a symbol of true commitment.</span>
            </div>
            <div class="kpi">
              <b>Legacy</b>
              <span>Turn memories into timeless inheritance.</span>
            </div>
          </div>

          <div class="heartline" aria-hidden="true"></div>
        </div>

        <aside class="asideTop">
          <div class="card walletBox" id="burn" aria-label="Burn wallet">
            <div class="row">
              <div>
                <p class="miniTitle" style="margin:0; font-weight:900;">🔥 Burn Wallet (Sacrifice)</p>
                <p class="smallmuted">Public on-chain address used for symbolic burns.</p>
              </div>
              <button class="copy" id="copyBurn" type="button">Copy</button>
            </div>
            <div class="divider"></div>
            <div class="mono" id="burnAddr">
              CtGKzKwjvE1Z8SxaLAeGkE1Q58PqkszjoExsUko3VAYu
            </div>
            <div class="divider"></div>
            <p class="smallmuted">
              Burns are irreversible. Always double-check the address before sending.
            </p>
          </div>

          <div class="card" aria-label="Quick links">
            <p class="miniTitle" style="font-weight:900;">Quick Links</p>
            <div style="display:flex; flex-direction:column; gap:10px;">
              <a class="pill" href="https://t.me/lovechainportal" target="_blank" rel="noopener noreferrer">
                💬 Telegram Portal
              </a>
              <a class="pill" href="https://x.com/LoveChainWorld" target="_blank" rel="noopener noreferrer">
                𝕏 LoveChainWorld
              </a>
            </div>
            <div class="divider"></div>
            <p class="smallmuted">
              Tip: pin the burn wallet in Telegram for transparency.
            </p>
          </div>
        </aside>
      </section>

      <section class="section" aria-label="What is LoveChain">
        <div class="card">
          <h2>What is LOVECHAIN?</h2>
          <p class="sub" style="max-width:none;">
            LOVECHAIN is designed to treat love as something sacred: not only felt, but preserved.
            It frames commitment as a story—made of memories and sacrifices—so it can be honored, remembered, and carried forward.
          </p>

          <div class="grid" role="list">
            <div class="tile" role="listitem">
              <b>💞 Memory of Us</b>
              <p>Preserve moments that matter—gentle, timeless, meaningful.</p>
            </div>
            <div class="tile" role="listitem">
              <b>🕯️ Forever Message</b>
              <p>Leave words for the future—anniversary notes, vows, and legacy letters.</p>
            </div>
            <div class="tile" role="listitem">
              <b>🔥 Burn as Sacrifice</b>
              <p>True love has a cost. Burns represent real commitment—permanent and visible on-chain.</p>
            </div>
          </div>

          <div class="divider"></div>

          <h2>Rituals (Simple & Powerful)</h2>
          <div class="grid" role="list">
            <div class="tile" role="listitem">
              <b>💍 Eternal Vow Burn</b>
              <p>Two hearts choose each other—recorded as a vow for eternity.</p>
            </div>
            <div class="tile" role="listitem">
              <b>🤍 Forgiveness Burn</b>
              <p>Forgiveness means losing ego. The burn becomes proof that love survived a wound.</p>
            </div>
            <div class="tile" role="listitem">
              <b>🎂 Memory Burn</b>
              <p>A small yearly burn to honor time—because time is the greatest sacrifice.</p>
            </div>
          </div>
        </div>
      </section>

      <section class="section" aria-label="Transparency">
        <div class="card">
          <h2>Transparency</h2>
          <p class="sub" style="max-width:none;">
            LOVECHAIN is built on trust. All ritual burns are public and verifiable. Use the official links below and
            never trust random DMs.
          </p>

          <div class="grid" role="list">
            <div class="tile" role="listitem">
              <b>Official Telegram</b>
              <p class="mono">https://t.me/lovechainportal</p>
            </div>
            <div class="tile" role="listitem">
              <b>Official X</b>
              <p class="mono">https://x.com/LoveChainWorld</p>
            </div>
            <div class="tile" role="listitem">
              <b>Burn Wallet</b>
              <p class="mono">CtGKzKwjvE1Z8SxaLAeGkE1Q58PqkszjoExsUko3VAYu</p>
            </div>
          </div>

          <div class="divider"></div>

          <p class="smallmuted">
            Disclaimer: This website is for informational purposes only and does not constitute financial advice.
            Cryptocurrency involves risk. Always do your own research.
          </p>
        </div>
      </section>

      <footer class="footer">
        <div class="row" style="align-items:flex-start;">
          <div>
            <div style="font-weight:900; color:#4a3e49;">LOVECHAIN</div>
            <div style="margin-top:6px;">Love, but forever.</div>
          </div>
          <div style="text-align:right;">
            <a class="pill" href="https://t.me/lovechainportal" target="_blank" rel="noopener noreferrer">Telegram</a>
            <a class="pill" href="https://x.com/LoveChainWorld" target="_blank" rel="noopener noreferrer">X</a>
          </div>
        </div>
      </footer>
    </main>
  </div>

  <div class="toast" id="toast">Copied!</div>

  <script>
    (function(){
      const burn = "CtGKzKwjvE1Z8SxaLAeGkE1Q58PqkszjoExsUko3VAYu";
      const toast = document.getElementById("toast");

      function showToast(text){
        toast.textContent = text || "Copied!";
        toast.classList.add("show");
        setTimeout(()=>toast.classList.remove("show"), 1200);
      }

      async function copy(text){
        try{
          await navigator.clipboard.writeText(text);
          showToast("Burn wallet copied");
        }catch(e){
          // Fallback
          const ta = document.createElement("textarea");
          ta.value = text;
          document.body.appendChild(ta);
          ta.select();
          document.execCommand("copy");
          ta.remove();
          showToast("Burn wallet copied");
        }
      }

      document.getElementById("copyBurn").addEventListener("click", ()=>copy(burn));
      document.getElementById("copyBurnTop").addEventListener("click", ()=>copy(burn));
      document.getElementById("burnAddr").addEventListener("click", ()=>copy(burn));
    })();
  </script>
</body>
</html>
