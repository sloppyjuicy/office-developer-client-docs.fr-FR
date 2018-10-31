---
title: Instruction ALTER TABLE (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 83ba764fa23c972c93156d418bffcde6f3239145
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863694"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="c175f-102">Instruction ALTER TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c175f-102">ALTER TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c175f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c175f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c175f-104">Modifie la structure d'une table après qu'elle a été créée avec l'instruction [CREATE TABLE](create-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c175f-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="c175f-105">[!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge ALTER TABLE, ni les instructions du langage de définition de données (DDL), avec des bases de données autres que Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c175f-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="c175f-106">Utilisez les méthodes **Create DAO** à la place.</span><span class="sxs-lookup"><span data-stu-id="c175f-106">Use the **DAO Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="c175f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c175f-107">Syntax</span></span>

<span data-ttu-id="c175f-108">ALTER TABLE *table* {ajouter {de la colonne *type de champ*\[(*taille*)\] \[non NULL\] \[CONSTRAINT *index* \] | ALTER COLUMN *type de champ*\[(*taille*)\] | CONSTRAINT *index de plusieurs champs*} | DROP {COLUMN *champ* I CONSTRAINT *nom de l’index*}}</span><span class="sxs-lookup"><span data-stu-id="c175f-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="c175f-109">L'instruction ALTER TABLE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c175f-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c175f-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c175f-110">Part</span></span></p></th>
<th><p><span data-ttu-id="c175f-111">Description</span><span class="sxs-lookup"><span data-stu-id="c175f-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c175f-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="c175f-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-113">Nom de la table à modifier.</span><span class="sxs-lookup"><span data-stu-id="c175f-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c175f-114"><em>champ</em></span><span class="sxs-lookup"><span data-stu-id="c175f-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-p102">Nom du champ à ajouter ou à supprimer de la <em>table</em>. Ou, nom du champ à modifier dans la <em>table</em>.</span><span class="sxs-lookup"><span data-stu-id="c175f-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c175f-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="c175f-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-118">Type de données du <em>champ</em>.</span><span class="sxs-lookup"><span data-stu-id="c175f-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c175f-119"><em>taille</em></span><span class="sxs-lookup"><span data-stu-id="c175f-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-120">Taille du champ en nombre de caractères (champs texte et binaires seulement).</span><span class="sxs-lookup"><span data-stu-id="c175f-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c175f-121"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="c175f-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-122">Index du <em>champ</em>.</span><span class="sxs-lookup"><span data-stu-id="c175f-122">The index for <em>field</em>.</span></span> <span data-ttu-id="c175f-123">Pour plus d’informations sur la création de cet index, voir la <a href="constraint-clause-microsoft-access-sql.md">clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="c175f-123">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c175f-124"><em>index de plusieurs champs</em></span><span class="sxs-lookup"><span data-stu-id="c175f-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-125">La définition d’un index de plusieurs champs à ajouter au <em>tableau</em>.</span><span class="sxs-lookup"><span data-stu-id="c175f-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="c175f-126">Pour plus d’informations sur la création de cet index, voir la <a href="constraint-clause-microsoft-access-sql.md">clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="c175f-126">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c175f-127"><em>nom de l'index</em></span><span class="sxs-lookup"><span data-stu-id="c175f-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="c175f-128">Nom de l'index de plusieurs champs à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c175f-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c175f-129">Notes</span><span class="sxs-lookup"><span data-stu-id="c175f-129">Remarks</span></span>

<span data-ttu-id="c175f-130">À l’aide de l’instruction ALTER TABLE, vous pouvez modifier une table existante de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="c175f-130">By using the ALTER TABLE statement, you can alter an existing table in several ways.</span></span> <span data-ttu-id="c175f-131">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c175f-131">You can:</span></span>

- <span data-ttu-id="c175f-p106">Utilisez ADD COLUMN pour ajouter un champ à la table. Vous devez pour cela spécifier le nom du champ, le type des données et éventuellement la taille du champ (pour les champs texte et binaires). Par exemple, l'instruction suivante ajoute un champ texte de 25 caractères appelé Notes à la table Employees :</span><span class="sxs-lookup"><span data-stu-id="c175f-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="c175f-135">Vous pouvez également définir un index sur ce champ.</span><span class="sxs-lookup"><span data-stu-id="c175f-135">You can also define an index on that field.</span></span> <span data-ttu-id="c175f-136">Pour plus d’informations sur les index monochamp, voir la [clause CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c175f-136">For more information about single-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="c175f-137">Si vous spécifiez NOT NULL pour un champ, les nouveaux enregistrements sont requis pour contenir des données valides dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="c175f-137">If you specify NOT NULL for a field, new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="c175f-p108">Utilisez ALTER COLUMN pour changer le type des données d'un champ existant. Vous devez pour cela spécifier le nom du champ, le nouveau type des données et éventuellement la taille du champ (pour les champs texte et binaires). Par exemple, l'instruction suivante change le type des données d'un champ ZipCode de la table Employees en remplaçant l'entier qui s'y trouvait par du texte comportant 10 caractères :</span><span class="sxs-lookup"><span data-stu-id="c175f-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```
  
- <span data-ttu-id="c175f-141">Utilisez ADD CONSTRAINT pour ajouter un index de plusieurs champs.</span><span class="sxs-lookup"><span data-stu-id="c175f-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="c175f-142">Pour plus d’informations sur les index de plusieurs champs, voir la [clause CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c175f-142">For more information about multiple-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="c175f-p110">Utilisez DROP COLUMN pour supprimer un champ. Vous ne devez pour cela spécifier que le nom du champ.</span><span class="sxs-lookup"><span data-stu-id="c175f-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

- <span data-ttu-id="c175f-p111">Utilisez DROP CONSTRAINT pour supprimer un index de plusieurs champs. Vous ne devez pour cela spécifier que le nom de l'index suivant le mot réservé CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="c175f-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>

> [!NOTE] 
> - <span data-ttu-id="c175f-147">[!REMARQUE] Vous ne pouvez pas ajouter ou supprimer plus d'un champ ou d'un index à la fois.</span><span class="sxs-lookup"><span data-stu-id="c175f-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="c175f-148">Vous pouvez utiliser l’instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour ajouter un index d’un ou de plusieurs champs à une table et l’instruction ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) pour supprimer un index créé avec ALTER TABLE ou CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="c175f-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="c175f-p112">Vous pouvez utiliser NOT NULL sur un seul champ ou dans une clause CONSTRAINT nommée qui s'applique à un index d'un ou de plusieurs champs nommé CONSTRAINT. En revanche, vous ne pouvez appliquer la restriction NOT NULL à un champ qu'une seule fois. Si vous appliquez plusieurs fois cette restriction, une erreur d'exécution de produit. 
</span><span class="sxs-lookup"><span data-stu-id="c175f-p112">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="c175f-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="c175f-152">Example</span></span>

<span data-ttu-id="c175f-153">Dans cet exemple, un champ Salary avec le type de données **Money** est ajouté à la table Employees.</span><span class="sxs-lookup"><span data-stu-id="c175f-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="c175f-154">Dans cet exemple, le type de données **Money** du champ Salary est remplacé par **Char**.</span><span class="sxs-lookup"><span data-stu-id="c175f-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="c175f-155">Dans cet exemple, le champ Salary est supprimé de la table Employees.</span><span class="sxs-lookup"><span data-stu-id="c175f-155">This example removes the Salary field from the Employees table.</span></span>

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="c175f-p113">Dans cet exemple, une clé étrangère est ajoutée à la table Orders. La clé étrangère est basée sur le champ EmployeeID et fait référence au champ EmployeeID de la table Employees. Vous n'avez pas besoin d'indiquer le champ EmployeeID à la suite de la table Employees dans la clause REFERENCES, car EmployeeID est la clé primaire de la table Employees.</span><span class="sxs-lookup"><span data-stu-id="c175f-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="c175f-159">Dans cet exemple, la clé étrangère est supprimée de la table Orders.</span><span class="sxs-lookup"><span data-stu-id="c175f-159">This example removes the foreign key from the Orders table.</span></span>

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
