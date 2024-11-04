# CYSE492-AY24-Senior-Design

### Installation Guide

The following steps have been successful on MacOS Sonoma 14.6.

#### 1. Conda Environment Setup

1. install miniconda by following either one of the two tutorials:
   https://www.codecademy.com/article/setting-up-jupyter-notebook#heading-mac-anaconda

   https://docs.anaconda.com/miniconda/

2. Create a conda environment using terminal:

   ```shell
   # Create an environment
   conda create --name YOUR_ENV_NAME
   ```

   In my case, I created an env called 'speech-adv', so all the following commands use 'speech-adv' as the conda env name.

   ```sh
   conda create --name speech-adv
   ```

   Activate your environment:

   ```sh
   conda activate speech-adv
   ```

   

3. Install dependency packages inside your conda environment. Note that python 3.11 is the version that works for me. Upgrading to a higher python version raised a few incompatibility issues.

   ```
   conda install python=3.11 pytorch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 -c pytorch
   conda install 'ffmpeg<5'
   pip install numpy==1.24.1 matplotlib torchaudio tqdm scipy librosa
   ```

#### 2. Clone the github repo:

clone the 'ASRAdversarialAttacks' repo and put it under the same directory where you have the 'tutorial.ipynb' jupyter notebook.

```
git clone https://github.com/hammaad2002/ASRAdversarialAttacks.git
git clone https://github.com/hammaad2002/CRDNN_Model.git
```



#### 3. Run the jupyter Notebook, which contains two adversarial attacks:

1. FGSM Attack (not very successful)
2. BIM Attack (successful)

The jupyter notebook large reuses the instruction from the **Adversarial Attack on ASR Models** code. It can serve as a starting code for kicking off the project.



### Homework for you:

1. **Reproduce** the above steps to make sure each of you can run the jupyter code.
2. **Create a github repo** with each of you as contributors for developing your project. You can start by folking this repo.
3. Read, understand, and **present in detail** the methdology of two main Adversarial Attacks (need to explain the math part):
   1. (Fast Gradient Sign Method (FGSM) , first proposed in this paper: Goodfellow, Ian J. ["Explaining and harnessing adversarial examples." *arXiv preprint arXiv:1412.6572* (2014).](https://arxiv.org/pdf/1412.6572)  
   2. Basic Iterative Method (BIM), first proposed in this paper: Kurakin, Alexey, Ian J. Goodfellow, and Samy Bengio. ["Adversarial examples in the physical world." *Artificial intelligence safety and security*. Chapman and Hall/CRC, 2018. 99-112.](https://arxiv.org/pdf/1607.02533)
4. Play with the **Torchaudio** toolkit and get familar with the Speech-to-Text process. **Torchaudio** provides all kinds of pretrained models, datasets for automatic speech recognition application. Below is a beginner-tutorial FYI: https://pytorch.org/audio/master/tutorials/speech_recognition_pipeline_tutorial.html#sphx-glr-tutorials-speech-recognition-pipeline-tutorial-py

 
