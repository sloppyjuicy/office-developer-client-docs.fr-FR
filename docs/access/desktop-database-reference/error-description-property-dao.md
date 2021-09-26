---
title: Error.Description, propriété (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 20d912de4692a86fab56a664e63df2e17635963f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589602"
---
# <a name="errordescription-property-dao"></a>Error.Description, propriété (DAO)


**S’applique à** : Access 2013, Office 2013
 

Renvoie une chaîne descriptive associée à une erreur. Il s'agit de la propriété par défaut de l'objet **Error**.

## <a name="syntax"></a>Syntaxe

*.* Description

*expression* Variable qui représente un objet **Error.**

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

