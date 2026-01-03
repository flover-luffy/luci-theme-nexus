# LESS 编译指南

## 方法一：使用 WSL Ubuntu 25.10

### 1. 安装 Node.js 和 npm（如果尚未安装）

```bash
# 在 WSL 中执行
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
```

### 2. 安装 LESS 编译器

```bash
sudo npm install -g less
```

### 3. 编译 LESS 文件

```bash
# 切换到项目目录（使用 WSL 路径）
cd /mnt/e/code/luci-theme-argon/less

# 编译 cascade.less
lessc cascade.less ../htdocs/luci-static/argon/css/cascade.css

# 编译 dark.less
lessc dark.less ../htdocs/luci-static/argon/css/dark.css

# 验证编译结果
ls -lh ../htdocs/luci-static/argon/css/
```

---

## 方法二：使用在线 LESS 编译器（快速测试）

如果只是想快速查看效果，可以使用在线工具：

1. 访问 https://lesscss.org/less-preview/
2. 复制 `less/cascade.less` 的内容
3. 点击编译查看生成的 CSS
4. 保存到 `htdocs/luci-static/argon/css/cascade.css`

对 `dark.less` 重复相同步骤。

---

## 方法三：使用 Windows 本地 Node.js

### 1. 安装 Node.js for Windows

从 https://nodejs.org/ 下载并安装 LTS 版本

### 2. 安装 LESS

```powershell
npm install -g less
```

### 3. 编译文件

```powershell
cd e:\code\luci-theme-argon\less
lessc cascade.less ..\htdocs\luci-static\argon\css\cascade.css
lessc dark.less ..\htdocs\luci-static\argon\css\dark.css
```

---

## 验证编译结果

编译成功后，检查生成的 CSS 文件：

```bash
# 检查文件大小（应该比原来大）
ls -lh htdocs/luci-static/argon/css/

# 查看文件开头（应该包含编译后的 CSS）
head -n 20 htdocs/luci-static/argon/css/cascade.css
```

---

## 常见问题

### Q: 编译时出现 "variable is undefined" 错误
A: 这通常是因为 LESS 变量引用问题。检查 `cascade.less` 中的变量定义顺序。

### Q: 编译后的 CSS 文件很小
A: 可能是编译失败。检查终端输出的错误信息。

### Q: 如何压缩 CSS？
A: 使用 `--clean-css` 选项：
```bash
lessc --clean-css cascade.less cascade.css
```

---

## 推荐方法

**推荐使用方法一（WSL）**，因为：
- 与 OpenWrt 开发环境一致
- 更好的命令行工具支持
- 便于集成到构建流程

只需要一次性安装 Node.js 和 LESS，之后每次修改主题只需运行编译命令即可。
