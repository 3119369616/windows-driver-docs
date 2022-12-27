---
title: Diagnose method of the MSFT\_Volume class
description: Performs a diagnostic on the volume, returning any actionable results.
ms.assetid: 57B10BFE-DD51-4E33-A7C9-8AB89953D638
keywords:
- Diagnose method Windows Storage Management API
- Diagnose method Windows Storage Management API , MSFT_Volume class
- MSFT_Volume class Windows Storage Management API , Diagnose method
topic_type:
- apiref
api_name:
- MSFT_Volume.Diagnose
api_location:
- Root\Microsoft\Windows\Storage
api_type:
- COM
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Diagnose method of the MSFT\_Volume class

Performs a diagnostic on the volume, returning any actionable results.

## Syntax


```mof
UInt32 Diagnose(
  [out] String DiagnoseResults[o],
  [out] String ExtendedStatus
);
```



## Parameters

<dl> <dt>

*DiagnoseResults* \[out\]
</dt> <dd>

An array of strings containing embedded [**MSFT\_StorageDiagnoseResult**](msft-storagediagnoseresult.md) objects specifying the actionable results of the diagnose.

</dd> <dt>

*ExtendedStatus* \[out\]
</dt> <dd>

A string that contains an embedded [**MSFT\_StorageExtendedStatus**](msft-storageextendedstatus.md) object.

This parameter allows the storage provider to return extended (implementation-specific) error information.

</dd> </dl>

## Return value

<dl> <dt>

**Success** (0)
</dt> <dt>

**Not Supported** (1)
</dt> <dt>

**Unspecified Error** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Failed** (4)
</dt> <dt>

**Invalid Parameter** (5)
</dt> <dt>

**Method Parameters Checked - Job Started** (4096)
</dt> <dt>

**Access denied** (40001)
</dt> <dt>

**There are not enough resources to complete the operation.** (40002)
</dt> <dt>

**Cache out of date** (40003)
</dt> <dt>

**Failed to communicate with cluster health resource.** (59000)
</dt> </dl>

## Requirements



|                                     |                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 10 \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows Server 2016 \[desktop apps only\]<br/>                                      |
| Namespace<br/>                | Root\\Microsoft\\Windows\\Storage<br/>                                              |
| MOF<br/>                      | <dl> <dt>Storagewmi.mof</dt> </dl> |



## See also

<dl> <dt>

[**MSFT\_Volume**](msft-volume.md)
</dt> </dl>

 

 





