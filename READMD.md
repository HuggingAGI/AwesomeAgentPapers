# 2025年，AI Agent干货资料、论文综述都在这了


## 1. AI Agent：LLM时代的下一个突破口?

最近相信大家都被Deepseek刷屏了，但训练顶尖模型却只是少数人的战场，真正的产业革命正逐渐转向 **AI Agent（智能体）** 的探索——让LLM从“对话工具”蜕变为“行动者”，通过**自主决策与工具调用**，真正落地于复杂场景。

如果说LLM是大脑，AI Agent则为其赋予了感知环境、规划任务、调用工具（如搜索、API、代码执行）的“手脚”，使其能独立完成订票、数据分析、跨系统协作等实际需求。这种能力突破，让开发者无需从头训练模型，即可通过“智能体架构”激活LLM的无限潜力，成为未来AI应用创新的核心方向。  

![加入社群，+v: iamxxn886](assets/qrcode.png)

### 1.1 什么是AI Agent？

关于Agent，有很多种说法，到底什么样的系统属于AI Agent？

去年，吴恩达提出了Agentic Workflow，还有类似BabyAGI的自主智能体。广义上说，这两种都算AI Agent，两者都能在未来GenAI应用场景发挥巨大作用，但两种有本质上的区别。

### 1.2 Agents与Agentic Workflow的本质区别

二者的核心差异在于系统架构的自主权分配，直接决定了任务执行的灵活性与适用边界。用戏剧比喻：

- **Workflow是严格遵循剧本的演员**

- **Agent是自带导演思维的即兴表演者**

决策控制模式：

- **Agentic Workflow（工作流）**：基于预设规则的线性编排，通过硬编码或配置化流程控制LLM与工具的执行顺序（例如：先调用搜索API获取信息 → 再通过代码工具处理数据 → 最后调用邮件API发送结果）。其决策路径如同火车轨道，所有分支和工具调用在开发阶段已固定。

- **Agent（智能体）**：采用动态决策引擎，由LLM自主生成任务分解策略和工具调用序列（例如：面对“帮我策划旅行”的需求，可能自主选择先查天气 → 再比价机票 → 最后生成行程表）。其决策路径更像GPS导航，根据实时反馈动态调整路线。


### 1.3 两者的系统架构特征

| **维度**         | **Agentic Workflow**                  | **Agent**                          |
|------------------|---------------------------------------|------------------------------------|
| **自主性**       | 低：严格遵循开发者设定的逻辑链条       | 高：LLM自主生成决策树与执行计划     |
| **灵活性**       | 确定性输出，适合结构化场景             | 非确定性输出，适合开放性问题         |
| **工具调用**      | 工具类型和调用顺序预先绑定             | 动态选择工具组合（如临时切换API）    |
| **容错机制**      | 依赖开发者预设异常处理                  | 通过反思（ReAct等框架）自主纠错      |



### 1.4 **技术实现差异**  

- **Agentic Workflow**：依赖**有限状态机（FSM）**或**低代码平台**实现流程编排，开发成本低但扩展性受限**。

- **Agent**：需要构建**认知架构**（如MetaGPT中的角色分工、AutoGPT的目标分解），通常结合记忆机制（VectorDB）、工具库（Toolkit）与强化学习实现持续进化。  

Agentic Workflow是“自动化”，用规则解放人力；Agent是“智能化”，用认知突破规则边界。前者解决效率问题，后者创造解决未知问题的可能性。


## 2. 值得关注的论文综述

要更加系统性的了解AI Agent的前世今生，我们还可以进一步研究2024年AI Agent的这几篇经典综述。这些论文不仅为研究人员提供了宝贵的研究路线图，也为AI Agent的未来发展提供了深刻的洞见。

### 1. Agent AI: Surveying the Horizons of Multimodal Interaction

`多模态` `页数：80页` `引用数：52`

链接: https://arxiv.org/pdf/2401.03568

[阅读PDF](./survey/1_2401.03568v2.pdf)

本篇综述由斯坦福大学、微软研究院、加州大学洛杉矶分校、华盛顿大学等机构的学者联合撰写，包括李飞飞、Jianfeng Gao等。

主要讨论了多模态人工智能系统，尤其是智能体Agent在物理和虚拟环境中的交互性。论文核心分为五个部分：Agent AI的概念、Agent AI存在的挑战、Agent AI的学习、Agent AI的分类与应用、跨模态、跨领域和跨现实的Agent AI。

不仅为研究人员和AI领域提供了一个研究路线图，更是AI领域未来发展的洞见。通过深入探讨多模态交互中的复杂问题，论文为AI Agent的发展提供了新的方向和思路。


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/02/1738481856361-784247de-aa6f-44c4-a89a-ff886d00d49e.png)


