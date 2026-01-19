# AI Mixed-Cut: AI Intelligent Mixed-Cut Workflow

[简体中文](./README.md) | [English](./README_en.md)

[![GitHub stars](https://img.shields.io/github/stars/toki-plus/ai-mixed-cut?style=social)](https://github.com/toki-plus/ai-mixed-cut/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/toki-plus/ai-mixed-cut?style=social)](https://github.com/toki-plus/ai-mixed-cut/network/members)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/toki-plus/ai-mixed-cut/pulls)

**AI Mixed-Cut is a groundbreaking AI content generation tool that employs a unique "Deconstruct-Reconstruct" model to deeply analyze existing video content into a reusable creative library, then fully automates the generation of a continuous stream of highly original, brand-new short videos.**

This project is designed to provide content creators with an ultimate solution for evolving from imitation to innovation, breaking free from the inefficient cycle of "rewriting" and "deduplication" to enter a new era of intelligent, scalable, and original content production.

<p align="center">
  <a href="https://www.bilibili.com/video/BV1aAxQeLEu1" target="_blank">
    <img src="./assets/images/cover_demo.png" alt="Click to watch the demo video on Bilibili (Coming Soon)" width="800"/>
  </a>
  <br>
  <em>(Click the cover to watch the HD demo video on Bilibili)</em>
</p>

---

## ✨ Core Features

This project redefines video content re-creation with a three-phase intelligent pipeline:

### Module 1: AI Content Engine

-   **✍️ One-Click Script Extraction**: Input Douyin (China's TikTok) share links to automatically extract the video's full title, tags, and script.
-   **🧩 Deep Library Deconstruction**:
    -   **Topic Deconstruction**: Distills the core topic, target audience, and value proposition of a video, creating `topics.json`.
    -   **Framework Deconstruction**: Abstracts the video's narrative structure and content formula, creating `frameworks.json`.
    -   **Golden Sentence Deconstruction**: Mines and stores high-quality, universally applicable sentences, creating `golden_sentences.json`.
-   **🧬 Intelligent Script Reconstruction**:
    -   Randomly selects "topics," "frameworks," and "golden sentences" from the deconstructed library.
    -   Leverages a large language model (LLM) to follow the chosen framework and topic, integrating the golden sentences as key viewpoints to create a structurally similar but entirely new and original script.
    -   Automatically generates accompanying viral titles, tags, and cover text.

### Module 2: Intelligent Audio Synthesis

-   **🎙️ High-Quality Voices**: Integrates with Microsoft Edge TTS, offering natural-sounding voices across multiple languages and emotions, with fine-tuned control over rate, pitch, and volume.
-   **📜 Automatic Subtitle Generation**: Simultaneously creates a perfectly synchronized `.srt` subtitle file alongside the audio.
-   **✂️ Intelligent Line-Break Optimization**: Employs an advanced algorithm to post-process the generated subtitles, optimizing line breaks for semantic clarity and visual appeal, enhancing the viewer's reading experience.

### Module 3: Cinematic Video Generation

-   **🎞️ Dynamic Material Splicing**: Configure multiple video material folders, which can be stitched together sequentially or randomly. Set a "fixed duration," "random duration," or "original duration" for each material.
-   **💥 Advanced Visual Effects**:
    -   **Cinematic Color Grading (LUT)**: Randomly applies professional-grade LUT filters for an instant quality boost.
    -   **Dynamic Visuals**: Includes dynamic zoom/pan camera movements, random rotation, color shifting, texture noise, background blur, and more to enrich the visual layers.
    -   **Dynamic Masks & Picture-in-Picture**: Randomly overlays artistic masks or dynamic video footage to increase visual uniqueness.
    -   **Smart Transitions**: Enables a variety of cool `xfade` video transitions when stitching longer videos.
-   **🚀 Hardware Acceleration**: Full support for NVIDIA (NVENC) GPUs for hardware-based encoding, dramatically reducing video rendering times.
-   **GUI & Workflow**:
    -   Provides a comprehensive graphical interface with all parameters clearly laid out, supporting a one-click full workflow.
    -   Allows for independent execution of each module for easy debugging and testing.

## 📸 Screenshots

<p align="center">
  <img src="./images/cover_software.png" alt="Main UI" width="800"/>
  <br>
  <em>The main user interface, showcasing the four modular workflows.</em>
</p>

## 🚀 Quick Start

### System Requirements

1.  **OS**: Windows.
2.  **Software/Tools**:
    | Software/Tool       | Download/Installation Instructions                             | Notes                                               |
    | :------------------ | :------------------------------------------------------------- | :-------------------------------------------------- |
    | **FFmpeg**          | [Gyan.dev Builds](https://www.gyan.dev/ffmpeg/builds/)         | **Must** be extracted and its `bin` directory added to the system `PATH`. |
    | **Google Chrome**   | [Official Download](https://www.google.com/chrome/)            | Required for AI features to drive the browser for Doubao interaction. |

### Installation & Configuration

-   **Download Link**: https://download.llxoxll.com/latest/yanqu_mixed_cut_v2

## 📖 Usage Guide

1.  **Log in to Doubao**:
    -   In "Module 1", click the **"Login / Refresh Session"** button.
    -   Scan the QR code in the popped-up browser to log in to Doubao.
    -   **After successful login, manually close the browser window.** The program will save your session.
2.  **Configure Workflow**:
    -   **Module 1**: Paste multiple Douyin video share links into the text box, one per line.
    -   **Module 2**: Select your preferred language, gender, and specific voice. Adjust rate, volume, and pitch with the sliders.
    -   **Module 3**:
        -   Click "Add Material Group" to configure at least one local folder of video clips.
        -   Check the desired video effects.
    -   **Module 4**: In the "Hardware & Task" section, set GPU concurrency, generation count, etc.
3.  **Execute Tasks**:
    -   **Step-by-Step (Recommended for first-time use)**:
        1.  Click **"Start Extraction"** and wait for the AI to extract scripts.
        2.  Click **"Start Deconstruction"** to build your creative library.
        3.  Click **"Start Full Workflow"**. The program will now automatically execute the "Reconstruct -> Generate Audio -> Generate Video" pipeline.
    -   **One-Click Execution**: After configuration, simply click **"Start Full Workflow"** to run the entire process starting from script reconstruction.
4.  **View Results**: All intermediate files and final videos are saved in the `output` folder for easy access and management.

---

<p align="center">
  <strong>For custom development or technical inquiries, please connect via:</strong>
</p>
<table align="center">
  <tr>
    <td align="center">
      <img src="./images/wechat.png" alt="WeChat QR Code" width="200"/>
      <br />
      <sub><b>WeChat</b></sub>
      <br />
      <sub>ID: toki-plus (Note: "GitHub Customization")</sub>
    </td>
    <td align="center">
      <img src="./images/gzh.png" alt="Public Account QR Code" width="200"/>
      <br />
      <sub><b>Public Account</b></sub>
      <br />
      <sub>Scan for tech articles</sub>
    </td>
  </tr>
</table>

## 📂 My Other Open-Source Projects

-   **[Netease Downloader](https://github.com/toki-plus/netease-downloader)**: An elegant, feature-rich desktop application for downloading high-quality and lossless music from Netease Cloud Music, with support for playlists, albums, QR login, and automatic metadata tagging.
-   **[AI-Trader-For-MT4](https://github.com/toki-plus/ai-trader-for-mt4)**: A revolutionary open-source framework that transforms a Large Language Model (LLM) into an autonomous trading agent for the MetaTrader 4 (MT4) platform.
-   **[Auto USPS Tracker](https://github.com/toki-plus/auto-usps-tracker)**: An efficient USPS bulk package tracker for e-commerce sellers, featuring anti-blocking scraping and formatted Excel report generation.
-   **[AI Video Workflow](https://github.com/toki-plus/ai-video-workflow)**: A fully automated AI-native video generation pipeline, integrating Text-to-Image, Image-to-Video, and Text-to-Music models to create AIGC short videos with one click.
-   **[AI Highlight Clip](https://github.com/toki-plus/ai-highlight-clip)**: An AI-driven intelligent clipping tool that automatically analyzes and extracts "highlight moments" from long-form videos and generates viral titles.
-   **[AI TTV Workflow](https://github.com/toki-plus/ai-ttv-workflow)**: An AI-powered Text-to-Video tool that automatically converts any script into a short video with voiceover, subtitles, and a cover, supporting script extraction/re-creation/translation.
-   **[AB Video Deduplicator](https://github.com/toki-plus/AB-Video-Deduplicator)**: Utilizes an innovative "High-Framerate Frame-Mixing" technique to fundamentally alter a video's data fingerprint, designed to bypass originality detection/deduplication mechanisms on major short-video platforms.
-   **[Video Mover](https://github.com/toki-plus/video-mover)**: A fully automated content creation pipeline that monitors and downloads videos, performs multi-dimensional deduplication, generates AI titles, and publishes to multiple platforms with one click.

## 🤝 Contributing

Contributions of any kind are welcome! If you have ideas for new features, found a bug, or have any suggestions for improvement, please:
-   Submit an [Issue](https://github.com/toki-plus/ai-mixed-cut/issues) to start a discussion.
-   Fork this repository and submit a [Pull Request](https://github.com/toki-plus/ai-mixed-cut/pulls).

If this project has been helpful to you, please consider giving it a ⭐!

## 📜 License

This project is open-sourced under the MIT License. See the [LICENSE](LICENSE) file for details.
