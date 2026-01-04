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

# Nexus - OpenWrt LuCI Theme

Nexus is a **modern, professional OpenWrt LuCI theme**,  
featuring a professional blue color scheme, automatic dark/light mode switching,  
elegant Glassmorphism effects, and smooth user experience.

[![license][license-badge]][license]
[![prs][prs-badge]][prs]
[![issues][issues-badge]][issues]
[![release][release-badge]][release]
[![download][download-badge]][download]
[![contact][contact-badge]][contact]

**English** |
[简体中文][zh-cn-link]

[Features](#features) •
[Version History](#version-history) •
[Quick Start](#quick-start) •
[Notes](#notes) •
[Contributors](#contributors)

</div>

## Features

- 🎨 **Modern Design System** - Professional blue color scheme (#3B82F6), enterprise-grade dashboard style
- ✍️ **Elegant Typography** - Poppins + Open Sans font combination, modern and professional
- 🌓 **Dark/Light Mode** - Automatic or manual switching, respects system preferences
- 💎 **Glassmorphism Effects** - Optimized frosted glass effects with clear visual hierarchy
- ⚡ **Smooth Animations** - 150-300ms response time, supports prefers-reduced-motion
- 📱 **Responsive Design** - Perfect adaptation for desktop, tablet, and mobile
- ♿ **Accessibility** - WCAG AA compliant, high contrast text
- 🎭 **Custom Backgrounds** - Support for images or videos as login backgrounds

## Version History

Current latest version is v3.0.0 - [Click here][en-us-release-log] to view the complete version history.

### v3.0.0 (2026-01-04)

- 🎉 **Major Update**: Theme rebranded to Nexus
- 🎨 Color Upgrade: Professional blue palette (#3B82F6)
- ✍️ Font Upgrade: Poppins + Open Sans
- ⚡ Animation Optimization: 150-300ms + prefers-reduced-motion support
- 🎯 Shadow Optimization: Softer modern elevation
- ♿ Accessibility: WCAG compliance

## Quick Start

### Build with Official OpenWrt SnapShots and ImmortalWrt

```bash
cd openwrt/package
git clone https://github.com/jerrykuku/luci-theme-nexus.git
make menuconfig #choose LUCI->Theme->Luci-theme-nexus
make -j1 V=s
```

### Install on Official OpenWrt and ImmortalWrt

```bash
opkg install luci-compat
opkg install luci-lib-ipkg
wget --no-check-certificate https://github.com/jerrykuku/luci-theme-nexus/releases/download/v3.0.0/luci-theme-nexus_3.0.0_all.ipk
opkg install luci-theme-nexus*.ipk
```

### Activate Theme

1. Login to LuCI interface
2. Navigate to **System → System → Language and Style**
3. Select **Nexus** from the **Design** dropdown
4. Click **Save & Apply**

## Notes

- 💡 **Recommended Browsers**: Chrome/Edge/Firefox - Theme uses modern CSS3 features
- 🎨 **Glassmorphism**: Firefox requires manual enabling of `backdrop-filter` ([see how](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter))
- 📱 **Mobile**: Full support for touch operations and responsive layout
- ♿ **Accessibility**: Supports keyboard navigation and screen readers

## Technical Features

### Design System

- **Color Scheme**: Professional blue palette based on Tailwind Slate scale
- **Typography**: Poppins (headings) + Open Sans (body)
- **Shadow System**: 6-level soft shadows, Material Design compliant
- **Spacing System**: Mathematical spacing (0.25rem increments)
- **Border Radius**: Consistent rounded corners (6px-24px)

### Performance Optimization

- **Google Fonts**: Online loading, reduces package size
- **CSS Variables**: Easy customization and theme switching
- **Optimized Animations**: Reduced rendering overhead
- **Responsive Images**: Auto-adapt to device resolution

### Accessibility

- **WCAG AA**: Text contrast meets standards
- **Keyboard Navigation**: All interactive elements accessible via keyboard
- **Reduced Motion**: Respects user motion preference settings
- **Semantic HTML**: Screen reader friendly

## Contributors

<a href="https://github.com/jerrykuku/luci-theme-nexus/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=jerrykuku/luci-theme-nexus" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

## Related Projects

- [luci-app-nexus-config](https://github.com/jerrykuku/luci-app-nexus-config): Configuration plugin for Nexus theme
- [openwrt-package](https://github.com/jerrykuku/openwrt-package): My OpenWrt packages
- [CasaOS](https://github.com/IceWhaleTech/CasaOS): A simple, easy-to-use, elegant open-source personal cloud system

## Acknowledgments

This theme is based on the following excellent projects:

- [luci-theme-material](https://github.com/LuttyYang/luci-theme-material/) - Material Design theme
- [Argon Dashboard](https://demos.creative-tim.com/argon-dashboard/) - Design inspiration
- [Unsplash](https://unsplash.com/) - Login background images

## License

Licensed under the [Apache License 2.0](LICENSE)
