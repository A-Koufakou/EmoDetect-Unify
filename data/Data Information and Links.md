# Data Information and Links
Datasets: This file contains brief descriptions and links for recent datasets used in text-based emotion recognition (since 2018).

**CARER**
- Authors: Elvis Saravia, Hsien-Chi Toby Liu, Yen-Hao Huang, Junlin Wu, and Yi-Shin Chen.
- Size: total was 416,809 tweets. Sample we used for our experiments: 62,522 (with the same label distribution as the original).
- Description: Saravia et al. (2018) collected tweets with a set of hashtags they constructed, e.g. #depressed, #grief for sadness, or #fear, #worried for fear. The dataset posted on Hugging Face is labeled with Shaver (based on the hashtags), and it is a variant of the dataset presented in the article.
- Labels: anger, fear, joy, sadness, surprise, love
- Link to paper: https://aclanthology.org/D18-1404/
- Link to dataset: https://huggingface.co/datasets/dair-ai/emotion

**Covid-Worry**
- Authors: Bennett Kleinberg, Isabelle van der Vegt, and Maximilian Mozes
- Size: 5,350 survey responses from surveys given over 3 years
- Description: Contains survey responses collected in the UK first in 2020 and then 2021-22 (van der Vegt and Kleinberg, 2023). Participants wrote text and self-rated the records with specific emotions. It also contains demographics and other fields entered by the participants.
- Labels: anger, anxiety, disgust, desire, fear, happiness, relaxation, sadness
- Link to paper: https://aclanthology.org/2020.nlpcovid19-acl.11/  and https://www.nature.com/articles/s41597-023-02438-y 
- Links to datasets: For Covid-Worry in our experiments, we merged the results from 3 different phases (surveys) as follows:
  - 1st phase: https://raw.githubusercontent.com/ben-aaron188/covid19worry/master/data_phase_1/files/meta/rwwd_full.csv
  - 2nd phase: the authors interviewed participants from phase 1 again but not all of the participants from phase 1 took the 2nd survey. We took all the phase 2 data from this file: https://github.com/ben-aaron188/covid19worry/blob/master/data_repeated_measures/meta/rwwd_phase1_phase2.csv
  - 3rd phase: similar to the above, we took only the phase 3 results from the file on this link: https://osf.io/ckfxp
  - Finally, we merged all the entries as described above into one file, resulting in 5,350 entries.

**EmoEvent**
- Authors: Flor Miriam Plaza del Arco, Carlo Strapparava, L. Alfonso Urena Lopez, and Maite Martin
- Size: 7,303 English tweets
- Description: Contains tweets collected by Plaza-del-Arco et al. (2020) related to events in 2019. The resulting tweets in English and in Spanish were annotated by Amazon MTurkers.
- Labels: anger, disgust, fear, joy, sadness, surprise, neutral
- Link to paper: https://aclanthology.org/2020.lrec-1.186/
- Link to dataset: https://github.com/fmplaza/EmoEvent  Note: This repo has a couple of different versions of the data. For our experiments, we used the version where the hashtags, etc. had been replaced. 

**enISEAR**
- Authors: Enrica Troiano, Sebastian Padó, Roman Klinger
- Size: 1,001 English questionnaire responses
- Description: Answers from a questionnaire where crowdsourced annotators gave a description of an event for which they felt a particular emotion, given as input. Uses a framework similar to earlier ISEAR (International Survey on Emotion Antecedents and Reactions) (Scherer and Wallbott, 1994).
- Labels: anger, disgust, fear, joy, sadness, surprise, shame, guilt
- Link to paper: https://aclanthology.org/P19-1391/
- Link to dataset: https://www.ims.uni-stuttgart.de/forschung/ressourcen/korpora/deisear/

**Github-love (github-emotion-love)**
- Authors: Mia Mohammad Imran, Yashasvi Jain, Preetha Chatterjee, Kostadin Damevski
- Size: 1,719 GitHub comments
- Description: This dataset by Imran et al. (2022) contains GitHub comments on pull requests/issues for popular repositories, annotated by the authors. The paper used many detailed emotions, though the dataset available online has basic Shaver labels.
- Labels: anger, fear, joy, sadness, surprise, love
- Link to paper: https://dl.acm.org/doi/pdf/10.1145/3551349.3556925
- Link to dataset: https://huggingface.co/datasets/imranraad/github-emotion-love

