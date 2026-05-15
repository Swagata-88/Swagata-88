## Hi there 👋

<div align="center">

<style>
.scene {
  width: 220px;
  height: 220px;
  perspective: 800px;
  margin: 60px auto;
}

.cube {
  width: 100%;
  height: 100%;
  position: relative;
  transform-style: preserve-3d;
  animation: rotate 12s infinite linear;
}

.face {
  position: absolute;
  width: 220px;
  height: 220px;
  background: rgba(0, 247, 255, 0.1);
  border: 2px solid #00F7FF;
  box-shadow: 0 0 25px #00F7FF;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-size: 22px;
  font-weight: bold;
  color: white;
  font-family: Arial, sans-serif;
  backdrop-filter: blur(5px);
}

.front  { transform: rotateY(0deg) translateZ(110px); }
.back   { transform: rotateY(180deg) translateZ(110px); }
.right  { transform: rotateY(90deg) translateZ(110px); }
.left   { transform: rotateY(-90deg) translateZ(110px); }
.top    { transform: rotateX(90deg) translateZ(110px); }
.bottom { transform: rotateX(-90deg) translateZ(110px); }

@keyframes rotate {
  0% {
    transform: rotateX(0deg) rotateY(0deg);
  }
  100% {
    transform: rotateX(360deg) rotateY(360deg);
  }
}
</style>

<div class="scene">
  <div class="cube">

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
      Open<br>Source<br>Learner
    </div>

  </div>
</div>

</div>
