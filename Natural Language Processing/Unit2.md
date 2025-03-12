# Language Syntax and Semantics
### Q1. Define Morphology? Explain stem and affix classes of morphemes with Example. [5]

### **Morphology in NLP**  
**Morphology** is the branch of linguistics(भाषाशास्त्र) that studies the structure and formation of words. It analyzes how words are formed from **morphemes**, which are the smallest units of meaning in a language.  

For example, the word **"unhappily"** consists of three morphemes:  
- **un-** (prefix) → meaning "not"  
- **happy** (root) → meaning "joyful"  
- **-ly** (suffix) → meaning "in a manner of" 

- Morrphes help in understanding the meaning and usage of words.
- Morphology helps in understanding the structure of words and how they are formed.


---

### **Stem and Affix Classes of Morphemes**  

1. **Stem (Root Morpheme)**  
   - The core part of a word that carries its fundamental meaning.  
   - It can exist independently or with affixes.  
   - Example:  
     - "play" → root of **playing, played, playful**  
     - "run" → root of **running, runner**  

2. **Affix (Bound Morpheme)**  
   - Morphemes that **cannot stand alone** and must be attached to a stem.  
   - Classified into:
     - **Prefix:** Added before the stem (e.g., *un*happy, *re*write)  
     - **Suffix:** Added after the stem (e.g., play*ing*, joy*ful*)  
     - **Infix:** Inserted within a word (not common in English)  
     - **Circumfix:** Attached at both ends of a word (common in German, e.g., *ge-komm-en*)  

🚀 **Morphology helps in NLP tasks like stemming, lemmatization, and text normalization!**

---

### Q2. Explain Derivational and Inflectional morphology in detail with suitable Example. [8]

### **Morphology in NLP**  
Morphology is the study of word structure and formation. It is divided into **Derivational Morphology** and **Inflectional Morphology**, both of which play a crucial role in Natural Language Processing (NLP) for tasks like **stemming, lemmatization, and text normalization**.  

---

### **1. Derivational Morphology**  
**Definition:**  
- It deals with the formation of new words by adding prefixes or suffixes to a base word.  
- It often **changes the meaning or grammatical category** of the word.  

**Characteristics:**  
✅ Creates a **new** word with a different meaning.  
✅ Often changes **part of speech** (noun → verb, adjective → noun, etc.).  
✅ Can be **prefixes** (re-, un-, dis-) or **suffixes** (-ness, -ly, -ment).  
✅ The new word may have an **unpredictable meaning**.  

**Examples:**  
| Base Word | Derivational Form | Meaning Change |
|-----------|------------------|----------------|
| **Act** (verb) | **Action** (noun) | Verb → Noun |
| **Happy** (adj) | **Happiness** (noun) | Adj → Noun |
| **Teach** (verb) | **Teacher** (noun) | Verb → Noun |
| **Like** (verb) | **Dislike** (verb) | Meaning changed (opposite) |

---

### **2. Inflectional Morphology**  
**Definition:**  
- It modifies a word to express **grammatical features** such as **tense, number, person, or comparison**.  
- It **does not change the word’s core meaning or part of speech**.  

**Characteristics:**  
✅ Does **not create a new word**, only modifies its form.  
✅ Does **not change part of speech** (noun remains noun, verb remains verb, etc.).  
✅ Used for **grammatical functions** like pluralization, tense, and comparison.  
✅ The number of **inflectional affixes is limited** (only 8 in English).  

**Examples of Inflectional Morphemes in English:**  
| Base Word | Inflected Form | Function |
|-----------|--------------|----------|
| **Book** (noun) | **Books** | Plural form |
| **Run** (verb) | **Running** | Present participle |
| **Play** (verb) | **Played** | Past tense |
| **Big** (adj) | **Bigger** | Comparative form |
| **Fast** (adj) | **Fastest** | Superlative form |



