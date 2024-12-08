# LLM Pool - 多模型统一调用工具

这是一个用于统一调用多个大语言模型API的Python工具包。该工具包封装了OpenAI、Groq、Together等多个模型提供商的API调用，提供统一的接口进行模型调用。

## 功能介绍

### 核心功能
- **统一接口**: 提供统一的接口调用不同厂商的模型
- **多模型支持**: 支持OpenAI、Groq、Together等多个提供商的模型
- **异步调用**: 支持同步和异步两种调用方式
- **智能路由**: 根据模型名称自动路由到对应的提供商

### 支持的模型
- **DeepSeek**: deepseek-chat
- **Groq**: mixtral-8x7b-32768, llama3-70b-8192等
- **Together**: Qwen/Qwen2-72B-Instruct, codellama/CodeLlama-34b-Python-hf等
- **OpenAI**: gpt-4o, gpt-4o-mini

## 代码结构

### 主要类

#### ModelProvider (Enum)
- 模型提供商枚举类
- 包含DEEPSEEK、OPENAI、GROQ、TOGETHER等提供商

#### APIConfig (Dataclass)
- API配置数据类
- 包含base_url和api_key配置

#### ModelRegistry
- 模型注册表类
- 管理模型到提供商的映射关系
- 提供模型查询功能

#### ConfigManager
- 配置管理器类
- 管理各个提供商的API配置
- 从环境变量加载配置信息

#### LLMClientFactory
- LLM客户端工厂类
- 根据模型名称创建对应的客户端实例
- 支持同步和异步客户端创建

#### LLMResponse
- LLM响应处理类
- 处理聊天完成请求
- 支持JSON响应、工具调用等功能

