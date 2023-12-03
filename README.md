BIOMEDICAL NER
 INTRODUCTION
● Recognition of biomedical entities in biomedical research papers is a challenging task.
● Biomedical NER aims to recognize biomedical entities - chemicals, diseases, proteins and genes in 
a given text.
● Named entity recognition involves recognizing numerous domain-specific proper nouns in a
biomedical corpus.
● BioBERT directly learns WordPiece embeddings during pre-training and fine-tuning.
● For the evaluation metrics of NER, we used F1 score.
 NAMED ENTITY RECOGNITION

<img width="517" alt="image" src="https://github.com/hhtmy/Biomedical_named_entity_recogniton/assets/126352630/03f4e178-a3bb-421a-84d7-cbf352432281">

 DATA USED
 
● BC5CDR - 1500 PubMed articles 
○ 4409 chemicals
○ 5818 diseases
○ 3116 chemical-disease interactions

● CHEMPROT - 1820 PubMed articles

○ Chemical-protein interactions annotated by domain experts
○ Used in the BioCreative VI text mining chemical-protein interactions shared task.
○ Contains entities such as Chemical , GENE

DATA FORMATS


<img width="635" alt="image" src="https://github.com/hhtmy/Biomedical_named_entity_recogniton/assets/126352630/cd864867-b662-4958-b23c-8c7d5dd89e43">


<img width="673" alt="image" src="https://github.com/hhtmy/Biomedical_named_entity_recogniton/assets/126352630/7177e950-66cb-4af7-a5cc-bf1f3b3f23a5">

BIOBERT - Bidirectional Encoder Representations from Transformers for 
Biomedical Text Mining
● Directly applying the advancements in NLP to biomedical text mining often yields 
unsatisfactory results due to a word distribution shift from general domain corpora to 
biomedical corpora.
● BioBERT which is a domain-specific language representation model pre-trained on 
large-scale biomedical corpora.
● BioBERT largely outperforms BERT and previous state-of art models
● BioBERT significantly outperforms them on biomedical text mining tasks such as NER , RE 
and QA

<img width="713" alt="image" src="https://github.com/hhtmy/Biomedical_named_entity_recogniton/assets/126352630/4664e466-5af2-4e03-86b0-5d161621ebee">

<img width="668" alt="image" src="https://github.com/hhtmy/Biomedical_named_entity_recogniton/assets/126352630/1feb10e4-f953-49e2-99a9-c32d07166f6c">

RESULTS

<img width="665" alt="image" src="https://github.com/hhtmy/Biomedical_named_entity_recogniton/assets/126352630/304509cb-3e1e-44bf-a5a0-23e09f374fde">


The obtained F1 score for one epoch is approximately 80%


 CONCLUSION
 
● We have successfully built a generalised model with approximately 80% F1 score for the 
prediction of chemical, disease and gene in the research articles.
● We can attain more accuracy if we train the model on more epochs with high GPU 
acceleration. 
● We have fine-tuned the model with the help of pytorch lightning
