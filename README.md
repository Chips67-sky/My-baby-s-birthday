<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#210b13">
<title>for bernice ♡</title>
<style>
  :root{
    --bg:#16090f; --panel:#26121b; --wine:#7b263f; --rose:#e8a8b8;
    --cream:#fff1e7; --muted:#c9aeb6; --gold:#d8b887;
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{margin:0;background:radial-gradient(ellipse at top,#3a1425 0%,var(--bg) 58%);color:var(--cream);font-family:Georgia,'Times New Roman',serif;min-height:100vh;overflow-x:hidden}
  button{font:inherit;cursor:pointer}
  .grain{pointer-events:none;position:fixed;inset:0;opacity:.06;z-index:10;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.7'/%3E%3C/svg%3E")}
  .progress{position:fixed;top:0;left:0;height:3px;width:0;background:linear-gradient(90deg,var(--rose),var(--gold));z-index:20;transition:width .35s}
  .screen{min-height:100svh;display:none;align-items:center;justify-content:center;padding:32px 20px;position:relative;isolation:isolate}
  .screen.active{display:flex;animation:fadeIn .75s ease both}
  .wrap{width:min(760px,100%);text-align:center;position:relative}
  .eyebrow{letter-spacing:.26em;text-transform:uppercase;font:10px/1.8 Arial,sans-serif;color:var(--rose)}
  h1,h2{font-weight:normal;line-height:1.08;margin:16px 0}
  h1{font-size:clamp(44px,10vw,82px);letter-spacing:-.04em}
  h2{font-size:clamp(34px,7vw,58px)}
  p{font-size:clamp(16px,2.6vw,19px);line-height:1.8;color:#f1dfe2}
  .italic{font-style:italic;color:var(--rose)}
  .small{font:11px/1.8 Arial,sans-serif;color:var(--muted);letter-spacing:.05em}
  .btn{border:1px solid #b56a80;background:linear-gradient(135deg,#8b2d49,#572035);color:white;padding:14px 22px;border-radius:999px;box-shadow:0 8px 28px #0005;transition:transform .2s,filter .2s;letter-spacing:.04em}
  .btn:hover{transform:translateY(-3px);filter:brightness(1.15)}
  .btn.secondary{background:transparent;border-color:#69404e;color:var(--cream);box-shadow:none}
  .actions{display:flex;flex-wrap:wrap;gap:12px;justify-content:center;margin-top:28px}
  .heart{font-size:24px;color:var(--rose);animation:beat 1.6s infinite;display:inline-block}
  .orb{position:absolute;border:1px solid #b56a8030;border-radius:50%;width:260px;height:260px;z-index:-1;animation:float 9s ease-in-out infinite}
  .orb.one{top:12%;left:-120px}.orb.two{bottom:5%;right:-110px;width:180px;height:180px;animation-delay:-3s}
  .sparkles{position:absolute;inset:0;overflow:hidden;pointer-events:none;z-index:-1}
  .sparkles span{position:absolute;color:#d9a1b1;opacity:.55;animation:drift 12s linear infinite}
  .card{background:linear-gradient(145deg,#311724dd,#1b0b12ee);border:1px solid #8c4a5b66;border-radius:24px;padding:clamp(22px,5vw,42px);box-shadow:0 25px 90px #0005;text-align:left}
  .card p{font-size:16px}
  .letter{white-space:normal}
  .letter p{margin:0 0 17px}
  .photo-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px;margin:26px 0}
  .photo-slot{min-height:180px;border:1px dashed #b56a8077;border-radius:18px;display:flex;align-items:center;justify-content:center;padding:18px;text-align:center;background:linear-gradient(145deg,#4b2032,#211019);color:#dcb7c1;font:12px/1.7 Arial,sans-serif;overflow:hidden}
  .photo-slot img{width:100%;height:100%;min-height:180px;object-fit:cover;position:absolute;inset:0}
  .photo-slot{position:relative}
  .photo-slot span{position:relative;z-index:1}
  .reasons{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;margin-top:24px}
  .reason{border:1px solid #754053;background:#2c1420;color:var(--cream);border-radius:14px;padding:15px 12px;min-height:64px;transition:.25s}
  .reason:hover{background:#542136;transform:translateY(-2px)}
  .reason.revealed{border-color:var(--gold);color:var(--rose)}
  .reason-text{min-height:68px;color:var(--rose);font-style:italic}
  .final-seal{font-size:64px;animation:beat 1.6s infinite}
  .music-pill{position:fixed;right:14px;bottom:14px;z-index:30;background:#26121b;border:1px solid #754053;color:#f9dfe7;border-radius:999px;padding:10px 14px;font:12px Arial,sans-serif}
  .footer-note{margin-top:24px}
  @keyframes fadeIn{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
  @keyframes beat{0%,100%{transform:scale(1)}50%{transform:scale(1.12)}}
  @keyframes float{0%,100%{transform:translateY(0) rotate(0)}50%{transform:translateY(-24px) rotate(8deg)}}
  @keyframes drift{0%{transform:translateY(110vh) rotate(0);opacity:0}15%{opacity:.6}100%{transform:translateY(-20vh) rotate(300deg);opacity:0}}
  @media(max-width:520px){.photo-grid,.reasons{grid-template-columns:1fr 1fr}.photo-slot{min-height:140px}.card{padding:22px}.music-pill{bottom:10px;right:10px}}
  @media(prefers-reduced-motion:reduce){*,*::before,*::after{animation-duration:.01ms!important;transition-duration:.01ms!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<div class="grain"></div><div class="progress" id="progress"></div>
<div class="sparkles" id="sparkles"></div>
<button class="music-pill" id="musicBtn" onclick="toggleMusic()">♫ music: off</button>
<audio id="song" loop></audio>

<section class="screen active" id="s0">
  <div class="orb one"></div><div class="orb two"></div>
  <div class="wrap">
    <div class="eyebrow">a little something, just for you</div>
    <div class="heart" style="margin-top:28px">♡</div>
    <h1>for my<br><span class="italic">favourite girl.</span></h1>
    <p>made with love, for <strong>bernice ephraim imaobong</strong>.</p>
    <div class="actions"><button class="btn" onclick="go(1)">open your surprise ♡</button></div>
    <div class="small footer-note">best experienced with your sound on · take your time</div>
  </div>
</section>

<section class="screen" id="s1">
  <div class="wrap">
    <div class="eyebrow">chapter one · the birthday girl</div>
    <h2>happy sweet <span class="italic">sixteen.</span></h2>
    <p>today is about you. your smile, your laugh, your beautiful heart, and all the little things that make you <em>you</em>.</p>
    <p class="italic">and honestly? the world got a little luckier the day you were born.</p>
    <div class="actions"><button class="btn" onclick="go(2)">there's more…</button><button class="btn secondary" onclick="go(0)">back</button></div>
  </div>
</section>

<section class="screen" id="s2">
  <div class="wrap">
    <div class="eyebrow">chapter two · little memories</div>
    <h2>our little <span class="italic">corner.</span></h2>
    <p>these spaces are waiting for your favourite pictures together. tap a frame to choose a photo from your phone.</p>
    <div class="photo-grid">
      <label class="photo-slot"><input type="file" accept="image/*" hidden onchange="addPhoto(this)"><span>＋ add a favourite photo</span></label>
      <label class="photo-slot"><input type="file" accept="image/*" hidden onchange="addPhoto(this)"><span>＋ a silly memory</span></label>
      <label class="photo-slot"><input type="file" accept="image/*" hidden onchange="addPhoto(this)"><span>＋ your prettiest picture</span></label>
      <label class="photo-slot"><input type="file" accept="image/*" hidden onchange="addPhoto(this)"><span>＋ one just because</span></label>
    </div>
    <div class="small">photos you choose show on your device; add the actual photos to the site folder before publishing if you want her to see them too.</div>
    <div class="actions"><button class="btn" onclick="go(3)">next, pretty girl</button><button class="btn secondary" onclick="go(1)">back</button></div>
  </div>
</section>

<section class="screen" id="s3">
  <div class="wrap">
    <div class="eyebrow">chapter three · a tiny game</div>
    <h2>reasons i love <span class="italic">you.</span></h2>
    <p>tap the little cards. each one has a reason waiting underneath it.</p>
    <div class="reasons" id="reasons"></div>
    <p class="reason-text" id="reasonText">choose one, babyyy ♡</p>
    <div class="actions"><button class="btn" onclick="go(4)">okay, one last thing…</button><button class="btn secondary" onclick="go(2)">back</button></div>
  </div>
</section>

<section class="screen" id="s4">
  <div class="wrap">
    <div class="eyebrow">chapter four · from my heart</div>
    <h2>a letter for <span class="italic">you.</span></h2>
    <div class="card letter">
      <p>happy birthdayyyy to my babyyyy, my pretty girl, my favourite personnn ❤️. happy sweet sixteen to you, bernice ephraim imaobonggg.</p>
      <p>omggg babyyy, you're actually 16 nowww, and i genuinely can't explain how happy i am to celebrate you today. sometimes i actually think about how you're literally my first girlfriend and my childhood crush, and it's crazy to me how the little girl i used to have a crush on is now the girl i get to call mine. like how did i get this lucky honestly?</p>
      <p>you're genuinely one of the best things that has ever happened to me, and i'm so grateful to have you in my life. you're so beautiful, babyyy, and i genuinely don't think you understand just how beautiful you are. you're actually so gorgeous, and i don't think i'll ever get tired of telling you that.</p>
      <p>but it's not even just about your beauty, it's literally everything about you. your personality, your smile, your humour, the way you make me laugh, and how much i enjoy your presence. you're genuinely one of the funniest people i've ever met, and i love how you can make me happy without even trying. i could literally spend hours talking to you and still want more time with you.</p>
      <p>thank you for always being there for me, for encouraging me, for listening to me and for being someone who makes things feel a little better when life gets overwhelming. you probably don't even realise how much some of the things you do mean to me, but i appreciate you more than i can explain.</p>
      <p>you're my first girlfriend, my first crush, and someone i've grown to love more than i ever thought i could. i love you unconditionally, babyyy, and i hope i can keep showing you just how much you mean to me, not just today but every other day too. i want to see you happy, i want to see you achieve everything you dream of, and i want to be there cheering you on.</p>
      <p>as you turn 16, i pray that God blesses you with happiness, peace, good health, success and so many reasons to smile. i pray that this new age brings you beautiful memories, wonderful opportunities and everything your heart desires. you deserve so much love and happiness, and i hope life gives you plenty of both.</p>
      <p>honestly, i could keep writing about you because there's just so much i love about you, but i don't even think words could ever fully explain it. you're so special to me, bernice, and having you in my life is something i'll always be grateful for. i still find it crazy that my childhood crush became my girlfriend, and if i had to do it all over again, i'd still choose you.</p>
      <p>happy birthday once again, my love. i love you sooooo much, more than these words could ever explain, and i hope your 16th year is filled with all the happiness you deserve. keep being you, keep smiling, keep making me laugh and never forget just how beautiful you are, inside and out.</p>
      <p class="italic" style="text-align:right">always your boy ♡</p>
    </div>
    <div class="actions"><button class="btn" onclick="go(5)">wait… there's a final surprise</button><button class="btn secondary" onclick="go(3)">back</button></div>
  </div>
</section>

<section class="screen" id="s5">
  <div class="wrap">
    <div class="eyebrow">one last thing · just for you</div>
    <div class="final-seal">♡</div>
    <h2>if i could go back…</h2>
    <p>to when we were younger, before all of this, when you were just the girl i had a crush on…</p>
    <h2 class="italic">i'd still want it to be you.</h2>
    <p>happy birthday, my pretty girl. here's to you, to us, and to all the memories we haven't made yet.</p>
    <div class="actions"><button class="btn" onclick="confetti(); this.textContent='i love you, bernice ♡'">one more hug? ♡</button><button class="btn secondary" onclick="go(0)">start again</button></div>
    <div class="small footer-note">made with love · just for bernice</div>
  </div>
</section>

<script>
const reasons = [
  ["your beauty","because you're genuinely so, so pretty and i could look at you all day."],
  ["your smile","because seeing you smile makes me happy in a way i can't explain."],
  ["your humour","because you make me laugh even when you aren't trying."],
  ["your heart","because you care, you listen, and you show up for me."],
  ["your energy","because being around you is one of my favourite things."],
  ["your encouragement","because you remind me i can keep going when things get hard."],
  ["our story","because my childhood crush becoming my girlfriend still feels unreal."],
  ["just you","because i don't need one big reason. i love you for being you."]
];
const reasonsEl=document.getElementById('reasons');
reasons.forEach(([title,body])=>{
  const b=document.createElement('button'); b.className='reason'; b.textContent=title+' ♡';
  b.onclick=()=>{document.querySelectorAll('.reason').forEach(x=>x.classList.remove('revealed'));b.classList.add('revealed');document.getElementById('reasonText').textContent=body;};
  reasonsEl.appendChild(b);
});
function go(n){
  document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
  document.getElementById('s'+n).classList.add('active');
  document.getElementById('progress').style.width=((n/5)*100)+'%';
  window.scrollTo({top:0,behavior:'smooth'});
}
function addPhoto(input){
  const label=input.parentElement, file=input.files&&input.files[0]; if(!file)return;
  const old=label.querySelector('img');if(old)old.remove();
  const img=document.createElement('img');img.src=URL.createObjectURL(file);label.appendChild(img);
  const span=label.querySelector('span');if(span)span.textContent='photo selected ✓';
}
function toggleMusic(){
  const audio=document.getElementById('song'),btn=document.getElementById('musicBtn');
  if(!audio.src){alert('To add music: put a song file in the same folder as this HTML, then open this file in a text editor and replace the audio tag with: <audio id="song" loop src="your-song.mp3"></audio>');return;}
  if(audio.paused){audio.play();btn.textContent='♫ music: on';}else{audio.pause();btn.textContent='♫ music: off';}
}
const sparkle=document.getElementById('sparkles');
for(let i=0;i<24;i++){const s=document.createElement('span');s.textContent=['✧','·','♡','✦'][i%4];s.style.left=Math.random()*100+'%';s.style.animationDelay=(-Math.random()*12)+'s';s.style.animationDuration=(8+Math.random()*10)+'s';s.style.fontSize=(10+Math.random()*16)+'px';sparkle.appendChild(s);}
function confetti(){
  for(let i=0;i<65;i++){
    const e=document.createElement('span');e.textContent=['♡','✦','✧','♥'][Math.floor(Math.random()*4)];
    e.style.cssText=`position:fixed;z-index:99;left:${Math.random()*100}vw;top:-25px;color:${['#e8a8b8','#d8b887','#fff1e7'][i%3]};font-size:${12+Math.random()*20}px;pointer-events:none;transition:transform ${2+Math.random()*2}s ease,opacity 3s`;
    document.body.appendChild(e);requestAnimationFrame(()=>{e.style.transform=`translateY(${window.innerHeight+80}px) rotate(${Math.random()*500}deg)`;e.style.opacity='0';});setTimeout(()=>e.remove(),4200);
  }
}
</script>
</body>
</html> 
<img src="Snapchat-1004003003.jpg"
     alt="My favourite picture of Bernice">
     <img src="Snapchat-305400593_074928.jpg"
     alt="My most silliest picture of Bernice">
     <img src="Snapchat-694527159.jpg"
     alt="the one I love the most">
<section id="reasons">
  <h2>little things i love about you ♡</h2>

  <button onclick="showReason('smile')">your smile</button>
  <button onclick="showReason('beauty')">your beauty</button>
  <button onclick="showReason('humour')">your humour</button>
  <button onclick="showReason('heart')">your heart</button>
  <button onclick="showReason('story')">our story</button>

  <p id="reason-message">tap one, pretty girl ♡</p>
</section>

<script>
function showReason(reason) {
  const messages = {
    smile: "i love seeing you smile, babyyy. seeing you happy makes me happy too.",
    beauty: "you're genuinely so beautiful, bernice. i don't think i'll ever get tired of telling you that.",
    humour: "you're so funny and unserious sometimes, and i love how you can make me happy without even trying.",
    heart: "thank you for always being there for me, encouraging me and making things feel a little better missyyy.",
    story: "my childhood crush becoming my first girlfriend still feels incredible. if i could go back, i'd still choose you missy."
  };

  document.getElementById("reason-message").textContent =
    messages[reason];
}
</script><!-- ==========================================
     BERNICE'S FINAL BIRTHDAY SURPRISE 💗
=========================================== -->

<style>
#bernice-final-surprise {
    font-family: Georgia, "Times New Roman", serif;
    text-align: center;
    padding: 65px 18px;
    margin: 35px auto;
    max-width: 750px;
    color: #fff;
    background: linear-gradient(145deg, #260c20, #551a39, #24102c);
    border-radius: 25px;
    overflow: hidden;
    box-sizing: border-box;
}

#bernice-final-surprise * {
    box-sizing: border-box;
}

#bernice-final-surprise .surprise-label {
    color: #ffb9d5;
    letter-spacing: 3px;
    font-size: 12px;
    text-transform: uppercase;
}

#bernice-final-surprise .surprise-title {
    font-size: clamp(25px, 6vw, 38px);
    line-height: 1.3;
    margin: 15px 0;
}

#bernice-final-surprise .surprise-intro {
    color: #f8dce9;
    font-size: 15px;
    line-height: 1.8;
    margin: 0 auto 30px;
    max-width: 450px;
}

#bernice-final-surprise .envelope-button {
    position: relative;
    display: block;
    width: min(280px, 90%);
    height: 175px;
    margin: 35px auto 25px;
    border: none;
    background: transparent;
    cursor: pointer;
    perspective: 700px;
    animation: berniceFloat 3s ease-in-out infinite;
    -webkit-tap-highlight-color: transparent;
}

#bernice-final-surprise .envelope-body {
    position: absolute;
    inset: 25px 0 0;
    background: linear-gradient(135deg, #ffb5cd, #f36e9f);
    border-radius: 8px;
    box-shadow: 0 12px 30px #0005;
    overflow: hidden;
}

#bernice-final-surprise .envelope-body::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(
        135deg,
        transparent 49.5%,
        #e75c91 50%
    );
    clip-path: polygon(0 0, 100% 0, 50% 70%);
}

#bernice-final-surprise .envelope-flap {
    position: absolute;
    top: 25px;
    left: 0;
    width: 100%;
    height: 100px;
    background: #ffcee0;
    clip-path: polygon(0 0, 100% 0, 50% 100%);
    transform-origin: top center;
    transition: transform 0.7s ease;
    z-index: 3;
}

#bernice-final-surprise .envelope-heart {
    position: absolute;
    z-index: 5;
    top: 79px;
    left: 50%;
    transform: translateX(-50%);
    width: 49px;
    height: 49px;
    border-radius: 50%;
    background: #a70e48;
    border: 2px solid #ffecf4;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 27px;
    box-shadow: 0 4px 12px #0003;
    transition: transform 0.3s ease, opacity 0.3s ease;
}

#bernice-final-surprise .envelope-button:active
.envelope-heart {
    transform: translateX(-50%) scale(0.9);
}

#bernice-final-surprise .envelope-name {
    position: absolute;
    bottom: 12px;
    left: 0;
    width: 100%;
    color: #7c1743;
    font-size: 15px;
    font-weight: bold;
    letter-spacing: 1px;
    z-index: 2;
}

#bernice-final-surprise .envelope-button.is-open {
    animation: none;
}

#bernice-final-surprise .envelope-button.is-open
.envelope-flap {
    transform: rotateX(180deg);
}

#bernice-final-surprise .envelope-button.is-open
.envelope-heart {
    opacity: 0;
    pointer-events: none;
}

#bernice-final-surprise .tap-instruction {
    font-size: 13px;
    color: #ffd3e5;
    animation: bernicePulse 2s infinite;
}

#bernice-final-surprise .love-letter {
    display: none;
    text-align: left;
    max-width: 620px;
    margin: 35px auto 0;
    padding: clamp(22px, 5vw, 40px);
    color: #59233d;
    background: #fff8fc;
    border: 1px solid #f7d3e2;
    border-radius: 5px;
    box-shadow: 0 12px 40px #0004;
    line-height: 1.95;
    font-size: 15px;
    animation: berniceLetterReveal 0.8s ease both;
}

#bernice-final-surprise .love-letter.visible {
    display: block;
}

#bernice-final-surprise .letter-top {
    text-align: center;
    color: #c13e76;
    font-size: 12px;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 20px;
}

#bernice-final-surprise .letter-heading {
    text-align: center;
    font-size: clamp(23px, 5vw, 32px);
    line-height: 1.4;
    color: #a32359;
    margin: 10px 0 25px;
}

#bernice-final-surprise .letter-paragraph {
    margin: 0 0 20px;
    overflow-wrap: anywhere;
}

