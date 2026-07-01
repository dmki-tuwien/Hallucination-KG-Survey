# Source Code

This folder contains the notebooks used to reproduce the literature review methodology.

* **`acl_parsing.ipynb`** parses the ACL Anthology bibliography (in `.bib` format), available from the ACL Anthology website, and serializes it as a pickle file for faster loading. The output pickle file is already provided in the `data/` directory.

* **`analysis.ipynb`** merges the search results from the considered digital libraries and exports them as Excel (`.xlsx`) files to the `files/` directory, including both the complete set of records and a deduplicated version. It also generates summary analyses (e.g., publication counts by year), which are saved in `files/imgs/`.

* **`literature_review.ipynb`** retrieves literature from the following sources: DBLP, ACL Anthology, IEEE Xplore, ACM Digital Library, SpringerLink, Scopus, and arXiv (preprints are not included in the final survey). The retrieved results are stored as pickle files in the `results/` directory.
