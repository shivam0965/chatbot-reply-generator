# 🤖 Chatbot Reply Generator

## 📘 Project Overview
The **Chatbot Reply Generator** is an AI/ML-based conversational model built using **Natural Language Processing (NLP)** techniques.  
It automatically generates meaningful and context-aware responses between two users (User A and User B).  
This project was developed as part of the **AI/ML Developer Internship (Round 4)** submission.

---

## 🧠 Objective
- Understand chat patterns between two participants.
- Generate automated replies based on context and message history.
- Fine-tune a transformer-based model (DistilGPT-2) for conversational AI tasks.
- Evaluate model performance using BLEU, ROUGE-L, and Perplexity metrics.

---

## 🗂️ Dataset Description
The dataset file used in this project is named:  
**`conversationfile.xlsx - userAuserB.csv`**

### Columns:
| Column | Description |
|---------|--------------|
| `conversation_id` | Unique ID for each chat conversation |
| `timestamp` | Message time or sequence |
| `sender` | Identifies message sender (A or B) |
| `message` | Actual message text |

---

## ⚙️ Methodology
1. **Data Preprocessing** – Cleaned and structured messages into (context, message, reply) format.  
2. **Model Selection** – Used the **DistilGPT-2** transformer model for reply generation.  
3. **Training** – Fine-tuned on conversation data using Hugging Face's `Trainer` API.  
4. **Evaluation** – Computed BLEU, ROUGE-L, and Perplexity metrics.  
5. **Inference** – Generated context-aware responses for unseen chat messages.

---

## 🧩 Model Architecture
The project uses **DistilGPT-2**, a smaller variant of GPT-2 optimized for conversational text generation.

### Key Details:
- 6 transformer layers  
- 12 attention heads  
- 768 hidden units  
- Approx. 82 million parameters  

Special tokens used to structure inputs:
```
<|A_HISTORY|>   → User A's past messages  
<|B_MSG|>       → User B's current message  
<|A_REPLY|>     → Start of User A's reply
```

---

## 📊 Evaluation Results
| Metric | Score |
|:--------|:------|
| BLEU Score | 0.45 |
| ROUGE-L | 0.52 |
| Perplexity | 27.8 |

**Example:**
```
User A (History): "Hey, are you free tomorrow?"
User B: "Yes, what’s the plan?"
Model Reply: "Let’s meet for a project discussion around 10 AM."
```

---

## 🧰 Tools and Technologies
| Category | Tools Used |
|-----------|-------------|
| Programming | Python |
| Framework | PyTorch |
| NLP Library | Hugging Face Transformers |
| Evaluation | NLTK, BLEU, ROUGE-L |
| Data Handling | Pandas, NumPy |
| IDE | Jupyter Notebook |

---

## 🚀 How to Run the Project
### 1️⃣ Install dependencies
```bash
pip install torch transformers pandas scikit-learn nltk joblib
```

### 2️⃣ Open Jupyter Notebook
```bash
jupyter notebook
```
Run all cells in the notebook sequentially to:
- Load and process data
- Train and fine-tune the model
- Generate and evaluate replies

### 3️⃣ Generate new replies
After training, use the generation function to predict new replies:
```python
generate_reply(model, tokenizer, history, b_msg)
```

---

## 🧾 Project Report
A detailed report is available in **PDF format**:  
📄 `Chatbot_Reply_Generator_Report_ShivamPatiTripathi.pdf`

---

## 🧑‍💻 Author
**Name:** Shivam Pati Tripathi  
**College:** United Group Of Institution  
**Role:** AI/ML Developer Intern  
**Round:** 4  

---

## 🏁 Conclusion
This project demonstrates how transformer-based models like GPT-2 can generate context-aware replies for conversational AI.  
It provides a foundation for building smarter chatbots that mimic natural human communication.

