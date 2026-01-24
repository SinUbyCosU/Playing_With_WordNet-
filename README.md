# WordNet Learning Journey

A structured approach to learning WordNet - the lexical database for English.

## Learning Goals
Master WordNet fundamentals and advanced concepts for natural language processing tasks.

---

## Daily Progress

### Day 1: Synsets Basics
**Date:** January 21, 2026

**Topics Covered:**
- Introduction to Synsets (Synonym Sets)
- Understanding synset structure
- Accessing synset information (name, definition, examples)
- Working with lemmas
- Basic synset operations

**Key Concepts:**
- `wn.synsets('word')` - Get all synsets for a word
- `synset.definition()` - Get meaning
- `synset.examples()` - Get usage examples
- `synset.lemmas()` - Get words in the synset
- `synset.pos()` - Get part of speech

**Practice Done:**
- Explored different meanings of words
- Analyzed synset structure
- Worked with real examples

**Notes:**
- Synsets group words by meaning, not just similarity
- Same word can have multiple synsets (different meanings)
- Each synset represents one specific sense/meaning

---

### Day 2: POS Tagging
**Date:** January 25, 2026

**Topics Covered:**
- Part-of-Speech (POS) tagging fundamentals
- NLTK POS tagger implementation
- Analyzing ambiguous words in corpora
- Working with Brown corpus
- Understanding conditional frequency distributions

**Key Concepts:**
- `nltk.pos_tag(tokens)` - Tag words with parts of speech
- `brown.tagged_words()` - Get pre-tagged corpus data
- `ConditionalFreqDist` - Track tag frequencies per word
- POS tags: PRP (pronoun), VBZ (verb), NN (noun), JJ (adjective), etc.
- Ambiguous words - words that can serve multiple grammatical roles

**Practice Done:**
- Tagged a sample sentence
- Analyzed Brown corpus news section
- Found ambiguous words (words with multiple possible tags)
- Calculated percentage of ambiguous words

**Code Highlights:**
```python
# Basic POS tagging
text = nltk.word_tokenize("she sells seashells on the seashore")
print(nltk.pos_tag(text))

# Finding ambiguous words
brown_news_tagged = brown.tagged_words(categories='news')
data = nltk.ConditionalFreqDist((word.lower(), tag) for (word, tag) in brown_news_tagged)
```

**Notes:**
- POS tagging is crucial for understanding sentence structure
- Many words are ambiguous - meaning depends on context
- Brown corpus provides pre-tagged text for analysis
- The code shows 10 example ambiguous words then calculates a ratio
- Examples of ambiguous words: "primary" (NN/JJ), "said" (VBD/VBN)

---

### Day 3:
**Date:**

**Topics Covered:**


---

## Resources
- NLTK Documentation: https://www.nltk.org/
- WordNet Documentation: https://wordnet.princeton.edu/
- NLTK WordNet Interface: https://www.nltk.org/howto/wordnet.html

## Setup
```bash
pip install nltk
```

```python
import nltk
nltk.download('wordnet')
nltk.download('omw-1.4')
nltk.download('averaged_perceptron_tagger_eng')
nltk.download('punkt')
nltk.download('brown')
```

## Files
- `Word_Net_1.py` - Day 1: Synsets Basics
- `POS.py` - Day 2: Part-of-Speech Tagging Demo
- More files to be added as learning progresses...
