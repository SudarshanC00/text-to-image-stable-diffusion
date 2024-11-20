# Fine-Tuning Stable Diffusion for Text-to-Image Generation

This project demonstrates how to fine-tune a Stable Diffusion model for text-to-image generation using a custom dataset on a low-cost cloud GPU. It's based on the guides from [Training Stable Diffusion with a low-cost Cloud GPU](https://learn2train.medium.com/a-step-by-step-guide-for-non-technical-folks-on-training-stable-diffusion-with-a-low-cost-cloud-gpu-344c6b250d64) and [Fine-Tuning Stable Diffusion With A Curated Dataset](https://learn2train.medium.com/a-step-by-step-interactive-guide-on-fine-tuning-stable-diffusion-with-a-curated-dataset-c327135e9158).

## Table of Contents

1. [Project Overview](#project-overview)
2. [Requirements](#requirements)
3. [Setup](#setup)
4. [Usage](#usage)
5. [Training Process](#training-process)
6. [Evaluation](#evaluation)
7. [Results](#results)

## Project Overview

This project aims to fine-tune a Stable Diffusion 1.5 base model using a custom dataset to improve its ability to generate images in a specific style or domain. The process involves:

1. Setting up a low-cost cloud GPU environment
2. Preparing and uploading a custom dataset
3. Configuring and running the training process
4. Monitoring the training progress
5. Evaluating the fine-tuned model
6. Generating images using the fine-tuned model

## Requirements

- A cloud GPU instance with at least 24GB VRAM (e.g., RTX 3090, RTX 4090, or A6000)
- Python 3.7+
- CUDA-compatible environment
- Weights & Biases account for monitoring
- Hugging Face account for model hosting (optional)

## Setup

1. Clone this repository:
   ```
   git clone https://github.com/SudarshanC00/text-to-image-stable-diffusion.git
   cd text-to-image-stable-diffusion
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up your cloud GPU instance following the guide in the [Training Stable Diffusion with a low-cost Cloud GPU](https://learn2train.medium.com/a-step-by-step-guide-for-non-technical-folks-on-training-stable-diffusion-with-a-low-cost-cloud-gpu-344c6b250d64) article.

4. Prepare your custom dataset following the instructions in the [Fine-Tuning Stable Diffusion With A Curated Dataset](https://learn2train.medium.com/a-step-by-step-interactive-guide-on-fine-tuning-stable-diffusion-with-a-curated-dataset-c327135e9158) guide.

## Usage

1. Upload your prepared dataset to the cloud GPU instance.

2. Configure the training parameters in the `config.yaml` file.

3. Start the training process:
   ```
   python train.py
   ```

4. Monitor the training progress using Weights & Biases.

5. After training, evaluate the fine-tuned model using the provided Jupyter notebook.

6. Generate images using the fine-tuned model:
   ```
   python generate.py --prompt "Your text prompt here" --checkpoint path/to/checkpoint.safetensors
   ```

## Training Process

The training process involves fine-tuning a Stable Diffusion 1.5 base model using EveryDream 2 trainer. Key aspects of the training include:

- Using a custom dataset with captioned images
- Configuring training parameters such as batch size, learning rate, and number of epochs
- Implementing techniques like zero-frequency noise and conditional dropout
- Generating sample images during training for progress monitoring

Detailed training configurations can be found in the `config.yaml` file.

## Evaluation

Evaluate the fine-tuned model using the provided Jupyter notebook. This allows you to:

- Test different checkpoints saved during training
- Experiment with various prompts and generation parameters
- Compare the output of the fine-tuned model with the base model

## Results
![image](https://github.com/user-attachments/assets/579b1682-0339-443b-820f-e310331b48d1)
![image](https://github.com/user-attachments/assets/7f2bb31e-e3a6-4cdd-a968-26f5d4823ac6)
<img width="910" alt="Screenshot 2024-11-19 at 1 10 26 PM" src="https://github.com/user-attachments/assets/7eee23b3-5960-41a6-81f0-d504c7207443">


Citations:</br>
[1] https://learn2train.medium.com/a-step-by-step-guide-for-non-technical-folks-on-training-stable-diffusion-with-a-low-cost-cloud-gpu-344c6b250d64</br>
[2] https://learn2train.medium.com/a-step-by-step-interactive-guide-on-fine-tuning-stable-diffusion-with-a-curated-</br>
[3] https://learn2train.medium.com/a-step-by-step-guide-for-non-technical-folks-on-training-stable-diffusion-with-a-low-cost-cloud-gpu-344c6b250d64</br>
[4] https://learn2train.medium.com/a-step-by-step-interactive-guide-on-fine-tuning-stable-diffusion-with-a-curated-dataset-c327135e9158</br>
