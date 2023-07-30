# Plastizyme Miner
Plastizyme Miner aims to identify potential plastic-degrading enzymes, with a focus on Polyethylene terephthalate (PET), by analyzing metagenomic data. The repository builds upon previous work by ProteinGAN [https://github.com/Biomatter-Designs/ProteinGAN] and ESM  [https://github.com/facebookresearch/esm], leveraging ProteinGAN to augment real PET-degrading enzyme datasets and utilizing the enriched dataset to train classifiers based on the ESM model.

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
Protein GAN is trained using real PETase sequences and is capable of generating PET sequences. You can access the Kaggle notebook for Protein GAN [https://www.kaggle.com/code/mohammadrezarezae/plastizyme-miner-protein-gan]

# Classifier Using ESM embeding 
The classification pipeline employs the ESM model to generate feature vectors, which are then used as input for training and testing SVM, KNN, and Random Forest classifiers. The dataset used for classification can be found on Kaggle, and the Kaggle notebook for the classification process is available.
Link to kaggle data set [https://www.kaggle.com/datasets/mohammadrezarezae/petase-and-non-petases-protein-sequences]
Link to Kaggle notebook [https://www.kaggle.com/code/mohammadrezarezae/classsification-with-esm-embeding]