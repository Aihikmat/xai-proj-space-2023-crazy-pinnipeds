[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/_ksQZrdK)

# Explainable AI Assignment 1: Projection Space Exploration
In this assignment, you are challenged to analyze and compare solutions of a problem, game, algorithm, model, or anything else that can be represented by sequential states. For this, you will project the high-dimensional states to the two-dimensional space, connect the states, and add meta-data to the visualization.

Exemplary solutions are provided in the `solution_rubik.ipynb` and `solution_2048.ipynb` notebooks. 

Further examples to analyze are (board) games and approximation algorithms. The 2048 notebook uses [OpenAI Gym](https://gym.openai.com/) to create a game environment and produce state data. There is a variety of first and third party environments for Gym that can be used.

## General Information Submission

For the intermediate submission, please enter the group and dataset information. Coding is not yet necessary.

**Group Members**

| Student ID    | First Name  | Last Name      | E-Mail |  Workload [%] |
| --------------|-------------|----------------|--------|---------------|
| 51831270        | Markus      | Karner         |K51831270@students.jku.at  |45%         |
| 11913261        | Hikmatullah      | Razaghi        |donhiki10@gmail.com  |30%         |
| 12248150       | Mahmoud      | Elsherief         |mahmoudsherief2019@gmail.com  |0%         |
| 12147764       | Kareem     | Muhammed    |  K12147764@students.jku.at|25%         |

### Dataset
Please add your dataset to the repository (or provide a link if it is too large) and answer the following questions about it:

* Which dataset are you using? What is it about?
  We used the Cart Pole environment from Gymnamisum https://gymnasium.farama.org/environments/classic_control/cart_pole/ to train a DQN agent.
  This agent should hold the pole in center at a straight angle.
  The dataset has 4 observation variables: Cart Position, Cart Velocity, Pole Angle, Pole Angular Velocity.
  We uploaded a first version of it in the data folder. List of 500 episodes with variable length. So the shape is [500, sequence_length, 4]
* Where did you get this dataset from (i.e., source of the dataset)? How was the dataset generated?
  We created our own dataset by training an agent on the gym environment Cart Pole. Using the code from here https://pytorch.org/tutorials/intermediate/reinforcement_q_learning.html.
* What is dataset size in terms of nodes, items, rows, columns, ...?
  The dataset has 500 episodes with various sequence length and 4 observation variables at each sequence step.
* What do you want to analyze?
  We want to analyze how the training progresses to hold the pole in the center. By just plotting the sequence length one can already see when the agent learns. But we want to analyze if we can see something more in the observation variables at each step.
* What are you expecting to see?
  The first runs should all randomly deviate from the same start position (which should be close in the downprojection). We expcect a "perfect" agent to hold the pole in center (with long sequences).


## Final Submission

* Make sure that you pushed your GitHub repository and not just committed it locally.
* Sending us an email with the code is not necessary.
* Update the *environment.yml* file if you need additional libraries, otherwise the code is not executeable.
* Create a single, clearly named notebook with your solution, e.g. solution.ipynb.
* Save your final executed notebook as html (File > Download as > HTML) and add them to your repository.


## Development Environment

Checkout this repo and change into the folder:
```
git clone https://github.com/jku-icg-classroom/xai_proj_space_2023-crazy-pinnipeds.git
cd xai_proj_space_2023-crazy-pinnipeds
```

Load the conda environment from the shared `environment.yml` file:
```
conda env create -f environment.yml
conda activate xai_proj_space
```

> Hint: For more information on Anaconda and enviroments take a look at the README in our [tutorial repository](https://github.com/JKU-ICG/python-visualization-tutorial).

Then launch Jupyter Lab:
```
jupyter lab
```

Go to http://localhost:8888/ and open the *template* notebook.

Alternatively, you can also work with [binder](https://mybinder.org/), [deepnote](https://deepnote.com/), [colab](https://colab.research.google.com/), or any other service as long as the notebook runs in the standard Jupyter environment.
