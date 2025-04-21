# :earth_africa: GERA: Grammatical Errors for Russian (Annotated corpus)

## :envelope: Description
### Source
In contrast to previous works, our data consists of middle school essays written by **native speakers**. They were annotated by **university students with linguistic backgrounds**.

### Data Format
The corpus contains a fine-grained annotation of grammatical errors in **.M2 format**. Each annotated sample includes the source text and the corresponding edits. Each edit annotation consists of several columns including from left to right, the edit span, error type, correction, whether the edit is optional or required, remarks and annotator ID. If there are no mistakes in the sentences, there is a single line with error span `-1 -1` and error type `noop`.

### Size and Error Distribution
We have divided all the sentences into train, validation and test as 68\%, 12\% and 20\%, respectively. Samples have similar distributions by essay topics and error types.
|Sample|Sentences|\% of Incorrect Sentences|Tokens|
|--|--|--|--|
|Train|4592|50.30|81088|
|Validation|775|50.71|15478|
|Test|1314|48.48|22502|

The distribution of errors in our data differs from other corpora, containing more punctuation and less wordform errors. We refer to our article for more details (see **Cite us**).
### Model evaluations on GERA
We study the performance of several models on our data and find that **the finetuned YandexGPT model** is the best. It shows F<sub>0.5</sub>-score ~ 73\%. Among the models of smaller size, the highest score is reached by the ranker-generator pipeline, whose score is 71\%.

## :boom: Cite us
The corpus was presented in the paper **GERA: a corpus of Russian school texts annotated for Grammatical Error Correction**, which received the best paper award during the [AIST-2024 conference](https://aistconf.org/).

If you use GERA in your research, please cite:
```
Sorokin, A., Nasyrova, R. (2025). GERA: A Corpus of Russian School Texts Annotated for Grammatical Error Correction. In: Panchenko, A., et al. Analysis of Images, Social Networks and Texts. AIST 2024. Lecture Notes in Computer Science, vol 15419. Springer, Cham. https://doi.org/10.1007/978-3-031-88036-0_8
```

or
```
@InProceedings{10.1007/978-3-031-88036-0_8,
  author="Sorokin, Alexey
          and Nasyrova, Regina",
  editor="Panchenko, Alexander
          and Gubanov, Dmitriy
          and Khachay, Michael
          and Kutuzov, Andrey
          and Loukachevitch, Natalia
          and Kuznetsov, Andrey
          and Nikishina, Irina
          and Panov, Maxim
          and Pardalos, Panos M.
          and Savchenko, Andrey V.
          and Tsymbalov, Evgenii
          and Tutubalina, Elena
          and Kasieva, Aida
          and Ignatov, Dmitry I.",
  title="GERA: A Corpus of Russian School Texts Annotated for Grammatical Error Correction",
  booktitle="Analysis of Images, Social Networks and Texts",
  year="2025",
  publisher="Springer Nature Switzerland",
  address="Cham",
  pages="148--163",
  abstract="We present a new corpus for the task of grammatical error correction for the Russian language. In contrast to previous works, our data consists of middle school essays written by native speakers. In             total, the training data includes more than 4500 sentences and the test partition -- more than 1000 sentences. The corpus contains a detailed annotation of grammatical errors in .M2 format, fine-grained           error types are also available. The distribution of errors in our data differs from other corpora, containing more punctuation and less wordform errors. We study the performance of several models on our           data and find that the finetuned YandexGPT model is the best. It shows F{\$}{\$}{\_}{\{}0.5{\}}{\$}{\$}0.5-score about 73{\%}. Among the models of smaller size, the highest score is reached by the                 ranker-generator pipeline, whose score is 71{\%}.",
  isbn="978-3-031-88036-0"
  }
```
