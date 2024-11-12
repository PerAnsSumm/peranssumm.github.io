---
linkTitle: Documentation
title: Introduction
---

👋 Welcome to the official shared task website for PerAnsSumm: Perspective-aware Healthcare answer summarisation, a shared task organised at the CL4Health workshop colocated with NAACL 2025.

In recent years, healthcare community question-answering (CQA) forums have gained popularity, where users seek advice by posting healthcare-related questions and receiv- ing answers from other users. Even though these platforms are not necessarily fre- quented by experts, people often turn to them for their health-related inquiries for rea- sons such as the availability of free information, avoiding medical jargon, discomfort with discussing sensitive personal issues in person, and learning from the first-hand experiences of others [1]. The answers provide various user perspectives, such as per- sonal experiences, factual information, suggestions, and more. For example, Table 1 shows a CQA thread where a user seeks advice on ‘alternatives to gallstone surgery’. In the responses, users offer diverse perspectives: Answer 1 includes general informa- tion, suggestions, personal experiences, and potential implications. Similar trends are observed in the other user responses.

Traditionally, the CQA answer summarization task focuses on a single best-voted answer [2, 3] as a reference summary. However, a single answer does not capture all the perspectives offered in other responses. Moreover, a structured presentation of the information through perspective-specific summaries may be more useful for end users [4, 5]. To address these gaps, this proposal introduces a novel perspective-specific answer summarization task within a CQA setup.

<!--more-->

<!-- This site is a demo of the Hugo Blox Documentation theme. For the full documentation on how to use this template, refer to the [Hugo Blox Documentation](https://docs.hugoblox.com/). -->

## Task Description
Given a question Q, a set of answers A, and perspective categories (‘cause’, ‘suggestion’, ‘experience’, ‘question’, and ‘information’), you are assigned the following two tasks:
1. **Task A:** Identify the spans in the user answers that reflect a particular perspective.
2. **Task B:** Generate a concise summary that represents the underlying perspective contained within the spans across all answers.

## Dataset
We use the PUMA dataset [6], a perspective-aware summary annotated corpus of medical question-answer pairs. The PUMA dataset consists of 3, 167 CQA threads with approximately 10K answers filtered from the Yahoo! L6 corpus. Each answer in PUMA is annotated with five perspective spans: ‘cause’, ‘suggestion’, ‘experience’, ‘question’, and ‘information’. Following the perspective and span annotations, summaries are written for each identified perspective. These summaries are concise representations of the underlying perspectives contained within the spans across all answers. Each CQA thread has up to five perspective-specific summaries.


## Evaluation Metrics

For **Task A** (Span Identification), we use macro-averaged F1 score.

For **Task B** (Summary Generation), we use two sets of evaluation metrics that capture (i) relevance and (ii) factuality.  
* Relevance - ROUGE (R1, R2, and RL) [7], BLEU [8], Meteor [9], and BERTScore [10]
* Factuality - AlignScore [11] and SummaC [12]

## Timeline

**First call for participation:** 12th November, 2024  
**Release of task data (training, validation, seen_test):** 12th November, 2024  
**Release of test data:** 25th January, 2025  
**System submission deadline:** 1st February, 2025  
**Release of final results:** 5th February, 2025  
**System papers due:** 25th February, 2025  
**Notification of acceptance:** 7th March, 2025  
**Camera-ready papers due:**   
**CL4Health Workshop:**  

\* All deadlines are Anywhere on Earth (UTC - 12)

## Organisers
- **Shweta Yadav** - University of Illinois at Chicago, USA
- **Md. Shad Akhtar** - Indraprastha Institute of Information Technology Delhi, India
- **Siddhant Agarwal** - University of Illinois at Chicago, USA

## References

[1] Nestor Alvaro, Mike Conway, Son Doan, Christoph Lofi, John Overington, and Nigel Collier. Crowdsourcing twitter annotations to identify first-hand experiences of prescription drug use. Journal of biomedical informatics, 58:280–287, 2015.

[2] Tanya Chowdhury and Tanmoy Chakraborty. Cqasumm: Building references for community question answering summarization corpora. In Proceedings of the ACM india joint international conference on data science and management of data, pages 18–26, 2019.

[3] Tanya Chowdhury, Sachin Kumar, and Tanmoy Chakraborty. Neural abstractive summarization with structural attention. arXiv preprint arXiv:2004.09739, 2020.

[4] Christopher Tauchmann, Thomas Arnold, Andreas Hanselowski, Christian M Meyer, and Margot Mieskes. Beyond generic summarization: A multi-faceted hierarchical summarization corpus of large heterogeneous data. In Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018), 2018.

[5] Lea Frermann and Alexandre Klementiev. Inducing document structure for aspect-based summarization. In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pages 6263–6273, 2019.

[6] Gauri Naik, Sharad Chandakacherla, Shweta Yadav,and Md Shad Akhtar. No perspective, no perception!! perspective-aware healthcare answer summarization. In Lun-Wei Ku, Andre Martins, and Vivek Srikumar, editors, Findings of the Asso- ciation for Computational Linguistics ACL 2024, pages 15919–15932, Bangkok, Thailand and virtual meeting, August 2024. Association for Computational Linguistics.

[7] Chin-Yew Lin. ROUGE: A package for automatic evaluation of summaries. In Text Summarization Branches Out, pages 74–81, Barcelona, Spain, July 2004. Association for Computational Linguistics.

[8] Kishore Papineni, Salim Roukos, Todd Ward, and Wei-Jing Zhu. Bleu: a method for automatic evaluation of machine translation. In Pierre Isabelle, Eugene Charniak, and Dekang Lin, editors, Proceedings of the 40th Annual Meeting of the Association for Computational Linguistics, pages 311–318, Philadelphia, Pennsylvania, USA, July 2002. Association for Computational Linguistics.

[9] Satanjeev Banerjee and Alon Lavie. METEOR: An automatic metric for MT evaluation with improved correlation with human judgments. In Jade Goldstein, Alon Lavie, Chin-Yew Lin, and Clare Voss, editors, Proceedings of the ACL Workshop on Intrinsic and Extrinsic Evaluation Measures for Machine Translation and/or Summarization, pages 65–72, Ann Arbor, Michigan, June 2005. Association for Computational Linguistics.

[10] Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q. Weinberger, and Yoav Artzi. Bertscore: Evaluating text generation with bert. In International Conference on Learning Representations, 2020.

[11] Yuheng Zha, Yichi Yang, Ruichen Li, and Zhiting Hu. Alignscore: Evaluating factual consistency with a unified alignment function. In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 11328–11348, 2023.