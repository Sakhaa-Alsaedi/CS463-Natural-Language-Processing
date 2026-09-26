
# CS463 — Natural Language Processing
<img width="2172" height="724" alt="Image" src="https://github.com/user-attachments/assets/650b6303-1fae-4cce-a001-31f9b25d71d1" />

Welcome to the CS463 course repository. It brings together lecture slides, hands-on labs, Jupyter/Google Colab notebooks, shell exercises, and selected readings for natural language processing. The course introduces both theory and practice in programs that understand, generate, translate, and extract information from written language. It compares conventional and statistical techniques, then applies them to question answering, summarization, and machine translation. Arabic examples are included throughout where appropriate.

**College of Computer Science and Engineering · Taibah University**  
**Term:** Fall 2026–1448 · **Credit hours:** 3 · **Prerequisite:** CS362  
**Instructor:** Dr. Sakhaa Alsaedi · **Email:** [sbssaedi@taibahu.edu.sa](mailto:sbssaedi@taibahu.edu.sa)  
**Office hours:** Monday, 12:30–1:30 PM · Wednesday, 1:40–2:40 PM

> **Course materials:** Slides and course-authored notebooks will be linked as they are added. The external resources below are supplementary learning materials. Check the official course platform for submission instructions and assessment dates.

## Course goals

By the end of the course, students should be able to:

- Explain the goals and core concepts of NLP and describe how language relates to AI, knowledge representation, and inference.
- Interpret linguistic properties using descriptive and theoretical frameworks.
- Apply fundamental algorithms and programming tools to build and assess systems for text-based language processing.
- Work responsibly in a team and communicate technical ideas clearly in writing and presentations.

The course assumes prior knowledge of programming and fundamental intelligent systems. Teaching combines interactive lectures and lab sessions.

## Start here

1. Open the current week's slides when they are posted in `slides/`.
2. Open the corresponding `.ipynb` file from `notebooks/` in Jupyter or Google Colab. For a notebook hosted on GitHub, use Colab's **File → Open notebook → GitHub** option and paste its repository URL.
3. Follow the lab instructions and complete the exercises yourself.
4. Use the selected readings to review concepts and prepare for the journal club.

## Suggested repository layout

```text
.
├── README.md
├── slides/             # Weekly lecture slides
├── notebooks/          # Python and Colab labs (.ipynb)
├── shell-labs/         # Terminal commands, sample input, and instructions
├── data/               # Small teaching datasets, where redistribution is permitted
├── journal-club/       # Paper list and presentation guidance
└── resources/          # Additional course handouts
```

The folder names describe where to place future materials; they do not imply that those files have already been uploaded.

## Weekly lectures and labs

