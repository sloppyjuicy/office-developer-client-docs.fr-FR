---
title: DELETE, instruction (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: cf07e10b32dad6c1ef0dba2d2ad14b516ffe1ed5
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633553"
---
# <a name="delete-statement-microsoft-access-sql"></a>DELETE, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée une requête qui supprime les enregistrements d’une ou de plusieurs tables répertoriées dans la clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) qui satisfont à la clause [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).

## <a name="syntax"></a>Syntaxe

DELETE \[*table*.\*\] FROM *table* WHERE *criteria*

L’instruction DELETE est composée des éléments suivants :

<table>
<colgroup>
<col />
<col />
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
<td><p>Nom facultatif de la table où sont supprimés les enregistrements.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Nom de la table où sont supprimés les enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>Expression qui détermine les enregistrements à supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’instruction DELETE est particulièrement utile pour supprimer plusieurs enregistrements.

Pour supprimer une table entière de la base de données, vous pouvez utiliser la méthode **Execute** avec une instruction [DROP](drop-statement-microsoft-access-sql.md). Si vous supprimez la table, sa structure est perdue. En revanche, si vous utilisez la clause DELETE, seules les données sont supprimées ; la structure de la table et toutes ses propriétés, telles que les attributs des champs et les index, sont conservées.

Vous pouvez utiliser DELETE pour supprimer des enregistrements des tables qui sont dans une relation de un à plusieurs avec d'autres tables. Les opérations de suppression en cascade entraînent la suppression des enregistrements des tables qui sont du côté 'plusieurs' de la relation lorsque l'enregistrement correspondant du côté 'un' est supprimé dans la requête. Par exemple, dans la relation entre les tables Customers et Orders, la table Customers est du côté 'un' et la table Orders est du côté 'plusieurs' de la relation. Lorsqu'un enregistrement est supprimé de la table Customers, les enregistrements correspondants sont supprimés de la table Orders si l'option de suppression en cascade est spécifiée.

Une requête de suppression supprime les enregistrements, et pas seulement les données dans des champs spécifiques. Si vous voulez supprimer des valeurs dans un champ spécifique, créez une requête de mise à jour qui remplacent ces valeurs par des valeurs **Null**.

> [!IMPORTANT]
> - Une fois que des enregistrements sont supprimés à l'aide d'une requête de suppression, il n'est pas possible d'annuler cette opération. Si vous voulez savoir quels enregistrements ont été supprimés, examinez d'abord les résultats d'une requête de sélection qui utilise les mêmes critères, puis exécutez la requête de suppression.
> - Conservez toujours des copies de sauvegarde de vos données. Si vous ne supprimez pas les bons enregistrements, vous pouvez les récupérer à partir de vos copies de sauvegarde.

## <a name="example"></a>Exemple

Dans cet exemple, tous les enregistrements d'employés dont le titre est Trainee, sont supprimés. Lorsque la clause FROM ne comporte qu'une seule table, vous n'avez pas besoin d'indiquer le nom de la table dans l'instruction DELETE.



```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```
