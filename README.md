# fastai-fireholster
 
Stack

 fastai 
  - Sits on top of pytorch and provide higher level functions
  - 
 pytorch 
  - similar to tensor flow
  - recently has been seeing upward trend towards usage
 Python

 GPU Machine
  - nvidia
  - not needed for the course
  - Use COLAB or Paperspace
  
Use Forums for help
  - https://forums.fast.ai/c/part1-v4/46

Setup FastAI Locally
 - Install Anaconda
 - Intall Git
 - Install Python
 - Clone the fastai repo https://github.com/fastai/fastai.git
 - Go into fastai cloned folder
 - run 'conda env update' - will take a while to setup
 - run activate fastai
 - Install ipython extensions
    - pip install ipywidgets
    - jupyter nbextension enable --py widgetsnbextension --sys-prefix
- run jupyter notebook  
 
Now use it
- To run fastbook
    - Clone fastbook repo https://github.com/fastai/fastbook
    - open conda prompt
    - acitivate fastai
    - install fastbook dependencies 'conda install -c fastai fastbook'
    - run jupyter notebook
    - Start here
        - http://localhost:8891/notebooks/app_jupyter.ipynb - learn repl


- To see if fastai is using the GPU
    - Run
        import torch        
        torch.cuda.device(0)
        torch.cuda.device_count() (this will return the number of GPUs)
        torch.cuda.get_device_name(0) (this will return the GPU that will be used for running fastai)

Troubleshoot
- on Windows, Image data loaders fails to process (https://github.com/fastai/fastbook/issues/85)
    Reason: Pytorch multiprocessing does not work on windows
    Resolution: When creating dataloaders, pass num_workers = 0

- NVidia has announed CUDA for WSL2 - So if you want try it out (https://forums.fast.ai/t/platform-windows-10-using-wsl2-w-gpu/73521)
    - Download the CUDA Driver for your GPU - https://developer.nvidia.com/cuda/wsl/download
    - Install WSL
    - Install Ubuntu
    - Insatll CUDA on WSL
        - Navigate to https://developer.nvidia.com/cuda-downloads 82
        - Select Linux
        - X86_64
        - Ubuntu
        - 18.04
        - Deb local and follow the steps. I would list out the steps but am unsure if that is allowed as CUDA is also part of the NVIDIA developer program.
        It should be noted that even with CUDA installed, running nvidia-smi within Ubuntu will not yield any results. It says it cannot communicate with the driver. However, during training, the command can be run within PowerShell to get an instant look at the memory usage, but the “watch” command will not work.




    


