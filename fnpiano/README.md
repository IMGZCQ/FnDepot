# 🎹 对牛弹琴 · WebPiano

> 跑在浏览器里的虚拟钢琴，5 组八度 36 个白键 + 25 个黑键，从 C2 到 C7 完整覆盖。
> 鼠标、键盘两路触发，原生 Web Audio API 实时解码音色，零依赖、无构建步骤。

***

<img width="1280" height="720" alt="1280" src="https://github.com/user-attachments/assets/f3c5a3c4-ccb7-415b-9564-eed2237c4829" />



## ✨ 功能特点

| 特性                | 说明                                                                |
| ----------------- | ----------------------------------------------------------------- |
| 🎹 5** 组八度 61 键** | 36 个白键 + 25 个黑键，从 C2 完整覆盖到 C7                                     |
| 🖱️ **双输入方式**     | 鼠标点击琴键，或直接用电脑键盘按键演奏                                               |
| ⌨️ **多重键位映射**     | C4\~B6 同时绑定主键盘 + 方向键 + 数字小键盘，每键可触发多个物理键                           |
| 🎵 **黑键 hold 模式** | 按住 \` （反引号）或 `Backspace` 再按白键即可触发升半音黑键，避开 Shift/Ctrl/Alt 与系统快捷键冲突 |
| 🗺️ **键位示意图**     | 琴体下方有完整的键盘布局图，点击图上的键也能发声，触发时对应按钮实时高亮                              |
| 💡 **可视化反馈**      | 键位提示 + 音名显示可独立开关                                                  |
| 🔊 **分级缓存**       | 音色 1 天缓存，HTML/CSS/JS 不缓存，调试修改刷新即生效                                |
| 🐳 **多架构镜像**      | Docker 镜像同时支持 linux/amd64、linux/arm64、linux/arm/v7                |
| 🪟 **全平台二进制**     | 5 平台编译：Linux / Windows / macOS（amd64 + arm64）                     |
| 🛰️ **飞牛网关支持**    | 内置 Unix Socket 监听，可对接 fnOS 统一网关免端口访问                              |

***

## 🎼 键位一览

### 白键（C2 \~ C7，共 36 个）

| 八度       | 物理键位                                            |
| -------- | ----------------------------------------------- |
| C2 \~ E3 | 数字键 `1 2 3 4 5 6 7 8 9 0`                       |
| F3 \~ B3 | `Q W E R T Y U`                                 |
| C4 \~ B4 | `T Y U I O P A` + `← ↑ ↓ →` + 数字小键盘 `0 . Enter` |
| C5 \~ B5 | `S D F G H J K` + 数字小键盘 `1 2 3 4 5 6 7`         |
| C6 \~ B6 | `L Z X C V B N` + 数字小键盘 `8 9 + Num / * -`       |
| C7       | `M`                                             |

### 黑键（升半音）

每个白键对应的升半音黑键，按住   ` \` `（反引号）` 或 `Backspace` 的同时按下该白键的主键位即可触发。

> 键位图上 \` 和 `Bksp` 键被染成淡紫色，键帽下有"黑键"小字标识。

***

## 🖱️ 操作说明

### 演奏控制

| 操作方式           | 说明                               |
| :------------- | :------------------------------- |
| 🖱️ **鼠标点击琴键** | 直接点击琴体上的白键 / 黑键发声                |
| ⌨️ **键盘按键**    | 按下对应绑定的物理键发声，松开立即停止              |
| 🔤 **键位图点击**   | 琴体下方的键位示意图也可点击发声                 |
| 🟣 **黑键修饰**    | 按住 \` 或 `Backspace` + 白键主键，触发升半音 |

### 顶栏开关

| 控件          | 功能                      |
| :---------- | :---------------------- |
| ☑️ **键位提示** | 显示每个琴键上印的字母 / 符号        |
| ☑️ **音名**   | 显示 C2 / D#4 之类          |
| 🔊 **音量**   | 0\~100 直接控制 master gain |

***

## 🖼️ 界面布局

```
┌──────────────────────────────────────────────┐
│  🟪 对牛弹琴    ☑ 键位提示 ☑ 音名 🔊 80%    │  ← 顶栏
├──────────────────────────────────────────────┤
│        对牛弹琴 · PIANO       使用提示       │  ← 琴体品牌条
│   ┃█┃█┃█┃█┃█┃█┃█┃█┃█┃ ...                │  ← 琴键
│   C2 D2 E2 ... C7                            │
├──────────────────────────────────────────────┤
│  ` 1 2 3 4 5 6 7 8 9 0 - = Bksp ...         │  ← 键位图
│  Tab Q W E R T Y U I O P ...                 │
│  ...                                         │
└──────────────────────────────────────────────┘
```

