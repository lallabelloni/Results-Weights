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
\
Beginning of training...\
Epoch 1/10 - Training Loss: 1.8727 - Training Accuracy: 41.95% - Validation Loss: 1.6204 - Validation Accuracy: 49.97%\
Epoch 2/10 - Training Loss: 1.7421 - Training Accuracy: 45.51% - Validation Loss: 1.6379 - Validation Accuracy: 48.77%\
Epoch 3/10 - Training Loss: 1.6867 - Training Accuracy: 47.23% - Validation Loss: 1.5789 - Validation Accuracy: 51.52%\
Epoch 4/10 - Training Loss: 1.6472 - Training Accuracy: 48.34% - Validation Loss: 1.6497 - Validation Accuracy: 48.68%\
Epoch 5/10 - Training Loss: 1.6015 - Training Accuracy: 49.96% - Validation Loss: 1.5870 - Validation Accuracy: 50.71%\
Epoch 6/10 - Training Loss: 1.5621 - Training Accuracy: 50.71% - Validation Loss: 1.5596 - Validation Accuracy: 51.09%\
Epoch 7/10 - Training Loss: 1.5277 - Training Accuracy: 51.73% - Validation Loss: 1.5682 - Validation Accuracy: 50.95%\
Epoch 8/10 - Training Loss: 1.4963 - Training Accuracy: 52.98% - Validation Loss: 1.5912 - Validation Accuracy: 51.33%\
Epoch 9/10 - Training Loss: 1.4563 - Training Accuracy: 54.26% - Validation Loss: 1.6132 - Validation Accuracy: 49.50%\
Epoch 10/10 - Training Loss: 1.4196 - Training Accuracy: 55.06% - Validation Loss: 1.5722 - Validation Accuracy: 51.42%\
\
Training completed!
