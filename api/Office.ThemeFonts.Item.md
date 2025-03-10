---
title: ThemeFonts.Item method (Office)
ms.prod: office
api_name:
- Office.ThemeFonts.Item
ms.assetid: 09b437dd-9be3-223e-4b81-f83a1d44d53f
ms.date: 01/29/2019
ms.localizationpriority: medium
---


# ThemeFonts.Item method (Office)

Gets one of the three language fonts contained in the **ThemeFonts** collection.


## Syntax

_expression_.**Item**(_Index_)

_expression_ An expression that returns a **[ThemeFonts](Office.ThemeFonts.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Index_|Required|**[MsoFontLanguageIndex](office.msofontlanguageindex.md)**|The index value of the **ThemeFont** object.|

## Return value

ThemeFont


## Example

The following example sets the font for the body of a document to the Latin theme.


```vb
Dim tTheme As OfficeTheme 
Dim tfThemeFonts As ThemeFonts 
Dim latinMinorFont As ThemeFont 
Set tfThemeFonts = tTheme.ThemeFontScheme.MinorFont 
Set latinMinorFont = tfThemeFonts(msoThemeLatin)
```


## See also

- [ThemeFonts object members](overview/Library-Reference/themefonts-members-office.md)


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]