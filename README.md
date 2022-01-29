# mnst_cnn

Assignment for csce421 after lecture on convolutional neural networks.
Assignment was a contest between the class to see who could get highest accuracy on test dataset.
Model had a 100,000 parameter limit to make it fair for students that did not have powerful computers.
Forced students to rely more on techniques we learned in class rather than throwing more powerful hardware at the problem.

### My model
==========================================================================================
Layer (type:depth-idx)                   Output Shape              Param #
==========================================================================================
ImageClassifierNet                       --                        --
├─Sequential: 1-1                        [32, 32, 14, 14]          --
│    └─Conv2d: 2-1                       [32, 32, 28, 28]          832
│    └─Sigmoid: 2-2                      [32, 32, 28, 28]          --
│    └─MaxPool2d: 2-3                    [32, 32, 14, 14]          --
├─Sequential: 1-2                        [32, 64, 7, 7]            --
│    └─Conv2d: 2-4                       [32, 64, 14, 14]          51,264
│    └─Sigmoid: 2-5                      [32, 64, 14, 14]          --
│    └─MaxPool2d: 2-6                    [32, 64, 7, 7]            --
├─Dropout: 1-3                           [32, 3136]                --
├─Linear: 1-4                            [32, 10]                  31,370
==========================================================================================
Total params: 83,466
Trainable params: 83,466
Non-trainable params: 0
Total mult-adds (M): 343.40
==========================================================================================
Input size (MB): 0.10
Forward/backward pass size (MB): 9.64
Params size (MB): 0.33
Estimated Total Size (MB): 10.07
==========================================================================================

## Accuracy on public test dataset 
90.4%
## Accuracy on secret test dataset
90.5%