---
title: UNION, opération (Microsoft Access SQL)
TOCTitle: UNION Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 63ff883f35dabbbd69e1bf144eb32016f303c7ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879108"
---
# <a name="union-operation-microsoft-access-sql"></a>UNION, opération (Microsoft Access SQL)


**S’applique à**: Access 2013, Office 2013

Crée une requête Union qui combine les résultats de deux requêtes ou tables indépendantes ou plus.

## <a name="syntax"></a>Syntaxe

\[TABLE\] *Requête1* UNION \[tous les\] \[TABLE\] *requête2* \[UNION \[tous les\] \[TABLE\] *requêten* \[ ... \]\]

L'opération UNION est composée des arguments suivants :

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
<td><p><em>requête1-n</em></p></td>
<td><p>Instruction SELECT, nom d'une requête enregistrée ou d'une table enregistrée, précédé du mot clé TABLE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Vous pouvez fusionner les résultats de deux ou plusieurs requêtes, tables ou instructions SELECT, dans n'importe quel ordre, en une unique opération UNION. L'exemple suivant fusionne une table existante New Accounts avec une instruction SELECT :

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

Par défaut, l'opération UNION ne renvoie aucun enregistrement en double mais vous pouvez ajouter le prédicat [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) pour obtenir de façon certaine que tous les enregistrements soient renvoyés. La requête s'exécutera plus rapidement par ailleurs.

Toutes les requêtes impliquées dans une opération UNION doivent interroger le même nombre de champs qui, cependant, peuvent avoir des tailles et des types de données différents

N'utilisez des alias que dans la première instruction SELECT ; ils seront ignorés dans toutes les autres. Dans la clause ORDER BY, faites référence aux champs par leurs noms tels qu'ils sont spécifiés dans la première instruction SELECT.


> [!NOTE]
> <UL>
> <LI>
> <P>Vous pouvez utiliser une clause <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> ou <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> dans chaque argument <EM>requête</EM> pour regrouper les données renvoyées.</P>
> <LI>
> <P>Vous pouvez utiliser une clause <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> à la fin du dernier argument <EM>requête</EM> pour afficher les données renvoyées selon un ordre déterminé.</P></LI></UL>



## <a name="example"></a>Exemple

Dans cet exemple, le nom et la ville de tous les fournisseurs et clients du Brésil sont extraits.

La procédure EnumFields (que vous pouvez trouver dans l'exemple d'instruction SELECT) est appelée dans cet exemple.

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
