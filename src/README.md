# Source Code

This folder contains the notebooks used to reproduce the literature review methodology. Run them from this folder (paths are relative to `src/`).

* **`dblp_parsing.ipynb`** parses the DBLP XML dump (journal articles, conference/workshop papers, and parts in books or collections from 2020 onwards) and serializes it as a Parquet file (`data/dblp_anthology.parquet`) for faster loading. Before running, download the dump `dblp-2026-11-01.xml.gz` and the corresponding `dblp-2023-06-28.dtd` from [DROPS](https://drops.dagstuhl.de/) and save both in `data/`. These files are git-ignored, as is the generated Parquet file.

* **`acl_parsing.ipynb`** parses the ACL Anthology metadata (publications from 2020 onwards) and serializes it as a Parquet file (`data/acl_anthology.parquet`) for faster loading. The output file is git-ignored and must be generated before running `literature_review.ipynb`.

* **`literature_review.ipynb`** retrieves literature from the following sources: DBLP, ACL Anthology, IEEE Xplore, ACM Digital Library, SpringerLink, Scopus, and arXiv (preprints are not included in the final survey). DBLP and ACL are searched in the Parquet files above, ACM, IEEE, and Springer are parsed from the web-interface exports stored in `data/`, and Scopus and arXiv are queried through their APIs (the Scopus API key is read from `.env`). The retrieved results are stored as pickle files in the `results/` directory.

* **`analysis.ipynb`** merges the search results from the considered digital libraries and exports them as Excel (`.xlsx`) files to the `files/` directory, including the complete set of records (`combined_publications_*.xlsx`), a deduplicated version (`deduplicated_publications_*.xlsx`), and a deduplicated version enriched with citation counts (`deduplicated_publications_cites_*.xlsx`; Semantic Scholar counts are cached in `data/s2_cites_cache.csv`). It also generates summary analyses and figures (e.g., publications per year, organizations, models, model sizes, and venue types), which are saved in `files/imgs/`.
