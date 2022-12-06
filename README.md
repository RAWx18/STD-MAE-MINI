

## 💿 Dependencies

### OS

We recommend using BasicTS on Linux systems (*e.g.* Ubuntu and CentOS). 
Other systems (*e.g.*, Windows and macOS) have not been tested.

### Python

Python >= 3.6 (recommended >= 3.9).

[Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/) are recommended to create a virtual python environment.

### Other Dependencies

```bash
pip install -r requirements.txt
```

### Warning

BasicTS is built on PyTorch 1.9.1 or 1.10.0, while other versions have not been tested.


## Getting started

### Preparing Data


- **Pre-process Data**

you can pre-process all datasets by.

    
    cd /path/to/your/project
    bash scripts/data_preparation/all.sh
    

or  pre-process one dataset by

    
    cd /path/to/your/project
    python scripts/data_preparation/${DATASET_NAME}/generate_training_data.py
    
    
Replace `${DATASET_NAME}` with one of  `PEMS03`, `PEMS04`, `PEMS07`, `PEMS08`, or any other supported dataset. The processed data will be placed in `datasets/${DATASET_NAME}`.


### Model definition

GWN model is in the directory
```
basicts\archs\arch_zoo\gwnet_arch\
```

### Run GWN

```
python examples/run.py -c examples/GWNet/GWNet_PEMS03.py --gpus '0'
python examples/run.py -c examples/GWNet/GWNet_PEMS04.py --gpus '0'
python examples/run.py -c examples/GWNet/GWNet_PEMS07.py --gpus '0'
python examples/run.py -c examples/GWNet/GWNet_PEMS08.py --gpus '0'

```

### Results

```
See the directory \checkpoints\GWNet200 to see all results
```

## 📉  Results table

![Main results.](results/results.png)