#bernice-final-surprise .letter-ending {
    text-align: center;
    font-weight: bold;
    font-size: 18px;
    line-height: 1.8;
    color: #c12c6b;
    margin-top: 30px;
}

#bernice-final-surprise .close-letter {
    display: block;
    margin: 28px auto 0;
    padding: 12px 24px;
    background: #b52c68;
    color: white;
    border: none;
    border-radius: 25px;
    font-size: 14px;
    cursor: pointer;
}

#bernice-final-surprise .close-letter:hover {
    background: #8e194d;
}

@keyframes berniceFloat {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-9px);
    }
}

@keyframes bernicePulse {
    0%, 100% {
        opacity: 1;
    }
    50% {
        opacity: 0.55;
    }
}

@keyframes berniceLetterReveal {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@media (prefers-reduced-motion: reduce) {
    #bernice-final-surprise .envelope-button,
    #bernice-final-surprise .tap-instruction {
        animation: none;
    }

    #bernice-final-surprise .love-letter,
    #bernice-final-surprise .envelope-flap,
    #bernice-final-surprise .envelope-heart {
        animation: none;
        transition-duration: 0.01ms;
    }
}
</style>

<section id="bernice-final-surprise">

    <div class="surprise-label">A little something from my heart</div>

    <h2 class="surprise-title">
        One Last Surprise For You, My Love 💗
    </h2>

    <p class="surprise-intro">
        I've saved something special just for you, Bernice.
        A little letter filled with words from my heart.
        Tap the heart to open it, pretty girl. 💌
    </p>

    <button
        type="button"
        class="envelope-button"
        id="berniceEnvelope"
        aria-label="Open your birthday love letter"
        aria-expanded="false"
        aria-controls="berniceLoveLetter"
    >
        <span class="envelope-body">
            <span class="envelope-name">
                For Bernice, With Love ♡
            </span>
        </span>

        <span class="envelope-flap"></span>

        <span class="envelope-heart" aria-hidden="true">
            ♥
        </span>
    </button>

    <p class="tap-instruction" id="berniceTapText">
        ♡ Tap the heart to open your letter ♡
    </p>

    <article
        class="love-letter"
        id="berniceLoveLetter"
        aria-label="Your birthday love letter"
        aria-hidden="true"
        inert
    >
        <div class="letter-top">
            Written with love, just for you 💗
        </div>

        <h3 class="letter-heading">
            To My Pretty Girl, Bernice 🥹💖
        </h3>

        <p class="letter-paragraph">
            Happyyy birthdayyyy to my babyyyy, my pretty girl,
            my favourite personnn 😁💗. Happy sweet sixteen to you,
            Bernice Ephraim Imaobonggg. omggg babyyy, you're actually
            16 nowww, and i genuinely can't explain how happy i am
            to celebrate you today. sometimes i actually think about
            how you're literally my first girlfriend AND my childhood
            crush, and it's crazy to me how the little girl i used
            to have a crush on is now the girl i get to call mine.
            like how did i get this lucky honestly 😭❤️. you're
            genuinely one of the best things that has ever happened
            to me, and i'm so grateful to have you in my life.
            you're so beautiful, babyyy, and i genuinely don't think
            you understand just HOW BEAUTIFUL YOU ARE🫠💗💗💖.
            like babyyy😔✌🏽, how are you this pretty???? you're
            actually so gorgeous, and i don't think i'll ever get
            tired of telling you that because omgoshhhh😭 LOOK AT
            YOUUU. But it's not even just about your beauty, it's
            literally everything about you. your personality, your
            smile, your humour, the way you make me laugh, and how
            much i enjoy your presence. you're genuinely one of the
            funniest people i've ever met, and i love how you can
            make me happy without even trying.
        </p>

        <p class="letter-paragraph">
            I could literally spend hours talking to you and still
            want more time with you because being around you is
            something i enjoy so much. even the simplest moments
            with you mean a lot to me, and i hope you know that.
            thank you for always being there for me, for encouraging
            me, for listening to me and for being someone who makes
            things feel a little better when life gets overwhelming.
            you probably don't even realise how much some of the
            things you do mean to me, but i appreciate you more than
            i can explain. i love having you around, and i'm genuinely
            so happy that i get to experience this kind of love with
            you. you're my first girlfriend, my first crush, and
            someone i've grown to love more than i ever thought i
            could. i love you unconditionally, babyyy, and i hope
            i can keep showing you just how much you mean to me,
            not just today but every other day too. i want to see
            you happy, i want to see you achieve everything you dream
            of, and i want to be there cheering you on through all
            the beautiful things life has waiting for you.
        </p>

        <p class="letter-paragraph">
            as you turn 16 today, i pray that God blesses you with
            happiness, peace, good health, success and so many reasons
            to smile. I pray that this new age brings you beautiful
            memories, wonderful opportunities and everything your
            heart desires. you deserve so much love and happiness,
            and i hope life gives you plenty of both. i hope you
            never lose that beautiful smile of yours or that funny,
            amazing personality i adore so much. and whenever you
            have days when you don't feel your best, i hope you
            remember that you're loved, appreciated and so much more
            amazing than you realise.
        </p>

        <p class="letter-paragraph">
            honestly, i could keep writing about you because there's
            just so much i love about you, but i don't even think
            words could ever fully explain it. you're so special to
            me, bernice, and having you in my life is something i'll
            always be grateful for. i still find it crazy that my
            childhood crush became my girlfriend, and if i had to
            do it all over again, i'd still choose you. you're my
            pretty girl, my favourite person and one of the sweetest
            things that has ever happened to me. i hope your birthday
            is as beautiful as you are, even though i don't think
            anything could possibly compete with that face of yours
            😭❤️. happy birthday once again, my love. i love you
            sooooo much, more than these words could ever explain,
            and i hope your 16th year is filled with all the happiness
            you deserve. keep being you, keep smiling, keep making me
            laugh and never forget just how beautiful you are, inside
            and out. i love you endlessly, my babyyyy.
        </p>

        <div class="letter-ending">
            Happy sweet sixteen Berniceeee🥹💖💖💗
            <br><br>
            I love you endlessly, my babyyyy. ❤️
        </div>

        <button
            type="button"
            class="close-letter"
            id="berniceCloseLetter"
        >
            Fold my letter back up 💌
        </button>
    </article>

