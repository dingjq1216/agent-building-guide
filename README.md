# 智能体构建全流程指南

> 从大模型选型到生产部署 —— 掌握 AI Agent 从 0 到 1 的完整开发流程

## 项目简介

这是一份**系统性的技术指南**，以交互式 HTML 文档的形式，详细讲解如何从零开始构建生产级智能体（AI Agent）。涵盖 12 个核心章节，从底层大模型选型到上层部署运维的完整技术链路。

## 核心特性

- **12 章完整覆盖**：从模型选型到部署运维，全流程无遗漏
- **技术深度**：每种技术都深入到数学原理层面（如 LoRA 的低秩分解公式、RLHF 的 Bradley-Terry 模型、PPO 裁剪目标函数等）
- **交互式 UI**：代码块默认折叠可展开，技术详情面板手风琴式展开
- **可折叠代码**：所有代码示例默认折叠，点击展开，保持页面整洁
- **暗色主题**：深色护眼设计，毛玻璃效果，渐变色彩
- **响应式设计**：完美适配桌面和移动端
- **Mermaid 图表**：内置流程图、架构图、时序图

## 章节目录

| 章节 | 标题 | 核心内容 |
|------|------|----------|
| 01 | 大模型选型与硬件选型 | FP32/FP16/BF16/FP8/INT8/INT4 精度对比、GPU 显存计算、开源 vs 闭源 |
| 02 | 大模型训练 | 预训练、SFT、LoRA/QLoRA/Prefix Tuning/P-Tuning v2/Adapter/IA³、RLHF/DPO/KTO/ORPO 对齐 |
| 03 | 感知模块与关键技术 | 文本分块策略、ViT/CLIP/SigLIP 编码器、多模态融合 |
| 04 | 规划模块与关键技术 | CoT、ReAct、Plan-and-Execute、Tree-of-Thoughts (BFS/DFS/Beam Search) |
| 05 | 记忆模块与关键技术 | 短期对话管理、向量数据库 (HNSW/IVF/PQ)、知识图谱、RAG (重排序/混合检索/查询改写) |
| 06 | 行动模块与技术 | 工具注册中心、API 执行器、Docker 代码沙箱、硬件控制 (GPIO/Serial) |
| 07 | 结果反馈闭环 | 结果验证器、LLM-as-Judge 评分、自动修正控制器 |
| 08 | 反思模块 | Reflexion 框架、事后/事中/事前反思、执行监控器 |
| 09 | 上下文压缩机制 | 滑动窗口、Token 剪枝、语义摘要压缩、KV Cache 优化 (H2O/StreamingLLM) |
| 10 | Harness 与 Skills | Agent 运行时框架、Skill 设计模式、框架对比 (LangChain/LlamaIndex/AutoGPT/MetaGPT) |
| 11 | 工作流设计 | 工作流引擎、线性/分支/并行/循环模式、多 Agent 协作 |
| 12 | 部署与运维 | 推理优化 (量化/Continuous Batching/Speculative Decoding)、Docker 部署、Prometheus 监控 |

## 技术亮点

### 精度格式对比
详细对比 FP32、FP16、BF16、FP8 (E4M3/E5M2)、INT8、INT4/NF4 的位分配、动态范围、显存占用，附带量化数学公式。

### 微调技术详解
每种微调方法都有独立的技术面板，展开后包含：
- **LoRA**：低秩分解 W = W₀ + BA，秩选择策略，合并权重
- **QLoRA**：NF4 量化 + 双重量化 + 分页优化器
- **Prefix Tuning**：可学习前缀嵌入 [Pᵢ, X]
- **P-Tuning v2**：逐层连续提示
- **Adapter**：瓶颈网络 d→r→d
- **IA³**：元素级缩放向量

### 对齐技术深度解析
- **RLHF**：Bradley-Terry 奖励模型 + PPO 裁剪目标函数 (含 KL 惩罚)
- **DPO**：从策略比率直接推导奖励，消除奖励模型
- **KTO**：基于前景理论的二元反馈
- **ORPO**：单阶段 SFT + 偏好学习 (Odds Ratio)

## 使用方法

1. 克隆仓库
```bash
git clone https://github.com/your-username/agent-building-guide.git
```

2. 直接在浏览器中打开
```bash
# 方式一：直接打开
open agent-building-guide/agent-building-guide.html

# 方式二：启动本地服务器
cd agent-building-guide
python -m http.server 8000
# 访问 http://localhost:8000/agent-building-guide.html
```

## 技术栈

- **前端**：原生 HTML + CSS + JavaScript，无框架依赖
- **图表**：Mermaid.js (流程图、时序图)
- **字体**：Instrument Sans + JetBrains Mono
- **主题**：暗色主题，CSS 变量驱动

## 适用人群

- 具备 Python 基础和 AI 知识的开发者
- 希望构建智能体的工程师
- 学习 LLM 应用开发的学生

## 许可证

MIT License - 可自由使用、修改和分发

## 贡献

欢迎提交 Issue 和 Pull Request！
