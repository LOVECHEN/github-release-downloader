# Github Release Downloader

一个用于下载 GitHub Release 文件的命令行工具。

## 安装

### 通过 Homebrew 安装（仅支持 macOS）

```bash
# 添加 tap
brew tap lovechen/tap

# 安装
brew install grd

# 解决SHA256校验失败问题
brew update
brew reinstall grd

```

### 直接下载

从 [GitHub Releases](https://github.com/lovechen/github-release-downloader/releases) 页面下载对应系统的压缩包：

- Windows: `grd_Windows_x86_64.zip`
- macOS: 
  - Intel芯片: `grd_Darwin_x86_64.tar.gz`
  - M1/M2芯片: `grd_Darwin_arm64.tar.gz`
- Linux:
  - x86_64: `grd_Linux_x86_64.tar.gz`
  - ARM64: `grd_Linux_arm64.tar.gz`

## 使用方法

1. 交互模式:
   ```bash
   ./grd username/repo
   # 例如: ./grd LOVECHEN/v2rayN-mod
   ```

2. 指定下载序号:
   ```bash
   ./grd username/repo 1 2 3
   # 例如: ./grd LOVECHEN/v2rayN-mod 1 2
   ```

3. 下载全部:
   ```bash
   ./grd username/repo a
   # 例如: ./grd LOVECHEN/v2rayN-mod a
   ```

4. 环境变量方式:
   ```bash
   export GITHUB_URL="username/repo"
   ./grd
   ```
   
5. 代理设置:

MacOS/Linux:
```bash
export all_proxy="http://127.0.0.1:7890"
# 或
export all_proxy="socks5://127.0.0.1:7890"
```

Windows CMD:
```cmd
set all_proxy=http://127.0.0.1:7890
```

Windows PowerShell:
```powershell
$env:all_proxy="http://127.0.0.1:7890"
```

## 功能特点

- 支持交互式选择下载
- 支持批量下载指定版本
- 支持下载所有版本
- 自动创建版本目录
- 支持 HTTP/SOCKS5 代理
- 支持源码下载
- 跨平台支持 (Windows/macOS/Linux)

