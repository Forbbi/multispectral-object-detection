# EE798 Project

###Remember to do this 
Install : ``` # prompt: Torch version: 2.4.1+cu121
# Torchvision version: 0.19.1+cu121
# Torchaudio version: 2.4.1+cu121
# give me commnad to install this

```!pip install torch==2.4.1+cu121 torchvision==0.19.1+cu121 torchaudio==2.4.1+cu121 --extra-index-url https://download.pytorch.```


``` !pip uninstall wandb -y```


## Installation 
Python>=3.6.0 is required with all requirements.txt installed including PyTorch>=1.7 (The same as yolov5 https://github.com/ultralytics/yolov5 ).

#### Clone the repo
    git clone https://github.com/DocF/multispectral-object-detection](https://github.com/Forbbi/multispectral-object-detection.git
  
#### Install requirements
 ```bash
$ cd  multispectral-object-detection
$ pip install -r requirements.txt
```


## Run
#### Download the pretrained weights
yolov5 weights (pre-train) 

-[yolov5s] [google drive](https://drive.google.com/file/d/1UGAsaOvV7jVrk0RvFVYL6Vq0K7NQLD8H/view?usp=sharing)

-[yolov5m] [google drive](https://drive.google.com/file/d/1qB7L2vtlGppGjHp5xpXCKw14YHhbV4s1/view?usp=sharing)

-[yolov5l] [google drive](https://drive.google.com/file/d/12OFGLF73CqTgOCMJAycZ8lB4eW19D0nb/view?usp=sharing)

-[yolov5x] [google drive](https://drive.google.com/file/d/1e9xiQImx84KFQ_a7XXpn608I3rhRmKEn/view?usp=sharing)

###File structure 
Scrrenshot shared with you can see in github files

#### Change the model cfg
some example in models/transformer/

note!!!   we used xxxx_transfomerx3_dataset.yaml in our paper.

### Train Test and Detect
train: ``` !python train.py --weights yolov5l.pt --data /kaggle/working/multispectral-object-detection/data/multispectral/LLVIP.yaml --cfg /kaggle/working/multispectral-object-detection/models/transformer/yolov5l_fusion_transformer_llvip.yaml --epochs 100 --batch-size 8```

test: ```!python test.py --weights /kaggle/working/multispectral-object-detection/runs/train/exp/weights/best.pt --data /kaggle/working/multispectral-object-detection/data/multispectral/LLVIP.yaml  --batch-size 8```

#### References

https://github.com/ultralytics/yolov5

  
