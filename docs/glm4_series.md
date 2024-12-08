# GLM系列模型调用工具

这是一个用于调用智谱AI（ZhipuAI）GLM系列模型的Python工具包。该工具包封装了GLM-4、CogView-3和CogVideoX等模型的API调用，支持文本生成、图像生成、视频生成以及多模态对话等功能。

## 功能介绍

### 核心功能
- **文本生成**: 使用GLM-4模型进行文本生成和对话
- **图像生成**: 调用CogView-3模型,将文本描述转换为图像
- **视频生成**: 使用CogVideoX模型,基于文本描述生成视频内容
- **多模态对话**: 支持图片和视频的多模态对话能力
- **函数调用**: 支持Function Calling功能,可以调用外部API

## 代码结构

### GLMCreator类方法说明

#### 初始化配置
- `__init__()`: 初始化API密钥和配置环境
- `_download_file()`: 下载并保存生成的文件到assets目录

#### 生成功能
- `generate_image_description()`: 使用GLM-4生成详细的图片描述
- `text_to_image()`: 使用CogView-3将文本转换为图片
- `text_to_video()`: 使用CogVideoX将文本转换为视频

#### 多模态对话
- `vision_chat_with_video()`: 支持视频内容的多模态对话
- `vision_chat_with_image()`: 支持图片内容的多模态对话

#### 智能代理
- `agent_chat()`: 支持函数调用的智能对话代理
- `_mock_weather_api()`: 模拟天气API调用
- `_mock_stock_api()`: 模拟股票API调用

## 使用要求

### 环境依赖
- Python 3.7+
- zhipuai SDK
- python-dotenv
- requests

