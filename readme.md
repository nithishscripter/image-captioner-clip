# Image Captioner CLIP

## Description

**`CLIP with GPT Captioner`** is Image Captioning Model based on OpenAI's and GPT-2. The Model uses a Mapping module to "translate" CLIP embeddings ​​to GPT-2. The model is trained on the Flickr30k dataset, downloaded from Kaggle.

**The goal** Develop a tool that enhances accessibility for blind individuals by providing accurate and descriptive captions for digital images, enabling them to access and comprehend visual content independently.

The Model uses prefixes as in the [ClipCap](https://arxiv.org/abs/2111.09734) paper.

The Model was trained with a frozen CLIP, a fully trained Mapping Module (5-6x Transformer Encoder Layers) and with partially frozen GPT-2 (the first and last 14 layers were trained).

The training process was carried out using the [Kaggle](https://www.kaggle.com/) P100 GPU.

### Model Versions

> **Small** - [Download](https://drive.google.com/file/d/1pSQruQyg8KJq6VmzhMLFbT_VaHJMdlWF/view?usp=sharing)
>
> - Text Model - GPT-2 Small - 124M parameters
> - Mapping Module - 6x Transformer Encoder Layers
> - CLIP Base - Patch 32 model
> - 256M Parameters


## Usage

Create environment and install requirements:

```bash
python -m venv venv
# for windows
.\venv\Scripts\activate
# for linux/mac
source venv/bin/activate

pip install -r requirements.txt
```

And run prediction:

```bash
python .\src\predict.py -I <image_path> -S <model_size [S/L]> -C <checkpoint_name>
```

## Project By
```
Nithish
Sai Prassad
Prakash
Panjanathan
```