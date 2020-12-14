# ALPR using trained OCR model on custom dataset

This repository performs the License Plate Recognition based on this [project](https://github.com/sergiomsilva/alpr-unconstrained). The only modification is the OCR Detection, which is trained on private dataset.

## Overview of ALPR Procedure

- #### Step 1: Detect vehicles
- #### Step 2: Detect license plates
- #### Step 3: OCR

## Requirements

In order to run the code, check if these [libraries](https://github.com/chenghanc/alpr-unconstrained/blob/alpr/version-alpr27) are installed. Darknet framework is self-contained in the `darknet` folder and must be compiled before running the code

- #### darknet (libdarknet.so)
    * Compiled with GPU=1, CUDNN=1, OPENCV=1, LIBSO=1
        - `cd darknet && make -j20`

## Download Models

Download all the trained models (see this repo [alpr-unconstrained](https://github.com/sergiomsilva/alpr-unconstrained))

## Step 1: Vehicle Detection

- #### Use trained Yolo model to perform vehicle detection (see this repo [alpr-unconstrained](https://github.com/sergiomsilva/alpr-unconstrained))

## Step 2: License Plate Detection

- #### Use LP detector trained by this repo [alpr-unconstrained](https://github.com/sergiomsilva/alpr-unconstrained)

## Step 3: OCR Detection

- #### Perform OCR Detection. The model is trained on custom dataset using [darknet](https://github.com/AlexeyAB/darknet)

## Running a simple test

```shellscript
$ bash run-lpr.sh -i samples/test-lpr -o /tmp/output -c /tmp/output/results.csv
```

## Example
![](output/HKPseudoo7700108_output.png)

![](output/HKPseudoo7700107_output.png)

![](output/HKPseudoo7700232_output.png)

![](output/HKPseudoo7700193_output.png)









