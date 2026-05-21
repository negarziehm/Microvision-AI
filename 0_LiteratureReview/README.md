# Literature Review

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**: RA-UNet:A New Deep learning Segmentation Method for Semiconductor Wafer Defect Analysis on Fine-grained Scanning Electron Microscope (SEM) Images

  - https://www.researchgate.net/publication/370681497_RA-UNetA_New_Deep_learning_Segmentation_Method_for_Semiconductor_Wafer_Defect_Analysis_on_Fine-grained_Scanning_Electron_Microscope_SEM_Images
  - **Objective**: improve SEM defect quantitative analysis, overcome challenge of diverse defect morphologies, varying defect scales, and the intricate balance between defect areas and backgrounds
  - **Methods**: combined network structure = RA-UNet, 1. Focus on defects and reduce background info 2. UNet extracts morophological features
  - **Outcomes**: IoU score of 71.92 %
  - **Relation to the Project**: analysis of morphological features of individual defects, only few papers on this due to data limitation, interesting model architecture using transformer to extract defect first

- **Source 2**: Shinde et al. — Defect Detection in Photolithographic Patterns Using Synthetic Data

  - https://www.sciencedirect.com/science/article/pii/S240584402501761X
  - **Objective**: this paper studies deep learning for detecting photolithography defects in SEM images, especially when real labeled SEM data is limited
  - **Methods**: the authors generated synthetic SEM images with known bridge and break defects, automatically annotated them, and trained object detection models such as YOLOv8, SSD, and EfficientNet
  - **Outcomes**: YOLOv8 achieved the strongest result, with reported mean average precision of 96%, and when tested on real SEM data it detected 84.6% of bridge defects and 78.3% of break defects
  - **Relation to the Project**: introduces to different existing models, addresses issue of the limited data

- **Source 3**: Defect inspection in semiconductor images using FAST-MCD method and neural network

  - https://link.springer.com/content/pdf/10.1007/s00170-023-12287-z.pdf
  - **Objective**: Develop an automatic semiconductor defect inspection framework capable of detecting defects from a single SEM-like image without requiring golden/reference die images or layout databases. The work aims to improve robustness and interpretability for different semiconductor image structures.
  - **Methods**: The authors proposed a hybrid inspection pipeline that first classifies images into four categories: flat, linear, patterned, and complex.

Cosine similarity and moment tensor analysis were used for structural classification. FAST-MCD (Fast Minimum Covariance Determinant) statistical outlier detection was applied to flat images. Structure-removal techniques were used for linear and patterned images to generate defect-free references. A U-Net + ResNet-style segmentation neural network was applied for complex structures. Data augmentation included normalization, image complement, rotations, and flipping.
  - **Outcomes**: The proposed hybrid framework achieved better segmentation and detection performance compared to conventional CNN-only and self-similarity methods. Dataset: 171 semiconductor images collected from literature. Training set expanded to 2,480 images using augmentation. Achieved highest average GDS and IoU scores among compared methods. Successfully detected all 16 defective validation images while reducing false positives compared to competing approaches.
  - **Relation to the Project**: This paper is highly relevant to our project because it addresses semiconductor/SEM defect inspection under limited-data conditions, similar to our lithography SEM defect detection task. The work demonstrates how combining statistical image analysis with deep learning can improve explainability and robustness beyond conventional black-box CNNs. It also provides valuable ideas for handling repetitive SEM structures, preprocessing strategies, and segmentation-based defect localization using small datasets.
