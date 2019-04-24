---
title: Recordset2. index, propriété (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307300"
---
# <a name="recordset2index-property-dao"></a>Recordset2. index, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le nom de l'objet **[Index](index-object-dao.md)** actif dans un objet **[Recordset](recordset-object-dao.md)** de type table (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Évaluer

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Les enregistrements des tables de base ne sont pas stockés dans un ordre précis. La définition de la propriété **Index** modifie l'ordre des enregistrements renvoyés par la base de données, elle n'a aucune incidence sur l'ordre en fonction duquel ils sont enregistrés.

L'objet **Index** spécifié doit déjà être défini. Si vous attribuez à la propriété **Index** un objet **Index** qui n'existe pas ou si la propriété **Index** n'est pas définie lorsque vous appelez la méthode **[Seek](recordset2-seek-method-dao.md)**, une erreur piégeable se produit.

Examinez la collection **Indexes** d'un objet **TableDef** pour identifier les objets **Index** disponibles pour des objets **Recordset** de type table créés à partir de cet objet **TableDef**.

Pour créer un nouvel index pour la table, créez un objet **Index**, définissez ses propriétés, ajoutez-le à la collection **Indexes** de l'objet **TableDef** sous-jacent puis rouvrez l'objet **Recordset**.

Les enregistrements renvoyés à partir d'un objet **Recordset** de type table peuvent être uniquement classés en fonction des index définis pour l'objet **TableDef** sous-jacent. Pour trier les enregistrements d'une autre manière, vous pouvez ouvrir un objet Recordset de type feuille de réponse dynamique, instantané **** ou avant uniquement à l'aide d'une instruction SQL avec une clause ORDER BY.

> [!NOTE]
> - Il n'est pas nécessaire de créer des index pour les tables. Dans le cas de tables volumineuses et non indexées, l'accès à un enregistrement spécifique ou la création d'un objet **Recordset** peut demander du temps. D'autre part, la création d'un nombre excessif d'index ralentit les opérations de mise à jour, d'ajout et de suppression car tous les index sont automatiquement mis à jour.
> - Les enregistrements non indexés et lus à partir de tables sont renvoyés sans ordre particulier.
> - La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** présent dans l'objet **Index** détermine l'ordre des enregistrements et, par conséquent, les techniques d'accès à utiliser pour cet index.
> - Un index unique permet d'optimiser la recherche d'enregistrements.
> - Les index n'ont aucune incidence sur l'ordre physique d'une table de base. Ils affectent uniquement la procédure d'accès aux enregistrements utilisée par l'objet **Recordset** de type table lors de la sélection d'un index particulier ou de l'ouverture de l'objet **Recordset**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Index** pour définir plusieurs ordres de tri des enregistrements d'un objet **Recordset** de type table.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple illustre la méthode **Seek** qui permet à l'utilisateur de rechercher un produit en fonction d'un numéro d'identification.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
