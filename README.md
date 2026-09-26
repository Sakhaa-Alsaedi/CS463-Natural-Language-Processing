
# CS463 — Natural Language Processing
<img width="2172" height="724" alt="Image" src="https://github.com/user-attachments/assets/650b6303-1fae-4cce-a001-31f9b25d71d1" />

Welcome to the CS463 course repository. It brings together lecture slides, hands-on labs, Jupyter/Google Colab notebooks, shell exercises, and selected readings for natural language processing (NLP). The course introduces both theory and practice in programs that understand, generate, translate, and extract information from written language. It compares conventional and statistical techniques, then applies them to question answering, summarization, and machine translation. Arabic examples are included throughout where appropriate.

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
| **1 — Introduction to NLP** | A text-to-annotation pipeline | Inspect English and Arabic samples. Show tokenization, ambiguity, and the output of a pretrained POS/dependency pipeline; label the linguistic levels introduced in the slides. | [NLTK Book, Ch. 1](https://www.nltk.org/book/ch01.html) · [Stanza pipeline](https://stanfordnlp.github.io/stanza/pipeline.html) |
| **2 — Regular expressions** | Regex: shell versus Python | Use `grep -E` and Python `re` on the same UTF-8 corpus; extract dates, hashtags, and word variants, then measure precision and recall against a small hand-labeled answer key. | [NLTK Book, Ch. 3](https://www.nltk.org/book/ch03.html) |
| **3 — Morphology** | Arabic roots and analyses | Count words and plot a small Zipf curve; compare rule-based stemming with CAMeL morphological analyses (roots, stems, patterns, and affixes). Inspect ambiguous Arabic forms rather than assuming one analysis per word. | [CAMeL CLI](https://camel-tools.readthedocs.io/en/latest/cli_tools.html) · [CAMeL guided Colab](https://colab.research.google.com/drive/1Y3qCbD6Gw1KEw-lixQx1rI6WlyWnrnDS) |
| **4 — Language models** | N-grams, smoothing, perplexity | Implement unigram and bigram counts; compare unsmoothed and add-one/interpolated probabilities, handle unseen words, and report held-out perplexity. Optionally compare generated text with a small pretrained causal LM. | [NLTK `lm`](https://www.nltk.org/api/nltk.lm.html) · [Hugging Face causal LM](https://huggingface.co/docs/transformers/en/tasks/language_modeling) |
| **5 — Part-of-speech tagging I** | POS from the terminal | Run Stanford CoreNLP POS tagging from a shell on supplied sentences; inspect open/closed classes and ambiguous words. Repeat selected Arabic sentences with CAMeL or Stanza and compare tagsets. | [CoreNLP POS CLI](https://stanfordnlp.github.io/CoreNLP/pos.html) · [Stanza POS](https://stanfordnlp.github.io/stanza/pos.html) |
| **6 — Part-of-speech tagging II** | Baselines versus pretrained tags | Build default, unigram, and n-gram taggers; measure token accuracy and inspect a confusion table. Compare their mistakes with a pretrained tagger, keeping English and Arabic evaluations separate. | [NLTK Book, Ch. 5](https://www.nltk.org/book/ch05.html) · [CAMeL Tools](https://camel-tools.readthedocs.io/) |
| **7 — First midterm** | — | No regular lab. | — |
| **8 — Hidden Markov models** | Forward and Viterbi | Use a tiny two-state tagging HMM to calculate sequence likelihood with the forward algorithm and the best tag path with Viterbi; compare the two quantities and draw the trellis. | [NLTK tagging background](https://www.nltk.org/book/ch05.html) · Instructor notebook with a small transition/emission table |
| **9 — Syntactic and statistical parsing** | CKY and probabilistic parses | Fill a CKY chart by hand for a short ambiguous sentence; define a PCFG in NLTK, rank parses with `ViterbiParser`, then compare constituency output with a pretrained dependency parser. | [NLTK parsing](https://www.nltk.org/book/ch08.html) · [ViterbiParser](https://www.nltk.org/api/nltk.parse.viterbi.html) · [Stanza dependencies](https://stanfordnlp.github.io/stanza/depparse.html) |
| **10 — Lexical and statistical semantics** | Word senses and meaning | Explore WordNet relations and two senses of an ambiguous word. Construct a simple logical/semantic representation for one sentence; compare lexical similarity with a contextual embedding as an extension. | [NLTK lexical resources](https://www.nltk.org/book/ch02.html) · [NLTK sentence meaning](https://www.nltk.org/book/ch10.html) |
| **11 — Second midterm** | — | No regular lab. | — |
| **12 — Computational discourse** | Coherence and reference | Reorder a short paragraph and ask which version is more coherent. Annotate pronoun references across sentences, then build a small discourse representation. | [NLTK discourse examples](https://www.nltk.org/howto/drt.html) |
| **13 — Question answering and summarization** | Retrieve, answer, summarize | On a fixed document set, compare keyword retrieval with extractive QA; build an extractive summary and compare it with a pretrained abstractive model. Score sentence selection with precision/recall and audit generated claims against the source. | [Hugging Face QA](https://huggingface.co/learn/llm-course/chapter7/7) · [Summarization](https://huggingface.co/learn/llm-course/en/chapter7/5) |
| **14 — Machine translation** | Alignment and BLEU | Manually align words in a short bilingual pair, compare a literal baseline with a pretrained Arabic–English translation model, calculate corpus BLEU with SacreBLEU, and inspect meaning and morphology errors. | [Hugging Face translation](https://huggingface.co/learn/llm-course/en/chapter7/4?fw=pt) · [SacreBLEU](https://github.com/mjpost/sacrebleu) |
| **15 — Speech processing** | MFCC, ASR, and WER | Plot a waveform/spectrogram and MFCCs from a short recording; transcribe clean and noisy speech with a pretrained ASR model and compute word error rate. Treat TTS as an optional extension. | [Hugging Face Audio Course](https://huggingface.co/learn/audio-course/chapter0/introduction) · [JiWER](https://github.com/jitsi/jiwer) |

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

## Assessment

The Fall 2026 course card lists the following assessment weights. Refer to the course platform for exact dates and submission instructions.

| Assessment | Scheduled week | Weight |
|---|---:|---:|
| First midterm exam | 7 | 15% |
| Second midterm exam | 11 | 20% |
| Exercises and homework | 8 | 5% |
| Group project | 13 | 20% |
| Final exam | 16–18 | 40% |

Individual assignments must be original work. For group tasks, collaborate within your assigned group and cite all material you use. Follow the university's Student Handbook and course instructions for academic conduct and attendance.

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
g to their respective authors; follow their licenses and cite them when reusing material. If a hosted notebook or dependency changes, consult the linked project's current documentation.
