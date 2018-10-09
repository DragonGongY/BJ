# Surface inspection of continuous casting sheet billet use yolo v3

## Quick Start

1. Download weights from (链接: https://pan.baidu.com/s/1eBt4ejQ0X7IftPkZ454Dyw 提取码: jebf).
2. Run python yolo.py in command line and then add image

---

## Training

1. Generate your own annotation file and class names file.  
    One row for one image;  
    Row format: `image_file_path box1 box2 ... boxN`;  
    Box format: `x_min,y_min,x_max,y_max,class_id` (no space).  
    For VOC dataset, try `python voc_annotation.py`  
    Here is an example:
    ```
    path/to/img1.jpg 50,100,150,200,0 30,50,200,120,3
    path/to/img2.jpg 120,300,250,600,2
    ...
    ```

3. Modify train.py and start training.  
    `python train.py`  
    Use your trained weights or checkpoint weights in yolo.py.  
    Remember to modify class path or anchor path.

---

## Some issues to know

1. The test environment is
    - Python 3.5.2
    - Keras 2.1.5
    - tensorflow 1.6.0