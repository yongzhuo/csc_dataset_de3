---
license: apache-2.0
task_categories:
- text2text-generation
- text-generation
language:
- zh
tags:
- csc
- text-correct
- macro-correct
- chinese-spelling-correct
- corrector
---

# csc_public_de3数据集
## 数据来源
 - 1.由人民日报/学习强国/chinese-poetry等高质量数据人工生成;
 - 2.来自人民日报高质量语料;
 - 3.来自学习强国网站的高质量语料;
 - 4.源数据为qwen生成的好词好句;
 - 5.古诗词chinese-poetry; 文言文garychowcmu/daizhigev20;

## 测评指标
```
模型[Macropodus/macbert4mdcspell_v1](https://huggingface.co/Macropodus/macbert4mdcspell_v1)
common Sentence Level detection: acc:0.9547, precision:1.0000, recall:0.9547, f1:0.9768
common Sentence Level correction: acc:0.9309, precision:1.0000, recall:0.9309, f1:0.9642
strict Sentence Level detection: acc:0.9547, precision:0.9629, recall:0.9547, f1:0.9588
strict Sentence Level correction: acc:0.9309, precision:0.9389, recall:0.9309, f1:0.9349
common Token Level correction: precision:0.8865, recall:0.9898, f1:0.9353
common TOken Level correction: precision:0.9797, recall:0.9828, f1:0.9812
```

## 数据简介
 - 该数据主要为'的地得'纠错;
 - 其中训练数据130753条, 验证数据5545条, 测试数据5545条;
 - 句子平均长度为36, 最长句子长度为414, 最短为5, 95%的为89, 75%的为46, 60%的为34;
 - 每个句子中字的平均错误数为2;
 - 全量数据在HF(包括train.json)：[https://huggingface.co/datasets/Macropodus/csc_public_de3](https://huggingface.co/datasets/Macropodus/csc_public_de3)


## 数据详情
```
################################################################################################################################
train.json
130753
avg_errors: 2.074751630937722
avg_length: 36.39140210932063
414
5
95%:  89
90%:  69
85%:  58
80%:  51
75%:  46
70%:  41
60%:  34
50%:  29
################################################################################################################################
dev.json
5545
avg_errors: 2.047069431920649
avg_length: 35.767177637511274
278
5
95%:  85
90%:  66
85%:  56
80%:  49
75%:  45
70%:  41
60%:  35
50%:  29
################################################################################################################################
tet.json
5545
avg_errors: 2.028494138863841
avg_length: 35.982326420198376
277
5
95%:  88
90%:  66
85%:  56
80%:  49
75%:  45
70%:  41
60%:  34
50%:  29
```

## Cite
For citing this dataset, you can refer to the present GitHub project. For example, with BibTeX:
```
@software{macro-correct,
    url = {https://github.com/yongzhuo/macro-correct},
    author = {Yongzhuo Mo},
    title = {macro-correct},
    year = {2025}
```