| Week and lecture | Lab name | Lab activity | Supplementary resource |
|---|---|---|---|
| **1 — Introduction to NLP** | Explore a corpus | Inspect sentences, tokens, vocabulary, and word frequencies in English and Arabic text. | [NLTK: Language Processing and Python](https://www.nltk.org/book/ch01.html) |
| **2 — Regular expressions** | Text patterns in shell and Python | Extract dates, emails, and hashtags with `grep` and Python `re`; compare matches and Unicode behavior. | [NLTK: Processing Raw Text](https://www.nltk.org/book/ch03.html) |
| **3 — Morphology** | Analyze Arabic words | Compare stemming, lemmatization, and morphological analyses with CAMeL Tools. Try its command-line utilities and guided Colab. | [CAMeL CLI documentation](https://camel-tools.readthedocs.io/en/latest/cli_tools.html) · [CAMeL guided Colab](https://colab.research.google.com/drive/1Y3qCbD6Gw1KEw-lixQx1rI6WlyWnrnDS) |
| **4 — Language models** | Build a bigram model | Count n-grams, estimate next-word probabilities, generate short text, and compare with a pretrained model. | [NLTK: Corpora and conditional frequency distributions](https://www.nltk.org/book/ch02.html) · [Hugging Face: Causal language modeling](https://huggingface.co/docs/transformers/en/tasks/language_modeling) |
| **5 — Part-of-speech tagging I** | Tag from the terminal | Run a command-line POS tagger on a text file and inspect ambiguous words and tag labels. | [Stanford CoreNLP: POS tagging](https://stanfordnlp.github.io/CoreNLP/pos.html) · [Command-line setup](https://stanfordnlp.github.io/CoreNLP/cmdline.html) |
| **6 — Part-of-speech tagging II** | Evaluate taggers | Compare baseline, unigram, and n-gram taggers in a notebook; calculate accuracy and inspect errors. | [NLTK: Categorizing and Tagging Words](https://www.nltk.org/book/ch05.html) · [spaCy linguistic features](https://spacy.io/usage/linguistic-features) |
| **7 — First midterm** | — | No regular lab. | — |
| **8 — Hidden Markov models** | Viterbi decoding | Calculate transition and emission probabilities for a small tagging example, then implement Viterbi step by step. | [NLTK tagging chapter](https://www.nltk.org/book/ch05.html) |
| **9 — Syntactic and statistical parsing** | Parse ambiguous sentences | Build CFG and PCFG examples; compare parse trees and visualize dependencies. | [NLTK: Analyzing Sentence Structure](https://www.nltk.org/book/ch08.html) · [spaCy visualizers](https://spacy.io/usage/visualizers) |
| **10 — Lexical and statistical semantics** | Compare meanings | Examine WordNet senses and similarity; compare context-sensitive sentence representations. | [NLTK: Lexical Resources](https://www.nltk.org/book/ch02.html) · [Meaning of Sentences](https://www.nltk.org/book/ch10.html) |
| **11 — Second midterm** | — | No regular lab. | — |
| **12 — Computational discourse** | Track references | Resolve pronouns and entities across sentences; inspect a discourse representation. | [NLTK discourse examples](https://www.nltk.org/howto/drt.html) |
| **13 — Question answering and summarization** | Answer and summarize | Apply models to a supplied passage; compare answers and summaries with the source for factual accuracy. | [Hugging Face: Question answering](https://huggingface.co/learn/llm-course/chapter7/7) · [Summarization](https://huggingface.co/learn/llm-course/en/chapter7/5) |
| **14 — Machine translation** | Translate and evaluate | Translate short English–Arabic examples and analyze errors in meaning, morphology, and word order. | [Hugging Face: Translation](https://huggingface.co/learn/llm-course/en/chapter7/4?fw=pt) |
| **15 — Speech processing** | Transcribe and synthesize | Transcribe a short recording, inspect recognition errors, and demonstrate text-to-speech. | [Hugging Face Audio Course](https://huggingface.co/learn/audio-course/chapter0/introduction) · [SpeechBrain tutorials](https://speechbrain.readthedocs.io/en/v1.0.1/tutorials.html) |

## Shell-based activities

Some labs use terminal commands alongside notebooks. This helps students see each processing step and work with text files directly.

```bash
# Inspect a UTF-8 text file and locate lines containing a pattern.
wc -l data/sample.txt
grep -n 'pattern' data/sample.txt

# After installing Stanford CoreNLP and its models, run from its configured environment:
java edu.stanford.nlp.pipeline.StanfordCoreNLP -annotators tokenize,pos -file input.txt
```

The sample paths above are illustrative. Use the files supplied with the relevant lab. The CoreNLP command requires its Java package and models to be installed first. For Arabic morphology, follow the [CAMeL Tools command-line guide](https://camel-tools.readthedocs.io/en/latest/cli_tools.html).

## Journal club

Each student selects one paper for a **15-minute presentation**, followed by **5 minutes of questions**. Presentations take place during the final 20 minutes of class on the dates shown in the tracker. Add your name in its highlighted student column.

- [Journal club paper selection and presentation tracker](https://taibahuniv-my.sharepoint.com/:x:/g/personal/sbssaedi_taibahu_edu_sa/IQCBBFIzs7bdQ6adCq21BTC_AZ3e33sRmZTyYzCcZehl45Q?e=SkhejA)
- For each presentation, explain the research problem, method, data, evaluation, main results, limitations, and one follow-up idea.

## Recommended learning resources

**Required textbook in the course card:** Daniel Jurafsky and James H. Martin, *Speech and Language Processing*, 2nd edition (2008) or a later edition. The authors also provide an [online third-edition draft](https://web.stanford.edu/~jurafsky/slp3/); its chapter organization may differ from the second edition.

| Resource | Best use |
|---|---|
| [NLTK Book](https://www.nltk.org/book/) | Foundational text processing, tagging, parsing, and semantics |
| [CAMeL Tools guided Colab](https://colab.research.google.com/drive/1Y3qCbD6Gw1KEw-lixQx1rI6WlyWnrnDS) | Arabic preprocessing, morphology, and tagging |
| [Stanford CoreNLP documentation](https://stanfordnlp.github.io/CoreNLP/) | Command-line linguistic annotation |
| [spaCy linguistic features](https://spacy.io/usage/linguistic-features) | POS tags, dependencies, and morphology in a modern pipeline |
| [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) | Transformer models and practical NLP applications |
| [Hugging Face official notebooks](https://github.com/huggingface/transformers/tree/main/notebooks) | Colab-compatible notebooks for language modeling, QA, translation, and summarization |
| [Hugging Face Audio Course](https://huggingface.co/learn/audio-course/chapter0/introduction) | Speech recognition and text-to-speech |

## Using the materials

Course-authored slides and lab files will appear in their corresponding folders. External tutorials belong to their respective authors; follow their licenses and cite them when reusing material. If a hosted notebook or dependency changes, consult the linked project's current documentation.
