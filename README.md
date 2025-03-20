# EmoDetect-Unify
This repository contains data information and code for the article:

“Towards a new Benchmark for Emotion Detection in NLP: A Unifying Framework of Recent Corpora”
Authors: Anna Koufakou, Elijah Nieves, and John Peller (Florida Gulf Coast University, Fort Myers, Florida, USA)
At the “GenBench workshop: The second workshop on generalisation (benchmarking) in NLP” held at the 2024 EMNLP. 

Our paper: https://aclanthology.org/2024.genbench-1.13.pdf

## Summary: 
In this work, we introduced a unified framework of 11 publicly available text corpora labeled for emotion recognition tasks, presented since 2018. The main goal was to create a single, unified corpus that addresses key factors for generalization testing (Hupkes et al., 2023), such as shift in platform, language, topic, and emotion. We put significant effort in reviewing each dataset's paper and exploring its data organization and formatting (e.g., emotion labels representation) in order to integrate diverse corpora into a unified resource. Part of the unifying process involved mapping the original emotion labels in each corpus to a common set of emotions. After combining the datasets, we ran preliminary baseline experiments to assess emotion detection accuracy, providing a benchmark for other NLP researchers to compare their models. In this repository, we have made all data information and links as well as our code available, allowing users to recreate the unified framework with common emotion labels from all the datasets and run the baseline classification experiments.

- Dieuwke Hupkes, Mario Giulianelli, Verna Dankers, Mikel Artetxe, Yanai Elazar, Tiago Pimentel, Christos Christodoulopoulos, Karim Lasri, Naomi Saphra, Arabella Sinclair, et al. 2023. A taxonomy and review
of generalization research in nlp. Nature Machine Intelligence, 5(10):1161–1174.

## Contents:
- The “data” folder contains a list of the 11 datasets we used in the paper. For each corpus, we provide information about the paper, description of the data, and URLs. We did not redistribute or share the dataset since we do not own them. Instead, we link to the respective URLs to download each one. We also provide information about how we transformed the data for the experiments in our paper.
- The “code” folder has notebooks to a) build the unified framework with the common emotion labels from all datasets, and b) run the classification experiments by fine-tuning on the unified train set and then testing the model on each test set. 

## Challenges and Limitations:
Even though our work involved significant effort to understand the characteristics and formats of the original data, and to transform the data into a unified corpus, there are several limitations. 

This work included datasets presented since 2018, all in English and all represented as single-labeled with a common set of basic emotion labels. The dataset selection for benchmarking should be more expansive, not only in terms of languages and emotion labeling but also regarding data sources and topics. In the realm of emotion recognition using NLP, the linguistic and cultural diversity of emotions highlights the need for more inclusive and representative datasets. Furthermore, additional experimentation, especially cross-corpus, is essential to establish the unified framework as a valuable benchmark. We discuss these issues in the paper linked above.

The unified framework combined datasets from diffferent sources and formats (e.g. social media vs self-written essays) and, more importantly, perspectives and annotation processes. For example, one dataset might include self-annotated statements by the speakers about their feelings (either intentionally labeled or inferred from hashtags or Facebook reactions), while another might involve annotations by others assessing the apparent emotions of the speaker. Secondly, emotions may be defined differently in different annotation schemas: for example, _trust_ may be defined as _liking_ and _feeling safe_ in one schema, and as _sincerity_ and _moral correctness_ in another. 

It is important for NLP researchers to carefully consider these nuances and the suitability of such unified data for any specific application. Further, conclusions drawn about emotions from the unified data have to be carefully weighed to see if using such disparate data is reasonable.

Anyone using this unified framework should be aware of these challenges and limitations.

## Citing datasets and our work:
We sincerely appreciate the hard work from the original data creators! If you use any of the data in this work, you must cite the original publication(s), by using the specific citation provided for each dataset in the subfolder "data".

We did not redistribute or share any of the datasets; instead, we provided links to each original data repository / webpage. If you download any of the datasets, you must adhere to the specific permissions and licenses of the original datasets, per their webpage or repository. This ensures compliance with licensing and guarantees that all contributors receive appropriate recognition.

Finally, please cite our paper if you use our work:
```
@inproceedings{koufakou-etal-2024-towards,
 title={Towards a new Benchmark for Emotion Detection in {NLP}: A Unifying Framework of Recent Corpora},
 author={Koufakou, Anna and Nieves, Elijah and Peller, John},
 booktitle = "Proceedings of the 2nd GenBench Workshop on Generalisation (Benchmarking) in NLP",
 year={2024},
 publisher = "Association for Computational Linguistics",
 url = "https://aclanthology.org/2024.genbench-1.13",
 pages = "196--206"
}
```
Contact us with any questions: _akoufakou [at] fgcu [dot] edu_
