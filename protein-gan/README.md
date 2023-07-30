### Conda environment

* Install Miniconda3 Python 3.8 from official website 
https://docs.conda.io/en/latest/miniconda.html

* Create Enviroment 
environment.yml contains all the dependencies required in order to run ProteinGAN. You can simply run:`conda env create --file environment.yml`
Activate the new Enviroment 
```bash
conda activate tf1.14
```
* Add The project path 
```bash
export PYTHONPATH={path_to_protein_gan_repository}/src:{path_to_protein_gan_repository}/src/common:$PYTHONPATH
```

## Processing Data for training GAN
A dataset of known PETases has been collected.
We provide the raw taraining sequences as the fasta file in the directory `src/preprocessing/raw-data.fasta`.

Run the python notebook `src/preprocess.ipynb` to preprocess the raw data. The script takes care of  splitig data into train and validation as well as converting data to tfrecords which is then consumed by the model during training. 

## Training GAN
For training you can run train.ipynb script or run the command 
```bash
!conda run -n tf1.14 python -u -m generate --batch_size 8 --name test_run --steps 10 -shuffle_buffer_size 2 --loss_type non_saturating --discriminator_learning_rate 0.0001 --generator_learning_rate 0.0001 --dilation_rate 2 --n_seqs 1 --gf_dim 44 --df_dim 30 --dataset {PROTEIN_GAN_REPOSITORY_PATH}/src/preprocessing/data --nouse_cpu --architecture gumbel --pooling conv
```
## Generate Sequences using GAN
When traing is over the sequence could be generated using 
```bash 
!conda run -n tf1.14 python -u -m generate --batch_size 8 --name test_run --steps 10 -shuffle_buffer_size 2 --loss_type non_saturating --discriminator_learning_rate 0.0001 --generator_learning_rate 0.0001 --dilation_rate 2 --n_seqs 1 --gf_dim 44 --df_dim 30 --dataset {PROTEIN_GAN_REPOSITORY_PATH}/src/preprocessing/data --nouse_cpu --architecture gumbel --pooling conv
```
And print the generated Sequences using 

```bash
!cat {PROTEIN_GAN_REPOSITORY_PATH}/weights/sngan/*/*/*/*/*/*/*.fasta
```

You can also find a kaggle version of the training here 
plastizyme protein gan [https://www.kaggle.com/mohammadrezarezae/plastizyme-miner-protein-gan]