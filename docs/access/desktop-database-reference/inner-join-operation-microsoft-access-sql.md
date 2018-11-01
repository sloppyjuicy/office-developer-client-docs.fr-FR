---
title: INNER JOIN, opération (Microsoft Access SQL)
TOCTitle: INNER JOIN Operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 874f685a1db38c4a381f08289cb0c612e7e2eb4c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888894"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>INNER JOIN, opération (Microsoft Access SQL)


**S’applique à**: Access 2013, Office 2013


Combine les enregistrements de deux tables lorsque des valeurs correspondent dans un champ commun.

## <a name="syntax"></a>Syntaxe

FROM *table1* INNER JOIN *table2* sur la *table1*. *champ1* *OpérateurComparaison table2*. *Field2*

L'opération INNER JOIN est composée des arguments suivants :

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
<td><p>Noms des champs joints. S'ils ne sont pas numériques, les champs doivent être du même type et contenir le même type de données, mais il ne doivent pas obligatoirement avoir le même nom.</p></td>
</tr>
<tr class="odd">
<td><p><em>opérateurcomparaison</em></p></td>
<td><p>Tout opérateur de comparaison relationnel : &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=&quot; ou &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Vous pouvez utiliser une opération INNER JOIN dans n'importe quelle clause [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)). Il s'agit du type de jointure le plus courant. Les jointures internes combinent les enregistrements de deux tables lorsque des valeurs correspondent dans un champ commun aux deux tables.

Vous pouvez utiliser INNER JOIN avec les tables Departments et Employees pour sélectionner tous les employés dans chaque service. En revanche, pour sélectionner tous les services (même si aucun employé n'est affecté à certains services) ou tous les employés (même si certains d'entre eux ne sont pas affectés à un service), vous pouvez utiliser une opération [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) afin de créer une jointure externe.

Si vous essayez de joindre des champs contenant des données de type Mémo ou Objet OLE, une erreur se produit.

Vous pouvez joindre deux champs numériques de types identiques. Par exemple, vous pouvez joindre un champ AutoNumber à un champ Long, car ils sont de même type. En revanche, vous ne pouvez pas joindre des champs de type Single et Double.

L'exemple suivant montre comment vous pouvez joindre les tables Categories et Products sur le champ CategoryID :

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Dans l'exemple précédent, CategoryID est le champ joint, mais il n'est pas inclus dans le résultat de la requête, car il n'est pas inclus dans l'instruction [SELECT](select-statement-microsoft-access-sql.md). Pour inclure le champ joint, incluez le nom du champ dans l’instruction SELECT — dans SELECT.

Vous pouvez également lier plusieurs clauses ON dans une instruction JOIN, pour cela utilisez la syntaxe suivante :

Sélectionnez les *champs* FROM *table1* INNER JOIN *table2* ON *table1*. *champ1* *OpérateurComparaison* *table2*. *champ1* ET sur la *table1*. *Field2* *OpérateurComparaison* *table2*. *field2*) OU sur la *table1*. *argument champ3* *OpérateurComparaison* *table2*. *l’argument champ3*) \];

Vous pouvez également imbriquer des instructions JOIN à l'aide de la syntaxe suivante :

Sélectionnez les *champs* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \] *table3* \[INNER JOIN \[( \] *tablex* \[INNER JOIN …) \] Sur *table3*. *argument champ3* *OpérateurComparaison* *tablex*. *fieldx*) \] Sur la *table2*. *Field2* *OpérateurComparaison* *table3*. *l’argument champ3*) SUR la *table1*. *champ1* *OpérateurComparaison* *table2*. *field2*;

Une jointure LEFT JOIN ou RIGHT JOIN peut être imbriquée dans une jointure INNER JOIN, mais une jointure INNER JOIN ne peut pas être imbriquée dans une jointure LEFT JOIN ou RIGHT JOIN.

## <a name="example"></a>Exemple

Dans cet exemple, deux jointures équivalentes sont créées : une entre les tables Order Details et Orders et une autre entre les tables Orders et Employees. Ceci est nécessaire, car la table Employees ne contient pas de données de ventes et la table Order Details ne contient pas de données relatives aux employés. La requête produit une liste des employés avec le montant total de leurs ventes.

La procédure EnumFields (que vous pouvez trouver dans l'exemple d'instruction SELECT) est appelée dans cet exemple.

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
