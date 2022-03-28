[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"

# Navigation for Banana Collector

### Introduction

This project contains code for a trained reinforcement learning agent that solves a modified version of the Banana Collector task of UnityML 

![Trained Agent][image1]

  

The environment consists of a space in which there are blue and yellow bananas. The goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.

The state space is an array of 37 elements. It contains the agent's velocity, along with ray-based perception of objects around agent's forward direction, among others. Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, **the agent must get an average score of +13 over 100 consecutive episodes**.



### Getting Started

#### Dependencies
1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
2. Install Openai gym using `pip install gym`.
3. Install box2d and box2d-py: `pip install box2d`; `pip install box2d-py`. 
4. Clone the repository below and navigate to the `python/` folder.
```bash
git clone https://github.com/udacity/Value-based-methods.git
cd Value-based-methods/python
```
5. Replace the `requirements.txt` file in the `Value-based-methods/python` folder with the one provided in this repository. The difference is that pytorch has been bumped up to version 1.0.0. from version 0.4.0 in the original `Value-based-methods/python`. Then, install several dependencies with 

```bash
pip install .
```

6. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment. 

```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

7. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

![Kernel][image2]

#### Run code

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the environment file in the `p1_navigation/` folder of the `Value-based-methods` folder that was cloned in the Dependencies section, and unzip (or decompress) the file.

3. Copy the `banana_agent.py`, `banana_model.py`, `checkpoint.pth`, `Navigation.ipynb` files provided in this repository into the `p1_navigation/` folder of the `Value-based-methods` folder that was cloned in the Dependencies section. 

4. Start a jupyter notebook in the `drlnd` environment created in the Dependencies section. Set the kernel to `drlnd` kernel created in the Dependencies section.

#### Instructions

Follow the instructions in `Navigation.ipynb` to get started with training your own agent or watch an existing agent provided  in the `checkpoint.pth` file perform the task!

