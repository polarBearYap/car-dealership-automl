# car-dealership-automl

- An auto-trained machine learning model with interpretable prediction. (Normal ML model + model explainer)
- A proof of concept/simple prototype for ML model deployment in Azure.
- **Important**: Note that this repository is the prerequisite for another [repository](https://github.com/polarBearYap/car-dealership-flask-api). This repository is foucsed on model training and another one is focused on model deployment. Be sure to check out both.

## Table of Contents
* [Learning Purpose](#Learning-Purpose-)
* [Technology Applied](#Technology-Applied-)
* [Software Requirement](#Software-Requirement-)
* [Snapshot](#Snapshot)
* [Summary](#Summary)
* [Learning Lessons](#Learning-Lessons)
* [Credits](#Credits)

## Learning Purpose &#128218;
1. To learn how to implement explainable AI in deployment.
2. To learn ways to deploy machine learning models using AutoML APIs like Azure Machine Learning.
3. To get my hands dirty in DevOps &#128521;.

## Technology Applied &#129302;
- [Azure AutoML](https://docs.microsoft.com/en-us/azure/machine-learning/concept-automated-ml): Auto optmization of machine learning models without even trying &#129315;.

## Software Requirement &#128187;
- Jupyter Notebook
- Azure free account (Poor man choice &#129299;)

## Snapshot

1. Machine Learning Workspace

- ![snapshot10](snapshots/snapshot10.png)

2. Model and the model explainer deployed to AKS cluster.
- ![snapshot2](snapshots/snapshot2.png)

> As mentionend [here](#Learning-Lessons), I deleted the machine learning workspace earlier on because it's too expensive to put idle. Thus, GIF is not available &#128531;.

## Summary

1. The azure_automl_car_price_prediction.ipynb includes:

    a) Configure and run the Azure AutoML experiments.
    
    b) Retrieve the best model out of all runs and evaluate it.
    
    c) Refer to this [notebook](https://github.com/polarBearYap/car-dealership-automl/blob/main/azure_automl_car_price_prediction.ipynb) for the source code. Too bad, I forgot to save output for this notebook &#128531;.

2. The local_deployment_flask.ipynb includes:

    a) Train the SHAP Tree Explainer to be used in this [project](https://github.com/polarBearYap/car-dealership-flask-api). 
    
      - The explainer can be used to generating feature importance values for the whole dataset (global) and/or individual predictions (local).
      - In short, explainable AI/XAI/model interpretability is important for understanding how a ML model predicts and promote end-user trust on AI.
      - I learn the concepts of XAI mainly from [here](https://christophm.github.io/interpretable-ml-book/).  
      - More information regarding the explainer API can be found in this [MS Docs](https://docs.microsoft.com/en-gb/azure/machine-learning/how-to-machine-learning-interpretability).
    
    b) Deploy to local compute instance.
    
    c) Deploy to Azure Kubernetes Service (AKS).
    
    d) Refer to this [notebook](https://polarbearyap.github.io/car-dealership-automl/) for the source code.

> Note that both of these two notebooks are for display only. It needs a Azure Machine Learning workspace to execute.

## Learning Lessons

- I learn how the Azure cost is calculated, next time I should better delete all the machine learning resources ASAP. Or else the storage fee going to pile up &#128184;! 

## Credits

1. Stack Overflow Community
2. My university UTAR. For renewing my free $100 Azure credit yearly. However, I almost used finish already due to inexperience &#128546;.

Python dependencies can be found in the requirements.txt.
