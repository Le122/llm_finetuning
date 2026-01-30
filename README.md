
# LLM Fine-Tuning with LoRA on TPU

This repository demonstrates fine-tuning a Large Language Model using
LoRA (PEFT) on TPU via Hugging Face Trainer.

## Key Features
- TPU-based fine-tuning (Colab TPU)
- LoRA adapters using PEFT
- TPU-safe adapter reloading
- Hugging Face Hub integration




## Important TPU Note
Due to a known TPU/XLA edge case, LoRA adapters are reloaded using
`PeftModel.from_pretrained()` instead of moving models across devices.
Adapter merging is intentionally skipped to ensure stable inference.

## Model
- Base: TinyLLaMA 
- Fine-tuning: LoRA (PEFT)

## How to Run
Open the notebook in Google Colab and select TPU runtime.
