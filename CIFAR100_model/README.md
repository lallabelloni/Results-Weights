Using device: cuda:0\
Training set: 40000 immagini\
Validation set: 10000 immagini\
Test set: 10000 immagini\
Input : 32 , 3 @ 32 x 32\
------ Convolution 1 ------\
convolution 1 kernel : 5\
P :  0\
S :  1\
Output : 32 , 32 @ 28 x 28\
------ Pooling 1 ------\
pooling 1 kernel : 2\
S :  2\
Output : 32 , 32 @ 14 x 14\
------ Convolution 2 ------\
convolution 2 kernel : 5\
P :  0\
S :  1\
Output : 32 , 64 @ 10 x 10\
------ Pooling 2 ------\
poolung 2 kernel : 2\
S :  2\
Output : 32 , 64 @ 5 x 5\
------ Fully Connected Layers ------\
Input :  32 , 1600\
------ Layer 1 ------\
output :  32 , 2040\
------ Layer 2 ------\
output :  32 , 1024\
------ Output ------\
output :  32 , 20\

Model Architecture:\
==========================================================================================\
Layer (type:depth-idx)                   Output Shape              Param #\
==========================================================================================\
Sequential                               [32, 10]                  --\
├─Conv2d: 1-1                            [32, 32, 28, 28]          2,432\
├─ReLU: 1-2                              [32, 32, 28, 28]          --\
├─MaxPool2d: 1-3                         [32, 32, 14, 14]          --\
├─Dropout: 1-4                           [32, 32, 14, 14]          --\
├─Conv2d: 1-5                            [32, 64, 10, 10]          51,264\
├─ReLU: 1-6                              [32, 64, 10, 10]          --\
├─MaxPool2d: 1-7                         [32, 64, 5, 5]            --\
├─Dropout: 1-8                           [32, 64, 5, 5]            --\
├─Flatten: 1-9                           [32, 1600]                --\
├─Linear: 1-10                           [32, 2040]                3,266,040\
├─ReLU: 1-11                             [32, 2040]                --\
├─Linear: 1-12                           [32, 1024]                2,089,984\
├─ReLU: 1-13                             [32, 1024]                --\
├─Linear: 1-14                           [32, 10]                  10,250\
==========================================================================================\
Total params: 5,419,970\
Trainable params: 5,419,970\
Non-trainable params: 0\
Total mult-adds (Units.MEGABYTES): 396.78\
==========================================================================================\
Input size (MB): 0.39\
Forward/backward pass size (MB): 8.85\
Params size (MB): 21.68\
Estimated Total Size (MB): 30.92\
==========================================================================================\

Beginning of training...\
Epoch 1/10 - Training Loss: 2.5515 - Training Accuracy: 21.08% - Validation Loss: 2.3049 - Validation Accuracy: 28.40%\
Epoch 2/10 - Training Loss: 2.2806 - Training Accuracy: 29.55% - Validation Loss: 2.1686 - Validation Accuracy: 32.49%\
Epoch 3/10 - Training Loss: 2.1320 - Training Accuracy: 33.41% - Validation Loss: 2.0421 - Validation Accuracy: 37.06%\
Epoch 4/10 - Training Loss: 2.0203 - Training Accuracy: 37.23% - Validation Loss: 1.9442 - Validation Accuracy: 39.89%\
Epoch 5/10 - Training Loss: 1.9310 - Training Accuracy: 39.66% - Validation Loss: 1.8876 - Validation Accuracy: 42.22%\
Epoch 6/10 - Training Loss: 1.8499 - Training Accuracy: 41.99% - Validation Loss: 1.8323 - Validation Accuracy: 42.97%\
Epoch 7/10 - Training Loss: 1.7920 - Training Accuracy: 43.69% - Validation Loss: 1.7485 - Validation Accuracy: 45.68%\
Epoch 8/10 - Training Loss: 1.7388 - Training Accuracy: 45.23% - Validation Loss: 1.7350 - Validation Accuracy: 46.12%\
Epoch 9/10 - Training Loss: 1.6866 - Training Accuracy: 46.91% - Validation Loss: 1.7278 - Validation Accuracy: 46.67%\
Epoch 10/10 - Training Loss: 1.6319 - Training Accuracy: 48.58% - Validation Loss: 1.7215 - Validation Accuracy: 46.52%\

Training completed!\