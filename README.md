# Stylometry-driven Paraphrasing of User Stories with Large Language Models

This repository accompanies the paper on Stylometry-driven Paraphrasing of User Stories
with Large Language Models. Each folder contains files relevant to specific research questions addressed in the paper.

## Requirements

Before you begin you need to install the following:

- [Ollama](https://ollama.com/)

Pull the model that you want to use and make sure that ollama is running.

Install dependencies with

```
pip install -r requirements.txt
```

## Research Question 1 Experiments

The experiments related to Research Question 1 are located in the `rq1` folder. This folder contains the following files:

- **Synthetic User Stories.xlsx**: The dataset file containing synthetic user stories.
- **main.py**: The script that requests paraphrasing from the LLMs and saves the results.
- **metric.py**: A helper file that contains functions to compute stylometry metrics.
- **metricvalues\_(LLM_name).csv**: This file includes the paraphrased user stories and the corresponding stylometric values for each LLM. The `metricvalues_llama2.csv` file also contains values for the original user stories.
- **get_average_metric_vals.ipynb**: A Jupyter notebook containing code to calculate the average values for each stylometry metric from the CSV files.

### Instructions

1. Indicate the model name you want to use in the `main.py` file and run with the following command:
   ```bash
   python main.py
   ```
2. Specify the filename in `get_average_metric_vals.ipynb`.

## Research Question 2 Experiments

The experiments related to Research Question 2 are located in the `rq2` folder. This folder contains the following files:

- **Synthetic User Stories.xlsx**: This dataset file contains synthetic user stories.
- **main.py**: This script requests paraphrasing from the LLMs with instructions and saves the results.
- **metric.py**: A helper file that contains functions to compute stylometry metrics.
- **(LLM_modelname)-1.csv**: These files contain results for each LLM.
- **(LLM_modelname)-1-def.csv**: These files contain results for each LLM. The `-def` suffix indicates if the definition was included in the prompt.

### Instructions

1. Open `main.py` and specify whether you want to include the definition. Also, select the model name you want to use. Run the script with the following command:
   ```bash
   python main.py
   ```
2. Open `Evaluation Inference Classification.ipynb` to get the results for each stylometry metric.
