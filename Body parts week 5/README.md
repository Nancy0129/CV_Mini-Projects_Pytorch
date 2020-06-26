UNet Training:
------


Notebook|Label|model|train|eval|Augmentation| Epoch|LR|Input|Output
--------|:----:|:----:|:-----:|:-----:|:----------------:|:-------:|:---------:|:-------:|:---------:|
body-parts 2000_50|20|big|2000|600|×|50|0.01|×|×|
body-parts 10000_30|20|big|10000|1000|×|30|0.001|×|w1|
body-parts 30000_8|20|big|30000|1000|×|8|0.001|w1|w2|
body-parts 30000_8_2|20|big|30000|1000|vflip + hflip + rotation|8|0.001|w2|w3|
small model 10000_40|20|small|10000|1000|×|40|0.001|×|s1|
small model 30000_20|20|small|30000|1000|×|20|0.001|s1|s2|
small model 30000_20_2|20|small|30000|1000|vflip + hflip + rotation|20|0.001|s2|s3|
less-label 10000_60|9|small|10000|1000|×|60|0.001|×|L1|
less-label 30000_20|9|small|30000|1000|vflip + hflip + rotation|20|0.001|L1|L2|

	The conv layer channles:
	In the "big" model: 64 --> 128 --> 256 --> 512 --> 1024 --> 512 --> 256 --> 128 --> 64
	In the "small" model: 32 --> 64 --> 128 --> 256 --> 512 --> 256 --> 128 --> 64 --> 32
	
	Input: the input weight 
	Output: the output weight
	(w1,w2,w3 for big model; s1,s2,s3 for small model)

ResNet + UNet:
-------


Notebook|Label|Transfered|train|eval|Augmentation| Epoch|LR|Input|Output
--------|:----:|:----:|:-----:|:-----:|:----------------:|:-------:|:---------:|:-------:|:---------:|
Res+UNet 10000_50|20|Flase|10000|1000|×|60|0.001|×|×|
	
	
	
	
	
