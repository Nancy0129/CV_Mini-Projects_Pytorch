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
less-label 30000_20_2|9|small|30000|1000|vflip + hflip + rotation|20|0.001|L2|L3|

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
Res+UNet 10000_50|20|Flase|10000|1000|×|50|0.001|×|×|
Res+UNet_transfer 10000_60|20|True|10000|1000|vflip + hflip + rotation|60|0.001|×|r1|
Res+UNet_transfer 30000_25|20|True|10000|1000|vflip + hflip + rotation|25|0.001|r1|×|
Res+UNet_transfer 30000_30|20|True|10000|1000|vflip + hflip + rotation|30|0.001|r1|×|


Result:
--------
### 20 Labels:

Notebook|tran_acc|eval_acc|
--------|:----:|:----:|
body-parts 2000_50|0.23012|0.10795|
body-parts 10000_30|0.43956|0.18441|
body-parts 30000_8|0.42371|0.25031|
body-parts 30000_8_2|0.24414|0.22734|
small model 10000_40|0.42562|0.18260|
small model 30000_20|0.46599|0.24742|
small model 30000_20_2|0.25066|0.22219|
Res+UNet 10000_50|0.50680|0.22591|
Res+UNet_transfer 10000_60|0.29760|0.23355|
Res+UNet_transfer 30000_25|0.29075|0.24272|
Res+UNet_transfer 30000_30|0.29737|0.24287|
------

### 9 Labels:
Notebook|tran_acc|eval_acc|
--------|:----:|:----:|
less-label 10000_60|0.69559|0.43761|
less-label 30000_20|0.44565|0.41765|
less-label 30000_20_2|0.47672|0.43902|

	
	
	
	
	
