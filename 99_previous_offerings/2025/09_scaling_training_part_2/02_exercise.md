# Multi-GPU Training!

For this you will need access to runpod machines, send your (public) SSH keys to me!

`ssh-keygen`

`cat ~/.ssh/id_ed25519.pub`

X(?) people per machine, one SSH key per group.

SSH into your machine and run `nvidia-smi` to confirm you have two GPUs.

Run `python -c "import torch; print(torch.__version__)"` and confirm you have `2.4.1+cu124` installed


### Exercise 1: Explore Data Parallel and Extending it to Fully Sharded Data Parallel (45 min)

We will start with [nanoGPT](https://github.com/karpathy/nanoGPT), you should have this cloned in your home repo already.

We've already downloaded tiny shakespeare for you and installed all dependencies. Open a new tmux session (`tmux new-session -s train`) and start a training run using

```python
python train.py config/train_shakespeare_char.py
```

Watch the loss go down. While this goes on, you can detach from the tmux screen (`ctrl + B` followed by `D`) and run `watch nvidia-smi` to see GPU usage. You should see we are only running a single GPU run right now. 

Now run a 2GPU data parallel run using:

```python
torchrun --standalone --nproc_per_node=2 train.py config/train_shakespeare_char.py
```

This will initially give an error, try to debug this and get a data parallel training running. Observe the MFU (model flop utilization, higher is more efficient) as compared to the single GPU run.

Play with batch size and/or model size to saturate GPU consumption. 

Now extend this implementation to fully sharded data parallel, refer to [PyTorch docs](https://docs.pytorch.org/tutorials/intermediate/FSDP_tutorial.html).


### Exercise 2: Make MLP of the GPT Tensor Parallel (45 min)

Replace the nn.Linear in GPT's MLP with ColumnParallelLinear or RowParallelLinear (any one is fine for now). Take inspiration from [fairscale's implementation](https://github.com/facebookresearch/fairscale/blob/main/fairscale/nn/model_parallel/layers.py ), and feel free to use helper functions