### **Application in NLP**  
- **Derivational Morphology** helps in **word segmentation, stemming, and lemmatization**.  
- **Inflectional Morphology** helps in **part-of-speech tagging, machine translation, and syntactic analysis**.  

🚀 **Both types of morphology are crucial for NLP tasks like speech recognition, text classification, and search engines!**

---

### Q3. ** Explain Morphological Parsing with Finite State Transducers (FST)**  

#### **What is Morphological Parsing?**  
Morphological parsing is the process of analyzing a word into its morphemes (smallest meaning units), identifying its **root word, affixes (prefixes, suffixes), and grammatical features**.  

For example, the word **"cats"** can be parsed as:  
- **Root:** "cat"  
- **Suffix:** "-s" (plural marker)  
- **Meaning:** Noun, plural form  

---

### **Finite State Transducers (FST) in Morphological Parsing**  
A **Finite State Transducer (FST)** is an extension of a **Finite State Automaton (FSA)** that maps **input symbols to output symbols**. It is widely used for morphological parsing.  

#### **How FST Works in Morphological Parsing?**  
- FST **takes an inflected word as input** and produces its **morpheme breakdown as output**.  
- It consists of **states and transitions**, where each transition **maps input symbols (characters/words) to output symbols (morphemes or grammatical features)**.  

---

### **Example: Morphological Parsing Using FST**  

Let's parse the word **"cats"** using an FST:  

#### **1. Finite State Representation**  
A basic **Finite State Transducer (FST)** can be represented as:

| Input  | Output    |
|--------|----------|
| cats   | cat + N + PL |

- "cats" → **cat** (root)  
- "-s" → **Noun + Plural (N + PL)**  

This means **"cats"** is broken down into its **base word (cat) and plural marker (-s)**.

---

### **FST Diagram for Parsing "cats"**  

```plaintext
(q0) --c--> (q1) --a--> (q2) --t--> (q3) --s--> (q4)
q0: Start
q4: Final (Output: cat + N + PL)
```

---

### **Applications of FST in NLP**  
✅ **Lemmatization** → Converts inflected words to their base form (*running → run*).  
✅ **Spell Checking** → Identifies incorrect word forms.  
✅ **Machine Translation** → Helps in language conversion by understanding word structure.  
✅ **Speech Recognition** → Maps spoken input to text with correct morphology.  

🚀 **FST is a powerful tool for handling complex word structures in NLP efficiently!**

---

### Q4.### **Syntactic Representations in Natural Language Processing (NLP)**  

Syntactic representation refers to the **structure of sentences** in a language, focusing on how words are arranged to convey meaning. It helps in **understanding grammar, parsing sentences, and analyzing relationships between words**.  

---

### **Types of Syntactic Representations**  

1. **Constituency Grammar (Phrase Structure Trees)**  
   - Represents **sentence structure using hierarchical tree diagrams**.  
   - Based on **Phrase Structure Grammar (PSG)** or **Context-Free Grammar (CFG)**.  
   - Example: **"The cat sleeps."**  

     **Parse Tree Representation:**  
     ```
           S
          /  \
        NP   VP
       /  \    \
      Det  N    V
      The  cat sleeps
     ```
   - **Applications:** Used in **syntax parsing, machine translation, and text-to-speech systems**.

---

2. **Dependency Grammar (Dependency Trees)**  
   - Represents **grammatical relationships** between words using a directed graph.  
   - Words (nodes) are connected by directed edges that show dependencies.  
   - Example: **"The cat sleeps."**  

     **Dependency Tree Representation:**  
     ```
     sleeps
       |
       cat
      /   
    The
     ```
   - **Applications:** Used in **information extraction, sentiment analysis, and question answering systems**.

---

3. **Combinatory Categorial Grammar (CCG)**  
   - A type of grammar that assigns **syntactic categories** to words.  
   - Helps in **word sense disambiguation and semantic parsing**.  
   - Example:  
     ```
     The (Det)  cat (N)  sleeps (V)
     ```

