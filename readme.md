**Status:** Maintenance



# Spinning Up

### Installation

We currently support Ubuntu and macOS running Python 3.6

- [mujoco-py](https://github.com/openai/mujoco-py/tree/1.50.1.1): 1.50.1
- [gym](https://github.com/openai/gym): 0.15.7



#### Install mujoco-py

1. Obtain a 30-day free trial on the [MuJoCo website](https://www.roboti.us/license.html) or free license if you are a student. The license key will arrive in an email with your username and password.
2. Download the MuJoCo version 1.5 binaries for [Linux](https://www.roboti.us/download/mjpro150_linux.zip) or [OSX](https://www.roboti.us/download/mjpro150_osx.zip).
3. Unzip the downloaded `mjpro150` directory into `~/.mujoco/mjpro150`, and place your license key (the `mjkey.txt` file from your email) at `~/.mujoco/mjkey.txt`.
4. Change the env variable

```bash
# mujoco
export LD_LIBRARY_PATH="/disk2/lsy/.mujoco/mjpro150/bin:$LD_LIBRARY_PATH"
```

5. install mujico-py

```python
pip install 'mujoco-py<1.50.2,>=1.50.1'
```



#### Install gym

system packages

```bash
sudo apt-get update && sudo apt-get install -y libglu1-mesa-dev libgl1-mesa-dev libosmesa6-dev xvfb ffmpeg curl patchelf libglfw3 libglfw3-dev cmake zlib1g zlib1g-dev swig
```

gym package

``` bash
pip install 'gym[all]'
```



#### Install OpenMPI

For Linux:

``` bash
sudo apt-get update && sudo apt-get install -y libopenmpi-dev
```

For macOS:

``` bash
brew install openmpi
```



#### Install Stable Spinning Up

``` bash
git clone https://github.com/liushunyu/stable-spinningup.git
cd stable-spinningup
pip install -e .
```



### What's new

- 2020-08-26: Add simple MLP DQN implementation.
- 2020-08-24: Add tensorboard implementation for training and testing.



Spinning Up
----------------------------------

This is an educational resource produced by OpenAI that makes it easier to learn about deep reinforcement learning (deep RL).

For the unfamiliar: [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning) (RL) is a machine learning approach for teaching agents how to solve tasks by trial and error. Deep RL refers to the combination of RL with [deep learning](http://ufldl.stanford.edu/tutorial/).

This module contains a variety of helpful resources, including:

- a short [introduction](https://spinningup.openai.com/en/latest/spinningup/rl_intro.html) to RL terminology, kinds of algorithms, and basic theory,
- an [essay](https://spinningup.openai.com/en/latest/spinningup/spinningup.html) about how to grow into an RL research role,
- a [curated list](https://spinningup.openai.com/en/latest/spinningup/keypapers.html) of important papers organized by topic,
- a well-documented [code repo](https://github.com/openai/spinningup) of short, standalone implementations of key algorithms,
- and a few [exercises](https://spinningup.openai.com/en/latest/spinningup/exercises.html) to serve as warm-ups.

Get started at [spinningup.openai.com](https://spinningup.openai.com)!



Citing Spinning Up
------------------

If you reference or use Spinning Up in your research, please cite:

```
@article{SpinningUp2018,
    author = {Achiam, Joshua},
    title = {{Spinning Up in Deep Reinforcement Learning}},
    year = {2018}
}
```
