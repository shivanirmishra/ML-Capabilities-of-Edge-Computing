 ## **RL-based industrial controller**
 
 ### **On Server (Working on CPU)**
 
 #### **Steps to run examples of reinforcement learning using docker:**

**Check containers**: `docker ps -a`

1) docker run --gpus all -it --rm -v /home/ravi:/shivani nvcr.io/nvidia/pytorch:21.09-py3

It will remove itself after exiting

2) **Path:** cd /workspace/examples/upstream/reinforcement_learning

3) cat README.md

Install and run files written in readme

`pip install -r requirements.txt`

For REINFORCE:

`python reinforce.py`

For actor critic:

`python actor_critic.py`


