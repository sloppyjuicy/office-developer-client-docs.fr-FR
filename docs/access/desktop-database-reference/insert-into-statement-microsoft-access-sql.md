---
title: Instruction INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1635ff8ad43af45a62cd2223be853cefb5b6e999
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870799"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="bd8c8-102">Instruction INSERT INTO (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="bd8c8-102">INSERT INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="bd8c8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd8c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd8c8-p101">Ajoute un ou plusieurs enregistrements à une table. Cette opération est une requête Ajout.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p101">Adds a record or multiple records to a table. This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd8c8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd8c8-106">Syntax</span></span>

<span data-ttu-id="bd8c8-107">**Requête Ajout de plusieurs enregistrements**:</span><span class="sxs-lookup"><span data-stu-id="bd8c8-107">**Multiple-record append query**:</span></span>

<span data-ttu-id="bd8c8-108">INSERT INTO *cible* \[(*champ1*\[, *champ2*\[,... \] \])\] \[IN *basededonnéesexterne* \] sélectionnez \[ *source*. \] *champ1*\[, *champ2*\[,... \] FROM *expressiontable*</span><span class="sxs-lookup"><span data-stu-id="bd8c8-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

<span data-ttu-id="bd8c8-109">**Requête Ajout de seul enregistrement**:</span><span class="sxs-lookup"><span data-stu-id="bd8c8-109">**Single-record append query**:</span></span>

<span data-ttu-id="bd8c8-110">INSERT INTO *cible* \[(*champ1*\[, *champ2*\[,... \] \])\] Valeurs (*valeur1*\[, *valeur2*\[,... \])</span><span class="sxs-lookup"><span data-stu-id="bd8c8-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="bd8c8-111">L’instruction INSERT INTO comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bd8c8-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd8c8-112">Élément</span><span class="sxs-lookup"><span data-stu-id="bd8c8-112">Part</span></span></p></th>
<th><p><span data-ttu-id="bd8c8-113">Description</span><span class="sxs-lookup"><span data-stu-id="bd8c8-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd8c8-114"><em>cible</em></span><span class="sxs-lookup"><span data-stu-id="bd8c8-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="bd8c8-115">Nom de la table ou de la requête à laquelle ajouter les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd8c8-116"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="bd8c8-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="bd8c8-117">Noms des champs pour ajouter des données, si la suite de l’argument <em>cible</em> , ou les noms de champs pour obtenir des données à partir de, si la suite de l’argument <em>source</em> .</span><span class="sxs-lookup"><span data-stu-id="bd8c8-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd8c8-118"><em>basededonnéesexterne</em></span><span class="sxs-lookup"><span data-stu-id="bd8c8-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="bd8c8-p102">Chemin d'accès à une base de données externe. Pour une description du chemin d'accès, voir la clause <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </span><span class="sxs-lookup"><span data-stu-id="bd8c8-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd8c8-121"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="bd8c8-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="bd8c8-122">Nom de la table ou de la requête à partir de laquelle copier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd8c8-123"><em>expressiontable</em></span><span class="sxs-lookup"><span data-stu-id="bd8c8-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="bd8c8-p103">Nom des tables à partir desquelles les enregistrements sont insérés. Cet argument peut être un nom de table simple ou un composé issu d'une opération <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> ou <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a>, ou d'une requête enregistrée.  </span><span class="sxs-lookup"><span data-stu-id="bd8c8-p103">The name of the table or tables from which records are inserted. This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd8c8-126"><em>valeur1</em>, <em>valeur2</em></span><span class="sxs-lookup"><span data-stu-id="bd8c8-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="bd8c8-p104">Valeurs à insérer dans les champs spécifiques du nouvel enregistrement. Chaque valeur est insérée dans le champ qui correspond à la position de la valeur dans la liste : <em>valeur1</em> est insérée dans <em>champ1</em> du nouvel enregistrement, <em>valeur2</em> dans <em>champ2</em>, et ainsi de suite. Vous devez séparer les valeurs par une virgule et placer les champs de texte entre guillemets (' ').</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p104">The values to insert into the specific fields of the new record. Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on. You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bd8c8-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd8c8-130">Remarks</span></span>

<span data-ttu-id="bd8c8-p105">Vous pouvez utiliser l'instruction INSERT INTO pour ajouter un enregistrement unique à une table à l'aide de la syntaxe de requête Ajout d'enregistrement unique indiquée ci-dessus. Dans ce cas, votre code spécifie le nom et la valeur de chaque champ de l'enregistrement. Vous devez spécifier chacun des champs de l'enregistrement auxquels une valeur doit être attribuée, et la valeur de chaque champ. Si vous ne spécifiez pas tous les champs, la valeur par défaut ou une valeur **Null** est insérée dans les colonnes vides. Les enregistrements sont ajoutés à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p105">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above. In this case, your code specifies the name and value for each field of the record. You must specify each of the fields of the record that a value is to be assigned to and a value for that field. When you do not specify each field, the default value or **Null** is inserted for missing columns. Records are added to the end of the table.</span></span>

<span data-ttu-id="bd8c8-136">Vous pouvez également utiliser INSERT INTO pour ajouter un jeu d’enregistrements à partir d’une autre table ou requête à l’aide de la sélection...</span><span class="sxs-lookup"><span data-stu-id="bd8c8-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="bd8c8-137">FROM, clause, comme illustré à la syntaxe de requête Ajout de plusieurs enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="bd8c8-138">Dans ce cas, la clause SELECT spécifie les champs à ajouter à la table spécifiée *cible* .</span><span class="sxs-lookup"><span data-stu-id="bd8c8-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="bd8c8-139">La table *source* ou *cible* peut spécifier une table ou une requête.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="bd8c8-140">Si une requête est spécifiée, le moteur de base de données Microsoft Access ajoute des enregistrements à toutes les tables spécifiées par la requête.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="bd8c8-141">INSERT INTO est facultative mais lorsqu'elle est incluse, elle précède l'instruction [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="bd8c8-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="bd8c8-142">Si votre table de destination contient une clé primaire, assurez-vous que vous ajoutez des valeurs uniques et non **Null** dans les champs de clé primaire. Si ce n’est pas le cas, le moteur de base de données Microsoft Access n’ajoutera pas les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="bd8c8-p108">Si vous ajoutez des enregistrements à une table avec un champ NuméroAuto et que vous voulez renuméroter les enregistrements ajoutés, n'incluez pas le champ NuméroAuto dans votre requête. Incluez le champ NuméroAuto dans la requête si vous voulez conserver les valeurs d'origine du champ.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p108">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query. Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="bd8c8-145">Utilisez la clause IN pour ajouter des enregistrements à une table dans une autre base de données.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="bd8c8-146">Pour créer une table, utilisez l'instruction [SELECT... INTO](select-into-statement-microsoft-access-sql.md) au lieu de créer une requête Création de table.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="bd8c8-147">Pour savoir quels enregistrements seront ajoutés avant d'exécuter la requête Ajout, exécutez d'abord une requête sélectionnée qui utilise les mêmes critères de sélection, et observez les résultats.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="bd8c8-p109">Une requête Ajout copie des enregistrements à partir d'une ou plusieurs tables vers une autre. Les tables contenant les enregistrements que vous ajoutez ne sont pas concernées par la requête Ajout.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p109">An append query copies records from one or more tables to another. The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="bd8c8-p110">Au lieu d'ajouter des enregistrements existants à partir d'une autre table, vous pouvez spécifier la valeur de chaque champ dans un nouvel enregistrement unique à l'aide de la clause VALUES. Si vous omettez la liste de champs, la clause VALUES doit inclure une valeur pour chaque champ de la table. Sinon, l'opération INSERT échoue. Utilisez une instruction INSERT INTO supplémentaire avec une clause VALUES pour chaque enregistrement supplémentaire que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p110">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause. If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail. Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="bd8c8-153">**Liens fournis par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="bd8c8-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="bd8c8-154">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="bd8c8-155">Générer des numéros séquentiels pour les instructions INSERT/UPDATE</span><span class="sxs-lookup"><span data-stu-id="bd8c8-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="bd8c8-156">Formateur SQL vers VBA</span><span class="sxs-lookup"><span data-stu-id="bd8c8-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="bd8c8-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd8c8-157">Example</span></span>

<span data-ttu-id="bd8c8-p112">Cet exemple sélectionne tous les enregistrements dans une table New Customers hypothétique et les ajoute à la table Customers. Lorsque les colonnes individuelles ne sont pas désignées, les noms de colonne de la table SELECT doivent correspondre exactement à ceux de la table INSERT INTO.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-p112">This example selects all records in a hypothetical New Customers table and adds them to the Customers table. When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="bd8c8-160">Cet exemple crée un nouvel enregistrement dans la table Employees.</span><span class="sxs-lookup"><span data-stu-id="bd8c8-160">This example creates a new record in the Employees table.</span></span>

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

