# ALPR using trained OCR model on custom dataset

This repository contains the author's trained OCR model on custom dataset

## Overview

- #### Step 1: Detect vehicles
- #### Step 2: Detect license plates
- #### Step 3: OCR

## Requirements

In order to run the code, check if these [libraries](https://github.com/chenghanc/alpr-unconstrained/blob/alpr/version-alpr27) are installed. Darknet framework is self-contained in the `darknet` folder and must be compiled before running the code

```shellscript
$ cd darknet && make
```

## Download Models

Download all the trained models (see this repo [alpr-unconstrained](https://github.com/sergiomsilva/alpr-unconstrained))

## Vehicle Detection

- #### Use trained Yolo model to perform vehicle detection (see this repo [alpr-unconstrained](https://github.com/sergiomsilva/alpr-unconstrained))

## License Plate Detection

- #### Use LP detector trained by this repo [alpr-unconstrained](https://github.com/sergiomsilva/alpr-unconstrained)

## OCR Detection

- #### Perform OCR Detection. The model is trained on custom dataset using [darknet](https://github.com/AlexeyAB/darknet)

## Running a simple test

```shellscript
$ bash run-lpr.sh -i samples/test-lpr -o /tmp/output -c /tmp/output/results.csv
```

## Example
![](output/HKPseudoo7700108.jpg)

