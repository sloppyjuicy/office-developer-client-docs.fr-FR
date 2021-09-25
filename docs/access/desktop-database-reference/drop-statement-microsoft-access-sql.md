---
title: DROP, instruction (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 79e844c7694bf399496fb79bebf550e7c51ba8f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562684"
---
# <a name="drop-statement-microsoft-access-sql"></a>DROP, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Supprime une table, une procédure ou un affichage existants d’une base de données, ou supprime un index existant d’une table.

> [!NOTE]
> Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction DROP, ni les instructions DDL, avec des bases de données autres que Microsoft Access. Pour cela, utilisez la méthode DAO **Delete**.

## <a name="syntax"></a>Syntaxe

DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}

L’instruction DROP est composée des éléments suivants :

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
<td><p><em>table</em></p></td>
<td><p>Nom de la table à supprimer, ou de la table à partir de laquelle un index doit être supprimé.</p></td>
</tr>
<tr class="even">
<td><p><em>procedure</em></p></td>
<td><p>Nom de la procédure à supprimer.</p></td>
</tr>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>Nom de l’affichage à supprimer.</p></td>
</tr>
<tr class="even">
<td><p><em>index</em></p></td>
<td><p>Nom de l’index à supprimer de la <em>table.</em></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous devez fermer la table avant de pouvoir la supprimer ou de pouvoir y supprimer un index.

Vous pouvez également utiliser [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) pour supprimer un index d'une table.

Vous pouvez utiliser [CREATE TABLE](create-table-statement-microsoft-access-sql.md) pour créer une table et [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ou ALTER TABLE pour créer un index. Pour modifier une table, utilisez ALTER TABLE.

## <a name="example"></a>Exemple

Dans l'exemple suivant, un index NewIndex hypothétique est censé exister dans la table Employees de la base de données Northwind.

Dans cet exemple, l'index NewIndex est supprimé de la table Employees.

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Dans cet exemple, la table Employees est supprimée de la base de données.

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