</section>

<script>
(function () {
    const envelope = document.getElementById("berniceEnvelope");
    const letter = document.getElementById("berniceLoveLetter");
    const tapText = document.getElementById("berniceTapText");
    const closeButton = document.getElementById("berniceCloseLetter");

    if (!envelope || !letter || !tapText || !closeButton) {
        return;
    }

    function openLetter() {
        envelope.classList.add("is-open");
        letter.classList.add("visible");

        letter.removeAttribute("inert");
        letter.setAttribute("aria-hidden", "false");

        envelope.setAttribute("aria-expanded", "true");
        tapText.textContent = "♡ A little piece of my heart, just for you ♡";

        window.setTimeout(function () {
            letter.scrollIntoView({
                behavior: "smooth",
                block: "start"
            });
        }, 250);
    }

    function closeLetter() {
        letter.classList.remove("visible");
        letter.setAttribute("inert", "");
        letter.setAttribute("aria-hidden", "true");

        envelope.classList.remove("is-open");
        envelope.setAttribute("aria-expanded", "false");

        tapText.textContent = "♡ Tap the heart to open your letter ♡";

        envelope.scrollIntoView({
            behavior: "smooth",
            block: "center"
        });
    }

    envelope.addEventListener("click", function () {
        if (letter.classList.contains("visible")) {
            closeLetter();
        } else {
            openLetter();
        }
    });

    closeButton.addEventListener("click", closeLetter);
})();
</script><!-- ==========================================
     BERNICE'S FINAL BIRTHDAY SURPRISE 💗
