# mnist_cnn

Assignment for csce421 after lecture on convolutional neural networks.
Assignment was a contest between the class to see who could get highest accuracy on test dataset.
Model had a 100,000 parameter limit to make it fair for students that did not have powerful computers.
Forced students to rely more on techniques we learned in class rather than throwing more powerful hardware at the problem.

### My model
-------------------------------------------------------------------------
Layer | Output Shape | Param #
-------------------------------------------------------------------------
- ImageClassifierNet
  - Sequential | [32, 32, 14, 14] | 0
    - Conv2d | [32, 32, 28, 28] | 832
    - Sigmoid | [32, 32, 28, 28] | 0
    - MaxPool2d | [32, 32, 14, 14] | 0 
  - Sequential | [32, 64, 7, 7] | 0
    - Conv2d | [32, 64, 14, 14] | 51,264
    - Sigmoid | [32, 64, 14, 14] | 0
    - MaxPool2d | [32, 64, 7, 7] | 0
  - Dropout | [32, 3136] | 0
  - Linear | [32, 10] | 31,370
-------------------------------------------------------------------------
- Total params: 83,466
- Trainable params: 83,466
- Non-trainable params: 0
- Total mult-adds (M): 343.40
-------------------------------------------------------------------------
- Input size (MB): 0.10
- Forward/backward pass size (MB): 9.64
- Params size (MB): 0.33
- Estimated Total Size (MB): 10.07
-------------------------------------------------------------------------

## Accuracy on public test dataset 
90.4%
## Accuracy on secret test dataset
90.5%
