## Setup for running without a GPU:

+ install a pytorch version from the [install command generator here](https://pytorch.org/get-started/locally/), per your platform and selecting CPU and not CUDA! you can simply do that after install the pip requirements as usual.

+ download the project's actual model file (.pth) [from here](https://github.com/PeterL1n/RobustVideoMatting) or elsewhere. if you run with `--variant mobilenetv3` like below, download the mobilenet based model from there, e.g. `rvm_mobilenetv3.pth`.

## Running

example command:
```shell
python inference.py --variant mobilenetv3 --device cpu --input-source data/video/raw/1.avi --output-type video --checkpoint rvm_mobilenetv3.pth --output-composition output1.avi
```

## See also
https://github.com/PeterL1n/BackgroundMattingV2 ― although it requires a background picture, it may be more robust and economical in scenarios where
taking a background person-less picture is suitable.
