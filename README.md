# Project Title: SAR Image Change Detection Using Mathematical Morphology and Enhanced K-Means Clustering
## 1. Project Overview
This project implements the core methodology from the article "SAR Image Change Detection Based on Mathematical Morphology and the K-Means Clustering Algorithm." The primary goal of this work is to detect changes in Synthetic Aperture Radar (SAR) images using a combination of mathematical morphology operations and the K-Means clustering algorithm. SAR images are crucial in remote sensing due to their ability to capture data regardless of weather or lighting conditions. In this repository, I have replicated the algorithm as described in the article and further enhanced the detection accuracy by refining certain steps in the process.

## 2. SAR Change Detection Methodology
The original method outlined in the paper utilizes a multi-step approach that combines mathematical morphology with K-Means clustering. The process begins by applying noise suppression techniques and then performing a morphological filtering step to reduce small, insignificant changes. Following this, a mean-ratio operator is used to highlight significant changes between two SAR images captured at different times. Finally, the K-Means algorithm is applied to group pixels into different clusters that represent changed and unchanged areas. This repository faithfully replicates these steps, ensuring accuracy in change detection while handling radar image complexities.

## 3. Enhancements to the Original Approach
One major improvement introduced in this project is the use of advanced denoising techniques. While the original article did not specify certain kernel sizes or parameters for morphological filtering, I experimented with different kernel sizes and utilized more advanced denoising algorithms such as Non-Local Means and TV Chambolle denoising. These modifications allowed me to achieve smoother edges and sharper boundaries between change and no-change areas, enhancing the clarity of the final result.

## 4. Implementation Details
The implementation is structured in Python, with dependencies including libraries like OpenCV, Scikit-learn, and NumPy. The algorithm was applied to several datasets mentioned in the original paper, including the Ottawa, Bern, and Yellow River datasets. In this repository, I provide scripts that reproduce the original results and also showcase the improvements achieved through advanced filtering and denoising. The key implementation stages include:

1- Preprocessing of SAR images.
2- Morphological filtering with optimized parameters.
3- Ratio calculation for identifying changes.
- K-Means clustering to classify pixels into change/no-change clusters.
## 5. Performance and Results
The accuracy improvements were validated using multiple SAR datasets. By applying enhanced denoising and optimized kernel sizes, the detection accuracy showed a noticeable improvement. For example, in the Ottawa dataset, the accuracy reached 97.02% with a kappa coefficient of 0.8871, surpassing the results from the original implementation. These results show that by refining the noise removal process and adjusting the clustering algorithm’s parameters, a more robust change detection can be achieved.

## 6. Comparison with the Base Results
In comparison with the base results provided in the article, the modifications introduced here led to improved overall accuracy across all datasets. Specifically, the Yellow River dataset showed significant enhancements due to the implementation of the bilateral and Gaussian filters. The original paper did not provide explicit details on filter sizes and some of the denoising methods used, but by addressing these gaps, I was able to produce more reliable results, as demonstrated in the comparisons included in the report.

## 7. How to Use
To run the implementation, clone the repository and install the necessary dependencies listed in requirements.txt. The main script is main.py, where you can specify the input SAR images. The results will include visual outputs of the detected changes and performance metrics such as accuracy and the kappa coefficient. Detailed instructions for running the code and reproducing the results are included in the instructions.md file.
