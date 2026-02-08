## 工业界最新动向

**Linux From Scratch (LFS) 宣布停止支持 System V 版本**
久负盛名的 Linux From Scratch (LFS) 项目宣布将不再维护基于 System V 的版本，未来将全面转向 systemd。官方表示这一决定主要是由于维护工作量巨大，目前所有编辑均为志愿者，面对上游数千个软件包的更新已不堪重负。这一变动标志着在 DIY Linux 社区中，传统的 init 系统正逐渐让位于现代化的初始化系统。
原文：[Linux from Scratch to drop System V versions](https://lwn.net/Articles/1057509/)

**ReKindle：专为电子墨水屏设计的 Web 操作系统**
ReKindle 是一款专门针对 E-ink 电子墨水设备优化的 Web 操作系统，旨在提升低刷新率屏幕上的阅读与交互体验。该系统通过 Web 技术提供了轻量化的界面，试图解决传统移动操作系统在电子书阅读器上运行缓慢的问题。它为各类电子阅读器和低功耗显示设备提供了一个统一且高效的软件平台。
原文：[ReKindle – web-based operating system designed specifically for E-ink devices](https://rekindle.ink)

**Wine 11.2 发布，持续提升跨平台兼容性**
Wine 项目发布了 11.2 版本，进一步增强了在 Linux、BSD 和 macOS 上运行 Windows 应用程序的能力。此版本包含多项性能优化和错误修复，特别是在处理复杂图形应用和办公软件方面表现更佳。对于希望从 Windows 迁移到 Linux 平台的专业用户和游戏玩家来说，这依然是不可或缺的兼容层工具。
原文：[Wine 11.2 – Run Windows Applications on Linux, BSD, Solaris and macOS](https://gitlab.winehq.org/wine/wine/-/releases/wine-11.2)

**Matchlock：为 AI 智能体打造的 Linux 沙箱环境**
Matchlock 是一款基于 Linux 的新型沙箱工具，专门用于隔离和运行 AI 智能体生成的代码。随着 AI 自动编程的普及，如何安全地执行未经审核的代码成为挑战，Matchlock 通过内核级隔离确保了执行环境的安全。该工具为开发者在构建自动化 AI 工作流时提供了一层关键的安全保障。
原文：[Matchlock: Linux-based sandboxing for AI agents](https://github.com/jingkaihe/matchlock)

**BreezyBox：无需 Linux 内核的 ESP32 嵌入式操作系统**
BreezyBox 为 ESP32-S3 芯片提供了一个类似 DOS 的操作环境，完全绕过了重量级的 Linux 内核。它内置了 Shell、应用安装程序和快速文本驱动，旨在为嵌入式开发提供极致的响应速度和低开销体验。这对于追求老派编程体验或在资源受限硬件上进行高性能开发的工程师极具吸引力。
原文：[Show HN: Look Ma, No Linux: Shell, App Installer, Vi, Cc on ESP32-S3 / BreezyBox](https://github.com/valdanylchuk/breezydemo)

**Portview：轻量级 Linux 端口诊断工具**
Portview 是一款仅 930 KB 且零依赖的 Linux 端口查看工具，旨在简化网络诊断流程。它通过直观的界面告诉用户哪些进程正在占用特定端口，从而替代了复杂的 `lsof` 或 `netstat` 命令组合。该工具采用单二进制文件分发，非常适合系统管理员在各类服务器环境中快速部署使用。
原文：[Show HN: Portview, A diagnostic-first port viewer for Linux (~930 KB, zero deps)](https://github.com/Mapika/portview)

**开源办公与创作软件迎来重大更新**
LibreOffice 26.2 和专业音频工作站 Ardour 9.0 相继发布。LibreOffice 重点改进了复杂文档的处理性能和与闭源格式的兼容性；而 Ardour 9.0 则引入了用户期待已久的 Region FX 和触摸屏支持。这些更新巩固了 Linux 在专业办公和多媒体创作领域的地位。
原文：[LibreOffice 26.2 released](https://lwn.net/Articles/1057256/)
原文：[Ardour 9.0 released](https://lwn.net/Articles/1057548/)

---

## 学术界最新研究

本节今日暂无突出动态。

---

## Linux 内核社区热点与趋势

**内核机器学习库 ML-Lib 提案引发关注**
开发者 Viacheslav Dubeyko 向内核邮件列表提交了在 Linux 内核中引入机器学习库（ML-Lib）的 RFC 提案。该库旨在允许内核子系统利用 ML 模型进行逻辑优化和配置调整，例如通过 eBPF 注入合成逻辑。虽然目前该提案还处于早期阶段且文档尚不完善，但它展示了内核向“智能化”自我优化演进的潜在方向。
原文：[ML-Lib: Machine Learning Library Proposed for the Linux Kernel](https://www.phoronix.com/news/Linux-Kernel-ML-LIB-RFC)

**GCC 17 将支持内核控制流完整性（CFI）**
内核安全专家 Kees Cook 提交了一套补丁，旨在为 GCC 编译器添加内核控制流完整性（CFI）支持。此前该功能主要依赖 Clang 的特定标志，GCC 的加入将使更多使用 GNU 工具链的发行版能够获得这一关键的安全防护。CFI 能够有效防止攻击者通过劫持间接跳转来利用系统漏洞，显著提升内核的防御能力。
原文：[Kernel control-flow-integrity support comes to GCC](https://lwn.net/Articles/1056601/)

**交换子系统现代化：告别 swap map**
Linux 内核正计划对交换（swap）子系统进行深度现代化改造，核心举措是用新的“交换表（swap table）”结构替换陈旧的 swap map。这项工作旨在简化内存管理代码并提升在高负载下的交换效率。预计在接下来的几个内核版本中，用户将看到更简洁、更快速的内存交换逻辑。
原文：[Modernizing swapping: the end of the swap map](https://lwn.net/Articles/1057102/)

**Futex Robust List API 改进讨论**
在 Linux Plumbers 会议上，开发者讨论了现有 robust futex API 存在的竞态条件等问题。该 API 负责在进程退出时清理其持有的锁，对 Linux 游戏性能和系统稳定性至关重要。社区正寻求通过新的 API 设计来彻底解决这些难以触发的边缘错误，以提供更可靠的用户态同步机制。
原文：[API changes for the futex robust list](https://lwn.net/Articles/1056387/)

**多版本稳定版内核与 6.19-rc8 发布**
内核维护者 Greg Kroah-Hartman 发布了包括 6.18.9、6.12.69 在内的六个稳定版内核更新，修复了大量已知漏洞。同时，Linus Torvalds 发布了 6.19-rc8，标志着新版本已进入最后的打磨阶段。建议所有生产环境用户及时跟进这些包含重要安全补丁的 LTS 更新。
原文：[Six stable kernels for Friday](https://lwn.net/Articles/1057550/)
原文：[6.19-rc8: mainline](https://www.kernel.org/)

---

## 业界大厂动向

**Meta 将 Linux 内核打造为全球规模的负载均衡器**
Meta（原 Facebook）分享了其如何深度定制 Linux 内核，将其转化为支撑全球业务的负载均衡系统。通过大规模应用 eBPF 技术和对内核网络栈的针对性修改，Meta 实现了极高的吞吐量和灵活的流量调度。这一案例充分展示了 Linux 内核在超大规模云基础设施中的可塑性和核心价值。
原文：[How Meta Made Linux a Planet-Scale Load Balancer](https://softwarefrontier.substack.com/p/how-meta-turned-the-linux-kernel)

**Arm、Google 与 Collabora 联合开发 Rust GPU 驱动**
由 Arm、Google 和 Collabora 联合发起的 Tyr 项目，成功为 Arm Mali 硬件开发出了基于 Rust 语言的 GPU 驱动原型。该驱动在 Linux Plumbers 会议上展示了流畅运行 3D 游戏的能力，并计划在 2026 年正式并入主线。这符合 Linux 内核 DRM 子系统未来强制要求使用 Rust 编写新驱动的发展趋势。
原文：[The future for Tyr](https://lwn.net/Articles/1055590/)

**各大发行版厂商密集发布安全更新**
包括 Red Hat、Oracle、SUSE 和 Ubuntu 在内的业界大厂近期密集发布了针对内核、glibc 及各类系统组件的安全补丁。这些更新涵盖了从底层驱动到上游应用（如 Python、OpenSSL）的多个漏洞修复。这体现了企业级 Linux 供应商在维护开源生态安全方面的协同努力。
原文：[Security updates for Friday](https://lwn.net/Articles/1057506/)
原文：[Security updates for Thursday](https://lwn.net/Articles/1057381/)

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
