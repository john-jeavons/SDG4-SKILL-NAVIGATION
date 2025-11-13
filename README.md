# SDG4-SKILL-NAVIGATION
# 🎓 SDG4 Skill Navigator - Query Classification Model
[Project link](https://huggingface.co/spaces/johnjeavons/sdg4-skill-navigator)
## 1. Project Overview

This project implements a text classification model designed to automatically categorize user queries related to skills and educational opportunities. The primary goal is to serve as the core engine for an **SDG4 Skill Navigator** platform, helping route users to the correct resources based on their needs.

The model is fine-tuned from the **DistilBERT** architecture using the Hugging Face ecosystem (Transformers and Datasets libraries).

### 🏷️ Classification Labels

The model classifies input text into one of five categories:
* `FIND_FREE_COURSE`: Queries seeking zero-cost or free online courses.
* `SEEK_AI_SKILLS`: Queries specifically interested in Artificial Intelligence (AI) and Machine Learning skills.
* `ASK_BEGINNER_INFO`: Fundamental, introductory, or "explain like I'm new" questions.
* `CERT_PATH_REQUEST`: Requests for accredited programs, diplomas, or recognized certificates (e.g., Google, AWS, Coursera).
* `GENERAL_GREETING`: General greetings or non-skill-specific conversation starters.

***

## 2. Setup and Installation

This project is delivered as a single Jupyter Notebook (`project (1).ipynb`). It is designed to be run in a cloud environment like **Google Colab** for easy reproducibility.

### Prerequisites

1.  **Google Colab / Jupyter Environment:** An environment with GPU access (a **T4 GPU** is recommended for efficient training).
2.  **Hugging Face Account:** An account on the Hugging Face Hub is required to push the trained model. A write token must be configured as a secret named `HF_TOKEN`.

### Dependencies

Run the following command in the first cell of the notebook to install all required libraries:

```bash
!pip install transformers datasets accelerate pyarrow==19.0.0
3. How to Run the Project
Open the Notebook: Load project (1).ipynb in Google Colab.

Authenticate: Run the cell to log in to the Hugging Face Hub using your secure token.

Data & Preprocessing: Run the cells for data creation, tokenization, and dataset splitting.

Training: Run the cell containing the Trainer and trainer.train() method. This will train the model for 10 epochs.

Deployment: Upon completion, the model and tokenizer are automatically pushed to the Hugging Face Hub. The notebook confirms the deployment with a final print statement.

Demo: The final cells demonstrate model inference using the Hugging Face pipeline and a simple Gradio interface for interactive testing.

4. Deployment and Model Card
The trained and deployed model, along with its configuration and detailed results, is available on the Hugging Face Hub. This card provides details on the model architecture, training parameters, evaluation metrics, and licensing.

[🔗 Hugging Face Model Card Link]
login to hugging face 

5. Contact
For questions regarding this project, please contact the repository owner.
