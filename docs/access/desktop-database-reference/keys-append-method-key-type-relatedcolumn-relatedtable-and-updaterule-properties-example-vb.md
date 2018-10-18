---
<span data-ttu-id="f9bc0-101"><<<<<<< Titre tête : Keys Append, méthode, Key Type, RelatedColumn propriétés-exemple (VB) TOCTitle : Keys Append, méthode, Key Type, RelatedColumn, RelatedTable et UpdateRule propriétés-exemple (VB) === titre : Keys Append, méthode, la clé Type, RelatedColumn, propriétés-exemple (VB) TOCTitle : Keys Append, méthode, Key Type, RelatedColumn, RelatedTable et UpdateRule, propriétés-exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="f9bc0-101"><<<<<<< HEAD title: Keys Append Method, Key Type, RelatedColumn Properties Example (VB) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB) ======= title: Keys Append Method, Key Type, RelatedColumn properties example (VB) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="f9bc0-102">Master ms:assetid : d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl : https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID : ms.date 48547871 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="f9bc0-102">master ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID: 48547871 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f9bc0-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="f9bc0-103"><<<<<<< HEAD</span></span>
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="f9bc0-104">Keys Append, méthode - Exemple de propriétés Key Type, RelatedColumn, RelatedTable et UpdateRule (VB)</span><span class="sxs-lookup"><span data-stu-id="f9bc0-104">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</span></span>
=======
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="f9bc0-105">Clés méthode Append, Key Type, RelatedColumn, RelatedTable et UpdateRule, propriétés-exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="f9bc0-105">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="f9bc0-106">master</span><span class="sxs-lookup"><span data-stu-id="f9bc0-106">master</span></span>


<span data-ttu-id="f9bc0-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9bc0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f9bc0-108">Le code suivant montre comment créer une clé étrangère.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-108">The following code demonstrates how to create a new foreign key.</span></span> <span data-ttu-id="f9bc0-109">Il suppose l’existent de deux tables (**clients** et **commandes**).</span><span class="sxs-lookup"><span data-stu-id="f9bc0-109">It assumes two tables (**Customers** and **Orders**) exist.</span></span>

```vb 
 
' BeginCreateKeyVB 
Sub Main() 
 On Error GoTo CreateKeyError 
 
 Dim kyForeign As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the foreign key 
 kyForeign.Name = "CustOrder" 
 kyForeign.Type = adKeyForeign 
 kyForeign.RelatedTable = "Customers" 
 kyForeign.Columns.Append "CustomerId" 
 kyForeign.Columns("CustomerId").RelatedColumn = "CustomerId" 
 kyForeign.UpdateRule = adRICascade 
 
 ' Append the foreign key 
 cat.Tables("Orders").Keys.Append kyForeign 
 
 'Delete the Key as this is a demonstration 
 cat.Tables("Orders").Keys.Delete kyForeign.Name 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 Exit Sub 
 
CreateKeyError: 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateKeyVB 
```

