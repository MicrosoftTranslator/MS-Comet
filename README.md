# MS-Comet and MS-COMET-QE

We release checkpoints for two new metrics that are build on top of the [COMET](https://github.com/Unbabel/COMET) architecture. 
It was fine-tuned on several times larger collection of human judgement containing 15 domains and 113 languages.


## Installation

COMET requires python 3.8 or above. The simple installation from PyPI

```bash
pip install --upgrade pip  # ensures that pip is current 
pip install unbabel-comet
```
or
```bash
pip install unbabel-comet==1.1.2 --use-feature=2020-resolver
```

For more details, check: [https://github.com/Unbabel/COMET](https://github.com/Unbabel/COMET)


## Usage

Basic scoring command:

```bash
comet-score -s src.de -t hyp1.en -r ref.en --model_storage_path PATH/TO/CHECKPOINT
```

where PATH/TO/CHECKPOINT depends on selected model:

> reference-based MS-COMET-22: `checkpoints/MS-COMET-22/model/MS-COMET-22.ckpt`
> quality estimation MS-COMET-QE-22 `checkpoints/MS-COMET-QE-22/model/MS-COMET-QE-22.ckpt`

For more details and other usages, follow [https://github.com/Unbabel/COMET](https://github.com/Unbabel/COMET)

## Citation

```
@inproceedings{kocmi2022mscomet,
  title = {MS-COMET: More and Better Human Judgements Improve Metric Performance},
  author = {Tom Kocmi and Hitokazu Matsushita and Christian Federmann},
  booktitle = {Proceedings of the Seventh Conference on Machine Translation},
  month = {December},
  year = {2022},
  address = {Online},
  publisher = {Association for Computational Linguistics}
}
```