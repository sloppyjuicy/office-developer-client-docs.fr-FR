---
title: Description, HelpContext, HelpFile propriétés-exemple (VB)
TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB)
ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15)
ms:contentKeyID: 48544304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8c15c60e5465e5bb0dae551e3234616e2da11ee
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470324"
---
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="cceaa-102">Description, HelpContext, HelpFile, NativeError, Number, Source et SQLState, propriétés - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="cceaa-102">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB)</span></span>


<span data-ttu-id="cceaa-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cceaa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cceaa-104">Cet exemple déclenche une erreur, l'intercepte et affiche les propriétés [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md) et [SQLState](sqlstate-property-ado.md) de l'objet [Error](error-object-ado.md) qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="cceaa-104">This example triggers an error, traps it, and displays the [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md), and [SQLState](sqlstate-property-ado.md) properties of the resulting [Error](error-object-ado.md) object.</span></span>

```vb
    'BeginDescriptionVB
    Public Sub Main()
    
        Dim Cnxn As ADODB.Connection
        Dim Err As ADODB.Error
        Dim strError As String
        
        On Error GoTo ErrorHandler
        
        ' Intentionally trigger an error
        Set Cnxn = New ADODB.Connection
        Cnxn.Open "nothing"
        
        Set Cnxn = Nothing
        Exit Sub
    
    ErrorHandler:
    
        ' Enumerate Errors collection and display
        ' properties of each Error object
        For Each Err In Cnxn.Errors
            strError = "Error #" & Err.Number & vbCr & _
                "   " & Err.Description & vbCr & _
                "   (Source: " & Err.Source & ")" & vbCr & _
                "   (SQL State: " & Err.SQLState & ")" & vbCr & _
                "   (NativeError: " & Err.NativeError & ")" & vbCr
            If Err.HelpFile = "" Then
                strError = strError & "   No Help file available"
            Else
                strError = strError & _
                   "   (HelpFile: " & Err.HelpFile & ")" & vbCr & _
                   "   (HelpContext: " & Err.HelpContext & ")" & _
                   vbCr & vbCr
            End If
             
            Debug.Print strError
        Next
    
        Resume Next
    End Sub
    'EndDescriptionVB
```
