# Technical Documentation Template for EN 18031 (-1, -2 and -3)

## Table of Contents
1. [Purpose](#purpose)
2. [Structure of the template](#structure)
3. [Instructions / How to use](#instruction)
4. [Notes](#notes)
5. [Verification](#verification)
6. [Copyright notice](#copy)


## Purpose <a name='purpose'></a>
As many of you may be experiencing, the EN 18031 standards are extremely complex and challenging, and the RED DA is just around the corner. It is the first time the IoT industry is navigating such a demanding cybersecurity regulation. Rather than working in silos, we believe that collaboration, knowledge sharing, and mutual support are essential to overcoming these complexities together. In this spirit, we are excited to present our Technical Documentation template as an open-source project and contribution to the industry. We invite you to join us in this endeavor by providing feedback and suggestions to enhance the template. A heartfelt thank you to those who have already contributed, whether by sharing insights or opening issues.

This template is designed to help manufacturers of connected products to assemble the Technical Documentation required to demonstrate compliance with the standards EN 18031-1, EN 18031-2 and EN 18031-3.
This template proposes a structured approach to document the Required Information expected by the standards. If a standard is not applied, refer to the Instructions below to modify the template accordingly.
This template strives to strike a balance between the ease of use for both manufacturers documenting the Required Information and for the evaluators reviewing the Technical Documentation.

## Structure of the template <a name='structure'></a>
This template consists of different worksheets (or tabs) organized as follows:

- **ProductInfo**: Provides some general information about the equipment and its manufacturer. (Inspired by ETSI TS 103 701, Identification of the DUT)

- **ResultSummary**: Provides a list of all requirements and aggregates their Decision Tree results (PASS, NA, FAIL). These results are automatically calculated based on the values in the TableContent (see below). This means you can monitor you compliance status per requirement at a glance.

- **TableContent**: Provides a mapping between the Required Information and the worksheets of this template where the information can be documented. For example, the information to be documented under the identifier [E.Info.ACM-1.SecurityAsset] and the information related to the decision tree [E.Info.DT.ACM-1] and [E.Just.DT.ACM-1] can be documented in the worksheet **ACM-1.SecAssets**. **TableContent** also provides the number of Decision Tree results that are passing, failing and not applicable. These results are automatically calculated based on the values inputted in the respective worksheets. Additionally, TableContent provides an easy way to navigate to the various worksheets by embedding hyperlinks.
  
- **Overview-SecAsset, Overview-NetAsset, Overview-PrivAsset, Overview-FinAsset**: Lists of all the security/network/privacy/financial assets contained in the equipment. For each asset, you can provide an indication whether certain conditions are met (e.g., whether the asset is accessible over a network interface). This helps to identify whether an asset is in scope of a given requirement (e.g., when an asset is accessible over a network interface, it is in scope of requirement GEC-2 and GEC-3). See Note 2 below for an explanation of the term "asset in scope of requirement".

- **Remaining worksheets**: Contain the Required Information for the requirements of the standards. For example, the worksheet **AUM-1-1.ACM** contains the Required Information for the identifier [E.Info.AUM-1-1.ACM].
Note 1: Some worksheets may contain information for more than one identifier. For example, **RLM-1** contains information for both [E.Info.RLM-1.NetworkInterface] and [E.Info.RLM-1.RLM].
Note 2: Yes, there are many tabs! However, this is due to EN 18031 standards requiring a lot of information and imposing specific identifiers. We provide one tab for each category of information expected by the requirements. For example, ACM-1 has one tab per asset type. This allows to format the information in tables and use the expected identifiers.
Note 3: In order to navigate easily across the many worksheets, we recommend making use of the hyperlinks in TableContent and the other worksheets (see top left, Navigation).

## Instructions / How to use <a name='instruction'></a>
The completion of the Technical Documentation is an iterative process and will likely require the user to revisit and update the same pages multiple times.
We recommend starting with these 3 steps below and iterating over them until the Technical Documentation is considered completed.

**Step 0** (Optional): Adjust the template to focus on the standard(s) applied by deleting the unnecessary worksheets. Go to the worksheet **TableContent**, and go through the worksheets listed in the colum "Worksheet/tab". Delete each worksheet indicated as being relevant only to the standard(s) that is not applied. For example, if only EN 18031-1 is applied, you can delete the worksheet **ACM-1.PrivAsset** since it is only relevant to EN 18031-2. Do the same in the worksheet **ResultSummary** by deleting the unnecessary rows. Additionally, delete the unnecessary **Overview-...** worksheets. For example, if only EN 18031-1 is applied, delete **Overview-PrivAssets** and **Overview-FinAssets**.

**Step 1**: Start by completing the worksheets **Overview-...*** as much as you can in order to document the assets in the equipment. You can consider our articles on assets identification provided on our website (https://zealience.com/resource-hub/articles).
For each asset, give it a name in the first column. We recommend using meaningful names which will help for the review (e.g. "PubKeyUpdatesVerification"). Then, indicate the type of asset and whether it is sensitive or confidential, before describing the asset. Next, answer the questions listed in the columns E onward. This will help you identify whether an asset is in scope of certain requirements. For example, if you answer Yes to the first question "Is accessible by entities?" (column E), the asset is in scope of the requirement ACM-1 and must be documented in the worksheet ACM-1.SecAsset. (See Note 2 and 3 below.)
As mentioned, completing the Technical Documentation is an iterative process and therefore it may not be possible to complete Step 1 (i.e. listing all the assets) in one go. Revisit this step as many times as needed.

**Step 2**: Based on the assets identified in Step 1, you can proceed to the respective worksheets and provide the necessary information. It is recommended to have the standards open and refer to the information provided there for each identifier. For example, while completing the worksheet **AUM-1-1.ACM**, it will be beneficial to refer to the expected information to be provided for [E.Info.AUM-1-1.ACM.ManagedAccessNetworkAsset]. Moreover, certain identifiers in this template are marked with "(conditional)" below their name. This indicates that a certain condition needs to be met for the information to be necessary. The condition is provided in the standards.

**Step 3**:  Complete the remaining worksheets which applicability is not based on the worksheets **Overview-...**. Certain requirements such as SUM-* or CCK-*  require to be documented regardless of the conditions met by certain assets documented in Overview-*. As you may encounter new assets while documenting security mechanisms, you can go back to Step 1 and document them.

## Notes <a name='notes'></a>
1. To be usable, this template requires to own a copy of the standards EN 18031-1, EN18031-2 and EN18031-3.
2. We make a distinction between the terms "asset is in scope of a requirement" and "a requirement is applicable to an asset". An asset is in scope of a requirement when it meets the condition expressed in one of the "entry points" of the Decisition Trees. For example, when an asset is stored presistently on the equipment, we say that this asset is "in scope of SSM-1" since the entry point states "For each [...] asset persistently stored on the equipment". However, the applicability of requirements is determined by the Decision Tree nodes. Based on a certain condition (i.e., the "exit node" in a given Decision Tree), a requirement may not be applicable to an asset. Pursuing the previous example of the stored asset, if it is protected by physical or logical measures in the target operational environment of the equipment (the condition expressed in DT.SSM-1.DN-1), the  requirement SSM-1 is considered not applicable to that asset (yet, the justification still requires to be documented). If that condition is not met, then the exit node will be DT.SSM-1.DN-2, in which case the requirement is applicable and must be met for that asset.
3. There is no connection/link made between the answers to questions and the other worksheets. For example, answering Yes or No to questions will not have any effects in other parts of this template.  The only links made are the Decision Tree results in each worksheet which will be reflected in the TableContent.
4. The grey boxes with a dash are cells in which a selection can be made. Click on the dropdown and make your selection (e.g., Yes/No, or PASS/FAIL/NA)
5. The green boxes marked "(ref)" suggest that you can provide the name of an entry of a different worksheet as a reference. This is a suggestion to prevent duplication of information. For example, when documenting a security asset that is persistently stored (in the worksheet **SSM-1.SecAsset**), the standards expect a description of the secure storage mechanism (under the identifier [E.Info.SSM-1.SecurityAsset.SSM]). Rather than describing the storage mechanism here, it should suffice to provide a reference to the storage mechanism in **SSM-2.SSM worksheet** and decribe it there.
6. The algorithms of Decision Trees are not implemented in this template, therefore you must ensure the validity of your selected path through the Decisions Trees (i.e. validate with the standards) and provide the necessary justification. Watch out, certain Decision Trees are different, depending on the standards applied (e.g., the Decision Trees of SCM-* in EN 18031-3 are different from those in EN 18031-1 and -2).
7. There are typos in some of the Required Information's identifiers and inconsistencies between the identifiers used across the three standards. We did not address them to remain align with the standards and to allow for quick searches in the standards.
8. For certain requirements, we have identified a number of corner cases/issues with their Decision Trees' logic. These issues make it difficult to document the paths through the Trees. Whenever a requirement has such issues, we provide some explanation/interpretation and suggest instead how to best document it. Examples include GEC-1 or LGM-4.

## Verification <a name='verification'></a>
| Name     | Size    | SHA256    |
| :---     |  :---   | :---      |
| Template_EN18031-1_TechnicalDoc.v1.xlsx | 155.163 bytes | f14febcab545301d417c6200a792aa2f765c8d044a7b18c0e93bc383d683d065 |
| Template_EN18031-1_TechnicalDoc.v1.1.xlsx | 161.025 bytes | 5b57e9d4bf7ca9b45320373c32f50c0e3a27f191743ace4e6ac35f0ef9270d27 |
| Template_EN18031_TechnicalDoc.v1.2.xlsx | 229.907 bytes | b3fc178e4db86268bfd553b815670725f375624d051c2d3be2274cf0638841af |
| Template_EN18031_TechnicalDoc.v1.3.xlsx | 304.629 bytes |  6ed01641e93abad77873dc86f92335e663fdf8b6ce3092237fb5e19ccc20fcf8|

## Copyright Notice <a name='copy'></a>
Copyright 2025 Zealience GmbH. This work is openly licensed via CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/)
https://zealience.com
