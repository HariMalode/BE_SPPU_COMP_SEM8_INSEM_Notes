# Introduction to Natural Language Processing

### Q1. What is Natural Language Processing(NLP)? Discuss various stages involved in NLP process with suitable example. [8]

### **Natural Language Processing (NLP)**  
- Natural Language Processing (NLP) is a subfield of artificial intelligence (AI) that enables computers to understand, interpret, and generate human language.
- It involves the development of algorithms and techniques to process and analyze human language data.
- NLP has a wide range of applications, including machine translation, sentiment analysis, chatbots, and more.
- It combines elements of linguistics, computer science, and statistics to enable computers to understand and interact with human language.

### **Stages Involved in NLP Process**  

The NLP process consists of several key stages:  

1. **Tokenization**  
   - Breaking text into individual words or sentences.  
   - Example: `"Natural Language Processing"` → `["Natural", "Language", "Processing"]`  

2. **Stopword Removal**  
   - Removing common words like "is," "the," "and" that do not contribute to meaning.  
   - Example: `"I love to play football"` → `["love", "play", "football"]`  

3. **Stemming and Lemmatization**  
   - **Stemming**: Reducing words to their root form.  
     - Example: `"running", "runs", "ran"` → `"run"`  
   - **Lemmatization**: Mapping words to their dictionary base form.  
     - Example: `"better"` → `"good"`  

4. **Part-of-Speech (POS) Tagging**  
   - Assigning grammatical tags to words.  
   - Example: `"The cat sits on the mat."` → `[("The", ARTICLE), ("cat", NOUN), ("sits", VERB)]`  

5. **Named Entity Recognition (NER)**  
   - Identifying entities like names, locations, and dates.  
   - Example: `"Apple Inc. is based in California."` → `[("Apple Inc.", ORG), ("California", LOC)]`  

6. **Sentiment Analysis**  
   - Determining the sentiment of a text (positive, negative, or neutral).  
   - Example: `"I love this product!"` → `Positive Sentiment`  

7. **Text Summarization**  
   - Generating a concise summary of a large text.  
   - Example: `"The article discusses climate change effects..."` → `"Climate change impacts discussed."`  

8. **Machine Translation**  
   - Translating text from one language to another.  
   - Example: `"Hello"` → `"Bonjour" (French)`  

These stages enable various NLP applications like chatbots, search engines, and speech recognition systems. 🚀

---


### Q2. Differentiate between Natural languages and Programming languages. [7]

### **Difference between Natural Languages and Programming Languages**  

| Feature            | Natural Language | Programming Language |
|--------------------|----------------|----------------------|
| **Definition**     | Language used for human communication (e.g., English, Hindi). | Language used to communicate with computers (e.g., Python, Java). |
| **Structure**      | Flexible, ambiguous, and context-dependent. | Strict syntax and structure with predefined rules. |
| **Grammar Rules**  | Complex, varies across languages, and often ambiguous. | Well-defined and follows precise grammar and syntax. |
| **Interpretation** | Depends on context, tone, and culture. | Unambiguous, interpreted exactly as written. |
| **Evolution**      | Evolves naturally over time through social use. | Designed and updated systematically by developers. |
| **Processing**     | Understood by humans and requires cognitive interpretation. | Understood by computers and follows logical execution. |
| **Example**       | "Can you pass me the book?" | `print("Hello, World!")` |
| **Error Tolerance** | Can tolerate grammatical errors and still convey meaning. | Even a small syntax error can lead to program failure. |
| **Purpose**        | Used for everyday communication, literature, and expression. | Used to create software, automate tasks, and control systems. |

Natural languages are used for human communication, whereas programming languages provide instructions for computers in a structured and precise manner. 🚀

---

### Q3. Explain Tokenization with it's different types. [5]

### **Tokenization in NLP**  
- Tokenization is the process of splitting a text into smaller units called **tokens**.
- These tokens can be words, sentences, or subwords, depending on the level of tokenization.
- It is a fundamental step in NLP as it helps in text processing and analysis.
- Tokenization is crucial for tasks like text classification, sentiment analysis, and machine translation.


---

### **Types of Tokenization**  

1. **Word Tokenization**  
   - Splits text into individual words.  
   - Example: `"Natural Language Processing is amazing!"`  
     - **Tokens**: `["Natural", "Language", "Processing", "is", "amazing", "!"]`

2. **Sentence Tokenization**  
   - Splits text into individual sentences.  
   - Example: `"Hello! How are you? I am fine."`  
     - **Tokens**: `["Hello!", "How are you?", "I am fine."]`

3. **Subword Tokenization**  
   - Breaks words into smaller meaningful units, especially useful for handling unknown words.  
   - Used in **Byte Pair Encoding (BPE), WordPiece, and SentencePiece**.  
   - Example: `"unhappiness"`  
     - **Tokens**: `["un", "happi", "ness"]`

4. **Character Tokenization**  
   - Splits text into individual characters.  
   - Example: `"NLP"`  
     - **Tokens**: `["N", "L", "P"]`  
   - Useful for text with many typos or for languages without clear word boundaries.

---

### **Importance of Tokenization**  
- Helps in text preprocessing for NLP models.  
- Reduces complexity by converting raw text into structured format.  
- Used in machine translation, sentiment analysis, and text summarization.  

🚀 **Tokenization is the first step in making text understandable for computers!**

---

### Q4. What do you mean by part-of-speech Tagging? What is the need of this task in NLP. [5]

### **Part-of-Speech (POS) Tagging**  
- Part-of-Speech (POS) Tagging is the process of assigning grammatical categories (such as noun, verb, adjective, etc.) to words in a sentence based on their context and usage. 
- It is a crucial step in Natural Language Processing (NLP) as it provides valuable information about the structure and meaning of a sentence.  
- POS tagging is essential for tasks like named entity recognition, sentiment analysis, and machine translation.

