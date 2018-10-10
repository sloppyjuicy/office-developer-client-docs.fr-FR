---
title: Views Delete, méthode - Exemple (VB)
TOCTitle: Views Delete Method Example (VB)
ms:assetid: 423cd4e6-dfa5-8559-b1f3-b789a7aa9590
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249194(v=office.15)
ms:contentKeyID: 48544474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87efa9fa63fd9561ab27c4a11062e3af6a5f5817
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469933"
---
# <a name="views-delete-method-example-vb"></a><span data-ttu-id="f3812-102">Views Delete, méthode - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="f3812-102">Views Delete Method Example (VB)</span></span>


<span data-ttu-id="f3812-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3812-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f3812-104">Le code suivant montre comment utiliser la méthode [Delete](delete-method-adox-collections.md) pour supprimer une vue du catalogue.</span><span class="sxs-lookup"><span data-stu-id="f3812-104">The following code shows how to use the [Delete](delete-method-adox-collections.md) method to delete a view from the catalog.</span></span>

```vb 
 
' BeginDeleteViewVB 
Sub Main() 
 On Error GoTo DeleteViewError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 'Delete the View 
 cat.Views.Delete "AllCustomers" 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
DeleteViewError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndDeleteViewVB 
```

