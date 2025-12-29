# 📊 LLM Dataset Generator

A Gradio-based web application that leverages **Llama-3.2-3B-Instruct** to generate custom datasets based on natural language descriptions. Users can specify column names, data types, and row counts, then preview and download the result as a CSV.

## 🚀 Features

* **Natural Language to Table**: Simply describe the data you need.
* **Interactive Chat**: Refine your dataset through conversation (e.g., "Add a column for 'Email'").
* **Live Streaming**: See the model "think" and build the table in real-time.
* **CSV Export**: Extract the generated Markdown table and download it for use in Excel or Pandas.

---

## 🛠 Prerequisites

To run this notebook, you must have the following set up:

1. **Hugging Face Account**: You need an account at [huggingface.co](https://huggingface.co/).
2. **Llama 3.2 Authorization**:
* This model is a **gated model**. You must visit the [Meta Llama 3.2 3B Instruct](https://huggingface.co/meta-llama/Llama-3.2-3B-Instruct) page.
* Request access and wait for Meta to approve (usually takes a few minutes to an hour).


3. **Hugging Face Token**:
* Create a token with `Read` access in your [Hugging Face Settings](https://huggingface.co/settings/tokens).
* In Colab, it is recommended to store this as a secret named `HF_TOKEN`.



---

## ⚠️ Model Performance Disclaimer

This application uses a **Local LLM** (Llama-3.2-3B-Instruct).

* **Size vs. Capability**: This model is significantly smaller than "frontier" models (like GPT-4 or Llama-3-70B).
* **Limitations**: It may occasionally struggle with complex logical constraints, very large row counts in a single pass, or highly specialized domain knowledge.
* **Best Practice**: For the best results, keep your prompts clear and specific. If the model fails to follow a complex instruction, try breaking the request into smaller steps.

---

## 💻 Installation & Usage

1. **Clone the repository**:
```bash
git clone https://github.com/ohausner/datasetgeneratorchat.git

```


2. **Open in Colab**: Upload the `.ipynb` file to Google Colab.
3. **Set your Secrets**: Add your `HF_TOKEN` to the Colab "Secrets" (key icon).
4. **Run All Cells**: The Gradio interface will launch at the bottom of the notebook, providing a public or local URL.

---

## 📄 License

This project utilizes Meta's Llama 3.2. Use of this model is subject to the [Llama 3.2 Community License Agreement](https://huggingface.co/meta-llama/Llama-3.2-3B-Instruct/blob/main/LICENSE.txt).
