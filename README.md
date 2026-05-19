---
base_model: Qwen/Qwen2.5-1.5B-Instruct
library_name: peft
pipeline_tag: text-generation
tags:
  - leyoai
  - qwen2.5
  - lora
  - sft
  - workflow-automation
  - flow-automation
license: apache-2.0
language:
  - zh
  - en
---

# LeyoAI Flow Model - Large

## 中文介绍

LeyoAI Flow Model (Large) 是基于 Qwen2.5-1.5B-Instruct 微调的流程自动化助手，专注于工作流设计、业务流程优化和自动化方案生成。该模型使用 LoRA (rank=16, alpha=32) 进行高效微调，适用于流程建模和自动化任务。

### 使用方法

```python
from peft import PeftModel
from transformers import AutoModelForCausalLM, AutoTokenizer

base_model = AutoModelForCausalLM.from_pretrained("Qwen/Qwen2.5-1.5B-Instruct")
model = PeftModel.from_pretrained(base_model, "FFZwai/leyoai-flow-large")
tokenizer = AutoTokenizer.from_pretrained("Qwen/Qwen2.5-1.5B-Instruct")
```

### 训练详情

- 基座模型: Qwen2.5-1.5B-Instruct
- 微调方式: LoRA (rank=16, alpha=32)
- 训练设备: Mac Studio (MPS)
- 训练精度: FP32

### 性能指标

| 指标 | 值 |
|------|-----|
| Eval Loss | N/A |
| Accuracy | N/A |

## English Introduction

LeyoAI Flow Model (Large) is a workflow automation assistant fine-tuned from Qwen2.5-1.5B-Instruct, specializing in workflow design, business process optimization, and automation solution generation. The model uses LoRA (rank=16, alpha=32) for efficient fine-tuning.

### Usage

```python
from peft import PeftModel
from transformers import AutoModelForCausalLM, AutoTokenizer

base_model = AutoModelForCausalLM.from_pretrained("Qwen/Qwen2.5-1.5B-Instruct")
model = PeftModel.from_pretrained(base_model, "FFZwai/leyoai-flow-large")
tokenizer = AutoTokenizer.from_pretrained("Qwen/Qwen2.5-1.5B-Instruct")
```

### Training Details

- Base Model: Qwen2.5-1.5B-Instruct
- Fine-tuning: LoRA (rank=16, alpha=32)
- Device: Mac Studio (MPS)
- Precision: FP32

## License

Apache 2.0

## Links

- Website: https://leyoai.vercel.app
- GitHub: https://github.com/richard3153/leyoai-landing

