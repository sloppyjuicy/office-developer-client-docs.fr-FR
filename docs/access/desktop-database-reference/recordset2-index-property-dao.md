---
title: Propriété Recordset2.index (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 034fd349f140e931d1a5f654dfb275854aa2b78d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998979"
---
# <a name="recordset2index-property-dao"></a>Propriété Recordset2.index (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le nom de l'objet **[Index](index-object-dao.md)** actif d'un objet **[Recordset](recordset-object-dao.md)** de type table (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Index

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Les enregistrements des tables de base ne sont stockés dans aucun ordre particulier. Le fait de définir la propriété **Index** modifie l'ordre des enregistrements renvoyés de la base de données ; cela n'affecte par l'ordre dans lequel les enregistrements sont stockés.

L'objet **Index** spécifié doit déjà être défini. Si vous définissez la propriété **Index** d'un objet **Index** qui n'existe pas ou si la propriété **Index** n'est pas définie lorsque vous utilisez la méthode **[Seek](recordset2-seek-method-dao.md)**, une erreur capturable survient.

Examinez la collection **Indexes** d'un objet **TableDef** pour déterminer les objets **Index** disponibles pour les objets **Recordset** de type table créés à partir de cet objet **TableDef**.

Vous pouvez créer un nouvel index pour la table en créant un nouvel objet **Index**, définissant ses propriétés, l'ajoutant à la collection **Indexes** de l'objet **TableDef** sous-jacent et en rouvrant l'objet **Recordset**.

Les enregistrements renvoyés d'un objet **Recordset** de type table peuvent être classés uniquement par les index définis pour l'objet **TableDef** sous-jacent. Pour trier les enregistrements d’une autre façon, vous pouvez ouvrir un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique à l’aide d’une instruction SQL avec une clause ORDER BY.

> [!NOTE]
> - Vous n'avez pas à créer d'index pour les tables. Avec des grandes tables non indexées, l'accès à un enregistrement spécifique ou la création d'un objet **Recordset** peut prendre du temps. Toutefois, la création d'un nombre trop important d'index ralentit les opérations de mise à jour, d'ajout et de suppression car tous les index sont automatiquement mis à jour.
> - Les enregistrements lus à partir des tables non indexées sont retournés sans ordre particulier.
> - La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** de l'objet **Index** détermine l'ordre des enregistrements et, par conséquent, les techniques d'accès à utiliser pour cet index.
> - Un index unique permet d'optimiser la recherche d'enregistrements.
> - Les index n'affectent pas l'ordre physique d'une table de base, ils affectent uniquement la manière dont l'objet **Recordset** de type table accède aux enregistrements lorsqu'un index spécifique est choisi ou lorsque l'objet **Recordset** est ouvert.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Index** pour définir des ordres d'enregistrements différents pour un objet **Recordset** de type table.

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

Cet exemple démontre la méthode **Seek** en permettant à l'utilisateur de rechercher un produit en fonction d'un numéro d'identification.

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
