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
    - Linear
    - Off
    - Discontinous
    - trend_reg: Here more tricky as we had to modify the `_add_batch_regularizations` method

4. For the lr_finder we had to add code at the beginning of the forward method. This code assigns a dummy "ID" to all the individuals, and consequently, the lr_finder will be executed as if the trend mode were "global"


# TO BE DONE: ALFONSO  (search for that)
- Discontinuous
- pytorch how to pass arguments to forward -- To pass the meta (the learning rate size finder is not working right now)


TO DO:
- Remove tensorboard 
- Check if torchvision is a computer vision library - if so i installed it without meaninng it - Uninstall