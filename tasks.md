# SimpleText@CLEF-2024 Tasks

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organizers](./organizers) | [Contact](./contact) | [CLEF-2023](https://simpletext-project.com/2023/clef/)

---
## How to participate
In order to participate, you should sign up at the [CLEF](https://clef2024.clef-initiative.eu/index.php) website: [http://clef2024-labs-registration.dei.unipd.it/](http://clef2023-labs-registration.dei.unipd.it/). 

All team members should join the SimpleText mailing list:
[https://groups.google.com/g/simpletext](https://groups.google.com/g/simpletext). 

The data will be made available to all registered participants.

## Task 1: Retrieving passages to include in a simplified summary

Given a popular science article targeted to a general audience, this task aims at retrieving passages, which can help to understand this article, from a large corpus of academic abstracts and bibliographic metadata. Relevant passages should relate to any of the topics in the source article. These passages can be complex and require further simplification to be carried out in tasks 2 and 3. Task 1 focuses on content retrieval.

### Data
We use popular science articles as a source for the types of topics the general public is interested in and as a validation of the reading level that is suitable for them. The main corpus is a large set of scientific abstracts plus associated metadata covering the field of computer science and engineering. We reuse the collection of academic abstracts from the Citation Network Dataset ([12th version released in 2020](https://www.aminer.cn/citation). This collection was extracted from DBLP, ACM, MAG (Microsoft Academic Graph), and other sources. It includes, in particular, 4,232,520 abstracts in English, published be-
fore 2020. Search requests are based on popular press articles targeted to a general audience, based on The Guardian and Tech Xplore. Each of these popular science articles represents a general topic that has to be analyzed to retrieve relevant scientific information from the corpus.

We provide the URLs to original articles, the title, and the textual content of each popular science article as a general topic. Each general topic was also enriched with one or more specific keyword queries manually extracted from their content, creating a familiar information retrieval task ranking passages or abstracts in response to a query. Available training data from 2023 includes 29 (train) and 34 (test) queries, with the later set having an extensive recall base due to the large number of submissions in 2023. In 2024, we will extend this test collection with additional test queries.

### Evaluation
Topical relevance was evaluated last year with a 0-2 score on the relevance degree towards the content of the original article. In 2023, we provided an initial analysis of text complexity (based on readability measures) and authoritativeness (based on academic impact measures). In 2024, we plan to provide additional evaluation measures on both topical relevance and complexity/credibility. While these criteria can provide
different levels of comparison between systems, we will continue to provide standard ranking scores based on NDCG.

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
