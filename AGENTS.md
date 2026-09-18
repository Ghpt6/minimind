项目内容如下：

- **根目录文件**
  - [eval_llm.py]：命令行模型推理与对话测试。
  - [README.md]：项目介绍、训练教程、部署说明和更新记录。
  - [requirements.txt]：Python 依赖列表。  

- **[model/]：模型实现**
  - `model_minimind.py`：MiniMind 模型结构，包含 Dense、MoE、注意力和位置编码。
  - `model_lora.py`：LoRA 的实现、加载、保存与权重合并。
  - `tokenizer.json`：分词器词表与规则。
  - `tokenizer_config.json`：分词器配置与聊天模板。

- **[trainer/]：训练代码**
  - `train_tokenizer.py`：训练分词器。
  - `train_pretrain.py`：预训练。
  - `train_full_sft.py`：全参数监督微调。
  - `train_lora.py`：LoRA 微调。
  - `train_dpo.py`：DPO 偏好优化。
  - `train_ppo.py`：PPO 强化学习。
  - `train_grpo.py`：GRPO 等强化学习训练。
  - `train_agent.py`：支持多轮工具调用的 Agent 强化学习。
  - `train_distillation.py`：教师模型向学生模型蒸馏。
  - `rollout_engine.py`：训练中的文本生成引擎，支持 PyTorch、SGLang。
  - `trainer_utils.py`：训练通用工具，包括学习率、分布式训练、检查点和模型初始化。

- **[dataset/]：数据处理**
  - `lm_dataset.py`：预训练、SFT、DPO、RLAIF、Agent RL 的数据加载与处理。
  - `dataset.md`：数据集存放说明。
  - 当前目录没有实际训练数据文件，需另行下载。

- **[scripts/]：推理与辅助工具**
  - `web_demo.py`：基于 Streamlit 的网页聊天界面。
  - `serve_openai_api.py`：兼容 OpenAI API 的模型服务。
  - `chat_api.py`：API 聊天调用示例。
  - `eval_toolcall.py`：工具调用测试与评估。
  - `convert_model.py`：模型格式转换及 LoRA 权重合并导出。


目前用户是一个初学者，正在通过这个项目来学习大模型训练相关的知识。