## 工业界最新动向

**Linux From Scratch (LFS) 宣布停止支持 System V 初始化系统**
历史悠久的 Linux From Scratch (LFS) 项目宣布将不再发布基于 System V 的版本，未来将全面转向 systemd。官方表示，由于上游软件包更新极其频繁，且项目完全依赖志愿者，维护两个初始化系统的版本已导致工作量过载。这一决定反映了 systemd 在现代 Linux 生态中已占据绝对主导地位，即使是追求极致定制的社区也在向其靠拢。
原文：[Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)

**Matchlock：针对 AI 智能体的 Linux 沙箱环境**
Matchlock 是一款专门为 AI 智能体（AI Agents）设计的 Linux 沙箱工具，旨在解决 AI 运行不受控代码时的安全风险。它利用 Linux 内核的隔离特性，为 AI 任务创建一个受限的执行环境，防止其对宿主系统进行非法访问。随着 AI 自动化工具的普及，这种针对特定应用场景的系统级安全加固正成为工业界的新热点。
原文：[Matchlock: Linux-based sandboxing for AI agents](https://github.com/jingkaihe/matchlock)

**ReKindle：专为电子墨水屏设计的 Web 操作系统**
ReKindle 是一款针对 E-ink 电子墨水屏设备深度优化的 Web 操作系统，旨在提升此类设备的交互响应速度。该系统针对墨水屏低刷新率、高延迟的物理特性，在界面渲染和系统调度上做了特殊处理，试图打破传统 OS 在电子阅读器上的体验瓶颈。这为嵌入式设备和特殊显示技术的垂直整合提供了新的参考方案。
原文：[ReKindle – web-based operating system designed specifically for E-ink devices](https://rekindle.ink)

**BreezyBox：在 ESP32 上实现类 DOS 的非 Linux 开发体验**
开发者展示了名为 BreezyBox 的项目，在 ESP32-S3 微控制器上构建了一个包含 Shell、应用安装器和编辑器且不依赖 Linux 的完整环境。该项目规避了 Linux 内核在低功耗嵌入式设备上的沉重开销，提供了类似早期 DOS 时代的直接硬件操控感。它证明了在特定物联网场景下，轻量级自定义系统仍具有极高的开发效率和运行优势。
原文：[Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)

**多款 Linux 关键应用发布重大版本更新**
本周 Linux 生态迎来多个重要软件更新，包括 Wine 11.2 提升了 Windows 应用兼容性，LibreOffice 26.2 增强了文档处理性能，以及专业音频工作站 Ardour 9.0 的发布。这些更新进一步巩固了 Linux 在办公、专业创作及跨平台应用运行方面的实用性。同时，各大发行版如 Ubuntu、SUSE 和 Debian 也密集发布了针对内核及核心库的安全补丁。
原文：[Wine 11.2](https://gitlab.winehq.org/wine/wine/-/releases/wine-11.2) | [LibreOffice 26.2](https://lwn.net/Articles/1057256/) | [Ardour 9.0](https://lwn.net/Articles/1057548/)

---

## 学术界最新研究

本节今日暂无突出动态。

---

## Linux 内核社区热点与趋势

**内核机器学习库 ML-Lib 提议引发讨论**
开发者 Viacheslav Dubeyko 向内核邮件列表提交了一个名为 ML-Lib 的 RFC 补丁，提议在 Linux 内核中引入机器学习库。该库的目标是利用 ML 模型来优化内核子系统的逻辑配置，例如通过处理内部状态数据来动态调整 eBPF 逻辑。尽管目前该提案尚处于早期阶段且文档不足，但它展示了内核开发者试图引入智能化决策机制来应对复杂系统调优的趋势。
原文：[ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC)

**GCC 将引入内核控制流完整性（CFI）支持**
内核安全专家 Kees Cook 提交了一套补丁，旨在为 GCC 编译器添加对内核控制流完整性（KCFI）的支持。此前该功能主要由 Clang 编译器通过 `-fsanitize=kcfi` 提供，用于防止攻击者通过篡改间接函数调用来劫持执行流。一旦该补丁并入 GCC 17，将显著提升使用 GCC 构建的 Linux 内核的防御能力，缩小不同编译器间的安全特性差距。
原文：[Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/)

**内核交换子系统（Swap）启动现代化改造**
Linux 内核的交换子系统正在进行一系列数据结构重构，计划引入新的“交换表（Swap Table）”来取代陈旧的“交换映射（Swap Map）”。这一改进旨在简化内核处理内存交换的逻辑，减少锁竞争并提升在大内存、高并发场景下的性能。社区预计这些改动将在接下来的几个合并窗口中逐步落地，使交换子系统更加高效和易于维护。
原文：[Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/)

**Futex Robust List API 面临重构以解决竞态问题**
在 Linux Plumbers 会议上，开发者讨论了 Futex robust list API 存在的缺陷，该 API 用于确保进程异常退出时能正确释放锁。目前的实现存在难以触发的竞态条件，可能导致用户空间程序死锁或资源泄露。社区正在构思一套全新的 API 方案，以彻底解决 Linux 游戏和高性能计算中常见的同步可靠性问题。
原文：[API changes for the futex robust list](https://lwn.net/Articles/1056387/)

**六个稳定版内核分支同步更新**
内核维护者 Greg Kroah-Hartman 发布了包括 6.18.9、6.12.69 以及多个长期支持版本（5.15、5.10 等）在内的六个稳定版更新。这些版本修复了大量驱动程序和核心子系统中的 Bug，并包含关键的安全加固。社区强烈建议所有生产环境用户根据所使用的分支尽快完成升级。
原文：[Six stable kernels for Friday](https://lwn.net/Articles/1057550/)

---

## 业界大厂动向

**Meta：利用 Linux 内核构建全球规模的负载均衡器**
Meta（原 Facebook）分享了其如何深度定制 Linux 内核，将其转化为支撑全球流量的负载均衡系统。通过结合 eBPF 技术和对内核网络协议栈的优化，Meta 实现了在不牺牲性能的前提下进行灵活的流量调度。这一案例展示了顶级互联网公司如何通过改造开源内核，解决传统硬件负载均衡器无法应对的超大规模并发挑战。
原文：[How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)

**Tyr 项目：Arm、Google 与 Collabora 联手推进 Rust GPU 驱动**
由 Arm、Collabora 和 Google 联合发起的 Tyr 项目宣布取得重要进展，成功开发出用于 Arm Mali 硬件的 Rust 语言 GPU 驱动原型。该项目在 Linux Plumbers 会议上展示了其运行 3D 游戏的能力，性能表现优异。随着 Linux DRM 子系统计划在未来强制要求新驱动使用 Rust，Tyr 项目为移动端图形驱动的安全性与现代化树立了标杆。
原文：[The future for Tyr](https://lwn.net/Articles/1055590/)

**Google 与各厂商持续推送 Android 相关内核安全更新**
在最新的安全通报中，Google 联合 Oracle、Red Hat 和 Ubuntu 等厂商，针对 Linux 内核中的多个高危漏洞发布了补丁。这些漏洞涉及网络栈、虚拟化组件（qemu-kvm）以及文件系统权限管理。大厂的协同行动确保了从云端服务器到移动端 Android 设备的整个 Linux 生态能够快速响应潜在的安全威胁。
原文：[Security updates for Friday](https://lwn.net/Articles/1057506/)

---

## 参考链接

### Hacker News

- [Show HN: Portview, A diagnostic-first port viewer for Linux (~930 KB, zero deps)](https://github.com/Mapika/portview)
- [Matchlock: Linux-based sandboxing for AI agents](https://github.com/jingkaihe/matchlock)
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