---

4. **Tree-Adjoining Grammar (TAG)**  
   - A formalism that captures **long-distance dependencies**.  
   - Useful for **handling complex sentences and linguistic phenomena** like relative clauses.  

---

### **Applications of Syntactic Representations in NLP**  
✅ **Syntax Parsing** → Helps in understanding sentence structure.  
✅ **Machine Translation** → Translates text while preserving grammar rules.  
✅ **Speech Recognition** → Analyzes spoken sentences for better accuracy.  
✅ **Chatbots & Question Answering** → Understands user queries grammatically.  

🚀 **Syntactic representations are crucial for making NLP systems understand human language effectively!**

---


### Q5. What is Probabilistic context-free grammars? State the benefits of probabilistic parsing. [7]

### **Probabilistic Context-Free Grammars (PCFGs)**  

#### **What is PCFG?**  
A **Probabilistic Context-Free Grammar (PCFG)** is an **extension of Context-Free Grammar (CFG)** where each production rule is assigned a probability. These probabilities help in choosing the **most likely parse tree** for a given sentence.  

#### **Structure of PCFG**  
A PCFG consists of:  
1. **A set of non-terminal symbols (N)** → Represents sentence components (e.g., S for sentence, NP for noun phrase).  
2. **A set of terminal symbols (Σ)** → Represents words (e.g., "cat", "sleeps").  
3. **A set of production rules (R)** → Defines how non-terminals expand into terminals or other non-terminals.  
4. **A start symbol (S)** → The root of the parse tree.  
5. **Probabilities assigned to each rule** → The likelihood of applying a rule.  

#### **Example of PCFG**  
### **Simple Example of PCFG**  

Consider the sentence: **"The cat sleeps."**  

#### **Grammar Rules with Probabilities:**  
1. A **sentence (S)** consists of a **noun phrase (NP)** and a **verb phrase (VP)** → **(Probability = 1.0)**  
2. A **noun phrase (NP)** consists of a **determiner (Det)** and a **noun (N)** → **(Probability = 0.8)**  
3. A **verb phrase (VP)** consists of a **verb (V)** → **(Probability = 1.0)**  
4. The word **"The"** is a **determiner (Det)** → **(Probability = 1.0)**  
5. The word **"cat"** is a **noun (N)** → **(Probability = 0.6)**  
6. The word **"sleeps"** is a **verb (V)** → **(Probability = 1.0)**  

#### **Calculating Sentence Probability:**  
- **Probability of NP (The cat):** \( 0.8 \times 1.0 \times 0.6 = 0.48 \)  
- **Probability of VP (sleeps):** \( 1.0 \times 1.0 = 1.0 \)  
- **Total Sentence Probability:** \( 1.0 \times 0.48 \times 1.0 = 0.48 \)  

Thus, **PCFG helps select the most probable sentence structure in NLP.**

---

### **Benefits of Probabilistic Parsing**  
✅ **Handles Ambiguity** → PCFG helps resolve syntactic ambiguity by selecting the most likely parse tree.  
✅ **Improves NLP Accuracy** → Used in **machine translation, speech recognition, and syntactic parsing**.  
✅ **Ranks Multiple Parse Trees** → Assigns probabilities to different parses and selects the best one.  
✅ **Better Real-world Language Modeling** → Helps deal with **incomplete, noisy, or informal sentences**.  

🚀 **PCFG is widely used in NLP applications like machine translation, speech processing, and AI-driven chatbots!**

---

### Q6. What are different techniques for the semantic analysis for statement
  

Semantic analysis focuses on **understanding the meaning** of a statement in Natural Language Processing (NLP). The key techniques include:  

---

### **1. Lexical Semantics**  
- Analyzes the meaning of individual words.  
- Uses **synonyms, antonyms, and word sense disambiguation** to determine word meaning.  
- **Example:** The word *"bank"* can mean **a financial institution** or **a riverbank**, depending on the context.  

---