***

## 📝 更新日志

| 版本         | 更新内容                                                                        |
| :--------- | :-------------------------------------------------------------------------- |
| **v0.1.6** | C4\~B6 接入多重键位（方向键 / 数字小键盘）；黑键改用 \` / `Backspace` 修饰键避免系统快捷键冲突；琴体下方增加完整键位示意图 |
| **v0.1.3** | 引入飞牛 fnOS Unix Socket 网关支持，可免端口接入统一网关；日志统一输出到 stdout，结构化访问日志                |
| **v0.1.0** | 5 组八度 61 键基础播放；Web Audio API 预解码音色；分级缓存策略；多架构 Docker 镜像                     |
| **更早之前**   | 初版 8080 端口单平台运行                                                             |

***

## 🚀 快速开始

### 方式一：Docker Compose 部署（推荐）

#### 创建 `docker-compose.yml`

```yaml
services:
  webpiano:
    container_name: webpiano             # 容器名称
    image: imgzcq/webpiano:latest        # Docker 镜像名称
    ports: [9177:9177]                   # 访问端口:内部端口
    restart: always                      # 开机自启
```

#### 启动

```bash
docker compose up -d
```

镜像默认监听 `9177` 端口，浏览器打开 `http://localhost:9177` 即可开弹。

#### 更新镜像三步曲

1. Compose > 清理项目
2. 本地镜像 > 删除原来的镜像
3. 返回 Compose > 构建

***

### 方式二：本地直接跑

需要本地已安装 Go 1.21+。

```bash
cd go-piano
go run .
```

默认监听 `:9177`，浏览器打开 `http://localhost:9177` 即可。

可指定参数：

```bash
go run . -addr=":9000" -root=./static
```

支持的命令行参数：

| 参数        | 默认值                    | 说明                       |
| --------- | ---------------------- | ------------------------ |
| `-addr`   | `:9177`                | HTTP 监听地址                |
| `-root`   | `static`               | 静态文件根目录                  |
| `-sock`   | `/target/fnpiano.sock` | Unix Socket 监听路径（空字符串禁用） |
| `-prefix` | `/app/fnpiano`         | 网关路径前缀（空字符串禁用前缀重写）       |

***

### 方式三：下载预编译二进制

