# NoisyNet-DQN

I implement the [NoisyNet](https://arxiv.org/abs/1706.10295) for DQN-based RL algorithms. The code is evaluated on Atari2000, which is commonly used to benchmark the RL algorithms. Also, the tensorflow summary is added to better visualize the training process. 

Disclaimer: this code is highl based on [@openai/baselines](https://github.com/openai/baselines). Thanks for the great works!

## Usage

First, move the modified files to openai baselines (to support NoisyNet)
```
mv build_graph.py ./baselines/baselines/deepq/build_graph.py
mv tf_util.py ./baselines/baselines/common/tf_util.py
```

And add this line to your .bashrc (append to the PYTHONPATH)
```
export PYTHONPATH="PATH-TO-NoisyNet-DQN/baselines:$PYTHONPATH"
```

Train the agent and be patient
```python
# with NoisyNet-DQN
python train.py --env Breakout --no-double-q --noisy
# with vanilla DQN
python train.py --env Breakout --no-double-q
```

## Results


## Reference
- Noisy Networks for Exploration
- Human-level control through deep reinforcement learning
- Deep Reinforcement Learning with Double Q-learning
- Dueling Network Architectures for Deep Reinforcement Learning
