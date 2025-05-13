# 🚀 我的 AI 项目演示页

欢迎来到我的项目主页！

## 🌟 项目简介

本项目基于 Transformer 架构，实现文本生成视频。

## 🎥 动态演示

下方是模型生成的视频预览（GIF 动画将自动播放）：

![演示动画](asserts/eg.gif)

## 📄 论文地址

[点击查看论文](https://arxiv.org/abs/1234.5678)

## 💻 GitHub 项目

[查看源码](https://github.com/yourname/yourproject)

## 📌 技术关键词

- 文本生成视频（Text-to-Video）
- Transformer 编码器
- Diffusion 模型 
## 🎬 项目演示轮播图

<div style="text-align: center; max-width: 600px; margin: auto;">
  <img id="gifSlider" src="asserts/gif1.gif" alt="GIF展示" style="width:100%; border-radius: 10px; box-shadow: 0 0 10px #ccc;">
  <br>
  <button onclick="prevGif()">⬅️ 上一个</button>
  <button onclick="nextGif()">➡️ 下一个</button>
</div>

<script>
  const gifs = ["asserts/gif1.gif", "asserts/gif2.gif", "asserts/gif3.gif"]; // 修改为你实际上传的 GIF 路径
  let currentIndex = 0;

  function showGif(index) {
    const img = document.getElementById("gifSlider");
    img.src = gifs[index];
  }

  function prevGif() {
    currentIndex = (currentIndex - 1 + gifs.length) % gifs.length;
    showGif(currentIndex);
  }

  function nextGif() {
    currentIndex = (currentIndex + 1) % gifs.length;
    showGif(currentIndex);
  }
</script>
##🎬 项目演示轮播图

欢迎来到我的演示页面！下面是多个自动播放的动图，点击按钮即可切换查看。

<div style="text-align: center; max-width: 600px; margin: auto;">
  <img id="gifSlider" src="asserts/gif1.gif" alt="GIF展示" style="width:100%; border-radius: 10px; box-shadow: 0 0 10px #ccc;">
  <br><br>
  <button onclick="prevGif()" style="padding: 8px 16px; font-size: 16px;">⬅️ 上一个</button>
  <button onclick="nextGif()" style="padding: 8px 16px; font-size: 16px;">➡️ 下一个</button>
</div>

<script>
  const gifs = ["asserts/gif1.gif", "asserts/gif2.gif", "asserts/gif3.gif"];
  let currentIndex = 0;

  function showGif(index) {
    const img = document.getElementById("gifSlider");
    img.src = gifs[index];
  }

  function prevGif() {
    currentIndex = (currentIndex - 1 + gifs.length) % gifs.length;
    showGif(currentIndex);
  }

  function nextGif() {
    currentIndex = (currentIndex + 1) % gifs.length;
    showGif(currentIndex);
  }

  // 可选：每隔5秒自动切换GIF
  setInterval(() => {
    nextGif();
  }, 5000);
</script>

## 🎞️ 滑动轮播演示图

<style>
.slider-container {
  position: relative;
  width: 100%;
  max-width: 600px;
  margin: auto;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0 0 10px #ccc;
}

.slider {
  display: flex;
  transition: transform 0.5s ease;
  width: 100%;
}

.slider img {
  width: 100%;
  flex-shrink: 0;
}

/* 按钮样式：左右两侧浮动 */
.nav-button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10;
  background-color: rgba(0, 0, 0, 0.4);
  color: white;
  border: none;
  font-size: 24px;
  padding: 10px 15px;
  cursor: pointer;
  border-radius: 50%;
}

#prevBtn {
  left: 10px;
}

#nextBtn {
  right: 10px;
}

.nav-button:hover {
  background-color: rgba(0, 0, 0, 0.7);
}
</style>

<div class="slider-container">
  <div class="slider" id="slider">
    <img src="asserts/gif1.gif" alt="GIF 1">
    <img src="asserts/gif2.gif" alt="GIF 2">
    <img src="asserts/gif3.gif" alt="GIF 3">
  </div>

  <!-- 左右按钮 -->
  <button class="nav-button" id="prevBtn" onclick="prevSlide()">&#10094;</button>
  <button class="nav-button" id="nextBtn" onclick="nextSlide()">&#10095;</button>
</div>

<script>
  const slider = document.getElementById("slider");
  const totalSlides = slider.children.length;
  let currentSlide = 0;

  function updateSlide() {
    const slideWidth = slider.clientWidth;
    slider.style.transform = `translateX(-${currentSlide * slideWidth}px)`;
  }

  function prevSlide() {
    currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
    updateSlide();
  }

  function nextSlide() {
    currentSlide = (currentSlide + 1) % totalSlides;
    updateSlide();
  }

  setInterval(() => {
    nextSlide();
  }, 5000);

  window.addEventListener("resize", updateSlide);
</script>

##视频播放实验
<div style="text-align:center;">
  <video width="640" controls autoplay loop muted>
    <source src="asserts/demo.mp4" type="video/mp4">
    你的浏览器不支持视频播放。
  </video>
  <p style="font-size:14px; margin-top:5px;">视频 1：系统演示</p>
</div>

##多组轮播实验
<style>
.carousel-container {
  position: relative;
  width: 100%;
  overflow: hidden;
  max-width: 1000px;
  margin: auto;
}

.carousel-track {
  display: flex;
  transition: transform 0.5s ease;
  width: 300%; /* 三组 */
}

.carousel-group {
  display: flex;
  justify-content: center;
  flex: 0 0 100%;
  gap: 20px;
}

.carousel-group img {
  width: 200px;
  height: auto;
  border-radius: 10px;
}

/* 左右按钮样式 */
.carousel-button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 15px;
  font-size: 18px;
  cursor: pointer;
  border-radius: 50%;
}

.carousel-button:hover {
  background-color: rgba(0, 0, 0, 0.7);
}

#prevBtn {
  left: 10px;
}

#nextBtn {
  right: 10px;
}
</style>

<div class="carousel-container">
  <div class="carousel-track" id="carouselTrack">
    <div class="carousel-group">
      <img src="asserts/gif1.gif">
      <img src="asserts/gif2.gif">
      <img src="asserts/gif3.gif">
    </div>
    <div class="carousel-group">
      <img src="asserts/gif4.gif">
      <img src="asserts/gif5.gif">
      <img src="asserts/gif6.gif">
    </div>
    <div class="carousel-group">
      <img src="asserts/gif7.gif">
      <img src="asserts/gif8.gif">
      <img src="asserts/gif9.gif">
    </div>
  </div>

  <!-- 左右切换按钮 -->
  <button class="carousel-button" id="prevBtn" onclick="prevGroup()">❮</button>
  <button class="carousel-button" id="nextBtn" onclick="nextGroup()">❯</button>
</div>

<script>
  let currentIndex = 0;
  const totalGroups = 3;

  function updateCarousel() {
    const track = document.getElementById("carouselTrack");
    const offset = -100 * currentIndex;
    track.style.transform = `translateX(${offset}%)`;
  }

  function prevGroup() {
    currentIndex = (currentIndex - 1 + totalGroups) % totalGroups;
    updateCarousel();
  }

  function nextGroup() {
    currentIndex = (currentIndex + 1) % totalGroups;
    updateCarousel();
  }
</script>

