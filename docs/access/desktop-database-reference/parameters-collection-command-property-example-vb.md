---
title: Parameters, collection - Exemple de propriété Command (VB)
TOCTitle: Parameters Collection, Command property example (VB)
ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15)
ms:contentKeyID: 48544290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a42506553da935f4d2622ad76b9dabc26573e890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568725"
---
# <a name="parameters-collection-command-property-example-vb"></a>Parameters, collection - Exemple de propriété Command (VB)


**S’applique à** : Access 2013, Office 2013

Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) avec l'objet [Command](command-object-ado.md) afin d'extraire les données de paramètres pour la procédure.

```vb 
 
' BeginParametersVB 
Sub Main() 
 On Error GoTo ProcedureParametersError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command object 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Retrieve Parameter information 
 cmd.Parameters.Refresh 
 For Each prm In cmd.Parameters 
 Debug.Print prm.Name & ":" & prm.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureParametersError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndParametersVB 
```

