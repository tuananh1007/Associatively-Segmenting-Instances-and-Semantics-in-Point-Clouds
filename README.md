# Associatively Segmenting Instances and Semantics in Point Clouds

[[arXiv]]()

## Overview

## Dependencies
*  [TensorFlow](https://www.tensorflow.org/)

## Data and Model
* Prepared HDF5 data for training is available[here]().

* Download 3D indoor parsing dataset (S3DIS Dataset) for testing and visualization. Version 1.2 of the dataset is used in this work.

``` bash
python collect_indoor3d_data.py
python gen_h5.py
cd data && python generate_input_list.py
cd ..
```

* (optional) Models can be downloaded from [here]().

## Usage

* Compile TF Operators
Refer to [PointNet++](https://github.com/charlesq34/pointnet2)

* Training
``` bash
cd models/ASIS/
ln -s ../../data .
sh +x train.sh 5
```

* Evaluation
``` bash
python eval_iou_accuracy.py
```

Note: We test on Area5 and train on the rest folds in default. 6 fold CV can be conducted in a similar way.

## Citation
If our work is useful for your research, please consider citing:

@article{asis,
  title={Associatively Segmenting Instances and Semantics in Point Clouds},
  author={Xinlong Wang, Shu Liu, Xiaoyong Shen, Chunhua Shen, Jiaya Jia},
  journal={arXiv preprint arXiv:},
  year={2018}
}

## Acknowledgemets
This code largely benefits from following repositories:
[PointNet++](https://github.com/charlesq34/pointnet2),
[SGPN](https://github.com/laughtervv/SGPN),
[DGCNN](https://github.com/WangYueFt/dgcnn) and
[DiscLoss-tf](https://github.com/hq-jiang/instance-segmentation-with-discriminative-loss-tensorflow) 



