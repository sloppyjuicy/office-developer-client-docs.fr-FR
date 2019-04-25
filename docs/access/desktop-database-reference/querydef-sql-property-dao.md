---
title: QueryDef.SQL, propriété (DAO)
TOCTitle: SQL property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c51f0da8541cf0ba2790827c58a0b017bd6ed875
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300979"
---
# <a name="querydefsql-property-dao"></a><span data-ttu-id="97672-102">QueryDef.SQL, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="97672-102">QueryDef.SQL Property (DAO)</span></span>

<span data-ttu-id="97672-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97672-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97672-104">Définit ou renvoie l’instruction SQL qui définit la requête exécutée par un objet **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="97672-104">Sets or returns the SQL statement that defines the query executed by a **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97672-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97672-105">Syntax</span></span>

<span data-ttu-id="97672-106">*expression* .SQL</span><span class="sxs-lookup"><span data-stu-id="97672-106">expression  . SQL</span></span>

<span data-ttu-id="97672-107">*expression* Variable représentant un objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="97672-107">*expression*  A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="97672-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="97672-108">Remarks</span></span>

<span data-ttu-id="97672-p101">Le **SQL** propriété contient l’instruction SQL qui détermine la manière dont les enregistrements sont sélectionnés, regroupées et triées lorsque vous exécutez la requête. Vous pouvez utiliser la requête pour sélectionner des enregistrements à inclure dans un \*\* [jeu d’enregistrements](recordset-object-dao.md) \*\* objet. Vous pouvez également définir des requêtes action pour modifier les données sans renvoi d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="97672-p101">The **SQL** property contains the SQL statement that determines how records are selected, grouped, and ordered when you execute the query. You can use the query to select records to include in a **[Recordset](recordset-object-dao.md)** object. You can also define action queries to modify data without returning records.</span></span>

<span data-ttu-id="97672-p102">La syntaxe SQL utilisée dans une requête doit respecter le langage SQL du moteur de requête est déterminé par le type d’espace de travail. Dans un espace de travail Microsoft Access, utilisez le langage SQL Microsoft Access, sauf si vous créez une requête SQL directe, auquel cas, vous devez utiliser le langage du serveur.</span><span class="sxs-lookup"><span data-stu-id="97672-p102">The SQL syntax used in a query must conform to the SQL dialect of the query engine, which is determined by the type of workspace. In a Microsoft Access workspace, use the Microsoft Access SQL dialect, unless you create an SQL pass-through query, in which case you should use the dialect of the server.</span></span>

<span data-ttu-id="97672-p103">Si l’instruction SQL inclut des paramètres pour la requête, vous devez définir ces avant l’exécution. Jusqu'à ce que vous réinitialisez les paramètres, les mêmes valeurs de paramètre sont appliqués à chaque fois que vous exécutez la requête.</span><span class="sxs-lookup"><span data-stu-id="97672-p103">If the SQL statement includes parameters for the query, you must set these before execution. Until you reset the parameters, the same parameter values are applied each time you execute the query.</span></span>

<span data-ttu-id="97672-116">Dans un espace de travail Microsoft Access, à l’aide un **QueryDef** objet est la meilleure méthode pour effectuer des opérations directes SQL sur sources de données ODBC connectées moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="97672-116">In a Microsoft Access workspace, using a **QueryDef** object is the preferred way to perform SQL pass-through operations on Microsoft Access database engine-connected ODBC data sources.</span></span> <span data-ttu-id="97672-117">En définissant une source de données ODBC pour la propriété **[Connect](querydef-connect-property-dao.md)** d’un objet **QueryDef**, vous pouvez utilisez un langage SQL non Microsoft Access dans la requête à transmettre au serveur externe.</span><span class="sxs-lookup"><span data-stu-id="97672-117">By setting the **QueryDef** object's **[Connect](querydef-connect-property-dao.md)** property to an ODBC data source, you can use non-Microsoft-Access-database SQL in the query to be passed to the external server.</span></span> <span data-ttu-id="97672-118">Par exemple, vous pouvez utiliser des instructions TRANSACT SQL (avec Microsoft SQL Server ou Sybase SQL Server bases de données), le moteur de base de données Microsoft Access serait sinon Évitez de traiter.</span><span class="sxs-lookup"><span data-stu-id="97672-118">For example, you can use TRANSACT SQL statements (with Microsoft SQL Server or Sybase SQL Server databases), which the Microsoft Access database engine would otherwise not process.</span></span>

> [!NOTE]
> <span data-ttu-id="97672-119">Si vous affectez à la propriété une chaîne concaténée avec une valeur non entière et que les paramètres système spécifient un caractère décimal américain tel que la virgule (par exemple, `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`), une erreur est générée lorsque vous tentez d’exécuter l’objet **QueryDef** dans une base de données du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="97672-119">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example,  `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`, and  ), an error will result when you try to execute the **QueryDef** object in a Microsoft Access database engine database.</span></span> <span data-ttu-id="97672-120">Il s’agit, car lors de la concaténation, le nombre est converti en une chaîne à l’aide du caractère décimal par défaut de votre système et Microsoft Access SQL accepte uniquement des caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="97672-120">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="97672-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="97672-121">Example</span></span>

