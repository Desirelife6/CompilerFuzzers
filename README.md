# Compiler Silent Bug Deduplication via Holistic Analysis

Welcome to the homepage of $D^3$! This the implementation of our research "Silent Compiler Bug De-duplication via Three-Dimensional Analysis".

## Introduction

Compiler testing is an important task for assuring the quality of compilers, but investigating test failures is very time-consuming. This is because many test failures are caused by the same compiler bug (known as bug duplication problem). In this work, we propose a novel technique (called $D^3$) to solve the duplication problem on silent compiler bugs. Its key insight is to characterize the silent bugs from the testing process and identify three-dimensional information (i.e., test program, optimizations, and test execution) for bug de-duplication.

Figure 1 presents the workflow of $D^3$. Specifically, for a silent bug (denoted as b), $D^3$ considers three-dimensional information to depict the test failure, i.e., test program (denoted as p), optimizations (denoted as o), and test execution (denoted as c). Then, $D^3$ measures the distance among test failures based on the three-dimensional information for silent bug de-duplication.

<img src="figures/overview.png" alt="overview" style="zoom:100%;" />

<p align="center">Figure 1: Overview of D3</p>

To evaluate the effectiveness of $D^3$, we conducted an empirical study based on four released datasets, which contain 2,024 test failures caused by 62 uniques bugs from four versions of GCC and LLVM. Our results show that $D^3$ significantly outperforms the two state-of-the-art compiler bug de-duplication techniques (called Tamer and Transformer in our work). Table 1 shows the overall experimental results.

<p align="center">Table 1: Overall experimental results</p>

<img src="figures/results.png" alt="overview" style="zoom:150%;" />

## Getting Started

### Use pre-calculated distances

If you don't want to process the data and calculate the distances by youself, we provide the pre-calculated distances in folder `distances`.

**Unzip the data.zip under your project directory first**, then just run the following command to get the result, which will be saved in the `results` folder.

```
python test.py --dataset llvm280 --loop_time 100
```

Note that `--dataset` indicates which data set to test on. The options are 'gcc430', 'gcc440', 'gcc450', and 'llvm280'. `--loop_time` indicates the number of times the test is repeated, and the results are averaged. We recommend at least 100 times to avoid random factors. 

6f07074562fb71ed0f5255ecc2737b6299b5caa1



9f9260eca596172b7f64c62c95ff6ef1b93c2131



## Directory description

```markdown

```

