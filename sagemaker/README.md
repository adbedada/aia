# Yolo on Sagemaker

The Dockerfile is used to create a YOLO-ECR file that saves the `darknet` github repository and compile it.
    
* Save Yolo setting files in the `cfg` folder
        
        - your.data 
        - your.cfg
        - your.names 
 
* Your Dataset should be stored in the `data` folder in the following structure.
    
        data 
          |---> custom
                |---> object
                    |---> train
                            |--->images
                                |---> image_001.jpg
                                |---> image_002.jpg
                                ...
                            |--->labels
                                |---> label_001.txt
                                |---> label_002.txt
                                ...
                   |---> test
                   ...
                |----> train.txt
                |-----> test.txt
                
Inside the  `custom` folder, you should also save the `train.txt` and `test.txt` files
pointing to the image and label files inside the  `object` folder.
