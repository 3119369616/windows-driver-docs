---
title: CM_PROB_FAILED_POST_START
description: CM_PROB_FAILED_POST_START
ms.assetid: 82d43c8b-d5de-4395-9ca0-34d2258b9772
keywords:
- CM_PROB_FAILED_POST_START
ms.date: 04/20/2017
ms.localizationpriority: medium
---

# CM_PROB_FAILED_POST_START

This function is reserved for system use.

A driver has reported a device failure.

## Error Code

43

### Display Message

"Windows has stopped this device because it has reported problems. (Code 43)"

### Recommended Resolution

Uninstall and reinstall the device.

One of the drivers controlling the device told the operating system the device failed in some manner in response to IRP_MN_QUERY_PNP_DEVICE_STATE.
