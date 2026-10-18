# cathtedassign-test-datasets

Test data for [nf-cath-ted-assign](https://github.com/UCLOrengoGroup/nf-cath-ted-assign) (nf-core/cathtedassign).

Interim location until the data moves to its long-term home (nf-core/test-datasets or S3). Paths below are relative to the repository root and match what the pipeline expects under `params.pipelines_testdata_base_path`.

## Content

### `prepare_input/`

Small structure archives for the input-preparation steps. Every structure is an unmodified file from its source.

| File | Structures | Exercises |
| --- | --- | --- |
| `predicted_set1.zip` | AFDB models A0A009DWJ5 (47 residues), A0A009DYA3 (50), A0A003 (340) | listing and chunking structures from a zip; length filtering (raise the minimum residue threshold to reject the two short models) |
| `predicted_set2.zip` | AFDB models A0A009DY47 (56), A0A000 (394) | a second input zip |
| `experimental_set1.zip` | PDB entries 1UBQ (ubiquitin, one chain plus waters), 4HHB (haemoglobin, four chains) | renumbering experimental structures and removing waters; rejection of multi-chain entries |
| `samplesheet_test.csv` | All three archives | pipeline-level test (`-profile test`) |

## Sources and licences

- AlphaFold DB models, taken from the TED test set in [UCLOrengoGroup/domain-annotation-pipeline](https://github.com/UCLOrengoGroup/domain-annotation-pipeline) (`assets/test_ids/30-ted-ids.zip`). AlphaFold DB data is available under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).
- PDB entries [1UBQ](https://www.rcsb.org/structure/1UBQ) and [4HHB](https://www.rcsb.org/structure/4HHB), downloaded from RCSB PDB. PDB data is available under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
