# 音乐术语词典

这是一个交互式的音乐术语查询工具，支持中文、拼音和英文搜索，并提供术语收藏、导出等功能。

## 功能特点

- 支持多种搜索方式（中文、拼音、英文）
- 模糊匹配和智能提示
- 收藏夹功能
- 搜索历史记录
- 多种格式导出（TXT、Word、Excel、HTML）
- 自动数据备份
- 统计信息显示

## Python 安装教程

### Windows 用户
1. 访问 Python 官网：https://www.python.org/downloads/
2. 点击"Download Python x.x.x"下载最新版本
3. 运行安装程序
   - ✅ 勾选"Add Python to PATH"
   - 点击"Install Now"开始安装
4. 验证安装：
   - 打开命令提示符（按 Win+R，输入 cmd）
   - 输入：`python --version`
   - 如果显示版本号，说明安装成功

### Mac 用户
1. 使用 Homebrew 安装（推荐）：
   ```bash
   # 安装 Homebrew（如果没有）
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   
   # 安装 Python
   brew install python
   ```

2. 或直接下载安装：
   - 访问 https://www.python.org/downloads/
   - 下载 Mac 版本安装包
   - 双击运行安装程序

3. 验证安装：
   - 打开终端
   - 输入：`python3 --version`

### Linux 用户
大多数 Linux 发行版已预装 Python。如果没有：

1. Ubuntu/Debian：
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip
   ```

2. Fedora：
   ```bash
   sudo dnf install python3 python3-pip
   ```

3. 验证安装：
   ```bash
   python3 --version
   ```

### pip 包管理器
如果 pip 未安装：

1. Windows：
   ```bash
   python -m ensurepip --default-pip
   ```

2. Mac/Linux：
   ```bash
   python3 -m ensurepip --default-pip
   ```

升级 pip：
```bash
# Windows
python -m pip install --upgrade pip

# Mac/Linux
python3 -m pip install --upgrade pip
```

## 安装步骤

1. 确保已安装 Python 3.6 或更高版本
   ```bash
   python --version
   ```

2. 下载项目文件
   # 直接下载 music_dict on computer.py 文件

3. 安装必要的 Python 库
   ```bash
   pip install pypinyin python-docx pandas openpyxl
   ```

4. 运行程序
   ```bash
   python music_dict on computer.py
   ```

   Mac/Linux 用户也可以：
   ```bash
   chmod +x music_dict on computer.py  # 添加执行权限
   ./music_dict on computer.py  # 直接运行
   ```

## 使用说明

### 基本搜索
- 输入中文：如 "甜美"
- 输入拼音：如 "tianmei"
- 输入英文：如 "dolce"
- 支持部分匹配：如 "dol"

### 常用命令
- `?` : 显示帮助信息
- `dc1` : 退出程序
- `cl1` : 清空收藏夹
- `exp` : 导出收藏夹
- `fav` : 查看收藏夹
- `his` : 查看搜索历史
- `stat` : 显示统计信息

### 收藏功能
1. 单个搜索结果时：
   - 直接选择是否收藏（y/n）

2. 多个搜索结果时：
   - 输入编号（1-N）选择要收藏的术语
   - 输入 0 取消收藏

### 导出功能
1. 输入 `exp` 进入导出模式
2. 选择导出格式：
   - 1: 文本文件 (.txt)
   - 2: Word文档 (.docx)
   - 3: Excel表格 (.xlsx)
   - 4: HTML网页 (.html)
3. 选择导出位置：
   - 1: 桌面
   - 2: 下载
   - 3: 文档
   - 4: 当前目录

### 数据备份
- 程序会自动备份用户数据和程序文件
- 备份文件存储在 `.music_dict_data/backups` 目录下
- 如果程序文件丢失，可以通过以下步骤恢复：
  1. 在程序原本位置按 Command + Shift + . 显示隐藏目录
  2. 进入 .music_dict_data/backups 目录
  3. 找到最新的 program_backup_*.zip 文件
  4. 解压获取程序备份

## 搜索技巧

1. 可以使用拼音首字母：
   - 如 "tm" 代替 "tianmei"

2. 优先使用完整关键词：
   - 完整词汇会得到更精确的结果

3. 结果太多时：
   - 尝试使用更长的关键词
   - 可以组合中文和拼音搜索

4. 找不到结果时：
   - 尝试使用同义词
   - 检查拼写是否正确
   - 尝试不同的搜索方式

## 注意事项

1. 首次运行时会在程序所在目录创建 `.music_dict_data` 文件夹，用于存储用户数据
2. 导出功能需要相应的 Python 库支持
3. 建议定期导出收藏夹，以备份重要数据

## 常见问题

Q: 程序无法启动？
A: 检查 Python 版本和必要库是否正确安装

Q: 找不到导出的文件？
A: 检查选择的导出位置，默认会提示导出路径

Q: 收藏的术语丢失？
A: 检查 `.music_dict_data` 目录下的备份文件

## 手机用户使用说明

对于手机用户，我们提供了一个简化版本的音乐术语词典（music_dict on mobile.py），可以使用 Pythonista 等 Python IDE App 运行。

### 安装步骤（iOS - Pythonista）
1. 在 App Store 下载安装 Pythonista
2. 安装 StaSh（用于使用 pip）：
   - 创建一个新的 Python 文件（点击 + 号）
   - 复制并粘贴以下代码：
     ```python
     import requests as r; exec(r.get('https://bit.ly/get-stash').content)
     ```
   - 运行该文件
   - 等待安装完成，然后重启 Pythonista
   - 运行新生成的 `launch_stash.py` 文件进入终端
   - 在终端中使用 pip 安装所需库：
     pip install pypinyin

> 提示：如果需要查看详细的安装教程，可以观看[视频教程](https://www.youtube.com/watch?v=RYS0bZ5Iivk)

3. 将 music_dict_old.py 导入 Pythonista

### 安装步骤（Android - Pydroid）
1. 在 Google Play 下载安装 Pydroid
2. 将 music_dict on mobile.py 导入 Pydroid
3. 安装必要的库：
   pip install pypinyin


### 简化版功能
- 基本的中文、拼音、英文搜索
- 近义词匹配
- 模糊匹配
- 无需联网即可使用

### 使用限制
简化版不包含以下功能：
- 收藏夹
- 导出功能
- 搜索历史
- 数据备份

### 注意事项
1. 手机版为轻量级版本，适合日常快速查询
2. 如需完整功能，建议使用电脑版
3. 部分手机 Python IDE 可能需要付费
