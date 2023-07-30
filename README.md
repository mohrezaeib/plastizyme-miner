# Plastizyme Miner
Identify potential plastic degrading enzymes focusing on Polyethylene terephthalate (PET), by analysing metagenomic data.
This Repository is based on previous work by ProteinGAN [https://github.com/Biomatter-Designs/ProteinGAN] and ESM [https://github.com/facebookresearch/esm]
ProteinGAN is tailored to augment real PET-degrading enzyme datasets.
The Enriched dataset is utilized to train the classifiers based on the ESM model. 
## Paper abstract

## Licenses

All material is made available under Creative Commons BY-NC 4.0 license. You can use, redistribute, 
and adapt the material for **non-commercial** purposes, as long as you give appropriate credit by citing our paper 
and indicating any changes that you've made.

## System requirements
- Operating System: Linux.
- 64-bit Python 3.7 installation.
- blastp: 2.6.0+
- TensorFlow 1.13.1 or newer with GPU support.
- One or more NVIDIA GPUs. Recomendation: NVIDIA at least P100 GPU with 16GB.
- NVIDIA driver 418.87 or newer, CUDA toolkit 10.1 or newer, cuDNN 7.6.2 or newer.
Or you can use Kaggle virtual machine to run the script as notebook.


# Protein GAN
ProteinGan is trained with real PETase sequences, learns to generate PET sequences.
Link to Kaggle notebook [https://www.kaggle.com/code/mohammadrezarezae/plastizyme-miner-protein-gan]

# Classifier Using ESM embeding 
The classification piple line run using ESM model to embed feature vectors then SVM, KNN, and Random forest classifier use the embeding as input for training and test. 
Link to kaggle data set [https://www.kaggle.com/datasets/mohammadrezarezae/petase-and-non-petases-protein-sequences]
Link to Kaggle notebook [https://www.kaggle.com/code/mohammadrezarezae/classsification-with-esm-embeding]