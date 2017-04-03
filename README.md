# README

## Usage

1. copy `extract_features_txt.cpp` to `caffe_root/tools/`
2. cd `caffe_root`
3. `make all -j`
4. create a `.sh` file contains

## .sh file usage
```
extract_features_txt pretrained_net_param feature_extraction_proto_file
       extract_feature_blob_name1[,name2,...]
       save_feature_txt_name1[,name2,...]
       num_mini_batches
       [CPU/GPU] [DEVICE_ID=0]
```

## example
```
./build/tools/extract_features_txt.bin models/bvlc_reference_caffenet/bvlc_reference_caffenet.caffemodel examples/_temp/imagenet_val.prototxt pool5,fc7 examples/_temp/features/pool5.txt,examples/_temp/features/fc7.txt 1000 CPU
```

```
./build/tools/extract_features_txt.bin models/bvlc_reference_caffenet/bvlc_reference_caffenet.caffemodel examples/_temp/imagenet_val.prototxt pool5,fc7 examples/_temp/features/pool5.txt,examples/_temp/features/fc7.txt 1000 GPU 0
```
