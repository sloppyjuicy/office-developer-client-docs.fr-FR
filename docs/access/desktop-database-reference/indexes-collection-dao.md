---
title: Indexes, collection (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f731862e12a75f91d07ea7d012cc33dad5be0b55
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701178"
---
# <a name="indexes-collection-dao"></a>Indexes, collection (DAO)

**S’applique à**: Access 2013, Office 2013

Une collection **Indexes** contient tous les objets **Index** stockés d'un objet **TableDef** (Espaces de travail Microsoft Access uniquement).

## <a name="remarks"></a>Remarques

Lorsque vous accédez à un objet Recordset de type table, la propriété **Index** de l'objet permet de spécifier l'ordre des enregistrements. Affectez-lui comme valeur le paramètre de propriété **Name** d'un objet **Index** existant dans la collection **Indexes** de l'objet **[TableDef](tabledef-object-dao.md)** sous-jacent à l'objet **[Recordset](recordset-object-dao.md)**.

> [!NOTE]
> [!REMARQUE] Vous pouvez utiliser la méthode **Append** ou **Delete** sur une collection **Indexes** uniquement si le paramètre de propriété **[Updatable](connection-updatable-property-dao.md)** de l'objet **TableDef** contenant est défini sur **True**.

Après avoir créé un nouvel objet **Index**, il convient d'utiliser la méthode **Append** pour l'ajouter à la collection **Indexes** de l'objet **TableDef**.

> [!IMPORTANT]
> [!IMPORTANTE] Vérifiez que vos données sont conformes aux attributs de votre nouvel index. Si ce dernier exige des valeurs uniques, vérifiez que les enregistrements de données existants n'ont aucun doublon. S'il en existe, le moteur de base de données Microsoft Access ne peut pas créer l'index ; une erreur capturable survient alors lorsque vous tentez d'utiliser la méthode Append sur le nouvel index.

## <a name="example"></a>Exemple

Cet exemple crée un nouvel objet **Index**, l'ajoute à la collection **Indexes** de la **TableDef** Employees, puis énumère la collection **Indexes** de la **TableDef**. Enfin, il énumère un objet **Recordset**, d'abord à l'aide de l' **Index** primaire, ensuite à l'aide du nouvel objet **Index**. La procédure IndexOutput est requise pour exécuter cette opération.

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

Cet exemple utilise la méthode **CreateIndex** pour créer deux nouveaux objets **Index** et les ajouter à la collection **Indexes** de l'objet **TableDef** Employees. Il énumère ensuite la collection **Indexes** de l'objet **TableDef**, la collection **Fields** des nouveaux objets **Index**, et la collection Properties des nouveaux objets **Index**. La fonction CreateIndexOutput est requise pour exécuter cette opération.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
