# Image-Generation-Finetuning

This project demonstrates how to fine-tune a Stable Diffusion model for image generation and compare its performance with the original pre-trained model.

## Overview

- **Stable Diffusion Loading**: The notebook loads a pre-trained Stable Diffusion v1.5 model as the starting point.
- **Fine-tuning with Local Dataset**: The notebook shows the process of fine-tuning a Stable Diffusion model, the UNet component of the model is fine-tuned using a custom dataset of images stored locally. This process adapts the model to generate images tailored to a specific domain or style, such as new species generation or other custom tasks.
- **Comparison**: The outputs of the base and fine-tuned models are compared using the same text prompts and random seed.
- **Evaluation**: The quality of generated images is evaluated using the CLIP model, which scores how well each image matches its prompt.

## How to Use

1. **Install Dependencies**  
   Install required Python libraries:
   ```
   pip install -r requirements.txt
   ```

2. **Run the Notebook**  
   Open and execute `stablediff_model_finuted.ipynb` in Jupyter Notebook or VS Code.

3. **Model Files**  
   - The fine-tuned UNet and tokenizer files are located in the `finetuned-model/` directory after being generated.
   - The notebook will automatically load both the base and fine-tuned models.

4. **Image Generation & Evaluation**  
   - The notebook generates images for a set of prompts using both models.
   - It uses the CLIP model to score each image and prints the results for comparison.

## Results

For each prompt, the notebook displays the CLIP scores for both models and highlights which model performed better.

---

This project provides a practical example of loading, fine-tuning, and evaluating diffusion models for custom image generation tasks using a specific dataset.