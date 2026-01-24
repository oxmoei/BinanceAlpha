# 🤖 币安Alpha市场监控与AI智能分析系统

一个强大的加密货币监控工具，专注于币安Alpha市场分析，提供实时数据收集、上币信息跟踪、市场情绪分析和AI辅助投资建议。

## 📌 功能特点

- ✅ 实时获取并分析币安Alpha市场项目列表
- ✅ 自动检测并跟踪币安现货和创新区上新代币
- ✅ 支持多区块链平台分析（以太坊、BNB Chain、Solana等）
- ✅ 集成DeepSeek AI模型提供智能投资建议
- ✅ 按区块链平台分类整理加密货币项目数据
- ✅ 通过WebHook推送实时市场动态和分析报告
- ✅ 完善的代理配置支持，确保全球范围内稳定访问
- ✅ 支持Docker化部署，便于快速搭建和维护

## 🖥️ 支持平台

- ![Windows](https://img.shields.io/badge/-Windows-0078D6?logo=windows&logoColor=white)
- ![macOS](https://img.shields.io/badge/-macOS-000000?logo=apple&logoColor=white)
- ![Linux](https://img.shields.io/badge/-Linux-FCC624?logo=linux&logoColor=black)
- ![WSL](https://img.shields.io/badge/-WSL-0078D6?logo=windows&logoColor=white) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;➡️[如何在 Windows 上安装 WSL2](https://medium.com/@cryptoguy_/在-windows-上安装-wsl2-和-ubuntu-a857dab92c3e)

## ⚙️ 系统要求

- Python 3.7+
- 互联网连接（用于获取最新市场数据）
- 支持代理服务器配置
- DeepSeek API密钥（用于AI分析功能）

## 🛡️ 安装依赖

### 🔴Linux、WSL、macOS 用户
确保你已安装 `git`，如果未安装请参考➡️[安装git教程](./安装git教程.md)

```bash
git clone https://github.com/oxmoei/BinanceAlpha.git && cd BinanceAlpha && ./install.sh
```

### 🔴Windows 用户
确保你已安装 `git`，如果未安装请参考➡️[安装git教程](./安装git教程.md)

```powershell
# 请以管理员身份启动 PowerShell，依次执行以下命令
Set-ExecutionPolicy Bypass -Scope CurrentUser
git clone https://github.com/oxmoei/BinanceAlpha.git
cd BinanceAlpha
.\install.ps1
```

## 📝 配置环境变量`.env`文件：

```env
WEBHOOK_URL=your_webhook_url_here
DEEPSEEK_API_KEY=your_api_key_here
```

## 🖐️ 使用方法

```
# 获取最新币安Alpha项目列表
poetry run python main.py

# 强制更新数据并重新分析
poetry run python main.py --force

# 获取特定区块链平台的项目
poetry run python main.py --platform Ethereum

# 显示帮助信息
poetry run python main.py --help
```

### Docker部署

本项目支持Docker部署，使用以下命令快速启动：

```bash
# 构建Docker镜像
docker-compose build

# 启动服务
docker-compose up -d
```
---
## 🌐 配置选项

在`config.py`文件中，您可以自定义以下配置：

- **代理设置**：配置`PROXY_URL`和`USE_PROXY`实现全球稳定访问
- **区块链平台**：在`BLOCKCHAIN_PLATFORMS`中添加或修改支持的区块链平台
- **AI模型参数**：调整`DEEPSEEK_AI`配置优化AI分析效果
- **WebHook**：配置`WEBHOOK_URL`实现数据推送
- **数据目录**：通过`DATA_DIRS`自定义各类数据存储位置

## 📊 数据分析能力

### 币安Alpha项目分析

- 项目基础信息提取与展示
- 市值、交易量和价格变化监控
- 自动检测是否已上线币安现货或创新区
- 区块链平台分类分析

### AI智能投资建议

系统利用DeepSeek AI模型分析市场数据，提供：

- 市场总体趋势评估
- 热门区块链生态系统分析
- 潜力项目识别与推荐
- 多维度投资风险评估
- 短期、中期和长期投资建议

## 🗼 数据来源

- 币安Alpha项目数据：CoinMarketCap API
- 币安现货与创新区数据：Binance API
- 区块链平台分类信息：项目标签与描述分析

## ⚠️ 注意事项

- 本系统仅提供市场数据分析参考，不构成投资建议
- 加密货币市场风险较大，请谨慎投资
- API访问可能受到速率限制，请合理控制请求频率
- 使用AI顾问功能需要有效的DeepSeek API密钥

## 许可证

MIT License
