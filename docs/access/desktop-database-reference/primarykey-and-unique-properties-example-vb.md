---
<span data-ttu-id="5a916-101"><<<<<<< Titre tête : PrimaryKey et Unique propriétés exemple (VB) TOCTitle : PrimaryKey et Unique propriétés exemple (VB) === titre : PrimaryKey et Unique, propriétés-exemple (VB) TOCTitle : PrimaryKey et Unique, propriétés-exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="5a916-101"><<<<<<< HEAD title: PrimaryKey and Unique Properties Example (VB) TOCTitle: PrimaryKey and Unique Properties Example (VB) ======= title: PrimaryKey and Unique properties example (VB) TOCTitle: PrimaryKey and Unique properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="5a916-102">Master ms:assetid : 888f1a35-b883-2449-3b70-103e5116b29f ms:mtpsurl : https://msdn.microsoft.com/library/JJ249597(v=office.15) ms:contentKeyID : ms.date 48546137 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="5a916-102">master ms:assetid: 888f1a35-b883-2449-3b70-103e5116b29f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249597(v=office.15) ms:contentKeyID: 48546137 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5a916-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5a916-103"><<<<<<< HEAD</span></span>
# <a name="primarykey-and-unique-properties-example-vb"></a><span data-ttu-id="5a916-104">PrimaryKey et Unique, propriétés - Exemples (VB)</span><span class="sxs-lookup"><span data-stu-id="5a916-104">PrimaryKey and Unique Properties Example (VB)</span></span>
=======
# <a name="primarykey-and-unique-properties-example-vb"></a><span data-ttu-id="5a916-105">PrimaryKey et Unique, propriétés-exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="5a916-105">PrimaryKey and Unique properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="5a916-106">master</span><span class="sxs-lookup"><span data-stu-id="5a916-106">master</span></span>


<span data-ttu-id="5a916-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a916-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5a916-p101">Cet exemple illustre les propriétés [PrimaryKey](primarykey-property-adox.md) et [Unique](unique-property-adox.md) d'un objet [Index](index-object-adox.md). Le code crée une table de deux colonnes. Les propriétés **PrimaryKey** et **Unique** servent à définir une colonne en tant que clé primaire pour laquelle les doublons ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="5a916-p101">This example demonstrates the [PrimaryKey](primarykey-property-adox.md) and [Unique](unique-property-adox.md) properties of an [Index](index-object-adox.md). The code creates a new table with two columns. The **PrimaryKey** and **Unique** properties are used to make one column the primary key for which duplicate values are not allowed.</span></span>

```vb 
 
' BeginPrimaryKeyVB 
Sub Main() 
 On Error GoTo PrimaryKeyXError 
 
 Dim catNorthwind As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 Dim idxNew As New ADOX.Index 
 Dim idxLoop As New ADOX.Index 
 Dim colLoop As New ADOX.Column 
 
 ' Connect the catalog 
 catNorthwind.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append new Primary Key index on NumField column 
 ' to new table 
 idxNew.Name = "NumIndex" 
 idxNew.Columns.Append "NumField" 
 idxNew.PrimaryKey = True 
 idxNew.Unique = True 
 tblNew.Indexes.Append idxNew 
 
 ' Append an index on Textfield to new table. 
 ' Note the different technique: Specifying index and 
 ' column name as parameters of the Append method 
 tblNew.Indexes.Append "TextIndex", "TextField" 
 
 ' Append the new table 
 catNorthwind.Tables.Append tblNew 
 
 With tblNew 
 Debug.Print tblNew.Indexes.Count & " Indexes in " & _ 
 tblNew.Name & " Table" 
 
 ' Enumerate Indexes collection. 
 For Each idxLoop In .Indexes 
 With idxLoop 
 Debug.Print "Index " & .Name 
 Debug.Print " Primary key = " & .PrimaryKey 
 Debug.Print " Unique = " & .Unique 
 
 ' Enumerate Columns collection of each Index 
 ' object. 
 Debug.Print " Columns" 
 For Each colLoop In .Columns 
 Debug.Print " " & colLoop.Name 
 Next colLoop 
 End With 
 Next idxLoop 
 
 End With 
 
 ' Delete new table as this is a demonstration. 
 catNorthwind.Tables.Delete tblNew.Name 
 
 'Clean up 
 Set catNorthwind.ActiveConnection = Nothing 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 Exit Sub 
 
PrimaryKeyXError: 
 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndPrimaryKeyVB 
```

