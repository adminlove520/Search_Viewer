# 🕵️ Search Viewer

> 空间测绘与信息收集工具

[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue)]()
[![Language](https://img.shields.io/badge/Language-Python%20%7C%20C%2B%2B-yellow)]()
[![License](https://img.shields.io/badge/License-GPL--3.0-green)]()

---

## 📋 简介

Search Viewer 是一款聚合多平台空间测绘 API 的图形化工具，帮助安全研究人员和渗透测试人员进行信息收集与资产发现。

## ✨ 特性

- 🔍 **多平台聚合**：支持 Fofa、Hunter、Shodan、360 Quake、Zoomeye、Censys
- 📊 **一键导出**：支持 CSV、JSON 等格式导出
- 🎨 **图形界面**：简洁易用的 GUI
- 📈 **多窗口展示**：支持多标签页同时查询
- 🔎 **历史记录**：保存查询历史

## 🖥️ 支持平台

| 平台 | 说明 | 用途 |
|------|------|------|
| **Fofa** | 网络空间搜索引擎 | 资产发现、子域名 |
| **Hunter** | 鹰图 | 企业资产查询 |
| **Shodan** | 物联网搜索引擎 | 设备发现 |
| **360 Quake** | 360空间测绘 | 资产发现 |
| **Zoomeye** | 钟馗之眼 | 网络空间探测 |
| **Censys** | 网络测绘 | SSL证书查询 |

## 🚀 快速开始

### 安装

```bash
# 克隆项目
git clone https://github.com/adminlove520/Search_Viewer.git
cd Search_Viewer

# 安装依赖 (Python版本)
pip install pyside2 requests

# 运行
python Search_Viewer.py
```

### 配置 API Key

首次使用需要在界面中配置各平台的 API Key：

| 平台 | 获取方式 |
|------|----------|
| Fofa | https://fofa.info |
| Hunter | https://hunter.qianxin.com |
| Shodan | https://www.shodan.io |
| 360 Quake | https://quake.360.cn |
| Zoomeye | https://www.zoomeye.org |

## 📖 使用示例

### Fofa 查询

```bash
# 查找 nginx 服务器
title="nginx"

# 查找特定域名资产
domain="example.com"

# 组合查询
domain="example.com" && port=443
```

### Shodan 查询

```bash
# 查找 nginx
nginx

# 查找中国区的 SSH
ssh country:CN
```

## 📂 项目结构

```
Search_Viewer/
├── Search_Viewer.py      # 主程序
├── Search_Viewer_ui.py   # UI 文件
├── resources_rc.py       # 资源文件
├── iconhash.py          # IconHash 工具
├── favicon.ico          # 图标
├── image/               # 截图
└── README.MD            # 说明文档
```

## 📄 许可证

GPL-3.0 License

## 🙏 感谢

- 感谢原项目 https://github.com/G3et/Search_Viewer

---

## 📝 更新日志

### v4.2 (2025/2/6)
- Fofa 新增 CTRL+W 关闭页面
- Fofa 新增历史查询记录
- 去除自定义域名
- 查询内容靠前

### v4.1 (2024/6/15)
- Fofa 界面搜索不再覆盖，每次查询有新窗口
- 修复查询时页码问题
- Fofa 新增排序、新增多个字段
- 新增自定义域名

### v4.0 (2024/3/6)
- 去除 Censys
- 使用 QT C++ 重构
- 新增回车查询、右键打开浏览器
- 导出可自选路径
- 支持缩放、支持全选
- 修复查询过大闪退问题

### v3.0 (2023/7/15)
- 新增 Censys
- quake 和 zoomeye 代码优化
- 界面改动，新增语法参考
- 修复已知 BUG

### v2.0 (2023/02/17)
- 修复导出时间戳
- 修复 Hunter 恢复页码
- 新增 360 Quake
- 新增 Zoomeye

### v1.0 (2022/11/12)
- 初始版本
- 支持多线程
- 支持 Fofa iconhash
- 支持一键导出
