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

pip install verl --no-cache-dir
pip install sentence-transformers
pip install vllm==0.12.0 --no-cache-dir
pip install flash-attn --no-build-isolation --no-cache-dir
```


# Run:

```
git clone -b ishika https://github.com/agarwalishika/grpo_synthesis
```

# some small changes in files to make:
1. in `/home/ec2-user/.conda/envs/verl/lib/python3.10/site-packages/verl/workers/rollout/vllm_rollout/vllm_async_server.py`, change line 198:

```
self.config.max_model_len = self.model_config.hf_config.max_position_embeddings
```

to: 
```
self.config.max_model_len = self.config.max_model_len
```


2. in `/home/ec2-user/.conda/envs/verl/lib/python3.10/site-packages/verl/experimental/agent_loop/agent_loop.py`, to line 515:

```
return await self._agent_loop_postprocess(output, **kwargs)
```

add the following line above it (kwargs):
```
kwargs.pop("output", None)
return await self._agent_loop_postprocess(output, **kwargs)
```

# To run GRPO
1. Run a reward function (as a service): run any of the files in `services/`
- examples for commands are in `run_services.sh`

2. Run `run_verl.sh`. It takes 4 arguments (examples are in `run_experiments.sh`):
- the model name
- the path of the reward function
- the job name
- the message you want to send to yourself to indicate it is done (see step 3 below)

[Optional] 3. If you'd like to attach a Slack webhook to send you a message when the training job is done, follow these instructions: https://www.svix.com/resources/guides/how-to-get-slack-webhook-url/
- Add your webhook link to the bottom of the `curl` command in `run_verl.sh`