---
title: Type, propriété – Exemple (propriété) (VB)
TOCTitle: Type property example (Property) (VB)
ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15)
ms:contentKeyID: 48547209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b6da8e0e699c8f81c0b13c285662156817c8b880
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593403"
---
# <a name="type-property-example-property-vb"></a>Type, propriété – Exemple (propriété) (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la propriété [Type](type-property-ado.md). C'est un modèle d'utilitaire permettant de répertorier les noms et les types d'une collection ([Properties](properties-collection-ado.md) ou [Fields](fields-collection-ado.md), par exemple).

Il n'est pas nécessaire d'ouvrir le [Recordset](recordset-object-ado.md) pour accéder à la collection **Properties** qui lui correspond ; ses propriétés sont générées lorsque l'objet **Recordset** est instancié. Toutefois, si l'on attribue à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, cela ajoute plusieurs propriétés dynamiques à la collection **Properties** de l'objet **Recordset**, ce qui rend l'exemple un peu plus intéressant. Pour les besoins de l'illustration, nous utilisons explicitement la propriété [Item](item-property-ado.md) pour accéder à chaque objet [Property](property-object-ado.md).

```vb 
 
'BeginTypePropertyVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rst As ADODB.Recordset 
 Dim prop As ADODB.Property 
 ' property variables 
 Dim ix As Integer 
 Dim strMsg As String 
 
 ' create client-side recordset 
 Set rst = New ADODB.Recordset 
 rst.CursorLocation = adUseClient 
 ' enumerate property types 
 For ix = 0 To rst.Properties.Count - 1 
 Set prop = rst.Properties.Item(ix) 
 Select Case prop.Type 
 Case adBigInt 
 strMsg = "adBigInt" 
 Case adBinary 
 strMsg = "adBinary" 
 Case adBoolean 
 strMsg = "adBoolean" 
 Case adBSTR 
 strMsg = "adBSTR" 
 Case adChapter 
 strMsg = "adChapter" 
 Case adChar 
 strMsg = "adChar" 
 Case adCurrency 
 strMsg = "adCurrency" 
 Case adDate 
 strMsg = "adDate" 
 Case adDBDate 
 strMsg = "adDBDate" 
 Case adDBTime 
 strMsg = "adDBTime" 
 Case adDBTimeStamp 
 strMsg = "adDBTimeStamp" 
 Case adDecimal 
 strMsg = "adDecimal" 
 Case adDouble 
 strMsg = "adDouble" 
 Case adEmpty 
 strMsg = "adEmpty" 
 Case adError 
 strMsg = "adError" 
 Case adFileTime 
 strMsg = "adFileTime" 
 Case adGUID 
 strMsg = "adGUID" 
 Case adIDispatch 
 strMsg = "adIDispatch" 
 Case adInteger 
 strMsg = "adInteger" 
 Case adIUnknown 
 strMsg = "adIUnknown" 
 Case adLongVarBinary 
 strMsg = "adLongVarBinary" 
 Case adLongVarChar 
 strMsg = "adLongVarChar" 
 Case adLongVarWChar 
 strMsg = "adLongVarWChar" 
 Case adNumeric 
 strMsg = "adNumeric" 
 Case adPropVariant 
 strMsg = "adPropVariant" 
 Case adSingle 
 strMsg = "adSingle" 
 Case adSmallInt 
 strMsg = "adSmallInt" 
 Case adTinyInt 
 strMsg = "adTinyInt" 
 Case adUnsignedBigInt 
 strMsg = "adUnsignedBigInt" 
 Case adUnsignedInt 
 strMsg = "adUnsignedInt" 
 Case adUnsignedSmallInt 
 strMsg = "adUnsignedSmallInt" 
 Case adUnsignedTinyInt 
 strMsg = "adUnsignedTinyInt" 
 Case adUserDefined 
 strMsg = "adUserDefined" 
 Case adVarBinary 
 strMsg = "adVarBinary" 
 Case adVarChar 
 strMsg = "adVarChar" 
 Case adVariant 
 strMsg = "adVariant" 
 Case adVarNumeric 
 strMsg = "adVarNumeric" 
 Case adVarWChar 
 strMsg = "adVarWChar" 
 Case adWChar 
 strMsg = "adWChar" 
 Case Else 
 strMsg = "*UNKNOWN*" 
 End Select 
 'show results 
 Debug.Print "Property " & ix & ": " & prop.Name & _ 
 ", Type = " & strMsg 
 Next ix 
 
 ' clean up 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndTypePropertyVB 
```

