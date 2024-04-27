# Final Year Project - Vehicular Task Allocation Framework

This repository contains the implementation and results of our vehicular task allocation framework, designed to integrate machine learning models with a reinforcement learning (RL) framework using Proximal Policy Optimization (PPO) algorithm.

## Repository Structure

- `/Training`: Contains all the training files for our models. Each model has a set of four files, each corresponding to different noise levels and task quantities:
  - Baseline (PPO Only)
  - PPO + Ridge
  - PPO + SVR
  - PPO + KNN
- `/Test`: Contains the files used for testing each of the trained models. Each file corresponds to the model trained with a specific noise level and task quantity.
- `/Datasets`: Includes all datasets used for training ML models and for assigning tasks to the vehicles.
- `/Plots_and_Tables`: Contains files used for generating plots and tables for data analysis and results presentation in the report.

## Datasets

- `VehicleTrainingDataset.csv`: Used for training the machine learning models.
- `1000VehicleDataset.csv`: Used for assigning tasks to vehicles.
- `RandomTasks200.csv`: Task dataset used for training on 200 tasks.
- `RandomTasks400.csv`: Task dataset used for training on 400 tasks.
- `RandomTasks200Test.csv`: Task dataset used for testing models trained on 200 tasks.
- `RandomTasks400Test.csv`: Task dataset used for  testing models trained on 400 tasks.

## Training and Testing

The training and testing of our models were conducted as follows:

- Training:
  - Each model was trained with four different configurations: 0.01 noise with 200 tasks, 0.1 noise with 200 tasks, 0.01 noise with 400 tasks, 0.1 noise with 400 tasks.
  - The code for each training configuration was run 10 times, and the results from the final (100th) iteration were collected.

- Testing:
  - The trained models were then tested with a single run on a set of either 200 random tasks or 400 random tasks, depending on the training configuration.
  - The final successful assignments and mean reward metrics were collected from these tests.

## Results

The results from the training and testing phases were used to construct box plots and other visualizations for the project report, demonstrating the performance and robustness of our proposed task allocation framework.

## Usage

To replicate our experiments or to utilize the framework for your own task allocation scenarios, navigate to the respective training or test file within the `/Training` or `/Test` directory and execute the Python scripts as per the standard Python execution procedures.

## Acknowledgments

We would like to acknowledge the contributions of all team members, project supervisors, and anyone who offered insights and feedback during the development of this project.

