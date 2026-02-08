## 工业界最新动向

*   **Portview 推出针对 Linux 的诊断优先端口查看工具**
    一款轻量级（约 930 KB）、零依赖的 Linux 命令行工具，旨在简化端口占用查询，无需记忆复杂的 lsof 或 netstat 命令。[Show HN: Portview, A diagnostic-first port viewer for Linux](https://github.com/Mapika/portview)

*   **Matchlock 为 AI 智能体提供基于 Linux 的沙箱环境**
    针对 AI 智能体（AI Agents）开发的 Linux 沙箱系统，旨在提升运行 AI 生成代码时的安全性。[Matchlock: Linux-based sandboxing for AI agents](https://github.com/jingkaihe/matchlock)

*   **KDE Linux 桌面环境近期动态更新**
    KDE 项目分享了过去几个月的忙碌进展，涵盖了桌面环境的性能优化与功能改进。[Busy Months in KDE Linux](https://pointieststick.com/2026/02/06/busy-months-in-kde-linux/)

*   **媒体评测：重回 Linux 桌面后的体验反思**
    The Verge 发布文章讨论了从其他系统回归 Linux 后的挫折体验，引发了关于 Linux 桌面易用性的广泛讨论。[I went back to Linux and it was a mistake](https://www.theverge.com/report/875077/linux-was-a-mistake)

*   **ReKindle：专为电子墨水屏设计的 Web 操作系统**
    一款针对 E-ink 设备优化的新型操作系统，采用 Web 技术构建，旨在提升电子阅读器等设备的交互体验。[ReKindle – web-based operating system designed specifically for E-ink devices](https://rekindle.ink)

*   **CodeVerse Linux：面向开发者的 Arch Linux 衍生版**
    社区驱动的 Arch Linux 发行版，预设 Wayland 桌面环境，旨在为开发者提供简洁、快速且开箱即用的系统体验。[Show HN: The CodeVerse Hub Linux](https://github.com/TheCodeVerseHub/CodeVerseLinuxDistro)

*   **Wine 11.2 版本发布，增强跨平台应用兼容性**
    Wine 11.2 正式发布，继续改进在 Linux、BSD 和 macOS 上运行 Windows 应用程序的能力。[Wine 11.2 – Run Windows Applications on Linux, BSD, Solaris and macOS](https://gitlab.winehq.org/wine/wine/-/releases/wine-11.2)

*   **BreezyBox：在 ESP32-S3 上实现类 DOS 的非 Linux 壳层环境**
    展示了在嵌入式硬件上运行的轻量级系统环境，包含 Shell、应用安装器及 Vi 编辑器，无需完整的 Linux 内核。[Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)

*   **Linux From Scratch (LFS) 宣布停止支持 System V 版本**
    由于维护人力有限及上游变化剧烈，LFS 项目决定放弃 System V 初始化系统的版本，未来将专注于 systemd。[Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)

*   **多款开源生产力软件发布重大更新**
    数字音频工作站 Ardour 9.0 和办公套件 LibreOffice 26.2 相继发布，带来了性能提升和新功能支持。[Ardour 9.0 released](https://lwn.net/Articles/1057548/) | [LibreOffice 26.2 released](https://lwn.net/Articles/1057256/)

*   **本周多发行版发布安全更新**
    包括 Debian、Fedora、SUSE、Ubuntu 及 AlmaLinux 在内的多个发行版发布了针对内核、Python 及各类库的安全补丁。[Security updates for Friday](https://lwn.net/Articles/1057506/)

## 学术界最新研究

*   **研究评估 AI 智能体团队在软件工程任务中的协作效率**
    论文通过 SWE-Verified 基准测试，探讨了多智能体协作模式在解决真实 GitHub 问题时是否优于单一强力智能体。[Show HN: Measuring how AI agent teams improve issue resolution on SWE-Verified](https://arxiv.org/abs/2602.01465)

## Linux 内核社区热点与趋势

*   **内核开发者提议引入内置机器学习库 (ML-Lib)**
    Viacheslav Dubeyko 提交了在 Linux 内核中集成机器学习库的 RFC，旨在利用 ML 模型优化内核子系统的逻辑配置与推理。[ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC) (来源: Phoronix/LWN)

*   **Linux 内核交换子系统现代化：告别 swap map**
    内核社区正在推进交换子系统的重构，计划用新的“交换表”结构取代旧的 swap map，以简化代码并提升性能。[Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/) (来源: LWN)

*   **GCC 17 将支持内核控制流完整性 (CFI)**
    Kees Cook 提交的补丁集有望让 GCC 支持 `-fsanitize=kcfi` 标志，从而为内核提供与 Clang 类似的转发沿 CFI 保护。[Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/) (来源: LWN)

*   **Futex Robust List API 面临重构**
    针对现有 Robust Futex API 在处理锁清理时的缺陷，开发者在 Linux Plumbers 会议上讨论了新的 API 设计方案以修复竞态条件。[API changes for the futex robust list](https://lwn.net/Articles/1056387/) (来源: LWN)

*   **Linux 6.19-rc8 及多个稳定版内核发布**
    Linus Torvalds 发布了 6.19 的第 8 个候选版本；同时 Greg Kroah-Hartman 发布了包括 6.18.9、6.12.69 在内的六个稳定分支更新。[6.19-rc8: mainline](https://www.kernel.org/) | [Six stable kernels for Friday](https://lwn.net/Articles/1057550/)

## 业界大厂动向

*   **Meta 分享如何将 Linux 内核转化为全球规模的负载均衡器**
    Meta 详细介绍了其对 Linux 内核的深度定制，使其能够支撑起行星级规模的网络流量分发与负载均衡。[How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)

*   **Arm 与 Google 协作推进 Rust 编写的 GPU 驱动项目 Tyr**
    Tyr 项目旨在为 Arm Mali 硬件开发 Rust 语言驱动，目前已能运行 3D 游戏，并计划在 2026 年推进上游合并，响应内核对 Rust 驱动的要求。[The future for Tyr](https://lwn.net/Articles/1055590/) (来源: LWN)

*   **Google 及其合作伙伴推动 AI 智能体安全中间件 Latch**
    针对 AI 智能体访问关键系统的风险，开源了名为 Latch 的安全代理，用于拦截并审核智能体的工具调用。[Show HN: Latch – Open-source security middleware for AI agents](https://www.latchagent.com/)

---

## 参考链接

### Hacker News

- [Show HN: Portview, A diagnostic-first port viewer for Linux (~930 KB, zero deps)](https://github.com/Mapika/portview)
- [Matchlock: Linux-based sandboxing for AI agents](https://github.com/jingkaihe/matchlock)
- [Busy Months in KDE Linux](https://pointieststick.com/2026/02/06/busy-months-in-kde-linux/)
- [I went back to Linux and it was a mistake](https://www.theverge.com/report/875077/linux-was-a-mistake)
- [Show HN: Measuring how AI agent teams improve issue resolution on SWE-Verified](https://arxiv.org/abs/2602.01465)
- [ReKindle – web-based operating system designed specifically for E-ink devices](https://rekindle.ink)
- [How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)
- [Show HN: The Codeverse Hub Linux](https://github.com/TheCodeVerseHub/CodeVerseLinuxDistro)
- [Show HN: I'm 75, building an OSS Virtual Protest Protocol for digital activism](https://github.com/voice-of-japan/Virtual-Protest-Protocol/blob/main/README.md)
- [BTDUex Safe? The Back End Withdrawal Anomalies](https://news.ycombinator.com/item?id=46922244)
- [Show HN: Portview what's on your ports (diagnostic-first, single binary, Linux)](https://github.com/Mapika/portview)
- [Wine 11.2 – Run Windows Applications on Linux, BSD, Solaris and macOS](https://gitlab.winehq.org/wine/wine/-/releases/wine-11.2)
- [Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)
- [Machine Learning library in Linux kernel](https://lore.kernel.org/lkml/20260206191136.2609767-1-slava@dubeyko.com/)
- [ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC)
- [Show HN: Latch – Open-source security middleware for AI agents](https://www.latchagent.com/)

### LWN.net

- [An in-kernel machine-learning library](https://lwn.net/Articles/1057569/)
- [Six stable kernels for Friday](https://lwn.net/Articles/1057550/)
- [Ardour 9.0 released](https://lwn.net/Articles/1057548/)
- [[$] Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/)
- [Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)
- [Security updates for Friday](https://lwn.net/Articles/1057506/)
- [[$] Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/)
- [Security updates for Thursday](https://lwn.net/Articles/1057381/)
- [[$] LWN.net Weekly Edition for February 5, 2026](https://lwn.net/Articles/1056417/)
- [[$] API changes for the futex robust list](https://lwn.net/Articles/1056387/)
- [[$] Sigil simplifies creating and editing EPUBs](https://lwn.net/Articles/1054751/)
- [LibreOffice 26.2 released](https://lwn.net/Articles/1057256/)
- [Security updates for Wednesday](https://lwn.net/Articles/1057247/)
- [[$] The future for Tyr](https://lwn.net/Articles/1055590/)
- [Security updates for Tuesday](https://lwn.net/Articles/1057047/)

### Linux Weekly News (RSS)

- [An in-kernel machine-learning library](https://lwn.net/Articles/1057569/)
- [Six stable kernels for Friday](https://lwn.net/Articles/1057550/)
- [Ardour 9.0 released](https://lwn.net/Articles/1057548/)
- [[$] Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/)
- [Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)
- [Security updates for Friday](https://lwn.net/Articles/1057506/)
- [[$] Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/)
- [Security updates for Thursday](https://lwn.net/Articles/1057381/)
- [[$] LWN.net Weekly Edition for February 5, 2026](https://lwn.net/Articles/1056417/)
- [[$] API changes for the futex robust list](https://lwn.net/Articles/1056387/)
- [[$] Sigil simplifies creating and editing EPUBs](https://lwn.net/Articles/1054751/)
- [LibreOffice 26.2 released](https://lwn.net/Articles/1057256/)
- [Security updates for Wednesday](https://lwn.net/Articles/1057247/)
- [[$] The future for Tyr](https://lwn.net/Articles/1055590/)
- [Security updates for Tuesday](https://lwn.net/Articles/1057047/)

### Kernel.org

- [6.18.9: stable](https://www.kernel.org/)
- [6.12.69: longterm](https://www.kernel.org/)
- [6.6.123: longterm](https://www.kernel.org/)
- [6.1.162: longterm](https://www.kernel.org/)
- [5.15.199: longterm](https://www.kernel.org/)
- [5.10.249: longterm](https://www.kernel.org/)
- [next-20260205: linux-next](https://www.kernel.org/)
- [6.19-rc8: mainline](https://www.kernel.org/)
