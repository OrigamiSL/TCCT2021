# TCCT2021
Convolutional Transformer Architectures Complementary to Time Series Forecasting Transformer Models

Paper: TCCT: Tightly-Coupled Convolutional Transformer on Time Series Forecasting
https://arxiv.org/abs/2108.12784

It has already been accepted by Neurocomputing:

Journal ref.: Neurocomputing, Volume 480, 1 April 2022, Pages 131-145

doi: 10.1016/j.neucom.2022.01.039

# Usage
Copy all files and paste them into Informer2020-main[1][2]. Cover all files if needed.

Three architectures are added:

  CSPAttention: A self-attention mechanism mirroring CSPNet belonging to CNN. It cuts down nearly 30% of memory occupation and 50% of time complexity of self-attention mechanism while achieving equivalent or superior forecasting accuracy. 
  
  Dilated Causal Convolution: It replaces canonical convolution to connect self-attention blocks. It helps Transformer model acquire exponentially receptive field growth with a little more negligible computation cost. Therefore, the learning capability of Transformer is strengthened.
  
  Passthrough Mechanism: It concatenates feature maps of different scales of self-attention blocks, thus getting more fine-grained information. Alike to feature pyramids commonly used in CNN and image processing, it expands feature maps leading to better forecasting performance of Transformer model.
  
LogSparse Attention[3][4] is added in models/attn.py

# Postscript
Note that TCCT architectures could also be applied to other time series forecasting Transformer or Transformer-like models. However, necessary transformations are needed.
# Reference
[1] Zhou, H., Zhang, S., Peng, J., Zhang, S., Li, J., Xiong, H., & Zhang, W. (2020). Informer: Beyond Efficient Transformer for Long Sequence Time-Series Forecasting. arXiv preprint arXiv:2012.07436.

[2] https://github.com/zhouhaoyi/Informer2020

[3] Li, S., Jin, X., Xuan, Y., Zhou, X., Chen, W., Wang, Y. X., & Yan, X. (2019). Enhancing the locality and breaking the memory bottleneck of transformer on time series forecasting. arXiv preprint arXiv:1907.00235.

[4] https://github.com/AIStream-Peelout/flow-forecast
