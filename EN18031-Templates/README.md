# Technical Documentation Template for hEN 18031-1 & -2

## Table of Contents
1. [Purpose](#purpose)
2. [Structure of the template](#structure)
3. [Instructions / How to use](#instruction)
4. [Notes](#notes)
5. [Verification](#verification)
6. [Copyright notice](#copy)


## Purpose <a name='purpose'></a>
This template is designed to help manufacturers of connected products to assemble the Technical Documentation required to demonstrate compliance with the standard EN 18031-1 and EN 18031-2. This template proposes a structured approach to document the Required Information expected by the standards. If only one of the two standards needs to be applied, refer to the Instructions below to modify the template accordingly.

The template strives to strike a balance between the ease of use for both manufacturers documenting the Required Information and for the evaluators reviewing the Technical Documentation.

## Structure of the template <a name='structure'></a>
This template consists of different worksheets (or tabs) organized as follows:

- **ProductInfo**: Provides some general information about the device and its manufacturer. (Inspired by ESTI TS 103 701, Identification of the DUT)

- **TableContent**: Provides a mapping between the Required Information and the worksheets of this template where the information can be documented. For example, the information to be documented under the identifier [E.Info.ACM-1.SecurityAsset] and the information related to the decision tree [E.Info.DT.ACM-1] and [E.Just.DT.ACM-1] can be documented in the worksheet ACM-1.SecAssets.

- **Overview-SecAsset, Overview-NetAsset and Overview-PrivAsset**: Lists of all the security/network/privacy assets contained in the equipment. For each asset, you can provide an indication whether certain conditions are met (e.g., whether the asset is accessible over a network interface).

- **Remaining worksheets**: Contain the Required Information for the requirements of the standards. For example, the worksheet AUM-1-1.ACM contains the Required Information for the identifier [E.Info.AUM-1-1.ACM].
Note: Some worksheets may contain information for more than one identifier. For example, RLM-1 contains information for both [E.Info.RLM-1.NetworkInterface] and [E.Info.RLM-1.RLM].

## Instructions / How to use <a name='instruction'></a>
The completion of the Technical Documentation is an iterative process and will likely require the user to revisit and update the same pages multiple times.
We recommend starting with these 3 steps below and iterating over them until the Technical Documentation is considered completed.

**Step 0** (Optional): Adjust the template to focus on the standard applied by deleting the unnecessary worksheets. Go to the worksheet TableContent and go through the worksheets listed in the colum "Worksheet/tab". Delete each worksheet indicated as being appliable only to the standard that is not applied. For example, if only EN 18031-1 is applied, you can delete the worksheet "ACM-1.PrivAsset" since it only applied to EN 18031-2.
Additionally, delete the unnecessary Overview worksheet: If only EN 18031-1 is applied, delete Overview-PrivAssets. If only EN 18031-2 is applied, delete Overview-NetAssets.

**Step 1**: Start by completing the worksheets Overview-* to document the assets in the device. 
For each asset, give it a name in the first column. We recommend using meaningful names which will help for the review (e.g. "PubKeyUpdatesVerification"). Then, indicate the type of asset and whether it is sensitive or confidential, before describing the asset. Next, answer the questions listed in the columns E onward. This will help you identify the applicability of certain requirements. For example, if you answer Yes to the first question "Is accessible by entities?" (column E), the asset is in scope of the requirement ACM-1 and must be documented in the worksheet ACM-1.SecAsset. (See Note 2 and 3 below.)
As mentioned, completing the Technical Documentation is an iterative process and therefore it may not be possible to complete Step 1 (i.e. listing all the assets) in one go. Revisit this step as many times as needed.

**Step 2**: Based on the assets documented and the applicable requirements identified, you can proceed to the respective worksheets and provide the necessary information. It is recommended to have the standards open and refer to the information provided there for each identifier. For example, while completing the worksheet "AUM-1-1.ACM", it will be beneficial to refer to the expected information to be provided for [E.Info.AUM-1-1.ACM.ManagedAccessNetworkAsset]. Moreover, certain identifiers in this template are marked with "(conditional)" below their name. This indicates that a certain condition needs to be met for the information to be necessary. The condition is provided in the standard.

**Step 3**: Complete the remaining worksheets which applicability is not based on the worksheets Overview-*. Certain requirements such as SUM-* or CCK-*  require to be documented regardless of the conditions met by certain assets documented in Overview-*.

## Notes <a name='notes'></a>
1. To be usable, this template requires to own a copy of the standards EN 18031-1 and EN18031-2.
2. We use the term "asset is in scope of a requirement" to express the following concept: A certain requirement may by applicable to a given asset, however, based on certain conditions expressed in the standards, there may be cases rendering the requirement not applicable for that asset. For example, an asset accessible by entities is in scope of requirement ACM-1, but if the asset is meant to be publicly accessible, ACM-1 will be not applicable to this asset.
3. There is no connection/link made between the answers to questions and the other worksheets. For example, answering Yes or No to questions will not have any effects in other parts of this template. 
4. The grey boxes with a dash are cells in which a selection can be made. Click on the dropdown and make your selection (e.g., Yes/No, or PASS/FAIL/NA)
5. The green boxes marked "(ref)" suggest that you can provide the name of an entry of a different worksheet as a reference. 
6. The algorithms of Decision Trees are not implemented in this template, therefore you must ensure the validity of your selected path through the decisions trees (i.e. validate with the standard) and provide the necessary justification.

## Verification <a name='verification'></a>
| Name     | Size    | SHA256    |
| :---     |  :---   | :---      |
| Template_EN18031-1_TechnicalDoc.v1.xlsx | 155.163 bytes | f14febcab545301d417c6200a792aa2f765c8d044a7b18c0e93bc383d683d065 |
| Template_EN18031-1_TechnicalDoc.v1.1.xlsx | 161.025 bytes | 5b57e9d4bf7ca9b45320373c32f50c0e3a27f191743ace4e6ac35f0ef9270d27 |
| Template_EN18031_TechnicalDoc.v1.2.xlsx | 229.907 bytes | b3fc178e4db86268bfd553b815670725f375624d051c2d3be2274cf0638841af |

## Copyright Notice <a name='copy'></a>
Copyright 2025 Zealience GmbH. This work is openly licensed via CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/)
https://zealience.com
