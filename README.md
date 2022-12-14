## HEXA: Human Demo Augmented Explorer and Achiever

<img src="https://github.com/karthik19967829/hexa-benchmark/blob/main/Figure5-1.png" width="1000">

<img src="https://russellmendonca.github.io/data/lexa-method.gif" width="600">


## Setup

Create the conda environment by running : 

```
conda env create -f environment.yml
```

Clone the [hexa-benchmark](https://github.com/karthik19967829/hexa-benchmark) repo, and modify the python path   
`export PYTHONPATH=<path to lexa-training>/lexa:<path to lexa-benchmark>`  

Export the following variables for rendering  
`export MUJOCO_RENDERER=egl; export MUJOCO_GL=egl`

**WARNING!** Make sure to use the right python and mujoco version. The robobin environment code is known to break with other versions. Other environments might or might not work.

## Training

First source the environment : `source activate lexa`

For training, run : 

```
export CUDA_VISIBLE_DEVICES=<gpu_id>  
python train.py --configs defaults lexa_temporal --task kitchen --logdir <log path>
```

To view the graphs and gifs during training, run `tensorboard --logdir <log path>`


## Acknowledgements
This code was developed on top of LEXA code base https://github.com/orybkin/lexa
This code was developed using [Dreamer V2](https://github.com/danijar/dreamerv2) and [Plan2Explore](https://github.com/ramanans1/plan2explore).
