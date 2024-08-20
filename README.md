# KPop Model Image Generator
![out-0](https://github.com/user-attachments/assets/e7be19a3-fa68-47bd-a242-7c87ef45749c)

This repository contains the fine-tuned model and necessary files to generate images of yourself with a specific idol using a pretrained model from the FLUX series. The model was fine-tuned for a specific use case where you provide images of yourself and your idol, and the model generates high-quality images featuring both of you.

## Model Details

- **Pretrained Model**: FLUX
  - **Commercial Option**: `black-forest-labs/FLUX.1-schnell`
  - **Non-Commercial Option**: `black-forest-labs/FLUX.1-Dev`
- **Training Dataset**: Approximately 30 images of yourself and the specific idol. (Note: Using more images can improve the model's performance.)
- **Hardware Used**: A100 GPU with 80GB RAM
- **Training Time**: 30 minutes

## Files in the Repository

- `config.yaml`: Configuration file used during the training process.
- `flux_train_replicate.safetensors`: The fine-tuned model weights saved in safetensors format.
- `optimizer.pt`: Optimizer state used during training.
- `output`: Directory containing the final outputs after training.

## Usage

1. **Using the Pre-Trained Model**: 
   - If you want to generate images with the current model, simply load the model weights provided in `flux_train_replicate.safetensors`. Once loaded, the model is ready to generate images without any additional training required.

2. **Fine-Tuning Your Own Model**:
   - If you prefer to create your own model with different characters or images, you can start by loading the base model from Hugging Face (`black-forest-labs/FLUX.1-schnell` or `black-forest-labs/FLUX.1-Dev`).
   - Fine-tune the model using your own dataset. For example, in this case, the model was fine-tuned using a collection of images of an Asian idol and some of my own even it not exactly how i look but it captures some aspects like Beards,glasses, all what you need to take into consideration is the quality of data: **Garbage in,Garbage Out**.

## Notes

- The model was trained for 30 minutes on an A100 GPU with 80GB of RAM.
- For best results, consider expanding your training dataset with additional images.
