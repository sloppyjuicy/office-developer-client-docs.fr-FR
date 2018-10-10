---
title: Database.CreateTableDef, méthode (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e85c9f22ecfa6efa11a3d916e0bb374948df6104
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470338"
---
# <a name="databasecreatetabledef-method-dao"></a>Database.CreateTableDef, méthode (DAO)

**S’applique à**: Access 2013 | Office 2013

Crée un objet **[TableDef](tabledef-object-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . CreateTableDef (***nom***, ***attributs***, ***SourceTableName***, ***connecter***)

*expression* Variable qui représente un objet de **base de données** .

### <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>TableDef</strong>. Consultez la propriété <strong><a href="tabledef-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms d’objets <strong>TableDef</strong> valides.</p></td>
</tr>
<tr class="even">
<td><p>Attributs</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Constante ou combinaison de constantes spécifiant une ou plusieurs caractéristiques du nouvel objet <strong>TableDef</strong>. Pour plus d'informations, consultez la propriété <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>SourceTableName</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui comprend le nom d’une table d’une base de données externe représentant la source des données d’origine. La chaîne source devient la valeur affectée à la propriété <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> du nouvel objet <strong>TableDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Connexion</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) contenant des informations sur la source d’une base de données ouverte, une base de données utilisée dans une requête directe ou une table liée. Consultez la propriété <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> pour plus d’informations sur les chaînes de connexion valides.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

TableDef

## <a name="remarks"></a>Remarques

Si vous omettez un ou plusieurs arguments facultatifs avec la méthode **CreateTableDef**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou redéfinir la propriété correspondante avant d'ajouter le nouvel objet à la collection. Après l'ajout de l'objet, il est toujours possible de modifier certaines de ses propriétés. Pour plus d'informations, consultez les rubriques des différentes propriétés.

Si le nom fait référence à un objet qui est déjà membre de la collection, ou si vous spécifiez une propriété non valide dans l’objet **TableDef** ou **[Field](field-object-dao.md)** que vous ajoutez, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](tabledefs-append-method-dao.md)** . En outre, vous ne pouvez pas ajouter d'objet **TableDef** à la collection **TableDefs** avant d'avoir défini au moins un objet **Field** pour l'objet **TableDef**.

Pour supprimer un objet **TableDef** de la collection **[TableDefs](tabledefs-collection-dao.md)**, appelez la méthode **[Delete](tabledefs-delete-method-dao.md)** sur la collection.

## <a name="example"></a>Exemple

Cet exemple crée un objet **TableDef** dans la base de données Northwind.

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple utilise les méthodes **CreateTableDef** et **FillCache** ainsi que les propriétés **CacheSize**, **CacheStart** et **SourceTableName** pour énumérer deux fois les enregistrements dans une table liée. Ensuite, il énumère également deux fois les enregistrements avec un cache de 50 enregistrements. Enfin, il affiche les statistiques de performance pour les deux exécutions, avec et sans mise en cache, dans la table liée.

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