=========================================== -->

<style>
#bernice-final-surprise {
    font-family: Georgia, "Times New Roman", serif;
    text-align: center;
    padding: 65px 18px;
    margin: 35px auto;
    max-width: 750px;
    color: #fff;
    background: linear-gradient(145deg, #260c20, #551a39, #24102c);
    border-radius: 25px;
    overflow: hidden;
    box-sizing: border-box;
}

#bernice-final-surprise * {
    box-sizing: border-box;
}

#bernice-final-surprise .surprise-label {
    color: #ffb9d5;
    letter-spacing: 3px;
    font-size: 12px;
    text-transform: uppercase;
}

#bernice-final-surprise .surprise-title {
    font-size: clamp(25px, 6vw, 38px);
    line-height: 1.3;
    margin: 15px 0;
}

#bernice-final-surprise .surprise-intro {
    color: #f8dce9;
    font-size: 15px;
    line-height: 1.8;
    margin: 0 auto 30px;
    max-width: 450px;
}

#bernice-final-surprise .envelope-button {
    position: relative;
    display: block;
    width: min(280px, 90%);
    height: 175px;
    margin: 35px auto 25px;
    border: none;
    background: transparent;
    cursor: pointer;
    perspective: 700px;
    animation: berniceFloat 3s ease-in-out infinite;
    -webkit-tap-highlight-color: transparent;
}

