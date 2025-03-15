Using device: cuda:0
Training set: 40000 immagini
Validation set: 10000 immagini
Test set: 10000 immagini
Input : 32 , 3 @ 32 x 32
------ Convolution 1 ------
convolution 1 kernel : 5
P :  0
S :  1
Output : 32 , 6 @ 28 x 28
------ Pooling 1 ------
pooling 1 kernel : 2
S :  2
Output : 32 , 6 @ 14 x 14
------ Convolution 2 ------
convolution 2 kernel : 5
P :  0
S :  1
Output : 32 , 16 @ 10 x 10
------ Pooling 2 ------
pooling 2 kernel : 2
S :  2
Output : 32 , 16 @ 5 x 5
------ Fully Connected Layers ------
Input :  32 , 400
------ Layer 1 ------
output :  32 , 120
------ Layer 2 ------
output :  32 , 84
------ Output ------
output :  32 , 10

Model Architecture:
==========================================================================================
Layer (type:depth-idx)                   Output Shape              Param # 
==========================================================================================
Sequential                               [32, 10]                  --      
├─Conv2d: 1-1                            [32, 6, 28, 28]           456     
├─ReLU: 1-2                              [32, 6, 28, 28]           --      
├─MaxPool2d: 1-3                         [32, 6, 14, 14]           --      
├─Conv2d: 1-4                            [32, 16, 10, 10]          2,416   
├─ReLU: 1-5                              [32, 16, 10, 10]          --      
├─MaxPool2d: 1-6                         [32, 16, 5, 5]            --      
├─Flatten: 1-7                           [32, 400]                 --      
├─Linear: 1-8                            [32, 120]                 48,120  
├─ReLU: 1-9                              [32, 120]                 --      
├─Linear: 1-10                           [32, 84]                  10,164  
├─ReLU: 1-11                             [32, 84]                  --      
├─Linear: 1-12                           [32, 10]                  850     
==========================================================================================
Total params: 62,006
Trainable params: 62,006
Non-trainable params: 0
Total mult-adds (Units.MEGABYTES): 21.06
==========================================================================================
Input size (MB): 0.39
Forward/backward pass size (MB): 1.67
Params size (MB): 0.25
Estimated Total Size (MB): 2.31
==========================================================================================

Beginning of training...
Epoch 1/10 - Training Loss: 1.6243 - Training Accuracy: 40.36% - Validation Loss: 1.4119 - Validation Accuracy: 48.88%
Epoch 2/10 - Training Loss: 1.3416 - Training Accuracy: 51.59% - Validation Loss: 1.2978 - Validation Accuracy: 53.57%
Epoch 3/10 - Training Loss: 1.2210 - Training Accuracy: 56.17% - Validation Loss: 1.2286 - Validation Accuracy: 56.24%
Epoch 4/10 - Training Loss: 1.1384 - Training Accuracy: 59.26% - Validation Loss: 1.1727 - Validation Accuracy: 58.45%
Epoch 5/10 - Training Loss: 1.0684 - Training Accuracy: 61.82% - Validation Loss: 1.1221 - Validation Accuracy: 59.95%
Epoch 6/10 - Training Loss: 1.0084 - Training Accuracy: 64.08% - Validation Loss: 1.0833 - Validation Accuracy: 61.81%
Epoch 7/10 - Training Loss: 0.9638 - Training Accuracy: 65.59% - Validation Loss: 1.0821 - Validation Accuracy: 61.43%
Epoch 8/10 - Training Loss: 0.9220 - Training Accuracy: 67.23% - Validation Loss: 1.0952 - Validation Accuracy: 62.28%
Epoch 9/10 - Training Loss: 0.8837 - Training Accuracy: 68.28% - Validation Loss: 1.0894 - Validation Accuracy: 62.26%
Epoch 10/10 - Training Loss: 0.8461 - Training Accuracy: 70.01% - Validation Loss: 1.1050 - Validation Accuracy: 62.57%

Training completed!

Testing started!
Test Loss: 1.1119 - Test Accuracy: 62.70%

Testing completed!

![alt text](Figure_1.png)
