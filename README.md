# amr-samples-metamodels-package
This repository contains data for training and testing metamodels (Kriging, RBF, ...) that are used in a new surrogate based optimization (SBO) process called adaptive model refinement. The resulting trained metamodels are also included in this package. For further information on this data set or the new SBO method associated with it, please refer to our paper:
Ghassemi, P., Mehmani, A., and Chowdhury, S., Adaptive In-Situ Model Refinement for Surrogate-augmented Population-based Optimization, Structural and Multidisciplinary Optimization. April 2020. Springer. https://doi.org/10.1007/s00158-020-02592-6 

The following sections provide further information on the usage of this data set and its corresponding metamodels: 

# JSON File 
The metamodel (surrogate model) hyperparameters and the paper information are included in the JSON file "model_info.json". This JSON file has two main enteries (field names):

## Metamodels Information
The entry "models" contains the model information. This item has 5 enteries (the problem names): Six-hump Camel Back, Branin-Hoo, Dixon-Price, Griewank functions, and the Building Energey Management problem. The first four models (the benchmark problems) have three enteries: "pso-amr", "pso-amr-local", "pso-sbo-k1", and the last model (the application problem) has two eneries: "pso-amr" and "pso-sbo". Each model contains the model hyper-parameters, the dataset name, and the optimum value (computed using high-fidelity simulation/model).

## Paper Information
The entry "paper" provides the article information, such as title, author list, publisher, and journal name.

# Data Set
The total data set (including initial data set and the infill sample points) for each problem has been saved as a text file. For the "amr" and "amr-local" methods, the first "m" samples in the file give the initial data set (DoE), and the rest samples are the infill points. The value of "m" can be retrieved by looking at the value of "sample-size" in the "initial" enetry.  
