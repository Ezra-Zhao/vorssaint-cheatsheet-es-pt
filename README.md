# Vorssaint 速查表 | Vorssaint Cheatsheet | Guía rápida de Vorssaint

> 一页看懂 Vorssaint：一个免费开源的 macOS 菜单栏图标，装下 Mac 用户平时一个一个买的那串小工具——按应用调音量、真系统监控、更好的应用切换器与窗口吸附、Dock 预览、剪贴板历史、文本片段、截图录屏、卸载器与 Homebrew 管理，外加给刘海屏的 Dynamic Island（还能盯着 Claude、Codex、Copilot 的额度，长任务跑完提醒你）。无账号、无遥测、无订阅；只装你用的，用不上的功能不加载、不占资源、不跟你要权限。

- 上游项目：[vorssaint/vorssaint-utils](https://github.com/vorssaint/vorssaint-utils)（2026-11-02 实测 32,437 ★ / 1,566 forks，94 个 release，GPL-3.0；名称与 logo 是商标）
- 平台：仅 macOS 14 Sonoma 或更新 + Apple Silicon
- 本页结构：中文主文 → English → Español → Português

---

Apoyo y más: [GitHub Sponsors](https://github.com/sponsors/Ezra-Zhao) · [Gumroad — plantillas y cuadernos que uso](https://ezraflow28.gumroad.com) · [Ko-fi](https://ko-fi.com/ezra777zhao)

## 它是什么、不是什么

| 是 | 不是 |
|---|---|
| 一个菜单栏工具箱：九组功能按需选装，不用的功能彻底不加载、从界面消失 | 不是全家桶强塞：装法就是「只装你用的」，重装某功能会恢复它之前的设置 |
| 免费开源（GPL-3.0），本地优先：无账号、无分析、无追踪 | 不是订阅制小工具的又一份账单：没有付费墙，作者原话「免费，而且会一直免费」 |
| 权限最小化：设置时只按你勾选的功能要权限，权限页还会提醒你哪个已授权限已经没功能在用了 | 不是装上就全权在握的系统魔改工具：每个权限都有通俗说明、标明谁在用 |
| App 界面支持十三种以上语言 | 官方上手文档以英文为主；本页的西/葡语是学习译稿 |

## 安装一行版

```bash
brew install --cask vorssaint
```

或去 [Releases 页](https://github.com/vorssaint/vorssaint-utils/releases)下 `.dmg`，把 Vorssaint 拖进 Applications。官方构建用 Apple Developer ID 签名并公证，macOS 打开不拦、更新后权限不丢。

前提只有两条：**Apple Silicon + macOS 14 或更新**。Intel Mac 与更老的系统不在支持范围，别白折腾。

卸载：`brew uninstall --cask vorssaint`；想连设置与权限一起清干净，用上游仓里的 `./Tools/uninstall.sh`。

## 「只装你用的」功能选装卡

设置里逐组勾选（也可以先套一个预设再增删）。下面是九组功能各自的招牌件，勾之前先想「我每周真会用它吗」：

| 组 | 招牌功能 | 谁最需要 |
|---|---|---|
| 声音 | 按应用单独调音量（可超 100% 增益、无需音频驱动）；按应用分输出设备（音乐走音箱、通话走耳机）；麦克风工具 | 同时开会、听歌、看视频的人 |
| 系统监控 | CPU/GPU/内存/温度/电池健康的真实读数 + 历史曲线 + 耗电应用榜；风扇控制（beta，可设手动转速或温度曲线）；菜单栏读数；流量与测速；高负载/高温/内存压力/低电量告警 | 想知道 Mac 在忙什么、热什么的人 |
| 窗口与 Dock | 带实时预览的应用切换器；窗口吸附与跨屏布局；Dock 图标悬停预览窗口；绿按钮最大化不新建 Space；固定 Space 顺序；⌘Q/⌘W 防误触保护 | 多窗口多屏重度用户 |
| 键鼠 | 文本片段（短触发词展开成模板，带日期/剪贴板变量）；平滑滚动、线性滚动、关鼠标加速；三指点按变中键；Caps Lock 变 Super key；磨损按键去抖与连点过滤 | 每天打字量大、鼠标键盘都挑的人 |
| 剪贴板与文件 | 可搜索的剪贴板历史（文字/图片/文件，可置顶）；定时自动清剪贴板；纯文本粘贴；拖拽暂存 Shelf；Finder 里 ⌘X/⌘V 移动文件、F2 重命名；链接去跟踪参数 | 复制粘贴是主业的人 |
| 日常工具 | 刘海屏 Dynamic Island（音乐、日历、计时器、下载进度）；**AI 额度面板**：盯 Claude、Codex、OpenCode、GitHub Copilot 的额度/重置时间/token，长任务完成时提醒；命令栏（搜应用/文件/剪贴板/片段，还能算数换单位）；径向菜单；速记板；擦屏模式 | 已经把 AI 编程工具当生产力的 Mac 用户 |
| 捕获创作 | 截图（区域/窗口/整屏/滚动长图，带标注、打码、水印）；录屏（系统声与麦克风分轨，可导出 GIF）；离线 OCR 抠屏上文字；取色器；本地媒体工具（压视频、批量转图） | 经常做教程、提 bug、交材料的人 |
| 应用管理 | 应用更新一处查；清理缓存与残留；卸载器（删之前先列关联文件给你确认）；Homebrew 管理（搜、装、卸不用开终端）；端口占用查看 | 怕「删不干净」和终端恐惧症的人 |
| 电源与显示 | 防休眠（可定时、合盖也工作）；逐屏亮度控制（可低于显示器最低亮度）；XDR 屏额外亮度；睡眠时断蓝牙 | 合盖接屏办公、移动办公的人 |

## 它能替掉的那串付费小工具（类别对照）

| 过去单独买/订的能力 | Vorssaint 里对应 |
|---|---|
| 按应用音量混音器 | 声音组：音量混音 + 按应用输出 |
| 系统状态监控仪 | 系统监控组：真读数 + 历史曲线 + 菜单栏读数 |
| 窗口管理/吸附工具 | 窗口与 Dock 组：吸附、布局、切换器、Dock 预览 |
| 剪贴板管理器 | 剪贴板组：历史搜索 + 置顶 + 自动清理 |
| 截图录屏工具 | 捕获创作组：截图标注打码 + 分轨录屏 |
| 应用卸载器 | 应用管理组：卸载器 + 关联文件清单 |
| 防休眠小工具 | 电源组：防休眠（含合盖场景） |
| 刘海屏信息岛 | 日常工具组：Dynamic Island |

德国媒体（borncity / MakeUseOf 一类口径）算过这笔账：一串同类付费小工具合计约 $100+/年订阅——此数为媒体估算（证据 B），不是上游自报；但结论方向成立：这类钱现在可以一份都不花。

## 权限最小化提醒

- **只授你勾选功能需要的权限**：设置流程只会为你选的功能申请权限，没启用的功能不碰系统权限。
- **权限页会「反向提醒」**：每个权限都写明用途、哪些功能在用；某个已授权限如果已经没有任何功能在用，它会指出来并给你撤销的快捷入口——这是同类工具里少见的诚实设计，装完值得去那页看一眼。
- **隐私口径是原文级的**：无账号、无分析、无追踪；联网只发生在看得见的地方——检查更新、测速、Homebrew 操作、可选的在线歌词查询、你主动生成的截图/录屏临时分享链接、你明确发送的反馈。其余全在本地。

## 诚实标注区

- **平台门槛是硬的**：只支持 Apple Silicon + macOS 14+。Intel Mac 用户请直接划走，这不是「装上试试」能解决的事。
- **GPL 开源 ≠ 名字随便用**：源码是 GPL-3.0，但 Vorssaint 的名称、logo 与外观受其 TRADEMARKS 保护；fork 必须换自己的名字与形象，别拿原名发版。
- **个别功能要说清边界**（上游自己标注的）：麦克风静音不是隐私锁——Siri 和某些应用仍可能听到，指示灯只表示功能开着；风扇控制还是 beta；AI 额度面板里 Copilot 的 token 总量要等会话关闭指标到达才更新，API 价值估算用的是基础费率。引用这些功能时别说过头。
- **迭代极快**：2026-06 建仓、不到五个月 94 个 release、冲上 GitHub 趋势榜；功能名单以你装的那一版为准，本页对应 2026-11-02 的上游 README。
- **App 有西/葡语界面，上手文档是英文**：界面支持十三种以上语言，西/葡语用户装上就能用母语操作，但选装与权限这类设置说明的完整文档仍是英文——这正是本页的用处。

---

## English (summary)

Vorssaint (by vorssaint, ~32.4k stars as of 2026-11-01, GPL-3.0 for the code; the name and logo are trademarked) packs the utilities Mac users usually buy one by one into a single free menu-bar icon: a per-app volume mixer with over-100% boost, a real system monitor (CPU/GPU/temperatures/battery health, fan control in beta), a better app switcher with window snapping and Dock previews, searchable clipboard history, text snippets, a full screenshot/recording suite, an uninstaller and a Homebrew manager — plus a Dynamic Island for notched Macs that can also track Claude, Codex, OpenCode and GitHub Copilot quotas and ping you when a long task finishes.

Its defining rule is "install only what you use": features are picked individually (or from a preset), uninstalled features stop loading and disappear, and setup asks only for the permissions your chosen features need — the permissions page even flags grants that nothing uses anymore. It is local-first with no account, no analytics, no telemetry and no subscription. Install with `brew install --cask vorssaint` or the signed, notarized .dmg from Releases.

Honest notes: it requires Apple Silicon and macOS 14+, no exceptions; the app UI speaks 13+ languages while the setup docs are English-first; a few features carry upstream-stated limits (mic mute is not a privacy lock, fan control is beta); and German tech media estimate the replaced paid utilities at $100+/year in subscriptions — a media estimate, not the vendor's claim.

---

## Español (guía rápida — traducción de estudio, pendiente de revisión por un hablante nativo)

Vorssaint (de vorssaint, ~32,4 mil estrellas a noviembre de 2026, GPL-3.0 para el código; el nombre y el logo son marcas registradas) reúne en un solo icono gratuito de la barra de menús las utilidades que los usuarios de Mac suelen comprar una por una: mezclador de volumen por app (con ganancia por encima del 100 %), un monitor de sistema real (CPU/GPU/temperaturas/salud de la batería, control de ventiladores en beta), un conmutador de apps mejor con ajuste de ventanas y vistas previas del Dock, historial del portapapeles con búsqueda, fragmentos de texto, un paquete completo de captura y grabación de pantalla, un desinstalador y un gestor de Homebrew — además de una Dynamic Island para Macs con notch que también vigila las cuotas de Claude, Codex, OpenCode y GitHub Copilot y avisa cuando termina una tarea larga.

**Su regla de oro es «instala solo lo que usas»**: las funciones se eligen una a una (o desde un preset), las no instaladas dejan de cargarse y desaparecen, y la configuración solo pide los permisos que necesitan las funciones que elegiste — la página de permisos incluso señala los que ya nadie usa. Es local primero: sin cuenta, sin analíticas, sin telemetría y sin suscripción. **Instalación**: `brew install --cask vorssaint` o el .dmg firmado y notarizado desde Releases.

**Notas honestas**: exige Apple Silicon y macOS 14+, sin excepciones; la interfaz está en más de 13 idiomas, pero la documentación de configuración está en inglés; algunas funciones traen límites declarados por el propio proyecto (el silencio del micrófono no es un candado de privacidad; el control de ventiladores es beta); y medios alemanes estiman en más de 100 $/año las suscripciones de utilidades que reemplaza — una estimación de la prensa, no una afirmación del autor.

---

## Português (guia rápido — tradução de estudo, aguardando revisão de um falante nativo)

O Vorssaint (de vorssaint, ~32,4 mil estrelas em novembro de 2026, GPL-3.0 para o código; o nome e o logo são marcas registradas) reúne em um único ícone gratuito da barra de menus os utilitários que os usuários de Mac costumam comprar um por um: mixer de volume por app (com ganho acima de 100%), um monitor de sistema de verdade (CPU/GPU/temperaturas/saúde da bateria, controle de ventoinhas em beta), um alternador de apps melhor com encaixe de janelas e prévias do Dock, histórico da área de transferência com busca, snippets de texto, um pacote completo de captura e gravação de tela, um desinstalador e um gerenciador do Homebrew — além de uma Dynamic Island para Macs com notch que também acompanha as cotas de Claude, Codex, OpenCode e GitHub Copilot e avisa quando uma tarefa longa termina.

**A regra de ouro é «instale só o que você usa»**: os recursos são escolhidos um a um (ou a partir de um preset), os não instalados param de carregar e somem, e a configuração só pede as permissões de que os recursos escolhidos precisam — a página de permissões até aponta as que ninguém mais usa. É local primeiro: sem conta, sem analytics, sem telemetria e sem assinatura. **Instalação**: `brew install --cask vorssaint` ou o .dmg assinado e notarizado na página de Releases.

**Notas honestas**: exige Apple Silicon e macOS 14+, sem exceções; a interface está em mais de 13 idiomas, mas a documentação de configuração está em inglês; alguns recursos trazem limites declarados pelo próprio projeto (o mudo do microfone não é um cadeado de privacidade; o controle de ventoinhas é beta); e a imprensa alemã estima em mais de US$ 100/ano as assinaturas dos utilitários que ele substitui — uma estimativa da mídia, não uma afirmação do autor.

---

## 来源与声明

- 灵感来源 / Source / Fuente / Fonte: [vorssaint/vorssaint-utils](https://github.com/vorssaint/vorssaint-utils)（官网 vorssaint.com）
- 本仓是个人学习整理：内容用我自己的话总结自上游公开文档，不搬运原文；功能名单、安装命令与系统要求以 2026-11-02 的上游 README 为准，上游迭代很快，请以官方文档为最终依据。本仓与 Vorssaint 项目无隶属关系，不使用其名称与 logo 作为本仓标识。
- 西语、葡语部分为学习译稿，待母语校对。Las secciones en español y portugués son traducciones de estudio pendientes de revisión nativa.
- License: MIT © 2026 Guangyi Zhao