#bernice-final-surprise .envelope-body {
    position: absolute;
    inset: 25px 0 0;
    background: linear-gradient(135deg, #ffb5cd, #f36e9f);
    border-radius: 8px;
    box-shadow: 0 12px 30px #0005;
    overflow: hidden;
}

#bernice-final-surprise .envelope-body::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(
        135deg,
        transparent 49.5%,
        #e75c91 50%
    );
    clip-path: polygon(0 0, 100% 0, 50% 70%);
}

#bernice-final-surprise .envelope-flap {
    position: absolute;
    top: 25px;
    left: 0;
    width: 100%;
    height: 100px;
    background: #ffcee0;
    clip-path: polygon(0 0, 100% 0, 50% 100%);
    transform-origin: top center;
    transition: transform 0.7s ease;
    z-index: 3;
}

#bernice-final-surprise .envelope-heart {
    position: absolute;
    z-index: 5;
    top: 79px;
    left: 50%;
    transform: translateX(-50%);
    width: 49px;
    height: 49px;
    border-radius: 50%;
    background: #a70e48;
    border: 2px solid #ffecf4;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 27px;
    box-shadow: 0 4px 12px #0003;
    transition: transform 0.3s ease, opacity 0.3s ease;
}

#bernice-final-surprise .envelope-button:active
.envelope-heart {
    transform: translateX(-50%) scale(0.9);
}

