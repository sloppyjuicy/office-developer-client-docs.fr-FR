---
title: UPDATE, instruction (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6a0404c21b308f6e389ee5577cc212763e660774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306243"
---
# <a name="update-statement-microsoft-access-sql"></a>UPDATE, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée une  qui modifie les valeurs des champs d’une table spécifiée en fonction de critères spécifiés.

## <a name="syntax"></a>Syntaxe

UPDATE *table* SET *newvalue* WHERE *criteria*;

L’instruction SELECT comprend les parties suivantes :

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
<td><p>Nom de la table contenant les données que vous voulez modifier.</p></td>
</tr>
<tr class="even">
<td><p><em>newvalue</em></p></td>
<td><p>Expression qui détermine la valeur à insérer dans un champ particulier dans les enregistrements mis à jour.</p></td>
</tr>
<tr class="odd">
<td><p><em>critères</em></p></td>
<td><p>Expression qui détermine quels enregistrements sont mis à jour. Seuls les enregistrements correspondant à l’expression sont mis à jour.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’instruction UPDATE est particulièrement utile lorsque vous souhaitez modifier de nombreux enregistrements ou que les enregistrements que vous souhaitez modifier résident dans plusieurs tables.

Vous pouvez modifier plusieurs champs simultanément. L’exemple suivant augmente les valeurs de OrderAmount de 10 pour cent et les valeurs de Freight de 3 pour cent pour les transporteurs résidant au Royaume-Uni (UK) :

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- L’instruction UPDATE ne génère pas de jeu de résultats. Par ailleurs, une fois les enregistrements mis à jour à l’aide d’une requête de mise à jour, vous ne pouvez pas annuler l’opération. Pour savoir quels enregistrements ont été mis à jour, commencez par examiner les résultats d’une  qui utilise les mêmes critères, puis exécutez la requête de mise à jour.
- Conservez toujours des copies de sauvegarde de vos données. Si vous mettez à jour des enregistrements par inadvertance, vous pourrez les récupérer à partir de vos copies de sauvegarde.



## <a name="example"></a>Exemple

Cet exemple modifie les valeurs dans le champ responsable à 5 pour tous les enregistrements d’employé qui ont actuellement valeurs responsable de 2.

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
