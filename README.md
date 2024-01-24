# Lightweight Convolution Transformer
Paper Link: [Lightweight convolution transformer for cross-patient seizure detection in multi-channel EEG signals
](https://doi.org/10.1016/j.cmpb.2023.107856))

By [Salim Rukhsar<sup>[1]</sup><span>&#42;</span>](https://www.linkedin.com/in/salim-rukhsar-10845282/),
[Anil K. Tiwari<sup>[1]</sup><span>&#42;</span>](http://home.iitj.ac.in/~akt/),

In association with Image Processing and Computer Vision Lab @ Indian Institute of Technology jodhpur<sup>[1]</sup>.

This repo contain pytorch implementation of Lightweight convolution transformer for cross-patient seizure detection in multi-channel EEG signals as explained in the [Lightweight convolution transformer](https://doi.org/10.1016/j.cmpb.2023.107856) paper. This Transformer architecture is inspired from the compact convolution Transformer [here](https://arxiv.org/abs/2104.05704) and modified for processing the multichannel EEG signals.![](model.png)

## Usage:
```python

## Testing the LCT model    
data = torch.rand(5,1,256,23) # Generate a sample data with a sigle channel
embed_dim= 40
input_shape = data.shape
num_heads = 4

model = LCTModel(input_shape,
        embed_dim,
        num_heads,
        positional_emb=True,
        stochastic_depth_rate=0.1,
        dropout = 0.1,
        transformer_layers=2,
        num_classes=5)

out = model(data)
print(out.shape)
```

## Citation
```bibtex
@article{RUKHSAR2023107856,
title = {Lightweight convolution transformer for cross-patient seizure detection in multi-channel EEG signals},
journal = {Computer Methods and Programs in Biomedicine},
volume = {242},
pages = {107856},
year = {2023},
issn = {0169-2607},
doi = {https://doi.org/10.1016/j.cmpb.2023.107856},
url = {https://www.sciencedirect.com/science/article/pii/S0169260723005229},
author = {Salim Rukhsar and Anil Kumar Tiwari},
}
```
