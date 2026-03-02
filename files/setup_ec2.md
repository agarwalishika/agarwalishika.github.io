Make sure to make an instance with 30gb of EBS (i think).

[To mount EBS to this EC2 instance](https://docs.aws.amazon.com/ebs/latest/userguide/ebs-using-volumes.html):
1. run this and find the volume at the bottom that says "disk" with no MOUNTPOINT, and that the same size as the one you requested:
```
lsblk
```

2. make sure this outputs "data"
```
sudo file -s /dev/VOLUME_STR
```

3. create the file system and mount it locally
```
sudo mkfs -t xfs /dev/VOLUME_STR
sudo mkdir /data
sudo mount /dev/VOLUME_STR /data
```

4. verify your results:
```
lsblk
```


Run:

```
sudo dnf install tmux
sudo dnf install git

git clone -b ishika https://github.com/agarwalishika/grpo_synthesis
```

set up anaconda:
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
sudo bash ~/miniconda.sh -b -p /data/miniconda
/data/miniconda/bin/conda init bash
```

create env:

```
tmux

conda create -n verl python=3.10
conda activate verl

pip install verl --cache-dir /data/tmp
```