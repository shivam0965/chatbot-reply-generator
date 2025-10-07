# 💬 Chat Reply Recommendation System

## 📘 Overview
The Chat Reply Recommendation System is an AI-based text generation project built using the GPT-2 Transformer model.  
It takes a user’s chat message as input and predicts the most relevant reply, trained on a single dataset containing conversational data.  
This project demonstrates how natural language models can generate human-like responses suitable for chatbots, virtual assistants, and conversation simulators.

---

## 🎯 Objectives
- Preprocess and clean conversational data for model training.  
- Fine-tune the GPT-2 model on a single chat dataset.  
- Generate intelligent and contextually appropriate responses.  
- Evaluate performance using BLEU score for linguistic accuracy.  

---

## 🧩 Project Workflow

### 1️⃣ Data Preprocessing
- Loaded a single dataset (conversationfile.csv or .xlsx) containing chat messages.  
- Removed missing entries and stripped whitespace.  
- Formed input–output pairs, where each message is followed by its reply.

### 2️⃣ Model Setup
- Used the GPT-2 model from Hugging Face’s transformers library.  
- Initialized tokenizer and model with pre-trained weights.  
- Assigned EOS token as padding token for compatibility.  

### 3️⃣ Model Training
- Fine-tuned the model using AdamW optimizer on message–reply pairs.  
- The loss function automatically computed during training.  
- The model learned contextual relationships between user inputs and replies.  

### 4️⃣ Reply Generation
- Generated replies for unseen user inputs using the trained GPT-2 model.  
- Controlled text generation using parameters like max_length.  

### 5️⃣ Evaluation
- Used BLEU score to evaluate the quality of generated replies.  
- Lower training loss and higher BLEU scores indicated better performance.  

---

## 🧠 Technologies Used

| Technology | Description |
|-------------|-------------|
| Python | Core programming language |
| Pandas | Data loading and preprocessing |
| Transformers | Model loading and text generation |
| PyTorch | Model optimization and fine-tuning |
| NLTK | Evaluation using BLEU score |

---
