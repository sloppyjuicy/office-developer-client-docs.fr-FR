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
ms.localizationpriority: high
ms.openlocfilehash: 0a407c6b164f2558be46ab2804693121ba07a5c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593634"
---
# <a name="select-statement-microsoft-access-sql"></a>SELECT, instruction (Microsoft Access SQL)

**S’applique à :** Access 2013 | Office 2013

Demande au moteur de base de données Microsoft Access de renvoyer des informations depuis la base de données sous la forme d'un jeu d'enregistrements.

## <a name="syntax"></a>Syntaxe

SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE… \] \[GROUP BY… \] \[HAVING… \] \[ORDER BY… \] \[WITH OWNERACCESS OPTION\]

L'instruction SELECT est composée des arguments suivants :

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
<td><p><em>prédicat</em></p></td>
<td><p>Un des prédicats suivants : <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW ou TOP</a>. Les prédicats permettent de limiter le nombre d’enregistrements renvoyés. Si aucun n’est précisé, ALL est choisi par défaut.</p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>Indique que tous les champs de la ou des tables spécifiées sont sélectionnés.</p></td>
</tr>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Nom de la table contenant les champs dans lesquels les enregistrements sont sélectionnés.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Noms des champs contenant les données à extraire. Si vous incluez plusieurs champs, les données seront extraites dans l'ordre indiqué.</p></td>
</tr>
<tr class="odd">
<td><p><em>alias1</em>, <em>alias2</em></p></td>
<td><p>Noms à utiliser comme en-têtes de colonne à la place des noms de colonnes d'origine d'une <em>table</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>expressiontable</em></p></td>
<td><p>Nom de la ou des tables contenant les données à extraire</p></td>
</tr>
<tr class="odd">
<td><p><em>basededonnéesexterne</em></p></td>
<td><p>Nom de la base de données contenant les tables spécifiées par l'argument <em>expressiontable</em> si elles ne se trouvent pas dans la base de données actuelle.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Pour effectuer cette opération, le moteur de base de données Microsoft Jet recherche la ou les tables spécifiées, extrait les colonnes choisies, sélectionne les lignes qui correspondent aux critères, trie et/ou regroupe ces lignes dans l’ordre indiqué.

Les instructions SELECT ne modifient pas les données dans la base de données.

SELECT constitue généralement le premier mot d’une instruction SQL. Les instructions SQL sont pour la plupart des instructions SELECT ou [SELECT…INTO](select-into-statement-microsoft-access-sql.md).

La syntaxe minimale d'une instruction SELECT est la suivante :

SELECT *champs* FROM *table*

Vous pouvez utiliser un astérisque (*) pour sélectionner tous les champs d'une table. Dans l'exemple suivant, tous les champs de la table Employees sont sélectionnés :

```sql
SELECT * FROM Employees;
```

Si le nom d'un champ figure dans plusieurs tables stipulées par la clause FROM, faites-le précéder du nom de la table correspondante et de l'opérateur **.** (point). Dans l'exemple suivant, le champ Department se trouve à la fois dans les tables Employees et Supervisors. L'instruction SQL sélectionne les départements dans la table Employees et les noms des superviseurs dans la table Supervisors :

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

Lorsqu'un objet **Recordset** est créé, le moteur de base de données Microsoft Jet utilise le nom de champ de la table comme nom de l'objet **Field** dans l'objet **Recordset**. Si vous souhaitez utiliser un autre nom de champ ou un nom qui n'est pas concerné par l'expression utilisée pour générer le champ, utilisez le mot réservé AS. L'exemple suivant utilise le titre Birth comme nom pour l'objet **Field** renvoyé dans l'objet **Recordset** résultant :

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

Chaque fois que vous utilisez des fonctions d'agrégation ou des requêtes qui renvoient des noms d'objet **Field** ambigus ou en double, vous devez utiliser la clause AS pour fournir un nom de remplacement à l'objet **Field**. Dans l'exemple suivant, le titre Effectif est utilisé comme nom pour l'objet **Field** renvoyé dans l'objet **Recordset** :

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

Vous pouvez utiliser les autres clauses d'une instruction SELECT pour limiter et organiser plus encore les données renvoyées. Pour plus d'informations, consultez la rubrique d'aide relative à la clause que vous utilisez.

**Liens fournis par** la communauté [UtterAccess](https://www.utteraccess.com). UtterAccess est le forum d’aide et wiki de Microsoft Access de référence.

- [SQL au formateur VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Affichage des enregistrements dans une plage définie](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>Exemple

Dans cet exemple, le champ hypothétique Salary est censé exister dans la table Employees. Notez que ce champ n'existe pas dans la table Employees de la base de données Northwind.

Dans cet exemple, un objet **Recordset** de type feuille dynamique basé sur une instruction SQL est créé. Cet objet sélectionne les champs LastName et FirstName de tous les enregistrements de la table Employees. La procédure EnumFields, qui imprime le contenu de l'objet **Recordset** dans la fenêtre **Débogage**, est appelée.

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

Dans cet exemple, le nombre d'enregistrements comportant une entrée dans le champ PostalCode est calculé et le champ renvoyé est nommé Tally.

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

Dans cet exemple, le nombre d'employés est indiqué ainsi que les salaires maximal et moyen.

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

§LSA La procédure **Sub** EnumFields bénéficie d’un objet **Recordset** à partir de la procédure appelante. La procédure met en forme et imprime les champs de l’objet **Recordset** dans la fenêtre **Débogage**. La variable est la largeur de champ imprimé voulue. Certains champs peuvent être tronqués.

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




