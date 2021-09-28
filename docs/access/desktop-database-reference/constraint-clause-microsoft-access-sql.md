---
title: CONSTRAINT, clause (Microsoft Access SQL)
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
ms.localizationpriority: high
ms.openlocfilehash: 590a83fef68680325cb9d0b039c996375751edc7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615738"
---
# <a name="constraint-clause-microsoft-access-sql"></a>CONSTRAINT, clause (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Une contrainte est similaire à un index, bien qu'elle puisse être utilisée pour établir une relation avec une autre table.

Utilisez la clause CONSTRAINT dans les instructions [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) et [CREATE TABLE](create-table-statement-microsoft-access-sql.md) pour créer ou supprimer des contraintes. Il existe deux types de clauses CONSTRAINT : une permettant de créer une contrainte sur un seul champ et l'autre permettant de créer une contrainte sur plusieurs champs.

> [!NOTE]
> Le moteur de base de données Microsoft Access ne prend pas en charge la clause CONSTRAINT, ni les instructions du langage de définition de données (DDL), avec des bases de données autres que Microsoft Access. Pour cela, utilisez les méthodes **Create** DAO.

## <a name="syntax"></a>Syntaxe

### <a name="single-field-constraint"></a>Contrainte sur un seul champ

CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

### <a name="multiple-field-constraint"></a>Contrainte sur plusieurs champs

CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

La clause CONSTRAINT comprend les deux parties suivantes :

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
<td><p><em>name</em></p></td>
<td><p>Nom de la contrainte à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>primary1</em>, <em>primary2</em></p></td>
<td><p>Nom du ou des champs à désigner comme clé primaire.</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>Nom du ou des champs à désigner en tant que clé unique.</p></td>
</tr>
<tr class="even">
<td><p><em>notnull1, notnull2</em></p></td>
<td><p>Nom du ou des champs limités à des valeurs non Null.</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>Nom du ou des champs de clé étrangère qui font référence à des champs d'une autre table.</p></td>
</tr>
<tr class="even">
<td><p><em>foreigntable</em></p></td>
<td><p>Nom de la table étrangère contenant les champs spécifiés par <em>champétranger</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>foreignfield1</em>, <em>foreignfield2</em></p></td>
<td><p>Nom du ou des champs dans <em>foreigntable</em> spécifiés par <em>ref1</em>, <em>ref2</em>. Vous pouvez omettre cette clause si le champ référencé est la clé primaire de <em>foreigntable</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous utilisez la syntaxe pour une contrainte sur champ unique dans la clause de définition de champ d’une instruction ALTER TABLE ou CREATE TABLE qui suit immédiatement la spécification du type de données du champ.

Utilisez la syntaxe d'une contrainte sur plusieurs champs quand vous employez le mot réservé CONSTRAINT en dehors d'une clause de définition de champ dans une instruction ALTER TABLE ou CREATE TABLE.

La clause CONSTRAINT vous permet de désigner un champ comme l’un des types suivants de contraintes :

- Vous pouvez utiliser le mot réservé UNIQUE pour désigner un champ en tant que clé unique. Cela signifie que deux enregistrements dans la table peuvent avoir la même valeur dans ce champ. Vous pouvez contraindre tout champ ou toute liste de champs comme uniques. Si une contrainte sur plusieurs champs est désignée comme clé unique, les valeurs combinées de tous les champs dans l’index doivent être uniques, même si deux enregistrements ou plus ont la même valeur dans un seul des champs.

- Vous pouvez utiliser les mots réservés PRIMARY KEY pour désigner un champ ou un ensemble de champs dans une table en tant que clé primaire. Toutes les valeurs dans la clé primaire devant être uniques et non **Null**, il ne peut y avoir qu’une seule clé primaire pour une table.
    
  > [!NOTE]
  > Ne définissez pas une contrainte PRIMARY KEY sur une table possédant déjà une clé primaire. Si vous le faites, une erreur se produit.

- Vous pouvez utiliser les mots réservés FOREIGN KEY pour désigner un champ comme clé étrangère. Si la clé primaire de la table étrangère est constituée de plusieurs champs, vous devez utiliser une définition de contrainte sur plusieurs champs qui répertorie tous les champs de référence, le nom de la table étrangère et les noms des champs référencés dans la table étrangère dans le même ordre que celui des champs de référence.Si les champs référencés constituent la clé primaire de la table étrangère, vous n'avez pas besoin de les spécifier. Par défaut, le moteur de base de données traite les champs référencés comme s'ils constituaient la clé primaire de la table étrangère. Les contraintes de clé étrangère définissent des actions spécifiques à effectuer lorsque la valeur d'une clé primaire correspondante change :

- Vous pouvez spécifier des actions à effectuer sur la table étrangère en fonction d’une action correspondante appliquée à une clé primaire dans la table sur laquelle la clause CONSTRAINT est définie. Par exemple, envisagez la définition suivante pour la table Customers (Clients) :
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Envisagez la définition suivante de la table Orders (Commandes), qui définit une relation de clé étrangère référençant la clé primaire de la table Customers (Clients) :
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Les deux clauses ON UPDATE CASCADE et ON DELETE CASCADE sont définies sur la clé étrangère. La clause ON UPDATE CASCADE indique que si l'identificateur d'un client (CustId) est modifié dans la table Customer, le nouvel identificateur sera répercuté dans la table Orders. Chaque commande contenant l'identificateur du client sera mise à jour avec le nouvel identificateur. La clause ON DELETE CASCADE indique que si un client est supprimé de la table Customer, toutes les lignes de la table Orders contenant l'identificateur de ce client seront également supprimées. Examinez cette autre définition de la table Orders qui utilise l'action SET NULL à la place de l'action CASCADE :
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  La clause ON UPDATE SET NULL signifie que, si l’ID d’un client (CustId) est mis à jour dans la table Customers (Clients), les valeurs de clé étrangère correspondantes dans la table Orders (Commandes) sont automatiquement définies sur NULL. De même, la clause ON DELETE SET NULL signifie que, si un client est supprimé de la table Customers (Clients), toutes les clés étrangères correspondantes dans la table Orders (Commandes) sont automatiquement définies sur NULL.

Pour empêcher la création automatique d’index pour des clés étrangères, vous pouvez utiliser le modificateur NO INDEX. N’utilisez cette forme de définition de clé étrangère que dans les cas où les valeurs d’index obtenues seraient fréquemment dupliquées. Quand les valeurs d’un index de clé étrangère sont fréquemment dupliquées, l’utilisation d’un index peut être moins efficace qu’une simple analyse de table. La tenue à jour de ce type d’index, avec des lignes insérées et supprimées dans la table, a pour effet de dégrader les performances et n’offre aucun avantage.

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

