<!-- markdownlint-configure-file {
  "MD013": {
    "code_blocks": false,
    "tables": false,
    "line_length":200
  },
  "MD033": false,
  "MD041": false
} -->

[license]: /LICENSE
[license-badge]: https://img.shields.io/github/license/jerrykuku/luci-theme-nexus?style=flat-square&a=1
[prs]: https://github.com/jerrykuku/luci-theme-nexus/pulls
[prs-badge]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
[issues]: https://github.com/jerrykuku/luci-theme-nexus/issues/new
[issues-badge]: https://img.shields.io/badge/Issues-welcome-brightgreen.svg?style=flat-square
[release]: https://github.com/jerrykuku/luci-theme-nexus/releases
[release-badge]: https://img.shields.io/github/v/release/jerrykuku/luci-theme-nexus?style=flat-square
[download]: https://github.com/jerrykuku/luci-theme-nexus/releases
[download-badge]: https://img.shields.io/github/downloads/jerrykuku/luci-theme-nexus/total?style=flat-square
[contact]: https://t.me/jerryk6
[contact-badge]: https://img.shields.io/badge/Contact-telegram-blue?style=flat-square
[en-us-link]: /README.md
[zh-cn-link]: /README_ZH.md
[en-us-release-log]: /RELEASE.md
[zh-cn-release-log]: /RELEASE_ZH.md
[config-link]: https://github.com/jerrykuku/luci-app-nexus-config/releases
[lede]: https://github.com/coolsnowwolf/lede
[official]: https://github.com/openwrt/openwrt
[immortalwrt]: https://github.com/immortalwrt/immortalwrt

<div align="center">

# Nexus - OpenWrt LuCI 主题

Nexus 是**一款现代、专业的 OpenWrt LuCI 主题**,  
采用专业蓝色配色方案,支持深色/浅色模式自动切换,  
提供优雅的 Glassmorphism 效果和流畅的用户体验。

[![license][license-badge]][license]
[![prs][prs-badge]][prs]
[![issues][issues-badge]][issues]
[![release][release-badge]][release]
[![download][download-badge]][download]
[![contact][contact-badge]][contact]

[English][en-us-link] |
**简体中文**

[特色](#特色) •
[版本历史](#版本历史) •
[快速开始](#快速开始) •
[注意事项](#注意事项) •
[贡献者](#贡献者)

</div>

## 特色

- 🎨 **现代设计系统** - 专业蓝色配色 (#3B82F6),符合企业级 dashboard 风格
- ✍️ **优雅字体** - Poppins + Open Sans 字体组合,现代专业
- 🌓 **深色/浅色模式** - 支持自动或手动切换,符合系统偏好
- 💎 **Glassmorphism 效果** - 优化的毛玻璃效果,视觉层次分明
- ⚡ **流畅动画** - 150-300ms 响应时长,支持 prefers-reduced-motion
- 📱 **响应式设计** - 完美适配桌面、平板、手机
- ♿ **可访问性** - 符合 WCAG AA 标准,高对比度文本
- 🎭 **自定义背景** - 支持图片或视频作为登录背景

## 版本历史

当前最新版本为 v3.0.0 - [点击这里][zh-cn-release-log]查看完整的版本历史日志。

### v3.0.0 (2026-01-04)

- 🎉 **重大更新**: 主题重命名为 Nexus
- 🎨 配色升级: 专业蓝色系 (#3B82F6)
- ✍️ 字体升级: Poppins + Open Sans
- ⚡ 动画优化: 150-300ms + prefers-reduced-motion 支持
- 🎯 阴影优化: 更柔和的现代层级
- ♿ 可访问性: WCAG 标准支持

## 快速开始

### 使用官方 OpenWrt SnapShots 和 ImmortalWrt

```bash
cd openwrt/package
git clone https://github.com/jerrykuku/luci-theme-nexus.git
make menuconfig #choose LUCI->Theme->Luci-theme-nexus
make -j1 V=s
```

### 在官方和 ImmortalWrt 上安装

```bash
opkg install luci-compat
opkg install luci-lib-ipkg
wget --no-check-certificate https://github.com/jerrykuku/luci-theme-nexus/releases/download/v3.0.0/luci-theme-nexus_3.0.0_all.ipk
opkg install luci-theme-nexus*.ipk
```

### 激活主题

1. 登录 LuCI 界面
2. 进入 **System → System → Language and Style**
3. 在 **Design** 下拉菜单中选择 **Nexus**
4. 点击 **Save & Apply**

## 注意事项

- 💡 **推荐浏览器**: Chrome/Edge/Firefox - 主题使用了现代 CSS3 功能
- 🎨 **Glassmorphism**: Firefox 需要手动启用 `backdrop-filter` ([查看方法](https://developer.mozilla.org/zh-CN/docs/Web/CSS/backdrop-filter))
- 📱 **移动端**: 完美支持触摸操作和响应式布局
- ♿ **可访问性**: 支持键盘导航和屏幕阅读器

## 技术特性

### 设计系统

- **配色方案**: 专业蓝色系,基于 Tailwind Slate 色阶
- **字体系统**: Poppins (标题) + Open Sans (正文)
- **阴影系统**: 6 级柔和阴影,符合 Material Design
- **间距系统**: 数学间距 (0.25rem 增量)
- **圆角系统**: 一致的圆角设计 (6px-24px)

### 性能优化

- **Google Fonts**: 在线加载,减少包体积
- **CSS 变量**: 易于定制和主题切换
- **优化动画**: 减少渲染开销
- **响应式图片**: 自动适配设备分辨率

### 可访问性

- **WCAG AA**: 文本对比度符合标准
- **键盘导航**: 所有交互元素可通过键盘访问
- **Reduced Motion**: 支持用户运动偏好设置
- **语义化 HTML**: 屏幕阅读器友好

## 贡献者

<a href="https://github.com/jerrykuku/luci-theme-nexus/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=jerrykuku/luci-theme-nexus" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

## 相关项目

- [luci-app-nexus-config](https://github.com/jerrykuku/luci-app-nexus-config): Nexus 主题的设置插件
- [openwrt-package](https://github.com/jerrykuku/openwrt-package): 我的 OpenWrt Package
- [CasaOS](https://github.com/IceWhaleTech/CasaOS): 一个简单、易用且优雅的开源个人家庭云系统

## 致谢

本主题基于以下优秀项目:

- [luci-theme-material](https://github.com/LuttyYang/luci-theme-material/) - Material Design 主题
- [Argon Dashboard](https://demos.creative-tim.com/argon-dashboard/) - 设计灵感来源
- [Unsplash](https://unsplash.com/) - 登录背景图片

## 许可证

Licensed under the [Apache License 2.0](LICENSE)
