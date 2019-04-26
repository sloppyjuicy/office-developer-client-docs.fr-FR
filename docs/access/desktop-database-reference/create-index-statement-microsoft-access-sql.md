---
title: CREATE INDEX, instruction (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295428"
---
# <a name="create-index-statement-microsoft-access-sql"></a>CREATE INDEX, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée un index sur une table existante.

> [!NOTE]
> Pour les bases de données autres que celles de type Microsoft Access, le moteur de base de données Microsoft Access ne prend pas en charge CREATE INDEX (sauf pour créer un pseudo index sur une table liée ODBC), ni les instructions du langage de définition de données (DDL). Utilisez plutôt les méthodes **Create** de DAO. Pour plus d'informations, voir la section Notes.

## <a name="syntax"></a>Syntaxe

CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]

L’instruction CREATE INDEX comprend les parties suivantes :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>index</em></p></td>
<td><p>Nom de l’index à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Nom de la table existante qui contiendra l’index.</p></td>
</tr>
<tr class="odd">
<td><p><em>field</em></p></td>
<td><p>Nom du champ ou des champs à indexer. Pour créer un index d'un seul champ, indiquez le nom du champ entre parenthèses suivi du nom de la table. Pour créer un index de plusieurs champs, indiquez le nom de chaque champ à inclure dans l'index. Pour créer des index décroissants, utilisez le mot réservé DESC, sinon les index sont considérés comme croissants.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Pour interdire la présence de valeurs en double dans les champs indexés d’enregistrements différents, utilisez le mot réservé UNIQUE.

Vous pouvez appliquer des règles de validation dans la clause WITH facultative. Vous pouvez :

- Interdire les entrées Null dans les champs indexés des nouveaux enregistrements en utilisant l’option DISALLOW NULL.

- Empêcher que des enregistrements dont la valeur est **Null** dans les champs indexés soient inclus dans l’index en utilisant l’option IGNORE NULL.

- désigner les champs indexés en tant que clé primaire en utilisant le mot réservé PRIMARY. Ceci implique que la clé soit unique, aussi vous pouvez omettre le mot réservé UNIQUE.

Vous pouvez utiliser CREATE INDEX pour créer un pseudo index sur une table liée dans une source de données ODBC, telle que Microsoft SQL Server qui ne comporte pas d'index. Pour créer un pseudo-index, vous n’avez pas besoin d’autorisation ou d’accès au serveur distant. La base de données distante ignore l’existence du pseudo-index et n’est nullement affectée par celui-ci. Vous utilisez la même syntaxe pour les tables liées et natives. La création d’un pseudo index sur une table ordinairement en lecture seule peut être particulièrement utile.

Vous pouvez également utiliser l'instruction [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) pour ajouter un index d'un seul champ ou de plusieurs champs à une table et l'instruction ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) pour supprimer un index créé avec ALTER TABLE ou CREATE INDEX.

> [!NOTE]
> N’utilisez pas le mot réservé PRIMARY lorsque vous créez un index sur une table qui possède déjà une clé primaire. Autrement, une erreur se produit.

## <a name="example"></a>Exemple

Dans cet exemple, un index comportant les champs Home Phone et Extension dans la table Employees est créé.

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Dans cet exemple, un index est créé sur la table Customers utilisant le champ CustomerID. Deux enregistrements ne peuvent pas avoir les mêmes données dans le champ CustomerID et aucune valeur Null n'est autorisée.

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
