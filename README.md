# Event Centric AI Research (Survey)

### Content
- ##### [Introduction](#Intro)
- ##### [Events in NLP/NLU](#NLP_Tasks)
- ##### [Events in CV](#CV_Tasks)
- ##### [Methodology](#Methods)
- ##### [Acknowledgements](#Ack)

## <a name="Intro"></a> Introduction
Human languages always involve the description of real-world events, and so do millions of videos on the Internet. 

## <a name="NLP_Tasks"></a> NLP Tasks
### 0. Annotation Efforts
- [TAC KBP 2017 Event Sequence Annotation Guidelines v1.1](http://cairo.lti.cs.cmu.edu/kbp/2017/event/TAC_KBP_2017_Event_Coreference_and_Sequence_Annotation_Guidelines_v1.1.pdf)

### 1. Event extraction (Detection)
#### Datasets
- [ACE 2005](https://catalog.ldc.upenn.edu/LDC2006T06): provides entity, value, time, relation, and event annotations for English, Chinese, and Arabic.
- [REO](): the Rich Event Ontology (REO) ([Brown et al., 2017](https://aclanthology.org/W17-2712/)) unifies two existing knowledge resources (i.e., FrameNet ([Fillmore et al., 2003](https://framenet.icsi.berkeley.edu/fndrupal/)) and VerbNet ([Kipper et al., 2008](https://verbs.colorado.edu/verbnet/))) and two event annotated datasets (i.e., ACE ([Doddington et al., 2004](https://aclanthology.org/L04-1011/)) and ERE ([Song et al., 2015](https://aclanthology.org/W15-0812/))) to allow users to query multiple linguistic resources and combine event annotations. 
- [MAVEN](https://www.aclweb.org/anthology/2020.emnlp-main.129.pdf): select 4,480 documents in total, covering 90 of the 95 major event topics defined in EventWiki. 
#### Models
- [Lin et al., ACL'20](https://www.aclweb.org/anthology/2020.acl-main.713.pdf): OneIE

### 2. Event Coreference Resolution
#### Datasets
- [ECB+](http://www.lrec-conf.org/proceedings/lrec2014/pdf/840_Paper.pdf)
#### Models
- [Upadhyay et al., COLING'16](https://aclanthology.org/C16-1183.pdf)
- [Choubey et al., ACL'18](https://aclanthology.org/P18-1045.pdf)
- [Choubey et al., EACL'21](https://aclanthology.org/2021.eacl-main.101.pdf)
- [Lai et al., NAACL'21](https://aclanthology.org/2021.naacl-main.274.pdf)

### 3. Temporal Relation & Duration
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
- [Pustejovsky et al., 2003; Chklovski and Pantel, 2004; Bethard, 2013; Llorens et al., 2010; D’Souza and Ng, 2013; Chambers et al., 2014]()
- [Ning et al. (TCR), ACL'18](https://www.aclweb.org/anthology/P18-1212.pdf): TCR (71.1 in F1)
- [Ning et al. (MATRES), ACL'18](https://www.aclweb.org/anthology/P18-1122.pdf): MATRES (69.0 in F1)
- [Ning et al., EMNLP'19](https://www.aclweb.org/anthology/D19-1642.pdf): MATRES (76.7 in F1), TCR (78.6 in F1)
- [Han et al., EMNLP'19](https://www.aclweb.org/anthology/D19-1041.pdf): MATRES (59.6 in F1, *End-to-end*), TB-Dense (49.4 in F1, *End-to-end*)
- [Han et al., CoNLL'19](https://www.aclweb.org/anthology/K19-1062.pdf): MATRES (81.7 in F1), TB-Dense (63.2 in F1), TCR (80.9 in F1)
- [Han et al., EMNLP'20](https://www.aclweb.org/anthology/2020.emnlp-main.461.pdf): TB-Dense (50.5 in F1, *End-to-end*), 2012 i2b2 Challenge (77.3 in F1, *End-to-end*)
- [Yang et al., EMNLP'20 (Findings)](https://aclanthology.org/2020.findings-emnlp.302.pdf)
- [Han et al., NAACL'21 Demo](https://www.aclweb.org/anthology/2021.naacl-demos.7.pdf): TB-Dense (64.5 in F1), MATRES (75.5 in F1)
- [Wen et al., NAACL'21 Demo](https://www.aclweb.org/anthology/2021.naacl-demos.16.pdf): MATRES (78.8 in F1), MATRES-b (89.6 in Acc.)

### 4. Causal relations et al. (pre-condition, enablement, counterfactual, implicit causal)
#### Datasets
- [RED](https://www.aclweb.org/anthology/W16-5706.pdf)
- [CaTeRs](https://www.aclweb.org/anthology/W16-1007.pdf)
- [ESTER](https://arxiv.org/pdf/2104.08350.pdf): five types of event semantic relations: CAUSAL, SUB-EVENT, CO-REFERENCE, CONDITIONAL and COUNTERFACTUAL
#### Models
- [Girju, 2003; Bethard and Martin, 2008; Riaz and Girju, 2010; Do et al., 2011; Riaz and Girju, 2013; Mirza and Tonelli, 2014, 2016]()
- [Segers et al., LREC'18](https://aclanthology.org/L18-1725.pdf)
- [Ning et al., ACL'18](https://www.aclweb.org/anthology/P18-1212.pdf): TCR (77.3 in F1)
- [Gao et al., NAACL'19](https://aclanthology.org/N19-1179.pdf)

### 5. Super-sub (parent-child) relations / Event Hierarchy Construction
#### Datasets
- [RED](https://www.aclweb.org/anthology/W16-5706.pdf)
- [HiEve](http://www.lrec-conf.org/proceedings/lrec2014/pdf/1023_Paper.pdf): randomly selected 100 documents from the GraphEve corpus, which contains gold-annotated event mentions; given a pair of event mentions, annotators were instructed to annotate one of the following relation types: SuperSub, SubSuper, Coref, NoRel
- [IC](https://www.aclweb.org/anthology/W13-1203.pdf): 100 texts in the IC domain; annotated only instances of full coreference, Subevent, and Member relations
- [ESTER](https://arxiv.org/pdf/2104.08350.pdf)
#### Models
- [Araki et al., LREC'14](http://www.lrec-conf.org/proceedings/lrec2014/pdf/963_Paper.pdf): We used a corpus consisting of 65 newspaper articles in the IC domain.
- [Badgett et al., EMNLP'16](https://aclanthology.org/D16-1088.pdf)
- [Yao et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.430.pdf)

### 6. Essentiality & Salience
#### Datasets
#### Models
- [Upadhyay et al., EVENTS WS'16](https://aclanthology.org/W16-1001.pdf)
- [Choubey et al., NAACL'18](https://aclanthology.org/N18-2055.pdf)
- [Jindal et al., COLING'20](https://aclanthology.org/2020.coling-main.10.pdf)
- [Zhang et al., ongoing]

### 7. Goal / Intention Detection
#### Models
- [Zhang et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.374v2.pdf)
- [Lyu et al., AACL'20](https://aclanthology.org/2020.aacl-main.35.pdf)
- [Chen et al., CoNLL'20](https://aclanthology.org/2020.conll-1.43.pdf)

### 8. Implicit Events
- [Zhou et al., NAACL'21](https://aclanthology.org/2021.naacl-main.107.pdf)

### 9. Schema Induction
#### Models
- [Li et al., EMNLP'20](https://www.aclweb.org/anthology/2020.emnlp-main.50.pdf): Event Graph Schema, where two event types are connected through multiple paths involving entities that fill important roles in a coherent story; introduce Path Language Model, an auto-regressive language model trained on event-event paths,  and select salient and coherent paths to probabilistically construct these graph schemas. 
- [Zhang et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.119.pdf): leverages analogies among processes and conceptualization of sub-event instances to predict the whole sub-event sequence of previously unseen open-domain processes

### Event & Discourse
- [Dai et al., EMNLP'19](https://aclanthology.org/D19-1295.pdf): propose a regularization approach that tightly integratesthese constraints with contexts for deriving word representations
- [Choubey et al., ACL'20](https://aclanthology.org/2020.acl-main.478.pdf)
- [Chen et al., AACL'20](https://aclanthology.org/2020.aacl-main.81.pdf)

### 10. Event Representation & Application
#### Models
- [Chaturvedi et al., EMNLP'17](https://aclanthology.org/D17-1168.pdf): Event Prediction
- [Peng et al., CoNLL'17](https://aclanthology.org/K17-1019.pdf): 
- [Peng et al., CoNLL'19](https://aclanthology.org/K19-1051/): EventLM
- [Zeng et al., TextGraphs'21](https://www.aclweb.org/anthology/2021.textgraphs-1.5.pdf): Event Network Embedding, aiming at representing events with low-dimensional and informative embeddings by incorporating neighboring events; Event Network constructed from one VOA news article, where events are connected through entities involved; 

### 11. Common Sense & Knowledge
#### Models
- [Ning et al., NAACL'18](https://aclanthology.org/N18-1077.pdf)
- [Yao et al., ACL'18](https://aclanthology.org/P18-1050.pdf): explored narratology principles and built a weakly supervised approach that identifies 287k narrative paragraphs from three large text corpora; then extracted rich temporal event knowledge from these narrative paragraphs.   
- [Zhou et al., ACL'20](https://aclanthology.org/2020.acl-main.678.pdf)
- [Yao et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.430.pdf)
- [Choubey et al., EACL'21](https://aclanthology.org/2021.eacl-main.101.pdf)

### 12. Event Knowledge Graphs
- [EventKG](https://arxiv.org/pdf/1804.04526.pdf): A Multilingual Event-Centric Temporal Knowledge Graph
- [ASER](https://hkust-knowcomp.github.io/ASER/html/index.html): Activities, States, Events, and their Relations
- [EventWiki](https://www.aclweb.org/anthology/L18-1079.pdf): EventWiki concentrate on major events, in which all entries in EventWiki are important events in mankind history. 


## <a name="CV_Tasks"></a> Events in CV
### 1. Event Extraction
#### Datasets
- [Li et al., ACL'20](https://aclanthology.org/2020.acl-main.230.pdf): Video M2E2
#### Models
- [Jin et al., IEEE Transactions on Multimedia'21](https://ieeexplore.ieee.org/document/9405453)
- [Wen et al., NAACL'21 Demo](https://www.aclweb.org/anthology/2021.naacl-demos.16.pdf): Video M2E2 (70.0 in Acc.)
### 2. Event Grounding
#### Models
- [Bao et al., AAAI'21](https://ojs.aaai.org/index.php/AAAI/article/view/16175)
### 3. Action Localization & Event Captioning
#### Models
- [Krishna et al., ICCV'17](https://openaccess.thecvf.com/content_ICCV_2017/papers/Krishna_Dense-Captioning_Events_in_ICCV_2017_paper.pdf)
- [Gong et al., IJCAI'21](http://www.muyadong.com/publication.html)
### 4. Event Prediction
- [Lei et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.706.pdf)



## <a name="Methods"></a> Methodology
### 1. Meta-Learning
- [Finn et al., ICML'17](http://proceedings.mlr.press/v70/finn17a/finn17a.pdf)
- [Bansal et al., COLING'20](https://aclanthology.org/2020.coling-main.448.pdf)
- [Yin et al., arXiv preprint'20](https://arxiv.org/pdf/2007.09604.pdf)
- [Deng et al., WSDM'20](https://dl.acm.org/doi/pdf/10.1145/3336191.3371796): propose a Dynamic-Memory-Based Prototypical Network (DMB-PN), which exploits Dynamic Memory Network (DMN) to not only learn better prototypes for event types, but also produce more robust sentence encodings for event mentions
### 2. Constrained Learning
- [Han et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.461.pdf): propose a framework that enhances deep neural network with distributional constraints constructed by probabilistic domain knowledge. We solve the constrained inference problem via Lagrangian Relaxation and apply it to end-to-end event temporal relation extraction tasks
- [Wang et al., EMNLP'20](https://aclanthology.org/2020.emnlp-main.51.pdf)
### 3. Zero-shot (few-shot) Learning
- [Zhang et al., ACL'21 (Findings)](https://arxiv.org/abs/2012.15243)
- [Lyu et al., ACL'21]()
### 4. Graph Networks
- [Chen et al., AACL'20](https://aclanthology.org/2020.aacl-main.81.pdf): build graphs with candidate role filler extractions enriched by sentential embeddings as nodes, and use graph attention networks to identify event regions in a document and aggregate event information
- [Wen et al., NAACL'21](https://aclanthology.org/2021.naacl-main.6.pdf)
### 5. Noisy Labels
- [Zhou et al., arXiv preprint'21](https://arxiv.org/pdf/2104.08656.pdf)
### 6. Pre-training
- [Zhou et al., ACL'20](https://aclanthology.org/2020.acl-main.678.pdf): proposes a novel sequence modeling approach that exploits explicit and implicit mentions of temporal common sense, extracted from a large corpus, to build TACOLM, a temporal common sense language model.
- [He et al., ACL'20](https://aclanthology.org/2020.acl-main.772.pdf): QUASE learns representations from QA data, using BERT or other state-of-the-art contextual language models


## <a name="Ack"></a> Professors Working on Events
- Dan Roth, Heng Ji, Ruihong Huang, Claire Cardie, Nanyun Peng, Chris Callison Burch, Martha Palmer, Eduard Hovy, Yadong Mu