**GoEmotions**
- Authors: Dorottya Demszky, Dana Movshovitz-Attias, Jeongwoo Ko, Alan Cowen, Gaurav Nemade, Sujith Ravi
- Size: about 58K Reddit comments. The dataset we used has 43,975 records.
- Description: Contains Reddit comments with fine-grained multi-label human annotations. For our paper, we transformed the dataset to single-label: we kept only records with a single label or if the multiple labels mapped to the same label in our common set of emotions.
- Labels: 27 emotions + neutral. Revised from Cowen and Keltner. They also included Ekman mapping for their emotions https://github.com/google-research/google-research/blob/master/goemotions/data/ekman_mapping.json 
- Link to paper: https://aclanthology.org/2020.acl-main.372/
- Link to dataset: https://github.com/google-research/google-research/tree/master/goemotions

**GoodNews (GoodNewsEveryone)**
- Authors: Laura Oberländer, Evgeny Kim, Roman Klinger
- Size: about 5K 
- Description: A corpus of news headlines in English annotated with emotions, semantic roles, and reader perception by crowdsourcing.
- Labels: Extended Plutchik (15 emotions + neutral)
- Link to paper: https://aclanthology.org/2020.lrec-1.194.pdf
- Link to dataset: https://www.ims.uni-stuttgart.de/forschung/ressourcen/korpora/goodnewseveryone/

**StackOv-GS (StackOverflow - Gold Standard)**
- Authors: Nicole Novielli, Fabio Calefato, Filippo Lanubile
- Size: 2,974 Stack Overflow posts
- Description: Novielli et al. (2018) collected Stack Overflow questions, answers, and comments. They were annotated by volunteers.
- Labels: anger, disgust, fear, joy, sadness, surprise, love
- Link to paper: https://dl.acm.org/doi/pdf/10.1145/3196398.3196453
- Link to dataset: https://github.com/collab-uniba/EmotionDatasetMSR18

**TweetEval**
- Authors: Francesco Barbieri, Jose Camacho-Collados, Leonardo Neves, Luis Espinosa-Anke
- Size: 5,052 tweets
- Description: A unified Twitter dataset with seven heterogeneous Twitter-specific classification tasks. Includes Affect in Tweets (Mohammad et al., 2018), only keeping single-label records and removing rare emotions.
- Labels: anger, joy, optimism, sadness
- Link to paper: https://aclanthology.org/2020.findings-emnlp.148/
- Link to dataset: https://github.com/cardiffnlp/tweeteval/tree/main/datasets/emotion

**Universal Joy**
- Authors: Sotiris Lamprinidis, Federico Bianchi, Daniel Hardt, Dirk Hovy
- Size: total was 167,313 Facebook posts (English set). Sample we used for our experiments: 50,195 (same label distribution as original data)
- Description: Lamprinidis et al. (2021) presented a dataset with anonymized public Facebook posts collected in 2014 in 18 languages. The authors labeled the records.
- Labels: anger, anticipation, fear, joy, sadness
- Link to paper: https://aclanthology.org/2021.wassa-1.7/
- Link to dataset: https://github.com/sotlampr/universal-joy

**WASSA-21**
- Authors: Valentin Barriere, João Sedoc, Shabnam Tafreshi, and Salvatore Giorgi
- Size: 2,385 essays.
- Description: Part of the 11th Workshop on Computational Approaches to Subjectivity, Sentiment & Social Media Analysis (WASSA 2021) shared task. Contains essays written to express empathy and distress after reading news articles related to harm to an individual, nature, etc. The emotion labels were first predicted by Neural Networks and then post-annotated by crowdsourcing workers and a PhD student.
- Labels: anger, disgust, fear, joy, sadness, surprise, neutral
- Link to paper: https://aclanthology.org/2021.wassa-1.10/
- Link to dataset: https://competitions.codalab.org/competitions/28713
  - Update Oct 15, 2024: it seems old competitions are not working, so you could look into the data in wassa 2022 (according to the paper the shared task in 2022 re-used the 2021 data)  https://codalab.lisn.upsaclay.fr/competitions/834#learn_the_details-datasets 
