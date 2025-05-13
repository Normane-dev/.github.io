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

欢迎体验自动播放的 GIF 滑动展示功能。

<style>
.slider-container {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: auto;
  border-radius: 10px;
  box-shadow: 0 0 10px #ccc;
  position: relative;
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
.button-container {
  text-align: center;
  margin-top: 10px;
}
.button-container button {
  padding: 10px 20px;
  font-size: 16px;
}
</style>

<div class="slider-container">
  <div class="slider" id="slider">
    <img src="assets/gif1.gif" alt="GIF 1">
    <img src="assets/gif2.gif" alt="GIF 2">
    <img src="assets/gif3.gif" alt="GIF 3">
  </div>
</div>

<div class="button-container">
  <button onclick="prevSlide()">⬅️ 上一张</button>
  <button onclick="nextSlide()">➡️ 下一张</button>
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

  // 自动滑动每5秒
  setInterval(() => {
    nextSlide();
  }, 5000);

  // 防止页面大小调整后位置错乱
  window.addEventListener("resize", updateSlide);
</script>

