# Data

This directory contains the raw datasets used for the literature review and analysis. Unless otherwise noted, these files are unmodified exports obtained directly from their respective sources.

| Dataset | Description | Origin | Association |
| ------- | ----------- | ------ | ----------- |
| `acm.bib` | Bibliographic records from the literature search on the ACM Digital Library. | [ACM Digital Library](https://dl.acm.org/search/advanced) | Association for Computing Machinery (ACM) |
| `ieee.bib` | Bibliographic records from the literature search on IEEE Xplore. | [IEEE Xplore Digital Library](https://ieeexplore.ieee.org/search/advanced/command) | Institute of Electrical and Electronics Engineers (IEEE) |
| `springer.csv` | Bibliographic records from the literature search on SpringerLink. | [SpringerLink](https://link.springer.com/advanced-search?query=&sortBy=relevance&advanced-search=true) | Springer Nature |
| `acl_anthology.pkl` | Serialized list of ACL Anthology publications from 2020 onwards. | [ACL Anthology](https://aclanthology.org/) | Association for Computational Linguistics (ACL) |

## Notes

* The ACM, IEEE, and Springer datasets are exports from the corresponding digital libraries and preserve the original metadata provided by each source, according to the respective search queries.
* The ACL Anthology dataset is derived from the official ACL Anthology metadata and includes publications from 2020 onward. The ACL Anthology is maintained by the ACL Anthology volunteer team on behalf of the Association for Computational Linguistics.

## Search Queries and Settings

The following table contains the settings of the literature search across the ACM Digital Library, IEEE Xplore, and SpringerLink.

| Database | Publication Period | Search Field | Search Query |
| -------- | ------------------ | ------------ | ------------ |
| ACM Digital Library | 2020 onwards | Abstract | `(language model* OR llm*) AND (knowledge graph* OR kg*) AND hallucinat*` |
| IEEE Xplore | 2020 onwards | Abstract | `(language model* OR llm*) AND (knowledge graph* OR kg*) AND hallucinat*` |
| SpringerLink | 2020 onwards | Title | `(language model* OR llm* OR encoder* OR decoder* OR gpt OR rag) AND (knowledge* OR graph* OR kg*) AND (hallucinat* OR fact* OR qa OR trust* OR coheren* OR reliab* OR explain*)` |

