# Local VQGAN-CLIP

Largely based off of [NerdyRodent's code](https://github.com/nerdyrodent/VQGAN-CLIP), which is largely based on our own notebooks. They also have the start of a [Guided Diffusion](https://github.com/nerdyrodent/CLIP-Guided-Diffusion) repo.

## Quick Start

First install dependencies via `pip install -r requirements.txt`.

Next, download a vqgaan checkpoint with a command like:
```bash
mkdir checkpoints

curl -L -o checkpoints/vqgan_imagenet_f16_16384.yaml -C - 'https://heibox.uni-heidelberg.de/d/a7530b09fed84f80a887/files/?p=%2Fconfigs%2Fmodel.yaml&dl=1' #ImageNet 16384
curl -L -o checkpoints/vqgan_imagenet_f16_16384.ckpt -C - 'https://heibox.uni-heidelberg.de/d/a7530b09fed84f80a887/files/?p=%2Fckpts%2Flast.ckpt&dl=1' #ImageNet 16384
```

You are now ready to go! Try `python main.py -p "A painting of an apple in a fruit bowl"`.
