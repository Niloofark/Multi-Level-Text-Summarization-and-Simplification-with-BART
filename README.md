## Multi-Level Text Simplification with BART

An end-to-end NLP pipeline for text simplification and summarization using BART, applied across two phases: OneStopEnglish (OSE) in Phase 1 and M3 in Phase 2.
Includes full data cleaning, EDA, fine-tuning, and joint multi-dataset training.

## Notebooks
- Phase 1
  - Data Cleaning and EDA
  - Training and Evaluation
- Phase 2
  - Data Cleaning and EDA
  - Fine-Tuning
  - Joint Training


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
