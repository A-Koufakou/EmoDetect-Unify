# EmoDetect-Unify
This repository contains data information and code for the article:

“Towards a new Benchmark for Emotion Detection in NLP: A Unifying Framework of Recent Corpora”
Authors: Anna Koufakou, Elijah Nieves, and John Peller (Florida Gulf Coast University, Fort Myers, Florida, USA)
At the “GenBench workshop: The second workshop on generalisation (benchmarking) in NLP” held at the 2024 EMNLP. 
https://genbench.org/workshop/ 

## Summary: 
To address the need for new NLP emotion detection benchmarks, we selected several recent diverse emotion-annotated corpora, combined them into a unified framework by mapping into a set of common emotions and performed baseline experiments for emotion detection with the unified framework.

## Contents:
- The “data” folder contains a list of the 11 datasets we used in the paper. For each corpus, we provide information about the paper, description of the data, and URLs. Since we do not own the datasets, we link to the respective URLs to download each one. We also provide information about how we transformed the data for the experiments in our paper.
- The “code” folder has notebooks to a) build the unified framework with the common emotion labels from all datasets, and b) run the classification experiments by fine-tuning on the unified train set and then testing the model on each test set. 

## Citation:
Please cite our paper if you use our work:
```
@inproceedings{koufakou2024emobench,
 title={Towards a new Benchmark for Emotion Detection in {NLP}: A Unifying Framework of Recent Corpora},
 author={Koufakou, Anna and Nieves, Elijah and Peller, John},
 booktitle={Proceedings of the 2nd GenBench workshop on generalisation (benchmarking) in NLP},
 year={2024}
}
```
Contact us with any questions: _akoufakou [at] fgcu [dot] edu_
