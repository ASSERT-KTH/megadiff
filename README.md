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

### Architecture

- Each folder represents a diff size measured in changed lines
- One unified diff file per commit (can diff over multiple files)

Example usage:

```
xzcat ./8/ae49f3458915859104ebd1e0858a409e01291e6d.diff.xz
```

The datasets are also available on Huggingface:

- <https://huggingface.co/datasets/ASSERT-KTH/megadiff>
- <https://huggingface.co/datasets/ASSERT-KTH/megadiff-single-function>

### Benchmark Leakage

Megadiff contains samples extracted from some projects contained in Defects4J.
An analysis on single-function Megadiff and Defects4J samples shows that:
- Math-28 and Math-44 fixed versions are included in Megadiff
- Math-28, Math-44, and JacksonDatabind-82 functions (possibily after the bug-fix) are included in 5 Megadiff samples
- Math-28, Closure-101, Closure-83, Closure-107, JacksonDatabind-58, JacksonDatabind-82, Math-44, Math-38, Gson-10 change the same file as some Megadiff samples

Note that this analysis only looks at the functions changed, and does not regard other code
