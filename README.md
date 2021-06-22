# Facebook Research ParlAI conversational AI sentimental analysis using expert.ai
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)

### Demo Link
https://www.youtube.com/watch?v=YUS7YCJ9rgs


### Model saving for continous fine tuning


**What is ParlAI?**

ParlAI is a python-based platform for enabling dialog AI research.

Its goal is to provide researchers:

  * a unified framework for sharing, training and testing dialog models

  *  many popular datasets available all in one place, with the ability to multi-task over them

  * seamless integration of Amazon Mechanical Turk for data collection and human evaluation

  * integration with chat services like Facebook Messenger to connect agents with humans in a chat interface
link: https://github.com/facebookresearch/ParlAI

In ParlAI, we call an environment a world. In each world, there are agents. Examples of agents include models and datasets. Agents interact with each other by taking turns acting and observing acts.

To concretize this, we’ll consider the train loop used to train a Image Seq2Seq model trained on all DodecaDialogue tasks and fine-tuned on the Empathetic Dialogue task, We call this train environment a world, and it contains two agents - the seq2seq model and the dataset. The model and dataset agents interact with each other in this way: the dataset acts first and outputs a batch of train examples with the correct labels. The model observes this act to get the train examples, and then acts by doing a single train step on this batch (predicting labels and updating its parameters according to the loss). The dataset observes this act and outputs the next batch, and so on.


**Installation setup**

1. Install anaconda python. (https://anaconda.org/)
2. create a conda environment
``` 
conda create -n cortx pip python=3.7
```
3. activate the environment
``` 
conda activate cortx
```
4. Install the requirements
``` 
pip install -r requirements.txt
```





``` 

python application.py -mf zoo:blender/blender_90M/model -t blended_skill_talk

```
1. For each user there will be a unique id to seperate conversations. 
2. Each connection will include one world, one AI agent and multiple users.

## For dashboard
### Go to this link
https://github.com/kishorkuttan/dashboard
![alt text](https://github.com/kishorkuttan/Deep-Coversational-AI-Sentiment-Analysis-dashboard-/blob/master/Screenshot%20from%202021-06-23%2002-32-46.png)
![alt text](https://github.com/kishorkuttan/Deep-Coversational-AI-Sentiment-Analysis-dashboard-/blob/master/Screenshot%20from%202021-06-23%2002-33-02.png)



## Reference
1. https://github.com/facebookresearch/ParlAI
2. https://parl.ai/docs/zoo.html
3. https://arxiv.org/abs/1905.01969
4. https://parl.ai/projects/polyencoder/ 




