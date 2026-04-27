<div align="center">
<h2> HiDRA: Hierarchical Degradation Representation and Adaptation with Generative Priors for Enhancing Infrared Vision</h2>
Zihang Chen, Zhu Liu, Changbo Yan, Jinyuan Liu, Risheng Liu

</div>

---
### Updates

[2026-3-20] Our paper has been accepted by CVPR 2026, the inference and code is available..

---

### Preparation

For preparation, first, you should create a new environment:

```
conda create -n hidra python=3.10
conda activate hidra
pip install -r requirements.txt
```

Then download the base model [SD-turbo](https://huggingface.co/stabilityai/sd-turbo), the pretrained [weights](https://drive.google.com/drive/folders/12rkVbM3el62cArIVyRdhwRBiN4857TXt?usp=drive_link) and the [HM-TIR](https://github.com/Zihang-Chen/HM-TIR) dataset and put in the proper place.

### Training
Run the shell:
```
sh train.sh
```

### Inference and testing
Please change the paths of evaluate input and output in test.sh, then run:
```
sh test.sh
```
then, to get enhanced TIR images metrics, run the following command:
```
python src/evaluate_img.py --subfolders FPNC BSR --dataset your/enhanced/TIR/images --label_dir label/TIR/images --metrics lpips dists fid niqe maniqa
```

### Any Question

If you have any other questions about the code, please email to [Zihang Chen](mailto:chenzi_hang@mail.dlut.edu.cn).


## Acknowledgement
Our core codes are based on [S3Diff](https://github.com/ArcticHare105/S3Diff), thanks for their contributions.




