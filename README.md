# Korean Language Understanding Evaluation (a.k.a KLUE) 

The KLUE project is introduced by [UpstageAI](https://www.upstage.ai/) to make advances in Korean NLP. Korean pre-trained language models(PLMs) have appeared to solve Korean NLP problems since PLMs have brought significant performance gains in NLP problems in other languages. However, unlike the increasing usage of the Korean models, none of the proper evaluation datasets has been opened yet. The lack of such benchmark dataset limits the fair comparison between the models and further progress on model architectures.

## Goal
1. KLUE project aims to build a **trustworthy** evaluation dataset that can be used for both **commercial and non-commercial purposes**. 
2. Our second goal is to release **publicly available Korean Language Models-BERT, RoBERTa, DistilRoBERTa, ELECTRA- as baselines** and summarize findings from ablation studies on training strategies of Korean Language Models.

### 1. Benchmark Dataset
KLUE dataset is composed of 9 tasks:
- Named Entity Recognition (NER)
- (Part-Of-Speech) + Dependency Parsing (DP)
- Topic Classification (TC)
- Relation Extraction (RE)
- Natural Language Inference (NLI)
- Sentence Textual Similarity (STS)
- Machine Reading Comprehension (MRC)
- Task-Oriented Dialogue understanding (TOD)
- Open-Domain Dialogue understanding (OOD)


### 2. Benchmark PLMs
We have trained 4 models: BERT, RoBERTa, DistilRoBERTa, ELECTRA. All models except distilled one will be released in small, base, and large size. <br>
You can find pretraining codes in below repositories:
- [BERT](https://github.com/Korean-Benchmark/KLUE-BERT)
- RoBERTa
- [ELECTRA](https://github.com/Korean-Benchmark/KLUE-ELECTRA)
- [DistilRoBERTa](https://github.com/Korean-Benchmark/KLUE-DistilBERT)


## Members
### Researchers
[Sungjoon Park](https://github.com/SungjoonPark), [Jihyung Moon](https://github.com/inmoonlight), [Sungdong Kim](https://github.com/DSKSD), [Wonik Cho](https://github.com/warnikchow), Jiyoon Han, [Jangwon Park](https://github.com/monologg), [Joohong Lee](https://github.com/roomylee), [Junseong Kim](https://github.com/codertimo), Seongbo Jang, Youngsook Song, Chisung Song, Sungwon Ryu, Hyunwoo Kim, Byeongchang Kim, [Seonghyun Kim](https://github.com/MrBananaHuman), Taehwan Oh, Sangwoo Seo, Seungwon Do, [Lucy Park](https://github.com/e9t), Inkwon Lee, Kyungtae Lim, Jay Shin, Younghoon Jeong, Sangjun Koo, [Dongjun Lee](https://github.com/DongJunLee), Jongwon Lee

### Advisors
Alice Oh, Jungwoo Ha, Kyunghyun Cho


## Sponsors
NAVER Corporation, Kakao Enterprise, Selectstar, Riiid, DeepNatural, KAIST

## License

According to the license terms, we should follow the same license given to the raw corpus. Note that we deliberately chose [CC-BY](https://creativecommons.org/licenses/by/4.0/) or [CC-BY-SA](https://creativecommons.org/licenses/by-sa/4.0/) corpus. <br>
Otherwise, we apply [CC-BY](https://creativecommons.org/licenses/by/4.0/). 
