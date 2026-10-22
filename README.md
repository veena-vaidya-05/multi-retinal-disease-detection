# Multi-Retinal-Disease Detection Using Hybrid Transformer

Multi-label detection of 8 retinal conditions from fundus images on the ODIR-5K dataset, using a hybrid EfficientNet-B3 + CBAM + FPN + Swin-T model. Includes Grad-CAM and occlusion explanations and a Gradio web UI for left and right eye images.

## Classes
Normal, Diabetes, Glaucoma, Cataract, AMD, Hypertension, Myopia, Other

## Dataset
ODIR-5K (Kaggle: andrewmvd/ocular-disease-recognition-odir5k)

## Model
- EfficientNet-B3 (CNN) with CBAM attention and FPN
- Swin-T (transformer)
- Features are fused, then a classifier gives 8 yes/no outputs (sigmoid)

## Workflow
1. Verify dataset and build per-eye labels
2. Patient-level split: 70 / 15 / 15
3. Preprocessing: resize to 224x224 + CLAHE
4. Training with Asymmetric Loss and AdamW
5. Best validation checkpoint (macro AUC)
6. Evaluation: AUC, F1, precision, recall, specificity, PR-AUC, accuracy
7. Explainability: Grad-CAM and occlusion maps
8. Gradio web UI (left eye and right eye upload)

## How to run
1. Open the notebook on Kaggle with GPU enabled and Internet ON.
2. Add the ODIR-5K dataset as input.
3. Run the cells in order.

## Files
- `multiretinaldiseasedetectionusinghybridtransforms.ipynb`: full project code (kaggle notebook)

## Note
Research prototype. Not for medical use.

## Teams
SINDHU,
SNEHA S SHETTY,
VEENA VASUDEVA VAIDYA,
VENKATESH R,
Dept. of ISE, EPCET