#bernice-final-surprise .envelope-name {
    position: absolute;
    bottom: 12px;
    left: 0;
    width: 100%;
    color: #7c1743;
    font-size: 15px;
    font-weight: bold;
    letter-spacing: 1px;
    z-index: 2;
}

#bernice-final-surprise .envelope-button.is-open {
    animation: none;
}

#bernice-final-surprise .envelope-button.is-open
.envelope-flap {
    transform: rotateX(180deg);
}

#bernice-final-surprise .envelope-button.is-open
.envelope-heart {
    opacity: 0;
    pointer-events: none;
}

#bernice-final-surprise .tap-instruction {
    font-size: 13px;
    color: #ffd3e5;
    animation: bernicePulse 2s infinite;
}

#bernice-final-surprise .love-letter {
    display: none;
    text-align: left;
    max-width: 620px;
    margin: 35px auto 0;
    padding: clamp(22px, 5vw, 40px);
    color: #59233d;
    background: #fff8fc;
    border: 1px solid #f7d3e2;
    border-radius: 5px;
    box-shadow: 0 12px 40px #0004;
    line-height: 1.95;
    font-size: 15px;
    animation: berniceLetterReveal 0.8s ease both;
}

#bernice-final-surprise .love-letter.visible {
    display: block;
}

#bernice-final-surprise .letter-top {
    text-align: center;
    color: #c13e76;
    font-size: 12px;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 20px;
}

