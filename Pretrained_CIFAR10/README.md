Using device: cuda:0
Training set: 40000 immagini
Validation set: 10000 immagini
Test set: 10000 immagini
Input : 32 , 3 @ 32 x 32
------ Convolution 1 ------
convolution 1 kernel : 5
P :  0
S :  1
Output : 32 , 32 @ 28 x 28
------ Pooling 1 ------
pooling 1 kernel : 2
S :  2
Output : 32 , 32 @ 14 x 14
------ Convolution 2 ------
convolution 2 kernel : 5
P :  0
S :  1
Output : 32 , 64 @ 10 x 10
------ Pooling 2 ------
pooling 2 kernel : 2
S :  2
Output : 32 , 64 @ 5 x 5
------ Fully Connected Layers ------
Input :  32 , 1600
------ Layer 1 ------
output :  32 , 2040
------ Layer 2 ------
output :  32 , 1024
------ Output ------
output :  32 , 10

Model Architecture:
==========================================================================================
Layer (type:depth-idx)                   Output Shape              Param #
==========================================================================================
Sequential                               [32, 10]                  --
├─Conv2d: 1-1                            [32, 32, 28, 28]          2,432
├─ReLU: 1-2                              [32, 32, 28, 28]          --
├─MaxPool2d: 1-3                         [32, 32, 14, 14]          --
├─Dropout: 1-4                           [32, 32, 14, 14]          --
├─Conv2d: 1-5                            [32, 64, 10, 10]          51,264
├─ReLU: 1-6                              [32, 64, 10, 10]          --
├─MaxPool2d: 1-7                         [32, 64, 5, 5]            --
├─Dropout: 1-8                           [32, 64, 5, 5]            --
├─Flatten: 1-9                           [32, 1600]                --
├─Linear: 1-10                           [32, 2040]                3,266,040
├─ReLU: 1-11                             [32, 2040]                --
├─Linear: 1-12                           [32, 1024]                2,089,984
├─ReLU: 1-13                             [32, 1024]                --
├─Linear: 1-14                           [32, 10]                  10,250
==========================================================================================
Total params: 5,419,970
Trainable params: 5,419,970
Non-trainable params: 0
Total mult-adds (Units.MEGABYTES): 396.78
==========================================================================================
Input size (MB): 0.39
Forward/backward pass size (MB): 8.85
Params size (MB): 21.68
Estimated Total Size (MB): 30.92
==========================================================================================

Beginning of training...
Epoch 1/10 - Training Loss: 1.5822 - Training Accuracy: 41.73% - Validation Loss: 1.3476 - Validation Accuracy: 51.46%
Epoch 2/10 - Training Loss: 1.2852 - Training Accuracy: 53.63% - Validation Loss: 1.1056 - Validation Accuracy: 61.31%
Epoch 3/10 - Training Loss: 1.1397 - Training Accuracy: 59.23% - Validation Loss: 1.0242 - Validation Accuracy: 64.09%
Epoch 4/10 - Training Loss: 1.0342 - Training Accuracy: 63.33% - Validation Loss: 0.9444 - Validation Accuracy: 67.34%
Epoch 5/10 - Training Loss: 0.9397 - Training Accuracy: 66.65% - Validation Loss: 0.8839 - Validation Accuracy: 69.19%
Epoch 6/10 - Training Loss: 0.8598 - Training Accuracy: 69.60% - Validation Loss: 0.8256 - Validation Accuracy: 71.15%
Epoch 7/10 - Training Loss: 0.7929 - Training Accuracy: 71.81% - Validation Loss: 0.8262 - Validation Accuracy: 71.63%
Epoch 8/10 - Training Loss: 0.7397 - Training Accuracy: 73.67% - Validation Loss: 0.7891 - Validation Accuracy: 72.43%
Epoch 9/10 - Training Loss: 0.6872 - Training Accuracy: 75.52% - Validation Loss: 0.7940 - Validation Accuracy: 72.19%
Epoch 10/10 - Training Loss: 0.6380 - Training Accuracy: 77.27% - Validation Loss: 0.7866 - Validation Accuracy: 73.46%

Training completed!

Testing started!
Test Loss: 0.7952 - Test Accuracy: 73.19%

Testing completed!