# Image-Labelling
Steps to how to start labelling objects for TensorFlow

###### Step 1
Install [labelImg](https://github.com/heartexlabs/labelImg)

###### Step 2
Clone Repo and place it anywhere (not in labelImg Directory)

###### Step 3
Put all **`.jpg`** images in `images/`

###### Step 4
Follow Steps for [labelImg](https://github.com/heartexlabs/labelImg)

###### Step 5
open `/images` as dir

###### Step 6
change save dir to `/annotations`

**<-- Start labelling -->**

###### Step 7
Place the `.jpg` and `.xml` in `/images/test` and `/images/train`

###### Step 8
run: 
```
python3 xml_to_csv.py
```

###### Step 9
run: 
```
python3 generate_tfrecord.py --csv_input=data/test_labels.csv --output_path=data/test.record --image_dir=images/ --name={Exact Class Name}
```
###### Step 9
run: 
```
python3 generate_tfrecord.py --csv_input=data/train_labels.csv --output_path=data/train.record --image_dir=images/ --name={Exact Class Name}`
```
Class Names are case sensitive

> note: install any missing dependecies: i.g. `pip3 install tensorflow Pillow object_detection`