### **2. Syntax-Driven Semantic Analysis**  
- Uses **grammar rules** to derive meaning based on sentence structure.  
- Helps in **parsing sentences** and associating words correctly.  
- **Example:**  
  - "He ate a cake." ✅ (Valid meaning)  
  - "He ate the happiness." ❌ (Incorrect meaning due to syntax rules).  

---

### **3. Named Entity Recognition (NER)**  
- Identifies **proper nouns, locations, organizations, dates, etc.**  
- **Example:** In **"Apple Inc. released a new iPhone in California."**,  
  - **Apple Inc.** → Organization  
  - **California** → Location  

---

### **4. Word Sense Disambiguation (WSD)**  
- Determines the **correct meaning of a word** in context.  
- **Example:**  
  - *"He went to the **bank** to deposit money."* (Bank = Financial Institution)  
  - *"He sat by the **bank** of the river."* (Bank = Riverbank)  

---

### **5. Semantic Role Labeling (SRL)**  
- Identifies the roles of words in a sentence (who did what to whom).  
- **Example:**  
  - *"John gave Mary a book."*  
  - **John** → Giver (Agent)  
  - **Mary** → Receiver  
  - **Book** → Object  

---

### **6. Ontology-Based Analysis**  
- Uses a **hierarchical knowledge base** to understand relationships between words.  
- Example: **"Dog"** is a type of **"Animal"**, which is a type of **"Living Being"**.  

---

### **7. Distributional Semantics (Vector-Based Methods)**  
- Uses **Word Embeddings** (Word2Vec, GloVe) to find relationships between words.  
- Example: **"King - Man + Woman = Queen"** (Word Vector Similarity).  

---

### **Conclusion:**  
🔹 Semantic analysis helps machines **understand meaning** for **chatbots, search engines, and machine translation**.  
🔹 Techniques like **WSD, NER, and SRL** are widely used in NLP applications. 🚀

---
 
### Q7. Explain with suitable examples following relationship between word meanings, 1. Homonymy 2. Polysemy 3. Synonymy 4. Hyponymy 5. Antonymy 6. Hypernomy 7. Meronomy [7]

### **Relationships Between Word Meanings with Examples**  

1️⃣ **Homonymy**  
- Words that **sound or look the same** but have **different meanings**.  
- **Example:**  
  - **"Bat"** (a flying animal) 🦇  
  - **"Bat"** (used in cricket) 🏏  

---

2️⃣ **Polysemy**  
- A single word having **multiple related meanings**.  
- **Example:**  
  - **"Head"** (of a person) 👤  
  - **"Head"** (of a company) 🏢  

---

3️⃣ **Synonymy**  
- Words that have **the same or similar meanings**.  
- **Example:**  
  - **"Big"** = **"Large"**  
  - **"Happy"** = **"Joyful"**  

---

4️⃣ **Hyponymy**  
- A word that represents a **subcategory** of a broader category.  
- **Example:**  
  - **"Rose"** 🌹 is a hyponym of **"Flower"** 🌸  
  - **"Car"** 🚗 is a hyponym of **"Vehicle"** 🚙  

---

5️⃣ **Antonymy**  
- Words with **opposite meanings**.  
- **Example:**  
  - **"Hot"** ❄️ vs **"Cold"** 🔥  
  - **"Fast"** 🚀 vs **"Slow"** 🐢  

---

6️⃣ **Hypernymy**  
- A word that represents a **broader category** for specific words (opposite of hyponymy).  
- **Example:**  
  - **"Bird"** 🦜 is a hypernym of **"Parrot"**  
  - **"Furniture"** 🛋️ is a hypernym of **"Chair"**  

---

7️⃣ **Meronymy**  
- A word that denotes a **part of something larger**.  
- **Example:**  
  - **"Wheel"** is a meronym of **"Car"**  
  - **"Leaf"** is a meronym of **"Tree"** 🌳  

---

