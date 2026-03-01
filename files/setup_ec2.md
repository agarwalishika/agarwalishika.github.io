Run:

```
sudo dnf install git

git clone -b ishika https://github.com/agarwalishika/grpo_synthesis/tree/master
```

set up anaconda:
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
bash ~/miniconda.sh -b -p $HOME/miniconda
~/miniconda/bin/conda init bash
```

create env:

```
conda create -n verl python=3.10
conda activate verl

pip install verl
```