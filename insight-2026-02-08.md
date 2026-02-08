## 工业界最新动向

**Wine 11.2 及其暂存版发布，增强对 Linux 下 Photoshop 的支持**
Wine 项目近日发布了 11.2 正式版及其 Staging 暂存版，继续提升在 Linux、macOS 和 BSD 等系统上运行 Windows 应用的能力。本次更新的重点在于引入了更多针对 Adobe Photoshop 的兼容性补丁，旨在解决该专业软件在非 Windows 环境下的运行稳定性问题。这对于希望在 Linux 平台上进行专业图像处理的用户来说是一个重要的进展。
原文：[Wine-Staging 11.2 Brings More Patches to Help Adobe Photoshop on Linux](https://www.phoronix.com/news/Wine-Staging-11.2)

**Linux From Scratch (LFS) 宣布停止支持 System V 版本**
著名的 Linux From Scratch 项目宣布将不再维护基于 System V 的发行版本，未来将全面转向 systemd。官方表示这一决定主要是由于维护压力过大，志愿者团队难以同时兼顾两套初始化系统的海量上游更新。这意味着 Linux 社区中坚持传统初始化系统的阵地进一步缩小，systemd 的主流地位更加稳固。
原文：[Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)

**LibreOffice 26.2 正式发布，提升复杂文档处理性能**
开源办公套件 LibreOffice 推出了 26.2 版本，重点改进了日常办公中的交互流畅度。新版本增强了与专有文档格式的兼容性，并在处理大型复杂表格和文档时表现出更好的响应速度。该版本继续强调隐私保护与开放标准，确保用户在无需订阅的情况下拥有对文档的完全控制权。
原文：[LibreOffice 26.2 released](https://lwn.net/Articles/1057256/)

**BreezyBox：在 ESP32-S3 上实现无需 Linux 的类 DOS 体验**
开发者展示了一个名为 BreezyBox 的项目，它在 ESP32-S3 微控制器上构建了一个包含 Shell、Vi 编辑器和应用安装器的环境，而无需运行完整的 Linux 内核。该项目通过自定义的快速文本模式驱动程序，为嵌入式设备带来了类似早期 DOS 时代的开发体验。这种轻量级方案为低功耗硬件上的交互式应用提供了新的可能性。
原文：[Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)

**多款 Linux 发行版发布安全更新，涵盖内核与关键组件**
包括 AlmaLinux、Debian、Fedora、SUSE 和 Ubuntu 在内的多个主流发行版近期密集发布了安全补丁。更新内容涉及 Linux 内核漏洞修复、Python 运行环境安全增强以及 Chromium、OpenSSL 等核心组件的加固。建议系统管理员及时检查并应用这些更新，以防范潜在的安全风险。
原文：[Security updates for Friday](https://lwn.net/Articles/1057506/)

## 学术界最新研究

本节今日暂无突出动态。

## Linux 内核社区热点与趋势

**内核机器学习库 (ML-Lib) 提案引发社区关注**
开发者 Viacheslav Dubeyko 提交了一份在 Linux 内核中引入机器学习库的 RFC 提案，旨在通过 ML 模型优化内核子系统的逻辑配置。该库计划支持数据采集、模型训练、测试及推理过程，例如利用 eBPF 注入合成逻辑。虽然目前该提案尚处于早期阶段且缺乏详尽文档，但它开启了内核自适应优化和智能化管理的新讨论方向。
原文：[ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC)

**GCC 编译器将支持内核控制流完整性 (CFI) 保护**
内核安全专家 Kees Cook 提交了一套补丁，旨在为 GCC 编译器添加 `-fsanitize=kcfi` 支持，该功能此前仅在 Clang 中可用。CFI 技术通过保护间接函数调用，能有效防止攻击者通过劫持跳转指令来控制系统。这一改进预计将随 GCC 17 发布，届时使用 GCC 编译的 Linux 内核将获得更强的安全防御能力。
原文：[Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/)

**内核交换 (Swap) 子系统现代化：告别旧有的 Swap Map**
Linux 内核正在推进交换子系统的重构工作，计划用新的“交换表 (Swap Table)”结构取代过时的数据结构。这一系列改进旨在简化交换逻辑并提升处理速度，相关代码已排入后续的开发周期。完成现代化改造后，内核在内存压力下的页面交换效率将得到显著提升。
原文：[Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/)

**Tyr 项目：使用 Rust 为 Arm Mali GPU 开发驱动程序**
由 Arm、Collabora 和 Google 联合推进的 Tyr 项目展示了其在 Rust 编写 GPU 驱动方面的最新进展，已能成功运行 3D 游戏。随着内核 DRM 子系统计划在未来一年内强制要求新驱动使用 Rust 编写，Tyr 的经验将成为行业标杆。该项目计划在 2026 年完成上游合并，标志着 Rust 在高性能图形驱动领域的正式落地。
原文：[The future for Tyr](https://lwn.net/Articles/1055590/)

**Linux 内核发布多个稳定版及 6.19-rc8 预发布版**
内核维护者 Greg Kroah-Hartman 发布了包括 6.18.9、6.12.69 在内的六个稳定分支更新，修复了大量已知问题。同时，主线版本也迎来了 6.19-rc8，标志着新版本已进入最后的稳定化阶段。用户和发行版厂商被建议尽快升级到最新的稳定分支以获取关键修复。
原文：[Six stable kernels for Friday](https://lwn.net/Articles/1057550/)

## 业界大厂动向

**Meta 分享如何将 Linux 内核转化为全球规模的负载均衡器**
Meta（原 Facebook）详细介绍了其利用 Linux 内核特性构建全球负载均衡系统的技术实践。通过深度定制内核网络栈和利用 eBPF 等技术，Meta 实现了在海量流量下的高效调度与故障隔离。这一案例展示了顶级互联网公司如何通过改造通用内核来支撑其庞大的基础设施需求。
原文：[How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)

## 云原生领域

本节今日暂无突出动态。

## AI 领域

**SpaceX 与 xAI 的潜在合并：构建“冯·诺依曼”式自我复制基础设施**
关于 SpaceX 与 xAI 可能合并的讨论引发了对未来基础设施的遐想，核心在于构建具备自我复制能力的 AI 驱动系统。该愿景涵盖了轨道数据中心、月球制造工厂以及利用 AI 机器人进行小行星采矿。这种结合可能将 AI 从纯软件层面推向物理世界的指数级扩张，实现真正意义上的地外文明基础设施建设。
原文：[SpaceX-xAI Merger: Nobody's Talking About the von Neumann Elephant in the Room](https://news.ycombinator.com/item?id=46933827)

**Matchlock：利用 Linux 沙箱保护 AI Agent 工作负载**
Matchlock 项目推出了一种基于 Linux 的沙箱机制，专门用于安全地运行 AI 代理（AI Agent）任务。随着 AI 代理在系统操作中的权限增加，如何防止其误操作或恶意行为成为关键挑战。Matchlock 通过内核级的隔离技术，为 AI 代理提供了一个受限的执行环境，确保其在完成任务的同时不会危害宿主系统安全。
原文：[Matchlock – Secures AI agent workloads with a Linux-based sandbox](https://github.com/jingkaihe/matchlock)

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
