## Multi-Level Text Simplification with BART

A complete BART-based text simplification system covering data cleaning, EDA, fine-tuning, and evaluation on the OneStopEnglish and M3 datasets. The project develops level-controlled simplification models and a joint multi-dataset model that generalizes across both domains.


## Notebooks

- Capstone Phase1_Data Cleaning and EDA.ipynb
- Capstone Phase1_Training and Evaluation.ipynb
- Capstone phase2_Data Cleaning and EDA.ipynb
- Capstone phase2_Model FineTunning.ipynb
- Capstone phase2_joint.ipynb



## Overview
## Phase 1 — OneStopEnglish

- Clean & analyze ADV/INT/ELE aligned texts

- Train BART for multi-level simplification (Adv→Int, Adv→Ele, Int→Ele)

## Phase 2 — M3 Dataset

- Clean multi-domain M3 dataset

- Fine-tune the Phase-1 model on M3

- Select best checkpoint using ROUGE

## Joint Model — OSE + M3

- Combine both datasets

- Add control tokens: <TASK:OSE> <TASK:M3> <LEVEL:adv/int/elem>

- Train unified multi-dataset simplification model

## Installation
git clone https://github.com/yourusername/your-repo
cd your-repo

python3 -m venv env
source env/bin/activate    # Mac/Linux
env\Scripts\activate       # Windows

pip install transformers datasets sentencepiece torch rouge-score

## Example Input → Output

Input (Advanced):
The economic ramifications of the policy were profoundly underestimated by analysts.

Output (Simplified):
Experts did not understand how the policy would affect the economy.

Joint Model Example:

<TASK:OSE> <LEVEL:elem> The investigation revealed several structural weaknesses in the organization.


Output:
The study found weak areas in the company.

## How to Run

Run notebooks in order:

1. Phase1_Data Cleaning and EDA
2. Phase1_Training and Evaluation
3. Phase2_Data Cleaning and EDA
4. Phase2_Model FineTunning
5. Phase2_Joint


All notebooks are Colab-ready with Drive paths included.

## Tools

Python • PyTorch • HuggingFace Transformers • ROUGE-score • Pandas • Colab

## License

For academic use. Datasets follow original creator licenses (OSE, M3).
