---
title: ALTER TABLE (Microsoft Access SQL), instruction
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 07a83c16368caa6e5c05c7554300c5589a437067
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734181"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>ALTER TABLE (Microsoft Access SQL), instruction

**S’applique à** : Access 2013, Office 2013

Modifie la structure d’une table après qu’elle a été créée avec l’instruction [CREATE TABLE](create-table-statement-microsoft-access-sql.md).

> [!NOTE]
> Le moteur de base de données Access ne prend pas en charge l’utilisation de l’instruction ALTER TABLE ou d’instructions en langage de définition de données (DDL) avec des bases de données autres que Microsoft Access. Utilisez plutôt les méthodes **Create** de DAO.

## <a name="syntax"></a>Syntaxe

ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }

L'instruction ALTER TABLE est composée des arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Nom de la table à modifier.</p></td>
</tr>
<tr class="even">
<td><p><em>champ</em></p></td>
<td><p>Nom du champ à ajouter ou à supprimer de la <em>table</em>. Ou, nom du champ à modifier dans la <em>table</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Type de données du <em>champ</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>taille</em></p></td>
<td><p>Taille du champ en nombre de caractères (champs texte et binaires seulement).</p></td>
</tr>
<tr class="odd">
<td><p><em>index</em></p></td>
<td><p>Index pour <em>field</em>. Pour plus d’informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT, clause</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>Définition d’un index multichamp à ajouter à <em>table</em>. Pour plus d’informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT, clause</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>indexname</em></p></td>
<td><p>Nom de l'index de plusieurs champs à supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’instruction ALTER TABLE permet de modifier une table existante de plusieurs manières. Vous pouvez :

- Utilisez ADD COLUMN pour ajouter un champ à la table. Vous devez pour cela spécifier le nom du champ, le type des données et éventuellement la taille du champ (pour les champs texte et binaires). Par exemple, l'instruction suivante ajoute un champ texte de 25 caractères appelé Notes à la table Employees :
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  Vous pouvez également définir un index sur ce champ. Pour plus d’informations sur les index à champ unique, voir [CONSTRAINT, clause](constraint-clause-microsoft-access-sql.md).
    
  Si vous spécifiez NOT NULL pour un champ, les nouveaux enregistrements doivent disposer de données valides dans ce champ.

- Utilisez ALTER COLUMN pour changer le type des données d'un champ existant. Vous devez pour cela spécifier le nom du champ, le nouveau type des données et éventuellement la taille du champ (pour les champs texte et binaires). Par exemple, l'instruction suivante change le type des données d'un champ ZipCode de la table Employees en remplaçant l'entier qui s'y trouvait par du texte comportant 10 caractères :
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- Utilisez l’instruction ADD CONSTRAINT pour ajouter un index multichamp. Pour plus d’informations sur les index multichamps, voir [CONSTRAINT, clause](constraint-clause-microsoft-access-sql.md).

- Utilisez DROP COLUMN pour supprimer un champ. Vous ne devez pour cela spécifier que le nom du champ.

- Utilisez DROP CONSTRAINT pour supprimer un index de plusieurs champs. Vous ne devez pour cela spécifier que le nom de l'index suivant le mot réservé CONSTRAINT.


> [!NOTE] 
> - Vous ne pouvez pas ajouter ou supprimer plus d'un champ ou d'un index à la fois.
> - Vous pouvez utiliser l’instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour ajouter un index d’un ou de plusieurs champs à une table et l’instruction ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) pour supprimer un index créé avec ALTER TABLE ou CREATE INDEX.
> - Vous pouvez utiliser l’instruction NON NULL sur un champ unique ou à l’intérieur d’une clause CONSTRAINT nommée qui s’applique à une instruction CONSTRAINT nommée portant sur un ou plusieurs champs. Toutefois, vous ne pouvez appliquer la restriction NON NULL qu’une seule fois à un champ. Une tentative d’appliquer cette restriction plusieurs fois génère une erreur d’exécution.

## <a name="example"></a>Exemple

Dans cet exemple, un champ Salary avec le type de données **Money** est ajouté à la table Employees.

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Dans cet exemple, le type de données **Money** du champ Salary est remplacé par **Char**.

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Modify the existing Salary field of the Employees table  
        ' by changing it to a CHAR data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Dans cet exemple, le champ Salary est supprimé de la table Employees.

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Dans cet exemple, une clé étrangère est ajoutée à la table Orders. La clé étrangère est basée sur le champ EmployeeID et fait référence au champ EmployeeID de la table Employees. Vous n’avez pas besoin d’indiquer le champ EmployeeID à la suite de la table Employees dans la clause REFERENCES, car EmployeeID est la clé primaire de la table Employees.

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Dans cet exemple, la clé étrangère est supprimée de la table Orders.

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
