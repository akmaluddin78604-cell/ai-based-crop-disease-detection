# AI-Based Crop Disease Detection Using Deep Learning

A literature-based study and proposed framework for detecting crop
diseases using artificial intelligence, computer vision, and deep
learning.

## Project Overview

Crop diseases can reduce agricultural productivity, particularly when
symptoms are not identified early. This project reviews deep-learning
approaches for recognizing crop diseases from plant images and proposes
an end-to-end framework that can support preliminary disease screening
in agricultural settings.

The study covers **rice, wheat, sugarcane, maize, cotton, soybean,
potato, tea, and jute**. It discusses image classification, object
detection, image acquisition, transfer learning, explainable AI, and
deployment on mobile or edge devices.

> **Project status:** This repository describes the study and proposed
> methodology in the accompanying academic report. The report does not
> establish that a complete, trained, deployable detection application
> has been implemented. Add source code, trained weights, and measured
> results here when they are available.

## Objectives

-   Study AI and deep-learning techniques used for crop disease
    detection.
-   Review crop-specific research and reported methods.
-   Examine datasets, image preprocessing, augmentation, and transfer
    learning.
-   Compare deep-learning model families and their strengths and
    limitations.
-   Identify challenges that affect performance in real field
    conditions.
-   Propose a multi-crop detection workflow with explainability and
    practical deployment in mind.

## Crops in Scope

-   Rice
-   Wheat
-   Sugarcane
-   Maize
-   Cotton
-   Soybean
-   Potato
-   Tea
-   Jute

**Note on jute:** The report treats jute as a proposed extension and
research gap because the reviewed reference material did not provide a
sufficiently identified jute-specific study. No jute accuracy or study
result is claimed.

## Proposed Workflow

1.  **Image acquisition** -- collect plant or leaf images using
    smartphones, digital cameras, field cameras, or UAVs.
2.  **Preprocessing** -- prepare images for model input, including
    resizing and normalization as appropriate.
3.  **Data augmentation** -- use suitable transformations such as
    rotation, flipping, scaling, brightness and contrast changes, and
    controlled noise.
4.  **Model selection** -- choose a model based on crop, dataset size,
    hardware, and whether the task is classification or detection.
5.  **Training and validation** -- split data into training, validation,
    and test sets while avoiding leakage between images from the same
    plant or field.
6.  **Prediction** -- classify a crop image or detect disease instances
    and their locations.
7.  **Explainability** -- where appropriate, use methods such as
    Grad-CAM, SHAP, or LIME to provide visual explanations.
8.  **Deployment concept** -- consider smartphone, edge-device, or cloud
    inference depending on connectivity and available computing
    resources.

## Deep-Learning Approaches Reviewed

  -----------------------------------------------------------------------
  Model / approach        Potential role          Main consideration
  ----------------------- ----------------------- -----------------------
  CNN                     Image classification    Learns image features
                                                  automatically; may need
                                                  substantial data

  ResNet                  Classification          Residual connections
                                                  support deeper networks

  MobileNet               Classification and edge Compact and efficient
                          deployment              

  Inception               Classification          Multi-scale feature
                                                  extraction; more
                                                  computationally
                                                  demanding

  DenseNet                Classification          Feature reuse; may add
                                                  memory and compute
                                                  overhead

  ConvNeXt                Classification          Modern CNN feature
                                                  representation

  YOLO                    Object detection        Localizes multiple
                                                  instances; requires
                                                  bounding-box
                                                  annotations

  Vision Transformer      Classification or       Global attention; can
                          detection               be data- and
                                                  compute-intensive

  Attention modules       Feature refinement      Can emphasize
                                                  disease-relevant
                                                  regions but add
                                                  complexity
  -----------------------------------------------------------------------

The report does not identify one model as universally best for every
crop or dataset.

## Datasets Mentioned in the Report

The report references the following datasets and approximate image
counts from its source material:

  Dataset                      Crop coverage      Approximate images
  ---------------------------- ---------------- --------------------
  PlantVillage                 Multiple crops                 87,000
  PlantDoc                     Multiple crops                  2,598
  Rice disease image dataset   Rice                            4,200
  Maize dataset                Maize                           2,107
  Wheat dataset                Wheat                           1,600
  Tea dataset                  Tea                             6,325
  Soybean dataset              Soybean                         3,150

These figures are reproduced as representative counts reported in the
academic report; verify the original dataset sources before using them
in experiments.

## Evaluation Metrics

A future implementation should report suitable metrics for its task:

