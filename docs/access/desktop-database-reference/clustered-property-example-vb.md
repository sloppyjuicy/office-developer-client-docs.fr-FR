---
title: Clustered, propriété - Exemple (VB)
TOCTitle: Clustered Property Example (VB)
ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15)
ms:contentKeyID: 48543293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4cf09b0e8393eca74b1ed8fbaca8591a99103b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471435"
---
# <a name="clustered-property-example-vb"></a><span data-ttu-id="b84eb-102">Clustered, propriété - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="b84eb-102">Clustered Property Example (VB)</span></span>


<span data-ttu-id="b84eb-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b84eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b84eb-104">Cet exemple illustre la propriété [Clustered](clustered-property-adox.md) d’un [Index](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b84eb-104">This example demonstrates the [Clustered](clustered-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="b84eb-105">Notez que les bases de données Microsoft Jet ne prennent pas charge les index cluster, cet exemple retourne la **valeur False** pour la propriété **Clustered** de tous les index de la base de données *Northwind* .</span><span class="sxs-lookup"><span data-stu-id="b84eb-105">Note that Microsoft Jet databases do not support clustered indexes, so this example will return **False** for the **Clustered** property of all indexes in the *Northwind* database.</span></span>

```vb 
 
' BeginClusteredVB 
Sub Main() 
 On Error GoTo ClusteredXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblLoop As ADOX.Table 
 Dim idxLoop As ADOX.Index 
 Dim strCnn As String 
 
 strCnn = "Provider='SQLOLEDB';Data Source='MySqlServer';Initial Catalog='pubs';" & _ 
 "Integrated Security='SSPI';" 
 ' Connect the catalog. 
 cnn.Open strCnn 
 cat.ActiveConnection = cnn 
 
 ' Enumerate Tables 
 For Each tblLoop In cat.Tables 
 'Enumerate Indexes 
 For Each idxLoop In tblLoop.Indexes 
 Debug.Print tblLoop.Name & " " & _ 
 idxLoop.Name & " " & idxLoop.Clustered 
 Next idxLoop 
 Next tblLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ClusteredXError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndClusteredVB 
```

