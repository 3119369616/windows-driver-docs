---
title: Device Experience Scenarios for Document Devices
description: Device Experience Scenarios for Document Devices
ms.assetid: 8e01e9d7-5017-4e0a-90b8-4a025e25a60b
ms.date: 01/30/2019
ms.localizationpriority: medium
---

# Device Experience Scenarios for Document Devices

The Devices and Printers folder shows devices that are connected to a computer, including the document devices.

The following screen shot shows a typical Devices and Printers folder.

![screen shot illustrating a typical devices and printers folder](images/devicestage002.png)

The following screen shot shows a Devices and Printers view and Device Stage.

![screen shot illustrating devices and printers view and device stage](images/devicestage003.png)

## Document Devices in Devices and Printers

All printers that appear in the Printers folder include the following:

- Locally connected printers
- Networked printers connected through TCP/IP
- Point and Print connections
- HTTP-connected printers
- Printer connections redirected through the Remote Desktop Connection utility
- Virtual printers (including the Microsoft Shared Fax and the Microsoft XPS Document Writer)

All scanners installed with a Windows Image Acquisition (WIA) driver appear in the Devices and Printers view. Only scanners that are connected by Plug and Play or PnP-X appear in this view.

MFPs that connect to the PC by Plug and Play or PnP-X will appear in the Devices and Printers view as a single, composite device instead of as separate printer and scanner devices. Network MFPs that connect to a PC by using TCP/IP only are recognized as separate print and scan devices. The manufacturer can still provide a custom device experience that includes custom icons and a Device Stage page, but the Devices and Printers view displays the printer and scanner functions in the MFP as separate devices.

An MFP appears in the Devices and Printers view only if both the printer and scanner functions in the MFP are installed. If only the printer function is installed, this function appears in the view as a stand-alone printer, and if only the scanner function is installed, this function appears as a stand-alone scanner.

The Devices and Printers user interface treats the fax queues that the Microsoft Shared Fax driver creates as print queues. All context menus and command bar menus that are available for print queues are available for these queues.

If third-party fax drivers appear as printers in the spooler, the Devices and Printers user interface treats them as print queues and provides printer context menus, command bar menus, and generic printer icons for them.

If an MFP has a fax queue that enumerates as a print queue, it will appear as part of MFP.

If an MFP has a fax function that does not enumerate as a print queue, the Devices and Printers user interface can identify the fax as part of the MFP only if a device container identifier (ContainerID) for the fax functional device instance can be found. Manufacturers must provide custom metadata to specify the tasks for such fax devices. For more information about ContainerIDs, see the Identifying Device Functions in MFPs section.

Device manufacturers may author Device Stage for printers, scanners, and multi-function printers. Both locally attached printers (such as a printer that has a USB connection) and network-connected printers can have customized device experiences.

## Device Experience in Devices and Printers

In the Printers folder is removed and all printers and scanners appear in the Devices and Printers view.

If a manufacturer does not supply a custom Device Stage metadata package for a printer, scanner, or MFP device, the devices will still appear in the Devices and Printers view. Devices and Printers user interface provides a default device experience for the device. The default device experience does not include a Device Stage page for the device.

As shown in Figure 3, the device icon and the context menu that appears when the user right-clicks a device in the Devices and Printers view is different for devices that have customized device experiences and those devices that have default device experiences. In this example, the device is a locally connected MFP. For the default experience, shown on the left side of Figure 3, the device is represented by a generic printer icon. For the customized experience, shown on the right side of Figure 3, the device is represented by a custom icon that the manufacturer supplies. For the customized experience, the default action in the context menu is **Open**. Clicking **Open** opens the Device Stage page. **Open in new window** opens the Device Stage in a new window. For the default experience, the device has no associated Device Stage page and the context menu does not contain an **Open** option. Clicking the **See what's printing** option opens the print queue.

![figures comparing the menus for the default device experience and the custom device experience](images/devicestage004.png)

## Device Stage Custom Experience

With Device Stage, manufacturers can easily extend their product and corporate brands to the desktop. Figure 4 shows a typical branded Device Stage Custom Experience.

![figure 4: branded device stage custom experience](images/devicestage005.jpg)

Manufacturers customize the device experience. They can include their own tasks (launch applications, download software, access product manuals, update firmware, buy accessories), include a wide range of device status, and update the experience at any time to reflect their most current offerings. Device Stage experiences can be created for specific models of a device. Depending on your product strategy, you can opt to create a general device experience for a whole line of devices or modify each experience down to the color of each individual device model.

Device Stage experiences are distributed through Microsoft servers to Windows 7 clients in device metadata packages. Any updates to the custom device experience will be available on Microsoft's servers, downloaded to Windows if found, and installed automatically. If the user is using Device Stage at the time, an option to upgrade immediately will be offered. Otherwise, the update will be applied the next time Device Stage is used.

Device Stage experiences may be distributed with manufacture's setup applications as well.
