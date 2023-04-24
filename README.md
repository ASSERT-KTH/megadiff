# Megadiff, a dataset of source code changes


If you use Megadiff, please cite the following technical report:

"[Megadiff: A Dataset of 600k Java Source Code Changes Categorized by Diff Size](http://arxiv.org/pdf/2108.04631)". Technical Report 2108.04631, Arxiv; 2021. 

```
@techreport{megadiff,
  TITLE = {{Megadiff: A Dataset of 600k Java Source Code Changes Categorized by Diff Size}},
  AUTHOR = {Martin Monperrus and Matias Martinez and He Ye and Fernanda Madeiral and Thomas Durieux and Zhongxing Yu},
  URL = {http://arxiv.org/pdf/2108.04631},
  INSTITUTION = {Arxiv},
  NUMBER = {2108.04631},
  YEAR = {2021},
}
```

Architecture
- each folder represents a diff size measured in changed lines
- one unified diff file per commit (can diff over multiple files)
