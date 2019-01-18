---
title: Propriété Error.Description (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714562"
---
# <a name="errordescription-property-dao"></a>Propriété Error.Description (DAO)


**S’applique à**: Access 2013, Office 2013
 

Renvoie une chaîne descriptive associée à une erreur. Il s'agit de la propriété par défaut de l'objet **Error**.

## <a name="syntax"></a>Syntaxe

*expression* . Description

*expression* Variable qui représente un objet **Error** .

## <a name="remarks"></a>Remarques

La propriété **Description** comprend une brève description de l'erreur. Elle permet de signaler à l'utilisateur la présence d'une erreur que vous ne pouvez ou ne souhaitez pas gérer.

## <a name="example"></a>Exemple

L'exemple ci-dessous force une erreur, l'intercepte et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet qui en résulte.

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

