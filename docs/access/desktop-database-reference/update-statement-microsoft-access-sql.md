---
title: Mise à jour, instruction (Microsoft Access SQL)
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
ms.openlocfilehash: 7a761fbc6404cf72818271b956bfc63516942d25
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863282"
---
# <a name="update-statement-microsoft-access-sql"></a>Mise à jour, instruction (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

Crée une requête Mise à jour qui modifie les valeurs dans les champs d'une table spécifiée, sur la base de critères spécifiés.

## <a name="syntax"></a>Syntaxe

UPDATE *table* SET *NouvelleValeur* WHERE *critère*;

L’instruction UPDATE se compose de trois éléments :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Élément</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Nom de la table contenant les données que vous souhaitez modifier.</p></td>
</tr>
<tr class="even">
<td><p><em>newValue</em></p></td>
<td><p>Expression qui détermine la valeur à insérer dans un champ particulier dans les enregistrements mis à jour.</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>Expression qui détermine les enregistrements qui seront mis à jour. Seuls les enregistrements qui répondent à l'expression sont mis à jour.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'instruction UPDATE est particulièrement utile lorsque vous voulez modifier un grand nombre d'enregistrements ou lorsque les enregistrements que vous souhaitez modifier se trouvent dans plusieurs tables.

Vous pouvez modifier plusieurs champs simultanément. L’exemple suivant augmente les valeurs Order Amount de 10 % et les valeurs Freight de 3 % pour les expéditeurs au Royaume-Uni :

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- L’instruction UPDATE ne génère pas de jeu de résultats. En outre, une fois que vous mettez à jour les enregistrements à l’aide d’une requête Mise à jour, vous ne pouvez pas annuler l’opération. Pour savoir quels enregistrements ont été mis à jour, examinez d’abord les résultats d’une requête Sélection qui utilise les mêmes critères, puis exécutez la requête Mise à jour.
- Conservez toujours les copies de sauvegarde de vos données. Si vous mettez à jour les mauvais enregistrements, vous pouvez les récupérer à partir de vos copies de sauvegarde.



## <a name="example"></a>Exemple

Cet exemple modifie les valeurs dans le champ ReportsTo sur 5 pour tous les enregistrements des employés qui ont actuellement des valeurs ReportsTo définies sur 2.

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
