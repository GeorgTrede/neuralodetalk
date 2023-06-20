# NeuralODE Talk
Material of the seminar talk on Neural ODEs held in summer 2023, Heidelberg Universtiy

NeuralODEs are a great concept for transforming fixed time step predictions (such as ResNets) into a continuous time algorithm. This allows to determine states at any point in time and using well known and studied ODE solvers that can provide certain requested levels of accuracy.

In this repo you can find the slides used in the talk as well as two jupyter notebooks:
- One gives a comparison of using a plain MLP/NN, a ResNet and finally a NeuralODE to predict a simple toy model, showing advantages and disadvantages of each one
- The second one is a "real world" use case, where weather data is downloaded from a publically available API and a NeuralODE is trained to model this data. After training, also states in between the provided training points can be predicted/inferred.

### Requirements

In order to run the provided jupyter notebooks yourself, you'll need the following libraries:
`torch`, `torchdiffeq`, `scipy`, `pandas`, `numpy`, `matplotlib`. All of these can be installed using `pip`:

```
pip install torchdiffeq torch numpy scipy pandas matplotlib
```
