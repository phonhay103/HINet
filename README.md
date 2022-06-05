## Pre-requisites
The project was developed using python 3 with the following packages.
- Pytorch
- Opencv
- Lmdb
- SciPy
- PyYAML
- Scikit-image

1. Install [Pytorch](https://pytorch.org/get-started/locally/)
2. Install with pip:
```bash
pip install -r requirements.txt
```

## Datasets
- Rain 13k - Test: [Here](https://drive.google.com/drive/folders/1PDWggNh8ylevFmrjo-JEvlmqsDlWWvZs)
- Place it in `datasets`

## Pre-trained Models
- Download the pre-trained [model](https://drive.google.com/file/d/1AVedAkb1B2F2b3XGWlMFFVSsNfQlCwxa/view?usp=sharing)
- Place it in `pretrained`

## Evaluation
- Option: `options/test.yml`
+ For Single Image Dataset:
```
datasets:
    test:
        type: SingleImageDataset
        dataroot_lq: <img_path>
    path:
        pretrain_network_g: <model_path>

```

+ For Pair Image Dataset:
```
datasets:
    test:
        type: PairedImageDataset
        dataroot_gt <input_path>
        dataroot_lq: <target_path>
    path:
        pretrain_network_g: <model_path>

```

- Run: `python test.py -opt options/test.yml`