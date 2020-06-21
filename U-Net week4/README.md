Training with MSE Loss:
------

    U Net small number try 1:     300 images  40+50E
  
    U Net small number try 2:     600 images  70E
  
    U Net 3000_30:                3000 images 30E
	
	U Net 3000_70:                3000 images 70E     --> w1
	
	w1_10000_30:                  10000 images, based on w1, 30E    --> w2
  
	w2_10000+augmentation_30:     10000 images, add augmentation, based on w2
  
	w2_2000+augmentation_100：    2000 images, add augmentation, based on w2 100E
	

Comparison of Loss Function:
------
	
	
Notebook|train|eval|Data Augmentation| Epoch|Threshold
--------|-----|-----|----------------|-------|---------|
Accuracy comparison of Loss Function_50E|1000|500|\checkmark|100|\times
Accuracy comparison of Loss Function_100E|1000|500|\checkmark|100|\times
Comparison of Dice and MSE with threshold|1000|500|\checkmark|100|\checkmark
	
------
	
	
Training with Dice Loss:
------

	DiceLoss_2000_100:        2000 images, add augmentation, 100E   --> w1 

	DiceLoss_4000_50:		  4000 images, add augmentation, 50E   
	
	
	
	
	
	
	
