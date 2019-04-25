---
title: UNION, opération (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314699"
---
# <a name="union-operation-microsoft-access-sql"></a>UNION, opération (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

L’opération UNION dans Access crée une requête Union qui combine les résultats d’au moins deux requêtes ou tables indépendantes.

## <a name="syntax"></a>Syntaxe

\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ … \]\]

L’opération UNION comprend les parties suivantes :

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
<td><p><em>query1-n</em></p></td>
<td><p>Instruction SELECT, nom d’une requête stockée, ou nom d’une table stockée précédés du mot clé TABLE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez fusionner les résultats d’au moins deux requêtes, tables et instructions SELECT, dans n’importe quelle combinaison, en une seule opération UNION. L’exemple suivant fusionne une table existante nommée New Accounts (Nouveaux comptes) et une instruction SELECT :

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

Par défaut, aucun enregistrement en double n’est renvoyé lorsque vous utilisez une opération UNION. Toutefois, vous pouvez inclure le prédicat ALL pour vous assurer que tous les enregistrements soient renvoyés. Cela accélère également l’exécution de la requête.

Toutes les requêtes dans une opération UNION doivent demander le même nombre de champs. Toutefois, les champs ne doivent pas nécessairement avoir les même taille ou .

Utiliser des alias uniquement dans la première instruction SELECT, car ils sont ignorés dans les autres. Dans la clause ORDER BY, faites référence aux champs par la manière dont ils sont appelés dans la première instruction SELECT.

> [!NOTE]
> - Vous pouvez utiliser une clause GROUP BY ou HAVING dans chaque argument [requête](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) pour regrouper les données renvoyées.
> - Vous pouvez utiliser une clause ORDER BY à la fin du dernier argument [requête](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) pour afficher les données renvoyées dans un ordre spécifié.

## <a name="example"></a>Exemple

Cet exemple extrait les noms et les villes de tous les fournisseurs et clients au Brésil. Il appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
