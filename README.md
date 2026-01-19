# DualT-Fusion
Multimodal data sources are becoming increasingly important across a wide range of scientific and real-world domains, including astrophysics, remote sensing, and healthcare, where complementary information is often captured by heterogeneous signals such as multivariate time series and images. Effectively integrating these modalities remains nontrivial due to differences in structure, scale, and information density, as well as limited labeled data. We propose DualT-Fusion, a unified transformer-based framework that jointly models temporal dynamics and visual patterns while enabling robust cross-modal alignment. The framework incorporates a Transformer encoder designed for multivariate time series, alongside a Vision Transformer for image data. To facilitate effective cross-modal interaction, we introduce a lightweight cross-attention fusion mechanism with a learnable temperature parameter that adaptively regulates the strength of cross-modal integration. In addition, DualT-Fusion employs a supervised contrastive objective to enforce class-consistent alignment between modality-specific embeddings while preserving modality-specific information. The resulting fused representation is used for downstream classification via a simple linear head, with the overall objective automatically balancing supervised classification and contrastive alignment. Experiments on multimodal solar flare benchmark dataset demonstrate that DualT-Fusion shows effectiveness for learning coherent representations from heterogeneous scientific data.

# Includes main framework module and dataset creation scripts

* <code> DATA\SWAN-SF </code> for preprocessed SWAN-SF data points, in case of training all components from scratch, the folders to keep data files must be placed under here (names and paths can be specified while running the relevant notebook cells). The original dataset has to be located in <code> DATA\SWAN-SF </code> and multimodal dataset will be created under <code> DATA\SWAN-SF_IMG </code>
  
* <code> SRC/MULTIMODAL </code> The details for each notebook file are as follows:
  - <code>H01_VOLX_dataset_creation.ipynb</code>: This module is to create the multimodal time series-image dataset in a single notebook file.
  - <code>H02_VXframework_vXDoubleT.ipynb</code>: This module contains the framework components.
    
# Execution Details 
* To view our modules, experiments, and results in a single file, given modules are sufficient.
* Since SWAN-SF is a large dataset, we do not include the preprocessed dataset in DATA\Preprocessed-SWANSF-main, if you need to train the components and start the experiments from scratch, don't hesitate to contact us!
* Original SWAN-SF data comes from: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EBCFKM, we use the preprocessed version as discussed in our paper.
* All experiments are done with python 3.9.13, pytorch 2.1.0, numpy 1.25.2

