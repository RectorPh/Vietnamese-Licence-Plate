License-Plate-Recognition

* Identify the region containing the license plate using **Yolo Tiny v3**.
* Use a segmentation algorithm to separate each character on the license plate.
* Build a CNN model to classify the characters.
* Reformat the license plate to determine whether it consists of one or two lines.

## Install environments
```
pip install -r requirements.txt
```

## Quick start
You can clone this repo and run it immediately using the command below. Replace link_to_image with the path to the image you want to read.
```
python main.py --image_path=link_to_image 
```

## Results
This license plate recognition project can work on both single-line and double-line license plates. Even if the license plate is slightly obscured, it can still be read. :sunglasses:
<p align="center" >
<img src="https://images.viblo.asia/877154c3-929f-431c-a728-4a994acf6869.png" >
    Image 4: Result
</p>

However, there are still some disadvantages :worried::

* When the input image is tilted too much, some characters will be mistakenly identified as the wrong line. One solution is to use a transformer network to rotate the inclined image back to the straight image.
* Sometimes 8 and B, 0 and D are misidentified.
* Poor performance when the image is too blurry.