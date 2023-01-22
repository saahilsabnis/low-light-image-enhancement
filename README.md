# low-light-image-enhancement

## Introduction

This is an implementation of the Research paper - [Learning Enriched Features for Real Image Restoration and Enhancement](https://arxiv.org/abs/2003.06792)

The goal of this research was recovering high-quality image content from its low-light image which is a degraded version. Image
restoration has its various applications, such as in
photography, security, medical imaging, and remote sensing. In this example, we will see an implementation of the 
**MIRNet** model proposed by Zamir, Et al. for low-light image enhancement, which is a fully-convolutional architecture that
learns an enriched set of
features that combines contextual information from multiple scales, while
simultaneously preserving the high-resolution spatial details.

### References:

- [The Retinex Theory of Color Vision](http://www.cnbc.cmu.edu/~tai/cp_papers/E.Land_Retinex_Theory_ScientifcAmerican.pdf)
- [Two deterministic half-quadratic regularization algorithms for computed imaging](https://ieeexplore.ieee.org/document/413553)



## Model Architecture

Here are the main features of the MIRNet model:

- A feature extraction model that computes a complementary set of features across multiple
spatial scales, while maintaining the original high-resolution features to preserve
precise spatial details.
- A regularly repeated mechanism for information exchange, where the features across
multi-resolution branches are progressively fused together for improved representation
learning.
- A new approach to fuse multi-scale features using a selective kernel network
that dynamically combines variable receptive fields and faithfully preserves
the original feature information at each spatial resolution.
- A recursive residual design that progressively breaks down the input signal
in order to simplify the overall learning process, and allows the construction
of very deep networks.


![Architecture](https://user-images.githubusercontent.com/50745306/213896132-54ce3972-cb56-4b76-87a5-6501f204534b.png)



## Results

![Result1](https://user-images.githubusercontent.com/50745306/213896274-0bf77e3c-e94b-44d4-8ce5-d1671b179591.png)
![Result2](https://user-images.githubusercontent.com/50745306/213896275-2effbd53-43aa-4174-a80a-84a73ff79908.png)
![Result3](https://user-images.githubusercontent.com/50745306/213896276-35b392cd-51db-4c52-9fff-43d5f9bed8b3.png)