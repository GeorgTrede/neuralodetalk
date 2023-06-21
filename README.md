# NeuralODE Talk

NeuralODEs are a great concept for transforming fixed time step predictions (such as ResNets) into a continuous time algorithm. This allows the user of well known ODE solvers that can provide certain requested levels of accuracy and moreover calculate the function at any time point, not just at fixed ones.

If you're looking for a simple walkthrough explaining NeuralODEs at a low level again, check out the following article: [Neural ODEs - breakdown of another deep learning breakthrough](https://towardsdatascience.com/neural-odes-breakdown-of-another-deep-learning-breakthrough-3e78c7213795). For a great explanation of the adjoint method (used for efficiently doing backprop in continuous time), the YouTube video by "Machine Learning & Simulation" is really worth it: [Adjoint State Method for an ODE](https://www.youtube.com/watch?v=k6s2G5MZv-I).

In this repo you can find the slides used in the talk as well as two jupyter notebooks:
- One gives a comparison of using a plain MLP/NN, a ResNet and finally a NeuralODE to predict a simple toy model, showing advantages and disadvantages of each one
- The second one is a "real world" use case, where weather data is downloaded from a publically available API and a NeuralODE is trained to model this data. After training, also states in between the provided training points can be predicted/inferred.

### Requirements

In order to run the provided jupyter notebooks yourself, you'll need the following libraries:
`torch`, `torchdiffeq`, `scipy`, `pandas`, `numpy`, `matplotlib`. All of these can be installed using `pip`:

```
pip install torchdiffeq torch numpy scipy pandas matplotlib
```
