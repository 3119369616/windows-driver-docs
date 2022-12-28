---
title: AddPhysicalDisk method of the MSFT\_StoragePool class
description: Adds one or more physical disks from the primordial storage pool to an existing concrete storage pool.
ms.assetid: 5b6c5566-7a3f-4bc4-b69e-53664920c9b2
keywords:
- AddPhysicalDisk method Windows Storage Management API
- AddPhysicalDisk method Windows Storage Management API , MSFT_StoragePool class
- MSFT_StoragePool class Windows Storage Management API , AddPhysicalDisk method
topic_type:
- apiref
api_name:
- MSFT_StoragePool.AddPhysicalDisk
api_location:
- Root\Microsoft\Windows\Storage
api_type:
- COM
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# AddPhysicalDisk method of the MSFT\_StoragePool class

Adds one or more physical disks from the primordial storage pool to an existing concrete storage pool.

## Syntax


```mof
UInt32 AddPhysicalDisk(
  [in]  String              PhysicalDisks[],
  [in]  UInt16              Usage,
  [in]  Boolean             RunAsJob,
  [out] MSFT_StorageJob REF CreatedStorageJob,
  [out] String              ExtendedStatus
);
```



## Parameters

<dl> <dt>

*PhysicalDisks* \[in\]
</dt> <dd>

An array of strings, each of which contains an embedded [**MSFT\_PhysicalDisk**](msft-physicaldisk.md) instance that represents a physical disk to be added from the primordial storage pool to an existing concrete storage pool. This parameter is required and cannot be **NULL**.

</dd> <dt>

*Usage* \[in\]
</dt> <dd>

Specifies how the physical disks will be used in the storage pool s allocation policy. Storage pools are required to follow the assigned policy for a physical disk.

<dl> <dt>

<span id="Auto-Select"></span><span id="auto-select"></span><span id="AUTO-SELECT"></span>**Auto-Select** (1)
</dt> <dt>

<span id="Manual-Select"></span><span id="manual-select"></span><span id="MANUAL-SELECT"></span>**Manual-Select** (2)
</dt> <dt>

<span id="Hot_Spare"></span><span id="hot_spare"></span><span id="HOT_SPARE"></span>**Hot Spare** (3)
</dt> </dl> </dd> <dt>

*RunAsJob* \[in\]
</dt> <dd>

If **TRUE**, this method uses the *CreatedStorageJob* parameter when the request is taking a long time to service. If a storage job has been created to track the operation, this method will return **Method Parameters Checked - Job Started**.

> [!Note]  
> Even if *RunAsJob* is **TRUE**, this method can still return a result if it has finished in sufficient time.

 

If **FALSE** or **NULL**, this method will follow default WMI asynchronous behavior as determined by the client's method for invocation. In other words, it is synchronous unless requested otherwise.

</dd> <dt>

*CreatedStorageJob* \[out\]
</dt> <dd>

If *RunAsJob* is set to **TRUE** and this method takes a long time to execute, this parameter receives a reference to the storage job object that is used to track the long-running operation.

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

**Cannot connect to the storage provider.** (46000)
</dt> <dt>

**The storage provider cannot connect to the storage subsystem.** (46001)
</dt> <dt>

**This operation is not supported on primordial storage pools.** (48000)
</dt> <dt>

**The storage pool could not complete the operation because its health or operational status does not permit it.** (48006)
</dt> <dt>

**The storage pool could not complete the operation because its configuration is read-only.** (48007)
</dt> <dt>

**One of the physical disks specified is not supported by this operation.** (51000)
</dt> <dt>

**One of the physical disks specified is already in use.** (51002)
</dt> <dt>

**One of the physical disks specified uses a sector size that is not supported by this storage pool.** (51003)
</dt> </dl>

## Requirements



| Requirement | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                                |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                      |
| Namespace<br/>                | Root\\Microsoft\\Windows\\Storage<br/>                                              |
| MOF<br/>                      | <dl> <dt>Storagewmi.mof</dt> </dl> |



## See also

<dl> <dt>

[**MSFT\_StoragePool**](msft-storagepool.md)
</dt> </dl>

 

 





