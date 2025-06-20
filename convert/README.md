### Convert Inventory
- **Path**: `convert`
- **Usage**: `uses: org-metaeffekt/metaeffekt-components/convert@VERSION_TAG`
- **Description**: Converts an inventory into a SBOM, either in CycloneDX or SPDX format.

| Property                     | Required | Explanation                                                                  |
|------------------------------|----------|------------------------------------------------------------------------------|
| input-path                   | yes      | The input inventory file path from which to generate the bom.                |
| output-path                  | yes      | The output bom file path with the correct format extension.                  |
| document-name                | yes      | The document name listed in the bom.                                         |
| description                  | yes      | The document description listed in the bom.                                  |
| document-id-prefix           | yes      | Id prefix used for every component.                                          |
| organization                 | yes      | The organization which created the bom.                                      |
| organization-url             | yes      | The url of the organization which created the bom.                           |
| person                       | no       | The person which created the bom.                                            |
| comment                      | no       | A comment regarding the creation of the bom.                                 |
| output-format                | no       | Which output format the bom should be in. (Default JSON)                     |
| document-version             | no       | The current version of this bom.                                             |
| map-relationships            | no       | If relationships between inventory artifacts should be tracked.              |
| use-license-expressions      | no       | If license expressions or single licenses should be used.                    |
| include-license-texts        | no       | If license texts should be included.                                         |
| include-assets               | no       | If only artifacts should be included or assets as well.                      |
| include-technical-properties | no       | Only required to mitigate data-loss for multiple import/export cycles.       |
| derive-attributes-from-purl  | no       | If missing attributes should be derived from the PURL if present.            |
| custom-license-mappings      | no       | A custom license mapping file containing license identifier : license pairs. |