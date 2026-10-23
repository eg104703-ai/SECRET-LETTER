
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#650d2c">
<title>Something I Want to Tell You ❤️</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}

body{
  min-height:100vh;
  font-family:Georgia,serif;
  background:radial-gradient(circle at top,#9b244b,#41091e 65%,#20040e);
  color:#fff2f6;
  overflow-x:hidden;
}

#hearts{position:fixed;inset:0;pointer-events:none;overflow:hidden}

main{
  min-height:100svh;
  display:grid;
  place-items:center;
  padding:24px 15px;
  position:relative;
}

.card{
  width:100%;
  max-width:440px;
  text-align:center;
  padding:34px 24px;
  border:1px solid #ffffff30;
  border-radius:28px;
  background:#ffffff0d;
  backdrop-filter:blur(15px);
  box-shadow:0 20px 65px #0005;
  animation:appear 1s ease;
}

.top{
  font:11px Arial,sans-serif;
  letter-spacing:4px;
  color:#ffb4cc;
  text-transform:uppercase;
}

.bigheart{
  font-size:65px;
  margin:25px 0;
  animation:beat 1.4s infinite;
}

h1{
  font-size:clamp(30px,8vw,42px);
  line-height:1.2;
  margin-bottom:18px;
}

h1 span{color:#ff9fbd;font-style:italic}

p{
  font-size:15px;
  line-height:1.9;
  color:#f6d9e3;
}

button{
  width:100%;
  padding:15px;
  margin-top:20px;
  border:1px solid #ffc1d4;
  border-radius:50px;
  background:linear-gradient(100deg,#b20e46,#f04e83);
  color:white;
  font-size:15px;
  font-weight:bold;
  cursor:pointer;
  transition:.3s;
}

button:active{transform:scale(.97)}

.page{display:none}
.page.active{display:block;animation:reveal .8s ease}

.letter{
  text-align:left;
  padding:20px;
  margin-top:20px;
  border:1px solid #ffb7cd35;
  border-radius:20px;
  background:#ffffff0b;
}

.letter p{margin-bottom:15px}

.choices{
  display:grid;
  gap:12px;
  margin-top:20px;
}

.choices button{margin:0}
.secondary{
  background:transparent;
  border-color:#ff9fbd80;
}

.result{
  margin-top:22px;
  padding:18px;
  border-radius:18px;
  background:#ff8eb01a;
  animation:reveal .7s ease;
}

.small{
  font:11px Arial,sans-serif;
  color:#e6a8bd;
  margin-top:25px;
  letter-spacing:1px;
}

.floating{
  position:absolute;
  bottom:-40px;
  animation:float 7s linear forwards;
}

@keyframes beat{
  0%,100%{transform:scale(1)}
  50%{transform:scale(1.15)}
}

@keyframes appear{
  from{opacity:0;transform:translateY(20px)}
  to{opacity:1;transform:translateY(0)}
}

@keyframes reveal{
  from{opacity:0;transform:translateY(15px)}
  to{opacity:1;transform:translateY(0)}
}

@keyframes float{
  from{transform:translateY(0) rotate(0);opacity:0}
  15%{opacity:.8}
  to{transform:translateY(-110vh) rotate(40deg);opacity:0}
}

@media(prefers-reduced-motion:reduce){
  *,*::before,*::after{animation:none!important;transition:none!important}
}
</style>
</head>

<body>
<div id="hearts"></div>

<main>
<div class="card">

  <!-- PAGE 1 -->
  <section class="page active" id="page1">
    <div class="top">A little secret 💌</div>
    <div class="bigheart">❤️</div>

    <h1>Hey, <span>you...</span></h1>

    <p>
      There's something I've been wanting to tell you.
      Medyo kinakabahan ako, pero sana basahin mo
      hanggang dulo. 🥹
    </p>

    <button onclick="nextPage(2)">
      What is it? 💗
    </button>
  </section>

  <!-- PAGE 2 -->
  <section class="page" id="page2">
    <div class="top">From the heart</div>
    <div class="bigheart">💗</div>

    <h1>It's <span>you.</span></h1>

    <div class="letter">
      <p>
        Honestly, hindi ko alam kung paano ko ito
        sasabihin sa'yo nang personal, kaya dito ko
        na lang susubukan. ❤️
      </p>

      <p>
        At first, akala ko simpleng paghanga lang.
        Pero habang tumatagal, napapansin kong
        masaya ako kapag nakakausap kita, kapag
        nakikita kita, at kahit sa simpleng bagay
        na ginagawa mo.
      </p>

      <p>
        Hindi ko rin maintindihan kung bakit, pero
        may something sa'yo na iba para sa akin.
        You make my ordinary days feel a little
        more special.
      </p>

      <p>
        And I guess... I'm starting to like you
        more than I expected. 🥹💖
      </p>
    </div>

    <button onclick="nextPage(3)">
      There's more I want to say... 💌
    </button>
  </section>

  <!-- PAGE 3 -->
  <section class="page" id="page3">
    <div class="top">My honest confession</div>
    <div class="bigheart">💝</div>

    <h1>I <span>like you.</span></h1>

    <p>
      Hindi ko ito sinasabi para pilitin kang
      magkagusto rin sa akin. Gusto ko lang maging
      honest sa nararamdaman ko.
    </p>

    <p style="margin-top:15px">
      I like you for who you are, and I'd love to
      get to know you even more, if you're comfortable
      with that.
    </p>

    <p style="margin-top:18px">
      So, can I ask you something? 🥺
    </p>

    <button onclick="nextPage(4)">
      Tell me... ❤️
    </button>
  </section>

  <!-- PAGE 4 -->
  <section class="page" id="page4">
    <div class="top">One little question</div>
    <div class="bigheart">💌</div>

    <h1>What do <span>you think?</span></h1>

    <p>
      No pressure, okay? Whatever your answer is,
      I'll respect your feelings. I just wanted
      you to know mine. ❤️
    </p>

    <div class="choices">
      <button onclick="answer('yes')">
        💗 I like you too!
      </button>

      <button class="secondary" onclick="answer('maybe')">
        🥹 Can we get to know each other?
      </button>

      <button class="secondary" onclick="answer('no')">
        🤍 I see you as a friend
      </button>
    </div>

    <div id="result"></div>
    <div class="small">THANK YOU FOR READING THIS ♥</div>
  </section>

</div>
</main>

<script>
function nextPage(number){
  document.querySelectorAll(".page").forEach(page=>{
    page.classList.remove("active");
  });

  document.getElementById("page"+number).classList.add("active");
  window.scrollTo({top:0,behavior:"smooth"});
}

function answer(type){
  const result=document.getElementById("result");

  const messages={
    yes:"Wait... really? 🥹❤️ You just made me smile so much! Let's take our time and see where this goes. 💗",
    maybe:"Of course! ❤️ I'd love to get to know you better, at a pace that feels right for both of us. 🌷",
    no:"Thank you for being honest with me. 🤍 I respect your feelings, and I hope we can still be okay."
  };

  result.className="result";
  result.textContent=messages[type];

  for(let i=0;i<22;i++){
    setTimeout(createHeart,i*65);
  }
}

function createHeart(){
  const heart=document.createElement("span");
  heart.className="floating";
  heart.textContent=["♥","♡","💗","✨"][Math.floor(Math.random()*4)];
  heart.style.left=Math.random()*100+"%";
  heart.style.fontSize=(14+Math.random()*22)+"px";
  heart.style.color=["#ff8eb4","#ffd5e2","#ffffff"][Math.floor(Math.random()*3)];
  heart.style.animationDuration=(5+Math.random()*4)+"s";

  document.getElementById("hearts").appendChild(heart);
  setTimeout(()=>heart.remove(),9500);
}

setInterval(createHeart,650);
</script>
</body>
</html>
