# SSP Tooling

SSP (Sakura Script Player) 汉化工具包 / Sinicization Toolkit

基于 [ukatech/ssp-sinicization](https://github.com/ukatech/ssp-sinicization) 的汉化资源，集成 SSP 本体的一键安装程序。

## 下载 / Download

请前往 [Releases](https://github.com/RealCrystalNight/ssp-tooling/releases) 页面下载最新版本的 `ssp_2_8_31f.exe`。

## 功能 / Features

- SSP 2.8.31 一键安装（自动下载 Java 17 运行环境）
- 简体中文语言包集成
- 繁体中文语言包集成
- 基于 ssp-sinicization 的最新汉化资源

## 使用 / Usage

1. 下载 `ssp_2_8_31f.exe`
2. 双击运行
3. 首次运行会自动下载 Java 17（约 175MB），请保持网络畅通
4. 安装程序会自动部署 SSP 和语言包

## 构建 / Build

```bash
# 克隆本仓库
git clone https://github.com/RealCrystalNight/ssp-tooling.git
cd ssp-tooling

# 网站文件在 docs/ 目录
# GitHub Pages 已配置为从 docs/ 构建
```

## 鸣谢 / Credits

- [SSP BUGTRAQ](https://ssp.shillest.net/) — SSP 官方网站 / Official SSP website
- [ukatech/ssp-sinicization](https://github.com/ukatech/ssp-sinicization) — 中文语言包 / Chinese Language Packs
- [ponapalt/ssp](https://github.com/ponapalt/ssp) — SSP 源代码 / SSP Source Code
- [nikolat/sosiremi](https://github.com/nikolat/sosiremi) — GitHub NAR 文件列表 / GitHub NAR Listing

## 许可 / License

本项目采用与 ssp-sinicization 相同的许可协议。
This project is licensed under the same license as ssp-sinicization.

---

SSP Tooling — 伺か简体中文化项目

本页面是基于 SSP 官方站点的非官方镜像，提供汉化工具包的下载与说明。
This is an unofficial mirror of the SSP website providing sinicized toolkits.

---

### 关于伺か (Ukagaka) / 关于 SSP

伺か（うかがか）は、デスクトップ上でキャラクターを表示・操作するためのフリーウェアです。SSP（Sakura Script Player）は、伺か互換のベースウェア（実行環境）の一つで、最も広く使われています。

SSP を使うと、デスクトップに「ゴースト」と呼ばれるキャラクターが住み着き、話しかけたり、時計を表示したり、様々な機能を提供してくれます。ゴーストは NAR 形式で配布されており、ユーザーが自由に追加・切り替えができます。

### 伺か（Ukagaka）とは？

伺かは、2000 年代初頭から続くデスクトップマスコットエンジンの先駆けです。元々は「春望」という名前でスタートし、現在では多くの派生エンジンやツールが存在します。

- **SSP (Sakura Script Player)**: 現在最も広く使われているベースウェア
- **CROW**: 軽量ベースウェア
- **Ninix**: Linux 向けベースウェア
- **里々 (SatoSato)**: ゴースト開発用スクリプト言語（SHIORI）
- **YAYA**: 里々互換の別実装

SSP Tooling は、SSP を中国語環境で使いやすくするためのツールキットです。日本語や英語のオリジナル SSP に、中国語リソースを追加し、さらに自動インストーラを同梱しています。

### SSP の主な機能

- デスクトップキャラクターの表示と操作
- ゴースト（キャラクター）の追加・切り替え
- プラグインによる機能拡張
- カレンダー、時計、天気予報などのツール
- インターネットを介したゴースト同士の通信
- 音声合成エンジンとの連携
- SAORI（外部機能拡張）に対応

### ゴーストの探し方

ゴーストは以下のサイトで見つけることができます：

- [偽SoSiReMi](https://nikolat.github.io/sosiremi/) — GitHub で公開されている NAR ファイル一覧
- [SSP BUGTRAQ ゴースト配布](https://ssp.shillest.net/) — 公式サイトのゴーストリスト
- [うかぼーど](https://ukaboard.skr.jp/) — 伺かリンク集
- [Ghost Log](https://ghost-log.skr.jp/) — ゴースト更新情報

---

### 常见问题 (FAQ)

**Q: 为什么需要下载 Java？**
A: SSP 本身不需要 Java，但本安装程序使用 Java 来自动完成 SSP 的部署和配置。安装完成后，SSP 的运行不依赖 Java。

**Q: 这个汉化版和官方版有什么区别？**
A: 核心 SSP 引擎与官方版完全相同。我们只是添加了中文语言包和一键安装功能。所有功能与原版一致。

**Q: 如何卸载？**
A: 删除 `%APPDATA%\Microsoft\Speech\Oracle` 目录（Java 运行环境）和 SSP 的安装目录即可。

**Q: 为什么杀毒软件报毒？**
A: 这是误报（false positive）。SSP 是开源软件，本安装程序也是开源的。请将 `ssp.exe` 加入杀毒软件排除列表。

**Q: 支持 Windows 以外的系统吗？**
A: 本安装程序仅支持 Windows。Linux/macOS 用户可以使用 Wine 运行 SSP，或直接使用 [ninix-kagari](https://github.com/ninix/kagari)。

---

### 技術情報 (Technical Information)

本安装程序（ssp_2_8_31f.exe）是一个 Rust 编写的自解压安装器，功能包括：

1. 检测并安装 Java 17 运行环境（若缺失）
2. 解压 SSP 本体
3. 应用中文语言包
4. 配置 SSP 首次运行设置

安装程序使用以下技术栈：
- **Rust** — 核心安装逻辑（reqwest + zip 库）
- **Java 17 (Zulu JDK)** — SSP 部署工具
- **SSP 2.8.31** — 本体
- **ssp-sinicization** — 中文语言资源

---

### 開発者向け情報 (Developer Info)

本リポジトリは以下の構成になっています：

```
ssp-tooling/
├── docs/
│   ├── index.html    # GitHub Pages 网站主页面
│   └── style.css     # 网站样式
├── README.md         # 本文件
└── .github/          # GitHub 配置
    └── workflows/    # CI/CD (如有)
```

GitHub Pages 已配置为从 `docs/` 目录构建。修改 `docs/` 中的文件后，推送到 `main` 分支即可自动更新网站。

---

*SSP Tooling — 让伺か更贴近中文用户*
*SSP Tooling — Making Ukagaka Accessible to Chinese Users*
*SSP Tooling — 伺かを中国語ユーザーにより身近に*

最后更新 / Last Updated: 2026-06-16