### **Conclusion:**  
These relationships help in **semantic analysis** and improve **NLP applications** like **search engines, chatbots, and language understanding**. 🚀

---

### Q8. Explain CFG with suitable example. [5]


### **Context-Free Grammar (CFG) with Example**  

#### **What is CFG?**  
Context-Free Grammar (CFG) is a set of rules used to define the structure of sentences in a language. It consists of:  

1. **Non-Terminals (N):** Symbols like **S (Sentence), NP (Noun Phrase), VP (Verb Phrase)**.  
2. **Terminals (Σ):** Actual words like **"cat", "dog", "runs"**.  
3. **Start Symbol (S):** The main symbol from which a sentence is formed.  
4. **Production Rules (R):** Rules that define how sentences are created.  

---

### **Example of CFG**  

Consider a simple English sentence: **"The cat chases the dog."**  

#### **CFG Rules:**  
1. **S → NP VP** (A sentence consists of a Noun Phrase + Verb Phrase)  
2. **NP → Det N** (A Noun Phrase consists of a Determiner + Noun)  
3. **VP → V NP** (A Verb Phrase consists of a Verb + Noun Phrase)  
4. **Det → "The"**  
5. **N → "cat" | "dog"**  
6. **V → "chases"**  

---

### **How the Sentence is Formed?**  

1. **Start with S:** → **NP VP**  
2. **Expand NP:** → **Det N**  
3. **Expand VP:** → **V NP**  
4. **Replace Words:**  
   - Det → **"The"**  
   - N → **"cat"**  
   - V → **"chases"**  
   - NP → **Det N** → **"The dog"**  

So, the sentence formed is:  
👉 **"The cat chases the dog."**  

---

### **Why is CFG Important?**  
✔ Used in **NLP** to check grammar and sentence structure.  
✔ Helps in **chatbots, machine translation, and voice assistants**.

### Q8. Derive a top-down, depth-first, left-to-right parse tree for the given
sentence: [7]
The angry bear chased the frightened little squirrel
Use the following grammar rules to derive the parse tree:


### **Parse Tree for the Sentence**  
👉 **"The angry bear chased the frightened little squirrel."**  

#### **Given Grammar Rules:**  
1. **S → NP VP**  
2. **NP → Det Nom**  
3. **VP → V NP**  
4. **Nom → Adj Nom | N**  
5. **Det → "The" | "the"**  
6. **Adj → "little" | "angry" | "frightened"**  
7. **N → "squirrel" | "bear"**  
8. **V → "chased"**  

---

### **Step-by-Step Breakdown**  

1. **Start with S:**  
   - S → NP VP  

2. **Expand NP (Subject - "The angry bear"):**  
   - NP → Det Nom  
   - Det → "The"  
   - Nom → Adj Nom  
   - Adj → "angry"  
   - Nom → "bear"  

3. **Expand VP (Verb Phrase - "chased the frightened little squirrel"):**  
   - VP → V NP  
   - V → "chased"  

4. **Expand NP (Object - "the frightened little squirrel"):**  
   - NP → Det Nom  
   - Det → "the"  
   - Nom → Adj Nom  
   - Adj → "frightened"  
   - Nom → Adj Nom  
   - Adj → "little"  
   - Nom → "squirrel"  

---

### **Final Parse Tree Structure (Simplified View)**  

```
       S
      /  \
    NP    VP
   /  \   /   \
 Det  Nom V    NP
  |   /  \ |   /  \
The Adj  Nom chased Det Nom
    |    /  \   |   /   \
  angry N   Adj Nom Adj  N
       |    |   /   \   |
      bear fright. Adj  squirrel
              |    |
           little squirrel
```

---

### **Summary**  
✔ We started with **S → NP VP** and expanded each part step by step.  
✔ The **subject NP** ("The angry bear") and **object NP** ("the frightened little squirrel") were broken down into smaller components.  
✔ This parse tree helps **analyze sentence structure** in NLP. 🚀