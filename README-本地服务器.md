# 本地服务器使用说明

由于浏览器的安全限制，直接双击打开 HTML 文件（file:// 协议）无法使用 Canvas API 分析图片颜色。

## 解决方案：使用本地服务器

### 方法1：使用 Python（推荐）

1. 打开终端（Terminal）
2. 进入项目目录：
   ```bash
   cd "/Users/smzdm/Desktop/星火硬件"
   ```

3. 启动服务器：
   ```bash
   # Python 3
   python3 -m http.server 8000
   
   # 或者 Python 2
   python -m SimpleHTTPServer 8000
   ```

4. 在浏览器中访问：
   ```
   http://localhost:8000/homepage.html
   ```

### 方法2：使用 VS Code Live Server

1. 在 VS Code 中安装 "Live Server" 扩展
2. 右键点击 `homepage.html`
3. 选择 "Open with Live Server"

### 方法3：使用 Node.js http-server

1. 安装 http-server：
   ```bash
   npm install -g http-server
   ```

2. 进入项目目录并启动：
   ```bash
   cd "/Users/smzdm/Desktop/星火硬件"
   http-server -p 8000
   ```

3. 在浏览器中访问：
   ```
   http://localhost:8000/homepage.html
   ```

## 为什么需要本地服务器？

- 浏览器的安全策略不允许 `file://` 协议下的页面读取图片像素数据
- 使用 `http://localhost` 可以避免跨域问题
- 这是开发 Web 应用的标准做法
