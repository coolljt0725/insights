## 工业界最新动向

**Wine 11.2 发布，持续优化 Linux 上的 Adobe Photoshop 体验**
Wine 社区发布了 11.2 开发版本，其 Staging 分支引入了更多针对 Adobe Photoshop 的兼容性补丁。该版本致力于解决在 Linux 环境下运行大型专业软件时的图形渲染和 API 调用问题。随着补丁的不断完善，Linux 用户在无需虚拟机的情况下运行高性能创意软件的体验将得到显著提升。
原文：[Wine-Staging 11.2 Brings More Patches to Help Adobe Photoshop on Linux](https://www.phoronix.com/news/Wine-Staging-11.2)

**Linux From Scratch (LFS) 宣布放弃 System V 版本**
著名的「从零开始构建 Linux」项目 LFS 宣布将停止维护 System V 初始化系统的版本，未来将全面转向 systemd。官方表示，由于上游软件包更新量巨大，完全依赖志愿者的编辑团队已无法承受同时维护两套初始化系统的负担。这一决定标志着在自定义系统构建领域，传统的 System V 正在加速退出历史舞台。
原文：[Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)

**ReKindle：专为电子墨水屏设备设计的 Web 操作系统**
ReKindle 是一款新兴的基于 Web 技术的操作系统，旨在为各类 E-ink（电子墨水屏）设备提供流畅的交互体验。该系统针对电子墨水屏刷新率低的特性进行了深度优化，通过轻量化的架构提升响应速度。这为旧款电子阅读器的重获新生以及新型低功耗设备的开发提供了新的软件平台。
原文：[ReKindle – web-based operating system designed specifically for E-ink devices](https://rekindle.ink)

**BreezyBox：在 ESP32 上实现无需 Linux 的类 DOS 交互环境**
开发者推出了 BreezyBox 项目，在 ESP32-S3 微控制器上实现了包含 Shell、应用安装程序和 Vi 编辑器的完整环境，且不依赖 Linux 内核。该项目通过自定义的快速文本模式驱动程序，在嵌入式硬件上复刻了早期 DOS 时代的编程体验。这种「去内核化」的尝试为资源受限的物联网设备提供了一种极简且高效的开发思路。
原文：[Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)

**Matchlock：基于 Linux 沙箱的 AI 智能体安全工作负载方案**
Matchlock 是一个利用 Linux 内核安全特性构建的沙箱环境，专门用于保护 AI 智能体（AI Agents）的运行负载。它通过严格的隔离机制防止 AI 模型在执行任务时对宿主系统造成潜在威胁。随着 AI 自动化工具的普及，这种针对 AI 场景优化的内核级安全方案正成为工业界关注的重点。
原文：[Matchlock – Secures AI agent workloads with a Linux-based sandbox](https://github.com/jingkaihe/matchlock)

---

## 学术界最新研究

**本节今日暂无突出动态**

---

## Linux 内核社区热点与趋势

**内核机器学习库 ML-Lib 提案引发社区关注**
开发者 Viacheslav Dubeyko 提交了一份在 Linux 内核中引入机器学习库（ML-Lib）的 RFC 提案。该库旨在通过 ML 模型优化内核子系统的逻辑配置，例如根据内部状态动态调整 I/O 调度或内存管理策略。尽管这一想法极具前瞻性，但由于缺乏详细文档和实际应用案例，目前在社区中仍存在关于内核复杂性和安全性的广泛讨论。
原文：[ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC)

**内核交换子系统现代化：从 Swap Map 转向 Swap Table**
Linux 内核正在推进交换（Swap）子系统的重构工作，计划用全新的「Swap Table」结构取代陈旧的「Swap Map」。这一改进旨在简化内核处理交换空间的逻辑，并显著提升在高负载下的内存交换速度。预计在接下来的几个内核发布周期中，用户将感受到更高效的内存管理性能。
原文：[Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/)

**GCC 17 将引入内核控制流完整性（CFI）支持**
安全专家 Kees Cook 提交了一套补丁，旨在为 GCC 编译器添加内核控制流完整性（CFI）支持，该特性此前主要由 Clang 提供。CFI 技术通过限制间接跳转的范围，能有效防御多种旨在劫持内核执行流的攻击。如果该补丁顺利并入 GCC 17，将进一步统一 Linux 内核在不同编译器下的安全防护水平。
原文：[Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/)

**内核发布动态：6.19-rc8 发布与多版本稳定版更新**
Linus Torvalds 发布了 6.19-rc8，标志着新内核版本已进入最后的打磨阶段。与此同时，Greg Kroah-Hartman 发布了包括 6.18.9、6.12.69 在内的六个稳定版内核更新，修复了大量安全漏洞和功能错误。社区强烈建议所有生产环境用户及时升级到最新的稳定分支以确保系统安全。
原文：[Six stable kernels for Friday](https://lwn.net/Articles/1057550/)

**Tyr 项目：利用 Rust 为 Arm Mali GPU 开发驱动程序**
由 Arm、Collabora 和 Google 联合发起的 Tyr 项目取得了重要进展，成功在 Rust 编写的驱动上运行了 3D 游戏。该项目响应了内核 DRM 子系统未来可能强制要求使用 Rust 编写新驱动的趋势。Tyr 的成功不仅证明了 Rust 在复杂图形驱动开发中的可行性，也为 Arm 架构设备的开源驱动支持开辟了新路径。
原文：[The future for Tyr](https://lwn.net/Articles/1055590/)

---

## 业界大厂动向

**Meta：将 Linux 内核转化为全球规模的负载均衡器**
Meta（原 Facebook）分享了其如何利用 eBPF 和 XDP 技术，将标准的 Linux 内核改造为支撑全球业务的负载均衡系统。通过在内核早期阶段处理数据包，Meta 实现了极高的吞吐量和极低的延迟，摆脱了传统硬件负载均衡器的限制。这一实践充分展示了 Linux 内核在可编程网络领域的巨大潜力。
原文：[How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)

**SpaceX 与 xAI 愿景：轨道数据中心与自复制基础设施**
埃隆·马斯克旗下的 SpaceX 与 xAI 正在探讨更深层次的整合，其核心在于构建「轨道数据中心」以规避地球能源限制。该愿景还涉及利用 AI 驱动的机器人构建自复制的月球工厂和星际基础设施。虽然这一计划听起来带有科幻色彩，但其对分布式操作系统和极端环境下系统稳定性的要求，正推动着相关前沿技术的研发。
原文：[SpaceX-xAI Merger: Nobody's Talking About the von Neumann Elephant in the Room](https://news.ycombinator.com/item?id=46933827)

**Google 与 Collabora 推动内核 Futex API 改进**
针对 Linux 游戏性能中的瓶颈，来自 Google 和 Collabora 的开发者正在推动 Futex Robust List API 的变更。该提案旨在解决现有 API 在处理进程异常退出时锁清理不彻底的竞态条件问题。这一改进对于提升 Steam Deck 等 Linux 游戏设备的系统稳定性和多线程性能具有重要意义。
原文：[API changes for the futex robust list](https://lwn.net/Articles/1056387/)

---

## 参考链接

### Hacker News

- [SpaceX-xAI Merger: Nobody's Talking About the von Neumann Elephant in the Room](https://news.ycombinator.com/item?id=46933827)
- [Wine-Staging 11.2 Brings More Patches to Help Adobe Photoshop on Linux](https://www.phoronix.com/news/Wine-Staging-11.2)
- [Show HN: Portview, A diagnostic-first port viewer for Linux (~930 KB, zero deps)](https://github.com/Mapika/portview)
- [Matchlock – Secures AI agent workloads with a Linux-based sandbox](https://github.com/jingkaihe/matchlock)
- [Busy Months in KDE Linux](https://pointieststick.com/2026/02/06/busy-months-in-kde-linux/)
- [I went back to Linux and it was a mistake](https://www.theverge.com/report/875077/linux-was-a-mistake)
- [ReKindle – web-based operating system designed specifically for E-ink devices](https://rekindle.ink)
- [How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)
- [Show HN: The Codeverse Hub Linux](https://github.com/TheCodeVerseHub/CodeVerseLinuxDistro)
- [BTDUex Safe? The Back End Withdrawal Anomalies](https://news.ycombinator.com/item?id=46922244)
- [Show HN: Portview what's on your ports (diagnostic-first, single binary, Linux)](https://github.com/Mapika/portview)
- [Wine 11.2 – Run Windows Applications on Linux, BSD, Solaris and macOS](https://gitlab.winehq.org/wine/wine/-/releases/wine-11.2)
- [Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)
- [Machine Learning library in Linux kernel](https://lore.kernel.org/lkml/20260206191136.2609767-1-slava@dubeyko.com/)
- [ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC)

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
