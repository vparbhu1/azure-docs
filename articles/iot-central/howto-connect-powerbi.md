---
# Mandatory fields. See more on aka.ms/skyeye/meta.
title: Visualize your Azure IoT Central data in a Power BI dashboard | Microsoft Docs
description: Use the Azure IoT Central Analytics Power BI solution template to visualize and analyze your IoT Central data.
ms.service: iot-central
author: viv-liu
ms.author: viviali
ms.date: 07/16/2018
ms.topic: article
# Use only one of the following. Use ms.service for services, ms.prod for on-prem. Remove the # before the relevant field.
ms.prod: microsoft-iot-central
# product-name-from-white-list

# Optional fields. Don't forget to remove # if you need a field.
# ms.custom: can-be-multiple-comma-separated
# ms.devlang:devlang-from-white-list
# ms.suite: 
# ms.tgt_pltfrm:
# ms.reviewer:
manager: peterpr
---

# Visualize and analyze your Azure IoT Central data in a Power BI dashboard

![Power BI solution template pipeline](media/howto-connect-powerbi/iot-continuous-data-export.png)

Use the Azure IoT Central Analytics Power BI solution template to create a powerful Power BI dashboard to monitor the performance of your IoT devices. In your Power BI dashboard, you can:
- Track how much data your devices are sending over time
- Compare data volume between telemetry, states, and events
- Identify devices that are reporting lots of measurements
- Observe historical trends of device measurements
- Identify problematic devices that send lots of critical events

This solution template sets up the pipeline that takes the data in your Azure Blob storage account from [continuous data export](howto-export-data.md). This data flows through to Azure Functions, Azure Data Factory, and Azure SQL Database which process and transform the data to be visualized and analyzed in a Power BI report that you can download as a PBIX file. All of these resources are created in your Azure subscription, so you can customize each component to suit your needs. This solution template is completely open-sourced, so you can learn more about the architecture and extend the solution by visiting the [Github repo](https://aka.ms/iotcentralgithubpowerbisolutiontemplate).

**[Get the Azure IoT Central Analytics solution template from Microsoft AppSource.](https://aka.ms/iotcentralpowerbisolutiontemplate)**

## Prerequisites
Setting up the template requires the following:
- Access to an Azure subscription
- Exported data using [continuous data export](howto-export-data.md) from your IoT Central app. We recommend you turn on measurements, devices, and device template streams to get - the most out of the Power BI dashboard.
- Power BI Desktop (latest version)
- Power BI Pro (to share the template with others)

## Reports

Two reports are generated automatically. 

The first report shows a historical view of measurements reported by devices, and breaks down the different types of measurements and devices that have sent the highest number of measurements.

![Power BI report page 1](media/howto-connect-powerbi/template-page1-hasdata.PNG)

The second report dives deeper into events and shows a historical view of errors and warnings reported. It also shows which devices are reporting the highest number of events all up, as well as specifically error events and warning events.

![Power BI report page 2](media/howto-connect-powerbi/template-page2-hasdata.PNG)

## Resources

Visit AppSource to get the [Azure IoT Central Analytics solution template](https://aka.ms/iotcentralpowerbisolutiontemplate).

Visit the [Github repo](https://aka.ms/iotcentralgithubpowerbisolutiontemplate) to learn more about the architecture and extend the solution.

## Next steps

Now that you have learned how to visualize your data in Power BI, here is the suggested next step:

> [!div class="nextstepaction"]
> [How to manage devices](howto-manage-devices.md)