### 2. The Rise and Potential of Large Language Model Based Agents: A Survey

`页数：86页` `引用数：719`

链接: https://xuanjing-huang.github.io/files/agent.pdf

[阅读PDF](./survey/2_agent.pdf)


本篇论文由复旦大学自然语言处理团队和米哈游公司共同撰写，全文长达86页，共有600余篇参考文献。从AI Agent的历史出发，全面梳理了基于大型语言模型的智能代理现状，包括LLM-based Agent的背景、构成、应用场景以及备受关注的代理社会。同时，探讨了Agent相关的前瞻开放问题，对相关领域的未来发展趋势具有重要价值。

为理解基于大型语言模型的智能代理提供了全面的框架和背景，对推动AI Agent在不同领域的应用具有重要意义。通过深入分析LLM-based Agent的构成和应用场景，论文为研究人员提供了宝贵的参考和指导。


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738570154119-9b7ea6f3-f5dc-4818-b989-cba4a38e43b2.png)



![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738570179951-1a6fd027-2a4a-4026-8d18-043b2c80decc.png)


### 3. A survey on large language model based autonomous agents

`页数：26页` `引用数：919`

链接：https://link.springer.com/content/pdf/10.1007/s11704-024-40231-1.pdf

[阅读PDF](./survey/3_s11704-024-40231-1.pdf)


本文由中国人民大学高瓴人工智能学院研究团队撰写。系统综述了基于大语言模型（LLM）的自主Agent研究进展。

传统自主代理依赖有限知识在封闭环境中训练，与人类学习模式存在显著差异，而LLM通过海量网络知识获取展现出类人智能潜力。

论文从构建、应用与评估三方面展开分析：在构建层面，提出统一框架整合记忆、规划与工具使用等核心模块，通过外部知识库和工具调用增强LLM的决策能力。


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738571091165-3638ab89-6cfb-42be-9fe0-1947ff4a3a27.png)


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738571111275-216f0976-e70b-466a-8aeb-5da3937ade25.png)

### 4. Large Language Model based Multi-Agents: A Survey of Progress and Challenges

`页数：25页` `引用数：249`

链接：https://arxiv.org/pdf/2402.01680

[阅读PDF](./survey/4_2402.01680v2.pdf)

本文由南方科技大学等多所学校联合撰写。分析了LLM多智能体所模拟的领域和环境、这些智能体的特征及其通信方式，以及促进智能体能力发展的机制。

还总结了该领域常用的数据集和基准，以便有兴趣的研究人员能够方便地获取。为读者提供关于LLM多智能体系统研究进展和挑战的深刻见解。


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738571890270-465c2746-05ca-417d-af81-4b15b98c7f60.png)


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738571904427-8ffc31fb-0a93-4ba2-adba-f094243a6cb3.png)

### 5. Personal LLM Agents: Insights and Survey about the Capability, Efficiency and Security

`页数：62页` `引用数：114`

链接：https://arxiv.org/pdf/2401.05459

[阅读PDF](./survey/5_2401.05459v2.pdf)

本篇论文由清华大学人工智能产业研究院撰写。聚焦于个人大型语言模型（LLM）智能体，探讨了其架构、能力、效率和安全性等关键问题。

通过对领域专家的意见收集和分析，总结了个人LLM代理的关键组件和设计选择，并深入讨论了实现智能、高效和安全的个人LLM代理所面临的挑战，以及相应的解决方案。


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738572531777-05eff991-dc1e-4332-a963-0e609c9b7d92.png)


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738572621930-64731d97-8b8a-47cf-a64c-47458e6f1b29.png)


### 6. Understanding the planning of LLM agents: A survey

`页数：9页` `引用数：82`

链接：https://arxiv.org/pdf/2402.02716

[阅读PDF](./survey/6_2402.02716v1.pdf)

本篇论文由中国科学技术大学和华为诺亚方舟实验室的团队撰写。

对基于大型语言模型（LLM）的智能体规划进行了系统性回顾，提出了一个关于 LLM-Agent 规划的现有工作的分类体系，将其分为五个方向：任务分解、计划选择、外部模块、反思和记忆。每个方向都进行了全面分析，并讨论了该研究领域的挑战。作者旨在提供一个关于基于 LLM 的代理规划能力的系统性视角，这在该领域尚属首次。论文还评估了在四个基准测试上的几种代表性方法，为未来的研究方向提供了见解。

## 3. 值得关注的Multi-Agent框架

### 1. AutoGen 

`Star: 38.6K` `Fork: 5.7K`

GitHub: https://github.com/microsoft/autogen

