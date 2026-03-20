# applelll-ope.github.io
1
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>青蒙智旅 - 科技生态宣传片</title>
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Microsoft YaHei", sans-serif;
  }
  body {
    /* 科技感蓝绿色渐变+风动粒子背景 */
    background: linear-gradient(135deg, #0a2e38, #145c6d, #2ec4b6);
    min-height: 100vh;
    padding: 40px 20px;
    position: relative;
    overflow: hidden;
  }
  /* 风动粒子效果 */
  .wind-particles {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
  }
  .container {
    max-width: 900px;
    margin: 0 auto;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    border-radius: 24px;
    padding: 40px;
    box-shadow: 0 10px 40px rgba(0, 20, 30, 0.3);
    border: 1px solid rgba(100, 255, 200, 0.3);
    position: relative;
    z-index: 1;
  }
  .title {
    text-align: center;
    color: #e0f7f4;
    font-size: 28px;
    margin-bottom: 30px;
    text-shadow: 0 0 10px rgba(30, 200, 180, 0.5);
  }
  .video-wrap {
    position: relative;
    width: 100%;
    padding-top: 56.25%;
    border-radius: 18px;
    overflow: hidden;
    border: 2px solid rgba(72, 219, 196, 0.6);
    box-shadow: 0 0 20px rgba(30, 200, 180, 0.4);
  }
  iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
    border-radius: 16px;
  }
  .desc {
    text-align: center;
    color: #b8f0e8;
    margin-top: 20px;
    font-size: 16px;
    letter-spacing: 1px;
  }
</style>
</head>
<body>
  <!-- 风动粒子背景 -->
  <div class="wind-particles" id="windParticles"></div>
  
  <div class="container">
    <h2 class="title">🌬️ 青蒙智旅 · 科技赋能生态旅游</h2>
    <div class="video-wrap">
      <iframe src="https://player.bilibili.com/player.html?bvid=BV1JUAEzVEkB&page=1&high_quality=1" allowfullscreen></iframe>
    </div>
    <p class="desc">科技感蓝绿风 · 探索腾格里生态智慧之旅</p >
  </div>

  <!-- 风动粒子动画脚本 -->
  <script>
    const particles = document.getElementById('windParticles');
    for (let i = 0; i < 50; i++) {
      const particle = document.createElement('div');
      particle.style.position = 'absolute';
      particle.style.width = `${Math.random() * 3 + 1}px`;
      particle.style.height = `${Math.random() * 10 + 2}px`;
      particle.style.backgroundColor = `rgba(${100 + Math.random() * 155}, ${200 + Math.random() * 55}, ${180 + Math.random() * 75}, ${Math.random() * 0.5 + 0.2})`;
      particle.style.borderRadius = '50%';
      particle.style.left = `${Math.random() * 100}%`;
      particle.style.top = `${Math.random() * 100}%`;
      particle.style.animation = `windMove ${Math.random() * 15 + 10}s linear infinite`;
      particles.appendChild(particle);
    }

    // 风动动画关键帧
    const style = document.createElement('style');
    style.textContent = `
      @keyframes windMove {
        0% { transform: translateX(-10px) translateY(0); opacity: 0.2; }
        50% { opacity: 0.5; }
        100% { transform: translateX(100vw) translateY(${Math.random() * 50 - 25}px); opacity: 0.2; }
      }
    `;
    document.head.appendChild(style);
  </script>
</body>
</html>
