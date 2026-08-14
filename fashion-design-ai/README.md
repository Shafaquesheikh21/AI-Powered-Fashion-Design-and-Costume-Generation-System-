\# Fashion Design AI



An AI-powered fashion design toolkit with two components: a \*\*text-to-image generator\*\* for creating new fashion designs from text prompts, and an \*\*image modification tool\*\* for editing existing garment images (e.g. changing color, fabric, or style) using a text instruction.



\## Features



\- \*\*Text-to-Image Generation\*\* — Generate original fashion design concepts (e.g. bridal lehengas, sarees, contemporary outfits) from natural language prompts using Stable Diffusion 2.1.

\- \*\*Image Modification\*\* — Upload an existing garment image and transform it with a text prompt and adjustable strength slider (e.g. "convert the sari to vibrant red") using an SDXL refiner img2img pipeline.

\- Interactive \*\*Gradio\*\* web UI for both tools — no coding needed to try them out.



\## Project Structure



```

fashion-design-ai/

├── Image Generation.ipynb     # Generates fashion designs from text prompts

├── Image Modification.ipynb   # Modifies/edits an uploaded garment image

└── README.md

```



\## Tech Stack



\- \[PyTorch](https://pytorch.org/)

\- \[🤗 Diffusers](https://github.com/huggingface/diffusers) (`StableDiffusionPipeline`, `AutoPipelineForImage2Image`)

\- \[🤗 Datasets](https://github.com/huggingface/datasets) — trained/tested on `tonyassi/fashion-design-images`

\- \[Gradio](https://www.gradio.app/) for the interactive UI

\- Models: `stabilityai/stable-diffusion-2-1` (generation), `stabilityai/stable-diffusion-xl-refiner-1.0` (modification)



\## Setup



```bash

pip install torch diffusers datasets gradio pyarrow==8.0.0 xformers

```



A CUDA-capable GPU is strongly recommended — both pipelines fall back to CPU but will be very slow.



\## Usage



\### 1. Text-to-Image Generation

Open `Image Generation.ipynb` and run all cells. This launches a Gradio app where you can enter a prompt such as:



> "Design a traditional bridal lehenga with gold embroidery and a matching dupatta."



and get a generated design image back.



\### 2. Image Modification

Open `Image Modification.ipynb` and run all cells. This launches a Gradio app where you can:

1\. Upload an image of a garment.

2\. Enter a transformation prompt (e.g. "convert the sari to vibrant red").

3\. Adjust the strength slider to control how much the image changes.

4\. Get the transformed image back.



\## Notes



\- Both notebooks are designed to run in a GPU-backed environment (e.g. Google Colab with a GPU runtime).



\## Author



Shafaque Sheikh

