### Conda environment

* Install Miniconda3 Python 3.8 from official website 
https://docs.conda.io/en/latest/miniconda.html

* Create Enviroment 
environment.yml contains all the dependencies required in order to run ProteinGAN. You can simply run:`conda env create --file environment.yml`
* Add The project path 

```bash
export PYTHONPATH={path_to_repository}/src:{path_to_repository}/src/common:$PYTHONPATH
```

## Processing Data for training
A dataset of known PETases has been collected.
We provide the raw taraining sequences as the fasta file in the directory `src/preprocessing/raw-data.fasta`.

Run the python notebook `src/preprocess.ipynb` to preprocess the raw data. The script takes care of  splitig data into train and validation as well as converting data to tfrecords which is then consumed by the model during training. 

## Training

