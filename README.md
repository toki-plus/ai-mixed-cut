# AI Mixed-Cut: AI智能混剪工作流

[简体中文](./README.md) | [English](./README_en.md)

[![GitHub stars](https://img.shields.io/github/stars/toki-plus/ai-mixed-cut?style=social)](https://github.com/toki-plus/ai-mixed-cut/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/toki-plus/ai-mixed-cut?style=social)](https://github.com/toki-plus/ai-mixed-cut/network/members)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/toki-plus/ai-mixed-cut/pulls)

**AI Mixed-Cut 是一款颠覆性的AI内容生产工具，它通过“解构-重构”的独特模式，将现有视频内容深度解析为可复用的创作素材库，并基于此全自动地生成源源不断的、高度原创的全新短视频。**

本项目旨在为内容创作者提供一套从模仿到超越的终极解决方案，摆脱传统“洗稿”和“去重”的低效困境，进入真正意义上的智能化、规模化、原创化内容生产新时代。

<p align="center">
  <a href="https://www.bilibili.com/video/BV1aAxQeLEu1" target="_blank">
    <img src="./assets/images/cover_demo.png" alt="点击观看B站演示视频（暂未录制）" width="800"/>
  </a>
  <br>
  <em>(点击封面图跳转到 B 站观看高清演示视频)</em>
</p>

---

## ✨ 核心功能

本项目以一个三阶段的智能化流水线，重新定义了视频内容的二次创作：

### 模块一：AI 内容引擎 (AI Content Engine)

-   **✍️ 一键提取文案**: 输入抖音分享链接，自动提取视频的完整标题、标签和口播稿。
-   **🧩 深度解构素材库**:
    -   **主题解构**: 提炼视频的核心选题、目标人群和价值主张，形成 `topics.json`。
    -   **框架解构**: 抽象视频的叙事结构和内容公式，形成 `frameworks.json`。
    -   **金句解构**: 挖掘并存储具有普适性的高质量句子，形成 `golden_sentences.json`。
-   **🧬 智能重构新文案**:
    -   从已解构的素材库中随机抽取“主题”、“框架”和“金句”。
    -   调用AI大模型，遵循指定的框架和主题，将金句作为观点融入，创作出结构相似但内容全新的原创文案。
    -   自动生成配套的爆款标题、标签和封面文案。

### 模块二：智能音频合成 (Intelligent Audio Synthesis)

-   **🎙️ 高品质人声**: 集成微软 Edge TTS，提供多语言、多情感的自然人声，支持语速、音调、音量精细调节。
-   **📜 自动生成字幕**: 在生成音频的同时，同步创建时间轴精准的 `.srt` 字幕文件。
-   **✂️ 智能断句优化**: 采用先进算法，对生成的字幕进行二次处理，根据语义和视觉效果优化断句和换行，提升观众阅读体验。

### 模块三：电影级视频生成 (Cinematic Video Generation)

-   **🎞️ 动态素材拼接**: 支持配置多个视频素材文件夹，按顺序或随机拼接，并可设定每个素材的“固定时长”、“随机时长”或“原始时长”。
-   **💥 高级视觉特效**:
    -   **电影级调色 (LUT)**: 随机应用专业级 LUT 滤镜，一键提升视频质感。
    -   **动态视觉效果**: 包含动态缩放运镜、随机旋转、色彩偏移、纹理噪声、背景模糊等多种效果，极大丰富画面层次。
    -   **动态遮罩与画中画**: 随机叠加艺术遮罩或动态视频素材，增加视觉独特性。
    -   **智能转场**: 在拼接长视频时，可启用多种炫酷的 `xfade` 视频转场。
-   **🚀 硬件加速**: 全面支持 NVIDIA (NVENC) 显卡进行硬件编码，大幅缩短视频渲染时间。
-   **GUI 与工作流**:
    -   提供完整图形界面，所有参数一目了然，支持一键启动完整工作流。
    -   支持分模块独立运行，方便调试和测试。

## 📸 软件截图

<p align="center">
  <img src="./images/cover_software.png" alt="软件主界面" width="800"/>
  <br>
  <em>软件主界面，四大模块化工作流清晰可见。</em>
</p>

## 🚀 快速开始

### 系统要求

1.  **操作系统**: Windows。
2.  **软件/工具**:
    | 软件/工具           | 下载/安装说明                                                 | 备注                                              |
    | :------------------ | :------------------------------------------------------------ | :------------------------------------------------ |
    | **FFmpeg**          | [Gyan.dev Builds](https://www.gyan.dev/ffmpeg/builds/)        | **必须**解压并将其 `bin` 目录添加到系统环境变量。 |
    | **Google Chrome**   | [官方下载](https://www.google.com/chrome/)                    | AI 功能需要，用于驱动浏览器与豆包交互。           |

### 安装与配置

-   **下载链接**: https://download.llxoxll.com/latest/yanqu_mixed_cut_v2

## 📖 使用指南

1.  **登录豆包**:
    -   在“模块一”中，点击 **“登录/刷新会话”** 按钮。
    -   在弹出的浏览器中扫码登录豆包。
    -   **登录成功后，手动关闭该浏览器窗口**，程序会自动保存登录状态。
2.  **配置工作流**:
    -   **模块一**: 在文本框中粘贴多个抖音视频分享链接，每行一个。
    -   **模块二**: 选择喜欢的语言、性别和具体语音，可拖动滑块微调语速、音量和音调。
    -   **模块三**:
        -   点击“添加素材组”，配置至少一个本地视频素材文件夹。
        -   根据需要勾选各种视频特效。
    -   **模块四**: 在“硬件与任务”部分，设置GPU并发数、生成数量等。
3.  **执行任务**:
    -   **分步执行 (推荐首次使用)**:
        1.  点击 **“开始提取”**，等待AI完成文案提取。
        2.  点击 **“开始解构”**，建立你自己的创作素材库。
        3.  点击 **“开始完整工作流”**，此时程序将自动执行“重构-生成音频-生成视频”的完整流程。
    -   **一键执行**: 在配置完成后，直接点击 **“开始完整工作流”**，程序将从重构新文案开始，全自动执行所有后续步骤。
4.  **查看结果**: 所有中间文件和最终视频都保存在 `output` 文件夹中，方便查看和管理。

---

<p align="center">
  <strong>业务定制与技术交流，请添加：</strong>
</p>
<table align="center">
  <tr>
    <td align="center">
      <img src="./images/wechat.png" alt="微信二维码" width="200"/>
      <br />
      <sub><b>个人微信</b></sub>
      <br />
      <sub>微信号: toki-plus (请备注“GitHub定制”)</sub>
    </td>
    <td align="center">
      <img src="./images/gzh.png" alt="公众号二维码" width="200"/>
      <br />
      <sub><b>公众号</b></sub>
      <br />
      <sub>获取最新技术分享</sub>
    </td>
  </tr>
</table>

## 📂 我的其他开源项目

-   **[Netease Downloader](https://github.com/toki-plus/netease-downloader)**: 一款优雅、功能丰富的网易云音乐下载器，支持无损/高品质音质、歌单/专辑批量下载、扫码登录和自动写入ID3元数据。
-   **[AI-Trader-For-MT4](https://github.com/toki-plus/ai-trader-for-mt4)**: 革命性开源框架，将大语言模型（LLM）转变为能在MetaTrader 4（MT4）平台上进行自主交易的AI代理。
-   **[Auto USPS Tracker](https://github.com/toki-plus/auto-usps-tracker)**: 专为跨境电商卖家设计的高效USPS批量物流追踪器，支持防屏蔽抓取并生成精美Excel报告。
-   **[AI Video Workflow](https://github.com/toki-plus/ai-video-workflow)**: 全自动AI原生视频生成工作流，集成文生图、图生视频和文生音乐模型，一键创作AIGC短视频。
-   **[AI Highlight Clip](https://github.com/toki-plus/ai-highlight-clip)**: AI驱动的智能剪辑工具，全自动从长视频分析、提取“高光时刻”，并生成爆款标题。
-   **[AI TTV Workflow](https://github.com/toki-plus/ai-ttv-workflow)**: AI驱动的文本转视频工具，自动将文案转化为带配音、字幕和封面的短视频，支持文案提取/二创/翻译。
-   **[AB Video Deduplicator](https://github.com/toki-plus/AB-Video-Deduplicator)**: 创新“高帧率抽帧混合”技术，重构视频数据指纹，规避短视频平台原创度检测/查重机制。
-   **[Video Mover](https://github.com/toki-plus/video-mover)**: 全自动化内容创作流水线，自动监听下载视频、多维度去重、AI生成标题，一键发布多平台。

## 🤝 参与贡献

欢迎任何形式的贡献！如果你有新的功能点子、发现了Bug，或者有任何改进建议，请：
-   提交一个 [Issue](https://github.com/toki-plus/ai-mixed-cut/issues) 进行讨论。
-   Fork 本仓库并提交 [Pull Request](https://github.com/toki-plus/ai-mixed-cut/pulls)。

如果这个项目对你有帮助，请不吝点亮一颗 ⭐！
