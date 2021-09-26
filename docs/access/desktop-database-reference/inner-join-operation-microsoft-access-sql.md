---
title: INNER JOIN, opération (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
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
ms.localizationpriority: high
ms.openlocfilehash: 098e7e1616407c1927f32db6cbedbb07b6df1283
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568907"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>INNER JOIN, opération (Microsoft Access SQL)


**S’applique à** : Access 2013, Office 2013


Combine les enregistrements de deux tables chaque fois qu’un champ commun contient des valeurs correspondantes.

## <a name="syntax"></a>Syntaxe

FROM *table1* INNER JOIN *table2* ON *table1*.*champ1* *compopr table2*.*champ2*

L'opération INNER JOIN est composée des arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>Noms des champs joints. S'ils ne sont pas numériques, les champs doivent être du même type et contenir le même type de données, mais il ne doivent pas obligatoirement avoir le même nom.</p></td>
</tr>
<tr class="odd">
<td><p><em>oprcomp</em></p></td>
<td><p>Tout opérateur de comparaison relationnelles : &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; ou &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser une opération INNER JOIN dans n'importe quelle clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Il s'agit du type de jointure le plus courant. Les jointures internes combinent les enregistrements de deux tables lorsque des valeurs correspondent dans un champ commun aux deux tables.

Vous pouvez utiliser INNER JOIN avec les tables Departments et Employees pour sélectionner tous les employés dans chaque service. En revanche, pour sélectionner tous les services (même si aucun employé n'est affecté à certains services) ou tous les employés (même si certains d'entre eux ne sont pas affectés à un service), vous pouvez utiliser une opération [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) afin de créer une jointure externe.

Si vous essayez de joindre des champs contenant des données de type Mémo ou Objet OLE, une erreur se produit.

Vous pouvez joindre deux champs numériques quelconques de types similaires. Par exemple, vous pouvez opérer une jointure sur des champs NuméroAuto et Long parce qu’ils sont de types similaires. En revanche, vous ne pouvez pas joindre des types de champs Simple et Double.

L’exemple suivant montre comment joindre les tables Categories (Catégories) et Products (Produits) sur le champ CategoryID :

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Dans l’exemple précédent, CategoryID est le champ joint, mais il n’est pas inclus dans le résultat de la requête, car il n’est pas inclus dans l’instruction [SELECT](select-statement-microsoft-access-sql.md). Pour inclure le champ joint, incluez le nom du champ dans l’instruction SELECT ; dans ce cas, Categories.CategoryID.

Vous pouvez également lier plusieurs clauses ON dans une instruction JOIN, en utilisant la syntaxe suivante :

SELECT *champs* FROM *table1* INNER JOIN *table2* ON *table1*.*champ1* *compopr* *table2*.*champ1* AND ON *table1*.*champ2* *compopr* *table2*.*champ2* OR *table1*.*champ3* *compopr* *table2*.*champ3*;

Vous pouvez également imbriquer des instructions JOIN en utilisant la syntaxe suivante :

SELECT *champ* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*champ3* *compopr* *tablex*.*champx*)\] ON *table2*.*champ2* *compopr* *table3*.*champ3*) ON *table1*.*champ1* *compopr* *table2*.*champ2*;

Une jointure gauche (LEFT JOIN) ou droite (RIGHT JOIN) peut être imbriquée dans une jointure interne, mais une jointure interne ne peut pas être imbriquée dans une jointure gauche ou droite.

## <a name="example"></a>Exemple

Dans cet exemple, deux jointures équivalentes sont créées : une entre les tables Order Details et Orders et une autre entre les tables Orders et Employees. Ceci est nécessaire, car la table Employees ne contient pas de données de ventes et la table Order Details ne contient pas de données relatives aux employés. La requête produit une liste des employés avec le montant total de leurs ventes.

Cet exemple appelle la procédure EnumFields, que vous trouverez dans l’exemple d’instruction SELECT.

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
