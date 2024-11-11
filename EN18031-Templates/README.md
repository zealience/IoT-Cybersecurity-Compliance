# Templates for EN18031 series of standards

## EN18031-1

### Purpose
This template is designed to help manufacturers of connected products to assemble the Technical Documentation required to demonstrate compliance with the standard EN18031-1. This template proposes a structure to document the Required Information expected by the standard.

The template strives to strike a balance between the ease of use for both manufacturers documenting the Required Information and for the evaluators reviewing the work.

### Structure of the template
This template consists of different worksheets (or tabs) organized as follows:

- ProductInfo: Provides some general information about the device and its manufacturer. (Inspired from ESTI TS 103 701, Identification of the DUT)

- TableContent: Provides a mapping between the Required Information and the worksheets of this template where the information can be documented. For example, the information to be documented under the identifier [E.Info.ACM-1.SecurityAsset] and the information related to the decision tree [E.Info.DT.ACM-1] and [E.Just.DT.ACM-1] can be documented in the worksheet ACM-1.SecAssets.

- Overview-SecAsset and Overview-NetAsset: Lists of all the security and network assets contained in the device. For each asset, an indication of certain conditions met is provided (e.g., whether the asset is accessible over a network interface).

- Remaining worksheets: Contain the Required Information for each requirement of the standard. For example, the worksheet AUM-1-1.ACM contains the Required Information for the identifier [E.Info.AUM-1-1.ACM].
Note: Some worksheets may contain information for more than one identifier. For example, RLM-1 contains information for both [E.Info.RLM-1.NetworkInterface] and [E.Info.RLM-1.RLM].

### Instruction
The completion of the Technical Documentation is an iterative process and will likely require the user to revisit and update the same pages multiple times.
We recommend starting with these 3 steps below and iterating over them until the Technical Documentation is considered completed.

Step 1: Start by completing the worksheets Overview-* to document the assets in the device. 
For each asset, give it a name in the designated column. We recommend using meaningful names which will help for the review (e.g. "PubKeyUpdatesVerification"). Then, indicate the type of asset and whether it is sensitive or confidential, before describing the asset.
Next, answer the questions listed in the columns E to M. This will help you identify the applicability of certain requirements. For example, if you answer Yes to the first question "Is accessible by entities?" (column E), the requirement ACM-1 is applicable and the asset must be documented in the worksheet ACM-1.SecAsset. (See Note 2 below.)

Step 2: Based on the assets documented and the applicable requirements identified, you can now proceed to the respective worksheets and provide the necessary information. It is recommended to have the standard open and refer to the information provided there for each identifier. For example, while completing the worksheet "AUM-1-1.ACM", it will be beneficial to refer to the expected information to be provided for [E.Info.AUM-1-1.ACM.ManagedAccessNetworkAsset]. Moreover, certain identifiers in this template are marked with "(conditional)" below their name. This indicates that a certain condition needs to be met for the information to be necessary. The condition is provided in the standard.

Step 3: Complete the remaining worksheets which applicability is not based on the worksheets Overview-*. Certain requirements such as SUM-* or CCK-*  require to be documented regardless of the conditions met by certain assets documented in Overview-*.

### Verification
Name: Template_EN18031-1_TechnicalDoc.v1.xlsx

Size: 155163 bytes (151 KiB)

SHA256: f14febcab545301d417c6200a792aa2f765c8d044a7b18c0e93bc383d683d065

### Notes
1. To be usable, this template requires to own a copy of the standard EN18031-1.
2. There is no connection made between the answers to questions and the other worksheets. For example, answering Yes or No to questions will not have any effects in other parts of this template. 
3. The grey boxes with a dash are cells in which a selection can be made. Click on the dropdown and make your selection (e.g., Yes/No, or PASS/FAIL/NA)
4. The green boxes marked "(ref)" suggest that you can provide the name of an entry of a different worksheet as a reference. 
5. The algorithms of Decision Trees are not implemented in this template, therefore you must ensure the validity of your selected path through the decisions trees (i.e. validate with the standard) and provide the necessary justification.

## Copyright Notice
Copyright 2024 Zealience GmbH. This work is openly licensed via CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/)
