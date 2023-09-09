# Coping with Plenitude:  A Computational Approach to Selecting the Right Algorithm 

In this paper, we provide a strategy for selecting the best algorithm given a set of data when using Relational Class Analysis (RCA). Due to limitations on GitHub regarding the size of files, we have moved the code and data that we developed for this method to a public Google Drive folder. You can find it at the following link: https://drive.google.com/drive/folders/1tvPSUberqbiiB48cWTfcS95eQdQsWHO-

The folder contains four files. The .RDS files contain the simulations from the paper, which are used to fit models for selecting the best performing algorithm for your data. The .cpp file contains a C+ implementation of relationality that greatly speeds up its calculation. 

The primary file that you will use to perform metafeature selection is metafeature_RCA.R. It contains four primary functions:

1. evaluate.metafeatures() -- calculates the relevant metafeatures on your data.
2. predict.accuracies() -- uses the models provided in the RDS files to predict how accurately each distance measure/algorithm will perform on your data given the calculated metafeatures
3. select.method() -- selects the best available distance measure/algorithm given the predicted accuracies calculated in the previous step
4. metaRCA() -- which runs RCA using the selected distance measure

The basic workflow looks like this:

First, evaluate metafeatures on your data. 

```metafeatures = evaluate.metafeatures(data)```

Second, predict which measure will be most accurate given your data's metafeatures and the models provided in the .RDS files.

``` predictions = predict.accuracies(, models)```

Third, select the top N measures for your data. 

```top_measure = select.method(example_data, models, n = 1)```

Fourth, run RCA using that measure. 

```rca_result = metaRCA(example_data, measure = names(top_1[1]))```



Please feel free to direct any questions you may have about the code or paper to ramina.sotoudeh@yale.edu. 
