---
title: "DMSCHEMA_MINING_MODEL_XML Rowset | Microsoft Docs"
ms.date: 05/03/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: schema-rowsets
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
---
# DMSCHEMA_MINING_MODEL_XML Rowset
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
  Returns the XML structure of the mining model. The format of the XML string follows the Predictive Model Markup Language (PMML 2.1) standard.  
  
## Rowset Columns  
 The **DMSCHEMA_MINING_MODEL_XML** rowset contains the following columns.  
  
|Column name|Type indicator|Length|Description|  
|-----------------|--------------------|------------|-----------------|  
|**MODEL_CATALOG**|**DBTYPE_WSTR**||The catalog name. Populated with the name of the database of which the model is a member.|  
|**MODEL_SCHEMA**|**DBTYPE_WSTR**||The unqualified schema name. This column is not supported by [!INCLUDE[msCoName](../../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)]; it always contains **NULL**.|  
|**MODEL_NAME**|**DBTYPE_WSTR**||The model name. This column cannot contain **NULL**.|  
|**MODEL_TYPE**|**DBTYPE_WSTR**||The model type. It is a provider-specific string. It can be **NULL**.|  
|**MODEL_GUID**|**DBTYPE_GUID**||The GUID that identifies the model. Providers that do not use GUIDs to identify tables return **NULL**.|  
|**MODEL_PMML**|**DBTYPE_WSTR**||An XML representation of the model's content in PMML format.|  
|**SIZE**|**DBTYPE_UI4**||The number of bytes in the XML string.|  
|**LOCATION**|**DBTYPE_WSTR**||The location of the XML file. It is **NULL** if a physical file is not used for storage.|  
  
 This schema rowset is not sorted.  
  
## Restriction Columns  
 The DMSCHEMA_MINING_MODEL_XML rowset can be restricted on the columns listed in the following table.  
  
|Column name|Type indicator|Restriction State|  
|-----------------|--------------------|-----------------------|  
|**MODEL_CATALOG**|**DBTYPE_W**STR|Optional.|  
|**MODEL_SCHEMA**|**DBTYPE_WSTR**|Optional.|  
|**MODEL_NAME**|**DBTYPE_WSTR**|Optional.|  
|**MODEL_TYPE**|**DBTYPE_WSTR**|Optional.|  
  
## See Also  
 [Data Mining Schema Rowsets](../../../analysis-services/schema-rowsets/data-mining/data-mining-schema-rowsets.md)  
  
  
