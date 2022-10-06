# CLEF 2023 SimpleText Track

---

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [CLEF-2022](../2022/clef/en/index)
<!--- <img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">https://simpletext-project.com/2022/clef/') --->

---

<img align="left" src="https://github.com/simpletext-madics/2021/blob/main/clef/simpletext-logo-blue.png?raw=true" width="100"/>  

## SimpleText: Automatic Simplification of Scientific Texts


### Track Description

#### _Topics and Goals_

SimpleText tackles technical and evaluation challenges of scientific information access for laypersons, by providing appropriate reusable data and benchmarks for text simplification, promoting novel research to reduce barriers in understanding complex texts. The goal is to create a simplified summary of multiple scientific documents based on a popular science query which provides our user with an instant simplified overview on the specific topic she is interested in.  

We propose three tasks:  
**(1)** content selection (retrieving relevant abstracts),  
**(2)** complexity spotting (detecting and explaining complex concepts), and  
**(3)** text simplification (rewriting scientific text).  

To face these challenges, SimpleText aims to answer the following research questions: 

**RQ1** - What document and passage should be included in the simplified summary?  
**RQ2** - What kind of background information should be provided (what terms should be contextualized by giving a definition and/or application)?  
**RQ3** - How to improve the readability of a given short text (e.g. by reducing vocabulary and syntactic complexity) without information distortion?   

#### _Significance for the field_

Information access systems provide users with key information from reliable sources such as scientific literature; however, non-experts may tend to avoid these sources due to its complex language or their lack of background knowledge. Text simplification removes some of these barriers. SimpleText will be a step forward to make research really open, accessible and understandable for everyone and help to counter fake news based on scientific results. Simplified texts are more accessible for non-native speakers, young readers and people with reading disabilities. Also, text simplification allows the improvement of natural language processing (NLP) applications, including machine translation results. Automatic text simplification could be useful for various domains such as scientific communication, science journalism, politics, education, and technical writing.  

Information selection (Task 1) is an understudied task in document simplification [1] as existing works mainly focus on word/phrase-level [2] or sentence-level simplifications [3]. Surprisingly, the majority of corpora for sentence-level simplifications [4]–[7] are not direct simplifications of given  sentences but a result of automatic alignment from comparable corpora. In contrast to that, the SimpleText corpus [8] contains directly simplified sentences (truly parallel corpus) and has comparable size (648 sentences for now) to NEWSELA (2,259 sentences). We will continue to feed the SimpleText corpus (Task 3). The lack of background knowledge can become a barrier to reading comprehension and there is a knowledge threshold allowing reading comprehension [9]. Scientific text simplification presupposes the facilitation of readers’ understanding of complex content by establishing links to basic lexicon while traditional methods of text simplification try to eliminate complex concepts and constructions [2]. SimpleText is not limited to a “Split and Rephrase'' task [10] but also aims to provide a sufficient context to a scientific text (Task 2). We will focus on the helpfulness of the provided context. Compare the following two definitions: Hydroxychloroquine (sulfate) is a medication used to prevent and treat malaria; and Hydroxychloroquine is an aminoquinoline that is chloroquine in which one of the N-ethyl groups is hydroxylated at position 2. The second definition might be more concrete, but the first one might be preferable for users not familiar with chemistry.  

As a side result of the evaluation stage, we constructed a very interesting corpus of information distortion during text simplification [8]. To the best of our knowledge this is the first manually annotated corpus of information distortion.  

***

### Scenarios  

Rather than an afterthought, our track is motivated by a concrete use-case of societal importance, which is one of the main differences with earlier work on text simplification looking only at lexical and grammatical complexity in isolation. Hence, the use-case is already discussed above.  

***

### Tasks, evaluation, metrics  

We will keep the 3 shared tasks (and an open task) for 2023 edition. We will reuse data constructed in previous editions with additional topics and additional automatic and manual labels. We will also emphasize automatic evaluation and training using the 2022 data. Although we describe here the intended framework, the details will be discussed during the break-out session at CLEF-2022.  

- **Task 1: Content Selection: Selecting passages to include in a simplified summary**  

Given a popular science article from a major international newspaper, this task aims at retrieving all passages that would be relevant for this article, from a large corpus of scientific abstracts and bibliographic metadata. Relevant passages should relate to any of the topics in the source article. In 2023, _we will continue evaluating on topical relevance, but also on text complexity (using readability measures), and source authoritativeness (using academic impact measures)._

- **Task 2: Complexity Spotting: Identifying and explaining difficult concepts for laypersons**  