前往 [Releases](https://github.com/imgzcq/webpiano/releases) 下载对应平台的可执行文件：

| 平台            | 文件                           |
| ------------- | ---------------------------- |
| Linux amd64   | `webpiano-linux-amd64`       |
| Linux arm64   | `webpiano-linux-arm64`       |
| Windows amd64 | `webpiano-windows-amd64.exe` |
| macOS amd64   | `webpiano-darwin-amd64`      |
| macOS arm64   | `webpiano-darwin-arm64`      |

每个二进制都附带同名 `.sha256` 校验文件：

```bash
sha256sum -c webpiano-linux-amd64.sha256
```

直接运行即可（Windows 下双击 `webpiano-windows-amd64.exe`）。

***

### 方式四：飞牛fnOS 用户 直接安装

🏪 直接在 应用中心 搜索 **"对飞牛弹琴"** 下载安装（上架中...）

📦 三方商店 Fndepot 搜索 **"对飞牛弹琴"** 下载安装

***

## 🎹 运行界面
<img width="1094" height="559" alt="PixPin_2026-06-30_02-48-13" src="https://github.com/user-attachments/assets/3d3338a5-eaf4-4b61-8114-026b8ef57f99" />


## 📁 目录结构

```
go-piano/
├── main.go                              # 入口：HTTP 服务 + Unix Socket + 优雅关闭
├── go.mod                               # 模块声明，无第三方依赖
├── Dockerfile                           # 多阶段构建，最终镜像仅含二进制
├── docker-compose.yml
├── .dockerignore
├── .github/
│   └── workflows/
│       └── publish-and-release.yml      # Tag 触发：Docker 推送 + 多平台二进制 Release
├── internal/
│   └── server/
│       └── server.go                    # 静态文件服务 + Cache-Control 策略
└── static/
    ├── index.html                       # 页面骨架
    ├── style.css                        # 钢琴与键位图样式
    ├── app.js                           # 键盘事件、音频播放、键位图渲染
    ├── assets/
    │   └── icon.png                     # 站点图标 / 品牌标识
    └── samples/
        └── piano/                       # 61 个 mp3 音色文件
            ├── a49.mp3 ~ a90.mp3        # 白键
            └── b49.mp3 ~ b90.mp3        # 黑键
```

***

## 🔧 端口说明

|  主机端口  |  容器端口  | 说明         |
| :----: | :----: | ---------- |
| `9177` | `9177` | Web 服务访问端口 |

***

## 🛠️ 缓存策略

| 资源类型                             | Cache-Control           |
| -------------------------------- | ----------------------- |
| `*.mp3 / *.ogg / *.wav / *.flac` | `public, max-age=86400` |
| `*.js / *.css / *.html`          | `no-cache`              |

实现见 [server.go](file:///f:/飞牛图标工具/piano/go-piano/internal/server/server.go)。

***

## 🔒 安全维护

| 操作           | 方法                            |
| ------------ | ----------------------------- |
| 🔄 **版本升级**  | 拉取最新 Docker 镜像后重启容器即可，音色文件无状态 |
| 🧹 **清理缓存**  | 浏览器强制刷新 `Ctrl+Shift+R` 跳过前端缓存 |
| 🛡️ **限制访问** | 在反向代理层（fnOS 网关 / Nginx）做白名单即可 |

***

## 🧰 技术栈

- **后端**：Go 标准库 `net/http`，多阶段 Docker 镜像，内置 Unix Socket 监听
- **前端**：原生 HTML / CSS / JS，无构建工具
- **音频**：Web Audio API + `AudioContext.decodeAudioData` 预解码到 `AudioBuffer`
- **键盘事件**：优先使用 `e.code` 区分顶行数字键与数字小键盘（即使 NumLock 关闭也能识别）

***

## 📦 发布版本

仓库根目录打 tag（如 `v0.3.0`）即可触发 GitHub Actions：

- 推送 Docker 镜像到 Docker Hub（多架构：amd64 / arm64 / armv7）
- 产出 5 个平台的二进制（Linux / Windows / macOS）+ sha256 校验和，自动创建 GitHub Release

**GitHub Secrets 配置**（Settings → Secrets and variables → Actions → New repository secret）：

| Secret 名             | 必填 | 说明                                                                              |
| -------------------- | -- | ------------------------------------------------------------------------------- |
| `DOCKERHUB_USERNAME` | 否  | Docker Hub 用户名。缺失时 Docker 推送步骤自动跳过，只发布二进制                                       |
| `DOCKERHUB_TOKEN`    | 否  | Docker Hub Access Token（不是密码，建议在 <https://hub.docker.com/settings/security> 生成） |
| `GITHUB_TOKEN`       | 自动 | GitHub Actions 内置，无需手动配置，用于创建 Release                                           |

手动触发时可选 `build_type`：

- `docker_and_release`（默认）：两个都做
- `docker`：只推 Docker
- `release`：只发二进制

***

## 📝 开源协议

本项目基于 MIT 协议开源，欢迎 Star ⭐ 和贡献！
