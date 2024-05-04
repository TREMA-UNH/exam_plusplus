# exam_plusplus
Online Appendix for EXAM++


# TREC  Data Set used in Experimental Evaluation

- **car**: [TREC CAR Y3](http://trec-car.cs.unh.edu/datareleases/) : Comprising 131 queries and 721 query sub-
topics from the TREC Complex Answer Retrieval track. These
were harvested from titles and section headings from school
text books provided in the TQA dataset [13]. The system’s task
is to retrieve Wikipedia passages to synthesize a per-query re-
sponse that covers all query subtopics. Official track metrics
are MAP, NDCG@20, and R-precision; of 22 systems were
submitted to this track, several have identical rankings. We
use 16 distinguishable systems used by Sander et al.



# Workbench Software

All experiments can be reproduced with the [Autograder Workbench](https://github.com/TREMA-UNH/autograding-workbench)  software.




# Data for Reproduction


We provide data used in our EXAM++ evaluation


Each grade annotation appraoch is denoted as a `prompt_class` using different files with grades. All graded files can be obtained [here](https://www.cs.unh.edu/~dietz/EXAMpp/): 

Here configurations for compared methods:

* EXAM++: 
    * prompt_class `QuestionSelfRatedUnanswerablePromptWithChoices`
    * question-set `question-bank`
    * graded file `Thomas-Sun_few-HELM-FagB_few-Sun-FagB-exampp--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`

* Manual EXAM++: 
    * prompt_class `QuestionSelfRatedUnanswerablePromptWithChoices`
    * question-set `tqa`
    * graded file `manual-exampp-examqa--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`

* Manual-EXAM-QA (Using a question answering prompt with word overlap answer verification):
    * prompt_class `QuestionCompleteConcisePromptWithAnswerKey`
    * question-set `tqa`
    * graded file `manual-exampp-examqa--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`

* LLM-verified Manual-EXAM-QA (as previous but with LLM-based answer verification):
    * prompt_class `QuestionCompleteConcisePromptWithT5VerifiedAnswerKey2`
    * question-set `tqa`
    * graded file `llmverified-manual-exam-qa--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`

* Manual-EXAM-Squad2: Using Squad2 fine-tuned T5, with the question-answering pipeline. Answer verification with word overlap answer 
    * prompt_class `QuestionCompleteConcisePromptWithAnswerKey2`
    * question-set `tqa`
    * graded file `manual-exam-squad2--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`
    
* LLM-verified Manual-EXAM-Squad2 (as previous but with LLM-based answer verification): 
    * prompt_class `QuestionCompleteConcisePromptWithT5VerifiedAnswerKey2`
    * question-set `tqa`
    * graded file `llmverified-manual-exam-squad2--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`


* Direct Grading baselines 
    * grading_prompts `Thomas, Sun, Sun_few, HELM, FagB, FagB_few`:
    * graded file `Thomas-Sun_few-HELM-FagB_few-Sun-FagB-exampp--all-benchmarkY3test-qrels-runs-with-text.jsonl.gz`

    
    
Input filed with system responses: `benchmarkY3test-qrels-runs-with-text.jsonl.gz`


<!-- # Scripts --> 

<!-- Please see folder [scripts](scripts) for detailed bash scripts for reproducing results in this paper for each dataset.-->
