---
<span data-ttu-id="220cc-101"><<<<<<< Titre tête : DeleteRule propriété-Exemple (VB) TOCTitle : DeleteRule propriété-Exemple (VB) === titre : DeleteRule, propriété-Exemple (VB) TOCTitle : DeleteRule, propriété-Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="220cc-101"><<<<<<< HEAD title: DeleteRule Property Example (VB) TOCTitle: DeleteRule Property Example (VB) ======= title: DeleteRule property example (VB) TOCTitle: DeleteRule property example (VB)</span></span>
>>>>>>> <span data-ttu-id="220cc-102">Master ms:assetid : 354e00b6-cecb-1132-6923-fc9e8853fa0e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249114(v=office.15) ms:contentKeyID : ms.date 48544142 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="220cc-102">master ms:assetid: 354e00b6-cecb-1132-6923-fc9e8853fa0e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249114(v=office.15) ms:contentKeyID: 48544142 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="220cc-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="220cc-103"><<<<<<< HEAD</span></span>
# <a name="deleterule-property-example-vb"></a><span data-ttu-id="220cc-104">DeleteRule, propriété - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="220cc-104">DeleteRule Property Example (VB)</span></span>
=======
# <a name="deleterule-property-example-vb"></a><span data-ttu-id="220cc-105">DeleteRule, propriété-Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="220cc-105">DeleteRule property example (VB)</span></span>
>>>>>>> <span data-ttu-id="220cc-106">master</span><span class="sxs-lookup"><span data-stu-id="220cc-106">master</span></span>


<span data-ttu-id="220cc-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="220cc-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="220cc-p101">Cet exemple illustre la propriété [DeleteRule](deleterule-property-adox.md) d'un objet [Key](key-object-adox.md). Le code ajoute un nouvel objet [Table](table-object-adox.md), puis définit une nouvelle clé primaire en attribuant la valeur **adRICascade** à la propriété **DeleteRule**.</span><span class="sxs-lookup"><span data-stu-id="220cc-p101">This example demonstrates the [DeleteRule](deleterule-property-adox.md) property of a [Key](key-object-adox.md) object. The code appends a new [Table](table-object-adox.md) and then defines a new primary key, setting **DeleteRule** to **adRICascade**.</span></span>

```vb 
 
' BeginDeleteRuleVB 
Sub Main() 
 On Error GoTo DeleteRuleXError 
 
 Dim kyPrimary As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append the new table 
 cat.Tables.Append tblNew 
 
 ' Define the Primary key 
 kyPrimary.Name = "NumField" 
 kyPrimary.Type = adKeyPrimary 
 kyPrimary.RelatedTable = "Customers" 
 kyPrimary.Columns.Append "NumField" 
 kyPrimary.Columns("NumField").RelatedColumn = "CustomerId" 
 kyPrimary.DeleteRule = adRICascade 
 
 ' Append the primary key 
 cat.Tables("NewTable").Keys.Append kyPrimary 
 Debug.Print "The primary key is appended." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tblNew.Name 
 Debug.Print "The primary key is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 Exit Sub 
 
DeleteRuleXError: 
 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDeleteRuleVB 
```

