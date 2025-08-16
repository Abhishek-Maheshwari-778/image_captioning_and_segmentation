# 🖼️ Image Captioning & Panoptic Segmentation

An end-to-end Gradio app that combines **Mask2Former** (panoptic segmentation) with **BLIP-2** (image captioning) to produce a context-aware description of an image and draw labeled boxes for detected objects. Built with PyTorch and 🤗 Transformers.

---

## ✨ Features
- **Two-in-one pipeline:** Segments objects and generates a caption that references detected classes.  
- **Upload or URL input:** Choose to upload an image or paste an image URL.  
- **Interactive UI:** Clean Gradio interface with example images and one-click processing.  
- **GPU-aware:** Automatically uses CUDA if available for faster inference.  

---

## 🧠 Models Used
- **Segmentation:** `facebook/mask2former-swin-large-coco-panoptic` (Mask2Former) for **panoptic segmentation**.  
- **Captioning:** `Salesforce/blip2-opt-2.7b` (BLIP-2 OPT 2.7B) for **context-aware captions**.  

The script auto-downloads models from the Hugging Face Hub on first run.

---

## 🏗️ Project Structure
├── image_captioning_and_segmentation.py # Main app (Gradio UI + pipeline)
└── README.md # This file


---

## ⚙️ Installation
> Python 3.9+ recommended. A GPU with CUDA is ideal for speed, but CPU works too.

```bash
# 1) Create & activate a virtual environment (recommended)
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

# 2) Install dependencies
pip install --upgrade pip
pip install gradio transformers Pillow torch torchvision torchaudio

▶️ Usage
python image_captioning_and_segmentation.py
