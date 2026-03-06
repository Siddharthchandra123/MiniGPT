# 🧠 MiniLLM – A Lightweight GPT Built From Scratch

MiniLLM is a lightweight GPT-style language model built from scratch using PyTorch.
The project demonstrates how modern Large Language Models (LLMs) work internally, including tokenization, transformer architecture, causal attention, and autoregressive text generation.

The goal of this project is to understand and implement the core components of GPT models without relying on large frameworks.

# 🚀 Features

✅ GPT-style Transformer architecture
✅ SentencePiece tokenizer for efficient tokenization
✅ Causal self-attention for autoregressive prediction
✅ Positional embeddings to capture word order
✅ Custom dataset pipeline for training text models
✅ Text generation capability after training
✅ Designed to run on CPU laptops without GPU

# 🏗 Architecture

MiniLLM follows the standard GPT architecture:

Input Text
   ↓
Tokenizer (SentencePiece)
   ↓
Token Embeddings
   ↓
Positional Embeddings
   ↓
Transformer Decoder Layers
   ↓
Causal Self Attention
   ↓
Feed Forward Network
   ↓
Linear Output Layer
   ↓
Next Token Prediction

Key components:

Embedding Layer – converts tokens to vectors

Positional Encoding – preserves sequence order

Multi-Head Self Attention – learns contextual relationships

Feed Forward Network – nonlinear feature transformation

Layer Normalization – stabilizes training

# 📂 Project Structure
```
MiniLLM/
│
├── dataset/
│   └── school_dataset.json
│
├── tokenizer/
│   ├── tokenizer.model
│   └── tokenizer.vocab
│
├── model/
│   └── gpt_model.py
│
├── training/
│   └── train.py
│
├── notebook/
│   └── school_gpt_corrected.ipynb
│
└── README.md
# 📊 Model Configuration
```

Example configuration used in MiniLLM:

Parameter	Value
Embedding Size	128–256
Transformer Layers	3–6
Attention Heads	4–8
Vocabulary Size	~8000
Sequence Length	64–128

This results in a small but functional GPT-style model suitable for experimentation.

# ⚙️ Installation

Clone the repository:

git clone https://github.com/yourusername/MiniLLM.git
cd MiniLLM

Install dependencies:

pip install torch sentencepiece tqdm
# 📚 Dataset Preparation

The dataset is converted into a training text format:

Instruction: Answer the question
Context: The Earth revolves around the Sun
Question: What does the Earth revolve around?
Answer: The Sun

This format helps the model learn instruction-style responses.

# 🧪 Training the Model

Run the training script:

python train.py

Training pipeline:

Load dataset

Train SentencePiece tokenizer

Convert text → tokens

Create training sequences

Train GPT model using cross-entropy loss

The model can be trained on a CPU laptop with small datasets.

# ✨ Text Generation

After training, generate responses:

generate("Question: What does the moon revolve around? Answer:")

Example output:

The moon revolves around the Earth.
# 🎯 Learning Objectives

This project is designed to help understand:

How LLMs tokenize text

How transformers process sequences

How causal attention works

How language models generate text

MiniLLM is a learning-focused implementation rather than a production LLM.

# ⚡ Future Improvements

Planned improvements:

Retrieval Augmented Generation (RAG)

Larger training datasets

Better tokenizer training

GPU training support

Evaluation benchmarks

Instruction tuning

# 🤝 Contributing

Contributions are welcome!

If you'd like to improve MiniLLM:

Open an issue

Submit a pull request

Suggest new features

# 📜 License

This project is released under the MIT License.

# ⭐ Acknowledgements

Inspired by research and open-source work including:

GPT architecture

Transformer models

PyTorch deep learning ecosystem

# 💡 MiniLLM demonstrates that you can build a working language model from scratch with only a few hundred lines of code.