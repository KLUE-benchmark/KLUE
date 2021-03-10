# Korean Language Understanding Evaluation (a.k.a KLUE) 

The KLUE project is introduced by [UpstageAI](https://www.upstage.ai/) to make advances in Korean NLP. Korean pre-trained language models(PLMs) have appeared to solve Korean NLP problems since PLMs have brought significant performance gains in NLP problems in other languages. Despite the proliferation of Korean language models, however, none of the proper evaluation datasets has been opened yet. The lack of such benchmark dataset limits the fair comparison between the models and further progress on model architectures.

## Goal
1. KLUE project aims to build a **trustworthy** evaluation dataset that can be used for both **commercial and non-commercial purposes**. 
2. Our second goal is to release **publicly available Korean Language Models-BERT, RoBERTa, DistilRoBERTa, ELECTRA- as baselines** and summarize **findings from ablation studies on training strategies** of Korean Language Models.
3. We would like to run a fair KLUE leaderboard. Models are compared in terms of their size, inference speed, and so on.

## Benchmark Dataset
KLUE dataset is composed of 9 tasks:
- Named Entity Recognition (NER)
- (Part-Of-Speech) + Dependency Parsing (DP)
- Topic Classification (TC)
- Relation Extraction (RE)
- Natural Language Inference (NLI)
- Sentence Textual Similarity (STS)
- Machine Reading Comprehension (MRC)
- Task-Oriented Dialogue understanding (TOD)

`NOTE`: Details about each dataset - collection, annotation, quality, guidelines, and so on - will be described in the paper.

## Benchmark PLMs
We have trained 4 models: BERT, RoBERTa, DistilRoBERTa, and ELECTRA. All models except distilled one will be released in small, base, and large size. <br>

| Model                | Embedding size | Hidden size | # Layers | # Heads |
|----------------------|----------------|-------------|----------|---------|
| BERT-small           | 512            | 512         | 4        | 8       |
| BERT-base            | 768            | 768         | 12       | 12      |
| BERT-large           | 1024           | 1024        | 24       | 16      |
|                      |                |             |          |         |
| RoBERTa-small        | 768            | 768         | 6        | 12      |
| RoBERTa-base         | 768            | 768         | 12       | 12      |
| RoBERTa-large        | 1024           | 1024        | 24       | 16      |
|                      |                |             |          |         |
| DistilRoBERTa-base   | 768            | 768         | 6        | 12      |
|                      |                |             |          |         |
| ELECTRA-small        | 128            | 256         | 12       | 4       |
| ELECTRA-base         | 768            | 768         | 12       | 12      |
| ELECTRA-large        | 1024           | 1024        | 24       | 16      |


You can find pretraining codes in below repositories:
- [BERT](https://github.com/Korean-Benchmark/KLUE-BERT)
- RoBERTa
- [DistilRoBERTa](https://github.com/Korean-Benchmark/KLUE-DistilBERT)
- [ELECTRA](https://github.com/Korean-Benchmark/KLUE-ELECTRA)

`NOTE`:  All baselines are going to be uploaded in Huggingface Model Hub until the end of March. Stay tuned!

## Baseline Scores

Here are the corresponding KLUE scores on the test set:

| Model                | NER | DP  | TC  | RE  | NLI | STS | MRC | TOD |
|----------------------|-----|-----|-----|-----|-----|-----|-----|-----|
| BERT-small           | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
| BERT-base            | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
| BERT-large           | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
|                      |     |     |     |     |     |     |     |     |
| RoBERTa-small        | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
| RoBERTa-base         | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
| RoBERTa-large        | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
|                      |     |     |     |     |     |     |     |     |
| DistilRoBERTa-base   | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
|                      |     |     |     |     |     |     |     |     |
| ELECTRA-small        | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
| ELECTRA-base         | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |
| ELECTRA-large        | TBA | TBA | TBA | TBA | TBA | TBA | TBA | TBA |


## Leaderboard
TBA (Will be open in March)

## Members
### Researchers
[Sungjoon Park](https://github.com/SungjoonPark), [Jihyung Moon](https://github.com/inmoonlight), [Sungdong Kim](https://github.com/DSKSD), [Wonik Cho](https://github.com/warnikchow), Jiyoon Han, [Jangwon Park](https://github.com/monologg), [Joohong Lee](https://github.com/roomylee), [Junseong Kim](https://github.com/codertimo), Seongbo Jang, Youngsook Song, Chisung Song, Sungwon Ryu, Hyunwoo Kim, Byeongchang Kim, [Seonghyun Kim](https://github.com/MrBananaHuman), Taehwan Oh, Sangwoo Seo, Seungwon Do, [Lucy Park](https://github.com/e9t), Inkwon Lee, Kyungtae Lim, Jay Shin, Younghoon Jeong, Sangjun Koo, [Dongjun Lee](https://github.com/DongJunLee), Jongwon Lee, Juhyun Oh, Sunkyung Kim, Myeonghwa Lee

### Advisors
Alice Oh, Jungwoo Ha, Kyunghyun Cho

## Sponsors
NAVER Corporation, Google, Kakao Enterprise, Selectstar, ScatterLab, Riiid, DeepNatural, KAIST

## License

According to the license terms, we should follow the same license given to the raw corpus. Note that we deliberately chose [CC-BY](https://creativecommons.org/licenses/by/4.0/) or [CC-BY-SA](https://creativecommons.org/licenses/by-sa/4.0/) corpus. <br>
Otherwise, we apply [CC-BY](https://creativecommons.org/licenses/by/4.0/). 

## Disclaimer

This page is tentative and subject to change.
