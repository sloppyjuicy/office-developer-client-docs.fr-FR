---
title: Instruction CREATE INDEX (Microsoft Access SQL)
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
ms.openlocfilehash: 7710dd89a645b10d20044e2eeaeb26986730c843
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861553"
---
# <a name="create-index-statement-microsoft-access-sql"></a>Instruction CREATE INDEX (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

Crée un nouvel index sur une table existante.

> [!NOTE]
> Pour les bases de données Microsoft Access, le moteur de base de données Microsoft Access ne prend pas en charge l’utilisation de CREATE INDEX (sauf pour créer un pseudo index sur une table liée ODBC) ou une des instructions de langage de définition de données. Utilisez les méthodes **Create DAO** à la place. Pour plus d’informations, voir la section Remarques.

## <a name="syntax"></a>Syntaxe

CRÉER \[ UNIQUE \] INDEX *index* ON *table* (*champ* \[ASC | DESC\]\[, *champ* \[ASC | DESC\],... \]) \[WITH {PRIMARY | DISALLOW NULL | IGNORE NULL}\]

L'instruction CREATE INDEX est composée des arguments suivants :

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
<td><p><em>index</em></p></td>
<td><p>Nom de l'index à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Nom de la table existante qui contiendra l'index.</p></td>
</tr>
<tr class="odd">
<td><p><em>champ</em></p></td>
<td><p>Nom du champ ou des champs à indexer. Pour créer un index d'un seul champ, indiquez le nom du champ entre parenthèses suivi du nom de la table. Pour créer un index de plusieurs champs, indiquez le nom de chaque champ à inclure dans l'index. Pour créer des index décroissants, utilisez le mot réservé DESC, sinon les index sont considérés comme croissants.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Pour interdire les valeurs dupliquées dans les champs indexés de différent enregistrements, utilisez le mot réservé UNIQUE.

Dans la clause WITH facultative, vous pouvez appliquer des règles de validation de données. Vous pouvez :

- interdire les entrées Null dans les champs indexés de nouveaux enregistrements à l'aide de l'option DISALLOW NULL ;

- empêcher que des enregistrements avec des valeurs **Null** dans les champs indexés soient inclus dans l'index à l'aide de l'option IGNORE NULL ;

- désigner les champs indexés en tant que clé primaire en utilisant le mot réservé PRIMARY. Ceci implique que la clé soit unique, aussi vous pouvez omettre le mot réservé UNIQUE.

Vous pouvez utiliser CREATE INDEX pour créer un pseudo index sur une table liée dans une source de données ODBC, telle que Microsoft SQL Server, qui n’a pas déjà un index. Vous n'avez pas besoin d'une autorisation d'accès particulière au serveur distant pour créer un pseudo index ; la base de données distante ignore l'existence du pseudo index qui n'a par conséquent aucune incidence sur celle-ci. Utilisez la même syntaxe pour les tables liées et natives. Créer un pseudo index sur une table qui est normalement en lecture seule peut s'avérer particulièrement utile.

Vous pouvez également utiliser l'instruction [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) pour ajouter un index d'un seul champ ou de plusieurs champs à une table et l'instruction ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) pour supprimer un index créé avec ALTER TABLE ou CREATE INDEX.

> [!NOTE]
> [!REMARQUE] N'utilisez pas le mot réservé PRIMARY lorsque vous créez un nouvel index sur une table qui comporte déjà une clé primaire ; si vous le faites, une erreur se produit.

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
