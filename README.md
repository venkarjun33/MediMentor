# 🩺 MediMentor

**An AI-powered chatbot fine-tuned for healthcare consultations, built using LoRA and deployed with Gradio.**

---

## 🧠 Overview

MediMentor is a domain-specific healthcare chatbot developed by fine-tuning a lightweight large language model (LLM) for generating doctor-patient dialogues. This project adapts a general-purpose instruction-tuned model to understand and respond to medical queries effectively.

---

## 🎯 Features

- 🔍 **Healthcare Dialogue Understanding**
- 🛠️ **Efficient Fine-Tuning with LoRA & 4-bit Quantization**
- 💬 **Conversational Web Interface using Gradio**
- ⚡ **Fast Deployment with Lightweight Model (Phi-3 Mini)**
- 📦 **Hosted on Hugging Face for seamless integration**

---

## 🧰 Tech Stack

| Component          | Technology                  |
|-------------------|-----------------------------|
| Base Model        | `unsloth/Phi-3-mini-4k-instruct` |
| Fine-Tuning       | LoRA + 4-bit Quantization   |
| Dataset           | ChatDoctor-HealthCareMagic-100k |
| Interface         | Gradio                      |
| Hosting           | Hugging Face 🤗 Hub         |
| Frameworks        | Transformers, TRL, PEFT     |

---

## 🧪 Model Training

- **Technique**: Supervised fine-tuning using `SFTTrainer` from `trl`
- **Quantization**: 4-bit
- **LoRA Injection Points**: `q_proj`, `k_proj`, `v_proj`, `o_proj`, `gate_proj`, `up_proj`, `down_proj`
- **Hyperparameters**:
  - `r = 16`, `alpha = 16`, `dropout = 0`
  - Max tokens: 2048
- **Prompt Format**: Alpaca-style

### 🗃️ Dataset Format

- **Input**: Patient query  
- **Output**: Doctor response

---

## 💬 Chatbot Deployment

MediMentor is deployed as a web-based chatbot using Gradio.

### 📌 Features

- Intuitive UI with input box and response display
- Styled chat interface
- Example questions and disclaimers
- Supports CPU and CUDA

---

## 🚀 Getting Started

### 🔧 Installation

```bash
pip install gradio transformers
```
---
## 🌐 Online Access
You can try the live demo or view the model on Hugging Face here:
🔗 https://huggingface.co/Venkatesh20/healthbot
---

## UI Preview
![image](https://github.com/user-attachments/assets/0eda7283-1d3e-4271-837b-d0ff2babbcf0)
---

## ⚠️ Disclaimer
This chatbot is for educational and research purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always consult a licensed physician for any health-related concerns.
---

## 👤 Author
Venkateshwaran S V 


Coimbatore Institute of Technology
