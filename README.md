### Requirements

```
pip install torch==1.12.0+cu116 torchvision==0.13.0+cu116 torchaudio==0.12.0 --extra-index-url https://download.pytorch.org/whl/cu116
pip install numpy
pip install tqdm
```

### Run

The data root of CIFAR in ```./new_error_injection_gpu.py(500)``` needs to be modified.

Run the following command:

```
python new_error_injection_gpu.py
```

### Error Injection

The number of injected errors: ```./error_rate/vgg/error_count.csv``` (set to 1)

The layers to be injected: ```./quant/vgg_error.py(177)``` (set to [0])

The bit to be filpped: ```./quant/vgg_error.py(19)```

The threshold for determining errors: ```./new_error_injection_gpu.py(677)```


### Results

The results are saved in ```./log/error_prop.csv```. Each column represents image index, error magnitude, injected element in feature_map, injected element in feature_map_err, # different elements in conv0, ..., conv15, respectively. 
