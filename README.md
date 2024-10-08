# paper list

## Why SLMs may work
Pre-training loss is the key factor for downstream tasks and emergent ablities, not model size and data size:
+ [Understanding Emergent Abilities of Language Models from the Loss Perspective](https://arxiv.org/abs/2403.15796)

## Finetuning
SLMs are very suitable for finetuning to specific tasks and domains.

### Agent
+ [Octopus: On-device language model for function calling of software APIs](https://arxiv.org/pdf/2404.01549)
+ [Octopus v2: On-device language model for super agent](https://arxiv.org/pdf/2404.01744)
+ [Octopus v3: Technical Report for On-device Sub-billion Multimodal AI Agent](https://arxiv.org/pdf/2404.11459)
+ [Octopus v4: Graph of language models](https://arxiv.org/pdf/2404.19296)

### Specific domain
+ [RAD-PHI2: INSTRUCTION TUNING PHI-2 FOR RADIOLOGY](https://arxiv.org/pdf/2403.09725)

### Knowledge Injection
Injecting knowledge is crucial. Use RAG or FT? That's a question:
+ [Fine-Tuning or Retrieval? Comparing Knowledge Injection in LLMs](https://arxiv.org/pdf/2312.05934)
+ [INJECTING NEW KNOWLEDGE INTO LARGE LANGUAGE MODELS VIA SUPERVISED FINE-TUNING](https://arxiv.org/pdf/2404.00213)
+ [Adapting Large Language Models via Reading Comprehension](https://arxiv.org/pdf/2309.09530)
+ [RAG vs Fine-tuning: Pipelines, Tradeoffs, and a Case Study on Agriculture](https://arxiv.org/abs/2401.08406)
+ [RAFT: Adapting Language Model to Domain Specific RAG](https://arxiv.org/abs/2403.10131)

## SLMs, not LLMs
### Different Architecture
Different architecture or SLMs:
+ [MobileLLM: Optimizing Sub-billion Parameter Language Models for On-Device Use Cases](https://arxiv.org/pdf/2402.14905), which use parameter sharing techniques.
+ [Gemma2](https://storage.googleapis.com/deepmind-media/gemma/gemma-2-report.pdf), which combine local attention and global attention.

### Different Training Strategy
Knowledge distillation is great:
+ [Gemma2](https://storage.googleapis.com/deepmind-media/gemma/gemma-2-report.pdf), which use knowledge distillation in PT(Pre-Training) and IT(Instruction-Tuned) stage.

More data and longer training is good(but only with log scale):
+ [MiniCPM: Unveiling the Potential of Small Language Models with Scalable Training Strategies](https://arxiv.org/abs/2404.06395), which uses Warmup-Stable-Decay(WSD) lr scheduler for longer training time.
+ [Index-1.9B](https://github.com/bilibili/Index-1.9B/blob/main/Index-1.9B%20%E6%8A%80%E6%9C%AF%E6%8A%A5%E5%91%8A.pdf), which also use WSD.

## Reasoning Machine
More inference-time compute benefit LLMs, so it's a natural question: `Is it a better way to use cheaper and faster SLMs instead of LLMs to do complex reasoning in inference time?`

