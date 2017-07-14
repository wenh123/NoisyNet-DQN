# NoisyNet-DQN

I implement the [NoisyNet](https://arxiv.org/abs/1706.10295) for DQN-based RL algorithms. The code is evaluated on Atari2000, which is commonly used to benchmark the RL algorithms. Also, the tensorflow summary is added to better visualize the training process. More about my notes for NoisyNet can be found at [@andrewliao11/Deep-Reinforcement-Learning-Survey](andrewliao11/Deep-Reinforcement-Learning-Survey)

Disclaimer: this code is highl based on [@openai/baselines](https://github.com/openai/baselines). Thanks for the great works!

## Usage

First, move the modified files to openai baselines (to support NoisyNet)
```bash
git clone --recursive https://github.com/andrewliao11/NoisyNet-DQN.git
cd NoisyNet-DQN
mv build_graph.py ./baselines/baselines/deepq/build_graph.py
mv tf_util.py ./baselines/baselines/common/tf_util.py
```

And add this line to your .bashrc (append to the PYTHONPATH)
```bash
export PYTHONPATH="PATH-TO-NoisyNet-DQN/baselines:$PYTHONPATH"
```

Train the agent and be patient
```bash
# with NoisyNet-DQN
python train.py --env Breakout --no-double-q --noisy
# with vanilla DQN
python train.py --env Breakout --no-double-q
```

## Results

**orange: NoisyNet-DQN; blue: DQN**

Experiment on Breakout-NoFrameskip-v4:
![](figures/breakout.png)

Other experiment results will be added soon :fire:

The corresponding event files can be found at [drive]()

## Reference
- Noisy Networks for Exploration
- Human-level control through deep reinforcement learning
- Deep Reinforcement Learning with Double Q-learning
- Dueling Network Architectures for Deep Reinforcement Learning
