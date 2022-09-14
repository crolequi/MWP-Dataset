# Math23K

Math23K is a dataset created for math word problem solving, contains 23, 162 **Chinese** problems crawled from the Internet. The dataset is originally introduced in the paper **Deep Neural Solver for Math Word Problems**.

## Structure

```
.
├── README.md
├── processed_data
│   ├── 5-fold
│   │   ├── test_0.json
│   │   ├── test_1.json
│   │   ├── test_2.json
│   │   ├── test_3.json
│   │   ├── test_4.json
│   │   ├── train_0.json
│   │   ├── train_1.json
│   │   ├── train_2.json
│   │   ├── train_3.json
│   │   └── train_4.json
│   ├── train_test
│   │   ├── test.json
│   │   └── train.json
│   └── train_val_test
│       ├── test.json
│       ├── train.json
│       └── valid.json
└── raw_data
    ├── test.json
    └── train.json

5 directories, 18 files
```

## Usage

`raw_data` comes from https://ai.tencent.com/ailab/nlp/dialogue/#datasets, which is the rawest unprocessed dataset.

`processed_data` comes from https://github.com/allanj/Deductive-MWP, which contains three directories, `train_test`, `train_val_test` and `5-fold`. 

- `train_test` was obtained by dividing the original complete dataset, with the training set containing 22, 162 problems and the test set containing 1, 000 problems;
- `train_val_test` is further divided on the basis of `train_test`, and `train_val_test` divides `train_test`'s training set into training set and validation set (`train_val_test`'s test set is the same as `train_test`'s test set). The training set in `train_val_test` contains 21, 162 problems, the validation set contains 1, 000 problems, and the test set also has 1, 000 problems.
- `5-fold` is obtained from the original complete dataset by quintiles, which means that each test set in `5-fold` is about 20% the size of the original dataset, and the union of all test sets is the original dataset.

##  Leaderboard

https://paperswithcode.com/sota/math-word-problem-solving-on-math23k.