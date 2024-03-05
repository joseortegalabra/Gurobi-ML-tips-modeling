# Gurobi ML Tips
Repo that contains tips of modeling a optimization problem with machine learning models. 
IMPORTANT NOTE: All the examples follow one network used to create the optimization problem but each examples are individual each other and only represent an idea how to write differents constraints but not search the optimal value of the problem

### Example use case
The examples are created using the following network. 


### Optimization problem
This network can be represent as the following optimization problem

-- complete --


### Significado de las variables en el diagrama
- **X: Variables Primarias**: Variables de decisión de un optimizador y features de un modelo de machine learning. No se origina de ninguna relación anterior
- **Y: Variables Targets**: Variables de decisión de un optimizador y target de un modelo de machine learning
- **Z: Variables Secundarias**: Variables de decisión de un optimizador y features de un modelo de machine learning. Se diferencia de las variables primarias en que las variables secundarias se originan a partir de una relación con una Variable target
- **O: Variables Observadas**: NO son variables de decisión de un optimizador y solo son features de un modelo de machine learning

### Order Folders
- 0_temples: contains a basic template of notebooks to start working in this repo and how to acess to gurobi with and without licence
- 1_data: contains a code to generate fictious data for this example
- 2_modeling_ml: contains a codes to train a machine learning model for each process
- 3_optimization_tips: contains tips about how to use gurobi to do write some constraints with gurobi-pandas and gurobi-machine-learning
    - i_gurobi_pandas: contains codes with examples how to use gurobi and gurobi pandas to write differents constraints
    - ii_gurobi_machine_learning: contains codes with examples how to connect machine learning models as constrains in gurobi using gurobi-machine-learning package
    - iii_gurobi_automatization_optimizer: contains codes how to automatize the creation of gurobi models.
- 4_full_example_optimization_tanks: contain a full example about how to solve the full network (using all the tips development in the previous folder) and also, then how to automatize this kind of problems
- artifacts: contain artifact, data and models used in the full example "4_example_optimization_tanks"
- config: contain the configuration files to get the models and to build the full optimizer
      - config_ml_models_development: configuration files to train ml models
      - optimization_engine: configuration files of optimzer development in the full example


### List Examples modeling
-
-
-
-
-
-
-

### List Machine Learning models trained to connect to gubori



