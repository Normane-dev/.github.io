# 🚀 我的 AI 项目演示页

欢迎来到我的项目主页！

## 🌟 项目简介

本项目基于 Transformer 架构，实现文本生成视频。

## 🎥 动态演示

下方是模型生成的视频预览（GIF 动画将自动播放）：

![演示动画](assets/eg.gif)

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
  <img id="gifSlider" src="assets/gif1.gif" alt="GIF展示" style="width:100%; border-radius: 10px; box-shadow: 0 0 10px #ccc;">
  <br>
  <button onclick="prevGif()">⬅️ 上一个</button>
  <button onclick="nextGif()">➡️ 下一个</button>
</div>

<script>
  const gifs = ["assets/gif1.gif", "assets/gif2.gif", "assets/gif3.gif"]; // 修改为你实际上传的 GIF 路径
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
    <img src="assets/gif1.gif" alt="GIF 1">
    <img src="assets/gif2.gif" alt="GIF 2">
    <img src="assets/gif3.gif" alt="GIF 3">
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

## 放置视频实验
<div style="text-align:center;">
  <video width="640" controls autoplay loop muted>
    <source src="assets/demo.mp4" type="video/mp4">
    你的浏览器不支持视频播放。
  </video>
  <p style="font-size:14px; margin-top:5px;">视频 1：系统演示</p>
</div>