The goal of this task is to decide which concepts in scientific abstracts (up to 5) require explanation and contextualization to help a layperson to understand the text. For example, in the context of a query, some key concepts need to be contextualized (with a definition, example and/or use-case). In 2023, we ask participants to identify such concepts and _to provide useful and understandable explanations for them_. We will evaluate concepts in terms of their complexity and the detected concept spans. _We will evaluate the provided explanations in terms of their usefulness with regard to a query as well as their complexity for a lay user_.  

- **Task 3: Text Simplification: Scientific text simplification**  

The goal of this task is to provide a simplified version of text passages. Participants will be provided with the popular science articles and queries and matching abstracts of scientific papers. The abstracts can be split into sentences. As in 2022, we will evaluate the complexity of the provided simplifications as well as the errors and information distortion which might occur in the simplification process. In 2023, we will _expand the training and evaluation data and focus on large-scale automatic evaluation measures (SARI, ROUGE, compression, readability)_, supplemented with small-scale detailed human evaluation of other aspects.  

***

**Acknowledgement**  

SimpleText is supported by the French research network on Big Data - Data Science [MADICS](https://www.madics.fr/). The project was selected for funding by the French National Research Agency (ANR) in October 2022.

***

**References**  

[1]	Y. Zhong, C. Jiang, W. Xu, and J. J. Li, ‘Discourse Level Factors for Sentence Deletion in Text Simplification’, _Proc. AAAI Conf. Artif. Intell._, vol. 34, no. 05, Art. no. 05, Apr. 2020, doi: 10.1609/aaai.v34i05.6520.  

[2]	M. Maddela and W. Xu, ‘A Word-Complexity Lexicon and A Neural Readability Ranking Model for Lexical Simplification’, in _Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing_, Brussels, Belgium, Oct. 2018, pp. 3749–3760. doi: 10.18653/v1/D18-1410.  

[3]	Y. Dong, Z. Li, M. Rezagholizadeh, and J. C. K. Cheung, ‘EditNTS: An Neural Programmer-Interpreter Model for Sentence Simplification through Explicit Editing’, in _Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics_, Florence, Italy, Jul. 2019, pp. 3393–3402. doi: 10.18653/v1/P19-1331.  

[4]	Z. Zhu, D. Bernhard, and I. Gurevych, ‘A Monolingual Tree-based Translation Model for Sentence Simplification’, in _Proceedings of the 23rd International Conference on Computational Linguistics (Coling 2010)_, Beijing, China, Aug. 2010, pp. 1353–1361. Accessed: Apr. 23, 2021. [Online]. Available: https://www.aclweb.org/anthology/C10-1152  

[5]	W. Xu, C. Callison-Burch, and C. Napoles, ‘Problems in Current Text Simplification Research: New Data Can Help’, _Trans. Assoc. Comput. Linguist._, vol. 3, pp. 283–297, Dec. 2015, doi: 10.1162/tacl_a_00139.  

[6]	X. Zhang and M. Lapata, ‘Sentence Simplification with Deep Reinforcement Learning’, in _Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing_, Copenhagen, Denmark, Sep. 2017, pp. 584–594. doi: 10.18653/v1/D17-1062.  

[7]	R. Cardon and N. Grabar, ‘French Biomedical Text Simplification: When Small and Precise Helps’, in _Proceedings of the 28th International Conference on Computational Linguistics_, Barcelona, Spain (Online), 2020, pp. 710–716. doi: 10.18653/v1/2020.coling-main.62.  

[8]	L. Ermakova et al., ‘Overview of the CLEF 2022 SimpleText Lab: Automatic Simplification of Scientific Texts’, _Exp. IR Meets Multilinguality Multimodality Interact. Proc. Thirteen. Int. Conf. CLEF Assoc. CLEF 2022_, vol. 13390, 2022.  

[9]	T. O’Reilly, Z. Wang, and J. Sabatini, ‘How Much Knowledge Is Too Little? When a Lack of Knowledge Becomes a Barrier to Comprehension’:, _Psychol. Sci._, Jul. 2019, doi: 10.1177/0956797619862276.  

[10]	S. Narayan, C. Gardent, S. B. Cohen, and A. Shimorina, ‘Split and Rephrase’, in _Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing_, Copenhagen, Denmark, Sep. 2017, pp. 606–616. doi: 10.18653/v1/D17-1064.  

---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2023/blob/main/clef/en/clef_logo_2023.png?raw=true" width="150">](http://www.clef-initiative.eu/) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">