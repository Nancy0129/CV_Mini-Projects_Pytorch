# Caltech101

------May 29 20：03------

Tried 4 CNN models

(CNN2 always has the "cuda out of memory" probelm) 

Underfitting --> Overfitting

CNN4: training accuracy 0.92 eval accuracy 0.54

Setup_seed function seems not to work (results still random)

------May 30 18:20------

Trained model CNN4 twice

train accuracy: 0.90  eval accuracy: 0.63  

test accuracy: 0.608


------May 31 22：02------
Tried another 2 CNN models

Tried VGG structure (in CNN6)

Tried data augmentation (in CNN5)

Tried L2 regularization (in CNN 5,6)

Tried reducing learning rate when a metric has stopped improving (in CNN5,6)

The overfitting problem still exists and eval accuracy still low

------Jun 1 00：14------

Tried Transform learning ResNet 18

The best eval accuracy of that net is 0.923


