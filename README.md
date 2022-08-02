# reStructured Pretraining (All are in the [Paper](https://arxiv.org/pdf/2206.11147.pdf))
<p align="center">
<img src="https://user-images.githubusercontent.com/59123869/173596999-f21cb853-d88f-4004-ad15-d6105f6e6cb8.png" width="400"/>
</p>


### Hypothesis of NLP Technique Evolution
The iteration of technology always moves along the direction that system developers can design a better and more general system by doing fewer things.

### reStructure, Pre-training, Tuning Paradigm
This paradigm regards model pre-training/tuning as a data storing/accessing process, and claims that a good storing mechanism should make expected data easily accessible.



## Download reStructured Signals?
This dataset is a precious treasure, containing a variety of naturally occurring signals. Any downstream task you can think of (e.g., the college entrance exam mentioned in the RST paper) can benefit from being pre-trained on some of our provided signals. We spent several months collecting the following 29 signal types, accounting for a total of 46,926,447 data samples. We hope this dataset will be a valuable asset for everyone in natural language processing research.

We provide collected signals through [DataLab](https://github.com/ExpressAI/DataLab). For efficiency, we only provide 50,000 samples at most for each signal type. If you want all the samples we collected, please fill this [form](https://docs.google.com/forms/d/e/1FAIpQLSdPO50vSdfwoO3D7DQDVlupQnHgrXrwfF3ePE4X1H6BwgTn5g/viewform?usp=sf_link). More specifically, we collected the following signals.

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
Under planning

## Submit your AI to Gaokao?
See more [detail](https://github.com/ExpressAI/AI-Gaokao)

