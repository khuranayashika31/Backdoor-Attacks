# LAB 4: Backdoor Attacks

Yashika Khurana  
 
Net Id: yk2773  

NYU Tandon School of Engineering


## Overview

This repository contains all code used for the completion of Lab 4: Backdoor Attacks. 
The primary objective of this work is to design a backdoor detector. Leveraging the pruning defense discussed in class, we systematically prune the last pooling layer of the BadNet (B), removing channels based on their average activation values over the validation set. This process results in a refined network, B', where pruning ceases once the validation accuracy drops below a predefined threshold, providing us with a robust defense against backdoor attacks.We explore the performance of the repaired networks for varying pruning percentages (X={2%, 4%, 10%}) and save the model accordingly. Upon receiving a test input, GoodNet G runs through both B and B'. If the outputs from both classifiers align, indicating the prediction belongs to class i, G will produce the output as class i. Conversely, if the outputs differ, signifying a discrepancy in the predictions, G will generate an output corresponding to class N+1.

## Environment
The notebook requires high RAM. Due to which, it was run on NYU's HPC environment with the given specifications:
* Cores: 2
* Memory: 32 GB
* GPU: None
* CUDA Version: v11

## How To Run
Requires credentials to access NYU HPC.

* Retrieve the dataset and model by accessing [CSAW-HackML-2020.](https://github.com/csaw-hackml/CSAW-HackML-2020/tree/master/lab3)

* Transfer the contents of this folder to scratch/netid directory on NYU High-Performance Computing (HPC).

* Initiate a Jupyter Notebook session on NYU HPC.

* Launch the provided Jupyter notebook within the environment.

* Modify file locations within the notebook to establish connections with the dataset and badnet model.

* Run the notebook to execute the code with the specified configurations.










