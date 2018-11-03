---
title: Clause CONSTRAINT (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 26d2b4b6281dd762e95113d5ca022e7c0d136755
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937042"
---
# <a name="constraint-clause-microsoft-access-sql"></a>Clause CONSTRAINT (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Une contrainte est similaire à un index, bien qu'elle puisse être utilisée pour établir une relation avec une autre table.

Utilisez la clause CONSTRAINT dans les instructions [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) et [CREATE TABLE](create-table-statement-microsoft-access-sql.md) pour créer ou supprimer des contraintes. Il existe deux types de clauses CONSTRAINT : une permettant de créer une contrainte sur un seul champ et l'autre permettant de créer une contrainte sur plusieurs champs.

> [!NOTE]
> [!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge la clause CONSTRAINT, ni les instructions du langage de définition de données (DDL), avec des bases de données autres que Microsoft Access. Utilisez les méthodes DAO **créer** à la place.

## <a name="syntax"></a>Syntaxe

### <a name="single-field-constraint"></a>Contrainte sur un seul champ

CONSTRAINT *nom* {PRIMARY KEY | UNIQUE | NON NULL | REFERENCES *tableétrangère* \[(*champétranger1, champétranger2*)\] \[ON UPDATE CASCADE | La valeur NULL\] \[ON DELETE CASCADE | La valeur NULL\]}

### <a name="multiple-field-constraint"></a>Contrainte sur plusieurs champs

CONSTRAINT *nom* {PRIMARY KEY (*primaire1*\[, *primaire2* \[,... \]\]) | UNIQUE (*unique1*\[, *unique2* \[,... \]\]) | NON NULL (*nonnulle1*\[, *nonnulle2* \[,... \]\]) | CLÉ étrangère \[aucun INDEX\] (*réf1*\[, *réf2* \[,... \] \]) REFERENCES *tableétrangère* \[(*champétranger1* \[, *champétranger2* \[,... \] \])\] \[ON UPDATE CASCADE | La valeur NULL\] \[ON DELETE CASCADE | La valeur NULL\]}

La clause CONSTRAINT est composée des arguments suivants :

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
<td><p><em>name</em></p></td>
<td><p>Nom de la contrainte à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>primaire1</em>, <em>primaire2</em></p></td>
<td><p>Nom du ou des champs à désigner comme clé primaire.</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>Nom du ou des champs à désigner comme clé unique.</p></td>
</tr>
<tr class="even">
<td><p><em>nonnulle1, nonnulle2</em></p></td>
<td><p>Nom du ou des champs qui sont restreints à des valeurs non nulles.</p></td>
</tr>
<tr class="odd">
<td><p><em>réf1</em>, <em>réf2</em></p></td>
<td><p>Nom du ou des champs de clé étrangère qui font référence à des champs d'une autre table.</p></td>
</tr>
<tr class="even">
<td><p><em>tableétrangère </em></p></td>
<td><p>Nom de la table étrangère contenant les champs spécifiés par <em>champétranger</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>champétranger1</em>, <em>champétranger2</em></p></td>
<td><p>Nom du ou des champs de la <em>tableétrangère</em> spécifiés par <em>réf1</em> et <em>réf2</em>. Vous pouvez omettre cette clause si le champ référencé est la clé primaire de <em>tableétrangère</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Utilisez la syntaxe d'une contrainte sur un seul champ dans la clause de définition de champ d'une instruction ALTER TABLE ou CREATE TABLE immédiatement à la suite de la spécification du type de données du champ.

Utilisez la syntaxe d'une contrainte sur plusieurs champs quand vous employez le mot réservé CONSTRAINT en dehors d'une clause de définition de champ dans une instruction ALTER TABLE ou CREATE TABLE.

La clause CONSTRAINT vous permet de désigner un champ comme l'une des contraintes suivantes :

- Vous pouvez utiliser le mot réservé UNIQUE pour désigner un champ en tant que clé unique, ceci afin d'empêcher que ce champ ait la même dans deux enregistrements de la table. La contrainte que vous appliquez peut viser à rendre unique un champ ou une liste de champs. Si la contrainte appliquée sur plusieurs champs désigne ces derniers comme clé unique, les valeurs combinées de tous les champs dans l'index doivent être uniques, même un de ces champs a la même valeur dans au moins deux enregistrements.

- Vous pouvez utiliser les mots réservés PRIMARY KEY pour désigner un champ ou un ensemble de champs comme clé primaire. Toutes les valeurs dans la clé primaire doivent être uniques et non **Null**, en outre, il ne peut y avoir qu'une seule clé primaire par table.
    
  > [!NOTE]
  > [!REMARQUE] N'appliquez pas une contrainte PRIMARY KEY sur une table qui comporte déjà une clé primaire, car dans ce cas une erreur se produit.

- Vous pouvez utiliser les mots réservés FOREIGN KEY pour désigner un champ comme clé étrangère. Si la clé primaire de la table étrangère est constituée de plusieurs champs, vous devez utiliser une définition de contrainte sur plusieurs champs qui répertorie tous les champs de référence, le nom de la table étrangère et les noms des champs référencés dans la table étrangère dans le même ordre que celui des champs de référence.Si les champs référencés constituent la clé primaire de la table étrangère, vous n'avez pas besoin de les spécifier. Par défaut, le moteur de base de données traite les champs référencés comme s'ils constituaient la clé primaire de la table étrangère. Les contraintes de clé étrangère définissent des actions spécifiques à effectuer lorsque la valeur d'une clé primaire correspondante change :

- Vous pouvez spécifier les actions à effectuer sur la table étrangère en fonction de l'action correspondante effectuée sur une clé primaire dans la table sur laquelle la clause CONSTRAINT est définie. Par exemple, examinez la définition suivante de la table Customers :
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Examinez la définition suivante de la table Orders qui décrit une relation de clé étrangère référençant la clé primaire de la table Customers :
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Les deux clauses ON UPDATE CASCADE et ON DELETE CASCADE sont définies sur la clé étrangère. La clause ON UPDATE CASCADE indique que si l'identificateur d'un client (CustId) est modifié dans la table Customer, le nouvel identificateur sera répercuté dans la table Orders. Chaque commande contenant l'identificateur du client sera mise à jour avec le nouvel identificateur. La clause ON DELETE CASCADE indique que si un client est supprimé de la table Customer, toutes les lignes de la table Orders contenant l'identificateur de ce client seront également supprimées. Examinez cette autre définition de la table Orders qui utilise l'action SET NULL à la place de l'action CASCADE :
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  La clause ON UPDATE SET NULL indique que si l'identificateur d'un client (CustId) est modifié dans la table Customer, les valeurs de clé étrangère correspondantes dans la table Orders prendront automatiquement la valeur NULL. De même, la clause ON DELETE SET NULL indique que si un client est supprimé de la table Customer, toutes les clés étrangères correspondantes dans la table Orders prendront automatiquement la valeur NULL.

Pour empêcher la création automatique d'index de clés étrangères, le modificateur NO INDEX peut être utilisé. Cette forme de définition de clé étrangère doit être utilisée seulement lorsque les valeurs d'index produites sont fréquemment dupliquées. Dans ce cas, utiliser un index peut être moins efficace qu'effectuer simplement une analyse de la table. Créer ce type d'index, qui implique l'insertion et la suppression de lignes dans la table, nuit aux performances et ne présente aucun avantage.

## <a name="example"></a>Exemple

Cet exemple crée une nouvelle table appelée ThisTable qui comporte deux champs de texte.

```vb 
 Sub CreateTableX1()    
Dim dbs As Database 
 
    ' Modify this line to include the path to Northwind 
    ' on your computer. 
    Set dbs = OpenDatabase("Northwind.mdb") 
 
    ' Create a table with two text fields. 
    dbs.Execute "CREATE TABLE ThisTable " _ 
        & "(FirstName CHAR, LastName CHAR);" 
 
    dbs.Close 
 
End Sub
```

<br/>

Cet exemple crée une nouvelle table appelée MyTable avec deux champs de texte, un champ Date/Heure et un index unique composé de ces trois champs.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Cet exemple crée une nouvelle table avec deux champs de texte et un champ **Entier**. Le champ SSN correspond à la clé primaire.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

