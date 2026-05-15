## Hi there 👋

<div align="center">

<style>
body {
  background: #050816;
}

.scene {
  width: 240px;
  height: 240px;
  perspective: 1000px;
  margin: 80px auto;
}

.cube {
  width: 100%;
  height: 100%;
  position: relative;
  transform-style: preserve-3d;
  transition: transform 0.1s linear;
  animation: autoRotate 12s infinite linear;
}

.scene:hover .cube {
  animation-play-state: paused;
}

.face {
  position: absolute;
  width: 240px;
  height: 240px;
  background: rgba(0, 247, 255, 0.08);
  border: 2px solid #00F7FF;
  box-shadow:
    0 0 15px #00F7FF,
    0 0 30px #00F7FF,
    inset 0 0 15px #00F7FF;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-size: 24px;
  font-weight: bold;
  color: white;
  font-family: Arial, sans-serif;
  backdrop-filter: blur(8px);
  text-shadow: 0 0 10px #00F7FF;
}

.front  { transform: rotateY(0deg) translateZ(120px); }
.back   { transform: rotateY(180deg) translateZ(120px); }
.right  { transform: rotateY(90deg) translateZ(120px); }
.left   { transform: rotateY(-90deg) translateZ(120px); }
.top    { transform: rotateX(90deg) translateZ(120px); }
.bottom { transform: rotateX(-90deg) translateZ(120px); }

@keyframes autoRotate {
  0% {
    transform: rotateX(-20deg) rotateY(0deg);
  }
  100% {
    transform: rotateX(-20deg) rotateY(360deg);
  }
}
</style>

<div class="scene" id="scene">
  <div class="cube" id="cube">

    <div class="face front">
      Full Stack<br>Web Developer
    </div>

    <div class="face back">
      ML<br>Programmer
    </div>

    <div class="face right">
      Python<br>Developer
    </div>

    <div class="face left">
      Backend<br>Developer
    </div>

    <div class="face top">
      AI<br>Enthusiast
    </div>

    <div class="face bottom">
      Open Source<br>Learner
    </div>

  </div>
</div>

<script>
const cube = document.getElementById('cube');
const scene = document.getElementById('scene');

let rotateX = -20;
let rotateY = 0;
let isDragging = false;
let previousX;
let previousY;

scene.addEventListener('mousedown', (e) => {
  isDragging = true;
  previousX = e.clientX;
  previousY = e.clientY;
  cube.style.animation = 'none';
});

window.addEventListener('mouseup', () => {
  isDragging = false;
});

window.addEventListener('mousemove', (e) => {
  if (!isDragging) return;

  const deltaX = e.clientX - previousX;
  const deltaY = e.clientY - previousY;

  rotateY += deltaX * 0.5;
  rotateX -= deltaY * 0.5;

  cube.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;

  previousX = e.clientX;
  previousY = e.clientY;
});
</script>

</div>

