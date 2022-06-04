## Pre-requisites
The project was developed using python 3 with the following packages.
- Pytorch
- 

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
```
python test.py
```
or
```
python test.py --weights <model_weights> --input_dir <input_path> --result_dir <result_path>
```


<!--* train

    * ```python -m torch.distributed.launch --nproc_per_node=8 --master_port=4321 basicsr/train_rain.py -opt options/train/Rain13k/HINet.yml --launcher pytorch```
-->