-   **Accuracy:** proportion of all predictions that are correct.
-   **Precision:** proportion of predicted positive cases that are
    correct.
-   **Recall:** proportion of actual positive cases detected.
-   **F1-score:** harmonic mean of precision and recall.
-   **Mean Average Precision (mAP):** commonly used for object
    detection.
-   **Inference time / FPS:** practical prediction speed.
-   **Confusion matrix:** class-wise view of prediction errors.

Results from different papers should not be compared as a direct ranking
unless datasets, classes, test conditions, and metrics are comparable.

## Challenges and Research Gaps

-   Dataset bias and limited geographic diversity.
-   Differences in lighting, weather, backgrounds, cultivars, and growth
    stages.
-   Similar visual symptoms across diseases and nutrient deficiencies.
-   Multiple diseases occurring on the same plant.
-   Class imbalance and limited examples of rare diseases.
-   High computational requirements for some models.
-   Insufficient field validation and cross-domain testing.
-   Limited interpretability and biological validation of some
    explanation methods.
-   Need for dedicated, field-validated jute disease datasets.

## Proposed Directions

-   Build larger, geographically diverse field-image datasets.
-   Use augmentation and class-balancing methods carefully.
-   Evaluate models on field images from locations or times not
    represented in training.
-   Explore lightweight architectures, pruning, quantization, and edge
    optimization.
-   Consider object detection or multi-label classification for multiple
    diseases.
-   Validate explainability outputs with agricultural experts.
-   Explore RGB and multispectral, hyperspectral, or thermal data where
    practical.
-   Develop accessible, multilingual, offline-capable farmer-facing
    interfaces.

## Repository Structure

The following is a suggested structure for extending this report into a
software project:

``` text
ai-based-crop-disease-detection/
├── README.md
├── docs/
│   └── project-report.pdf
├── data/
│   └── README.md
├── notebooks/
├── src/
│   ├── preprocessing/
│   ├── training/
│   └── prediction/
├── models/
├── results/
├── requirements.txt
└── .gitignore
```

Only add folders and files that are actually present in the repository.
Do not commit large datasets or model weights without checking their
licences and GitHub storage limits.

## Getting Started

This repository currently documents the project study and proposed
workflow. There are no verified installation or execution commands in
the report.

When implementation code is added:

1.  Document the supported Python version and dependencies.
2.  Explain how to obtain and prepare each dataset.
3.  Provide training and evaluation commands.
4.  Document how to run inference on a sample image.
5.  Report the model architecture, dataset split, metrics, and
    limitations.

## Academic Project Details

**Project title:** AI-Based Crop Disease Detection Using Deep Learning

**Project team:** - Dhali Trisha --- 24STUCHH010313 - Garmella Srinidhi
--- 24STUCHH010433 - Mohammed Akmaluddin --- 24STUCHH010759

**Project supervisor:** Dr. Sanivarapu Prasanth Vaidya, Senior Assistant
Professor

**Institution:** Faculty of Science & Technology, ICFAI Foundation for
Higher Education, Hyderabad

**Report date:** November 2026

## References

The academic report includes research on plant disease detection, CNNs,
transfer learning, crop-specific disease recognition, UAV remote
sensing, and explainable AI. Key references listed in the report
include:

1.  Mohanty, S. P., Hughes, D. P., & Salathé, M. (2016). *Using deep
    learning for image-based plant disease detection*. Frontiers in
    Plant Science, 7, 1419.
2.  Ferentinos, K. P. (2018). *Deep learning models for plant disease
    detection and diagnosis*. Computers and Electronics in Agriculture,
    145, 311--318.
3.  Tirkey, D., Singh, K. K., & Tripathi, S. (2023). *Performance
    analysis of AI-based solutions for crop disease identification,
    detection, and classification*. Smart Agricultural Technology, 5,
    100238.
4.  Dolatabadian, T. X., Danilevicz, M. F., & Upadhyaya, S. R. (2025).
    *Image-based crop disease detection using machine learning*. Plant
    Pathology, 74(1), 18--38.
5.  Pan, S. J., & Yang, Q. (2010). *A survey on transfer learning*. IEEE
    Transactions on Knowledge and Data Engineering, 22, 1345--1359.

See the project report for the full reference list.

## GitHub Repository

After creating a repository on GitHub, replace the placeholder below
with its actual URL:

`https://github.com/<your-username>/ai-based-crop-disease-detection`

------------------------------------------------------------------------

*This README is based on the academic project report. It distinguishes
the literature review and proposed methodology from software features or
experimental results that have not yet been documented.*
