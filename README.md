# predict_quantum_acc
## Installation
Assume cuda-related packages have been installed.
```bash
$ git clone https://github.com/dtlics/torchquantum
$ cd torchquantum
$ pip install --editable .
```
## Usage
Please run
```bash
$ cd examples/quest
$ python train.py huge/default
```
as a simple example. and example output is as follows:
```bash
evalmode: False
dataset:
  name: huge.data
  split_ratio: [0.8, 0.1, 0.1]
model:
  name: simple
  use_only_global: False
  use_global_features: True
  use_gate_type: True
  use_qubit_index: True
  use_T1T2: True
  use_gate_error: True
  use_gate_index: True
  num_layers: 2
num_epochs: 100
batch_size: 1000
criterion:
  name: mse
optimizer:
  name: adam
  lr: 0.0005
  weight_decay: 0.0001
scheduler:
  name: constant
pdb: False
device: gpu
exp_name: huge/default
[2023-12-12 20:42:38.284] Model Size: 26417
Size of the data:  7000
[100 / 100],sqrtloss=0.02772982485849934         val_error:0.02812538752213184  

700
test_error:0.02791733444759953
best_val_error:0.02812538752213184
```
## DataSet
The data_set is stored in [Dataset Folder](examples/quest/data)

## Environment
The environment is as follows:
```bash
torch == 1.13.0
Torch-geometric == 2.2.0
Qiskit == 0.39.4
Python == 3.10.8
```
