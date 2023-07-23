### Conda environment

environment.yml contains all the dependencies required in order to run ProteinGAN. You can simply run:

`conda env create --file environment.yml`

```bash
export PYTHONPATH={path_to_repository}/src:{path_to_repository}/src/common:$PYTHONPATH
```

export PYTHONPATH=/home/mohre/D/Research/templates/ProteinGAN/src:/home/mohre/D/Research/templates/ProteinGAN/src/common:$PYTHONPATH


## Data for training