# PKBQAC Dataset

A Dataset for Personal Knowledge Base Question Ansewring and Unanswerable Question Correction
# Introduction
Previous works on knowledge base question answering focus on finding answers for answerable questions. In the real world applications, however, people often muddle up facts and ask those questions that cannot be answered with knowledge base. The personal knowledge base ([LiveKB](https://github.com/ntunlplab/Lifelog-LiveKB)) consists of 137 relations and 15,525 events written in Chinese collected from Twitter 18 users. In the construction of the dataset, we manully generate seven types of questions, including "who", "what", "where", "when", "how many", "duration", and "True or False". In summary, there are two types of answerable questions: (1) the answers can be retrieved from the KB, and (2) the questions can be answered with "True" or "False" based on the KB. The rest of the questions are unanswerable. As a result, the dataset contains 41,960 distinct Chinese questions, where the numbers of answerable and unanswerable questions are 38,201 and 3,759, respectively.

20210929 update dataset: correct some annotations of question type.

# Format
Each entry in the JSON format is consisted of "tweet_id" (the ids of the related tweets), "answerable" (is the question answerable), "question", and "correct_questions" (the possible corrected questions of the unanswerable question).

"question" and "correct_questions" are consist of "question" and "triple_mentions", where triples in "triple_mentions" means which events comprise the question, and the answer is in "tripleA".

# Example
```yaml
  {'answerable': False,
 'correct_questions': [{'question': '我租什么去北横经过外澳服务区伯朗咖啡',
                        'triple_mentions': {'time_info': {'index': None,
                                                          'mention': None},
                                            'tripleA': {'object': '单车',
                                                        'object_index': None,
                                                        'subject': '租',
                                                        'subject_index': '0',
                                                        'time': None,
                                                        'time_index': None},
                                            'tripleB': {'object': '外澳服务区伯朗咖啡',
                                                        'object_index': '9-17',
                                                        'subject': '去',
                                                        'subject_index': '0',
                                                        'time': None,
                                                        'time_index': None},
                                            'tripleC': {'object': '北横',
                                                        'object_index': '5-6',
                                                        'subject': '去',
                                                        'subject_index': '0',
                                                        'time': None,
                                                        'time_index': None}}}],
 'question': {'question': '我租什么去基隆火车站经过外澳服务区伯朗咖啡',
              'triple_mentions': {'tripleA': {'object': '车',
                                              'object_index': '8',
                                              'predicate': '租',
                                              'predicate_index': '1',
                                              'subject': '我',
                                              'subject_index': '0',
                                              'time': None,
                                              'time_index': None},
                                  'tripleB': {'object': '外澳服务区伯朗咖啡',
                                              'object_index': '12-20',
                                              'predicate': '去',
                                              'predicate_index': '4',
                                              'subject': '我',
                                              'subject_index': '0',
                                              'time': None,
                                              'time_index': None},
                                  'tripleC': {'object': '基隆火车站',
                                              'object_index': '5-9',
                                              'predicate': '经过',
                                              'predicate_index': '10-11',
                                              'subject': '我',
                                              'subject_index': '0',
                                              'time': None,
                                              'time_index': None}}},
 'question_type': 'what',
 'tweet_id': ['63166644754710528',
              '63414743309877248',
              '63568196883578880',
              '64215735244816384',
              '64232645214740480',
              '64280754770812928',
              '64336905436807168',
              '64341700734226432',
              '64503447835250690',
              '64540594885767168',
              '64578159307264001',
              '64654201615163392',
              '64669311163314176',
              '64671200013594624',
              '64861298684469248',
              '64863620894433280',
              '64877696022347776',
              '64896955318403072',
              '64914000235855872',
              '64960662308265984',
              '64960662366994432',
              '65035030010925056',
              '65040228779425794']}
```
# Download
Please click Google Form to fill out the questionnaire survey, the download link of the PKBQAC dataset will be sent to your e-mail inbox.

Please feel free to contact me if you have any questions.

Email Address: azyen@nlg.csie.ntu.edu.tw

# How to Cite the Corpus
Please cite the following papers when referring to the PKBQAC dataset in academic publications and papers.

An-Zi Yen, Hen-Hsen Huang, and Hsin-Hsi Chen (2021). “Unanswerable Question Correction in Question Answering over Personal Knowledge Base.” In Proceedings of the Thirty-Fifth AAAI Conference on Artificial Intelligence (AAAI-21), February 2-9, 2021.
