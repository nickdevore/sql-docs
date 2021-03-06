---
title: "Process Tabular Model Partitions | Microsoft Docs"
ms.custom: ""
ms.date: "03/01/2017"
ms.prod: analysis-services
ms.prod_service: "analysis-services, azure-analysis-services"
ms.service: ""
ms.component: ""
ms.reviewer: ""
ms.suite: "pro-bi"
ms.technology: 
  
ms.component: multidimensional-tabular
ms.component: data-mining
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6c498d2b-22d6-4661-bc21-2ee708336c8b
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
ms.workload: "Inactive"
---
# Process Tabular Model Partitions 
[!INCLUDE[ssas-appliesto-sqlas-aas](../../includes/ssas-appliesto-sqlas-aas.md)]
  Partitions divide a table into logical parts. Each partition can then be processed (Refreshed) independent of other partitions. The tasks in this topic describe how to process partitions in a model database by using the **Process Partitions** dialog box in [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)].  
  
###  <a name="bkmk_create_new"></a> To process a partition  
  
1.  In [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], right-click on the table that has the partitions you want to process, and then click **Partitions**.  
  
2.  In the **Partitions** dialog box, in **Partitions**, click on the Process button.  
  
3.  In the **Process Parition(s)** dialog box, in the **Mode** listbox, select one of the following process modes:  
  
    |Mode|Description|  
    |----------|-----------------|  
    |**Process Default**|Detects the process state of a partition object, and performs processing necessary to deliver unprocessed or partially processed partition objects to a fully processed state. Data for empty tables and partitions is loaded; hierarchies, calculated columns, and relationships are built or rebuilt.|  
    |**Process Full**|Processes a partition object and all the objects that it contains. When Process Full is run for an object that has already been processed, [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] drops all data in the object, and then processes the object. This kind of processing is required when a structural change has been made to an object.|  
    |**Process Data**|Load data into a partition or a table without rebuilding hierarchies or relationships or recalculating calculated columns and measures.|  
    |**Process Clear**|Removes all data from a partition.|  
    |**Process Add**|Incrementally update partition with new data.|  
  
4.  In the **Process** checkbox column, select the partitions you want to process with the selected mode, and then click **Ok**.  
  
## See Also  
 [Tabular Model Partitions](../../analysis-services/tabular-models/tabular-model-partitions-ssas-tabular.md)   
 [Create and Manage Tabular Model Partitions](../../analysis-services/tabular-models/create-and-manage-tabular-model-partitions-ssas-tabular.md)  
  
  
