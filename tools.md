# SimpleText@CLEF-2024 Tools

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organizers](./organizers) | [Contact](./contact) | [CLEF-2023](https://simpletext-project.com/2023/clef/)

---

## Relevant literature & tools
### Task 1: Automatic summarization tools
* Popular rankers are Anserini/Pyserini or trained neural rankers on HuggingFace.
* The track makes an elastic search API available to registered participants.

### Task 2: Terminology management tools
* **IDF**: Robertson, S. (2004), "Understanding inverse document frequency: on theoretical arguments for IDF", Journal of Documentation, Vol. 60 No. 5, pp. 503-520. [https://doi.org/10.1108/00220410410560582](https://doi.org/10.1108/00220410410560582)

### Task 3: Text simplification tools
* **JURASSIC**: AI21 Studio provides access to Jurassic-1 suite of language models. Jurassic-1 Jumbo is the largest model publicly available with no waitlist. The AI21 studio's playground provides ready-to-use promts for text simplification (see De-Jargonizer) [https://www.ai21.com/studio](https://www.ai21.com/studio)
* **GPT-2** is a large-scale unsupervised language model which performs machine translation, question answering, and summarization without task-specific training [https://github.com/openai/gpt-2](https://github.com/openai/gpt-2)
* **Multilingual T5 (mT5)** transformer model can be fine-tuned for text simplification e.g. by using [SimpleT5 library](https://github.com/Shivanandroy/simpleT5/). [https://github.com/google-research/multilingual-t5](https://github.com/google-research/multilingual-t5)
