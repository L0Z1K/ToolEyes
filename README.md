# ToolEyes

## ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios

> Data for paper [ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios](https://arxiv.org/abs/2401.00741)

Junjie Ye

jjye23@m.fudan.edu.cn

Jan. 01, 2024

## Introduction
Existing evaluations of tool learning primarily focus on validating the alignment of selected tools for large language models (LLMs) with expected outcomes. However, these approaches rely on a limited set of scenarios where answers can be pre-determined, diverging from genuine needs. Furthermore, a *sole* emphasis on outcomes disregards the intricate capabilities essential for LLMs to effectively utilize tools.
To tackle this issue, we propose *ToolEyes*, a fine-grained system tailored for the evaluation of the LLMs' tool learning capabilities in authentic scenarios. The system meticulously examines seven real-world scenarios, analyzing five dimensions crucial to LLMs in tool learning: *format alignment*, *intent comprehension*, *behavior planning*, *tool selection*, and *answer organization*.
Additionally, ToolEyes incorporates a tool library boasting approximately 600 tools, serving as an intermediary between LLMs and the physical world. Evaluations involving ten LLMs across three categories reveal a preference for specific scenarios and limited cognitive abilities in tool learning.
Intriguingly, expanding the model size even exacerbates the hindrance to tool learning.
These findings offer instructive insights aimed at advancing the field of tool learning.


<div>
<center>
<img src=Figures/ToolEyes.png>
</div>

## What's New

- **[2023.01.01]** Release the tool library and data for ToolEyes. Code for inference and evaluation is on its way.
- **[2024.01.01]** Paper available on [Arxiv](https://arxiv.org/abs/2401.00741).


## Requirement
- Run the command to install the packages required.
    ```bash
    pip install -r requirements.txt
    ```

## Data
The tool lobrary and test data are released, which can be found in `ToolEyes/Tool_Library` and `/ToolEyes/Test_Data`, respectively. Below is the statistics of the data:

| **Scenario**      | **TG** | **DU** | **RS** | **PL** | **IR** | **AM** | **FT** | **Total** |
|-------------------|--------|--------|--------|--------|--------|--------|--------|-----------|
| **# Cat**         | 5      | 5      | 6      | 8      | 9      | 6      | 2      | 41        |
| **# Subcat**      | 6      | 5      | 14     | 30     | 19     | 7      | 14     | 95        |
| **# Tool**        | 27     | 26     | 75     | 164    | 150    | 164    | 96     | 568       |
| **# Query**       | 58     | 49     | 56     | 70     | 54     | 45     | 50     | 382       |


## Results in Different Scenarios

We evaluate the tool learning performance of the LLMs across seven real-world scenarios.

<div>
<center>
<img src=Figures/result-scenario.png>
</div>

## Results of Different LLMs Capabilities

We examine the entirety of the tool learning process, focusing on the five dimensions of capability essential for LLMs to successfully undertake tool learning.

<div>
<center>
<img src=Figures/result-capability.png>
</div>


## Citation
If you find this project useful in your research, please cite:
```
@misc{ye2024tooleyes,
      title={ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios}, 
      author={Junjie Ye and Guanyu Li and Songyang Gao and Caishuang Huang and Yilong Wu and Sixian Li and Xiaoran Fan and Shihan Dou and Qi Zhang and Tao Gui and Xuanjing Huang},
      year={2024},
      eprint={2401.00741},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
