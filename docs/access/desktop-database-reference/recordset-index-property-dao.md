---
title: Recordset.Index, propriété (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: b671095411d2bbf96aed7156ac3482fddeb11624
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373003"
---
# <a name="recordsetindex-property-dao"></a>Recordset.Index, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le nom de l’objet **[Index](index-object-dao.md)** actuel dans un type de tableau **[Recordset](recordset-object-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* .Index

*expression* Variable représentant un objet **Recordset**.

## <a name="remarks"></a>Remarques

Les enregistrements de tables de base ne sont pas stockés dans un ordre particulier. Définir le **Index** propriété modifie l’ordre des enregistrements renvoyés à partir de la base de données ; il n’affecte pas l’ordre dans lequel les enregistrements sont stockés.

La valeur **Index** objet doit déjà être défini. Si vous définissez la **Index** propriété pour un **Index** objet n’existe pas ou si le **Index** propriété n’est pas définie lorsque vous utilisez le **[ Avance rapide](recordset-seek-method-dao.md)** méthode, une erreur récupérable se produit.

Examiner la **index** collection d’un **TableDef** objet pour déterminer les éléments **Index** objets sont disponibles pour le type de table **jeu d’enregistrements** les objets créés à partir de qui **TableDef** objet.

Vous pouvez créer un nouvel index de la table en créant une nouvelle **Index** objet définissant ses propriétés, en ajoutant le **index** ensemble de sous-jacents **TableDef** objet et rouvrir le **jeu d’enregistrements** objet.

Les enregistrements renvoyés à partir d'un objet **Recordset** de type table peuvent être uniquement classés en fonction des index définis pour l'objet **TableDef** sous-jacent. Pour trier les enregistrements d'une autre façon, vous pouvez ouvrir un objet **Recordset** de type feuille de réponse dynamique, instantané ou avant uniquement à l'aide d'une instruction SQL avec une clause ORDER BY.

> [!NOTE]
>
> - Vous ne devez créer d’index pour les tableaux. Avec des tableaux de grande taille, non indexés, accéder à un enregistrement spécifique ou en créant un **jeu d’enregistrements** objet peut prendre un certain temps. Créer des index trop grand nombre en revanche, ralentit la mise à jour, ajouter et supprimer des opérations, car tous les index sont automatiquement mis à jour.
> - Enregistrements lus à partir de tables sans index sont renvoyés dans aucune séquence particulière.
> - Le **[attributs](field-attributes-property-dao.md)** propriété de chaque **[champ](field-object-dao.md)** objet dans le **Index** objet détermine la ordre des enregistrements et par conséquent détermine les techniques d’accès à utiliser pour cet index.
> - Un index unique vous permet d’optimiser la recherche des enregistrements.
> - Les index n’ont aucune incidence sur l’ordre physique d’une table de base. Ils affectent uniquement la procédure d’accès aux enregistrements utilisée par l’objet **Recordset** de type table lors de la sélection d’un index particulier ou de l’ouverture d’un objet **Recordset**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Index** pour définir des ordres d’enregistrements différents pour un objet **Recordset** de type table.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
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

Cet exemple illustre la méthode **Seek** en autorisant l’utilisateur à rechercher un produit avec un numéro d’identification.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
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

L’exemple suivant montre comment utiliser la méthode Seek pour rechercher un enregistrement dans une table liée.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
