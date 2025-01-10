# 简易翻译 Web 应用

一个轻量级的基于 Web 的翻译应用，支持自动语言检测和中英互译。用户可以输入文本，应用会识别语言并将其翻译成目标语言。

---

## 功能特性

- **自动语言检测**：
  - 自动检测输入是中文还是英文。
- **中英互译**：
  - 在中文和英文之间进行翻译。
- **可配置设置**：
  - 配置 OpenAI API Key。
  - 选择使用的 OpenAI 模型（例如 GPT-4）。
  - 调整翻译结果的最大字符长度。
- **用户友好的界面**：
  - 简单直观的设计，包括输入和输出部分。

---

## 技术栈

- **前端**：React（或 Vue.js 替代）
- **后端**：Node.js + Express
- **API**：OpenAI GPT API 提供翻译服务
- **样式**：Tailwind CSS

---

## 前置要求

在运行应用之前，请确保具备以下条件：

1. **Node.js**：已安装并配置。
2. **OpenAI API Key**：在 [OpenAI 官网](https://platform.openai.com/) 注册并获取 API Key。

---

## 安装步骤

1. **克隆代码仓库**：

   ```bash
   git clone https://github.com/your-repo/simple-translator.git
   cd simple-translator
   ```

2. **安装依赖**：

   ```bash
   npm install
   ```

3. **设置环境变量**：

   在项目根目录创建 `.env` 文件并添加：

   ```env
   OPENAI_API_KEY=your-api-key
   PORT=3000
   ```

4. **运行应用**：

   ```bash
   npm start
   ```

5. **访问应用**：

   打开浏览器，访问 `http://localhost:3000`。

---

## 使用说明

1. **主界面**：
   - 在输入框中输入需要翻译的文本。
   - 应用会自动检测语言并显示翻译结果。

2. **设置界面**：
   - 点击齿轮图标进入设置页面。
   - 配置 API Key 并选择使用的 OpenAI 模型。
   - 保存设置后即可使用翻译功能。

---

## 项目结构

```
.
├── src
│   ├── components
│   │   ├── Translator.js  # 主翻译组件
│   │   ├── Settings.js    # 设置组件
│   ├── utils
│   │   ├── api.js         # API 交互逻辑
│   │   ├── language.js    # 语言检测逻辑
├── public
│   ├── index.html         # 入口 HTML 文件
├── .env                   # 环境变量
├── package.json           # 依赖与脚本
├── README.md              # 项目文档
```

---

## API 接口参考

### 翻译 API

- **接口地址**：`POST /translate`
- **请求参数**：
  ```json
  {
    "text": "string",
    "targetLanguage": "string"
  }
  ```
- **返回结果**：
  ```json
  {
    "translation": "string"
  }
  ```

---

## 未来增强功能

- 增加对更多语言的支持。
- 实现语音转文字和文字转语音功能。
- 添加用户认证以实现个性化 API Key 存储。

---

## 许可证

本项目基于 MIT 许可证开源。详情请参阅 `LICENSE` 文件。

---

## 贡献指南

欢迎贡献！请 fork 仓库并提交 Pull Request。

---

## 联系方式

如有问题或需要支持，请联系 [your-email@example.com]。
