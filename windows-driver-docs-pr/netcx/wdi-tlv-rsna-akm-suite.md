---
title: WDI_TLV_RSNA_AKM_SUITE (dot11wificxtypes.hpp)
ms.topic: reference
description: WDI_TLV_RSNA_AKM_SUITE is a WiFiCx TLV that contains the RSNA AKM suites that the driver supports.
ms.date: 02/07/2024
---

# WDI_TLV_RSNA_AKM_SUITE (dot11wificxtypes.hpp)

[!INCLUDE [WiFiCx topic note](../includes/wificx-version-warning.md)]

WDI_TLV_RSNA_AKM_SUITE is a WiFiCx TLV that contains the Robust Security Network Association (RSNA) authentication and key management (AKM) suites that the driver supports.

## TLV Type

0x205

## Length

The size (in bytes) of the array of [**RSNA_AKM_SUITE**](/windows-hardware/drivers/ddi/windot11/ne-windot11-rsna_akm_suite) enums. 

## Values

| Type | Description |
|-----------------|-----------------|
| [**RSNA_AKM_SUITE**](/windows-hardware/drivers/ddi/windot11/ne-windot11-rsna_akm_suite)[] | An array of RSNA AKM suites. |

## Requirements

|Requirement|Value|
|--- |--- |
|Minimum supported client|Windows 11, version 24H2|
|Header|dot11wificxtypes.hpp|
