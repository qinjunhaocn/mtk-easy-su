# Mtk Easy Su

[![](https://img.shields.io/github/downloads/JunioJsv/mtk-easy-su/total.svg)](https://github.com/JunioJsv/mtk-easy-su/releases/) [![](https://img.shields.io/badge/maintained-maybe-yellow.svg)](https://github.com/JunioJsv/mtk-easy-su)

欢迎使用 Mtk Easy Su，这是一款专为联发科（MediaTek）Android 设备设计的应用程序，用于通过 [Magisk](https://github.com/topjohnwu/Magisk) 和 Mtk-su 实现免刷机超级用户访问。此工具特别适合那些希望利用 [Diplomatic](https://forum.xda-developers.com/member.php?u=8132642) 发现的联发科安全漏洞的用户。

## 主要功能

- 轻松在您的联发科 Android 设备上建立免刷机超级用户访问权限
- 无缝集成 Magisk 和 Mtk-su，提供更强大的功能
- 通过基于终端的 [mtk-su](https://forum.xda-developers.com/t/amazing-temp-root-for-mediatek-armv8-2020-08-24.3922213/)，为高级用户提供对刷机过程的更多控制

## 快速开始

要开始使用 Mtk Easy Su，请按照以下简单步骤操作：

1. 在[此处](https://github.com/JunioJsv/mediatek-easy-root/releases)下载最新版本，但请注意，您需要自行承担相关风险。

2. 确保您已安装 [Magisk Manager](https://github.com/topjohnwu/Magisk/releases/tag/manager-v8.0.4) 以管理各个应用的 root 权限。

3. 在安装应用前，请禁用 **Google Play 保护机制**，因为最近的更新会错误地将此应用标记为有害应用。

```sh
/data/data/juniojsv.mtk.easy.su/files
UID: 0  cap: 3fffffffff  selinux: permissive  
Load policy from: /sys/fs/selinux/policy
20.4:MAGISK (20400)
client: launching new main daemon process
Exit value 0
```

## 重要提醒

- 请关注影响数百万 Android 设备的联发科关键后门漏洞。详情请查看 XDA 文章[此处](https://www.xda-developers.com/mediatek-su-rootkit-exploit/)。

- 请注意 2020 年 3 月之后发布的固件更新，它们可能会阻止 Mtk Easy Su 或 mtk-su 使用的方法。

- 要确认是否已获得超级用户权限，请检查日志返回的退出值。值为 0 表示成功并已获得 root 权限。

## 已测试设备

| 设备                 | 型号             | 芯片组             | 结果  |
| ------------------ | -------------- | --------------- | --- |
| LG X Power2        | M320N          | 联发科 MT6750      | 成功  |
| LG K10             | M250DS         | 联发科 MT6750      | 成功  |
| LG K10 Power       | M320TV         | 联发科 MT6750      | 成功  |
| LG K10 TV          | K430DSF        | 联发科 MT6753      | 成功  |
| LG K8              | K350           | 联发科 MT6735      | 失败  |
| LG K4              | X230DS         | 联发科 MT6737M     | 成功  |
| 摩托罗拉 Moto C        | XT1756         | 联发科 MT6737M     | 成功  |
| 摩托罗拉 Moto E4       | XT1773         | 联发科 MT6737      | 成功  |
| 阿尔卡特 A3 LX         | 9008X          | 联发科 MT8735B     | 成功  |
| 阿尔卡特 1             | 5033T          | 联发科 MT6739      | 成功  |
| 阿尔卡特 U5 3G         | 4047A          | 联发科 MT6580M     | 失败  |
| Blu Studio X8 HD   | S532           | 联发科 MT6580      | 失败  |
| Nook 平板 10.1       | BNTV650        | 联发科 A35-MT8167A | 成功  |
| 中兴 Blade A7 Prime  | OEM            | 联发科 A22-MT6761  | 成功  |
| OPPO F7            | CPH1821        | 联发科 MT6771      | 失败  |
| OPPO F3            | CPH1609        | 联发科 MT6750T     | 失败  |
| 联想 Vibe K5 Note    | A7020a48       | 联发科 MT6755      | 失败  |
| 联想 Tab E8          | TB-8304F1      | 联发科 MT8163      | 成功  |
| Vernee Mix 2       | Mix 2          | 联发科 MT6757CD    | 成功  |
| 诺基亚 1              | TA-1130        | 联发科 MT6739WW    | 失败  |
| 索尼 Xperia C5 Ultra | E5553          | 联发科 MT6752      | 成功  |
| 红米 6               | Cerus          | 联发科 MT6762      | 成功  |
| Ark Elf S8         | Elf S8         | 联发科 MT6580      | 成功  |
| 索尼 Xperia L3       | I4312          | 联发科 MT6762      | 成功  |
| 金立 S10             | GIONEE_SW17G04 | 联发科 MT6767      | 成功  |
| 金立 M7              | GIONEE_SW17G07 | 联发科 MT6758      | 成功  |
| 南方电信 PB1009        | PB1009         | 联发科 MT8167B     | 成功  |
| 魅族 MX6             | MX6            | 联发科 MT6797      | 成功  |

## 致谢

- 特别感谢 [Diplomatic](https://forum.xda-developers.com/member.php?u=8132642) 开发了驱动此应用的 mtk-su 工具。

- 感谢 LG K10 XDA 论坛的所有贡献者提供的宝贵见解和支持。

- 向 John Wu 致敬，感谢他通过 Magisk 为刷机社区做出的宝贵贡献。[@topjohnwu](https://twitter.com/topjohnwu)

## 警告

在锁定引导加载程序的情况下，切勿通过 Magisk Manager 更新 Magisk，否则您的设备将变砖！
请记住，虽然此工具旨在简化刷机过程，但我对使用过程中或使用后可能发生的任何意外概不负责。请谨慎操作！😊
