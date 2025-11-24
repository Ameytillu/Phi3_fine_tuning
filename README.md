# Phi-3 Hospitality Support Bot

A fine-tuned **Phi-3 Mini 4K Instruct** model built for hotel and hospitality AI agents.  
This project focuses on customer support, concierge automation, guest FAQs, and hospitality workflows — all powered by a domain-specialized Small Language Model (SLM).

---

## Overview
This repository contains my fine-tuned Phi-3 model designed specifically for the hospitality industry.  
The model has been trained on a custom dataset covering hotel FAQs, room types, policies, amenities, and guest services. It also includes knowledge of restaurants, spas, gyms, pools, parking, EV charging, check-in/check-out processes, tourist attractions, booking tasks, and local recommendations.

The goal is to deliver accurate, context-aware responses that enhance hotel AI agents and guest-facing applications.

---

## Model Details

| Feature              | Description                          |
|----------------------|--------------------------------------|
| **Base Model**       | Microsoft Phi-3 Mini 4K Instruct     |
| **Fine-Tuning Method** | SFT (Supervised Fine-Tuning)       |
| **Precision**        | 4-bit quantization during training   |
| **Final Artifact**   | Fully merged model (base + LoRA)     |
| **Training Hardware**| Google Colab Pro+ (A100 GPU)         |
| **Dataset Size**     | 50,000 hospitality examples          |
| **Training Time**    | ~7.5 hours                          |

---

## Repository Contents
This repo includes all the necessary artifacts to run the model:

- `pytorch_model.bin` — merged fine-tuned weights  
- `config.json` — model configuration  
- `tokenizer.json` / `tokenizer.model` — tokenizer files  
- `generation_config.json` — generation settings  
- Model card with usage examples  

The model can be loaded instantly via the Hugging Face Transformers pipeline.

---

## Intended Use
This model is optimized for hospitality-specific tasks such as:

- Hotel chatbots  
- Front desk automation  
- Concierge assistants  
- Room service & booking support  
- Travel and tourism recommendation systems  
- Hospitality training simulations  
- Multi-agent hotel AI systems  

---

## Training Metrics
- **Perplexity (PPL): 1.28**  
  A very low PPL indicates strong learning of the dataset and highly coherent outputs.

Training was monitored with **Weights & Biases (wandb)**, showing:
- Smooth and consistent loss reduction  
- Stable gradients throughout training  

---

## Summary
Phi-3 Hospitality Support Bot is a domain-specialized fine-tuned model that brings structured intelligence to hotel and hospitality workflows.  
It’s lightweight, efficient, and ready to power next-generation hotel AI agents with reliable, context-aware responses.
<img width="1786" height="1261" alt="image" src="https://github.com/user-attachments/assets/68d4be64-6569-4377-b95c-b3cda44cab61" />

- The train loss curve indicates rapid and stable convergence, demonstrating that the Phi-3 model efficiently adapted to the hospitality domain patterns.
- The linear decay LR schedule prevented catastrophic updates and stabilized late-stage weight refinement.
- Consistent progression of global steps and epochs indicates that the training loop operated without interruption or dropped batches.
- The gradient norm curve shows stable optimization without gradient explosion/vanishing, confirming that weight updates were controlled and consistent.

  <img width="885" height="618" alt="image" src="https://github.com/user-attachments/assets/8f89be5a-598c-420a-ba27-2f6eaf9426ca" />

  

