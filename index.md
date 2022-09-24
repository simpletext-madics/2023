# CLEF 2023 SimpleText Track

---

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](simpletex-madics/2022/clef/en/contact) |
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

### SimpleText’22 overview and lessons learned  

In the CLEF 2022 edition of SimpleText, a total of 62 teams registered for the SimpleText track [8]. A total of 40 users downloaded data from the server. A total of 9 distinct teams submitted 24 runs, of which 10 runs were updated. Two teams described in their papers their post-submission experience. 6 runs were submitted for Task 1: What is in (or out)? 4 runs were submitted for Task 2: What is unclear? 14 runs were submitted for Task 3: Rewrite this! We have also seen 2 post-submission runs for Task 2 and 1 post-submission runs for Task 3.  

For Task 1, we saw a clear difference in complexity between journalistic and scientific articles.  To bring such aspects into IR, the 2022 topical relevance qrels provide a unique resource that can be reused and enriched with additional judgments.  We can provide sentence-level judgments for known relevant passages, enabling a sentence extraction version of the 2022 task.  Moreover, we can add additional labels on text complexity and credibility of the source publication, based on large-scale automatic and small-scale manual judgments further enriching the 2022 qrels. As the recall base is small, we have to expand the test collection by increasing pooling depth and adding new subtopics and queries for the same set of popular science articles.  

In the 2022 edition, the Task 2 was limited to difficult term spotting however 10 runs for Task 3 provided context for difficult terms besides language simplification. This proves a demand in corpus with explanations of difficult terms integrated in a text. Thus, we will update Task 2 to provide this context besides searching for difficult terms. Evaluation stage allowed to increase the annotated data for term difficulty spotting. We will use these data as a first stage of the annotation for the corpus in 2023 as well as for a partial automatisation of evaluation.  

We observed that many large pre-trained models tend to insert unnecessary and even false information in the simplification due to their generative nature. Dealing with these kinds of information distortion is a problem of current interest in AI. Thus, we will continue to evaluate results with regard to the errors produced during simplification which differs SimpleText from the state-of-the-art text simplification evaluation metrics. For training data for Task 3, we also observe a significant difference in length and complexity between original and simplified sentences. We will continue to collect data and we will add automatic evaluation as a supplement to information distortion evaluation.  

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

### Lab organisers  

**Liana Ermakova (Chair, responsible for Tasks 2 and 3)** is associate professor of computer science at University of Western Brittany, France. She is the PI of the SimpleText project financed by the French National Research Agency (ANR) in 2022-2026. Dr. Ermakova chaired the JOKER@CLEF-2022 and SimpleText@CLEF 2021 and 2022 tracks. She participated in the INEX/CLEF Tweet Contextualization task in 2011-2014 and was co-organizer of CLEF Microblog Cultural Contextualization in 2016 and 2017. She is the main organizer of the SimpleText workshop at MADICS, INFORSID, and Mots/Machines.  

**Eric SanJuan (responsible for Task 1)** is permanent lecturer at the Institute of Technology of Avignon in the department of Statistics and Decision Support Systems (StID). He was co-organiser of the CLEF SimpleText track since 2021 as well as a co-organiser of MADICS and a research partner in the ANR project. Among others, he organized the following scientific activities: CLEF MC2 lab that aimed to evaluate microblog retrieval and contextualization, CLEF 2018 conference in Avignon. https://termwatch.es/  

**Stéphane Huet (Task 1)** is associate professor at the University of Avignon. He was co-organiser of the CLEF SimpleText track in 2022. He participated in CLEF 2016&2017 Cultural Microblog Contextualization Tasks, and in international machine translation tasks (WMT). https://cv.archives-ouvertes.fr/shuet  

**Jaap Kamps (Tasks 1 and 3)** is associate professor of Information Retrieval at the University of Amsterdam. He is a prolific organizer of IR evaluation tracks, including the CLEF SimpleText track since 2021 (also as research partner in the ANR project at Brest), the TREC Contextual Suggestion track 2012-2016, the CLEF Social Book Search track 2015-2016, and the INEX INititative for the Evaluation of XML Retrieval 2008-2014, see: https://e.humanities.uva.nl/  

**Olivier Augereau (Task 2)**, associate professor at École Nationale d'Ingénieurs de Brest (France), is a co-organiser of the SimpleText@MADICS workshop and a member of the French Research Group in Writing Communication (GRCE), which is interested in the SimpleText project. O. Augereau is an invited researcher at Osaka Metropolitan University and senior researcher at KEIO University. He works on text and reader mutual analysis.  

**Patrice Bellot (Task 2)** is a full professor at the University of Aix-Marseille, Laboratoire d'Informatique et Systèmes (LIS - CNRS/Aix-Marseille Université). He is co-organiser of the CLEF SimpleText track since 2021, and research partner in the ANR project. He participated in international challenges such as CLEF Social Book Search for query based recommendation, Semeval for sentiment analysis, TREC and CLEF for question-answering, TREC Entity, KBA, Medical for information retrieval and filtering. Between 2010 and 2014, he organized the Tweet Contextualization track in CLEF along with IRIT and LIMSI labs. https://ins2i.cnrs.fr/fr/personne/patrice-bellot  

A **PhD student** (to be hired on ANR) will work on Tasks 1 and 2 under the supervision of L.  Ermakova and P. Bellot.  

**Other colleagues participate in the Task organization:** Irina Ovchinnikova (ManPower Language Solution, Israel), Diana Nurbakova (INSA Lyon, France), Sílvia Araújo (University of Minho, Portugal), Radia Hannachi (University of South Brittany, France). We will also hire interns in translation and technical writing for data collection and evaluation.  

***

### Details of the expected target audience and how to reach them  

The  target audience are technical students and researchers in IR and NLP. We will also encourage manual runs (students in translation, foreign language teaching - especially Tasks 2 & 3) to enhance data for the next editions.  

SimpleText is labelized by the French research network on Big Data - Data Science [MADICS](https://www.madics.fr/).  We will spread the information via communication service in UBO, SimpleText Google group, mailing lists (SIGIR, info-ic, madics, clef, ntcir, bulle-i3, ln, nlp-seminar, romip, TRANSLATIO@jiscmail.ac.uk, organizers’ university mailing lists), social networks, organizers’ personal pages, the SimpleText project network, network of  the French Groupe of Research in Writing Communication ([GRCE](https://grce.labri.fr/)). We will also advertise the track at CLEF 2022 and ECIR 2023 and other conferences, workshops and local events. We are in contact with researchers who have been working on text simplification in Austria, Japan, Mexico and Russia. We will also propose SimpleText tasks as projects within the class on AI in Engineering School in Brest (France), as projects for master students in translation in UBO (France) and as a part of the intensive course on AI open for 9 universities of the [SEA-EU Alliance](https://sea-eu.org/).  

***

### Expected length of the lab session at the conference: half-day  

  -  45 min invited talk + 15 min for questions
  -  1h round table
  -  2h30 for presentations (~10 presentations of 15 min)  

**Acknowledgement**  

SimpleText is supported by the French research network on Big Data - Data Science [MADICS](https://www.madics.fr/). The project was selected for funding by the French National Research Agency (ANR) in October 2022.  

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

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-2021.png?raw=true" width="150">](http://www.clef-initiative.eu/) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">](http://clef2021.clef-initiative.eu/) 
