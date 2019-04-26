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
localization_priority: Priority
ms.openlocfilehash: 356620376658bb927c690056f4de9a01554aa47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295645"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="37022-102">CONSTRAINT, clause (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="37022-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="37022-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37022-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37022-104">Une contrainte est similaire à un index, bien qu'elle puisse être utilisée pour établir une relation avec une autre table.</span><span class="sxs-lookup"><span data-stu-id="37022-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="37022-p101">Utilisez la clause CONSTRAINT dans les instructions [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) et [CREATE TABLE](create-table-statement-microsoft-access-sql.md) pour créer ou supprimer des contraintes. Il existe deux types de clauses CONSTRAINT : une permettant de créer une contrainte sur un seul champ et l'autre permettant de créer une contrainte sur plusieurs champs.</span><span class="sxs-lookup"><span data-stu-id="37022-p101">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints. There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>

> [!NOTE]
> <span data-ttu-id="37022-107">Le moteur de base de données Microsoft Access ne prend pas en charge la clause CONSTRAINT, ni les instructions du langage de définition de données (DDL), avec des bases de données autres que Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="37022-107">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="37022-108">Utilisez plutôt les méthodes **Create** de DAO.</span><span class="sxs-lookup"><span data-stu-id="37022-108">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="37022-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37022-109">Syntax</span></span>

### <a name="single-field-constraint"></a><span data-ttu-id="37022-110">Contrainte sur un seul champ</span><span class="sxs-lookup"><span data-stu-id="37022-110">Single-field constraint:</span></span>

<span data-ttu-id="37022-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span><span class="sxs-lookup"><span data-stu-id="37022-111">CONSTRAINT name {PRIMARY KEY | UNIQUE | NOT NULL |
    REFERENCES foreigntable [(foreignfield1, foreignfield2)]
    [ON UPDATE CASCADE | SET NULL]
    [ON DELETE CASCADE | SET NULL]}</span></span>

### <a name="multiple-field-constraint"></a><span data-ttu-id="37022-112">Contrainte sur plusieurs champs</span><span class="sxs-lookup"><span data-stu-id="37022-112">Multiple-field constraint:</span></span>

<span data-ttu-id="37022-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span><span class="sxs-lookup"><span data-stu-id="37022-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="37022-114">La clause CONSTRAINT comprend les deux parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="37022-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37022-115">Quitter</span><span class="sxs-lookup"><span data-stu-id="37022-115">Part</span></span></p></th>
<th><p><span data-ttu-id="37022-116">Description</span><span class="sxs-lookup"><span data-stu-id="37022-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37022-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="37022-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="37022-118">Nom de la contrainte à créer.</span><span class="sxs-lookup"><span data-stu-id="37022-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37022-119"><em>primary1</em>, <em>primary2</em></span><span class="sxs-lookup"><span data-stu-id="37022-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="37022-120">Nom du ou des champs à désigner comme clé primaire.</span><span class="sxs-lookup"><span data-stu-id="37022-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37022-121"><em>unique1</em>, <em>unique2</em></span><span class="sxs-lookup"><span data-stu-id="37022-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="37022-122">Nom du ou des champs à désigner en tant que clé unique.</span><span class="sxs-lookup"><span data-stu-id="37022-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37022-123"><em>notnull1, notnull2</em></span><span class="sxs-lookup"><span data-stu-id="37022-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="37022-124">Nom du ou des champs limités à des valeurs non Null.</span><span class="sxs-lookup"><span data-stu-id="37022-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37022-125"><em>ref1</em>, <em>ref2</em></span><span class="sxs-lookup"><span data-stu-id="37022-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="37022-126">Nom du ou des champs de clé étrangère qui font référence à des champs d'une autre table.</span><span class="sxs-lookup"><span data-stu-id="37022-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37022-127"><em>foreigntable</em></span><span class="sxs-lookup"><span data-stu-id="37022-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="37022-128">Nom de la table étrangère contenant les champs spécifiés par <em>champétranger</em>.</span><span class="sxs-lookup"><span data-stu-id="37022-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37022-129"><em>foreignfield1</em>, <em>foreignfield2</em></span><span class="sxs-lookup"><span data-stu-id="37022-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="37022-p103">Nom du ou des champs dans <em>foreigntable</em> spécifiés par <em>ref1</em>, <em>ref2</em>. Vous pouvez omettre cette clause si le champ référencé est la clé primaire de <em>foreigntable</em>.</span><span class="sxs-lookup"><span data-stu-id="37022-p103">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>. You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="37022-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="37022-132">Remarks</span></span>

