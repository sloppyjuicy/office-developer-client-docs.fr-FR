---
title: Opérations LEFT JOIN, RIGHT JOIN (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.localizationpriority: high
ms.openlocfilehash: a00095f540455a234f4fc2fa5250d399ce183c53
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632783"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>Opérations LEFT JOIN, RIGHT JOIN (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Combine les enregistrements source-table lorsqu’ils sont utilisés dans une clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).

## <a name="syntax"></a>Syntaxe

FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.champ1* *compopr table2.champ2*

Les opérations LEFT JOIN et RIGHT JOIN sont composées des arguments suivants :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Partie</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table1</em>, <em>table2</em></p></td>
<td><p>Nom des tables dont les enregistrements sont combinés.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Noms des champs joints. Les champs doivent être du même type et doivent contenir le même type de données, mais il ne doivent pas obligatoirement avoir le même nom.</p></td>
</tr>
<tr class="odd">
<td><p><em>oprcomp</em></p></td>
<td><p>Tout opérateur de comparaison relationnelles : &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; ou &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez une opération LEFT JOIN pour créer une jointure externe gauche. Les jointures externes gauche comprennent tous les enregistrements de la première des deux tables (la table de gauche), même si aucune valeur de cette table ne correspond aux enregistrements dans la seconde table (la table de droite).

Utilisez une opération RIGHT JOIN pour créer une jointure externe droite. Les jointures externes droite comprennent tous les enregistrements de la seconde table (la table de droite), même si aucune valeur de cette table ne correspond aux enregistrements dans la première table (la table de gauche).

Par exemple, vous pouvez utiliser une jointure gauche avec les tables Departments (à gauche) et Employees (à droite) pour sélectionner tous les départements, y compris ceux auxquels aucun employé n’est assigné. Pour sélectionner tous les employés, y compris ceux qui ne sont affectés à aucun département, vous devez utiliser une jointure droite.

L’exemple suivant montre comment joindre les tables Categories (Catégories) et Products (Produits) sur le champ CategoryID. La requête produit la liste de toutes les catégories, dont celles qui ne contiennent aucun produit :

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Dans cet exemple, CategoryID est le champ joint, mais il n’est pas inclus dans les résultats de la requête, car il n’est pas inclus dans l’instruction [SELECT](select-statement-microsoft-access-sql.md). Pour inclure le champ joint, entrez son nom de champ dans l’instruction SELECT, dans ce cas, Categories.CategoryID.

> [!NOTE]
> - Pour créer une requête qui n’indique que les enregistrements dans lesquels les données dans les champs joints sont identiques, utilisez une opération [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Une jointure gauche (LEFT JOIN) ou droite (RIGHT JOIN) peut être imbriquée dans une jointure interne, mais une jointure interne ne peut pas être imbriquée dans une jointure gauche ou droite. Voyez la discussion relative à l’imbrication dans la rubrique Jointure interne pour voir comment imbriquer des jointures dans d’autres jointures.
> - Vous pouvez lier plusieurs clauses ON. Voyez la discussion relative à la liaison de clause dans la rubrique Jointure interne pour voir comment procéder
> - Si vous essayez de joindre des champs contenant des données de type Mémo ou Objet OLE, une erreur se produit.

## <a name="example"></a>Exemple

Cet exemple :
- Dans cet exemple, les champs hypothétiques Department Name et Department ID sont censés exister dans une table Employees. Notez que ces champs n'existent pas dans la table Employees de la base de données Northwind.

- Sélectionne tous les services, y compris ceux sans employés.

- Appelle la procédure EnumFields, que vous trouverez dans l’exemple d’instruction SELECT.


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
