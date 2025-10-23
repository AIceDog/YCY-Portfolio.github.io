---
layout: default
title: Yichen Yang's Works
---

<style>
  body {
    background-image: url('images/wallpaper.jpg'); /* <-- 在这里修改你的壁纸图片路径 */
    background-size: cover;             /* 铺满整个屏幕 */
    background-position: center;        /* 居中显示 */
    background-attachment: fixed;       /* 固定背景，滚动时背景不动 */
    background-repeat: no-repeat;       /* 防止图片平铺重复 */
  }
</style>


# Yichen Yang
**技术美术 (Technical Artist) | 专注于程序化生成 (PCG)**

你好！欢迎来到我的作品集。我致力于探索 Houdini、UE5 和 Python 在游戏开发中的程序化解决方案。

---

## 项目与作品

### 项目一：Houdini 程序化岩石包边 (Gaea/Houdini/UE5)

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
  <iframe 
    src="https://player.bilibili.com/player.html?bvid=BV1tmeRzBEWd&page=1" 
    scrolling="no" 
    border="0" 
    frameborder="no" 
    framespacing="0" 
    allowfullscreen="true"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

<p style="margin-top: 10px;">
  <strong>项目简介：</strong>
  <br><strong>Gaea:</strong> 负责生成基础地形地貌，并输出岩石区域遮罩（Mask）。
  <br><strong>Houdini:</strong> 利用 Gaea 遮罩，程序化撒点并放置大型主体岩石。通过 Python 脚本实现精细化控制，根据已有岩石位置和遮罩数据，自动生成（或放置）用于过渡和填充的细节岩石。
  <br><strong>UE5:</strong> 导入所有资产，并利用遮罩在材质中实现岩石与地形的自动包边和无缝融合。
  <br>
  <a href="https://www.bilibili.com/video/BV1tmeRzBEWd/" target="_blank">
    在 Bilibili 上观看 (获取弹幕和评论)
  </a>
</p>

<details style="border: 1px solid #ddd; padding: 10px; border-radius: 5px; margin-top: 15px;">
  <summary style="cursor: pointer;">
    <strong>点击展开/折叠项目效果图片 (共 3 张)</strong>
  </summary>
  <div style="margin-top: 10px;">
    <img src="images/Rocks_gaea.png" alt="Gaea 高程图" width="100%" style="margin-bottom: 10px;">
    <img src="images/Rocks_Houdini.png" alt="Houdini 节点" width="100%" style="margin-bottom: 10px;">
    <img src="images/Rocks_UE5.png" alt="UE5 最终效果" width="100%">
  </div>
</details>

* **使用技术：** Gaea, Houdini, VEX, UE5 (材质)

---

### 项目二：Houdini Python 程序化建筑

<p style="margin-top: 10px;">
  <strong>项目简介：</strong> 本项目是一个基于 Houdini 和 Python 构建的程序化建筑生成器。其核心思想是将‘乐高积木’（模块化组件）与多阶段算法相结合：
</p>

<ol style="text-align: left;">
  <li>
    <strong>体素化 (Voxelization):</strong> 首先，将任意输入几何体（或建筑轮廓）体素化，将其转换为一个三维空间网格，作为建筑的“地基”和可建造空间。
  </li>
  <li>
    <strong>内部流线 (A* Pathfinding):</strong> 接着，利用带约束的 A* 寻路算法，在体素空间中自动“雕刻”出核心的内部流线，如走廊和楼梯间。
  </li>
  <li>
    <strong>模块填充 (Template Matching):</strong> 最后，系统使用模板匹配算法，将一个预设的“乐高”模块库（如房间、拐角、T型路口等）智能地拼装到 A* 算法生成的路径和剩余空间中，最终组装成完整的建筑结构。
  </li>
</ol>

<p>
  <strong>使用技术：</strong> Houdini, Python (Houdini), Jupyter Notebook
</p>

<details style="border: 1px solid #ddd; padding: 10px; border-radius: 5px; margin-top: 15px;">
  <summary style="cursor: pointer;">
    <strong>点击展开/折叠项目效果图片 (共 9 张)</strong>
  </summary>
  <div style="margin-top: 10px;">
    <img src="images/building1_001.png" alt="建筑图片1" width="100%" style="margin-bottom: 10px;">
    <img src="images/building1_002.png" alt="建筑图片2" width="100%" style="margin-bottom: 10px;">
    <img src="images/building1_003.png" alt="建筑图片3" width="100%" style="margin-bottom: 10px;">
    <img src="images/building2_001.png" alt="建筑图片4" width="100%" style="margin-bottom: 10px;">
    <img src="images/building2_002.png" alt="建筑图片5" width="100%" style="margin-bottom: 10px;">
    <img src="images/building2_003.png" alt="建筑图片6" width="100%" style="margin-bottom: 10px;">
    <img src="images/building2_004.png" alt="建筑图片7" width="100%" style="margin-bottom: 10px;">
    <img src="images/building2_005.png" alt="建筑图片8" width="100%" style="margin-bottom: 10px;">
    <img src="images/building2_006.png" alt="建筑图片9" width="100%">
  </div>
</details>

---

### 非游戏项目：基于 Transformer 的 3D 人体姿态识别

<p style="margin-top: 10px;">
  <strong>项目简介：</strong> 在 Vision Transformer (ViT) 的基础上利用 Pytorch 搭建和训练神经网络, 实现从 2D 视频输入到 3D 人体骨骼动画的姿态估计。
  <br>
  <strong>使用技术：</strong> Python, Pytorch, Transformer (ViT)
  <br>
  <a href="https://github.com/AIceDog/JSTFormer.git" target="_blank">
    <strong>在 GitHub 上查看项目源码</strong>
  </a>
</p>

<table style="width:100%;">
  <tr>
    <td style="width:50%; padding-right: 5px;">
      <img src="gifs/JSTFormer_Sample1.gif" alt="输出效果1" width="100%">
      <p style="text-align:center; font-size: 0.9em; color: #555;">(输入视频)</p>
    </td>
    <td style="width:50%; padding-left: 5px;">
      <img src="gifs/JSTFormer_Sample2.gif" alt="输出效果2" width="100%">
      <p style="text-align:center; font-size: 0.9em; color: #555;">(3D姿态识别结果)</p>
    </td>
  </tr>
</table>

---

## 关于我

我热衷于在游戏中创建复杂的程序化系统，擅长使用 Houdini 和 UE5 构建高效可控的工具流来解决美术管线中的挑战。

* **核心技能：**
    * **DCC:** Houdini (VEX, Python), UE5 (Blueprints, Materials)
    * **编程:** Python, C++, HLSL
    * **其他:** Substance Designer, Computer Vision, Transformer
* **联系方式：**
    * **Email:** 15927443559@163.com
    * **LinkedIn:** <a href="https://www.linkedin.com/in/yichen-yang-72235b166/" target="_blank">linkedin.com/in/yichen-yang-72235b166</a>
