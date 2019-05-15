---
title: Bluetooth connect failure rate for machines with the driver
description: The measure aggregates telemetry from a 7-day sliding window into a percentage of instances where a Bluetooth device failed to connect with another device.
ms.topic: article
ms.date: 05/20/2019
ms.author: paslote
author: parkeratmicrosoft
ms.localizationpriority: medium
---

# Bluetooth connect failure rate for machines with the driver

## Description

If two devices are unable to connect with Bluetooth, the user will not be able to send or receive content to the other device. A disconnect can also indicate a communication problem between the devices. This measure calculates the failure rate of Bluetooth connections.

## Measure attributes

|Attribute|Value|
|----|----|
|**Audience**|Standard|
|**Time period**|7 day sliding window|
|**Measurement criteria**|Aggregation of instances|
|**Minimum population**|10 instances|
|**Passing criteria**|<= 10 % of Instances are connection failures|
|**Measure ID**|13897278|

## Calculation

1. The measure aggregates telemetry from a 7-day sliding window into a **percentage of instances where a Bluetooth device failed to connect with another device**.

   a. A single device can have multiple pairing Instances counted by the measure

2. Types of Instances:

   a. *Successful connect or disconnect event = 0% failure*

   b. *Failed to connect or successfully disconnect = 100% failure*

### Final calculation

*Bluetooth connect failure rate = average (all occurrences)*