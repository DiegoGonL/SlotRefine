# SlotRefine: A Fast Non-Autoregressive Model for Joint Intent Detection and Slot Filling

## FORK FOR DEEP LEARNING SUBJECT FOR ROBOTICS AND INTELLIGENT SYSTEMS MASTER'S DEGREE AT ULE

## Reference
Main paper to be cited ([Di Wu et al., 2020](https://www.aclweb.org/anthology/2020.emnlp-main.152.pdf))

```
@article{wu2020slotrefine,
  title={Slotrefine: A fast non-autoregressive model for joint intent detection and slot filling},
  author={Wu, Di and Ding, Liang and Lu, Fan and Xie, Jian},
  booktitle={EMNLP},
  year={2020}
}
```

## Requirements
Our system is build upon the [THUMT](https://github.com/THUNLP-MT/THUMT) codebase.

tensorflow 1.12 <br>
python 3.6

## Setup
There's an environment.yml file in the root directory. You can use it to create a conda environment with all the dependencies.
Use the following command to create the environment:
```
conda env create -f environment.yml
```

## Usage
```
sh train.atis.sh
```
or
```
python main.py --patience=40 --dataset=atis --split=" " --max_epochs=200 --batch_size=128 --valid_data_path=test --lr=0.001 --alpha=0.5 --rm_nums=True --hidden_size=80 --filter_size=80 --num_heads=16 --encode_mode='UTF-8' --num_encoder_layers=2 --attention_dropout=0.05 --residual_dropout=0.1 --multiply_embedding_mode='none' --dump=True
```
