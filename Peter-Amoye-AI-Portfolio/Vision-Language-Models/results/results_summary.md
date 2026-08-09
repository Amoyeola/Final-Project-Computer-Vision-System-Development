# VLM Results Summary

## CLIP zero-shot classification

- Dataset sample: 300 CIFAR-10 test images
- Baseline prompt accuracy: 90.3%
- Misclassified images: 29 of 300
- Most common confusion: frog predicted as cat, 5 times
- Second most common confusion: truck predicted as automobile, 4 times

## Prompt comparison

| Prompt | Accuracy |
|---|---:|
| `a low-resolution picture of a {}` | 91.0% |
| `a blurry low-resolution photo of a {}` | 90.7% |
| `a photo of a {}` | 90.3% |
| `a small image of a {}` | 89.0% |
| `{}` | 87.7% |

## BLIP

- Caption: “a group of men standing on a street”
- Correct VQA observations included phones, yellow buses, an outdoor setting, and texting.
- Counting limitation: BLIP reported five foreground men when four were clearly visible.
