# Word Embedding Demo
Das vorliegende Git-Repository enthält den Beispiel-Code für das Sitzungsreferat zum Thema ***Word Embeddings*** vom 05.12.2019 im Hauptseminar "Konzepte der Ähnlichkeit aus psycho- und computerlinguistischer Perspektive" (WS 2019/2020).

**Hinweis:**<br>
Das Jupyter-Notebook basiert in Teilen auf Tutorials von zwei Framworks für Word Embeddings (s.u.), weswegen ich an dieser Stelle auf die entsprechenden Quellen verweise:

- [Gensim Core Tutorial](https://radimrehurek.com/gensim/auto_examples/index.html)
- [Gensim word2vec Tutorial](https://radimrehurek.com/gensim/auto_examples/tutorials/run_word2vec.html#sphx-glr-auto-examples-tutorials-run-word2vec-py)
- [Flair Tutorial 2: Tagging your text](https://github.com/zalandoresearch/flair/blob/master/resources/docs/TUTORIAL_2_TAGGING.md)
- [FLair Tutorial 3: Word Embeddings](https://github.com/zalandoresearch/flair/blob/master/resources/docs/TUTORIAL_3_WORD_EMBEDDING.md)

## Online-Demos zu word2vec
Die gesamten word2vec-Embeddings von Google News können **interaktiv** auf folgenden Seiten durchsucht werden. Hierfür ist keine Programmiererfahrung notwendig!
- https://projector.tensorflow.org/
   - 2/3-D Darstellung der Daten möglich, Suche nach den n ähnlichsten Wörtern
- https://rare-technologies.com/word2vec-tutorial/#app
   - Web-Demo für Ähnlichkeitssuchen (mit "Analogieschlüssen", Filtern von untypischen Wörtern aus einer Reihe etc.)

## Frameworks
**Hinweis:** Alle gelisteten Frameworks sind für Python geschrieben im Hintergrund wird daraus jedoch - aus Performanzgründen - meist C-Code kompiliert (z.B. mit Cython).

- [Gensim (v3.8.1)](https://radimrehurek.com/gensim/)
  - Framework für verschiedene Topic-Modelle und Embeddings mit Fokus auf performante Implementation der entsprechenden Algorithmen.
- [Flair (v0.4.4)](https://github.com/zalandoresearch/flair)
  - Implementation des in [Akibat et al. (2018)](https://alanakbik.github.io/papers/coling2018.pdf) vorgestellten Embeddings-Verfahrens als leichtgewichtiges NLP-Framework.
- [Natural Language Toolkit (NLTK) (v3.4.5)](https://www.nltk.org/)
  - Sammlung verschiedener Funktionalitäten und Korpora zur computerlinguistischen Sprachverarbeitung. Enthält leider meist 'nur' ältere Verfahren, allerdings m.E. nach sehr gute Funktionaltiäten für Vorverarbeitung (z.B. Stemming, Tokenisierung, N-Gramm-Erstellung etc.). 
- [Jupyter (v1.0.0)](https://jupyter.org/)
  - Ermöglicht zellenweise Ausführung von Python-Code in Form eines sogenannten Notebooks. Eignet sich inbesondere für didaktische Präsentation von Programmiercode sowie schnelles Prototyping.
- [Scikit-Learn (v0.21.3)](https://scikit-learn.org/stable/)
  - Framework mit Implementationen der gängigsten Machine-Learning Algorithmen (nicht nur NLP). Leichter Zugriff auf Modelle durch einheitliche API.
- [Pytorch (v1.3.1)](https://pytorch.org/get-started/locally/)
  - Deep Learning Framework (Stichwort: Neuronale Netze), Grundlage für Flair.
- [Pandas (v0.25.3)](https://pandas.pydata.org/)
  - Framework zum tabellarischen Einlesen und Verarbeiten von Daten, vergleichbar mit Dataframes in R.
  
## Installation
- [**Python 3.6 installieren**](https://www.python.org/downloads/)<br> 
**Hinweis:**<br>
Getestet mit Python 3.6.8.<br>
Flair benötigt notwendigerweise Python 3.6+, die anderen Teile des Tutorials *könnten* aber auch älteren Python-Versionen laufen (**nicht getestet, keine Garantie**).

- [**Virtuelle Laufzeitumgebung für Python einrichten**](https://docs.python.org/3/tutorial/venv.html)<br>
Kommandozeile öffnen, dann folgende Befehle eingeben: 

```
# Wechsel in das Verzeichnis der Demo
cd path/to/repo/word_embeddings_demo
```

**Linux/Mac**
```
python3 -m venv venv
```
**Windows**
```
py -m venv venv
```

Anschließend muss die virtuelle Umgebung aktiviert werden (in derselben Kommandozeile):

**Linux/Mac**
```
source venv/bin/activate
```
**Windows**
```
venv\Scripts\activate
```

In der Kommandozeile sollte nun ein (venv) vor dem Prompt erscheinen.<br>
Anschließend können innerhalb dieser virtuellen Umgebung alle benötigten Software-Abhängigkeiten für die Demo installiert werden.

- [**Pytorch installieren**](https://pytorch.org/)
```
# Installation CPU-Version von Pytorch **in virtueller Umgebung *(ausreichend für Demo)
pip3 install torch==1.3.1+cpu torchvision==0.4.2+cpu -f https://download.pytorch.org/whl/torch_stable.html
```
**Hinweis:**<br>
Eine ausreichende Graphikkarte vorausgesetzt, kann auch die GPU-Version von Pytorch installiert werden (s. Pytorch installieren).

## Starten der Demo

- Jupyter-Notebook-Server starten<br>

**Linux/Mac**
```
jupyter notebook
```
**Windows**
```
venv\Scripts\jupyter-notebook.exe
```
- Öffnen des Jupyter-Notebooks im Browser (sollte automatisch geschehen)
```
# Folgenden Link öffnen:
http://localhost:8888/tree
```
Anschließend kann die Datei **word_embedding_demo.ipynb** geöffnet werden. Die Demo kann dann zellenweise ausgeführt werden.

## Quellen
- Jurafksy, D., & Martin, J. H. (2019). *Language and speech technologie: An introduction
to natural language processing, computational linguistics, and speech
recognition (3rd ed. draft)*. Retrieved from <https://web.stanford.edu/~jurafsky/slp3/ed3book.pdf>.

- Akbik, A., Blythe, D., & Vollgraf, R. (2018). [Contextual String Embeddings for Sequence Labeling](https://www.aclweb.org/anthology/C18-1139.pdf). *27th International Conference on Computational Linguistics, COLING 2018*, 1638-1649.

- Akbik, A., Bergmann, T., & Vollgraf, R. (2019). [Pooled Contextualized Embeddings for Named Entity Recognition](https://www.aclweb.org/anthology/N19-1078.pdf). *Annual Conference of the North American Chapter of the Association for Computational Linguistics, NAACL 2019*, 724–728].

- Akbik, A., Bergmann, T., Blythe, D., Rasul, K., Schweter, S.,& Vollgraf, R. (2019). [FLAIR: An Easy-to-Use Framework for State-of-the-Art NLP](https://www.aclweb.org/anthology/N19-4010.pdf). *Annual Conference of the North American Chapter of the Association for Computational Linguistics (Demonstrations), NAACL 2019*, 54–59.
