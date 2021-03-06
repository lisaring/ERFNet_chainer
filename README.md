# ERFNet_chainer
Implementation of ERFNet by chainer  
ERFNet: Efficient Residual Factorized ConvNet for
Real-time Semantic Segmentation [link](http://www.robesafe.uah.es/personal/eduardo.romera/pdfs/Romera17tits.pdf)
```
######## Training by cityscapes ########
# Calculate class balancing
python calculate_class_weight.py [mean or loss] --base_dir data_dir --result name --source ./pretrained_model/data.txt --num_classes 19 --dataset [cityscapes or camvid] --log_value 1.2
# Training encoder by cityscapes
python train.py experiments/enc_dec_paper.yml

######## Evaluate by cityscapes ########
python test.py experiments/test.yml

######## Visualize by cityscapes ########
python demo.py experiments/test.yml --img_path img.png
```

# Implementation
- Spatial Dropout using cupy
- Baseline, model architecture
- Evaluate by citydataset
- Calculate class weights for training model
- Poly leraning rate policy

# Requirement
- Python3
- Chainer3
- Cupy
- Chainercv
- OpenCV

# TODO
- Load pretrained model of resnet18 (if necessary)
