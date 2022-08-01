# reStructured Pretraining (All are in the [Paper](https://arxiv.org/pdf/2206.11147.pdf))
<p align="center">
<img src="https://user-images.githubusercontent.com/59123869/173596999-f21cb853-d88f-4004-ad15-d6105f6e6cb8.png" width="400"/>
</p>


### Hypothesis of NLP Technique Evolution
the iteration of technology always moves along the direction that system developers can design a better and more general system by doing fewer things

### reStructure, Pre-training, Tuning Paradigm
this paradigm regards model pre-training/tuning as a data storing/accessing process, and claims that a good storing mechanism should make expected data easily accessible



## Download reStructured Signals?
We provide collected signals through [DataLab](https://github.com/ExpressAI/DataLab). For efficiency, we only provide 50,000 samples at most for each signal type. If you want all the samples we collected, please fill this [form](). More specifically, we collected the following signals.

| Mine | Signal | #Sample | Use in DataLab | Application | 
| --- | --- | --- | --- | --- |
| [Rotten Tomatoes](https://www.rottentomatoes.com/) | (review, rating) | 5311109 | `load_dataset("rst", "rotten_tomatoes_sentiment")` | Sentiment classification | 
| [Daily Mail](https://www.dailymail.co.uk/home/index.html) | (text, category) | 899904 | `load_dataset("rst", "daily_mail_category")`| Topic classification | 
| [Daily Mail](https://www.dailymail.co.uk/home/index.html) | (title, text, summary) | 1026616 | `load_dataset("rst", "daily_mail_summary")` | Summarization; Sentence expansion|
| [Daily Mail](https://www.dailymail.co.uk/home/index.html) | (text, events) | 1006412 | `load_dataset("rst", "daily_mail_temporal")` | Temporal reasoning| 
| [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) | (entity, entity_type, text) | 2214274 | `load_dataset("rst", "wikidata_entity")` | Entity typing| 
| [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) | (subject, object, relation, text) | 1526674 | `load_dataset("rst", "wikidata_relation")` | Relation extraction; Fact retrieval| 
| [wikiHow](https://www.wikihow.com/Main-Page) | (text, category) | 112109 | `load_dataset("rst", "wikihow_text_category")` | Topic classification | 
| [wikiHow](https://www.wikihow.com/Main-Page) | (low_category, high_category) | 4868 | `load_dataset("rst", "wikihow_category_hierarchy")` | Relation extraction; Commonsense reasoning| 
| [wikiHow](https://www.wikihow.com/Main-Page) | (goal, steps) | 47956 | `load_dataset("rst", "wikihow_goal_step")` | Intent detection| 
| [wikiHow](https://www.wikihow.com/Main-Page) | (text, summary) | 703278 | `load_dataset("rst", "wikihow_summary")` | Summarization; Sentence expansion | 
| [wikiHow](https://www.wikihow.com/Main-Page) | (goal, first_step, second_step) | 47787 | `load_dataset("rst", "wikihow_procedure")` | Temporal reasoning |
| [wikiHow](https://www.wikihow.com/Main-Page) | (question, description, answer, related_questions) | 47705 | `load_dataset("rst", "wikihow_question")` | Question generation|
| [Wikipedia](https://www.wikipedia.org/) | (text, entities) |22231011 | `load_dataset("rst", "wikipedia_entities")` | Entity recognition| 
  [Wikipedia](https://www.wikipedia.org/) | (texts, titles) | 3296225 | `load_dataset("rst", "wikipedia_sections")` | Summarization| 
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, pos) | 27123 | `load_dataset("rst", "wordnet_pos")` | Part-of-speech tagging|
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, meaning, possible_meanings) | 27123 | `load_dataset("rst", "wordnet_meaning")` | Word sense disambiguation|
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, synonyms) | 17804 | `load_dataset("rst", "wordnet_synonym")`| Paraphrasing| 
| [WordNet](https://wordnet.princeton.edu/) | (word, sentence, antonyms) | 6408 | `load_dataset("rst", "wordnet_antonym")` |Negation | 
| [ConTRoL](http://arxiv.org/abs/2011.04864) | (premise, hypothesis, label) | 8323 | `load_dataset("rst", "qa_control")` | Natural language inference|
|[DREAM](https://transacl.org/ojs/index.php/tacl/article/view/1534)| (context, question, options, answer) | 9164 | `load_dataset("rst", "qa_dream")` | Reading comprehension|
| [LogiQA](https://doi.org/10.24963/ijcai.2020/501) | (context, question, options, answer) | 7974 | `load_dataset("rst", "qa_logiqa")` | Reading comprehension| 
| [ReClor](https://openreview.net/forum?id=HJgJtT4tvB) | (context, question, options, answer) | 5138 | `load_dataset("rst", "qa_reclor")` |Reading comprehension | 
| [RACE](https://doi.org/10.18653/v1/d17-1082) | (context, question, options, answer) | 44880 | `load_dataset("rst", "qa_race")` | Reading comprehension|
| [RACE-C](http://proceedings.mlr.press/v101/liang19a.html) | (context, question, options, answer) | 5093 | `load_dataset("rst", "qa_race_c")` | Reading comprehension|
| [TriviaQA](https://doi.org/10.18653/v1/P17-1147) | (context, question, answer) | 46636 | `load_dataset("rst", "qa_triviaqa")` |Reading comprehension |
| [Arxiv](https://arxiv.org/) | (text, category) | 1696348 | `load_dataset("rst", "arxiv_category")` |Topic classification| 
| [Arxiv](https://arxiv.org/) | (text, summary) | 1696348 | `load_dataset("rst", "arxiv_summary")` | Summarization; Sentence expansion|
| [Paperswithcode](https://paperswithcode.com/) | (text, entities, datasets, methods, tasks, metrics) | 4731233 | `load_dataset("rst", "paperswithcode_entity")` | Entity recognition| 
| [Paperswithcode](https://paperswithcode.com/) | (text, summary) | 120924 | `load_dataset("rst", "paperswithcode_summary")` | Summarization; Sentence expansion|


## Download reStructured Models?
Under planning

## Submit your AI to Gaokao?
See more [detail](https://github.com/ExpressAI/AI-Gaokao)

