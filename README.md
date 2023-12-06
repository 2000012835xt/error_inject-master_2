### Requirements

```
pip install torch==1.12.0+cu116 torchvision==0.13.0+cu116 torchaudio==0.12.0 --extra-index-url https://download.pytorch.org/whl/cu116
pip install numpy
pip install tqdm
```

### Run

The data root of CIFAR in ```./new_error_injection_gpu.py(500)``` needs to be modified
```
python new_error_injection_gpu.py
```

### Error Injection

The number of injected errors: ```./error_rate/vgg/error_count.csv```
The layers to be injected: ```./quant/vgg_error.py(177)```
The bit to be filpped: ```./quant/vgg_error.py(19)```
The Threshold for determining errors: ```./new_error_injection_gpu.py(677)```
