# Create instance:




# Set up anaconda:
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
sudo bash ~/miniconda.sh -b -p ~/miniconda
~/miniconda/bin/conda init bash
```

Close the terminal and open a new one.

Then,
```
wget https://developer.download.nvidia.com/compute/cuda/12.8.0/local_installers/cuda-repo-amzn2023-12-8-local-12.8.0_570.86.10-1.x86_64.rpm
sudo rpm -i cuda-repo-amzn2023-12-8-local-12.8.0_570.86.10-1.x86_64.rpm
sudo dnf clean all
sudo dnf -y install cuda-toolkit-12-8
echo "" >> ~/.bashrc
echo "export CUDA_HOME="/usr/local/cuda-12.8/"" >> ~/.bashrc
```

Add these things to your `~/.bashrc` file:
```
export SERVER_IP="127.0.0.1" # or your services' IP addr
alias py="python"
```

Also, sign into wandb.

# Create env (note: flash-attn takes forever to build):

```
tmux

conda create -n verl python=3.10
conda activate verl

pip install verl==0.6.0 --no-cache-dir
pip install vllm==0.8.3 --no-cache-dir
pip install flash-attn --no-build-isolation --no-cache-dir
pip install uvloop==0.21.0
pip install transformers==4.57.1
```


# Run:

```
git clone -b ishika https://github.com/agarwalishika/grpo_synthesis
```