## For visualization

1. install torchviz
2. install  torchsummary
3. in `_train_epoch` method --> added `self.train_epoch_prediction` to be able later to visualize the architecture.


## Local Trend
1. Adding a in config_trend a variable with is trend_global_local: str
    1.1. We add in NP init the variable
    1.2  We add in configure.Trend the variable. Also added condition on input value not belonging to ["global", "local"]

2. Creating the model.
    2.1 We create the `id_list` attribute in the `fit` method

3. Modifying the trend piecewise method, using meta and the corresponding "ID" 




# TO BE DONE: ALFONSO  (search for that)
- Discontinuous
- pytorch how to pass arguments to forward -- To pass the meta (the learning rate size finder is not working right now)


TO DO:
- Remove variables used to visualise (usually created through `locals()`)
- Remove tensorboard 
- Check if torchvision is a computer vision library - if so i installed it without meaninng it - Uninstall