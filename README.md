# Inference‑Based Video Generation Using GANs

**Team Members**  
- Om Vishal (@omvshal)  
- Pradyumn Vashisht 
- Saksham Rana 


---

## 🚀 Project Overview

We build a **Temporal GAN (TGAN)** to predict future video frames from a sequence of input frames.  
Our pipeline evolves through three experimental setups—each adding architectural or training refinements—to produce sharper, more temporally coherent frames on the UCF101 BenchPress subset.

---



## 📂 Repository Structure

```text
inference-video-gan/
├── code/
│   ├── setup2.ipynb             # Enhanced TGAN with residual blocks & BatchNorm
│   ├── setup3.ipynb             # Final TGAN with mixed‑precision & WGAN‑GP
│   ├── evaluate_psnr_ssim.ipynb  # PSNR & SSIM computation
│   └── frames_to_video.ipynb    # Assemble frames into MP4 videos
│
├── dataset/                     # Subset of UCF101 (BenchPress)
│   ├── train/                   # Training video files
│   └── val/                     # Validation video files
│
├── generated_frames/            # Model outputs (predicted frames)
│   ├── setup1/                  # Baseline TGAN frames
│   ├── setup2/                  # Residual‑block TGAN frames
│   └── setup3/                  # Mixed‑precision TGAN frames
│
└── stitched_videos/             # Reconstructed demo videos
    ├── video_8fps.mp4           # 8 fps generated video
    └── video_24fps.mp4          # 24 fps generated video
```
---

## 🔧 Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/omvshal/Major_Project.git

2. **Create and activate a virtual environment**
  python3 -m venv venv
  source venv/bin/activate

4. **Install dependencies**
   pip install -r requirements.txt
   
6. **Prepare the dataset**
   Download the UCF101 BenchPress subset
   Place raw .avi files under dataset/train/ and dataset/val/

## ▶ Usage
1. Train & Visualize SetUp 2
Open code/setup2.ipynb and run all cells to train the enhanced TGAN and view intermediate results.

2. Train & Visualize SetUp 3
Open code/setup3.ipynb and run all cells to train the final mixed‑precision TGAN and inspect outputs.

3. Evaluate Quality
In code/evaluate_psnr_ssim.ipynb, point to a generated frame folder (e.g. generated_frames/setup3/) to compute PSNR and SSIM.

4. Create Demo Videos
Run code/frames_to_video.ipynb, select:

Input folder: generated_frames/setup3/

FPS: 8 or 24
to produce stitched_videos/video_8fps.mp4 and stitched_videos/video_24fps.mp4.

## 🎥 Demo Video
A polished 5‑minute walkthrough is available at:
G89.mp4
