## Notes for Sean's folder

- **"Simple-Image-Extraction.ipynb"** will get you a 2d array, with the first dimension as the image, 
  second dimension as the label 1 as with mask, 0 as without mask.

- **"Image-Aug.ipynb"** will create a folder called **"AUG-Train"**, which contains augmented data.


Structure:

```AUG-Train
AUG-Train
├── Train-Mask
|   ├── mask0_0_1565.jpeg
|   └── mask0_0_2902.jpeg
└── Train-NoMask
    ├── nomask0_0_1155.jpeg
    ├── nomask0_0_2502.jpeg
    ├── nomask0_0_3896.jpeg
```

Other auxiliary files not on github:

```
test
├── with_mask
│   ├── 0-with-mask.jpg
│   ├── 1-with-mask.jpg
└── without_mask
    ├── 325.jpg
    ├── 326.jpg

```
## Swish activation function:

**How** **to use** **Swish** them in deep neural networks?

- **Tanh and sigmoid cause huge vanishing gradient problems**. Hence, they should not be used.
- **Start with ReLU in your network**. Activation layer is added after the weight layer (something like CNN, RNN, LSTM or linear dense layer) as discussed above in the article. If you think the model has stopped learning, then you can replace it with a LeakyReLU to avoid the Dying ReLU problem. However, the Leaky ReLU will increase the computation time a little bit.
- **If you also have Batch-Norm layers in your network, that is added before the activation function making the order CNN-Batch Norm-*Act***. Although the order of Batch-Norm and Activation function is a topic of debate and some say that the order doesn’t matter, I use the order mentioned above just to follow the original Batch-Norm paper.
- Activation functions work best in their default hyperparameters that are used in popular frameworks such as Tensorflow and Pytorch. However, one can fiddle with the negative slope in **LeakyReLU and set it to 0.02** to expedite learning.

