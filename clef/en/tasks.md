---

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](simpletex-madics/2022/en/index/index) | [CLEF-2022](../2022/clef/en/index)
<!--- <img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">https://simpletext-project.com/2022/clef/') --->

---

### Tasks, evaluation, metrics  

We will keep the 3 shared tasks (and an open task) for 2023 edition. We will reuse data constructed in previous editions with additional topics and additional automatic and manual labels. We will also emphasize automatic evaluation and training using the 2022 data. Although we describe here the intended framework, the details will be discussed during the break-out session at CLEF-2022.  

- **Task 1: Content Selection: Selecting passages to include in a simplified summary**  

Given a popular science article from a major international newspaper, this task aims at retrieving all passages that would be relevant for this article, from a large corpus of scientific abstracts and bibliographic metadata. Relevant passages should relate to any of the topics in the source article. In 2023, _we will continue evaluating on topical relevance, but also on text complexity (using readability measures), and source authoritativeness (using academic impact measures)._

- **Task 2: Complexity Spotting: Identifying and explaining difficult concepts for laypersons**  

The goal of this task is to decide which concepts in scientific abstracts (up to 5) require explanation and contextualization to help a layperson to understand the text. For example, in the context of a query, some key concepts need to be contextualized (with a definition, example and/or use-case). In 2023, we ask participants to identify such concepts and _to provide useful and understandable explanations for them_. We will evaluate concepts in terms of their complexity and the detected concept spans. _We will evaluate the provided explanations in terms of their usefulness with regard to a query as well as their complexity for a lay user_.  

- **Task 3: Text Simplification: Scientific text simplification**  

The goal of this task is to provide a simplified version of text passages. Participants will be provided with the popular science articles and queries and matching abstracts of scientific papers. The abstracts can be split into sentences. As in 2022, we will evaluate the complexity of the provided simplifications as well as the errors and information distortion which might occur in the simplification process. In 2023, we will _expand the training and evaluation data and focus on large-scale automatic evaluation measures (SARI, ROUGE, compression, readability)_, supplemented with small-scale detailed human evaluation of other aspects.  

***
