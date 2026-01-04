# Nexus 主题 - 版本历史

## v3.0.0 (2026-01-04)

### 🎉 重大更新

- **主题重命名**: 从 Argon 重命名为 Nexus
  - 新名称更符合路由器作为网络中心的定位
  - 完全重构的设计系统和配色方案

### 🎨 设计系统升级

#### 配色方案
- **主色调**: 从紫蓝渐变改为专业蓝色 (#3B82F6)
- **配色系统**: 采用 Tailwind Slate 色阶,更适合 dashboard
- **语义色**: 优化状态指示器颜色
  - Success: #10B981 (Emerald-500)
  - Info: #06B6D4 (Cyan-500)
  - Warning: #F59E0B (Amber-500)
  - Danger: #EF4444 (Red-500)

#### 字体系统
- **标题字体**: Poppins (几何、现代、友好)
- **正文字体**: Open Sans (人文主义、易读)
- **来源**: Google Fonts 在线加载
- **替代**: 移除本地 Google Sans 字体

#### 阴影系统
- **优化**: 降低不透明度 (0.1 → 0.08)
- **风格**: 更柔和的现代层级
- **符合**: Swiss Modernism 简洁美学

#### 动画系统
- **时长优化**: 150-300ms (原 150-350ms)
- **可访问性**: 添加 `prefers-reduced-motion` 支持
- **缓动函数**: 使用 ease-out/ease-in

#### Glassmorphism 效果
- **模糊半径**: 12px (原 16px)
- **不透明度**: 0.80 (原 0.75)
- **阴影**: 蓝色主题阴影

### ✨ 新增功能

- **可访问性支持**: 符合 WCAG AA 标准
- **Reduced Motion**: 尊重用户运动偏好设置
- **键盘导航**: 所有交互元素可通过键盘访问
- **高对比度**: 文本对比度优化

### 🔧 技术改进

- **CSS 变量**: 完整的设计令牌系统
- **模块化**: 更清晰的 LESS 文件结构
- **性能**: 优化动画和渲染性能
- **兼容性**: 保留 argon 图标字体向后兼容

### 📝 文档更新

- **README**: 完全重写,反映 Nexus 主题特性
- **安装指南**: 更新包名和命令
- **GitHub Actions**: 自动构建 Nexus 主题包

### 🗑️ 移除内容

- 移除旧的 Google Sans 本地字体
- 移除过时的配色变量
- 清理未使用的样式规则

---

## 升级指南

### 从 Argon 升级到 Nexus

如果您之前使用 Argon 主题,请按以下步骤升级:

1. **卸载旧主题**:
   ```bash
   opkg remove luci-theme-argon
   ```

2. **安装 Nexus**:
   ```bash
   opkg install luci-compat luci-lib-ipkg
   wget https://github.com/jerrykuku/luci-theme-nexus/releases/download/v3.0.0/luci-theme-nexus_3.0.0_all.ipk
   opkg install luci-theme-nexus*.ipk
   ```

3. **激活主题**:
   - 进入 **System → System → Language and Style**
   - 选择 **Nexus** 主题
   - 点击 **Save & Apply**

### 配置文件迁移

如果您使用了 `luci-app-argon-config`:

- 配置文件位置: `/etc/config/argon` → `/etc/config/nexus`
- 背景文件位置: `/www/luci-static/argon/background` → `/www/luci-static/nexus/background`
- 建议使用新的 `luci-app-nexus-config` (即将发布)

---

## 设计理念

Nexus 主题的设计遵循以下原则:

1. **专业性**: 企业级 dashboard 风格,适合专业用户
2. **现代性**: 使用最新的设计趋势和 CSS3 特性
3. **易用性**: 清晰的视觉层级,流畅的交互体验
4. **可访问性**: 符合 WCAG 标准,支持辅助技术
5. **性能**: 优化动画和渲染,确保流畅体验

---

## 致谢

感谢所有为 Argon 主题做出贡献的开发者和用户。Nexus 主题在 Argon 的基础上进行了全面升级,继承了其优秀的设计理念,并引入了更现代的设计系统。

特别感谢:
- [luci-theme-material](https://github.com/LuttyYang/luci-theme-material/) - 原始设计灵感
- [Argon Dashboard](https://demos.creative-tim.com/argon-dashboard/) - UI 设计参考
- OpenWrt 社区的所有贡献者