#bernice-final-surprise .letter-heading {
    text-align: center;
    font-size: clamp(23px, 5vw, 32px);
    line-height: 1.4;
    color: #a32359;
    margin: 10px 0 25px;
}

#bernice-final-surprise .letter-paragraph {
    margin: 0 0 20px;
    overflow-wrap: anywhere;
}

#bernice-final-surprise .letter-ending {
    text-align: center;
    font-weight: bold;
    font-size: 18px;
    line-height: 1.8;
    color: #c12c6b;
    margin-top: 30px;
}

#bernice-final-surprise .close-letter {
    display: block;
    margin: 28px auto 0;
    padding: 12px 24px;
    background: #b52c68;
    color: white;
    border: none;
    border-radius: 25px;
    font-size: 14px;
    cursor: pointer;
}

#bernice-final-surprise .close-letter:hover {
    background: #8e194d;
}

@keyframes berniceFloat {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-9px);
    }
}

@keyframes bernicePulse {
    0%, 100% {
        opacity: 1;
    }
    50% {
        opacity: 0.55;
    }
}

@keyframes berniceLetterReveal {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@media (prefers-reduced-motion: reduce) {
    #bernice-final-surprise .envelope-button,
    #bernice-final-surprise .tap-instruction {
        animation: none;
    }

    #bernice-final-surprise .love-letter,
    #bernice-final-surprise .envelope-flap,
    #bernice-final-surprise .envelope-heart {
        animation: none;
        transition-duration: 0.01ms;
    }
}
</style>