![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738573671002-283862a5-dc0c-4a6f-b62a-d89ae8354e2c.png)

由微软推出的一个框架，支持创建和管理多个自主Agent，协同完成复杂的任务。这个框架的灵活性极高，可以根据需求定义不同类型的Agent，包括特定任务的专家、通用助手、策略制定者等。AutoGen提供了一个虚拟的对话空间，让Agent之间可以相互沟通和协作，并支持多方对话和协作，包括文本、音频或视频形式。


### 2. LangGraph 

`Star: 8.6K` `Fork: 1.4K`

![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738573716452-0883eb0e-26c8-44b9-a9fe-878d6102c656.png)

GitHub: https://github.com/langchain-ai/langgraph

基于LangChain打造的Multi-Agent框架，通过引入有向循环图的理念，打造了一个极具灵活性和可定制性的解决方案。LangGraph不仅适用于各类Multi-Agent任务，还能支持几乎所有的多智能体编排应用，使其成为那些面临复杂任务、追求高度灵活性和定制化能力的开发者的首选工具。


### 3. OpenAI Swarm 

`Star: 18,4K` `Fork: 1.9K`

GitHub: https://github.com/openai/swarm

OpenAI推出的一个轻量级多智能体编排框架，致力于简化智能体的构建过程以及智能体间的交接操作（即Handoffs）。Swarm框架特别适合初学者，让他们能够轻松入门多智能体技术，快速搭建演示项目。Swarm的智能体组件可以配备工具、指令和其他参数来执行特定任务。

### 4. crewAI

`Star: 8.6K` `Fork: 720`

GitHub: https://github.com/crewAIInc/crewAI


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738574354424-16356284-adec-45c6-800b-2fd40258109e.png)


CrewAI推出的高性能多智能体协作框架，专注于复杂任务的分布式协同与动态角色分配。该框架提供直观的API设计，允许开发者通过声明式代码快速定义智能体角色、目标及交互规则，支持链式任务流、异步通信和实时状态监控。CrewAI强调"以任务为中心"的编排理念，内置任务优先级调度、结果聚合模块，适用于自动化工作流、数据管道和科研计算等场景，助力开发者构建工业级多智能体系统。


## 4. 值得关注的低代码平台

### 1. Dify  

`Star: 61.1K` `Fork: 9.1K`  

GitHub: https://github.com/langgenius/dify  


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738575945061-5dddf5e7-7fe4-4e31-80ac-6544083d5384.png)

核心功能包括可视化 AI Workflow 编排（Orchestration Studio）、高质量 RAG 检索增强生成引擎、多模型无缝切换，以及灵活的任务优先级调度和 Agent 框架。Dify 提供从数据预处理到模型监控的全链路工具，支持私有化部署与 API 集成。



### 2. FastGPT  
`Star: 20K` `Fork: 5.3K`  

GitHub: https://github.com/labring/FastGPT  


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738576117272-18315ff7-a06b-4836-a455-f66e5b4acb9c.png)

自动化数据预处理（支持 PDF、Word 等格式解析）、可视化工作流编排（Flow 模块）、与 OpenAI 对齐的 API 接口，以及针对海量数据的 QA 结构优化。


### BISHENG（毕昇）

`Star: 7.6K` `Fork: 1.3K`  

GitHub: https://github.com/dataelement/bisheng  


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738576521912-4e95946d-aca7-4fb2-a398-acffd8e88d39.png)


支持通过流程图形式自由组合循环、并行、批处理等复杂逻辑，覆盖文档审核、报告生成、多代理协作等企业级场景，用户可实时干预流程执行。集成统一模型管理、RAG增强生成、模型微调（SFT）、数据集管理、安全审计、RBAC权限控制等高阶功能，支持高并发与高可用部署。  

### RAGFlow  

`Star: 2.9K` `Fork: 30.8K`  

GitHub: https://github.com/infiniflow/ragflow


![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2025/02/03/1738576947112-94691627-977b-439a-a42c-1f43cc500b64.png)


专为检索增强生成（RAG）设计的开源框架，整合向量数据库与 LLM 生成能力，提供端到端的知识增强解决方案。最近也增加了Agent 编排的能力，值得一试。


<hr />

- 获取更多最新 Arxiv 论文更新: [https://github.com/HuggingAGI/HuggingArxivLLM](https://github.com/HuggingAGI/HuggingArxivLLM)!
- 加入社群，+v: iamxxn886
- 点击公众号菜单加入讨论
  ![](https://raw.githubusercontent.com/HuggingAGI/wx_assets/main/2024/07/31/1722434818326-94339e92-22f1-4472-9d27-fed232f70b5d.jpeg)
