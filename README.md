Model weights are here:

Pre-trained model weights: https://drive.google.com/file/d/19aU_duXUuogzflBNUPYfAH2jSus3RKls/view?usp=sharing

Kaggle position: 

<img width="2403" height="1136" alt="image" src="https://github.com/user-attachments/assets/99f7c31b-3ec9-4788-924a-5e12cf567b43" />

To setup the environment, host the notebook on Colab and use the T4 Nvidia GPUs. Here are some required packages:
```
torch
torchvision
numpy
pandas
Pillow
matplotlib
```

Put `train.zip` and `test.zip` in your Google Drive at:
```
/MyDrive/cse144/train.zip
/MyDrive/cse144/test.zip
```
The script will mount them automatically.

hyperparameters:
| Parameter | Value |
|---|---|
| Model | ViT-B/16 (IMAGENET1K\_SWAG\_E2E\_V1) |
| Image size | 384 × 384 |
| Optimizer | AdamW |
| Backbone LR | 1e-5 |
| Head LR | 1e-4 |
| Weight decay | 1e-4 |
| Epochs (val phase) | 60 |
| Epochs (full retrain) | 30 |
| Batch size | 32 |
| Random seed | 41 |

To generate `submission.csv` from a trained model:

1. Ensure `best_model_full.pth` is at `/content/drive/MyDrive/cse144/best_model_full.pth`
2. Run the inference cell at the bottom of `kaggle.ipynb`
3. Output is saved to `/content/drive/MyDrive/cse144/submission.csv`
