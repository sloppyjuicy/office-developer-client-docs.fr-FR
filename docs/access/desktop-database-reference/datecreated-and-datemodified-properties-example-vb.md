---
<span data-ttu-id="18397-101"><<<<<<< Titre tête : DateCreated et DateModified propriétés-exemple (VB) TOCTitle : DateCreated et DateModified propriétés-exemple (VB) === titre : DateCreated et DateModified, propriétés-exemple (VB) TOCTitle : DateCreated et DateModified, propriétés-exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="18397-101"><<<<<<< HEAD title: DateCreated and DateModified Properties Example (VB) TOCTitle: DateCreated and DateModified Properties Example (VB) ======= title: DateCreated and DateModified properties example (VB) TOCTitle: DateCreated and DateModified properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="18397-102">Master ms:assetid : 5afdb5a9-394f-c38f-83a4-ae7017673c5e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249316(v=office.15) ms:contentKeyID : ms.date 48545063 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="18397-102">master ms:assetid: 5afdb5a9-394f-c38f-83a4-ae7017673c5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249316(v=office.15) ms:contentKeyID: 48545063 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="18397-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="18397-103"><<<<<<< HEAD</span></span>
# <a name="datecreated-and-datemodified-properties-example-vb"></a><span data-ttu-id="18397-104">DateCreated et DateModified, propriétés - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="18397-104">DateCreated and DateModified Properties Example (VB)</span></span>
=======
# <a name="datecreated-and-datemodified-properties-example-vb"></a><span data-ttu-id="18397-105">DateCreated et DateModified, propriétés-exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="18397-105">DateCreated and DateModified properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="18397-106">master</span><span class="sxs-lookup"><span data-stu-id="18397-106">master</span></span>


<span data-ttu-id="18397-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18397-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18397-p101">Cet exemple illustre les propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md) par l'ajout d'un nouvel objet [Column](column-object-adox.md) à un objet [Table](table-object-adox.md) existant et la création d'un nouvel objet **Table**. L'exécution de cet exemple requiert la procédure DateOutput.</span><span class="sxs-lookup"><span data-stu-id="18397-p101">This example demonstrates the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties by adding a new [Column](column-object-adox.md) to an existing [Table](table-object-adox.md) and by creating a new **Table**. The DateOutput procedure is required for this example to run.</span></span>

```vb 
 
' BeginDateCreatedVB 
Sub Main() 
 On Error GoTo DateCreatedXError 
 
 Dim cat As New ADOX.Catalog 
 Dim tblEmployees As ADOX.Table 
 Dim tblNewTable As ADOX.Table 
 
 ' Connect the catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 With cat 
 Set tblEmployees = .Tables("Employees") 
 
 ' Print current information about the Employees table. 
 DateOutput "Current properties", tblEmployees 
 
 ' Create and append column to the Employees table. 
 tblEmployees.Columns.Append "NewColumn", adInteger 
 .Tables.Refresh 
 
 ' Print new information about the Employees table. 
 DateOutput "After creating a new column", tblEmployees 
 
 ' Delete new column because this is a demonstration. 
 tblEmployees.Columns.Delete "NewColumn" 
 
 ' Create and append new Table object to the Northwind database. 
 Set tblNewTable = New ADOX.Table 
 tblNewTable.Name = "NewTable" 
 tblNewTable.Columns.Append "NewColumn", adInteger 
 .Tables.Append tblNewTable 
 .Tables.Refresh 
 
 ' Print information about the new Table object. 
 DateOutput "After creating a new table", .Tables("NewTable") 
 
 ' Delete new Table object because this is a demonstration. 
 .Tables.Delete tblNewTable.Name 
 End With 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
DateCreatedXError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
 
Sub DateOutput(strTemp As String, tblTemp As ADOX.Table) 
 ' Print DateCreated and DateModified information about 
 ' specified Table object. 
 Debug.Print strTemp 
 Debug.Print " Table: " & tblTemp.Name 
 Debug.Print " DateCreated = " & tblTemp.DateCreated 
 Debug.Print " DateModified = " & tblTemp.DateModified 
 Debug.Print 
End Sub 
' EndDateCreatedVB 
```

