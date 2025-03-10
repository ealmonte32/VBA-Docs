---
title: CustomControl.IsVisible property (Access)
keywords: vbaac10.chm12038
f1_keywords:
- vbaac10.chm12038
ms.prod: access
api_name:
- Access.CustomControl.IsVisible
ms.assetid: e432566c-c8a9-6d08-4b01-5c5949248ba9
ms.date: 02/22/2019
ms.localizationpriority: medium
---


# CustomControl.IsVisible property (Access)

Use the **IsVisible** property to determine whether a control on a report is visible. Read/write **Boolean**.


## Syntax

_expression_.**IsVisible**

_expression_ A variable that represents a **[CustomControl](Access.CustomControl.md)** object.


## Remarks

You can set the **IsVisible** property only in the **Print** event of a report section that contains the control.

Use the **IsVisible** property together with the **HideDuplicates** property to determine when a control on a report is visible and show or hide other controls as a result. For example, you could hide a line control when a text box control is hidden because it contains duplicate values.


## Example

The following example uses the **IsVisible** property of a text box to control the display of a line control on a report. 

Paste the following code into the Declarations section of the report module, and then view the report to see the line formatting controlled by the **IsVisible** property.

```vb
Private Sub Detail_Print(Cancel As Integer, PrintCount As Integer) 
 If Me!CategoryID.IsVisible Then 
 Me!Line0.Visible = True 
 Else 
 Me!Line0.Visible = False 
 End If 
End Sub
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]