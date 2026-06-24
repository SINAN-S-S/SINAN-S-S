<style>
*{margin:0;padding:0;box-sizing:border-box}
body{background:#020817;color:#e2e8f0;font-family:'Segoe UI',sans-serif}

.banner{width:100%;background:#020817;position:relative;overflow:hidden;border-bottom:1px solid #0f172a}
.stars-wrap{position:absolute;inset:0;pointer-events:none}
.star{position:absolute;border-radius:50%;background:#1e40af}

.banner-inner{position:relative;z-index:2;display:flex;align-items:center;justify-content:space-between;padding:28px 36px 0}

.banner-left{flex:0 0 210px}
.greet{font-size:12px;color:#475569;display:flex;align-items:center;gap:6px;margin-bottom:6px;font-family:monospace}
.greet i{font-size:14px;color:#3b82f6}
.bname{font-size:36px;font-weight:700;color:#fff;line-height:1.1;letter-spacing:-1px}
.bname span{color:#3b82f6}
.brole{font-size:11px;color:#64748b;margin-top:5px;letter-spacing:.6px}
.btags{display:flex;flex-direction:column;gap:4px;margin-top:12px}
.btag{display:flex;align-items:center;gap:6px;font-size:11px;color:#64748b}
.btag i{font-size:13px;color:#3b82f6}

.scene{flex:1;display:flex;justify-content:center;align-items:flex-end;height:260px;position:relative}
.scan{position:absolute;top:0;left:0;right:0;height:2px;background:#3b82f610;animation:scan 5s linear infinite}
@keyframes scan{0%{top:0}100%{top:100%}}

.float-card{position:absolute;background:#070f1e;border:1px solid #1e3a5f;border-radius:5px;padding:4px 8px;font-size:8px;font-family:monospace;color:#60a5fa;z-index:10;display:flex;align-items:center;gap:4px}
.fc1{top:18px;left:8px;animation:flt 3.5s ease-in-out infinite}
.fc2{top:26px;right:8px;animation:flt 3.5s ease-in-out infinite .8s}
.fc3{bottom:70px;left:4px;animation:flt 3.5s ease-in-out infinite 1.6s}
@keyframes flt{0%,100%{transform:translateY(0)}50%{transform:translateY(-7px)}}

.monitor{position:absolute;display:flex;flex-direction:column;align-items:center}
.mon-frame{border-radius:6px;overflow:hidden;border:2px solid #1e3a5f}
.mon-bar{height:16px;background:#0a1628;display:flex;align-items:center;padding:0 7px;gap:4px;border-bottom:1px solid #1e3a5f}
.dot-r{width:6px;height:6px;border-radius:50%;background:#ef4444}
.dot-y{width:6px;height:6px;border-radius:50%;background:#f59e0b}
.dot-g{width:6px;height:6px;border-radius:50%;background:#22c55e}
.fname{font-size:7px;color:#334155;margin-left:4px;font-family:monospace}
.mon-screen{background:#030c1a;padding:6px 8px;font-family:'Courier New',monospace;font-size:7.5px;line-height:1.6}
.kw{color:#60a5fa}.fn{color:#a78bfa}.str{color:#86efac}.var{color:#fbbf24}.cm{color:#334155}.op{color:#f472b6}
.cur{display:inline-block;width:5px;height:9px;background:#3b82f6;vertical-align:middle;animation:bl 1s infinite}
@keyframes bl{0%,49%{opacity:1}50%,100%{opacity:0}}
.mon-stand{width:44px;height:12px;background:#0a1628;border-radius:0 0 3px 3px;border:1px solid #1e3a5f;border-top:none}
.mon-base{width:64px;height:4px;background:#0f172a;border-radius:3px}

.mon-l{bottom:14px;left:2px}
.mon-c{bottom:22px;left:50%;transform:translateX(-50%)}
.mon-r{bottom:14px;right:2px}

.section{padding:16px 28px;border-bottom:1px solid #0f172a}
.stitle{font-size:10px;font-weight:600;color:#3b82f6;text-transform:uppercase;letter-spacing:1.2px;margin-bottom:12px;display:flex;align-items:center;gap:7px}
.stitle::before{content:'';display:inline-block;width:3px;height:12px;background:#3b82f6;border-radius:0}
.stitle i{font-size:13px}

.about-p{font-size:13px;color:#94a3b8;line-height:1.8;max-width:580px}
.about-p b{color:#e2e8f0;font-weight:500}
.info-row{display:flex;gap:18px;margin-top:10px;flex-wrap:wrap}
.iitem{display:flex;align-items:center;gap:5px;font-size:11px;color:#64748b}
.iitem i{font-size:13px;color:#3b82f6}

.sk-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
.sk-card{background:#050d1a;border:1px solid #0f172a;border-radius:8px;padding:12px;transition:border-color .2s}
.sk-card:hover{border-color:#1e40af}
.sk-label{font-size:10px;color:#475569;text-transform:uppercase;letter-spacing:.8px;margin-bottom:10px;display:flex;align-items:center;gap:5px}
.sk-label i{font-size:13px;color:#3b82f6}
.icons-row{display:flex;flex-wrap:wrap;gap:8px}
.tech-icon{width:32px;height:32px;border-radius:7px;border:1px solid #0f172a;display:flex;align-items:center;justify-content:center;cursor:default;transition:border-color .2s;position:relative}
.tech-icon:hover{border-color:#1e40af}
.tech-icon img{width:20px;height:20px;object-fit:contain}
.tip{position:absolute;bottom:-22px;left:50%;transform:translateX(-50%);background:#0f172a;color:#94a3b8;font-size:9px;white-space:nowrap;padding:2px 6px;border-radius:3px;pointer-events:none;opacity:0;transition:opacity .15s;z-index:20;font-family:monospace}
.tech-icon:hover .tip{opacity:1}

.stats-row{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.stat{background:#050d1a;border:1px solid #0f172a;border-radius:8px;padding:14px;text-align:center}
.snum{font-size:24px;font-weight:700;color:#3b82f6}
.slbl{font-size:10px;color:#475569;margin-top:3px;display:flex;align-items:center;justify-content:center;gap:4px}
.slbl i{font-size:11px}

.socials{display:flex;gap:8px;flex-wrap:wrap}
.sbtn{display:flex;align-items:center;gap:6px;padding:6px 14px;border-radius:7px;font-size:11px;font-weight:500;text-decoration:none;border:1px solid;cursor:pointer}
.sgh{background:#050d1a;border-color:#1e3a5f;color:#94a3b8}
.sli{background:#001630;border-color:#1d4ed840;color:#60a5fa}
.sml{background:#1a0000;border-color:#7f1d1d40;color:#f87171}

.footer{background:#020817;border-top:1px solid #0f172a;padding:14px 28px;text-align:center}
.coffee{display:inline-flex;align-items:center;gap:7px;background:#1d3a6e;color:#93c5fd;padding:7px 18px;border-radius:7px;font-size:12px;font-weight:600;border:1px solid #1e40af;cursor:pointer}
</style>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">

<div class="banner">
  <div class="stars-wrap" id="stars"></div>
  <div class="banner-inner">
    <div class="banner-left">
      <div class="greet"><i class="ti ti-terminal-2" aria-hidden="true"></i> hello_world.js</div>
      <div class="bname">I'm <span>Sinan</span></div>
      <div class="brole">Full Stack Developer &nbsp;·&nbsp; MERN Stack</div>
      <div class="btags">
        <div class="btag"><i class="ti ti-map-pin" aria-hidden="true"></i> India</div>
        <div class="btag"><i class="ti ti-mail" aria-hidden="true"></i> sinan202408@gmail.com</div>
        <div class="btag"><i class="ti ti-users" aria-hidden="true"></i> Open to collaboration</div>
        <div class="btag"><i class="ti ti-briefcase" aria-hidden="true"></i> Open to work</div>
      </div>
    </div>

    <div class="scene">
      <div class="scan"></div>
      <div class="float-card fc1"><i class="ti ti-code" style="font-size:9px"></i> &lt;dev /&gt;</div>
      <div class="float-card fc2"><i class="ti ti-git-branch" style="font-size:9px"></i> main</div>
      <div class="float-card fc3"><i class="ti ti-database" style="font-size:9px"></i> MongoDB</div>

      <div class="monitor mon-l">
        <div class="mon-frame" style="width:114px">
          <div class="mon-bar"><div class="dot-r"></div><div class="dot-y"></div><div class="dot-g"></div><span class="fname">app.jsx</span></div>
          <div class="mon-screen" style="height:68px">
            <div><span class="kw">import</span> <span class="str">React</span></div>
            <div><span class="kw">from</span> <span class="op">'react'</span></div>
            <div><span class="cm">// components</span></div>
            <div><span class="fn">export</span> <span class="kw">default</span></div>
            <div><span class="var">App</span></div>
          </div>
        </div>
        <div class="mon-stand"></div><div class="mon-base"></div>
      </div>

      <div class="monitor mon-c">
        <div class="mon-frame" style="width:162px">
          <div class="mon-bar"><div class="dot-r"></div><div class="dot-y"></div><div class="dot-g"></div><span class="fname">sinan.js — main</span></div>
          <div class="mon-screen" style="height:84px">
            <div><span class="kw">const</span> <span class="var">dev</span> = {</div>
            <div>&nbsp;<span class="str">name</span>: <span class="op">"Sinan"</span>,</div>
            <div>&nbsp;<span class="str">stack</span>: [<span class="op">"MERN"</span>],</div>
            <div>&nbsp;<span class="str">ui</span>: <span class="op">"clean"</span>,</div>
            <div>&nbsp;<span class="str">ready</span>: <span class="kw">true</span></div>
            <div>}</div>
            <div><span class="fn">build</span>()<span class="cur"></span></div>
          </div>
        </div>
        <div class="mon-stand" style="width:52px"></div><div class="mon-base" style="width:78px"></div>
      </div>

      <div class="monitor mon-r">
        <div class="mon-frame" style="width:114px">
          <div class="mon-bar"><div class="dot-r"></div><div class="dot-y"></div><div class="dot-g"></div><span class="fname">server.js</span></div>
          <div class="mon-screen" style="height:68px">
            <div><span class="kw">const</span> <span class="var">app</span></div>
            <div>&nbsp;= <span class="fn">express</span>()</div>
            <div><span class="var">app</span>.<span class="fn">listen</span>(</div>
            <div>&nbsp;<span class="op">3000</span>, () =&gt; {</div>
            <div>&nbsp;<span class="cm">// running</span></div>
          </div>
        </div>
        <div class="mon-stand"></div><div class="mon-base"></div>
      </div>

      <svg width="500" height="120" viewBox="0 0 500 120" style="position:absolute;bottom:0;left:50%;transform:translateX(-50%)" role="img">
        <title>Developer at triple monitor desk</title>
        <rect x="20" y="108" width="460" height="9" rx="3" fill="#0a1628" stroke="#1e3a5f" stroke-width="1"/>
        <rect x="50" y="117" width="8" height="7" fill="#070f1e"/>
        <rect x="442" y="117" width="8" height="7" fill="#070f1e"/>
        <rect x="215" y="105" width="16" height="3" rx="1" fill="#1e3a5f"/>
        <rect x="232" y="94" width="36" height="14" rx="2" fill="#030c1a" stroke="#1e3a5f" stroke-width="1"/>
        <ellipse cx="250" cy="93" rx="18" ry="12" fill="#0a1628" stroke="#1e3a5f" stroke-width="1"/>
        <circle cx="250" cy="88" r="8" fill="#0f1f3d"/>
        <rect x="241" y="96" width="18" height="2" rx="1" fill="#1e3a5f"/>
        <rect x="231" y="68" width="38" height="26" rx="2" fill="#050d1a" stroke="#1e3a5f" stroke-width="1"/>
        <line x1="244" y1="68" x2="240" y2="82" stroke="#1e3a5f" stroke-width="1.5"/>
        <line x1="256" y1="68" x2="260" y2="82" stroke="#1e3a5f" stroke-width="1.5"/>
        <rect x="235" y="82" width="15" height="4" rx="1" fill="#0a1628" stroke="#1e40af" stroke-width=".5"/>
        <rect x="250" y="82" width="15" height="4" rx="1" fill="#0a1628" stroke="#1e40af" stroke-width=".5"/>
        <line x1="233" y1="94" x2="222" y2="105" stroke="#1e3a5f" stroke-width="2" stroke-linecap="round"/>
        <line x1="267" y1="94" x2="278" y2="105" stroke="#1e3a5f" stroke-width="2" stroke-linecap="round"/>
        <rect x="235" y="105" width="13" height="5" rx="1" fill="#0a1628" stroke="#1e3a5f" stroke-width=".5"/>
        <rect x="252" y="105" width="13" height="5" rx="1" fill="#0a1628" stroke="#1e3a5f" stroke-width=".5"/>
        <circle cx="250" cy="80" r="2.5" fill="#3b82f6" opacity=".7">
          <animate attributeName="opacity" values=".7;1;.7" dur="2s" repeatCount="indefinite"/>
        </circle>
      </svg>
    </div>
  </div>
</div>

<div class="section">
  <div class="stitle"><i class="ti ti-user" aria-hidden="true"></i> About me</div>
  <div class="about-p">
    I'm an aspiring <b>Full Stack Web Developer</b> passionate about building creative and functional web experiences.
    I focus on <b>clean UI design</b> and scalable <b>full-stack applications</b> using the MERN stack.
  </div>
  <div class="info-row">
    <div class="iitem"><i class="ti ti-map-pin" aria-hidden="true"></i> India</div>
    <div class="iitem"><i class="ti ti-mail" aria-hidden="true"></i> sinan202408@gmail.com</div>
    <div class="iitem"><i class="ti ti-accessible" aria-hidden="true"></i> Open to collaboration</div>
  </div>
</div>

<div class="section">
  <div class="stitle"><i class="ti ti-stack-2" aria-hidden="true"></i> Tech stack</div>
  <div class="sk-grid">
    <div class="sk-card">
      <div class="sk-label"><i class="ti ti-layout" aria-hidden="true"></i> Frontend</div>
      <div class="icons-row">
        <div class="tech-icon" style="background:#1a0f00"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5"><span class="tip">HTML5</span></div>
        <div class="tech-icon" style="background:#001020"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3"><span class="tip">CSS3</span></div>
        <div class="tech-icon" style="background:#1a1500"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JS"><span class="tip">JavaScript</span></div>
        <div class="tech-icon" style="background:#001a1f"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React"><span class="tip">React</span></div>
        <div class="tech-icon" style="background:#1a0f24"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redux/redux-original.svg" alt="Redux"><span class="tip">Redux</span></div>
        <div class="tech-icon" style="background:#001116"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" alt="Tailwind"><span class="tip">Tailwind</span></div>
        <div class="tech-icon" style="background:#0a0020"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" alt="Bootstrap"><span class="tip">Bootstrap</span></div>
      </div>
    </div>
    <div class="sk-card">
      <div class="sk-label"><i class="ti ti-server" aria-hidden="true"></i> Backend</div>
      <div class="icons-row">
        <div class="tech-icon" style="background:#091a08"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node"><span class="tip">Node.js</span></div>
        <div class="tech-icon" style="background:#0a0d10"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" alt="Express" style="filter:invert(1) brightness(.6)"><span class="tip">Express</span></div>
        <div class="tech-icon" style="background:#051228"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python"><span class="tip">Python</span></div>
        <div class="tech-icon" style="background:#010f08"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg" alt="Django" style="filter:brightness(2)"><span class="tip">Django</span></div>
      </div>
    </div>
    <div class="sk-card">
      <div class="sk-label"><i class="ti ti-database" aria-hidden="true"></i> Database</div>
      <div class="icons-row">
        <div class="tech-icon" style="background:#000f05"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="MongoDB"><span class="tip">MongoDB</span></div>
        <div class="tech-icon" style="background:#001116"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL"><span class="tip">MySQL</span></div>
      </div>
    </div>
    <div class="sk-card">
      <div class="sk-label"><i class="ti ti-tools" aria-hidden="true"></i> Tools</div>
      <div class="icons-row">
        <div class="tech-icon" style="background:#1a0500"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git"><span class="tip">Git</span></div>
        <div class="tech-icon" style="background:#050d1a"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" style="filter:invert(1) brightness(.7)"><span class="tip">GitHub</span></div>
        <div class="tech-icon" style="background:#00091a"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="VSCode"><span class="tip">VS Code</span></div>
        <div class="tech-icon" style="background:#120a1f"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" alt="Figma"><span class="tip">Figma</span></div>
      </div>
    </div>
  </div>
</div>

<div class="section">
  <div class="stitle"><i class="ti ti-chart-bar" aria-hidden="true"></i> GitHub stats</div>
  <div class="stats-row">
    <div class="stat">
      <div class="snum">120+</div>
      <div class="slbl"><i class="ti ti-git-commit" aria-hidden="true"></i> Total commits</div>
    </div>
    <div class="stat">
      <div class="snum" style="color:#a78bfa">15+</div>
      <div class="slbl"><i class="ti ti-folder" aria-hidden="true"></i> Repositories</div>
    </div>
    <div class="stat">
      <div class="snum" style="color:#22c55e;font-size:16px">Active</div>
      <div class="slbl"><i class="ti ti-flame" aria-hidden="true"></i> Current streak</div>
    </div>
  </div>
</div>

<div class="section" style="border-bottom:none">
  <div class="stitle"><i class="ti ti-share" aria-hidden="true"></i> Connect</div>
  <div class="socials">
    <a class="sbtn sgh" href="https://github.com/SINAN-S-S"><i class="ti ti-brand-github" style="font-size:14px" aria-hidden="true"></i> SINAN-S-S</a>
    <a class="sbtn sli" href="https://www.linkedin.com/in/sinan-9993273a7"><i class="ti ti-brand-linkedin" style="font-size:14px" aria-hidden="true"></i> LinkedIn</a>
    <a class="sbtn sml" href="mailto:sinan202408@gmail.com"><i class="ti ti-mail" style="font-size:14px" aria-hidden="true"></i> sinan202408@gmail.com</a>
  </div>
</div>

<div class="footer">
  <div style="font-size:11px;color:#334155;margin-bottom:9px;display:flex;align-items:center;justify-content:center;gap:5px">
    <i class="ti ti-heart" style="font-size:12px;color:#3b82f6" aria-hidden="true"></i> If you like my work, support me
  </div>
  <span class="coffee"><i class="ti ti-coffee" aria-hidden="true"></i> Buy me a coffee</span>
</div>

<script>
const sw = document.getElementById('stars');
for(let i=0;i<55;i++){
  const d=document.createElement('div');
  d.className='star';
  const sz=Math.random()>0.8?3:2;
  d.style.cssText=`left:${Math.random()*100}%;top:${Math.random()*100}%;width:${sz}px;height:${sz}px;opacity:${.08+Math.random()*.35};animation:bl ${2+Math.random()*3}s infinite ${Math.random()*3}s`;
  sw.appendChild(d);
}
const style=document.createElement('style');
style.textContent='@keyframes bl{0%,49%{opacity:inherit}50%,100%{opacity:0}}';
document.head.appendChild(style);
</script>
