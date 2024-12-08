# AI Model Integration Tools

这是一个集成多个AI模型调用的Python工具包，支持主流大语言模型和多模态模型的统一调用。

## 主要功能

### LLM Pool - 多模型统一调用
- **统一接口**: 支持OpenAI、Groq、Together等多个提供商的模型调用
- **异步支持**: 提供同步和异步两种调用方式
- **智能路由**: 自动根据模型名称路由到对应提供商
- **支持模型**:
  - DeepSeek: deepseek-chat
  - Groq: mixtral-8x7b-32768等
  - Together: Qwen2-72B-Instruct等
  - OpenAI: gpt-4o系列

### GLM Series - 智谱AI模型集成
- **文本生成**: GLM-4模型对话能力
- **图像生成**: CogView-3模型图像生成
- **视频生成**: CogVideoX模型视频生成
- **多模态对话**: 支持图片和视频的多模态对话
- **函数调用**: Function Calling功能支持

## 运行方式
重命名`.env.example`为`.env`，并填写对应的API Key

