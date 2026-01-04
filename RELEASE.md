# Nexus Theme - Version History

## v3.0.0 (2026-01-04)

### 🎉 Major Update

- **Theme Rebranding**: Renamed from Argon to Nexus
  - New name better reflects the router's role as a network nexus
  - Completely refactored design system and color scheme

### 🎨 Design System Upgrade

#### Color Scheme
- **Primary Color**: Changed from purple-blue gradient to professional blue (#3B82F6)
- **Color System**: Adopted Tailwind Slate scale, better suited for dashboards
- **Semantic Colors**: Optimized status indicator colors
  - Success: #10B981 (Emerald-500)
  - Info: #06B6D4 (Cyan-500)
  - Warning: #F59E0B (Amber-500)
  - Danger: #EF4444 (Red-500)

#### Typography System
- **Heading Font**: Poppins (geometric, modern, friendly)
- **Body Font**: Open Sans (humanist, readable)
- **Source**: Google Fonts online loading
- **Replacement**: Removed local Google Sans font

#### Shadow System
- **Optimization**: Reduced opacity (0.1 → 0.08)
- **Style**: Softer modern elevation
- **Compliance**: Swiss Modernism minimalist aesthetics

#### Animation System
- **Duration Optimization**: 150-300ms (from 150-350ms)
- **Accessibility**: Added `prefers-reduced-motion` support
- **Easing Functions**: Using ease-out/ease-in

#### Glassmorphism Effects
- **Blur Radius**: 12px (from 16px)
- **Opacity**: 0.80 (from 0.75)
- **Shadow**: Blue-themed shadow

### ✨ New Features

- **Accessibility Support**: WCAG AA compliant
- **Reduced Motion**: Respects user motion preferences
- **Keyboard Navigation**: All interactive elements accessible via keyboard
- **High Contrast**: Optimized text contrast

### 🔧 Technical Improvements

- **CSS Variables**: Complete design token system
- **Modular**: Clearer LESS file structure
- **Performance**: Optimized animations and rendering
- **Compatibility**: Retained argon icon font for backward compatibility

### 📝 Documentation Updates

- **README**: Completely rewritten to reflect Nexus theme features
- **Installation Guide**: Updated package names and commands
- **GitHub Actions**: Automated Nexus theme package building

### 🗑️ Removed Content

- Removed old Google Sans local font
- Removed outdated color variables
- Cleaned up unused style rules

---

## Upgrade Guide

### Upgrading from Argon to Nexus

If you previously used the Argon theme, follow these steps to upgrade:

1. **Uninstall Old Theme**:
   ```bash
   opkg remove luci-theme-argon
   ```

2. **Install Nexus**:
   ```bash
   opkg install luci-compat luci-lib-ipkg
   wget https://github.com/jerrykuku/luci-theme-nexus/releases/download/v3.0.0/luci-theme-nexus_3.0.0_all.ipk
   opkg install luci-theme-nexus*.ipk
   ```

3. **Activate Theme**:
   - Navigate to **System → System → Language and Style**
   - Select **Nexus** theme
   - Click **Save & Apply**

### Configuration File Migration

If you used `luci-app-argon-config`:

- Config file location: `/etc/config/argon` → `/etc/config/nexus`
- Background file location: `/www/luci-static/argon/background` → `/www/luci-static/nexus/background`
- Recommended to use new `luci-app-nexus-config` (coming soon)

---

## Design Philosophy

The Nexus theme design follows these principles:

1. **Professionalism**: Enterprise-grade dashboard style for professional users
2. **Modernity**: Using latest design trends and CSS3 features
3. **Usability**: Clear visual hierarchy, smooth interaction experience
4. **Accessibility**: WCAG compliant, supports assistive technologies
5. **Performance**: Optimized animations and rendering for smooth experience

---

## Acknowledgments

Thanks to all developers and users who contributed to the Argon theme. The Nexus theme is a comprehensive upgrade based on Argon, inheriting its excellent design philosophy while introducing a more modern design system.

Special thanks to:
- [luci-theme-material](https://github.com/LuttyYang/luci-theme-material/) - Original design inspiration
- [Argon Dashboard](https://demos.creative-tim.com/argon-dashboard/) - UI design reference
- All contributors in the OpenWrt community
