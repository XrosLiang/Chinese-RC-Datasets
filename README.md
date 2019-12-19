# Chinese Machine Reading Comprehension Datasets

**Note that, this repository will be updated irregularly.**

**If you find this repository helpful, please press the star button. Moreover, if you would like to use or repost the content in this repository, please indicate the orignal author and source link.**

## Content

| Section | Description |
|-|-|
| [Chinese Reading Comprehension Datasets](#Chinese-Reading-Comprehension-Datasets) | Describe public Chinese RC datasets |
| [State-of-the-art Systems](#State-of-the-art-Systems) | State-of-the-art systems and results |
| [Chinese Reading Comprehension Evaluations and Competitions](#Chinese-Reading-Comprehension-Evaluations-and-Competitions) | Introductions to Chinese RC competitions |


## Chinese Reading Comprehension Datasets
Here I list several Chinese reading comprehension datasets that are PUBLICLY available (with appropriate technical report or paper). If I missed something, feel free to inform me. Unless indicated, the datasets are in simplified Chinese.

| Dataset  | Genre | Query Type | Answer Type |  Document # | Query # | Download |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| People Daily & Children's Fairy Tale [1] | news & tale | Cloze | word | 28K | 100K | [link](https://github.com/ymcui/Chinese-Cloze-RC) |
| WebQA [2] | Web | User log | entity | - | 42K | [link](http://paddlepaddle.bj.bcebos.com/dataset/webqa/WebQA.v1.0.zip) |
| CMRC 2017 [3] | news | Cloze & Query | word | - | 364K | [link](https://github.com/ymcui/cmrc2017) | 
| DuReader [4] | Web | User log | free form | 1M | 200K | [link](https://github.com/baidu/DuReader) |
| CMRC 2018 [5] | Wiki | Query | Span | - | 18K | [link](https://github.com/ymcui/cmrc2018) |
| DRCD [6]<sup>(tranditional Chinese)</sup> | Wiki | Query | Span | - | 34K | [link](https://github.com/DRCSolutionService/DRCD) |
| C^3 [7] | mixed | Query | choice | 14K | 24K | [link](https://github.com/nlpdata/c3) |
| CMRC 2019 [8] | Story | cloze | Sentence | 1K | 100K | [link](https://github.com/ymcui/cmrc2019) |
| ChID [9] | varies | cloze | idiom | 580K | 729K | [link](https://github.com/zhengcj1/ChID-Dataset) | 

> [1] (Cui et al., 2016) Consensus Attention-based Neural Networks for Chinese Reading Comprehension. In COLING 2016. https://aclanthology.info/papers/C16-1167/c16-1167

> [2] (Li et al., 2016) Dataset and Neural Recurrent Sequence Labeling Model for Open-Domain Factoid Question Answering. In arXiv. https://arxiv.org/abs/1607.06275

> [3] (Cui et al., 2018) Dataset for the First Evaluation on Chinese Machine Reading Comprehension. In LREC 2018. http://www.lrec-conf.org/proceedings/lrec2018/summaries/32.html

> [4] (He et al., 2018) DuReader: a Chinese Machine Reading Comprehension Dataset from Real-world Applications. In ACL 2018 MRQA Workshop. https://aclanthology.info/papers/W18-2605/w18-2605

> [5] (Cui et al., 2018) A Span-Extraction Dataset for Chinese Machine Reading Comprehension. In arXiv. https://arxiv.org/abs/1810.07366

> [6] (Shao et al., 2018) DRCD: a Chinese Machine Reading Comprehension Dataset. In arXiv. https://arxiv.org/abs/1806.00920

> [7] (Sun et al., 2019) Probing Prior Knowledge Needed in Challenging Chinese Machine Reading Comprehension. https://arxiv.org/abs/1904.09679

> [8] (Cui et al., 2019) https://github.com/ymcui/cmrc2019

> [9] (Zheng et al., 2019) ChID: A Large-scale Chinese IDiom Dataset for Cloze Test. https://aclweb.org/anthology/papers/P/P19/P19-1075/


## State-of-the-art Systems
Here I list several state-of-the-art systems (published / unpublished) for these datasets. There is a big chance that I missed something. So feel free to inform me new entries on `Issue` tab.

### People Daily & Children's Fairy Tale
| System  | PD-DEV | PD-TEST | CFT-TEST-AUTO | CFT-TEST-HUMAN | Note |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: | 
| [SAW Reader (Zhang et al., 2018)](https://arxiv.org/pdf/1806.09103.pdf) | 72.8 | 75.1 | - | 43.8 | - |
| [CAW Reader (Zhang et al., 2018)](https://link.springer.com/chapter/10.1007/978-3-319-99495-6_3)| 69.4 | 70.5 | - | 39.7 | - |
| [CAS Reader (Cui et al., 2016)](https://aclanthology.info/papers/C16-1167/c16-1167) | 65.2 | 68.1 | 41.3 | 35.0 | - |
| [AS Reader (Cui et al., 2016)](https://aclanthology.info/papers/C16-1167/c16-1167) | 64.1 | 67.2 | 40.9 | 33.1 | - | 


### CMRC 2017
Leaderboard: https://hfl-rc.github.io/cmrc2017/leaderboard/

#### Cloze Track 
| System  | DEV | TEST | Note |
| :------ | :-----: | :-----: | :-----: |
| 6ESTATES PTE LTD (ensemble) | 81.85 | 81.90 | - |
| SJTU BCMI-NLP (ensemble) | 78.35 | 80.67 | - | 
| YunSiChuangZhi (ensemble) | 79.20 | 80.27 | - | 
| [SAW Reader (Zhang et al., 2018)](https://arxiv.org/pdf/1806.09103.pdf) | 78.95 | 78.80 | - |
| [CAW Reader (Zhang et al., 2018)](https://link.springer.com/chapter/10.1007/978-3-319-99495-6_3) | 77.95 | 78.50 | - |
| [Word + Char + BPE-FRQ (Zhang et al., 2018)](https://arxiv.org/pdf/1811.02364.pdf) | 79.05 | 78.83 | - |

#### User Query Track
| System  | DEV | TEST | Note |
| :------ | :-----: | :-----: | :-----: |
| ECNU (ensemble) | 90.45 | 69.53 | - |
| SXU-3 (single model) | 47.80 | 49.07 | - | 
| ZZU (single model) | 31.10 | 32.53 | - | 


### DuReader
Leaderboard: http://ai.baidu.com/broad/leaderboard?dataset=dureader

| System  | ROUGE-L | BLEU-4 | Note |
| :------ | :-----: | :-----: | :-----: |
| AliReader | 63.48 | 61.54 | - |
| NI-Reader (ensemble) | 63.38 | 59.23 | - |
| mrc_try_mingyan (single model) | 62.20 | 59.72 | - |
| [(Yan et al., 2018)](https://arxiv.org/pdf/1811.11374.pdf) | 50.71 | 49.39 | - |
| [(Li et al., 2018)](http://zhaohuilee.com/files/82.pdf) | 44.95 | 42.68 | - |
| [(Wang et al., 2018)](https://arxiv.org/pdf/1805.02220.pdf) | 44.18 | 40.97 | - |
| [(Xu et al., 2018)](https://www.matec-conferences.org/articles/matecconf/pdf/2018/91/matecconf_eitce2018_02047.pdf) | 39.60 | 34.76 | - |  
| [Match-LSTM (He et al., 2018)](https://aclanthology.info/papers/W18-2605/w18-2605) | 39.2 | 31.9 | - |
| [BiDAF (He et al., 2018)](https://aclanthology.info/papers/W18-2605/w18-2605) | 39.0 | 31.8 | - |


### CMRC 2018
Leaderboard: https://hfl-rc.github.io/cmrc2018/open_challenge/

| System  | DEV-EM | DEV-F1 | TEST-EM | TEST-F1 | CHALLENGE-EM | CHALLENGE-F1 | Note |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| P-Reader (single model) | 59.894 | 81.499 | 65.189 | 84.386 | 15.079 | 39.583 | - |
| GM-Reader (ensemble) | 58.931 | 80.069 | 64.045 | 83.046 | 15.675 | 37.315 | - |
| MCA-Reader (ensemble) | 66.698 | 85.538 | 71.175 | 88.090 | 15.476 | 37.104 | - | 
| Z-Reader (single model) | 79.776 | 92.696 | 74.178 | 88.145 | 13.889 | 37.422 | - |
| [SRC->DS(±) (Yang et al., 2019)](https://arxiv.org/abs/1904.06652) | 49.2 | 65.4 | - | - | - | - | - |

> More detailed results can be obtained in [CMRC 2018 Overview](https://arxiv.org/abs/1810.07366).
> Note that, some of the submission are using development set for training as well.

### DRCD
| System  | DEV-EM | DEV-F1 | TEST-EM | TEST-EM | Note |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: |
| [SRC + DS(±) (Yang et al., 2019)](https://arxiv.org/abs/1904.06652) | 55.4 | 67.7 | - | - | - |
| r-net (single model) | - | - | 29.1 | 44.4 | - |


### C^3
| System  | DEV-1A | TEST-1A | DEV-1B | TEST-1B | DEV-2A | TEST-2A | DEV-2B | TEST-2B | Note |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| [BERT_CN (Sun et al., 2019)](https://arxiv.org/abs/1904.09679) | 63.0 | 62.6 | 62.3 | 62.1 | 36.7 | 26.2 | 34.7 | 31.3 | - |


## Chinese Reading Comprehension Evaluations and Competitions
Along with the release of these datasets, there are also several Chinese Reading Comprehension evaluation workshops or competitions which further accelerate the research on this topic.

> 1. [The First Evaluation Workshop on Chinese Machine Reading Comprehension (CMRC 2017)](https://hfl-rc.github.io/cmrc2017/)  
Host: [CIPS-CL](http://www.cips-cl.org), [Joint Laboratory of HIT and iFLYTEK Research (HFL)](https://hfl-rc.github.io), [iFLYTEK Co. Ltd](http://www.iflytek.com)  
Competition Type: Cloze-style RC, User Query RC

> 2. [The Second Evaluation Workshop on Chinese Machine Reading Comprehension (CMRC 2018)](https://hfl-rc.github.io/cmrc2018/)  
Host: [CIPS-CL](http://www.cips-cl.org), [Joint Laboratory of HIT and iFLYTEK Research (HFL)](https://hfl-rc.github.io), [iFLYTEK Co. Ltd](http://www.iflytek.com)  
Competition Type: Span-Extraction RC  

> 3. [2018 NLP Challenge on Machine Reading Comprehension](http://mrc2018.cipsc.org.cn/)  
Host: [CCF](https://www.ccf.org.cn), [CIPSC](http://www.cipsc.org.cn), [Baidu Inc.](http://home.baidu.com)  
Competition Type: Open-Domain RC  

> 4. [CIPS-SOGOU QA Competition](http://task.www.sogou.com/cips-sogou_qa/)  
Host: [CIPSC](http://www.cipsc.org.cn), [SOGOU](http://www.sogou.com)  
Competition Type: Factoid QA, Non-Factoid QA  

> 5. [The Third Evaluation Workshop on Chinese Machine Reading Comprehension (CMRC 2019)](https://hfl-rc.github.io/cmrc2019/)  
Host: [CIPS-CL](http://www.cips-cl.org), [Joint Laboratory of HIT and iFLYTEK Research (HFL)](https://hfl-rc.github.io), [iFLYTEK Co. Ltd](http://www.iflytek.com)  
Competition Type: Sentence Cloze  

> 6. [2019 NLP Language and Intelligence Challenge](http://lic2019.ccf.org.cn)  
Host: [CCF](https://www.ccf.org.cn), [CIPSC](http://www.cipsc.org.cn), [Baidu Inc.](http://home.baidu.com)  
Competition Type: Open-Domain RC  

> 7. [Chinese Idiom Understanding Contest](https://biendata.com/competition/idiom/)  
Host: [CCF](https://www.ccf.org.cn), Tsinghua University  
Competition Type: Cloze Test


## Contact
For any problems, please leave a message in the `Github Issues`.


## Disclaimer
Any subjective comments in this repository only represents the idea of the owner (ymcui), and does not represent the claims of any organizations.
