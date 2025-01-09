
# Text-to-Image Generator

This repository contains a Python-based text-to-image generation tool that uses the `Stable Diffusion` model. It allows users to generate high-quality images based on textual prompts.

---

## Features
- **Text-to-Image Generation**: Generate images from textual descriptions using Stable Diffusion.
- **Customizable Parameters**: Configure image size, number of inference steps, and guidance scale.
- **GPU Support**: Leverages CUDA for faster image generation.

---

## Requirements
- Python 3.8 or higher
- Libraries:
  - `torch`
  - `diffusers`
  - `transformers`
  - `matplotlib`
  - `numpy`
  - `tqdm`

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/text-to-image-generator.git
   cd text-to-image-generator
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```


## Usage

### 1. Configuration
The configuration for the generator is defined in the `CFG` class. Key parameters include:
- **`device`**: Determines whether to use CUDA or CPU.
- **`seed`**: For reproducibility.
- **`image_gen_steps`**: Number of inference steps for image generation.
- **`image_gen_model_id`**: ID of the pre-trained Stable Diffusion model.
- **`image_gen_size`**: Dimensions of the generated image.
- **`image_gen_guidance_scale`**: Scale for guidance during generation.


## How It Works
1. The `StableDiffusionPipeline` from the `diffusers` library is used to load the Stable Diffusion model.
2. The `generate_image` function processes the input text prompt and generates an image based on the configuration in the `CFG` class.
3. The generated image is resized and returned as output.

---

## File Structure
```
text-to-image-generator/
├── your_script_name.py  # Main script containing the generator code
├── requirements.txt     # Dependencies for the project
├── README.md            # Project documentation
└── example-output.png   # Example output image
```

---

## Future Enhancements
- Add support for multiple image generation at once.
- Integrate advanced prompt generation using GPT models.
- Improve the user interface for non-programmers.



