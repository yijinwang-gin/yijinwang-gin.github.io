---
layout: page
title: 游戏 Demo
description: 游戏原型和交互作品
sitemap: false
permalink: /game-demo/
---

<style>
.demo-card {
  background: #f8f9fa;
  border-radius: 12px;
  padding: 2rem;
  margin-bottom: 2.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.06);
}
.demo-card h2 {
  margin-top: 0;
}
.demo-card blockquote {
  border-left: 3px solid #6c63ff;
  padding-left: 1rem;
  color: #666;
  font-style: italic;
}
.demo-card .status-tag {
  display: inline-block;
  background: #fff3cd;
  color: #856404;
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 600;
  margin-top: 0.5rem;
}
.demo-card .tagline {
  font-weight: 600;
  color: #6c63ff;
  letter-spacing: 0.05em;
  margin-top: 1rem;
}
.demo-card iframe,
.demo-card video {
  border-radius: 8px;
  margin-top: 1rem;
}
.video-placeholder {
  display: grid;
  place-items: center;
  min-height: 180px;
  margin-top: 1rem;
  padding: 1.5rem;
  border: 1px solid #e2e5e9;
  border-radius: 8px;
  background: #fff;
  text-align: center;
}
.video-placeholder button {
  padding: 0.65rem 1rem;
  border: 0;
  border-radius: 6px;
  background: #6c63ff;
  color: #fff;
  cursor: pointer;
  font: inherit;
}
.video-placeholder a {
  margin-top: 0.75rem;
  color: #666;
  font-size: 0.9rem;
}
.demo-gallery {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
  margin-top: 1.25rem;
}
.demo-gallery figure {
  margin: 0;
}
.demo-gallery img {
  display: block;
  width: 100%;
  border-radius: 8px;
}
.demo-gallery figcaption {
  margin-top: 0.5rem;
  color: #666;
  font-size: 0.9rem;
}
@media (max-width: 640px) {
  .demo-gallery {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="demo-card" markdown="1">

## 命名它（Name It）
> AI 对话互动｜开发中

一款以心理咨询场景为背景的 AI 对话互动游戏。玩家扮演咨询师，与来访者展开对话，从表达中抽取具有意义的词语，并在可视化的意识场景中剪断词语之间的关联，逐步推进干预与探索。

<p class="tagline">对话进入意识，词语改变关系。</p>

<div class="demo-gallery">
  <figure>
    <img src="/assets/demo/name-it-main.png" alt="命名它的咨询对话与词语关联界面" loading="lazy">
    <figcaption>咨询对话与词语关联</figcaption>
  </figure>
  <figure>
    <img src="/assets/demo/name-it-subconscious.png" alt="命名它的潜意识探索场景" loading="lazy">
    <figcaption>潜意识探索场景</figcaption>
  </figure>
</div>

<span class="status-tag">开发中 Demo，暂未上线</span>

</div>

<div class="demo-card" markdown="1">

## 未知信号源
> 推理解谜游戏（微信小游戏）

「未知信号源」—— 一款沉浸式跨维度解谜微信小程序。玩家通过操作一台来自异世界的「通讯仪」，窥视被害人「阿里亚斯」的私人设备，协助调查官星河破解一桩谋杀案。

<div class="video-placeholder" data-video-src="//player.bilibili.com/player.html?isOutside=true&aid=116322746964044&bvid=BV1t3XkBhEst&cid=37119460430&p=1&autoplay=0">
  <button type="button">点击播放演示视频</button>
  <a href="https://www.bilibili.com/video/BV1t3XkBhEst" target="_blank" rel="noopener">在 B 站打开</a>
</div>

<span class="status-tag">开发中 Demo，尚未上线</span>

</div>

<div class="demo-card" markdown="1">

## 睁开你的双眼（UNMASK）
> Global Game Jam 2026 | 主题：MASK

一款像素风格的叙事冒险游戏。

玩家扮演一个从黑暗中苏醒的角色，在一个被遮蔽（MASK）的世界中探索。通过收集光点、击败虚无怪物，逐渐揭开世界的面纱。随着旅程推进，画幅从30%扩展至全屏，象征着主角对世界认知的觉醒——从一无所知，到最终直面世界的真相（UNMASK）。

<p class="tagline">UNMASK the world. UNMASK yourself.</p>

<div class="video-placeholder" data-video-src="//player.bilibili.com/player.html?isOutside=true&aid=115994248943014&bvid=BV1mK6tBWEGR&cid=35748579340&p=1&autoplay=0">
  <button type="button">点击播放演示视频</button>
  <a href="https://www.bilibili.com/video/BV1mK6tBWEGR" target="_blank" rel="noopener">在 B 站打开</a>
</div>

</div>

<script>
document.querySelectorAll('.video-placeholder button').forEach(function (button) {
  button.addEventListener('click', function () {
    var placeholder = button.parentElement;
    var iframe = document.createElement('iframe');
    iframe.src = placeholder.dataset.videoSrc;
    iframe.scrolling = 'no';
    iframe.frameBorder = '0';
    iframe.allowFullscreen = true;
    iframe.width = '100%';
    iframe.height = '500';
    iframe.title = 'Bilibili 演示视频';
    placeholder.replaceWith(iframe);
  });
});
</script>

<div class="demo-card" markdown="1">

## FPS Demo（基于UE）

<video width="100%" controls preload="metadata" style="border-radius: 8px;">
  <source src="/assets/demo/FPSdemo_simple.mp4" type="video/mp4">
</video>

</div>