<span data-ttu-id="37022-133">Vous utilisez la syntaxe pour une contrainte sur champ unique dans la clause de définition de champ d’une instruction ALTER TABLE ou CREATE TABLE qui suit immédiatement la spécification du type de données du champ.</span><span class="sxs-lookup"><span data-stu-id="37022-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="37022-134">Utilisez la syntaxe d'une contrainte sur plusieurs champs quand vous employez le mot réservé CONSTRAINT en dehors d'une clause de définition de champ dans une instruction ALTER TABLE ou CREATE TABLE.</span><span class="sxs-lookup"><span data-stu-id="37022-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="37022-135">La clause CONSTRAINT vous permet de désigner un champ comme l’un des types suivants de contraintes :</span><span class="sxs-lookup"><span data-stu-id="37022-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="37022-p104">Vous pouvez utiliser le mot réservé UNIQUE pour désigner un champ en tant que clé unique. Cela signifie que deux enregistrements dans la table peuvent avoir la même valeur dans ce champ. Vous pouvez contraindre tout champ ou toute liste de champs comme uniques. Si une contrainte sur plusieurs champs est désignée comme clé unique, les valeurs combinées de tous les champs dans l’index doivent être uniques, même si deux enregistrements ou plus ont la même valeur dans un seul des champs.</span><span class="sxs-lookup"><span data-stu-id="37022-p104">You can use the UNIQUE reserved word to designate a field as a unique key. This means that no two records in the table can have the same value in this field. You can constrain any field or list of fields as unique. If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="37022-p105">Vous pouvez utiliser les mots réservés PRIMARY KEY pour désigner un champ ou un ensemble de champs dans une table en tant que clé primaire. Toutes les valeurs dans la clé primaire devant être uniques et non **Null**, il ne peut y avoir qu’une seule clé primaire pour une table.</span><span class="sxs-lookup"><span data-stu-id="37022-p105">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key. All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="37022-142">Ne définissez pas une contrainte PRIMARY KEY sur une table possédant déjà une clé primaire. Si vous le faites, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="37022-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="37022-p106">Vous pouvez utiliser les mots réservés FOREIGN KEY pour désigner un champ comme clé étrangère. Si la clé primaire de la table étrangère est constituée de plusieurs champs, vous devez utiliser une définition de contrainte sur plusieurs champs qui répertorie tous les champs de référence, le nom de la table étrangère et les noms des champs référencés dans la table étrangère dans le même ordre que celui des champs de référence.Si les champs référencés constituent la clé primaire de la table étrangère, vous n'avez pas besoin de les spécifier. Par défaut, le moteur de base de données traite les champs référencés comme s'ils constituaient la clé primaire de la table étrangère. Les contraintes de clé étrangère définissent des actions spécifiques à effectuer lorsque la valeur d'une clé primaire correspondante change :</span><span class="sxs-lookup"><span data-stu-id="37022-p106">You can use the FOREIGN KEY reserved words to designate a field as a foreign key. If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed. If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields. By default the database engine behaves as if the foreign table's primary key is the referenced fields. Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="37022-p107">Vous pouvez spécifier des actions à effectuer sur la table étrangère en fonction d’une action correspondante appliquée à une clé primaire dans la table sur laquelle la clause CONSTRAINT est définie. Par exemple, envisagez la définition suivante pour la table Customers (Clients) :</span><span class="sxs-lookup"><span data-stu-id="37022-p107">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined. For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="37022-150">Envisagez la définition suivante de la table Orders (Commandes), qui définit une relation de clé étrangère référençant la clé primaire de la table Customers (Clients) :</span><span class="sxs-lookup"><span data-stu-id="37022-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="37022-p108">Les deux clauses ON UPDATE CASCADE et ON DELETE CASCADE sont définies sur la clé étrangère. La clause ON UPDATE CASCADE indique que si l'identificateur d'un client (CustId) est modifié dans la table Customer, le nouvel identificateur sera répercuté dans la table Orders. Chaque commande contenant l'identificateur du client sera mise à jour avec le nouvel identificateur. La clause ON DELETE CASCADE indique que si un client est supprimé de la table Customer, toutes les lignes de la table Orders contenant l'identificateur de ce client seront également supprimées. Examinez cette autre définition de la table Orders qui utilise l'action SET NULL à la place de l'action CASCADE :</span><span class="sxs-lookup"><span data-stu-id="37022-p108">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key. The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table. Each order containing a corresponding customer identifier value will be updated automatically with the new value. The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted. Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="37022-p109">La clause ON UPDATE SET NULL signifie que, si l’ID d’un client (CustId) est mis à jour dans la table Customers (Clients), les valeurs de clé étrangère correspondantes dans la table Orders (Commandes) sont automatiquement définies sur NULL. De même, la clause ON DELETE SET NULL signifie que, si un client est supprimé de la table Customers (Clients), toutes les clés étrangères correspondantes dans la table Orders (Commandes) sont automatiquement définies sur NULL.</span><span class="sxs-lookup"><span data-stu-id="37022-p109">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL. Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="37022-p110">Pour empêcher la création automatique d’index pour des clés étrangères, vous pouvez utiliser le modificateur NO INDEX. N’utilisez cette forme de définition de clé étrangère que dans les cas où les valeurs d’index obtenues seraient fréquemment dupliquées. Quand les valeurs d’un index de clé étrangère sont fréquemment dupliquées, l’utilisation d’un index peut être moins efficace qu’une simple analyse de table. La tenue à jour de ce type d’index, avec des lignes insérées et supprimées dans la table, a pour effet de dégrader les performances et n’offre aucun avantage.</span><span class="sxs-lookup"><span data-stu-id="37022-p110">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used. This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated. Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan. Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="37022-162">Exemple</span><span class="sxs-lookup"><span data-stu-id="37022-162">Example</span></span>

<span data-ttu-id="37022-163">Cet exemple crée une nouvelle table appelée ThisTable qui comporte deux champs de texte.</span><span class="sxs-lookup"><span data-stu-id="37022-163">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="37022-164">Cet exemple crée une nouvelle table appelée MyTable avec deux champs de texte, un champ Date/Heure et un index unique composé de ces trois champs.</span><span class="sxs-lookup"><span data-stu-id="37022-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="37022-p111">Cet exemple crée une nouvelle table avec deux champs de texte et un champ **Entier**. Le champ SSN correspond à la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="37022-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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

