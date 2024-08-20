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

1. **Selecting the Model**: Choose between the commercial (`FLUX.1-schnell`) or non-commercial (`FLUX.1-Dev`) version of the FLUX model based on your usage needs.

2. **Training Data**: Ensure you have a dataset with approximately 30 images of yourself and the idol. More images are recommended for better results.

3. **Running Inference**: Use the provided files to generate new images featuring yourself with the idol.

## Notes

- The model was trained for 30 minutes on an A100 GPU with 80GB of RAM.
- For best results, consider expanding your training dataset with additional images.