<section id="bernice-final-surprise">

    <div class="surprise-label">A little something from my heart</div>

    <h2 class="surprise-title">
        One Last Surprise For You, My Love 💗
    </h2>

    <p class="surprise-intro">
        I've saved something special just for you, Bernice.
        A little letter filled with words from my heart.
        Tap the heart to open it, pretty girl. 💌
    </p>

    <button
        type="button"
        class="envelope-button"
        id="berniceEnvelope"
        aria-label="Open your birthday love letter"
        aria-expanded="false"
        aria-controls="berniceLoveLetter"
    >
        <span class="envelope-body">
            <span class="envelope-name">
                For Bernice, With Love ♡
            </span>
        </span>

        <span class="envelope-flap"></span>

        <span class="envelope-heart" aria-hidden="true">
            ♥
        </span>
    </button>

    <p class="tap-instruction" id="berniceTapText">
        ♡ Tap the heart to open your letter ♡
    </p>

    <article
        class="love-letter"
        id="berniceLoveLetter"
        aria-label="Your birthday love letter"
        aria-hidden="true"
        inert
    >
        <div class="letter-top">
            Written with love, just for you 💗
        </div>

        <h3 class="letter-heading">
            To My Pretty Girl, Bernice 🥹💖
        </h3>

        <p class="letter-paragraph">
            Happyyy birthdayyyy to my babyyyy, my pretty girl,
            my favourite personnn 😁💗. Happy sweet sixteen to you,
            Bernice Ephraim Imaobonggg. omggg babyyy, you're actually
            16 nowww, and i genuinely can't explain how happy i am
            to celebrate you today. sometimes i actually think about
            how you're literally my first girlfriend AND my childhood
            crush, and it's crazy to me how the little girl i used
            to have a crush on is now the girl i get to call mine.
            like how did i get this lucky honestly 😭❤️. you're
            genuinely one of the best things that has ever happened
            to me, and i'm so grateful to have you in my life.
            you're so beautiful, babyyy, and i genuinely don't think
            you understand just HOW BEAUTIFUL YOU ARE🫠💗💗💖.
            like babyyy😔✌🏽, how are you this pretty???? you're
            actually so gorgeous, and i don't think i'll ever get
            tired of telling you that because omgoshhhh😭 LOOK AT
            YOUUU. But it's not even just about your beauty, it's
            literally everything about you. your personality, your
            smile, your humour, the way you make me laugh, and how
            much i enjoy your presence. you're genuinely one of the
            funniest people i've ever met, and i love how you can
            make me happy without even trying.
        </p>

        <p class="letter-paragraph">
            I could literally spend hours talking to you and still
            want more time with you because being around you is
            something i enjoy so much. even the simplest moments
            with you mean a lot to me, and i hope you know that.
            thank you for always being there for me, for encouraging
            me, for listening to me and for being someone who makes
            things feel a little better when life gets overwhelming.
            you probably don't even realise how much some of the
            things you do mean to me, but i appreciate you more than
            i can explain. i love having you around, and i'm genuinely
            so happy that i get to experience this kind of love with
            you. you're my first girlfriend, my first crush, and
            someone i've grown to love more than i ever thought i
            could. i love you unconditionally, babyyy, and i hope
            i can keep showing you just how much you mean to me,
            not just today but every other day too. i want to see
            you happy, i want to see you achieve everything you dream
            of, and i want to be there cheering you on through all
            the beautiful things life has waiting for you.
        </p>

        <p class="letter-paragraph">
            as you turn 16 today, i pray that God blesses you with
            happiness, peace, good health, success and so many reasons
            to smile. I pray that this new age brings you beautiful
            memories, wonderful opportunities and everything your
            heart desires. you deserve so much love and happiness,
            and i hope life gives you plenty of both. i hope you
            never lose that beautiful smile of yours or that funny,
            amazing personality i adore so much. and whenever you
            have days when you don't feel your best, i hope you
            remember that you're loved, appreciated and so much more
            amazing than you realise.
        </p>

        <p class="letter-paragraph">
            honestly, i could keep writing about you because there's
            just so much i love about you, but i don't even think
            words could ever fully explain it. you're so special to
            me, bernice, and having you in my life is something i'll
            always be grateful for. i still find it crazy that my
            childhood crush became my girlfriend, and if i had to
            do it all over again, i'd still choose you. you're my
            pretty girl, my favourite person and one of the sweetest
            things that has ever happened to me. i hope your birthday
            is as beautiful as you are, even though i don't think
            anything could possibly compete with that face of yours
            😭❤️. happy birthday once again, my love. i love you
            sooooo much, more than these words could ever explain,
            and i hope your 16th year is filled with all the happiness
            you deserve. keep being you, keep smiling, keep making me
            laugh and never forget just how beautiful you are, inside
            and out. i love you endlessly, my babyyyy.
        </p>

        <div class="letter-ending">
            Happy sweet sixteen Berniceeee🥹💖💖💗
            <br><br>
            I love you endlessly, my babyyyy. ❤️
        </div>

        <button
            type="button"
            class="close-letter"
            id="berniceCloseLetter"
        >
            Fold my letter back up 💌
        </button>
    </article>

</section>

<script>
(function () {
    const envelope = document.getElementById("berniceEnvelope");
    const letter = document.getElementById("berniceLoveLetter");
    const tapText = document.getElementById("berniceTapText");
    const closeButton = document.getElementById("berniceCloseLetter");

    if (!envelope || !letter || !tapText || !closeButton) {
        return;
    }

    function openLetter() {
        envelope.classList.add("is-open");
        letter.classList.add("visible");

        letter.removeAttribute("inert");
        letter.setAttribute("aria-hidden", "false");

        envelope.setAttribute("aria-expanded", "true");
        tapText.textContent = "♡ A little piece of my heart, just for you ♡";

        window.setTimeout(function () {
            letter.scrollIntoView({
                behavior: "smooth",
                block: "start"
            });
        }, 250);
    }

    function closeLetter() {
        letter.classList.remove("visible");
        letter.setAttribute("inert", "");
        letter.setAttribute("aria-hidden", "true");

        envelope.classList.remove("is-open");
        envelope.setAttribute("aria-expanded", "false");

        tapText.textContent = "♡ Tap the heart to open your letter ♡";

        envelope.scrollIntoView({
            behavior: "smooth",
            block: "center"
        });
    }

    envelope.addEventListener("click", function () {
        if (letter.classList.contains("visible")) {
            closeLetter();
        } else {
            openLetter();
        }
    });

    closeButton.addEventListener("click", closeLetter);
})();
</script>
