---
title: WDI_TLV_SAE_COMMIT_PARAMS (dot11wificxtypes.hpp)
ms.topic: reference
description: WDI_TLV_SAE_COMMIT_PARAMS is a WiFiCx TLV that contains parameters for a Simultaneous Authentication of Equals (SAE) Commit request or response. 
ms.date: 02/29/2024
---

# WDI_TLV_SAE_COMMIT_PARAMS (dot11wificxtypes.hpp)

[!INCLUDE [WiFiCx topic note](../includes/wificx-version-warning.md)]

**WDI_TLV_SAE_COMMIT_PARAMS** is a TLV that contains parameters for a Simultaneous Authentication of Equals (SAE) Commit request or Commit response.

This TLV is used in the command parameters for [OID_WDI_SET_SAE_AUTH_PARAMS](oid-wdi-set-sae-auth-params.md).

## TLV type

0x150

## Length

The sum (in bytes) of the sizes of all contained TLVs.

## Values

| TLV | Type | Multiple TLV instances allowed | Optional | Description |
| --- | --- | --- | --- | --- |
| [WDI_TLV_SAE_FINITE_CYCLIC_GROUP](wdi-tlv-sae-finite-cyclic-group.md) | UINT16 |   |   | The Finite Cyclic Group used for SAE authentication. |
| [WDI_TLV_SAE_SCALAR](wdi-tlv-sae-scalar.md) | TLV\<LIST\<UINT8>> |   |  X | The Finite Field Element (FFE). |
| [WDI_TLV_SAE_ELEMENT](wdi-tlv-sae-element.md) | TLV\<LIST\<UINT8>> |   | X  | The Encoded Field Element (EFE). |
| [WDI_TLV_SAE_ANTI_CLOGGING_TOKEN](wdi-tlv-sae-anti-clogging-token.md) | TLV\<LIST\<UINT8>> |   |  X | The anti-clogging token as requested by the BSSID. |
| [WDI_TLV_SAE_REJECTED_GROUPS](wdi-tlv-sae-rejected-groups.md) | TLV\<LIST\<UINT8>> |   | X  | Any rejected groups. |
| [WDI_TLV_RSNA_AKM_SUITE](wdi-tlv-rsna-akm-suite.md) |   | | X | List of RSNA AKM suites. |
| [WDI_TLV_CIPHER_ALGORITHM](wdi-tlv-cipher-algorithm.md) |   | | X | A cipher algorithm value. |
| [WDI_TLV_SAE_STATUS_CODE](wdi-tlv-sae-status-code.md) |   | |  | The 802.11 SAE status code. |

## Requirements

|Requirement|Value|
|--- |--- |
|Minimum supported client|Windows 11|
|Minimum supported server|Windows Server 2022|
|Header|dot11wificxtypes.hpp|
