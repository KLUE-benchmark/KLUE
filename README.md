# KLUE: Korean Language Understanding Evaluation

The KLUE is introduced to make advances in Korean NLP. Korean pre-trained language models (PLMs) have appeared to solve Korean NLP problems since PLMs have brought significant performance gains in NLP problems in other languages. Despite the proliferation of Korean language models, however, none of the proper evaluation datasets has been opened yet. The lack of such benchmark dataset limits the fair comparison between the models and further progress on model architectures.

Along with the benchmark tasks and data, we provide **suitable evaluation metrics** and fine-tuning recipes for pretrained language models for each task. We furthermore release the PLMs, **KLUE-BERT** and **KLUE-RoBERTa**, to help reproducing baseline models on KLUE and thereby facilitate future research.

See [our paper](https://arxiv.org/pdf/2105.09680.pdf) for more details.


## Design Principles
In designing the Korean Language Understanding Evaluation (KLUE) benchmark, we aim to make KLUE;

1. cover **diverse** tasks and corpora
2. **accessible** to everyone without any restriction
3. include **accurate** and unambiguous annotations
4. **mitigate** AI ethical issues.


## Benchmark Datasets
KLUE benchmark is composed of 8 tasks:
- Topic Classification (TC)
- Sentence Textual Similarity (STS)
- Natural Language Inference (NLI)
- Named Entity Recognition (NER)
- Relation Extraction (RE)
- (Part-Of-Speech) + Dependency Parsing (DP)
- Machine Reading Comprehension (MRC)
- Dialogue State Tracking (DST)

See [wiki](https://github.com/KLUE-benchmark/KLUE/wiki) for dataset description. <br>

`NOTE`: In the paper, we describe more in detail how our 4 principles have guided creating KLUE from task selection, corpus selection, annotation protocols, determining evaluation metrics to baseline construction.


## KLUE-PLMs
We have trained 2 models: KLUE-BERT and KLUE-RoBERTa. <br>

| Model                | Embedding size | Hidden size | # Layers | # Heads |
|----------------------|----------------|-------------|----------|---------|
| KLUE-BERT-base            | 768            | 768         | 12       | 12      |
|                           |                |             |          |         |
| KLUE-RoBERTa-small        | 768            | 768         | 6        | 12      |
| KLUE-RoBERTa-base         | 768            | 768         | 12       | 12      |
| KLUE-RoBERTa-large        | 1024           | 1024        | 24       | 16      |

`NOTE`:  All the pretrained models are uploaded in Huggingface Model Hub. Check https://huggingface.co/klue.

## Baseline Scores

Evaluation results of our PLMs and other baselines on KLUE benchmark. **Bold** shows the best performance across the models, and _Italic_ indicates the best performance among `BASE` models.


| Model                    | TC    | STS   |       | NLI   | NER    |        | RE         |       | DP    |       | MRC   |       | DST   |       |
|--------------------------|-------|-------|-------|-------|--------|--------|------------|-------|-------|-------|-------|-------|-------|-------|
|                          | F1    | Pearsons' r | F1    | ACC   | entity F1 | char F1 | F1 | AUPRC | UAS   | LAS   | EM    | ROUGE | JGA   | Slot F1    |
| **mBERT-base** | 81.55 | 84.66 | 76.00 | 73.20 | 76.50 | 89.23 | 57.88 | 53.82 | 90.30 | 86.66 | 44.66 | 55.92 | 35.46 | 88.63 |
| **XLM-R-base**  | 83.52 | 89.16 | 82.01 | 77.33 | 80.37 | 92.12 | 57.46 | 54.98 | 89.20 | 87.69 | 27.48 | 53.93 | 39.82 | 89.61 |
| **XLM-R-large** | **86.06** | 92.97 | 85.86 | 85.93 | 82.27 | **93.22** | 58.39 | 61.15 | 92.71 | **88.70** | 35.99 | 66.77 | 41.20 | 89.80 |
||
| **KR-BERT-base**  | 84.58 | 88.61 | 81.07 | 77.17 | 74.58 | 90.13 | 62.74 | 60.94 | 89.92 | 87.48 | 48.28 | 58.54 | 45.33 | 90.70 |
| **koELECTRA-base** | 84.59 | _92.46_ | _84.84_ | _85.63_ | **_86.11_** | _92.56_ | 62.85 | 58.94 | 92.90 | 87.77 | 59.82 | 66.05 | 41.58 | 89.60 |
||
| **KLUE-BERT-base** | _85.73_ | 90.85 | 82.84 | 81.63 | 83.97 | 91.39 | 66.44 | 66.17 | 89.96 | 88.05 | 62.32 | 68.51 | 46.64 | 91.61 |
| **KLUE-RoBERTa-small** | 84.98 | 91.54 | 85.16 | 79.33 | 83.65 | 91.14 | 60.89 | 58.96 | 90.04 | 88.14 | 57.32 | 62.70 | 46.62 | 91.44 |
| **KLUE-RoBERTa-base** | 85.07 | 92.50 | 85.40 | 84.83 | 84.60 | 91.44 | _67.65_ | _68.55_ | _93.04_ | _88.32_ | _68.67_ | _73.98_ | _47.49_ | _91.64_ | 
| **KLUE-RoBERTa-large** | 85.69 | **93.35** | **86.63** | **89.17** | 85.00 | 91.86 | **71.13** | **72.98** | **93.48** | 88.36 | **75.58** | **80.59** | **50.22** | **92.23** |


## Leaderboard
https://klue-benchmark.com

### Submission Guideline
See https://aistages-prod-server-public.s3.amazonaws.com/app/Competitions/000065/data/klue_code.tar.gz 

## Members
### Researchers
[Sungjoon Park](https://github.com/SungjoonPark), [Jihyung Moon](https://github.com/inmoonlight), [Sungdong Kim](https://github.com/DSKSD), [Won Ik Cho](https://github.com/warnikchow), [Jiyoon Han](https://github.com/hanjiyoon01), [Jangwon Park](https://github.com/monologg), [Chisung Song](https://github.com/daydrill), [Junseong Kim](https://github.com/codertimo), [Youngsook Song](https://github.com/songys), [Taehwan Oh](https://github.com/Donquixohtae), [Joohong Lee](https://github.com/roomylee), [Juhyun Oh](https://github.com/juhyunohh), [Sungwon Ryu](https://github.com/Lyusungwon), [Younghoon Jeong](https://github.com/boychaboy), [Inkwon Lee](https://github.com/inkoon), [Sangwoo Seo](https://github.com/SeoSangwoo), [Dongjun Lee](https://github.com/DongJunLee), [Hyunwoo Kim](https://github.com/skywalker023), [Myeonghwa Lee](https://github.com/myeonghwa-lee), [Seongbo Jang](https://github.com/sb-jang), [Seungwon Do](https://github.com/dodoseung), [Sunkyoung Kim](https://github.com/Sunkyoung), [Kyungtae Lim](https://github.com/jujbob), [Jongwon Lee](https://github.com/jongwon-jay-lee), [Kyumin Park](https://github.com/Kyumin-Park), [Jamin Shin](https://github.com/jshin49), [Seonghyun Kim](https://github.com/MrBananaHuman), [Lucy Park](https://github.com/e9t)

### Advisors
[Alice Oh](https://github.com/aliceoh9), [Jung-Woo Ha](https://github.com/Jungwoo-ha), [Kyunghyun Cho](https://github.com/kyunghyuncho)

## Sponsors
- Platinum: Upstage, NAVER Clova, Google
- Gold: Kakao Enterprise
- Silver: Scatter Lab, Selectstar
- Bronze: Riiid, DeepNatural, KAIST
- Data Providers: Acrofan, KED

## Organizers
- Host: Upstage
- Co-organizers: Naver AI Labs, NYU, KAIST
- Research Collaborators: Kakao Enterprise, Scatter Lab, Riiid, Seoul National Univ., Yonsei Univ., Sogang Univ., Kyunghee Univ., Hanbat National Univ.

## Reference

```
@misc{park2021klue,
      title={KLUE: Korean Language Understanding Evaluation},
      author={Sungjoon Park and Jihyung Moon and Sungdong Kim and Won Ik Cho and Jiyoon Han and Jangwon Park and Chisung Song and Junseong Kim and Yongsook Song and Taehwan Oh and Joohong Lee and Juhyun Oh and Sungwon Lyu and Younghoon Jeong and Inkwon Lee and Sangwoo Seo and Dongjun Lee and Hyunwoo Kim and Myeonghwa Lee and Seongbo Jang and Seungwon Do and Sunkyoung Kim and Kyungtae Lim and Jongwon Lee and Kyumin Park and Jamin Shin and Seonghyun Kim and Lucy Park and Alice Oh and Jungwoo Ha and Kyunghyun Cho},
      year={2021},
      eprint={2105.09680},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

## License

This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />


