# Using simulated EEGs to train RNN and analyze real data
## The influence of potassium reversal potential on seizure

From synthetic data, we train a vanilla Recurrent Neural Network (RNN) to model the sequence of an electroencephalogram (EEG). We generated the training samples from the open-source simulation package of biological neural networks [NetPyNE](http://www.netpyne.org/index.html). Using NetPyNE, we modified some parameters at the cellular level of the brain. The K+ concentration in the extracellular space is one of the best described examples in seizures ion dinamics. 

![image](https://user-images.githubusercontent.com/34287081/213928200-de794f81-f84c-492d-aeb1-9ea206bfd1ed.png)

We generated simulations that were 23 seconds long with an internal integration timestep of 0.01. Data is sampled with a step size of 5 every millisecond totaling 260 simulations. Data were divided by 50% seizure and 50% non-seizure. Finally, we divide the simulation vector per second, totaling 5980 where we use 80% to train and 20% to test the model. This is a plotted example of the signals.
![image](https://user-images.githubusercontent.com/34287081/213928258-57801846-3593-49b3-8958-1954d0a620a4.png)

The [dataset](https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition) for model evaluation consists of 5 different folders, each with 100 files, with each file representing a single subject/person. Each file is a recording of brain activity for 23.6 seconds. The corresponding time-series is sampled into 4097 data points. Each data point is the value of the EEG recording at a different point in time. So we have total 500 individuals with each has 4097 data points for 23.5 seconds. This is a plotted example of the signals.

![image](https://user-images.githubusercontent.com/34287081/213930467-02740cee-107d-40ef-bbcb-0ed6f071ada4.png)

## Laconeu 2023

Project developed during the Latin American Summer School in Computational Neuroscience 2023.

<img src="https://user-images.githubusercontent.com/34287081/213933757-3de46318-cd90-417b-8b10-274b8d78e248.png" width="100" height="100" title="AC3E"><img src="https://user-images.githubusercontent.com/34287081/213934159-1c039b12-be04-491e-9270-f843c7ac6914.png" width="100" height="100" title="CINV">
<img src="https://user-images.githubusercontent.com/34287081/213934068-cb15825f-12dd-47fb-81da-6501a3272857.png" width="100" height="100" title="ICTP">
<img src="https://user-images.githubusercontent.com/34287081/213934198-5327509d-d377-4b4a-9212-8cc2e9537ed9.png" width="100" height="100" title="IBRO">


## Team

![image](https://user-images.githubusercontent.com/34287081/213763502-f9a8a7cb-5872-4047-a898-33cd571932b5.png)





## Install all dependencies
```
pip install -r requirements.txt
```
