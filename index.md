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
