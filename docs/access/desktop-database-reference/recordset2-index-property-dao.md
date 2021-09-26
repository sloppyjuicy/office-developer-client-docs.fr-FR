---
title: Recordset2.Index, propriété (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a01adf65d4358d12983c7d0c2e90aa9de02f1937
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611734"
---
# <a name="recordset2index-property-dao"></a>Recordset2.Index, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le nom de l’objet **[Index](index-object-dao.md)** actuel dans un type de tableau **[Recordset](recordset-object-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* .Index

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Les enregistrements de tables de base ne sont pas stockés dans un ordre particulier. Définir le **Index** propriété modifie l’ordre des enregistrements renvoyés à partir de la base de données ; il n’affecte pas l’ordre dans lequel les enregistrements sont stockés.

La valeur **Index** objet doit déjà être défini. Si vous définissez la **Index** propriété pour un **Index** objet n’existe pas ou si le **Index** propriété n’est pas définie lorsque vous utilisez le **[ Avance rapide](recordset2-seek-method-dao.md)** méthode, une erreur récupérable se produit.

Examiner la **index** collection d’un **TableDef** objet pour déterminer les éléments **Index** objets sont disponibles pour le type de table **jeu d’enregistrements** les objets créés à partir de qui **TableDef** objet.

Vous pouvez créer un nouvel index de la table en créant une nouvelle **Index** objet définissant ses propriétés, en ajoutant le **index** ensemble de sous-jacents **TableDef** objet et rouvrir le **jeu d’enregistrements** objet.

Enregistrements renvoyés à partir d’un type de table **jeu d’enregistrements** objet peut être ordonné de façon uniquement par les index définis pour sous-jacents **TableDef** objet. Pour trier les enregistrements d’une autre façon, vous pouvez ouvrir un objet **Recordset** de type feuille de réponse dynamique, instantané ou avant uniquement à l’aide d’une instruction SQL avec une clause ORDER BY.

> [!NOTE]
> - Vous ne devez créer d’index pour les tableaux. Avec des tableaux de grande taille, non indexés, accéder à un enregistrement spécifique ou en créant un **jeu d’enregistrements** objet peut prendre un certain temps. Créer des index trop grand nombre en revanche, ralentit la mise à jour, ajouter et supprimer des opérations, car tous les index sont automatiquement mis à jour.
> - Enregistrements lus à partir de tables sans index sont renvoyés dans aucune séquence particulière.
> - Le **[attributs](field-attributes-property-dao.md)** propriété de chaque **[champ](field-object-dao.md)** objet dans le **Index** objet détermine la ordre des enregistrements et par conséquent détermine les techniques d’accès à utiliser pour cet index.
> - Un index unique vous permet d’optimiser la recherche des enregistrements.
> - Les index n'ont aucune incidence sur l'ordre physique d'une table de base. Ils affectent uniquement la procédure d'accès aux enregistrements utilisée par l'objet **Recordset** de type table lors de la sélection d'un index particulier ou de l'ouverture de l'objet **Recordset**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Index** pour définir des ordres d’enregistrements différents pour un objet **Recordset** de type table.

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

Cet exemple illustre la méthode **Seek** en autorisant l’utilisateur à rechercher un produit avec un numéro d’identification.

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
