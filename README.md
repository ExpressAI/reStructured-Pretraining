# reStructured Pretraining (All are in the [Paper](https://arxiv.org/pdf/2206.11147.pdf))
<p align="center">
<img src="https://user-images.githubusercontent.com/59123869/173596999-f21cb853-d88f-4004-ad15-d6105f6e6cb8.png" width="400"/>
</p>

## Update
* 2022-09-04: release all models at [Huggingface](https://huggingface.co/XLab)
* 2022-08-15: release all data at [DataLab](https://github.com/ExpressAI/reStructured-Pretraining#download-restructured-signals)


### Hypothesis of NLP Technique Evolution
The iteration of technology always moves along the direction that system developers can design a better and more general system by doing fewer things.

### reStructure, Pre-training, Tuning Paradigm
This paradigm regards model pre-training/tuning as a data storing/accessing process, and claims that a good storing mechanism should make expected data easily accessible.



## Download reStructured Signals?
This dataset is a precious treasure, containing a variety of naturally occurring signals. Any downstream task you can think of (e.g., the college entrance exam mentioned in the RST paper) can benefit from being pre-trained on some of our provided signals. We spent several months collecting the following 29 signal types, accounting for a total of 46,926,447 data samples. We hope this dataset will be a valuable asset for everyone in natural language processing research.

We provide collected signals through [DataLab](https://github.com/ExpressAI/DataLab). For efficiency, we only provide 50,000 samples at most for each signal type. If you want all the samples we collected, please fill this [form](https://docs.google.com/forms/d/e/1FAIpQLSdPO50vSdfwoO3D7DQDVlupQnHgrXrwfF3ePE4X1H6BwgTn5g/viewform?usp=sf_link). More specifically, we collected the following signals.

One example:

```python
# pip install datalabs
from datalabs import load_dataset
rst = load_dataset("rst", "wikipedia_entities")

```

###### We will be happy :smiley: to know if the resource is helpful for your work, and please cite our [work](https://github.com/ExpressAI/reStructured-Pretraining/blob/main/README.md#Bib) :blush:

| Mine | Signal | #Sample | Use in DataLab | Some Applications | 
| --- | --- | --- | --- | --- |
| [Rotten Tomatoes](https://www.rottentomatoes.com/) | (review, rating) | 5,311,109 | `load_dataset("rst", "rotten_tomatoes_sentiment")` | Sentiment classification | 
| [Daily Mail](https://www.dailymail.co.uk/home/index.html) | (text, category) | 899,904 | `load_dataset("rst", "daily_mail_category")`| Topic classification | 
| [Daily Mail](https://www.dailymail.co.uk/home/index.html) | (title, text, summary) | 1,026,616 | `load_dataset("rst", "daily_mail_summary")` | Summarization; Sentence expansion|
| [Daily Mail](https://www.dailymail.co.uk/home/index.html) | (text, events) | 1,006,412 | `load_dataset("rst", "daily_mail_temporal")` | Temporal reasoning| 
| [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) | (entity, entity_type, text) | 2,214,274 | `load_dataset("rst", "wikidata_entity")` | Entity typing| 
| [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) | (subject, object, relation, text) | 1,526,674 | `load_dataset("rst", "wikidata_relation")` | Relation extraction; Fact retrieval| 
| [wikiHow](https://www.wikihow.com/Main-Page) | (text, category) | 112,109 | `load_dataset("rst", "wikihow_text_category")` | Topic classification | 
| [wikiHow](https://www.wikihow.com/Main-Page) | (low_category, high_category) | 4,868 | `load_dataset("rst", "wikihow_category_hierarchy")` | Relation extraction; Commonsense reasoning| 
| [wikiHow](https://www.wikihow.com/Main-Page) | (goal, steps) | 47,956 | `load_dataset("rst", "wikihow_goal_step")` | Intent detection| 
| [wikiHow](https://www.wikihow.com/Main-Page) | (text, summary) | 703,278 | `load_dataset("rst", "wikihow_summary")` | Summarization; Sentence expansion | 
| [wikiHow](https://www.wikihow.com/Main-Page) | (goal, first_step, second_step) | 47,787 | `load_dataset("rst", "wikihow_procedure")` | Temporal reasoning |
| [wikiHow](https://www.wikihow.com/Main-Page) | (question, description, answer, related_questions) | 47,705 | `load_dataset("rst", "wikihow_question")` | Question generation|
| [Wikipedia](https://www.wikipedia.org/) | (text, entities) |22,231,011 | `load_dataset("rst", "wikipedia_entities")` | Entity recognition| 
  [Wikipedia](https://www.wikipedia.org/) | (texts, titles) | 3,296,225 | `load_dataset("rst", "wikipedia_sections")` | Summarization| 
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, pos) | 27,123 | `load_dataset("rst", "wordnet_pos")` | Part-of-speech tagging|
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, meaning, possible_meanings) | 27,123 | `load_dataset("rst", "wordnet_meaning")` | Word sense disambiguation|
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, synonyms) | 17,804 | `load_dataset("rst", "wordnet_synonym")`| Paraphrasing| 
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, antonyms) | 6,408 | `load_dataset("rst", "wordnet_antonym")` |Negation | 
| [ConTRoL](http://arxiv.org/abs/2011.04864) | (premise, hypothesis, label) | 8,323 | `load_dataset("rst", "qa_control")` | Natural language inference|
|[DREAM](https://transacl.org/ojs/index.php/tacl/article/view/1534)| (context, question, options, answer) | 9,164 | `load_dataset("rst", "qa_dream")` | Reading comprehension|
| [LogiQA](https://doi.org/10.24963/ijcai.2020/501) | (context, question, options, answer) | 7,974 | `load_dataset("rst", "qa_logiqa")` | Reading comprehension| 
| [ReClor](https://openreview.net/forum?id=HJgJtT4tvB) | (context, question, options, answer) | 5,138 | `load_dataset("rst", "qa_reclor")` |Reading comprehension | 
| [RACE](https://doi.org/10.18653/v1/d17-1082) | (context, question, options, answer) | 44,880 | `load_dataset("rst", "qa_race")` | Reading comprehension|
| [RACE-C](http://proceedings.mlr.press/v101/liang19a.html) | (context, question, options, answer) | 5,093 | `load_dataset("rst", "qa_race_c")` | Reading comprehension|
| [TriviaQA](https://doi.org/10.18653/v1/P17-1147) | (context, question, answer) | 46,636 | `load_dataset("rst", "qa_triviaqa")` |Reading comprehension |
| [Arxiv](https://arxiv.org/) | (text, category) | 1,696,348 | `load_dataset("rst", "arxiv_category")` |Topic classification| 
| [Arxiv](https://arxiv.org/) | (text, summary) | 1,696,348 | `load_dataset("rst", "arxiv_summary")` | Summarization; Sentence expansion|
| [Paperswithcode](https://paperswithcode.com/) | (text, entities, datasets, methods, tasks, metrics) | 4,731,233 | `load_dataset("rst", "paperswithcode_entity")` | Entity recognition| 
| [Paperswithcode](https://paperswithcode.com/) | (text, summary) | 120,924 | `load_dataset("rst", "paperswithcode_summary")` | Summarization; Sentence expansion|


## Download reStructured Models?
Check all models at [Huggingface](https://huggingface.co/XLab)
### Model Description
We release all models introduced in our [paper](https://arxiv.org/pdf/2206.11147.pdf), covering 13 different application scenarios. Each model contains 11 billion parameters.

| Model      | Description | Recommended Application
| ----------- | ----------- |----------- |
| rst-all-11b                     | Trained with all the signals below except signals that are used to train Gaokao models        | All applications below （specialized models are recommended first if high performance is preferred） |
| rst-fact-retrieval-11b              | Trained with the following signals: WordNet meaning, WordNet part-of-speech, WordNet synonym, WordNet antonym, wikiHow category hierarchy, Wikidata relation, Wikidata entity typing, Paperswithcode entity typing       | Knowledge intensive tasks, information extraction tasks,factual checker  |
| rst-summarization-11b               | Trained with the following signals: DailyMail summary, Paperswithcode summary, arXiv summary, wikiHow summary    | Summarization or other general generation tasks, meta-evaluation (e.g., BARTScore)  |
| rst-temporal-reasoning-11b          | Trained with the following signals: DailyMail temporal information, wikiHow procedure       |  Temporal reasoning, relation extraction, event-based extraction |
| rst-information-extraction-11b      | Trained with the following signals: Paperswithcode entity, Paperswithcode entity typing, Wikidata entity typing, Wikidata relation, Wikipedia entity       |  Named entity recognition, relation extraction and other general IE tasks in the news, scientific or other domains|
| rst-intent-detection-11b            | Trained with the following signals: wikiHow goal-step relation       | Intent prediction, event prediction  |
| rst-topic-classification-11b        | Trained with the following signals: DailyMail category, arXiv category, wikiHow text category, Wikipedia section title | general text classification   |
| rst-word-sense-disambiguation-11b   | Trained with the following signals: WordNet meaning, WordNet part-of-speech, WordNet synonym, WordNet antonym   | Word sense disambiguation, part-of-speech tagging, general IE tasks, common sense reasoning  |
| rst-natural-language-inference-11b  | Trained with the following signals: ConTRoL dataset, DREAM dataset, LogiQA dataset, RACE & RACE-C dataset, ReClor dataset, DailyMail temporal information       | Natural language inference, multiple-choice question answering, reasoning  |
| rst-sentiment-classification-11b    | Trained with the following signals: Rotten Tomatoes sentiment, Wikipedia sentiment | Sentiment classification, emotion classification  |
| rst-gaokao-rc-11b                   | Trained with multiple-choice QA datasets that are used to train the [T0pp](https://huggingface.co/bigscience/T0pp) model       | General multiple-choice question answering|
| rst-gaokao-cloze-11b                | Trained with manually crafted cloze datasets    |  General cloze filling|
| **rst-gaokao-writing-11b**              | **Trained with example essays from past Gaokao-English exams and grammar error correction signals**       | **Essay writing, story generation, grammar error correction and other text generation tasks**  |



### Have a try?
```python
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM

tokenizer = AutoTokenizer.from_pretrained("XLab/rst-all-11b")
model = AutoModelForSeq2SeqLM.from_pretrained("XLab/rst-all-11b")

inputs = tokenizer.encode("TEXT: this is the best cast iron skillet you will ever buy. QUERY: Is this review \"positive\" or \"negative\"", return_tensors="pt")
outputs = model.generate(inputs)
print(tokenizer.decode(outputs[0], skip_special_tokens=True, clean_up_tokenization_spaces=True))
```

## Submit your AI to Gaokao?
See more [detail](https://github.com/ExpressAI/AI-Gaokao)

## Bib
```
@article{yuan2022restructured,
  title={reStructured Pre-training},
  author={Yuan, Weizhe and Liu, Pengfei},
  journal={arXiv preprint arXiv:2206.11147},
  year={2022}
}
```
