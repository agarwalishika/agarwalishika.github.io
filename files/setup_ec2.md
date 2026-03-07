# If you want an EBS

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
sudo mkdir /ebs_mount
sudo mount /dev/VOLUME_STR /ebs_mount
sudo chown -R $USER:$USER /ebs_mount
```

4. verify your results:
```
lsblk
```

# But you might not need one, so follow this instead:
## Set up anaconda:
```
sudo chown -R $USER:$USER /tmp
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
sudo bash ~/miniconda.sh -b -p /tmp/miniconda
/tmp/miniconda/bin/conda init bash
```

Create env:

```
tmux

conda create -n verl python=3.10
conda activate verl

pip install verl --no-cache-dir
pip install vllm --no-cache-dir
```

Run:

```
git clone -b ishika https://github.com/agarwalishika/grpo_synthesis
```