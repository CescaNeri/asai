## Auto ML

The increasingly growing size of data overcomes the availability of companies to analyze them.

AutoML smartly explores huge search spaces and regards the steps of data-preprocessing and modeling in the ML pipeline.

A data pipeline consists of a sequence of transformations.

### Auto Weka

Tool which allows for automated machine learning introducing **combined** algorithm selection and hyper-parameter optimization problems.

Elements:

* Data set
* Algorithms
* Hyper-parameters
* Metrics

Explore all the configurations is unfeasible, we need to explore a few of them but in a smart way:

* Divide the exploration in iterations
* Keep track of past evaluation scores
* Build / update a probabilistic model

### Sequential Model-Based Optimization

It is a formalization of the Bayesian Optimization:

1. Evaluate some random hyper-parameters configurations
2. Build a probabilistic model
3. Exploit the model and the acquisition function to find the next hyper-parameters configuration to evaluate
4. Evaluate the hyper-parameters configuration
5. Update the probabilistic model incorporating the new results
6. Repeat steps 3-5 until the budget exceeded

### Meta Learning

It refers to the use of the results obtained in other case studies (according to meta-features) to tune other models.

`OpenML` -> online repository 

## Explainable Artificial Intelligence

Humans and intelligence agents work together in intelligent socio-technical systems to produce overall **intelligent behavior**.
Information and actions by intelligent agents need to be understandable by humans to be **accepted** and **trusted**.

**Symbolic** approaches are understandable by humans (transparent), but are slow, while **sub-symbolic** approaches are fast but opaque.

The solution is to join these two approaches.

### Local Interpretable Model-Agnostic Explanations (LIME)

It is a library which allows a clear and intuitive interpretation of prediction, applicable to any sort of supervised predictor.

### Explanations via Symbolic Knowledge Extraction

Any algorithmic procedure accepting trained sub-symbolic predictors as input and producing symbolic knowledge as output. 
