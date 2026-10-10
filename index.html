<!doctype html>
<html lang="nl"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>Hormuz Tanker</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#dde8ee;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#060d14}}
:root[data-theme="dark"]{--bg:#060d14}
html{height:100%;scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;height:100%;background:var(--bg);display:grid;place-items:center;font-family:'Barlow Condensed',system-ui,sans-serif;overscroll-behavior:none;user-select:none;-webkit-user-select:none}
#g{position:relative;width:min(100vw,calc((100dvh - env(safe-area-inset-top,0px) - env(safe-area-inset-bottom,0px))*.625));aspect-ratio:5/8;overflow:hidden;font-size:calc(var(--u,1px)*16);background:#0d5c70}
canvas{width:100%;height:100%;display:block;touch-action:none}
#t{position:absolute;left:3%;right:3%;top:1.5%;background:#f3ecd8;color:#1b1a14;border-radius:.3em;padding:.45em .65em;font-size:.88em;line-height:1.15;border-left:.4em solid #888;box-shadow:0 .2em .6em rgba(0,0,0,.35);pointer-events:none;font-weight:600}
#t b{display:block;font-size:.8em;opacity:.65;font-weight:700}
#t.o{border-color:#2f9e5b}#t.c{border-color:#d63a2f}#t.v{border-color:#e0a21a}
#b{position:absolute;right:3%;bottom:1.2%;height:2.9em;padding:0 1.1em;font:700 1em inherit;font-family:inherit;border:0;border-radius:2em;background:#e0a21a;color:#1a1204;touch-action:manipulation;cursor:pointer}
#b.on{background:#d63a2f;color:#fff}
#b:focus-visible,#ov button:focus-visible{outline:3px solid #fff;outline-offset:2px}
#ov{position:absolute;inset:0;background:rgba(5,15,22,.86);display:flex;flex-direction:column;justify-content:center;padding:8%;color:#f3ecd8;gap:.3em;font-size:1em}
#ov h1{font-size:2.8em;line-height:.95;margin:0 0 .2em;font-weight:700}
#ov p{margin:.3em 0;font-size:1.05em;line-height:1.2;font-weight:600}
#ov small{opacity:.65;font-size:.85em}
#ov button{margin-top:.8em;align-self:flex-start;font:700 1.25em inherit;font-family:inherit;padding:.5em 1.4em;border:0;border-radius:2em;background:#e0a21a;color:#1a1204;cursor:pointer}
</style></head><body>
<div id="g"><canvas id="c" width="800" height="1280"></canvas><div id="t" style="display:none"></div><button id="b">⏩ Vol gas</button><div id="ov"></div></div>
<script>
const $=i=>document.getElementById(i),G=$('g'),cv=$('c'),x=cv.getContext('2d'),tw=$('t'),bt=$('b'),ov=$('ov');
const W=400,H=640,SEG=650,clamp=(v,a,b)=>Math.max(a,Math.min(b,v));
const LV=[{len:3200,pf:.3,mine:200,bomb:430,T:1.2},{len:3600,pf:.4,mine:150,bomb:320,T:1.1},{len:4000,pf:.5,mine:115,bomb:240,T:1}];
const TX={o:["De Straat van Hormuz is WIJD open. Prachtig water. Iedereen zegt het.","Geen blokkade. Nooit geweest. Fake news! Tankers, vaar maar door.","Hormuz is open voor zaken. Het beste verkeer ooit, geloof me.","Alles vlot in Hormuz. Heel rustig. Gewoon gáán, kapiteins."],
c:["De Straat van Hormuz is DICHT. Totaal dicht. Niemand komt erdoor.","Wij sluiten Hormuz. Heel slim, veel mensen zeggen dat.","Blokkade is een feit. Ik zou nu niet varen. Echt niet.","Hormuz: gesloten. Er komt iets groots aan. Je zult zien."],
v:["Open? Dicht? We zien het over twee weken. Misschien eerder.","Sommigen zeggen open, anderen dicht. Ik zeg: een beetje allebei.","We kijken heel serieus naar Hormuz. Beslissing komt snel. Of niet."]};
const Lx=w=>45+28*Math.sin(w*.0045)+14*Math.sin(w*.013+1),Rx=w=>W-(45+28*Math.sin(w*.004+2)+14*Math.sin(w*.011));
let S,hi=0,ac;try{hi=+localStorage.getItem('hh')||0}catch(e){}
const ns=(l,h,sc)=>({lvl:l,d:0,hull:h,score:sc,seg:-1,closed:false,nm:0,nb:0,mines:[],bombs:[],parts:[],px:200,py:480,tx:200,ty:480,ang:0,v:40,boost:false,shake:0,flash:0,t:0,run:false});
function snd(f,d,t,v,e){try{ac=ac||new(window.AudioContext||window.webkitAudioContext)();const o=ac.createOscillator(),g=ac.createGain(),n=ac.currentTime;o.type=t;o.frequency.setValueAtTime(f,n);o.frequency.exponentialRampToValueAtTime(e||f,n+d);g.gain.setValueAtTime(v,n);g.gain.exponentialRampToValueAtTime(.001,n+d);o.connect(g);g.connect(ac.destination);o.start();o.stop(n+d)}catch(e){}}
function show(h,p,b,f){ov.innerHTML='<h1>'+h+'</h1>'+p+'<button>'+b+'</button>';ov.style.display='flex';const k=ov.querySelector('button');k.onclick=()=>{ov.style.display='none';f()};k.focus()}
function bb(){bt.className=S.boost?'on':'';bt.textContent=S.boost?'⏸ Rustig aan':'⏩ Vol gas'}
function begin(l=0,h=100,sc=0){S=ns(l,h,sc);S.run=true;tw.style.display='';bb()}
function tb(){if(S&&S.run){S.boost=!S.boost;bb();snd(300,.1,'triangle',.08,500)}}
bt.onclick=tb;
function say(){const L=LV[S.lvl],r=Math.random(),k=r<.4?'o':r<.8?'c':'v',a=TX[k];
S.closed=k=='o'?Math.random()<L.pf:k=='c'?Math.random()>=L.pf:Math.random()<.5;
tw.className=k;tw.innerHTML='<b>De President, zojuist gepost</b>'+a[Math.random()*a.length|0];snd(520,.15,'triangle',.08,420)}
function boom(px,py){for(let i=0;i<26;i++){const a=Math.random()*6.28,s=30+Math.random()*130;S.parts.push({x:px,y:py,vx:Math.cos(a)*s,vy:Math.sin(a)*s,l:.6+Math.random()*.5,m:1.1,c:Math.random()<.5?'#ff9a2e':'#ffe27a',r:2+Math.random()*4})}snd(140,.5,'sawtooth',.22,30)}
function hit(px,py,d){S.hull-=d;S.shake=.5;S.flash=.35;boom(px,py);if(S.hull<=0){S.hull=0;over()}}
function over(){S.run=false;const sc=Math.floor(S.score);if(sc>hi){hi=sc;try{localStorage.setItem('hh',hi)}catch(e){}}
show('Tanker gezonken','<p>De romp scheurde open en de lading lekt in de Golf. Je haalde '+Math.floor(S.d/LV[S.lvl].len*100)+'% van level '+(S.lvl+1)+'.</p><p>Opbrengst: $ '+sc+' mln. Record: $ '+hi+' mln.</p><p>Tip: een uitspraak is geen zeekaart. Houd de zee in de gaten.</p>','Opnieuw',()=>begin())}
function done(){S.run=false;const sc=Math.floor(S.score),h=Math.round(S.hull);
if(S.lvl<2)show('Level '+(S.lvl+1)+' gehaald','<p>Lading veilig door de straat. Romp: '+h+'%. Opbrengst: $ '+sc+' mln.</p><p>Je krijgt wat reparatie. Het volgende level is gevaarlijker.</p>','Volgend level',()=>begin(S.lvl+1,Math.min(100,S.hull+25),S.score));
else{if(sc>hi){hi=sc;try{localStorage.setItem('hh',hi)}catch(e){}}show('Olie afgeleverd','<p>Je bent door Hormuz. De Golf van Oman ligt voor je. Romp: '+h+'%.</p><p>Opbrengst: $ '+sc+' mln. Record: $ '+hi+' mln.</p>','Nog een keer',()=>begin())}}
function spawnMines(){const L=LV[S.lvl],n=1+(Math.random()<.3+.15*S.lvl)+(Math.random()<.15*S.lvl);
for(let i=0;i<n;i++){const y=-20-i*50,w=S.d+H-y;S.mines.push({x:Lx(w)+25+Math.random()*(Rx(w)-Lx(w)-50),y,ph:Math.random()*6})}}
function spawnBomb(){const L=LV[S.lvl],bx=clamp(S.px+(Math.random()-.5)*110,70,330),by=S.py-S.v*L.T+(Math.random()-.5)*50;
S.bombs.push({x:bx,y:by,T:L.T,t:L.T,R:52,boom:0,ox:bx<200?-10:W+10,oy:by-170});snd(880,.1,'square',.05)}
const K={};
addEventListener('keydown',e=>{const c=e.code;if(c=='Space'){if(!e.repeat)tb();e.preventDefault()}
if(/Arrow|Key[WASD]/.test(c)){K[c]=1;e.preventDefault()}});
addEventListener('keyup',e=>{delete K[e.code]});
let dr=null;
cv.addEventListener('pointerdown',e=>{dr={id:e.pointerId,x:e.clientX,y:e.clientY};cv.setPointerCapture(e.pointerId)});
cv.addEventListener('pointermove',e=>{if(!dr||dr.id!=e.pointerId||!S||!S.run)return;const k=W/cv.clientWidth;S.tx+=(e.clientX-dr.x)*k*1.25;S.ty+=(e.clientY-dr.y)*k*1.25;dr.x=e.clientX;dr.y=e.clientY});
['pointerup','pointercancel'].forEach(n=>cv.addEventListener(n,()=>{dr=null}));
function upd(dt){const s=S,L=LV[s.lvl];s.t+=dt;
const base=62+s.lvl*10;s.v+=((s.boost?base*1.9:base)-s.v)*Math.min(1,dt*1.6);const dd=s.v*dt;s.d+=dd;s.score+=dd*(s.boost?2:1)*.02;
const sg=Math.floor(s.d/SEG);if(sg!=s.seg){s.seg=sg;say()}
const sp=230;if(K.ArrowLeft||K.KeyA)s.tx-=sp*dt;if(K.ArrowRight||K.KeyD)s.tx+=sp*dt;if(K.ArrowUp||K.KeyW)s.ty-=sp*dt;if(K.ArrowDown||K.KeyS)s.ty+=sp*dt;
const bd=y=>{const w=s.d+H-y;return[Lx(w)+18,Rx(w)-18]};
s.ty=clamp(s.ty,330,520);let b=bd(s.ty);s.tx=clamp(s.tx,b[0],b[1]);
const k=1-Math.exp(-3.2*dt),ox=s.px;s.px+=(s.tx-s.px)*k;s.py+=(s.ty-s.py)*k;b=bd(s.py);s.px=clamp(s.px,b[0],b[1]);
s.ang+=(clamp((s.px-ox)/dt*.004,-.35,.35)-s.ang)*.12;
if(s.closed&&s.d>150){s.nm-=dd;s.nb-=dd;if(s.nm<=0){spawnMines();s.nm=L.mine*(.6+Math.random()*.8)}if(s.nb<=0){spawnBomb();s.nb=L.bomb*(.6+Math.random()*.8)}}
for(const m of s.mines){m.y+=dd;m.x+=Math.sin(s.t*1.5+m.ph)*10*dt;const w=s.d+H-m.y;m.x=clamp(m.x,Lx(w)+12,Rx(w)-12);
for(const q of[-26,0,26])if(Math.hypot(s.px-m.x,s.py+q-m.y)<24){hit(m.x,m.y,34);m.dead=1;break}}
s.mines=s.mines.filter(m=>!m.dead&&m.y<H+40);
for(const m of s.bombs){m.y+=dd;m.oy+=dd;if(m.t>0){m.t-=dt;if(m.t<=0){m.boom=.45;boom(m.x,m.y);for(const q of[-26,0,26])if(Math.hypot(s.px-m.x,s.py+q-m.y)<m.R){hit(m.x,m.y,26);break}}}else m.boom-=dt}
s.bombs=s.bombs.filter(m=>m.t>0||m.boom>0);
for(const p of s.parts){p.x+=p.vx*dt;p.y+=(p.vy+s.v)*dt;p.l-=dt}s.parts=s.parts.filter(p=>p.l>0);
s.shake=Math.max(0,s.shake-dt);s.flash=Math.max(0,s.flash-dt);
if(s.run&&s.d>=L.len)done()}
function land(sd,off,f,st){x.beginPath();x.moveTo(sd?W:0,-10);for(let y=-10;y<=H+10;y+=10){const w=S.d+H-y;x.lineTo(sd?Rx(w)+off:Lx(w)-off,y)}x.lineTo(sd?W:0,H+10);x.closePath();x.fillStyle=f;x.fill();if(st){x.strokeStyle='rgba(255,255,255,.45)';x.lineWidth=3;x.stroke()}}
function ship(){x.save();x.translate(S.px,S.py);x.rotate(S.ang);
x.fillStyle='rgba(255,255,255,.22)';x.beginPath();x.moveTo(-9,38);x.lineTo(9,38);x.lineTo(18+S.v*.06,50+S.v*.35);x.lineTo(-18-S.v*.06,50+S.v*.35);x.fill();
x.fillStyle='#7d2519';x.strokeStyle='#2a1410';x.lineWidth=1.5;x.beginPath();x.moveTo(0,-44);x.quadraticCurveTo(15,-26,14,-6);x.lineTo(14,34);x.quadraticCurveTo(14,40,8,40);x.lineTo(-8,40);x.quadraticCurveTo(-14,40,-14,34);x.lineTo(-14,-6);x.quadraticCurveTo(-15,-26,0,-44);x.fill();x.stroke();
x.fillStyle='#556270';x.fillRect(-10,-30,20,46);x.fillStyle='#8a96a3';for(let i=0;i<4;i++){x.beginPath();x.arc(0,-23+i*11,4.2,0,7);x.fill()}
x.fillStyle='#ece7d6';x.fillRect(-10,20,20,15);x.fillStyle='#264a5c';x.fillRect(-9,22,18,3);x.fillStyle='#d0402c';x.beginPath();x.arc(0,31,3,0,7);x.fill();x.restore()}
function draw(){x.setTransform(2,0,0,2,0,0);const s=S;x.save();if(s.shake>0)x.translate((Math.random()-.5)*s.shake*16,(Math.random()-.5)*s.shake*16);
x.fillStyle='#0d5c70';x.fillRect(-20,-20,W+40,H+40);x.strokeStyle='rgba(255,255,255,.1)';x.lineWidth=2;
for(let i=0;i<46;i++){const wx=(i*127.3)%W,wy=(((i*71.9+s.d)%H)+H)%H;x.beginPath();x.moveTo(wx,wy);x.quadraticCurveTo(wx+6,wy-4,wx+12,wy);x.stroke()}
for(const sd of[0,1]){land(sd,-16,'#1a7280');land(sd,0,'#cfb277',1);land(sd,26,'#a98a52')}
for(const m of s.bombs){const p=1-Math.max(m.t,0)/m.T;
if(m.t>0){x.strokeStyle='rgba(255,70,50,.9)';x.lineWidth=2;x.setLineDash([6,5]);x.beginPath();x.arc(m.x,m.y,m.R,0,7);x.stroke();x.setLineDash([]);x.fillStyle='rgba(255,70,50,'+(.12+.25*p)+')';x.beginPath();x.arc(m.x,m.y,m.R*p,0,7);x.fill();
x.beginPath();x.moveTo(m.x-m.R-6,m.y);x.lineTo(m.x+m.R+6,m.y);x.moveTo(m.x,m.y-m.R-6);x.lineTo(m.x,m.y+m.R+6);x.stroke()}}
for(const m of s.mines){x.save();x.translate(m.x,m.y+Math.sin(s.t*2+m.ph)*1.5);x.strokeStyle='rgba(255,255,255,.2)';x.lineWidth=2;x.beginPath();x.arc(0,0,16+Math.sin(s.t*2+m.ph)*2,0,7);x.stroke();
x.strokeStyle=x.fillStyle='#1f262c';x.lineWidth=3;x.lineCap='round';for(let i=0;i<8;i++){const a=i*.785;x.beginPath();x.moveTo(Math.cos(a)*8,Math.sin(a)*8);x.lineTo(Math.cos(a)*14,Math.sin(a)*14);x.stroke()}
x.beginPath();x.arc(0,0,9,0,7);x.fill();x.fillStyle=Math.sin(s.t*6+m.ph)>0?'#ff4a3a':'#5a1a14';x.beginPath();x.arc(0,0,2.6,0,7);x.fill();x.restore()}
ship();
for(const m of s.bombs){if(m.t>0){const p=1-m.t/m.T,q=Math.max(0,p-.3),mx=m.ox+(m.x-m.ox)*p,my=m.oy+(m.y-m.oy)*p;x.strokeStyle='rgba(255,170,60,.85)';x.lineWidth=3;x.beginPath();x.moveTo(m.ox+(m.x-m.ox)*q,m.oy+(m.y-m.oy)*q);x.lineTo(mx,my);x.stroke();x.fillStyle='#fff3b0';x.beginPath();x.arc(mx,my,3.5,0,7);x.fill()}
else if(m.boom>0){const p=1-m.boom/.45,r=m.R*(.5+.6*p);x.fillStyle='rgba(255,140,30,'+(1-p)*.85+')';x.beginPath();x.arc(m.x,m.y,r,0,7);x.fill();x.fillStyle='rgba(255,235,140,'+(1-p)*.9+')';x.beginPath();x.arc(m.x,m.y,r*.55,0,7);x.fill()}}
for(const p of s.parts){x.globalAlpha=clamp(p.l/p.m,0,1);x.fillStyle=p.c;x.beginPath();x.arc(p.x,p.y,p.r,0,7);x.fill()}x.globalAlpha=1;x.restore();
if(s.flash>0){x.fillStyle='rgba(220,40,30,'+s.flash*.9+')';x.fillRect(0,0,W,H)}
x.fillStyle='rgba(5,12,18,.75)';x.fillRect(0,H-46,W,46);x.font='700 13px "Barlow Condensed",system-ui,sans-serif';x.textAlign='left';x.fillStyle='#cfd8de';
x.fillText('Romp',12,H-30);x.fillText('Level '+(s.lvl+1)+'/3, '+Math.min(100,Math.floor(s.d/LV[s.lvl].len*100))+'%',130,H-30);
x.fillStyle='#25333d';x.fillRect(12,H-24,104,10);x.fillRect(130,H-24,104,10);
x.fillStyle=s.hull>50?'#3fbf7f':s.hull>25?'#e0a21a':'#e0483a';x.fillRect(12,H-24,104*s.hull/100,10);
x.fillStyle='#5bb7d6';x.fillRect(130,H-24,104*Math.min(1,s.d/LV[s.lvl].len),10);
x.textAlign='right';x.font='700 18px "Barlow Condensed",system-ui,sans-serif';x.lineWidth=3;x.strokeStyle='rgba(0,0,0,.55)';const tx='$ '+Math.floor(s.score)+' mln'+(s.boost?'  x2':'');x.strokeText(tx,W-10,104);x.fillStyle='#f3ecd8';x.fillText(tx,W-10,104)}
let last=0;function loop(ts){requestAnimationFrame(loop);const dt=Math.min((ts-last)/1000||0,.05);last=ts;if(S.run)upd(dt);else S.d+=40*dt;draw()}
function rs(){G.style.setProperty('--u',G.clientWidth/400+'px')}addEventListener('resize',rs);rs();
S=ns(0,100,0);requestAnimationFrame(loop);
show('Hormuz Tanker','<p>Jij vaart een olietanker door de Straat van Hormuz. Geen radio, geen radar: alleen de uitspraken van de President.</p><p>Zegt hij dat de straat open is? Dan kun je vol gas geven voor dubbele winst. Dicht? Dan liggen er zeemijnen en komen er raketten aan.</p><p>Pas op: wat hij zegt klopt niet altijd.</p><p><small>Sturen: sleep met je vinger, of pijltjes en WASD. Vol gas: knop rechtsonder of spatiebalk.</small></p><p><small>Satire. De uitspraken zijn verzonnen, geen echte citaten.'+(hi?' Record: $ '+hi+' mln.':'')+'</small></p>','Vaar uit',()=>begin());
</script></body></html>
