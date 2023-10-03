# SimpleText@CLEF-2024 Tasks

[Home](./) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) 
[Program](./program) | [Publications](./publications) | [Organizers](./organizers) | [Contact](./contact) | [CLEF-2023](https://simpletext-project.com/2023/clef/)

---
## How to participate
In order to participate, you should sign up at the [CLEF](https://clef2024.clef-initiative.eu/index.php) website: [http://clef2024-labs-registration.dei.unipd.it/](http://clef2023-labs-registration.dei.unipd.it/). 

All team members should join the SimpleText mailing list:
[https://groups.google.com/g/simpletext](https://groups.google.com/g/simpletext). 

The data will be made available to all registered participants.

## Task 1: Content Selection: Selecting passages to include in a simplified summary

Given a popular science article from a major international newspaper, this task aims at retrieving all passages that would be relevant for this article, from a large corpus of scientific abstracts and bibliographic metadata. Relevant passages should relate to any of the topics in the source article. Relevant abstracts should relate to any of the topics in the source article. These passages can be complex and require further simplification to be carried out in tasks 2 and 3. Task 1 focuses on content retrieval. 

### Corpus: DBLP + abstracts
We use the Citation Network Dataset: 
- DBLP+Citation
- ACM Citation network, the 12th version released in 2020: [https://www.aminer.org/citation](https://www.aminer.org/citation)

An ElasticSearch index is provided to participants with access through an API. A JSON dump of the index is also available for participants.

### Queries
Topics are a selection of press articles from the Science section of The Guardian and Tech Xplore, enriched with queries manually extracted from the content of the article. It has been checked that at least 5 relevant abstracts can be found for each query.

### Evaluation
**Topical relevance**: 
Retrieval effectiveness will be evaluated on:

- Topic **relevance**: 
  - Not relevant (0)
  - Relevant (1)
  - Highly relevant (2)

We will use traditional IR measures to evaluate the effectiveness (NDCG@10, MAP, ...).

**Additional measures**: 
We plan to assess additional (non-topical relevance) aspects: 

- Text **complexity**:
  - Easy (0)
  - Difficult (1)
  - Very difficult (2)
- Source **credibility**: 
  - Low (0)
  - Medium (1)
  - High credibility (2)

We plan to provide additional evaluation scores based on these aspects.


## Task 2: Complexity Spotting: Identifying and explaining difficult concepts for general audience

The goal of this task is:
1. to decide which terms (up to 5) require explanation and contextualization to help a reader to understand a complex scientific text – for example, with regard to a query, terms that need to be contextualized (with a definition, example and/or use-case)
2. to provide short (one/two sentence) explanations/definitions for the detected difficult terms. For the abbreviations, the definition would be the extended abbreviation.

For each passage, participants should provide a ranked list of difficult terms with corresponding scores on the scale 1-3 (3 to be the most difficult terms, while the meaning of terms scored 1 can be derived or guessed) and definitions.  Passages (sentences) are considered to be independent, i.e. difficult term repetition is allowed.

Term pooling and automatic metrics (accuracy of term binary classification, NDCG for term ranking, kappa statistics, similarity of the provided definitions to ground-truth definitions…) will be used to evaluate these results.

## Task 3: Text Simplification: Scientific text simplification  

The goal of this task is to provide a simplified version of text passages. Participants will be provided with the popular science articles and queries and matching abstracts of scientific papers. The abstracts can be split into sentences. As in 2022, we will evaluate the complexity of the provided simplifications as well as the errors and information distortion which might occur in the simplification process. In 2023, we will *expand the training and evaluation data and focus on large-scale automatic evaluation measures (SARI, ROUGE, compression, readability)*, supplemented with small-scale detailed human evaluation of other aspects.

## Task 4: SOTA: Tracking the state-of-the-art in scholarly publications

Leaderboards are like scoreboards that display top AI model results for specific tasks, datasets, and metrics. Traditionally community-curated, as seen on paperswithcode.com, text mining could speed up their creation. The goal is to develop systems that recognize if an incoming AI paper reports model performances on benchmark datasets. If it does, the model should extract all related (task, dataset, metric, score) tuples that are reported in the work.
