---
title: Shape.Paste method (Visio)
keywords: vis_sdr.chm11216430
f1_keywords:
- vis_sdr.chm11216430
ms.prod: visio
api_name:
- Visio.Shape.Paste
ms.assetid: ce5892be-b5e7-2ca0-7ee1-aa4e602641a2
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Shape.Paste method (Visio)

Pastes the contents of the Clipboard into an object.


## Syntax

_expression_.**Paste** (_Flags_)

_expression_ A variable that represents a **[Shape](Visio.Shape.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Flags_|Optional| **Variant**|Determines how shapes are translated during the paste operation.|

## Return value

Nothing


## Remarks

The **Paste** method works only with **Shape** objects that are group shapes. Use the **Type** property of a shape to determine whether it is a group.

Possible values for  _Flags_ are declared by the Visio type library in **VisCutCopyPasteCodes**, and are described in the following table.



|**Flag**|Value|Description|
|:-----|:-----|:-----|
| **visCopyPasteNormal**|&H0|Follow default copying behavior.|
| **visCopyPasteNoTranslate**|&H1|Copy shapes to their original coordinate locations.|
| **visCopyPasteCenter**|&H2|Copy shapes to the center of the page.|
| **visCopyPasteNoHealConnectors**|&H4|Do not clean up connectors attached to cut shapes.|
| **visCopyPasteNoContainerMembers**|&H8|Do not cut and copy unselected members of containers or lists.|
| **visCopyPasteNoAssociatedCallouts**|&H16|Do not cut and copy unselected callouts associated with shapes.|
| **visCopyPasteDontAddToContainers**|&H32|Do not add pasted shapes to any underlying containers.|
| **visCopyPasteNoCascade**|&H64|Do not offset shapes on copy.|

Setting  _Flags_ to **visCopyPasteNormal** is the equivalent of the behavior in the user interface. You should use **visCopyPasteNormal** and the other flags consistently. For example, if you use the value **visCopyPasteNoTranslate** to copy, you should also use that value to paste, because that is the only way to ensure that shapes are pasted to their original coordinate location.

If you need to control the format of the pasted information and (optionally) establish a link to a source file (for example, a Microsoft Word document), use the **PasteSpecial** method.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]