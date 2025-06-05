# {metaeffekt} Actions

[![Test Actions](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME/actions/workflows/test-actions.yml/badge.svg)](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME/actions/workflows/test-actions.yml)

## Necessary Prerequisites

As the actions in this repository are executed via calls to maven, java and maven must be installed before running them.
To ensure compatibility, java 1.8 (zulu / corretto) and maven 3.9 are recommended.

## Available Actions

### Resolve Inventory
- **Path**: `resolve`
- **Usage**: `uses: YOUR_USERNAME/YOUR_REPO_NAME/resolve@v1`
- **Description**: Fetches additional information for software artifacts listed in an inventory


| Property           | Required | Explanation                                                                                          |
|--------------------|----------|------------------------------------------------------------------------------------------------------|
| cache-dependencies | no       | Cache dependencies to speed up subsequent runs, as well as all other actions contained in this repo. |
| input-path         | yes      | Path to the input inventory file to resolve.                                                         |
| output-path        | yes      | Path where the resolved inventory will be saved.                                                     |
| resolver-config    | no       | Path to the artifact resolver config file.                                                           |
| resolver-proxy     | no       | Path to the proxy config file for the resolver.                                                      |
| working-directory  | no       | The working directory in which intermediaries will be saved and steps performed.                     |

