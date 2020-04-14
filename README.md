# DR Loss
PyTorch Implementation for our CVPR'20 paper: "DR Loss: Improving Object Detection by Distributional Ranking"


## Requirements
* Python 3.7
* PyTorch 1.1
* [maskrcnn-benchmark](https://github.com/facebookresearch/maskrcnn-benchmark)

## Usage:

1. Put the loss file to the codebase of maskrcnn_benchmark at
```
maskrcnn-benchmark/maskrcnn_benchmark/layers/sigmoid_dr_loss.py
```
and add the class into "init.py".

2. Change the focal loss in RetinaNet to the dr loss at
```
maskrcnn-benchmark/maskrcnn_benchmark/modeling/rpn/retinanet/loss.py
```

3. Run RetinaNet with the configurations in "configs/dr_retina".

## Models:

model | lr sched| multi-scale training | mAP(minival) | mAP (test-dev) | link
-- | -- | -- | -- | -- | -- 
Dr_Retina_R-50-FPN | 1x | No | 37.4 | 37.6 | [Google Drive](https://drive.google.com/file/d/1bLNfqlQ3zpAKUihbZY-NKPe0pYAReUGy/view?usp=sharing)
Dr_Retina_R-101-FPN | 2x | Yes | 41.5 | 41.7 | [Google Drive](https://drive.google.com/file/d/1hMg_-epThR32DQtzCzpdhDTiriob9ir9/view?usp=sharing)

    
## Citation
If you use the package in your research, please cite our paper:
```
@inproceedings{qian2020dr,
  author    = {Qi Qian and
               Lei Chen and
               Hao Li and
               Rong Jin},
  title     = {DR Loss: Improving Object Detection by Distributional Ranking},
  booktitle = {{IEEE} Conference on Computer Vision and Pattern Recognition, {CVPR} 2020},
  year      = {2020}
}
```
