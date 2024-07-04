MEDIQA @ ACL-BioNLP 2019  -- Task 3: Question Answering (QA)


==============================
Task3: Question Answering (QA)
============================== 

Participants are tasked to:
- filter/classify the provided answers (1: correct, 0: incorrect). 
- re-rank the answers.  

Reuse of the systems developed in the first and second tasks is highly encouraged.

- For instance: 
i) the RQE system could be used to retrieve answered questions (e.g. from the MedQuAD dataset **) that are entailed from the original questions and use their answers to validate the system's answers and re-rank them; 
ii) the NLI system could be used to identify the relations (i.e. entailment, contradiction, neutral) between the answers of the same question, as well as the answers of the questions related by the entailment relation.
   
- We encourage all other ideas and approaches for using textual inference and question entailment to filter and re-rank the retrieved answers.  



========================
Task3-QA: Training Sets 
========================

We provide two datasets of medical questions and the associated answers retrieved by CHiQA (https://chiqa.nlm.nih.gov/): 

    1) MEDIQA2019-Task3-QA-TrainingSet1-LiveQAMed.xml => 104 consumer health questions covering different types of questions about diseases and drugs (TREC-2017-LiveQA medical test questions), and the associated answers. 

    2) MEDIQA2019-Task3-QA-TrainingSet2-Alexa.xml => 104 simple questions about the most frequent diseases (dataset named Alexa), and the associated answers. 

a) SystemRank: corresponds to CHiQA's rank. 

b) ReferenceRank: corresponds to the correct rank. 

c) ReferenceScore: is an additional score that we provide only in the training and validation sets, and that corresponds to the manual judgment/rating of the answer [4: Excellent, 3: Correct but Incomplete, 2: Related, 1: Incorrect].  

For the answer classification task: answers with scores 1 and 2 are considered as incorrect (label 0), and answers with scores 3 and 4 are considered as correct (label 1).  
 
===================================
Task3-QA: Validation & Test Sets
===================================

The validation and test sets are generated from a recent version of the medical QA system CHiQA, and cover similar types of questions about diseases and drugs.  

The test set has the same format, the answers are sorted by SystemRank (CHiQA's rank).    

<Question QID="">
        <QuestionText></QuestionText>
        <AnswerList>
            <Answer AID="">
                <AnswerURL></AnswerURL>
                <AnswerText></AnswerText>
            </Answer>
        <AnswerList>
 </Question>

If you use the QA training, validation or test sets, please cite our overview paper:     

Asma Ben Abacha, Chaitanya Shivade, and Dina Demner-Fushman. Overview of the MEDIQA 2019 Shared Task on Textual Inference, Question Entailment and Question Answering. ACL-BioNLP 2019. 



