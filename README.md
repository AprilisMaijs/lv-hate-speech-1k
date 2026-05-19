# Latvian Hate Speech Dataset

A manually annotated dataset of Latvian-language online comments for hate speech detection, created as part of a Master's thesis at the University of Latvia (2026).

## Overview

| Split | Neutral (0) | Offensive (1) | Hate Speech (2) | Total |
|-------|-------------|---------------|-----------------|-------|
| Train | 365 (52.1%) | 235 (33.6%)   | 100 (14.3%)     | 700   |
| Val   | 78 (52.0%)  | 50 (33.3%)    | 22 (14.7%)      | 150   |
| Test  | 78 (52.0%)  | 51 (34.0%)    | 21 (14.0%)      | 150   |
| **Full** | **521** | **336**       | **143**         | **1000** |

## Labels

| Value | Class | Description |
|-------|-------|-------------|
| `0` | Neutral | Does not contain offensive or hateful content |
| `1` | Offensive | Contains rude or degrading language, but does not meet the threshold for hate speech |
| `2` | Hate Speech | Promotes hatred, discrimination, or violence against a person or group based on protected characteristics (ethnicity, religion, gender, sexual orientation, etc.) |

The annotation scheme follows [Davidson et al. (2017)](https://arxiv.org/abs/1703.04009).

## Files

| File | Description |
|------|-------------|
| `lv_hate_speech_full.csv` | Complete dataset (1,000 comments) |

The file contains two columns: `text` (the comment) and `label` (0/1/2).

## Data Collection

Comments were sourced from the [Latvian user comment dataset 1.0](http://hdl.handle.net/11356/1407) (Shekhar et al., 2021), a corpus of ~12.4M comments from the Delfi news portal (2014–2019). Comments were filtered by language, length, and a curated keyword list to produce a candidate set for annotation. Annotation was performed by a single annotator using a structured labeling guide.

## Intended Use

This dataset is intended for **research purposes only**, specifically for:
- Developing and evaluating hate speech detection models for Latvian
- Benchmarking NLP methods on low-resource Baltic languages
- Studying the boundary between offensive language and hate speech

## Out-of-Scope Use

This dataset must **not** be used to:
- Build systems that surveil, target, or harass individuals
- Train models intended for deployment without human oversight
- Any commercial application without explicit permission from the authors

## Citation

If you use this dataset, please cite the accompanying thesis and the source corpus:

```bibtex
@mastersthesis{kairis2026latvian,
  author    = {Kairis, Marts},
  title     = {Naida runas noteikšana latviešu valodā, izmantojot mašīnmācīšanās metodes},
  school    = {University of Latvia},
  year      = {2026},
  url       = {https://github.com/AprilisMaijs/lv-hate-speech-1k}
}
```

```bibtex
@dataset{shekhar2021latvian,
  title     = {Latvian user comment dataset 1.0},
  author    = {Shekhar, Ravi and Purver, Matthew and Pollak, Senja and Pelicon, Andraž and Krustok, Ivar},
  year      = {2021},
  publisher = {Ekspress Meedia Group},
  doi       = {10.34894/EBQJRF},
  url       = {http://hdl.handle.net/11356/1407}
}
```

The experiment code accompanying this dataset is available at:
`https://github.com/AprilisMaijs/hate-speech-detection`

## License

MIT License — see the repository's LICENSE file for details.
