---
title: SELECT, instruction (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 2b03834914c352a0e9c462c50bee48ac992276e3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860580"
---
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="d638f-102">SELECT, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="d638f-102">SELECT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="d638f-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d638f-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="d638f-104">Demande au moteur de base de données Microsoft Access de renvoyer des informations depuis la base de données sous la forme d'un jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d638f-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="d638f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d638f-105">Syntax</span></span>

<span data-ttu-id="d638f-106">Sélectionnez \[ *prédicat* \] { \*  |  *table*.\*  |  \[ *table*. \] *champ1* \[AS *alias1* \] \[, \[ *table*. \] *field2* \[AS *alias2* \] \[,... \] \]} FROM *expressiontable* \[,... \] \[IN *basededonnéesexterne* \] \[où...</span><span class="sxs-lookup"><span data-stu-id="d638f-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="d638f-107">\]\[De groupe à...</span><span class="sxs-lookup"><span data-stu-id="d638f-107">\] \[GROUP BY…</span></span> <span data-ttu-id="d638f-108">\]\[HAVING …</span><span class="sxs-lookup"><span data-stu-id="d638f-108">\] \[HAVING…</span></span> <span data-ttu-id="d638f-109">\]\[ORDER BY …</span><span class="sxs-lookup"><span data-stu-id="d638f-109">\] \[ORDER BY…</span></span> <span data-ttu-id="d638f-110">\]\[Avec OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="d638f-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="d638f-111">L'instruction SELECT est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d638f-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d638f-112">Élément</span><span class="sxs-lookup"><span data-stu-id="d638f-112">Part</span></span></p></th>
<th><p><span data-ttu-id="d638f-113">Description</span><span class="sxs-lookup"><span data-stu-id="d638f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d638f-114"><em>prédicat</em></span><span class="sxs-lookup"><span data-stu-id="d638f-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="d638f-p102">Un des prédicats suivants : <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW ou TOP</a>. Les prédicats permettent de limiter le nombre d'enregistrements renvoyés. Si aucun n'est précisé, ALL est choisi par défaut.  </span><span class="sxs-lookup"><span data-stu-id="d638f-p102">One of the following predicates: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a>. You use the predicate to restrict the number of records returned. If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="d638f-118">Indique que tous les champs de la ou des tables spécifiées sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d638f-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d638f-119"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="d638f-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="d638f-120">Nom de la table contenant les champs dans lesquels les enregistrements sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d638f-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d638f-121"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="d638f-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="d638f-p103">Noms des champs contenant les données à extraire. Si vous incluez plusieurs champs, les données seront extraites dans l'ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="d638f-p103">The names of the fields containing the data you want to retrieve. If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d638f-124"><em>alias1</em>, <em>alias2</em></span><span class="sxs-lookup"><span data-stu-id="d638f-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="d638f-125">Noms à utiliser comme en-têtes de colonne à la place des noms de colonnes d'origine d'une <em>table</em>.</span><span class="sxs-lookup"><span data-stu-id="d638f-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d638f-126"><em>expressiontable</em></span><span class="sxs-lookup"><span data-stu-id="d638f-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="d638f-127">Nom de la ou des tables contenant les données à extraire</span><span class="sxs-lookup"><span data-stu-id="d638f-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d638f-128"><em>basededonnéesexterne</em></span><span class="sxs-lookup"><span data-stu-id="d638f-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="d638f-129">Nom de la base de données contenant les tables dans <em>expressiontable</em> si elles ne sont pas dans la base de données en cours.</span><span class="sxs-lookup"><span data-stu-id="d638f-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d638f-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="d638f-130">Remarks</span></span>

<span data-ttu-id="d638f-131">Pour effectuer cette opération, le moteur de base de données Microsoft Jet recherche l’ou les tables spécifiées, extrait les colonnes choisies, sélectionne les lignes qui correspondent aux critères, trie et/ou regroupe les lignes dans l’ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="d638f-131">To perform this operation, the Microsoft Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="d638f-132">Les instructions SELECT ne modifient pas les données dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="d638f-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="d638f-p104">SELECT constitue généralement le premier mot d'une instruction SQL. Les instructions SQL sont pour la plupart des instructions SELECT ou [SELECT…INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="d638f-p104">SELECT is usually the first word in an SQL statement. Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="d638f-135">La syntaxe minimale d'une instruction SELECT est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d638f-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="d638f-136">SELECT *champs* FROM *table*</span><span class="sxs-lookup"><span data-stu-id="d638f-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="d638f-p105">Vous pouvez utiliser un astérisque (\*) pour sélectionner tous les champs d'une table. Dans l'exemple suivant, tous les champs de la table Employees sont sélectionnés :</span><span class="sxs-lookup"><span data-stu-id="d638f-p105">You can use an asterisk (\*) to select all fields in a table. The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="d638f-p106">Si le nom d'un champ figure dans plusieurs tables stipulées par la clause FROM, faites-le précéder du nom de la table correspondante et de l'opérateur **.** (point). Dans l'exemple suivant, le champ Department se trouve à la fois dans les tables Employees et Supervisors. L'instruction SQL sélectionne les départements dans la table Employees et les noms des superviseurs dans la table Supervisors :</span><span class="sxs-lookup"><span data-stu-id="d638f-p106">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.** (dot) operator. In the following example, the Department field is in both the Employees table and the Supervisors table. The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="d638f-p107">Lorsqu'un objet **Recordset** est créé, le moteur de base de données Microsoft Jet utilise le nom de champ de la table comme nom de l'objet **Field** dans l'objet **Recordset**. Si vous souhaitez utiliser un autre nom de champ ou un nom qui n'est pas concerné par l'expression utilisée pour générer le champ, utilisez le mot réservé AS. L'exemple suivant utilise le titre Birth comme nom pour l'objet **Field** renvoyé dans l'objet **Recordset** résultant :</span><span class="sxs-lookup"><span data-stu-id="d638f-p107">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="d638f-p108">Chaque fois que vous utilisez des fonctions d'agrégation ou des requêtes qui renvoient des noms d'objet **Field** ambigus ou en double, vous devez utiliser la clause AS pour fournir un nom de remplacement à l'objet **Field**. Dans l'exemple suivant, le titre Effectif est utilisé comme nom pour l'objet **Field** renvoyé dans l'objet **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="d638f-p108">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object. The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="d638f-p109">Vous pouvez utiliser les autres clauses d'une instruction SELECT pour limiter et organiser plus encore les données renvoyées. Pour plus d'informations, consultez la rubrique d'aide relative à la clause que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="d638f-p109">You can use the other clauses in a SELECT statement to further restrict and organize your returned data. For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="d638f-150">**Liens fournis par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="d638f-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="d638f-151">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d638f-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="d638f-152">Formateur SQL vers VBA</span><span class="sxs-lookup"><span data-stu-id="d638f-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="d638f-153">Affichage des enregistrements dans une plage définie</span><span class="sxs-lookup"><span data-stu-id="d638f-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="d638f-154">Exemple</span><span class="sxs-lookup"><span data-stu-id="d638f-154">Example</span></span>

<span data-ttu-id="d638f-p111">Dans cet exemple, le champ hypothétique Salary est censé exister dans la table Employees. Notez que ce champ n'existe pas dans la table Employees de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="d638f-p111">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table. Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="d638f-p112">Dans cet exemple, un objet **Recordset** de type feuille dynamique basé sur une instruction SQL est créé. Cet objet sélectionne les champs LastName et FirstName de tous les enregistrements de la table Employees. La procédure EnumFields, qui imprime le contenu de l'objet **Recordset** dans la fenêtre **Débogage**, est appelée.</span><span class="sxs-lookup"><span data-stu-id="d638f-p112">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="d638f-159">Dans cet exemple, le nombre d'enregistrements comportant une entrée dans le champ PostalCode est calculé et le champ renvoyé est nommé Tally.</span><span class="sxs-lookup"><span data-stu-id="d638f-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="d638f-160">Dans cet exemple, le nombre d'employés est indiqué ainsi que les salaires maximal et moyen.</span><span class="sxs-lookup"><span data-stu-id="d638f-160">This example shows the number of employees and the average and maximum salaries.</span></span>

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="d638f-p113">§LSA La procédure **Sub** EnumFields bénéficie d'un objet **Recordset** à partir de la procédure appelante. La procédure met en forme et imprime les champs de l'objet **Recordset** dans la fenêtre **Débogage**. La variable est la largeur de champ imprimé voulue. Certains champs peuvent être tronqués.</span><span class="sxs-lookup"><span data-stu-id="d638f-p113">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure. The procedure then formats and prints the fields of the **Recordset** to the **Debug** window. The variable is the desired printed field width. Some fields may be truncated.</span></span>

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




