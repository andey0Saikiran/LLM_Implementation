# GPT Model from Scratch

This repository contains an implementation of a GPT model from scratch, covering everything from tokenization to text generation. The project follows a structured approach, highlighting key learning steps and implementation details.

## Key Learnings & Implementation Steps

### 1. Tokenization
#### **Step 1: Reading the Verdict Text**
- Loaded a text file containing a legal verdict.

#### **Step 2: Tokenization**
- Used regular expressions to split text into meaningful tokens.
- Preprocessed the tokens by removing unnecessary spaces and normalizing punctuation.

#### **Step 3: Creating Token IDs**
- Constructed a vocabulary where each token is mapped to a unique integer.

#### **Step 4: Implementing a Simple Tokenizer**
- Developed a class to encode text into token IDs and decode token IDs back into readable text.
- Included logic to handle spacing before punctuation.

### 2. Byte Pair Encoding (BPE)
#### **Step 1: Applying BPE Algorithm**
- Implemented a frequency-based subword tokenization technique.
- Merged frequently occurring character pairs iteratively to improve efficiency.

### 3. Data Preparation
#### **Step 1: Creating Input-Target Pairs**
- Prepared sequences where the input is a text segment, and the target is the next word.

#### **Step 2: Implementing a Data Loader**
- Tokenized the entire text.
- Used a **sliding window technique** to generate overlapping text sequences.
- Defined dataset properties to return the number of rows and fetch a specific data row when needed.

### 4. Embeddings
#### **Step 1: Implementing Token Embeddings**
- Converted token IDs into dense vector representations for better semantic understanding.

#### **Step 2: Adding Positional Embeddings**
- Incorporated positional encodings to retain the order of words within a sequence.

### 5. Attention Mechanisms
#### **Step 1: Simplified Attention Mechanism**
- Designed an attention mechanism to compute importance scores for tokens.

#### **Step 2: Implementing Self-Attention with Trainable Weights**
- Introduced learnable weight matrices to enhance context awareness.

#### **Step 3: Creating a Compact Self-Attention Class**
- Encapsulated self-attention logic in a reusable class.

#### **Step 4: Implementing Causal Attention**
- Modified self-attention to prevent tokens from attending to future words.

#### **Step 5: Extending Single-Head Attention to Multi-Head Attention**
- Implemented multiple attention heads to capture diverse relationships between tokens.

### 6. Transformer Block & GPT Model
#### **Step 1: Implementing Multi-Head Attention with Weights**
- Extended self-attention to use multiple independent attention heads.

#### **Step 2: Implementing GPT Architecture (Part 1: Dummy GPT Model)**
- Created a simple version of a GPT model with embeddings and attention layers.

#### **Step 3: Adding Layer Normalization**
- Integrated normalization layers to stabilize model training.

#### **Step 4: Implementing Feedforward Neural Network with GELU Activation**
- Used the GELU activation function for improved performance.

#### **Step 5: Adding Shortcut (Residual) Connections**
- Implemented skip connections to improve gradient flow and training stability.

#### **Step 6: Implementing Attention and Linear Layers in a Transformer Block**
- Combined all previous elements into a modular transformer block.

### 7. Full GPT Model Implementation
#### **Step 1: Assembling the Complete GPT Architecture**
- Integrated embedding layers, multi-head attention, feedforward layers, and normalization into a full GPT model.

#### **Step 2: Generating Text from Output Tokens**
- Used the trained model to generate coherent text sequences.


