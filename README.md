# Task-02: Image Generation with Pre-trained Models

## 📌 Project Overview
This project involves the implementation of a **Text-to-Image Generation** pipeline as part of my internship at **ProDigy InfoTech**. Using the **Stable Diffusion v1.5** model, I developed an interactive interface that allows users to generate high-quality, realistic images from textual descriptions.

## 🚀 Features
*   **Model:** Utilizes the pre-trained `runwayml/stable-diffusion-v1-5`.
*   **Performance:** Integrated **DPMSolverMultistepScheduler** for faster and sharper image generation.
*   **Interface:** Built a web-based UI using **Gradio** for seamless user interaction.
*   **Optimization:** Optimized for **CUDA-enabled GPUs** to ensure rapid inference.

## 🛠️ Tech Stack
*   **Language:** Python
*   **Libraries:** `diffusers`, `transformers`, `accelerate`, `torch`
*   **UI Framework:** `Gradio`
*   **Environment:** Google Colab (T4 GPU)

## 📸 Demo & Results

| Prompt | Generated Image |
| :--- | :--- |
| *A breathtaking wide-angle landscape of a sunflower farm at sunset.* | ![Sunflower Farm](link_to_your_image_1.png) |
| *A realistic commercial airplane flying through a clear blue sky.* | ![Plane](link_to_your_image_2.png) |
| *A hyper-realistic macro photograph of a red rose with dew drops.* | ![Rose](link_to_your_image_3.png) |

> **Note:** Replace the image links above with the actual images you save from your Gradio interface.

## ⚙️ How to Run
1.  Open the provided `.ipynb` notebook in **Google Colab**.
2.  Ensure the Runtime is set to **GPU** (Runtime > Change runtime type > T4 GPU).
3.  Install dependencies:
    ```bash
    pip install diffusers transformers accelerate gradio
    ```
4.  Run all cells to launch the Gradio interface.
5.  Enter your prompt and click **Submit**.

## 🧩 Challenges & Solutions
*   **Quality Issues:** Initial images were grainy. Fixed by switching the scheduler to `DPMSolverMultistepScheduler` and increasing `num_inference_steps` to 50.
*   **Connection Errors:** Encountered `SyntaxError: Unexpected token '<'` due to tunnel timeouts. Resolved by restarting the Gradio cell and using the local URL for stable recording.

---
Created by [Your Name] | Internship Task-02 | ProDigy InfoTech
