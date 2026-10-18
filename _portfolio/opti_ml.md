---
title: "Optimization for ML (CS-439) : Quantization on Q-learning"
title_fr: "Optimization for ML (CS-439) : Quantification appliquée au Q-learning"
excerpt: "Measuring the effectiveness of quantization on SpeedyQ and vanilla Q-learning. <a href='https://github.com/MathisHage/opti_ml_project'>[GitHub]</a>"
excerpt_fr: "Mesure de l'efficacité de la quantification sur SpeedyQ et le Q-learning classique. <a href='https://github.com/MathisHage/opti_ml_project'>[GitHub]</a>"
collection: portfolio
date: 2026-06-15
fr_url: /fr/projects/
---

# Measuring the effectiveness of quantization on SpeedyQ and vanilla Q-learning

**Authors** : Killian Didierjean, Charles Mercier, Mathis Hage  
**Institution** : EPFL — School of Computer and Communication Sciences  
**Course** : Optimization for ML (CS-439), June 2026  
**Repository** : [github.com/MathisHage/opti_ml_project](https://github.com/MathisHage/opti_ml_project)

---

## Abstract

Reinforcement Learning is today widely used to solve a variety of problems. In particular, Q-learning is a very popular method allowing one to learn a policy without needing a predefined model of the environment. However, it can rapidly require a lot of memory space to function. In this paper, we study quantization of the Q-table : we will see that this method can lead up to at least 8 times less space used, without any significant loss in results quality.

## Contribution

Our contribution was to compare two versions of Q-learning : vanilla and *SpeedyQ* and, more specifically, to see how they both behave under quantization of the Q-table at training time. Informally : up to what point can we discretize the possible values that a Q-table entry can take, while still obtaining quality results ?

## The Code & Setup

Our experiments were conducted in Python, and every bit of data in the report was generated from the Jupyter notebook. Our implementation uses [Gymnasium's CartPole environment](https://gymnasium.farama.org/environments/classic_control/cart_pole/). We also use [Joblib](https://joblib.readthedocs.io/en/stable/) to train multiple agents at the same time. Graph generation was done using [Matplotlib](https://matplotlib.org/), and computations were done with [NumPy](https://numpy.org/).

## Results

We observed that in most cases we obtain results comparable to full precision with only 8-bits quantization. This supports our claim that the results we obtained for our specific binning strategy were not an isolated case.

## Links
* [Code and Notebook on GitHub](https://github.com/MathisHage/opti_ml_project)
* [Report (PDF)](https://github.com/MathisHage/opti_ml_project/blob/main/report/report.pdf)
