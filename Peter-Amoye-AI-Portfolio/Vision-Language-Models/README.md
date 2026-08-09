# Vision-Language Models with CLIP and BLIP

## Problem Statement

Traditional computer vision models often perform one predefined task. Vision-language models connect visual information with natural language, enabling flexible tasks such as matching images with text, zero-shot classification, captioning, and visual question answering.

## Approach

This project explores two complementary model families:

- **CLIP** for image–text similarity and zero-shot classification
- **BLIP** for image captioning and visual question answering

The notebook compares model responses across several images and prompts and reflects on where concrete descriptions work better than abstract language.

## Technologies Used

- Python and Google Colab
- PyTorch
- Hugging Face Transformers
- CLIP and BLIP
- CIFAR-10
- Pillow, NumPy, and Matplotlib

## Dataset

The classification section uses the public CIFAR-10 dataset. Do not upload CIFAR-10 to GitHub. The notebook should load it programmatically and identify its source in the documentation.

## Results

The experiments demonstrate:

- Image-to-text and text-to-image similarity
- Zero-shot classification with natural-language prompts
- Automatic image captioning
- Visual question answering
- Stronger CLIP performance with clear, concrete prompts than with abstract descriptions

Add screenshots from the executed notebook showing one CLIP result and one BLIP caption or VQA result.

## Key Findings

- Prompt wording affects zero-shot predictions.
- CLIP is effective for similarity and classification but does not generate full natural-language descriptions.
- BLIP supports generative tasks such as captioning and answering questions about an image.
- Real applications must consider bias, hallucination, accessibility, and the need for human review.

## How to Run

1. Open `VLM_InClass_Lab_ITAI1378_Peter_Amoye.ipynb` in Google Colab.
2. Select a GPU runtime if available.
3. Run the installation and import cells first.
4. Run the remaining cells in order so all model and dataset variables are defined.
5. Confirm that images, similarity scores, captions, and answers are visible.

## Repository Files to Add

- `VLM_InClass_Lab_ITAI1378_Peter_Amoye.ipynb` — completed notebook with visible outputs
- `results/clip_result.png`
- `results/blip_result.png`
