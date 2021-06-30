# Event Centric AI Research (Survey)

### Content
- ##### [Introduction](#Intro)
- ##### [Events in NLP/NLU](#NLP_Tasks)
- ##### [Events in CV](#CV_Tasks)
- ##### [Event Knowledge Graphs](#KG_Tasks)
- ##### [Methodology](#Methods)
- ##### [Acknowledgements](#Ack)

## <a name="Intro"></a> Introduction
Human languages always involve the description of real-world events, and so do millions of videos on the Internet. 

## <a name="NLP_Tasks"></a> NLP Tasks
### Event extraction (Detection)
#### Datasets
- [ACE 2005](https://catalog.ldc.upenn.edu/LDC2006T06): provides entity, value, time, relation, and event annotations for English, Chinese, and Arabic.
- [MAVEN](https://www.aclweb.org/anthology/2020.emnlp-main.129.pdf): select 4,480 documents in total, covering 90 of the 95 major event topics defined in EventWiki. 
#### Models
- [OneIE](https://www.aclweb.org/anthology/2020.acl-main.713.pdf)
### Temporal relations
#### Datasets
- [TimeML](https://www.aaai.org/Papers/Symposia/Spring/2003/SS-03-07/SS03-07-005.pdf): a specification language for events and temporal expressions; EVENT, TIMEX3, SIGNAL, and LINK.
- [2012 i2b2 Challenge](https://academic.oup.com/jamia/article/20/5/806/726374): The Sixth Informatics for Integrating Biology and the Bedside (i2b2) Natural Language Processing Challenge for Clinical Records focused on the temporal relations in clinical narratives. 
- [TB-Dense](https://www.aclweb.org/anthology/Q14-1022.pdf): 12,715 labeled relations over 36 TimeBank newspaper articles; TB-Dense has 1.1K verb events, between which 3.4K event-event (EE) relations are annotated (excerpt from MATRES paper); train  / dev / test (doc: 22 / 5 / 9; pair: 4023 / 629 / 1427)
- [RED](https://www.aclweb.org/anthology/W16-5706.pdf): The Richer Event Description (RED) corpus presents 95 documents (totaling 54287 tokens) sampled both from news data and casual discussion forum interactions, which contain 8731 events, 1127 temporal expressions (TIMEX3s, section time, and document time labels), and 10320 entity markables. It contains 2390 identity chains, 1863 bridging relations, and 4969 event-event relations encompassing temporal, causal and subevent relations (as well as aspectual ALINK relations and reporting relations), as well as 8731 DOCTIMEREL temporal annotations linking these events to the document time.
- [TCR](https://www.aclweb.org/anthology/P18-1212.pdf): 25 newswire articles collected from CNN in 2010.
- [MATRES](https://www.aclweb.org/anthology/P18-1122.pdf): 275 documents; 72% of the events (0.8K) are anchored onto the main axis, resulting in 1.6K EE relations, and 16% (0.2K) are anchored onto orthogonal axes, resulting in 0.2K EE relations; train  / dev / test (doc: 183 / 72 / 20; pair: 6332 / - / 827)
- [McTaco](https://www.aclweb.org/anthology/D19-1332.pdf): 13K tuples, in the form of (sentence, question, candidate answer)
- [TORQUE](https://www.aclweb.org/anthology/2020.emnlp-main.88.pdf): a new English reading comprehension benchmark built on 3.2k news snippets with 21k human-generated questions querying temporal relationships
#### Models
- [Ning et al. (TCR), ACL'18](https://www.aclweb.org/anthology/P18-1212.pdf): TCR (71.1 in F1)
- [Ning et al. (MATRES), ACL'18](https://www.aclweb.org/anthology/P18-1122.pdf): MATRES (69.0 in F1)
- [Ning et al., EMNLP'19](https://www.aclweb.org/anthology/D19-1642.pdf): MATRES (76.7 in F1), TCR (78.6 in F1)
- [Han et al., EMNLP'19](https://www.aclweb.org/anthology/D19-1041.pdf): MATRES (59.6 in F1, *End-to-end*), TB-Dense (49.4 in F1, *End-to-end*)
- [Han et al., CoNLL'19](https://www.aclweb.org/anthology/K19-1062.pdf): MATRES (81.7 in F1), TB-Dense (63.2 in F1), TCR (80.9 in F1)
- [Han et al., EMNLP'20](https://www.aclweb.org/anthology/2020.emnlp-main.461.pdf): TB-Dense (50.5 in F1, *End-to-end*), 2012 i2b2 Challenge (77.3 in F1, *End-to-end*)
- [Han et al., NAACL'21 Demo](https://www.aclweb.org/anthology/2021.naacl-demos.7.pdf): TB-Dense (64.5 in F1), MATRES (75.5 in F1)
- [Wen et al., NAACL'21 Demo](https://www.aclweb.org/anthology/2021.naacl-demos.16.pdf): MATRES (78.8 in F1), MATRES-b (89.6 in Acc.)

### Causal relations
#### Datasets
- [RED](https://www.aclweb.org/anthology/W16-5706.pdf)
- [CaTeRs](https://www.aclweb.org/anthology/W16-1007.pdf)
- [ESTER](https://arxiv.org/pdf/2104.08350.pdf): five types of event semantic relations: CAUSAL, SUB-EVENT, CO-REFERENCE, CONDITIONAL and COUNTERFACTUAL
#### Models
- [Ning et al., ACL'18](https://www.aclweb.org/anthology/P18-1212.pdf): TCR (77.3 in F1)

### Super-sub (parent-child) relations / Event Hierarchy Construction
#### Datasets
- [RED](https://www.aclweb.org/anthology/W16-5706.pdf)
- [HiEve](http://www.lrec-conf.org/proceedings/lrec2014/pdf/1023_Paper.pdf): randomly selected 100 documents from the GraphEve corpus, which contains gold-annotated event mentions; given a pair of event mentions, annotators were instructed to annotate one of the following relation types: SuperSub, SubSuper, Coref, NoRel
- [IC](https://www.aclweb.org/anthology/W13-1203.pdf): 100 texts in the IC domain; annotated only instances of full coreference, Subevent, and Member relations
- [ESTER](https://arxiv.org/pdf/2104.08350.pdf)
#### Models
- [Araki et al., LREC'14]: We used a corpus consisting of 65 newspaper articles in the IC domain.

### Schema Induction
#### Models
- [Li et al., EMNLP'20](https://www.aclweb.org/anthology/2020.emnlp-main.50.pdf): Event Graph Schema, where two event types are connected through multiple paths involving entities that fill important roles in a coherent story; introduce Path Language Model, an auto-regressive language model trained on event-event paths,  and select salient and coherent paths to probabilistically construct these graph schemas. 

### Event Embedding
#### Models
- [Zeng et al., TextGraphs'21](https://www.aclweb.org/anthology/2021.textgraphs-1.5.pdf): Event Network Embedding, aiming at representing events with low-dimensional and informative embeddings by incorporating neighboring events; Event Network constructed from one VOA news article, where events are connected through entities involved; 

## <a name="CV_Tasks"></a> Events in CV
### Event Extraction
#### Datasets
- [](): Video M2E2
#### Models
- [Jin et al., IEEE Transactions on Multimedia'21](https://ieeexplore.ieee.org/document/9405453)
- [Wen et al., NAACL'21 Demo](https://www.aclweb.org/anthology/2021.naacl-demos.16.pdf): Video M2E2 (70.0 in Acc.)
### Event Grounding
#### Models
- [Bao et al., AAAI'21](https://ojs.aaai.org/index.php/AAAI/article/view/16175)
### Action Localization 
#### Models
- [Gong et al., IJCAI'21](http://www.muyadong.com/publication.html)

## <a name="KG_Tasks"></a> Event Knowledge Graphs
- [EventKG](https://arxiv.org/pdf/1804.04526.pdf): A Multilingual Event-Centric Temporal Knowledge Graph
- [ASER](https://hkust-knowcomp.github.io/ASER/html/index.html): Activities, States, Events, and their Relations
- [EventWiki](https://www.aclweb.org/anthology/L18-1079.pdf): EventWiki concentrate on major events, in which all entries in EventWiki are important events in mankind history. 

## <a name="Methods"></a> Methodology
- Meta-Learning
- Constrained Learning
- Zero-shot (few-shot) Learning
- Graph Networks
- Noisy Labels: [Zhou et al., preprint'21](https://arxiv.org/pdf/2104.08656.pdf)

## <a name="Ack"></a> Acknowledgements
