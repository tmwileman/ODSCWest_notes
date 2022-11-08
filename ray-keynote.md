# Making ML Scaling Easy
## November 2, 2022
## Ion Stoica, PhD
---
### Notes

- Trends
    - Apps increasingly incorporate AI
    - AI demands exploding 
        - Compute requirements 35x every two years
- Challenges
    - Scale at every stage (preprocessing, training, tuning, prediction, serving)
    - Difficult to stitch together all the tools that help you scale at each step
- Soution: Ray
    - FAT compute model 
        - Futures - refernece objects
        - Actors - remote objects
        - Tasks
```python
@ray.remote
def f(x):
    return r

x_id = f.remote(a)
y_id = f.remote(b)
ray.get([x_id, y_id])
```

- Ray Tune
    - Hyperparameter tuning
    - Supports distributed training
    - Supports distributed hyperparameter tuning
    - Supports distributed hyperparameter tuning with distributed training
- Ray Serve
    - Model serving
    - Supports distributed model serving
    - Supports distributed hyperparameter tuning with distributed model serving and distributed training
- Ray Datasets
    - Distributed data processing
    - Supports distributed data processing
    - Supports distributed hyperparameter tuning with distributed data processing, distributed model serving, and distributed training

- Distributed ML apps are becoming the norm
- Building distributed ML apps is hard
- Ray unified framework dramatically simplifies scaling ML apps

### Investigate
- Definition of FLOP

