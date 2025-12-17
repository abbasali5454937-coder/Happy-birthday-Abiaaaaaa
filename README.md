<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Abia! 🎉</title>
<style>
  body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #fbc2eb, #a6c1ee);
    height: 100vh;
    font-family: 'Comic Sans MS', cursive, sans-serif;
    overflow: hidden;
    text-align: center;
  }

  /* Glitter text */
  h1 {
    font-size: 3em;
    color: #ff4081;
    background: linear-gradient(90deg, #ff4081, #f1c40f, #3498db, #2ecc71);
    background-size: 300%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: glitter 3s linear infinite;
    margin-top: 1em;
  }

  @keyframes glitter {
    0% { background-position: 0% }
    100% { background-position: 300% }
  }

  p {
    color: #fff;
    font-size: 1.2em;
    margin: 0.5em 1em 2em 1em;
  }

  img.fancy {
    width: 200px;
    max-width: 50%;
    margin: 0.5em;
    animation: floatImg 4s ease-in-out infinite;
  }

  @keyframes floatImg {
    0%,100% { transform: translateY(0);}
    50% { transform: translateY(-20px);}
  }

  /* Balloons */
  .balloon {
    position: absolute;
    width: 50px;
    height: 70px;
    border-radius: 50%;
    bottom: -100px;
    animation: float 6s infinite;
  }
  .balloon:nth-child(1) { left: 5%; animation-delay: 0s; background: #f1c40f; }
  .balloon:nth-child(2) { left: 20%; animation-delay: 1s; background: #e74c3c; }
  .balloon:nth-child(3) { left: 35%; animation-delay: 2s; background: #3498db; }
  .balloon:nth-child(4) { left: 55%; animation-delay: 3s; background: #9b59b6; }
  .balloon:nth-child(5) { left: 70%; animation-delay: 4s; background: #2ecc71; }
  .balloon:nth-child(6) { left: 85%; animation-delay: 5s; background: #ff4081; }

  @keyframes float {
    0% { bottom: -100px; transform: translateX(0);}
    50% { transform: translateX(20px);}
    100% { bottom: 100%; transform: translateX(-20px);}
  }

  /* Confetti */
  .confetti {
    position: absolute;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    top: -10px;
    animation: confettiFall linear infinite;
  }
  @keyframes confettiFall {
    0% { transform: translateY(0) rotate(0deg);}
    100% { transform: translateY(120vh) rotate(360deg);}
  }

</style>
</head>
<body>

<h1>✨ Happy Birthday Abia! ✨</h1>
<p>Dear Abia, may your day be full of laughter, love, and magical moments! 🎂🎉 May every wish you make today turn into reality. Keep shining bright, because the world is better with your smile! 💖</p>

<!-- Fancy images -->
<img src="https://images.unsplash.com/photo-1606755962774-99e2cbf6d22a?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&w=400&q=80" class="fancy" alt="Birthday Cake">
<img src="https://images.unsplash.com/photo-1601758173920-18a0f6a1926c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&w=400&q=80" class="fancy" alt="Gifts">

<!-- Balloons -->
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>

<!-- Confetti -->
<script>
const colors = ['#f1c40f','#e74c3c','#3498db','#9b59b6','#2ecc71','#ff4081'];
for(let i=0;i<80;i++){
  const confetti = document.createElement('div');
  confetti.classList.add('confetti');
  confetti.style.left = Math.random()*100 + 'vw';
  confetti.style.backgroundColor = colors[Math.floor(Math.random()*colors.length)];
  confetti.style.width = confetti.style.height = (Math.random()*8 + 5) + 'px';
  confetti.style.animationDuration = (Math.random()*3 + 2) + 's';
  document.body.appendChild(confetti);
}

// Touch sparkle effect
document.body.addEventListener('click', e => {
  const sparkle = document.createElement('div');
  sparkle.style.position = 'absolute';
  sparkle.style.width = '15px';
  sparkle.style.height = '15px';
  sparkle.style.background = colors[Math.floor(Math.random()*colors.length)];
  sparkle.style.borderRadius = '50%';
  sparkle.style.left = e.clientX + 'px';
  sparkle.style.top = e.clientY + 'px';
  sparkle.style.opacity = 1;
  sparkle.style.transition = 'all 1s ease-out';
  document.body.appendChild(sparkle);
  setTimeout(() => {
    sparkle.style.top = e.clientY - 50 + 'px';
    sparkle.style.opacity = 0;
  }, 0);
  setTimeout(() => { sparkle.remove(); }, 1000);
});
</script>

</body>
</html>
