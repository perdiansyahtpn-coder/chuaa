<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Happy Birthday Cia!</title>
<style>
    body{
        margin:0;
        font-family:'Poppins', sans-serif;
        background:linear-gradient(135deg,#0d0d26,#1f1f3a,#3a3a5c);
        color:#fff;
        overflow-x:hidden;
    }

    /* Floating stars */
    .star{
        position:absolute;
        width:4px;
        height:4px;
        background:white;
        border-radius:50%;
        animation: twinkle 2s infinite ease-in-out;
        opacity:0.8;
    }
    @keyframes twinkle{
        0%{opacity:0.2; transform:scale(1);} 
        50%{opacity:1; transform:scale(1.8);} 
        100%{opacity:0.2; transform:scale(1);} 
    }

    .container{
        text-align:center;
        padding:100px 20px;
        position:relative;
        z-index:2;
    }

    h1{
        font-size:50px;
        font-weight:700;
        animation: glow 3s ease-in-out infinite alternate;
    }

    @keyframes glow{
        from{ text-shadow:0 0 10px #ff77ff, 0 0 20px #ff4dff, 0 0 30px #ff00ff; }
        to{ text-shadow:0 0 20px #81b3ff, 0 0 30px #3388ff, 0 0 40px #0059ff; }
    }

    .message{
        margin-top:20px;
        font-size:20px;
        max-width:700px;
        margin-left:auto;
        margin-right:auto;
        animation:fadeInUp 2s ease forwards;
        opacity:0;
    }

    @keyframes fadeInUp{
        0%{transform:translateY(40px); opacity:0;} 
        100%{transform:translateY(0); opacity:1;} 
    }

    .btn{
        margin-top:40px;
        padding:15px 35px;
        background:#ff6bff;
        border:none;
        color:#fff;
        border-radius:40px;
        cursor:pointer;
        font-size:18px;
        transition:0.3s;
        animation:pop 1.5s infinite;
    }

    @keyframes pop{
        0%,100%{ transform:scale(1);} 
        50%{ transform:scale(1.15);} 
    }

    .btn:hover{
        background:#a64dff;
    }

    /* Balloon animation */
    .balloon{
        position:absolute;
        width:60px;
        height:80px;
        background:#ff77ff;
        border-radius:50%;
        animation: floatUp 6s linear infinite;
        opacity:0.8;
    }

    @keyframes floatUp{
        0%{transform:translateY(100vh) rotate(0);} 
        100%{transform:translateY(-120vh) rotate(360deg);}    
    }
</style>
</head>
<body>

<!-- Random stars -->
<script>
for(let i=0;i<60;i++){
    let s=document.createElement("div");
    s.className="star";
    s.style.left=Math.random()*100+"%";
    s.style.top=Math.random()*100+"%";
    s.style.animationDelay=(Math.random()*2)+"s";
    document.body.appendChild(s);
}

for(let i=0;i<8;i++){
    let b=document.createElement("div");
    b.className="balloon";
    b.style.left=Math.random()*90+"%";
    b.style.background=`hsl(${Math.random()*360},80%,70%)`;
    b.style.animationDuration=(5 + Math.random()*5) + "s";
    document.body.appendChild(b);
}
</script>

<div class="container">
    <h1>🎉 Selamat Ulang Tahun, Cia! 🎉</h1>
    <p class="message">Semoga hari spesial kamu dipenuhi kebahagiaan, tawa, kejutan indah, dan semua hal baik yang kamu inginkan. Teruslah menjadi versi terbaik dari diri kamu. Kamu keren, hebat, dan berharga! 💖✨</p>
    <button class="btn" onclick="showCake()">Klik untuk Kejutan 🎁</button>
</div>

<div id="cakeBox" style="position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.85); display:flex; justify-content:center; align-items:center; flex-direction:column; z-index:999; opacity:0; pointer-events:none; transition:0.5s;">

<button onclick="closeCake()" style="position:fixed; bottom:25px; left:25px; padding:12px 28px; background:#4da6ff; border:none; border-radius:20px; color:white; font-size:18px; cursor:pointer; box-shadow:0 0 15px #4da6ff; z-index:2000;">Kembali</button>

        <div style="font-size:48px; margin-bottom:120px; font-weight:700; color:#ffd6ff; text-shadow:0 0 20px #ff66ff; animation:fadeIn 1.5s ease forwards;">
            🎉 Happy Birthday Cia 🎉
        </div>

        <!-- Cake container -->
        <div class="cake" style="width:230px; height:auto; padding-bottom:40px; position:relative; animation:popUp 1s ease forwards;">

    <!-- Bottom round layer -->
    <div style="width:230px; height:120px; background:#ff82b4; border-radius:0 0 30px 30px; position:relative; box-shadow:0 8px 25px rgba(0,0,0,0.4);">
        <div style="position:absolute; top:-25px; left:0; width:100%; height:40px; background:#ffd6f2; border-radius:20px; box-shadow:0 4px 15px rgba(0,0,0,0.2);"></div>
</div>

<!-- Tombol kembali di kiri bawah kue -->


    <!-- Middle round layer -->
    <div style="width:180px; height:100px; background:#ff9acb; border-radius:0 0 25px 25px; margin:auto; margin-top:-20px; position:relative; box-shadow:0 6px 20px rgba(0,0,0,0.35);">
        <div style="position:absolute; top:-22px; left:0; width:100%; height:35px; background:#ffe6f7; border-radius:20px; box-shadow:0 4px 10px rgba(0,0,0,0.2);"></div>
    </div>

    <!-- Top round layer -->
    <div style="width:140px; height:85px; background:#ffb8e0; border-radius:0 0 20px 20px; margin:auto; margin-top:-20px; position:relative; box-shadow:0 4px 15px rgba(0,0,0,0.25);">
        <div style="position:absolute; top:-20px; left:0; width:100%; height:30px; background:#fff0fa; border-radius:20px; box-shadow:0 3px 8px rgba(0,0,0,0.2);"></div>
    </div>

    <!-- Candle stick -->
    <div style="position:absolute; top:-80px; left:50%; transform:translateX(-50%); width:14px; height:40px; background:#ffe066; border-radius:7px; box-shadow:0 0 12px #fff066;"></div>

    <!-- Candle flame -->
    <div style="position:absolute; top:-105px; left:50%; transform:translateX(-50%); font-size:35px; animation:flame 0.9s infinite alternate;">🔥</div>

    <!-- Sprinkles -->
    <div style="position:absolute; top:20px; left:30px; width:12px; height:12px; background:#ffe066; border-radius:50%;"></div>
    <div style="position:absolute; top:60px; right:50px; width:10px; height:10px; background:#90f7ec; border-radius:50%;"></div>
    <div style="position:absolute; bottom:20px; left:80px; width:14px; height:14px; background:#ffadff; border-radius:50%;"></div>
</div>
</div>
</div>


    </div>

<script>
function showCake(){
    document.getElementById('cakeBox').style.opacity = '1';
    document.getElementById('cakeBox').style.pointerEvents = 'auto';
}
function closeCake(){
    document.getElementById('cakeBox').style.opacity = '0';
    document.getElementById('cakeBox').style.pointerEvents = 'none';
}
</script>

<style>
@keyframes popUp{
    from{transform:scale(0); opacity:0;} to{transform:scale(1); opacity:1;}
}
@keyframes flame{
    from{transform:scale(1);} to{transform:scale(1.3);} 
}
@keyframes fadeIn{
    from{opacity:0;} to{opacity:1;}
}
</style>

<script>
// Add 3D glow and wiggle
setTimeout(()=>{
 const cake = document.querySelector('#cakeBox .cake');
 if(cake){ cake.style.animation = 'popUp 1s ease forwards, wiggle 3s infinite ease-in-out'; }
},500);
</script>

<style>
@keyframes wiggle{
 0%,100%{transform:rotate(0);} 
 50%{transform:rotate(3deg);} 
}
</style>
<script>
// Confetti generator
function createConfetti(){
 for(let i=0;i<40;i++){
   let c=document.createElement('div');
   c.className='confetti';
   c.style.left=Math.random()*100+'%';
   c.style.background=`hsl(${Math.random()*360},80%,60%)`;
   c.style.animationDuration=(3+Math.random()*2)+'s';
   document.body.appendChild(c);
   setTimeout(()=>c.remove(),5000);
 }
}

// Glitter effect
function createGlitter(){
 for(let i=0;i<25;i++){
   let g=document.createElement('div');
   g.className='glitter';
   g.style.left=Math.random()*100+'%';
   g.style.top=Math.random()*100+'%';
   g.style.animationDuration=(1+Math.random()*1)+'s';
   document.body.appendChild(g);
   setTimeout(()=>g.remove(),2000);
 }
}

// Trigger when cake opens
const origShowCake = showCake;
showCake = function(){
  origShowCake();
  createConfetti();
  createGlitter();
};
</script>

<style>
.confetti{
  position:fixed;
  top:0;
  width:10px;
  height:14px;
  opacity:0.9;
  animation:fall linear forwards;
}
@keyframes fall{
  0%{transform:translateY(-20px) rotate(0);} 
  100%{transform:translateY(110vh) rotate(360deg);} 
}

.glitter{
  position:fixed;
  width:6px;
  height:6px;
  background:white;
  border-radius:50%;
  opacity:0.8;
  animation:sparkle ease-in-out infinite;
}
@keyframes sparkle{
  0%{transform:scale(0.4); opacity:0.3;} 
  50%{transform:scale(1.4); opacity:1;} 
  100%{transform:scale(0.4); opacity:0.3;} 
}
</style>
</body>
</html>
