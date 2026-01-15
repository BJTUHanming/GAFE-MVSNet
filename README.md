# Geometry-aware feature enhancement for multi-view stereo
## ⚙ Setup
#### 1. Recommended environment
- PyTorch 1.13
- Python 3.10

#### 2. DTU Dataset

**Training Data**. We adopt the full resolution ground-truth depth provided in CasMVSNet or MVSNet. Download [DTU training data](https://drive.google.com/file/d/1eDjh-_bxKKnEuz5h-HXS7EDJn59clx6V/view) and [Depth raw](https://virutalbuy-public.oss-cn-hangzhou.aliyuncs.com/share/cascade-stereo/CasMVSNet/dtu_data/dtu_train_hr/Depths_raw.zip). 
Unzip them and put the `Depth_raw` to `dtu_training` folder. The structure is just like:
```
dtu_training                          
       ├── Cameras                
       ├── Depths   
       ├── Depths_raw
       └── Rectified
```
**Testing Data**. Download [DTU testing data](https://drive.google.com/file/d/135oKPefcPTsdtLRzoDAQtPpHuoIrpRI_/view) and unzip it. The structure is just like:
```
dtu_testing                          
       ├── Cameras                
       ├── scan1   
       ├── scan2
       ├── ...
```

#### 3. BlendedMVS Dataset

**Training Data** and **Validation Data**. Download [BlendedMVS](https://drive.google.com/file/d/1ilxls-VJNvJnB7IaFj7P0ehMPr7ikRCb/view) and 
unzip it. And we only adopt 
BlendedMVS for finetuning and not testing on it. The structure is just like:
```
blendedmvs                          
       ├── 5a0271884e62597cdee0d0eb                
       ├── 5a3ca9cb270f0e3f14d0eddb   
       ├── ...
       ├── training_list.txt
       ├── ...
```

#### 4. Tanks and Temples Dataset

**Testing Data**. Download [Tanks and Temples](https://drive.google.com/file/d/1YArOJaX9WVLJh4757uE8AEREYkgszrCo/view) and 
unzip it. Here, we adopt the camera parameters of short depth range version (Included in your download), therefore, you should 
replace the `cams` folder in `intermediate` folder with the short depth range version manually. The 
structure is just like:
```
tanksandtemples                          
       ├── advanced                 
       │   ├── Auditorium       
       │   ├── ...  
       └── intermediate
           ├── Family       
           ├── ...          
```

## ⚖ Citation
If you find our work useful in your research please consider citing our paper:
```
@article{han2025geometry,
  title={Geometry-aware feature enhancement for multi-view stereo},
  author={Han, Ming and Yin, Hui and Chong, Aixin and Huang, Hua},
  journal={Digital Signal Processing},
  pages={105667},
  year={2025},
  publisher={Elsevier}
}
```

## 👩‍ Acknowledgements
Thanks to [MVSNet](https://github.com/YoYo000/MVSNet), [CasMVSNet](https://github.com/alibaba/cascade-stereo/tree/master/CasMVSNet) and [ET-MVSNet](https://github.com/TQTQliu/ET-MVSNet).
