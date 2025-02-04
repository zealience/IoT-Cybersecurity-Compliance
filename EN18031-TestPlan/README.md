# EN 18031-1 & -2 Test Plan Template
## Instructions
This template is designed to support the assessment of a radio equipment to demonstrate conformance with the standards EN 18031-1 and -2. It follows the instructions and assessment criteria laid down in these standards.

For each of the requirements listed in the standards, the template provides three parts to enable an evaluator to perform the required assessments and document the results:
1. Conceptual Assessment
2. Functional Completeness Assessment (where applicable)
3. Functional Sufficiency Assessment (where applicable)
The Summary Table below provides an overview of all the requirements and an indication when a given assessment is not necessary.

This template can be adjusted to cover only one of these standards. To do so, consult the table below and remove the requirements not needed.

| Standard applied	| Only EN 18031-1 | Only EN 18031-2 |
| :---     |  :---   | :---      |
| Requirement to remove | ACM-3, ACM-4, ACM-5, ACM-6, AUM-2-2, LGM-1, LGM-2, LGM-3, LGM-4, DLM-1, UNM-1, UNM-2, GEC-7	 | RLM-1, NMM-1, TCM-1 |

This template was designed to be used in conjunction with the template of the Technical Documentation also provided by Zealience (link). In particular, the assessments in this Test Plan refer to specific worksheets of this Technical Documentation. This ensures a straightforward evaluation process. This Test Plan template is still usable with a different Technical Documentation format, as it uses the official identifiers listed in the standards.

Each assessment is structured as follows:
* **Standards**: Indicates the standard(s) where this assessment is required.
* **Preconditions**: Indicates whether there are specific preconditions to be met before performing the assessment.
* **Identifiers**: Worksheets: Provides a link between an official identifier from the standard and the name of the worksheet (in the Technical Documentation template from Zealience) where the information for that identifier can be found. For example, “[E.Info.ACM-1.NetworkAsset]: ACM-1.NetAsset” means that the information to be documented under the identifier [E.Info.ACM-1.NetworkAsset] can be found in the worksheet ACM-1.NetAsset.
* **Test Items**: Indicates the items to be tested for a given assessment.
* **Instructions**: Provides a list of steps to be performed in order to complete the assessment.
* **Notes (Optional)**: Provides some extra information relevant for the evaluation.

Given the wide range of information to be assessed, Zealience suggests using prefixes to provide contextual information which may be useful for the evaluation. These prefixes are inspired by those used in ETSI TS 103 701. For example, in the Technical Documentation, a network function can be documented as “NetFunc-DHCP” where “DHCP” is its name of the function and the prefix “NetFunc” indicates that it is a network function. This approach is beneficial to remove ambiguity when a certain name can be used for different concepts. For example, a firewall can be an access control mechanism (prefixed with “AccCtrl”), and its implementation can be a security function (prefixed with “SecFunc”). The list of the abbreviations used throughout this Test Plan is provided below: 
* **NetFunc**: Network function
* **NetFuncConfig**: Network function configuration
* **PrivFunc**: Privacy function
* **PrivFuncConfig**: Privacy function configuration
* **PersoInfo**: Personal information
* **SecFunc**: Security function
* **SecParam**: Security parameter
* **AccCtrl**: Access control
* **AuthMech**: Authentication mechanism
* **UpdMech**: Update mechanism
* **StorageMech**: Storage mechanism
* **ComMech**: Communication mechanism
* **LogMech**: Logging mechanism
* **NetMonMech**: Network monitoring mechanism
* **TrafConMech**: Traffic control mechanism

## Verification
| Name     | Size    | SHA256    |
| :---     |  :---   | :---      |
| EN18031_1_2_TestPlan_Template.docx | 228.121 bytes | 7f8fb49efc09c66c71b447e2178a3b682bc09a612e6e0f0eb36b8d2bf1e59a64 |