<span data-ttu-id="97672-p106">Cet exemple illustre la **SQL** propriété en définissant et en modifiant le **SQL** propriété d’un fichier temporaire **QueryDef** et comparer les résultats. La fonction SQLOutput est requise pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="97672-p106">This example demonstrates the **SQL** property by setting and changing the **SQL** property of a temporary **QueryDef** and comparing the results. The SQLOutput function is required for this procedure to run.</span></span>

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="97672-p107">Cet exemple utilise la **CopyQueryDef** méthode pour créer une copie d’un **QueryDef** à partir d’un existant **jeu d’enregistrements** et modifie la copie en ajoutant une clause à la \*\* SQL\*\* propriété. Lorsque vous créez un permanente **QueryDef**, espaces, des points-virgules ou des sauts de ligne pourraient être ajoutés à la **SQL** propriété ; ces caractères supplémentaires doivent être supprimés avant des nouvelles clauses pouvant joint à l’instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="97672-p107">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the **SQL** property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the **SQL** property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="97672-126">Cet exemple montre une utilisation possible de CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="97672-126">This example shows a possible use of CopyQueryNew().</span></span> 
     
```vb
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="97672-p108">Cet exemple utilise les méthodes **CreateQueryDef** et **OpenRecordset**, ainsi que la propriété **SQL**, pour exécuter une requête sur la table de titres de la base de données exemple Microsoft SQL Server, Pubs, et renvoyer le titre et l’identificateur du titre du best-seller. Ensuite, il exécute une requête sur la table des auteurs et indique à l’utilisateur d’envoyer un chèque de bonification à chaque auteur en fonction de son pourcentage de droits d’auteur (la bonification totale s’élève à 1 000 euros et chaque auteur doit recevoir un pourcentage de ce montant).</span><span class="sxs-lookup"><span data-stu-id="97672-p108">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb
    Sub ClientServerX2() 
     
       Dim dbsCurrent As Database 
       Dim qdfBestSellers As QueryDef 
       Dim qdfBonusEarners As QueryDef 
       Dim rstTopSeller As Recordset 
       Dim rstBonusRecipients As Recordset 
       Dim strAuthorList As String 
     
       ' Open a database from which QueryDef objects can be  
       ' created. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a temporary QueryDef object to retrieve 
       ' data from a Microsoft SQL Server database. 
       Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
       With qdfBestSellers 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT title, title_id FROM titles " & _ 
             "ORDER BY ytd_sales DESC" 
          Set rstTopSeller = .OpenRecordset() 
          rstTopSeller.MoveFirst 
       End With 
     
       ' Create a temporary QueryDef to retrieve data from 
       ' a Microsoft SQL Server database based on the results from 
       ' the first query. 
       Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
       With qdfBonusEarners 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT * FROM titleauthor " & _ 
             "WHERE title_id = '" & _ 
             rstTopSeller!title_id & "'" 
          Set rstBonusRecipients = .OpenRecordset() 
       End With 
     
       ' Build the output string. 
       With rstBonusRecipients 
          Do While Not .EOF 
             strAuthorList = strAuthorList & "  " & _ 
                !au_id & ":  $" & (10 * !royaltyper) & vbCr 
             .MoveNext 
          Loop 
       End With 
     
       ' Display results. 
       MsgBox "Please send a check to the following " & _ 
          "authors in the amounts shown:" & vbCr & _ 
          strAuthorList & "for outstanding sales of " & _ 
          rstTopSeller!Title & "." 
     
       rstTopSeller.Close 
       dbsCurrent.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="97672-129">L’exemple suivant montre comment créer une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="97672-129">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="97672-130">Une requête nommée **myQuery** est créée avec deux paramètres nommés Param1 et Param2.</span><span class="sxs-lookup"><span data-stu-id="97672-130">A query named myQuery is created with two parameters, named  Param1 and  Param2.</span></span> <span data-ttu-id="97672-131">Pour ce faire, la propriété SQL de la requête est définie sur une instruction SQL qui définit les paramètres.</span><span class="sxs-lookup"><span data-stu-id="97672-131">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="97672-132">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="97672-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="97672-133">L’exemple suivant montre comment remplacer l’instruction SQL dans une requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="97672-133">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

```vb
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
    Dim strSELECT As String, strWhere As String
    Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
    Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
    strGROUPBY, strHAVING)
    
    ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
    & strGROUPBY &""& strHAVING &""& strOrderBy
    
    Exit_Procedure:
      Exit Function
    
    Error_Handler:
      MsgBox (Err.Number & ": " & Err.Description)
      Resume Exit_Procedure
    
    End Function
```
