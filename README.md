# [Kaggle Wheat Detection](https://www.kaggle.com/c/global-wheat-detection)
***
[[Google Colab](https://colab.research.google.com/drive/14JpjbrJpN3-R_FkXg7sigJcWOAehEYFC?usp=sharing)]


![Wheat](https://github.com/Jimut123/kaggle-wheat-detection/blob/master/test_batch0_gt.jpg)
![Wheat](https://github.com/Jimut123/kaggle-wheat-detection/blob/master/test_batch0_pred.jpg)
![Wheat](https://github.com/Jimut123/kaggle-wheat-detection/blob/master/train_batch2.jpg)

```

              from  n    params  module                                  arguments                     
  0             -1  1      8800  models.common.Focus                     [3, 80, 3]                    
  1             -1  1    115520  models.common.Conv                      [80, 160, 3, 2]               
  2             -1  1    315680  models.common.BottleneckCSP             [160, 160, 4]                 
  3             -1  1    461440  models.common.Conv                      [160, 320, 3, 2]              
  4             -1  1   3311680  models.common.BottleneckCSP             [320, 320, 12]                
  5             -1  1   1844480  models.common.Conv                      [320, 640, 3, 2]              
  6             -1  1  13228160  models.common.BottleneckCSP             [640, 640, 12]                
  7             -1  1   7375360  models.common.Conv                      [640, 1280, 3, 2]             
  8             -1  1   4099840  models.common.SPP                       [1280, 1280, [5, 9, 13]]      
  9             -1  1  20087040  models.common.BottleneckCSP             [1280, 1280, 4, False]        
 10             -1  1    820480  models.common.Conv                      [1280, 640, 1, 1]             
 11             -1  1         0  torch.nn.modules.upsampling.Upsample    [None, 2, 'nearest']          
 12        [-1, 6]  1         0  models.common.Concat                    [1]                           
 13             -1  1   5435520  models.common.BottleneckCSP             [1280, 640, 4, False]         
 14             -1  1    205440  models.common.Conv                      [640, 320, 1, 1]              
 15             -1  1         0  torch.nn.modules.upsampling.Upsample    [None, 2, 'nearest']          
 16        [-1, 4]  1         0  models.common.Concat                    [1]                           
 17             -1  1   1360960  models.common.BottleneckCSP             [640, 320, 4, False]          
 18             -1  1      5778  torch.nn.modules.conv.Conv2d            [320, 18, 1, 1]               
 19             -2  1    922240  models.common.Conv                      [320, 320, 3, 2]              
 20       [-1, 14]  1         0  models.common.Concat                    [1]                           
 21             -1  1   5025920  models.common.BottleneckCSP             [640, 640, 4, False]          
 22             -1  1     11538  torch.nn.modules.conv.Conv2d            [640, 18, 1, 1]               
 23             -2  1   3687680  models.common.Conv                      [640, 640, 3, 2]              
 24       [-1, 10]  1         0  models.common.Concat                    [1]                           
 25             -1  1  20087040  models.common.BottleneckCSP             [1280, 1280, 4, False]        
 26             -1  1     23058  torch.nn.modules.conv.Conv2d            [1280, 18, 1, 1]              
 27   [-1, 22, 18]  1         0  models.yolo.Detect                      [1, [[116, 90, 156, 198, 373, 326], [30, 61, 62, 45, 59, 119], [10, 13, 16, 30, 33, 23]]]
Model Summary: 407 layers, 8.84337e+07 parameters, 8.84337e+07 gradients

Optimizer groups: 134 .bias, 142 conv.weight, 131 other
Reading image shapes: 100% 3241/3241 [00:00<00:00, 13426.34it/s]
Caching labels convertor/fold0/labels/train2017.npy (3241 found, 0 missing, 0 empty, 0 duplicate, for 3241 images): 100% 3241/3241 [00:00<00:00, 4624.23it/s]
Saving labels to convertor/fold0/labels/train2017.npy for faster future loading
Reading image shapes: 100% 1216/1216 [00:00<00:00, 14743.19it/s]
Caching labels convertor/fold0/labels/val2017 (1216 found, 0 missing, 0 empty, 0 duplicate, for 1216 images): 100% 1216/1216 [00:00<00:00, 4898.86it/s]
Saving labels to convertor/fold0/labels/val2017.npy for faster future loading

Analyzing anchors... Best Possible Recall (BPR) = 0.9991
Image sizes 1024 train, 1024 test
Using 2 dataloader workers
Starting training for 1 epochs...

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
       0/0     9.12G   0.08411    0.1946         0    0.2787        38      1024: 100% 1081/1081 [25:29<00:00,  1.41s/it]
               Class      Images     Targets           P           R      mAP@.5  mAP@.5:.95: 100% 406/406 [05:55<00:00,  1.14it/s]
                 all    1.22e+03    5.32e+04       0.187       0.748       0.474       0.142
Optimizer stripped from weights/last_yolov5x_fold0.pt
1 epochs completed in 0.524 hours.

```


## References
***
* https://www.kaggle.com/nvnnghia/yolov5-pseudo-labeling
* https://www.kaggle.com/orkatz2/yolov5-train
* https://www.kaggle.com/c/global-wheat-detection/
* https://www.kaggle.com/qiaoyuanfang/yolov5

***





