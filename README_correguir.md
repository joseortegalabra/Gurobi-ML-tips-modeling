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
- **0_temples**: contains a basic template of notebooks to start working in this repo and how to acess to gurobi with and without licence
- **1_data**: contains a code to generate fictious data for this example
- **2_modeling_ml**: contains a codes to train a machine learning model for each process
- **3_optimization_tips**: contains tips about how to use gurobi to do write some constraints with gurobi-pandas and gurobi-machine-learning
    - **i_gurobi_pandas**: contains codes with examples how to use gurobi and gurobi pandas to write differents constraints
    - **ii_gurobi_machine_learning**: contains codes with examples how to connect machine learning models as constrains in gurobi using gurobi-machine-learning package
    - **iii_gurobi_automatization_optimizer**: contains codes how to automatize the creation of gurobi models.
- **---> 4_full_example_optimization_tanks**: contain a full example about how to solve the full network (using all the tips development in the previous folder) and also, then how to automatize the creaton of optimizer for this kind of problems
- **artifacts**: contain artifact, data and models used in the full example "4_example_optimization_tanks"
- **config**: contain the configuration files to get the models and to build the full optimizer
      - **config_ml_models_development**: configuration files to train ml models
      - **optimization_engine**: configuration files of optimzer development in the full example


### List Examples modeling. Examples located in the folder: 3_optimization_tips/i_gurobi_pandas
- **1_works_var_gurobi_pandas**: indicate how to define decision var and simple constraints in gurobi pandas. It works as hello_world_gurobi
- **2_constraints_absolute_values**: indicate how to define a constraint that have an absolute value
- **3_formula_as_constraint**: indicate how to add a custom formula as a contraint
- **4_fixed_values_decision_var**: indicate how to set a value of a decision variable (ex x1(t=0) = 10)
- **5_constraint_time_related**: indicate how to define constaints related to previous time for example X(t) - X(t-1) <= 10
- **5b_constraint_time_related-update**: the same previous with and adaptation in the codes.
- In the folder 3_optimization_tips/iii_gurobi_automatization_optimizer there a notebook to try to automtize the construction of gurobi optimizer for this kind of problems (semi automatization)

### List Machine Learning models trained to connect to gubori. Examples located in the folder: 3_optimization_tips/ii_gurobi_machine_learning
- **1_compatibility_gurobi_ml**: test if a ml model trained can connect to gurobi-machine-learning. using a free licence
- **2_compatibility_gurobi_ml_licence**: the same previos notebook but using gurobi with a paid licence
- **3_predict_model_multiple_time** using one machine learning model to predict a dataframe with multiple rows. In this example each row represent a set of elements. In this case, a set of time. X(t) -> ml model
- **4_predict_model_multiple_sets**: similar to a previous notebook. But in this notebook using a machine learning model to predict a dataframe that have multiple rows and its represents two or more subsets of data. X(p, t) -> ml model
- **5_piecewise_model_observed_variables**: how to train a "piecewise model". In this case, split the data according a observed features (that are not decision variable in the optimization model) and train differetns models according this segmentation. Then, load the ml model according the value of the observed variable
- In the folder 3_optimization_tips/iii_gurobi_automatization_optimizer there a notebook to try to automtize the construction of gurobi optimizer for this kind of problems (semi automatization)

### FULL EXAMPLE -  4_full_example_optimization_tanks
In the folder  4_full_example_optimization_tanks there a full example apply all the knowledge of previous notebook to develop the codes of the diagram. 

There two notebooks:
    - the first represent a hardoded optimization model (I recommend start always defining te optimization problem and write an hardoded because is more easy and can relationate the variables in a easy way). 
    - **the second one is the automatization of the previous notebook using the configuration files to create this kind of problems changing the number of variables and the number of process and tanks!!!**