# sacre-bird-phoenix

Review annotations and German sign-to-text back translations for the RWTH-PHOENIX-Weather 2014T sign language translation benchmark.

This repository contains derivative research data created for an audit of the RWTH-PHOENIX-Weather 2014T benchmark. To use this data together with the original benchmark, users must obtain RWTH-PHOENIX-Weather 2014T from its original providers and comply with the original corpus terms.

## Repository contents

The release contains the following pipe-separated CSV files:

```text
test_full_annotations_sacrebirdphoenix.csv
test_subset_backtranslations_sacrebirdphoenix.csv
train_annotations_sacrebirdphoenix.csv
```

All files use `|` as the delimiter.

### `train_annotations_sacrebirdphoenix.csv`

This file contains manual annotations for a structured sample of the PHOENIX training set.

Rows: `307`

Columns, in order:

| Column | Description |
|---|---|
| `name` | Segment identifier matching the original PHOENIX-2014T segment naming. |
| `information missing in the glosses` | Binary flag indicating that information present in the German text appears to be missing from the gloss sequence. |
| `information missing in the German text` | Binary flag indicating that information present in the gloss sequence appears to be missing from the German text. |
| `lexical errors` | Binary flag indicating a suspected lexical or content mismatch between glosses and German text. |
| `minor differences` | Binary flag indicating smaller differences that do not meaningfully affect adequacy. |
| `comment` | Free-text reviewer comment. |

### `test_full_annotations_sacrebirdphoenix.csv`

This file contains the full set of manual sign-to-text back translations and annotations for the PHOENIX test set.

Rows: `642`

Columns, in order:

| Column | Description |
|---|---|
| `name` | Segment identifier matching the original PHOENIX-2014T segment naming. |
| `back translation` | German sign-to-text back translation produced from the video. |
| `translation confidence` | Translation confidence score. Possible values are `0`, `0.5`, and `1`. |
| `technical quality problems` | Binary flag indicating noticeable video quality problems that may affect interpretation. |
| `comment` | Free-text comment on the back translation or video item. |

### `test_subset_backtranslations_sacrebirdphoenix.csv`

This file contains only the high-confidence subset of the test-set back translations.

Rows: `462`

Columns, in order:

| Column | Description |
|---|---|
| `name` | Segment identifier matching the original PHOENIX-2014T segment naming. |
| `back translation` | German sign-to-text back translation produced from the video. |
| `translation confidence` | Translation confidence score. This file includes only rows with `translation confidence = 1`. |
| `technical quality problems` | Binary flag indicating noticeable video quality problems that may affect interpretation. |
| `comment` | Free-text comment on the back translation or video item. |

## Intended use

This release is intended for non-commercial research on sign language translation evaluation, benchmark reliability, annotation quality, reference quality, and reference-based metric behaviour.

## Limitations

The annotations and back translations are the result of a targeted benchmark audit. Flags indicate reviewer judgements under the project’s annotation criteria. Absence of a flag does not necessarily mean that a segment is error-free.

The back translations are intended as supplementary evaluation material. They should be interpreted together with the methodological description in the accompanying publication.

## Citation

If you use this repository, please cite **both**:

1. the accompanying paper, and
2. the original RWTH-PHOENIX-Weather corpus papers.

### Accompanying paper

```bibtex
@inproceedings{czehmann:26064:sign-lang:lrec,
  author    = {Czehmann, Vera and Yazdani, Shakib and Hamidullah, Yasser and Nunnari, Fabrizio and Avramidis, Eleftherios},
  title     = {"A Sacred Bird Called the Phoenix". Auditing the most-used Parallel Corpus for {German} {Sign} {Language} Recognition and Translation},
  pages     = {80--92},
  editor    = {Efthimiou, Eleni and Fotinea, Stavroula-Evita and Hanke, Thomas and Hochgesang, Julie A. and Mesch, Johanna and Schulder, Marc},
  booktitle = {Proceedings of the {LREC2026} 12th Workshop on the Representation and Processing of Sign Languages: Language in Motion},
  maintitle = {15th International Conference on Language Resources and Evaluation ({LREC} 2026)},
  publisher = {{European Language Resources Association (ELRA)}},
  address   = {Palma, Mallorca, Spain},
  day       = {16},
  month     = may,
  year      = {2026},
  isbn      = {978-2-493814-82-1},
  language  = {english},
  url       = {https://www.sign-lang.uni-hamburg.de/lrec/pub/26064.html}
}
```

### Original corpus

Please also cite the original RWTH-PHOENIX-Weather corpus and its 2014 extension.

```bibtex
@inproceedings{forster2012rwthphoenixweather,
  author    = {Forster, Jens and Schmidt, Christoph and Hoyoux, Thomas and Koller, Oscar and Zelle, Uwe and Piater, Justus and Ney, Hermann},
  title     = {{RWTH-PHOENIX-Weather: A Large Vocabulary Sign Language Recognition and Translation Corpus}},
  booktitle = {Proceedings of the Eighth International Conference on Language Resources and Evaluation (LREC'12)},
  pages     = {3785--3789},
  year      = {2012},
  address   = {Istanbul, Turkey},
  publisher = {European Language Resources Association (ELRA)}
}
```

```bibtex
@inproceedings{forster2014extensions,
  author    = {Forster, Jens and Schmidt, Christoph and Koller, Oscar and Bellgardt, Martin and Ney, Hermann},
  title     = {{Extensions of the Sign Language Recognition and Translation Corpus RWTH-PHOENIX-Weather}},
  booktitle = {Proceedings of the Ninth International Conference on Language Resources and Evaluation (LREC'14)},
  pages     = {1911--1916},
  year      = {2014},
  address   = {Reykjavik, Iceland},
  publisher = {European Language Resources Association (ELRA)}
}
```

The RWTH-PHOENIX-Weather 2014T creators additionally asks users to cite Camgöz et al. (2018):

```bibtex
@inproceedings{camgoz2018neural,
  author    = {Camgoz, Necati Cihan and Hadfield, Simon and Koller, Oscar and Ney, Hermann and Bowden, Richard},
  title     = {{Neural Sign Language Translation}},
  booktitle = {Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year      = {2018},
  address   = {Salt Lake City, UT, USA}
}
```

## License

This repository is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (`CC BY-NC-SA 4.0`). See [`LICENSE`](LICENSE) for details.

This license applies to the derivative annotations, comments, and sign-to-text back translations provided in this repository. It does not grant rights to the original RWTH-PHOENIX-Weather 2014T corpus files, which remain subject to the original corpus providers’ terms.

Under `CC BY-NC-SA 4.0`, you may share and adapt the licensed material for non-commercial purposes, provided that you give appropriate credit, indicate changes, and distribute adapted material under the same license.

## Contact

For questions about this derivative release, please contact the authors of the accompanying paper.
