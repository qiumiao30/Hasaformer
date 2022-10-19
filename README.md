# Hasaformer
The implement of Hybrid Adaptive Self-Attention coupled with Differential Excitation for Time Series Anomaly Detection.

==========================================================
**The code will be released after the paper is received.**


# Introduction

None

# Model Overview

![model]()

# Geting Started
To clone this repo:
```bash
git clone https://github.com/qiumiao30/SLMR.git && cd Hasaformer
```

## 1. get data

- **SWaT & WaDI:** [Dataset Download](https://itrust.sutd.edu.sg/itrust-labs_datasets/), [Dataset Introduce](https://itrust.sutd.edu.sg/itrust-labs-home/itrust-labs_swat/)
- **PSM:** [Dataset Download and Introduction](https://github.com/eBay/RANSynCoders/tree/main/data)
- **SMD:** [Dataset Download and Introduction](https://github.com/NetManAIOps/OmniAnomaly)

## 2. Install Dependencies(Recomend Virtualenv)

- python>=3.7
- torch>=1.9

```python
pip install -r requirements.txt
```

## 3. dataset preprocess

```python
python data_preprocess.py --dataset $dataset_name$
```
`$dataset$` is one of SWAT, WaDI, SMD, PSM et al.

for example:

```python
python data_preprocess.py --dataset swat
```

## 4. Params

> - --dataset :  default "swat".
> - --lookback : Windows size, default 10.
> - --normalize : Whether to normalize, default True.
> - --epochs : default 10
> - --bs : Batch Size, default 256
> - --init_lr : init learning rate, default 1e-3
> - --val_split : val dataset, default 0.1
> - --dropout : 0.3

## 5. run

```python
python train.py --Params "value" --Parmas "value" ......
```

## 6. visualization 
![vis]()

