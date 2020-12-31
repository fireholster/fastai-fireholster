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

- Setup (Windows not using WSL)
    -FastAI Locally (Windows not using WSL)
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
 
    - Now use it
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

    - Troubleshoot
        - on Windows, Image data loaders fails to process (https://github.com/fastai/fastbook/issues/85)
            Reason: Pytorch multiprocessing does not work on windows
            Resolution: When creating dataloaders, pass num_workers = 0

- Setup (Windows using WSL and Cuda support)
    - Install CUDA on wSL2
        - Uninstalled Ubuntu
        - Disabled WSL and VPC
        - Regisetr to Windows insider program
        - Windows Update
        - Powershell: wsl --install
        - restart 
        - Installed NVIDIA WSL Drivers https://docs.nvidia.com/cuda/wsl-user-guide/index.html
        - All Good then


    - Now setup FastAI on ubuntu
        - Install Anaconda wget https://repo.anaconda.com/archive/Anaconda3-2019.10-Linux-x86_64.sh
        - run the downloaded .sh bash <filename>
        - update conda -  conda udpate -n base -c defaults conda
        - Create a new fastai env: conda create --name fastai
        - switch to the new env: conda activate fastai
        - Install fastai: conda install -c pytorch -c fastai fastai

    - Checking GPU Usage : watch -n 1 nvidia.smi.exe

    - Removing Cuda
        - sudo apt-get purge nvidia*
        - sudo apt-get autoremove
        - sudo apt-get autoclean
        - sudo rm -rf /usr/local/cuda*

    - Remove Cuda Toolkit :  sudo apt-get --purge remove cuda-toolkit-11-0




    


