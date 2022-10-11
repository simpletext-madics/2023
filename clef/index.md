# CLEF 2023 SimpleText Track

---

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [CLEF-2022](https://simpletext-project.com/2022/clef/en/)

---

<img align="left" src="https://github.com/simpletext-madics/2021/blob/main/clef/simpletext-logo-blue.png?raw=true" width="100"/>  

## SimpleText: Automatic Simplification of Scientific Texts


### Track Description

Users tend to avoid reliable sources such as scientific literature due to their complex vernacular and lacking background knowledge, resorting to shallow and derived sources on the web and in social media--often published for commercial or political incentives, rather than the informational value.   
Text simplification offers the potential to remove some of these access barriers, 
yet despite great progress in recent years, many technical and evaluation problems in this particular setting remain unsolved. 
SimpleText tackles technical and evaluation challenges of scientific information access for laypersons, by providing appropriate reusable data and benchmarks for text simplification, promoting novel research to reduce barriers in understanding complex texts. The goal is to create a simplified summary of multiple scientific documents based on a popular science query which provides our user with an instant simplified overview on the specific topic she is interested in.  We propose three tasks:
* Task 1: content selection (retrieving relevant abstracts);
* Task 2: complexity spotting (detecting and explaining complex concepts);
* Task 3: text simplification (rewriting scientific text).

#### _Topics and Goals_

SimpleText tackles technical and evaluation challenges of scientific information access for laypersons, by providing appropriate reusable data and benchmarks for text simplification, promoting novel research to reduce barriers in understanding complex texts. The goal is to create a simplified summary of multiple scientific documents based on a popular science query which provides our user with an instant simplified overview on the specific topic she is interested in.  

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

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2023/blob/main/clef/slides/clef_logo_2023.png?raw=true" width="150">](http://www.clef-initiative.eu/) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">
