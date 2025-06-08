# {metaeffekt} Components

[![Test Actions](https://github.com/org-metaeffekt/metaeffekt-components/actions/workflows/test-actions.yml/badge.svg?branch=main)](https://github.com/org-metaeffekt/metaeffekt-components/actions/workflows/test-actions.yml)

## Necessary Prerequisites

As the actions in this repository are executed via calls to maven, java and maven must be installed before running them.
To ensure compatibility, java 1.8 (zulu / corretto) and maven 3.9 are recommended.

## Available Actions

### Resolve Inventory
- **Path**: `resolve`
- **Usage**: `uses: org-metaeffekt/metaeffekt-components/resolve@VERSION_TAG`
- **Description**: Fetches additional information for software artifacts listed in an inventory


| Property           | Required | Explanation                                                                                          |
|--------------------|----------|------------------------------------------------------------------------------------------------------|
| cache-dependencies | no       | Cache dependencies to speed up subsequent runs, as well as all other actions contained in this repo. |
| input-path         | yes      | Path to the input inventory file to resolve.                                                         |
| output-path        | yes      | Path where the resolved inventory will be saved.                                                     |
| resolver-config    | no       | Path to the artifact resolver config file.                                                           |
| resolver-proxy     | no       | Path to the proxy config file for the resolver.                                                      |
| working-directory  | no       | The working directory in which intermediaries will be saved and steps performed.                     |

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

### Scan Inventory
- **Path**: `scan`
- **Usage**: `uses: org-metaeffekt/metaeffekt-components/scan@VERSION_TAG`
- **Description**: Fetches licensing and copyright information for software artifacts listed in an inventory


| Property              | Required | Explanation                                                                                                  |
|-----------------------|----------|--------------------------------------------------------------------------------------------------------------|
| cache-dependencies    | no       | Cache dependencies to speed up subsequent runs, as well as all other actions contained in this repo.         |
| input-path            | yes      | Path to the input inventory file to resolve.                                                                 |
| output-path           | yes      | Path where the resolved inventory will be saved.                                                             |
| intermediary-dir-path | yes      | Path where intermediaries for the scan process will be stored temporarily                                    |
| scanner-config-file   | yes      | Path to the scanner config file. This is a .properties file containing settings which control the scan flow. |
| scancode-binary-path  | no       | Path to the scancode binary. Should be set if scancode is enabled in the scanner-config-file.                |

