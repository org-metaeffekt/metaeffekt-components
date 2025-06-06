### Enrich Inventory
- **Path**: `enrich`
- **Usage**: `uses: org-metaeffekt/metaeffekt-components/enrich@VERSION_TAG`
- **Description**: Enhances vulnerability data in an inventory using multiple sources

| Property                         | Required | Explanation                                                                                          |
|----------------------------------|----------|------------------------------------------------------------------------------------------------------|
| cache-dependencies               | no       | Cache dependencies to speed up subsequent runs, as well as all other actions contained in this repo. |
| input-path                       | yes      | Path to the input inventory file to enrich.                                                          |
| output-path                      | yes      | Path where the enriched inventory will be saved.                                                     |
| activate-msrc                    | no       | Activates enrichment via data provided by msrc.                                                      |
| activate-nvd                     | no       | Activates enrichment via data provided by nvd.                                                       |
| activate-certfr                  | no       | Activates enrichment via data provided by certfr.                                                    |
| activate-certeu                  | no       | Activates enrichment via data provided by certeu.                                                    |
| activate-certsei                 | no       | Activates enrichment via data provided by certsei.                                                   |
| activate-ghsa                    | no       | Activates enrichment via data provided by ghsa.                                                      |
| activate-kev                     | no       | Activates enrichment via data provided by kev.                                                       |
| activate-epss                    | no       | Activates enrichment via data provided by epss.                                                      |
| activate-eol                     | no       | Activates enrichment via data provided by eol.                                                       |
| activate-status                  | no       | Activates the vulnerability status column.                                                           |
| activate-keywords                | no       | Activates the vulnerability keywords column.                                                         |
| activate-validation              | no       | Activates the vulnerability validation column.                                                       |
| activate-custom-vulnerabilites   | no       | Activates incorporation of provided custom vulnerabilities in the enrichment process.                |
| vulnerabilities-custom-directory | no       | Path to the directory containing custom vulnerability information.                                   |