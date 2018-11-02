---
title: LEFT JOIN, RIGHT JOIN, opérations (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: a16df1e26e4ab5617e6bf76aa93a11a936ccb49b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925897"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN, RIGHT JOIN, opérations (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Combine les enregistrements source-table lorsqu'ils sont utilisés dans une clause [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)).

## <a name="syntax"></a>Syntaxe

FROM *table1* \[ gauche | DROITE \] JOIN *table2* ON *Table1.champ1* *OpérateurComparaison Table2.champ2*

Les opérations LEFT JOIN et RIGHT JOIN sont composées des arguments suivants :

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
<td><p><em>table1</em>, <em>table2</em></p></td>
<td><p>Noms des tables à partir desquelles les enregistrements sont combinés.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Noms des champs joints. Les champs doivent être du même type et doivent contenir le même type de données, mais il ne doivent pas obligatoirement avoir le même nom.</p></td>
</tr>
<tr class="odd">
<td><p><em>opérateurcomparaison</em></p></td>
<td><p>Tout opérateur de comparaison relationnel : &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=&quot; ou &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Utilisez une opération LEFT JOIN pour créer une jointure externe gauche. Les jointures externes gauche comprennent tous les enregistrements de la première des deux tables (la table de gauche), même si aucune valeur de cette table ne correspond aux enregistrements dans la seconde table (la table de droite).

Utilisez une opération RIGHT JOIN pour créer une jointure externe droite. Les jointures externes droite comprennent tous les enregistrements de la seconde table (la table de droite), même si aucune valeur de cette table ne correspond aux enregistrements dans la première table (la table de gauche).

Vous pouvez par exemple utiliser LEFT JOIN avec les tables Departments (services) (gauche) et Employees (employés) (droite) pour sélectionner tous les services, y compris ceux auxquels aucun employé n'est assigné. Pour sélectionner tous les employés, y compris ceux qui ne sont pas assignés à un service, utilisez RIGHT JOIN.

L'exemple suivant montre comment vous pouvez joindre les tables Categories (catégories) et Products (produits) sur le champ CategoryID. La requête produit une liste de toutes les catégories, y compris celles qui ne contiennent aucun produit :

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Dans cet exemple, CategoryID est le champ joint, mais il n'est pas inclus dans les résultats de la requête, car il n'est pas inclus dans l'instruction [SELECT](select-statement-microsoft-access-sql.md). Pour inclure le champ joint, entrez le nom du champ dans l’instruction SELECT — dans SELECT.

> [!NOTE]
> - [!REMARQUE] Pour créer une requête qui n'indique que les enregistrements dans lesquels les données dans les champs joints sont identiques, utilisez une opération [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Une jointure LEFT JOIN ou RIGHT JOIN peut être imbriquée dans une jointure INNER JOIN, mais une jointure INNER JOIN ne peut pas être imbriquée dans une jointure LEFT JOIN ou RIGHT JOIN. Reportez-vous à la section concernant l'imbrication de jointures dans la rubrique INNER JOIN pour savoir comment imbriquer des jointures dans d'autres jointures.
> - Vous pouvez lier plusieurs clauses ON. Reportez-vous à la section concernant la liaison de clauses dans la rubrique INNER JOIN pour savoir comment procéder.
> - Si vous essayez de joindre des champs contenant des données de type Mémo ou Objet OLE, une erreur se produit.

## <a name="example"></a>Exemple

Cet exemple montre comment :
- Suppose l’existence de champs hypothétiques de nom du service et l’ID de service dans la table Employees. Notez que ces champs n'existent pas dans la table Employees de la base de données Northwind.

- Sélectionne tous les départements, y compris ceux sans employés.

- Appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.


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
