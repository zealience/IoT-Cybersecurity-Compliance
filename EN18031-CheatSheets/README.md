# Scoping conditions for requirements in relation to assets of EN 18031-1 and EN 18031-2

## Introduction:
This table helps identify the applicable requirements of EN 18031-1 and -2 for each asset type. When applying the standards, manufacturers have to identify the applicability of requirements for each asset. However, this is challenging due to the complexity of the standards. This table can be used as a cheat sheet to understand the interplay between the requirements and assets, allowing manufacturers to quickly identify what needs to be documented and to what extent.

(Some of the requirements of the EN 18031 standards are to be applied to an equipment's assets, while others are to be applied to security mechanisms (e.g. authentication mechanisms). The scope of this work is on those to be applied to security/privacy/network assets.)

## We propose the following definitions:

<ins>Asset "In scope" or "out of scope" of a requirement</ins>: We consider an asset to be "in scope" of a requirement when it meets a certain condition we call a "scoping condition" (see next point below). When in scope, an asset will have to be documented as instructed by the standard.
Example: A password (security asset) is communicated over a network interface. It is "in scope" of the requirement SCM-1 and needs to be documented under the identifier [E.Info.SCM-1.SecurityAsset] by providing all relevant information listed in the standards.

<ins>Scoping conditions</ins>:
These conditions determine whether an asset may have to fulfil a requirement. Further conditions will have to be checked to verify whether that asset needs to fulfil the requirement, i.e., whether the requirement is applicable to that asset or not (see next point below). The scoping conditions are detailed in the worksheet "ScopingConditions".
For example, if a security parameter is accessible by entities, it is in scope of the requirement ACM-1.

At a high level, the most prevalent scoping conditions are the following:
* Is the asset accessible by entities? -> in scope of ACM-1
  * Is it accessible over network interface? -> AUM-1-1, GEC-2, GEC-3
  * Is it accessible over user interface? AUM-1-2
* Is it stored persistently? -> SSM-1 and SSM-2 (and if applicable DLM-1, UNM-1 )
* Is it communicated over a network interface?
  * Does it require confidentiality, integrity or authenticity (or replay) protection -> SCM-1
    * Does it require integrity or authenticity protection? -> SCM-2
    * Does it require confidentiality protection? -> SCM-3
    * Does it require replay protection? -> SCM-4
* Is it protected by cryptography? -> CRY-1

<ins>Applicability/non-applicability of a requirement to an asset</ins>:
A requirement is <ins>not</ins> applicable to an asset when that asset is in scope AND that asset meets (at least) one of the conditions rendering the requirement "not applicable". Otherwise, the requirement is applicable to that asset, and that asset needs to fulfil it.

These conditions determining non-applicability can be seen in the respective decision trees of the requirements. Even when a requirement is not applicable to an asset, a justification needs to be documented for that asset, as instructed by the standards. Note that not all requirements have conditions of non-applicability, meaning that assets in scope must fulfil the requirement. For example, for the requirement SSM-3, confidential assets persistently stored on the equipment must be stored on a secure storage mechanism protecting their confidentiality.

Examples:
1. A password is communicated over a network interface (i.e. is in scope of SCM-1) and it is not communicated over a secure communication mechanism. However, the targeted environment where the equipment is to be deployed ensures that this asset is not exposed to unauthorized entities (condition of Decision Node 3). In this case, the requirement SCM-1 is deemed "not applicable" to this security asset, and a justification is to be provided (e.g. explaining the measures in place in the targeted environment that ensure that the asset is not exposed to unauthorized entities)
2. A password is communicated over a network interface (i.e. is in scope of SCM-1) and does not meet either the condition of the Decision Node 2 (i.e. the temporary exposure of the asset is required to establish/manage a connection) nor Decision Node 3 (see previous example). Therefore, this security asset needs to fulfil SCM-1, i.e. it needs to be communicated over a secure communication mechanism.


## How to use the table "Scoping Conditions":

* You can use this table per asset type: For each asset type, browse through its column to see what are the scoping condition(s) for a given requirement. For example, a personal information that is confidential and persistently stored on the equipment is in scope of SSM-3.
* You can use this table per requirement: For each requirement, browse through its row to see the scoping condition(s) for each asset type. For example, for the requirement SSM-3, only confidential personal information/privacy function configuration/security parameter/network function configuration are is scope.

## Notes:
* Some requirements are specific to the assets of either EN 18031-1 or EN 18031-2. In this case, the cell is greyed with the mention "NA for EN 18031-X". For example, the requirement ACM-3 is specific to EN 18031-2 and therefore the cells of the network assets are marked "NA for EN 18031-1".
* Some requirements are only relevant to specific assets. For example, ACM-3 may only be applicable to privacy functions which "enable children to access external content" and the "children's access [to those functions] is managed by access control mechanism per ACM-1". There are also requirements that are not relevant to any of the assets, since assets are out of scope. For example, the requirement AUM-2 is only applicable to authentication mechanisms (required per AUM-1-1 and AUM-1-2). In such cases, the assets' cells are greyed out with the mention "(asset out of scope)".

## Verification
| Name     | Size    | SHA256    |
| :---     |  :---   | :---      |
| CheatSheet_EN18031_TableScopingConditions_v1.0.xlsx | 36.056 bytes | 0c0bcd71d0aca614519ac36ec3d8d70ddd50af38e674aab35d6cbff2150679f5 |

