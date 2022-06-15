# Cyclic Models

List of files:
- `rank2.json`: Rank 2 models used in [1,2]. The data was obtained from the BNC and ukWaC corpora

## How to read the files

### `rank2.json`

- key (`verb noun`):  Contexts of the rank 2 model; e.g. for `throw pitcher` the two contexts will be *throw pitcher* and *pitcher throw*. 
    - `model`: Empirical model, e.g. for `pitcher throw`:
    ```
    [
        [
            [p(throw=0, pitcher=0)| throw pitcher, p(throw=0, pitcher=1)| throw pitcher],
            [p(throw=1, pitcher=0)| throw pitcher, p(throw=1, pitcher=1)| throw pitcher]
        ],
        [
            [p(throw=0, pitcher=0)| pitcher throw, p(throw=0, pitcher=1)| pitcher throw],
            [p(throw=1, pitcher=0)| pitcher throw, p(throw=1, pitcher=1)| pitcher throw]
        ]
    ]
    ```
    - `delta_v`: (2x) The direct influence from the verb
    - `delta_n`: (2x) The direct influence from the noun
    - `delta`: Degree of signalling
    - `non-contextuality`: (non-normalised) degree of *non*-contextuality (i.e. a model is contextual iff < 0)
    - `verb_ambiguity`: Level of ambiguity of the verb
    - `noun_ambiguity`: Level of ambiguity of the noun

[1] Wang, D., Sadrzadeh, M., Abramsky, S., & Cervantes, V. H. (2021). On the Quantum-like Contextuality of Ambiguous Phrases. Proceedings of the 2021 Workshop on Semantic Spaces at the Intersection of NLP, Physics, and Cognitive Science. Association for Computational Linguistics, 42–52.

[2] Wang, D., Sadrzadeh, M., Abramsky, S., Víctor, H., & Cervantes, V. H. (2021). Analysing Ambiguous Nouns and Verbs with Quantum Contextuality Tools. Journal of Cognitive Science, 22(3), 391-420.