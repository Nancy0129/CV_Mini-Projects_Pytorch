Training:
------


Notebook|model|train|eval|Augmentation| Epoch|LR|Input|Output
--------|:----:|:-----:|:-----:|:----------------:|:-------:|:---------:|:-------:|:---------:|
body-parts 2000_50|big|2000|600|×|50|0.01|×|×|
body-parts 10000_30|big|10000|1000|×|30|0.001|×|w1|
body-parts 30000_8|big|30000|1000|×|8|0.001|w1|w2|
body-parts 30000_8_2|big|30000|1000|vflip + hflip + rotation|8|0.001|w2|w3|
small model 10000_40|small|10000|1000|×|40|0.001|×|s1|
small model 30000_20|small|30000|1000|×|20|0.001|s1|s2|
small model 30000_20_2|small|30000|1000|vflip + hflip + rotation|20|0.001|s2|s3|

	

	
	
	
	
	
	
	