#### **Example:**  
Sentence: `"The quick brown fox jumps over the lazy dog."`  
POS Tags:  
- `The (DET)`  
- `quick (ADJ)`  
- `brown (ADJ)`  
- `fox (NOUN)`  
- `jumps (VERB)`  
- `over (PREP)`  
- `the (DET)`  
- `lazy (ADJ)`  
- `dog (NOUN)`

---

### **Need for POS Tagging in NLP**  

1. **Word Sense Disambiguation**  
   - Helps determine the correct meaning of a word based on its usage.  
   - Example: `"I saw a bat."` (bat = animal or sports equipment?)  

2. **Grammer Parsing**  
   - Helps in analyzing sentence structure for grammar checking and parsing.  

3. **Information Retrieval**  
   - Improves search engines by understanding the role of words in queries.  

4. **Speech Recognition & Text-to-Speech**  
   - Helps in pronunciation and speech synthesis by identifying word roles.  

5. **Machine Translation**  
   - Ensures accurate translations by understanding grammatical relationships.  

6. **Sentiment Analysis**  
   - Identifies adjectives and adverbs to determine sentiment in a text.

7. **Named Entity Recognition**
   - Helps in identifying and classifying named entities (people, places, organizations) in text.

   8. **Text Summarization**
   - Helps in summarizing text by identifying key phrases and sentences.

   9. **Question Answering**
   - Helps in answering questions by understanding the context and relationships between words.

🚀 **POS Tagging is a crucial step in NLP for understanding sentence structure and meaning!**

---

### Q5 Discuss the challenges of Natural Language Processing. [7] OR Why NLP is hard? 

### **Challenges in Natural Language Processing (NLP)**  

NLP faces several challenges due to the complexity and variability of human language. Some of the key challenges include:  

1. **Ambiguity**  
   - Words or sentences can have multiple meanings.  
   - Example: `"I saw the man with the telescope."` (Who has the telescope?)  

2. **Synonyms and Polysemy**  
   - Different words can have the same meaning (**synonyms**), and one word can have multiple meanings (**polysemy**).  
   - Example: `"bank"` (financial institution) vs. `"bank"` (riverbank).  

3. **Grammar and Syntax Variations**  
   - Different languages and dialects have varied grammatical rules.  
   - Example: `"He go to school"` (incorrect grammar but understandable).  

4. **Sarcasm and Irony**  
   - Difficult to detect tone and intent from text.  
   - Example: `"Oh great, another meeting!"` (Positive or Negative?).  

5. **Named Entity Recognition (NER) Issues**  
   - Identifying names of people, places, or organizations correctly.  
   - Example: `"Apple is launching a new product."` (Company vs. Fruit?).  

6. **Lack of Context Understanding**  
   - Words depend on surrounding text for meaning.  
   - Example: `"She didn't *bank* on losing the job."` (Here, "bank" means "expect").  

7. **Code-Switching and Multilingual Text**  
   - Users often mix languages in the same sentence.  
   - Example: `"Mujhe coffee *chahiye* now!"` (Hindi + English).  

8. **Data Sparsity and Low-Resource Languages**  
   - Some languages have limited labeled data for training NLP models.  

9. **Real-Time Processing**  
   - Handling large-scale text data efficiently in real-time applications.  

10. **Bias in NLP Models**  
   - AI models may inherit biases from training data, leading to unfair outcomes.  

🚀 **Overcoming these challenges requires better linguistic models, larger datasets, and improved deep learning techniques!**

### Q6. Explain finite automata with suitable example. [5]

### **Finite Automata in NLP**  

- A **Finite Automaton (FA)** is a mathematical model used in Natural Language Processing (NLP) to represent and process sequences of symbols, such as words and sentences.
- It is useful for **lexical analysis, pattern recognition, and syntactic parsing**.
- FA consists of **states**, **transitions**, and an **initial state**.
- It can be **deterministic** or **non-deterministic**.
- **States** represent different stages in the processing of a sequence.
- **Transitions** are the transitions between states based on input symbols.
- **Initial State** is the starting point of the automaton.
---

### **Types of Finite Automata**  

1. **Deterministic Finite Automaton (DFA)**  
   - Each state has exactly **one** transition for each input symbol.  
   - Used in **tokenization** and **keyword recognition**.  
   
2. **Non-Deterministic Finite Automaton (NFA)**  
   - A state can have **multiple transitions** for the same input symbol.  
   - Used in **pattern matching** and **regular expression processing**.  

---

### **Example: DFA for Identifying Simple English Words**  

Consider a DFA that recognizes the word **"chat"**:  

#### **States & Transitions**
- **q0** → Start State  
- **q1** → Reads 'c'  
- **q2** → Reads 'h'  
- **q3** → Reads 'a'  
- **q4** → Reads 't' (Final State ✅)  

| Current State | Input | Next State |
|--------------|------|-----------|
| q0           | c    | q1        |
| q1           | h    | q2        |
| q2           | a    | q3        |
| q3           | t    | q4 (Final) |

---

### **Applications of Finite Automata in NLP**
1. **Lexical Analysis**  
   - Used in tokenization to identify words, numbers, and punctuation.  

2. **Spell Checking**  
   - Detects incorrect words by checking valid transitions in a dictionary-based FA.  

3. **Named Entity Recognition (NER)**  
   - Identifies entities like names, locations, and dates using finite-state machines.  

4. **Regular Expressions**  
   - Pattern matching in search engines and text editors.  

5. **Text Parsing**  
   - Used in syntax checking and part-of-speech tagging.  

🚀 **Finite automata provide the foundation for efficient text processing in NLP!**