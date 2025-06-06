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
