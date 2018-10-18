---
title: Méthode Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15577750d7c6a2373178bce9fefff16fef512023
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602670"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="2fa98-102">Méthode Database.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="2fa98-102">Database.CreateQueryDef Method (DAO)</span></span>

<span data-ttu-id="2fa98-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fa98-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2fa98-104">Crée un objet **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="2fa98-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fa98-105">Syntax</span></span>

<span data-ttu-id="2fa98-106">*expression* . CreateQueryDef (***nom***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="2fa98-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="2fa98-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="2fa98-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2fa98-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fa98-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fa98-109">Name</span><span class="sxs-lookup"><span data-stu-id="2fa98-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2fa98-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="2fa98-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2fa98-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="2fa98-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2fa98-112">Description</span><span class="sxs-lookup"><span data-stu-id="2fa98-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fa98-113">Name</span><span class="sxs-lookup"><span data-stu-id="2fa98-113">Name</span></span></p></td>
<td><p><span data-ttu-id="2fa98-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2fa98-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="2fa98-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2fa98-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2fa98-116"><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="2fa98-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fa98-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="2fa98-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="2fa98-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2fa98-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="2fa98-119"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2fa98-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2fa98-p101"><strong>Variant</strong> (sous-type <strong>String</strong>) qui représente une instruction SQL définissant l’objet <strong>QueryDef</strong>. Si vous ne spécifiez pas cet argument, vous pouvez définir l’objet <strong>QueryDef</strong> en paramétrant sa propriété <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> avant ou après son ajout à une collection.</span><span class="sxs-lookup"><span data-stu-id="2fa98-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2fa98-122"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="2fa98-122"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="2fa98-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2fa98-123">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="2fa98-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2fa98-124">Return value</span></span>
>>>>>>> <span data-ttu-id="2fa98-125">master</span><span class="sxs-lookup"><span data-stu-id="2fa98-125">master</span></span>

<span data-ttu-id="2fa98-126">Objet QueryDef</span><span class="sxs-lookup"><span data-stu-id="2fa98-126">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa98-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="2fa98-127">Remarks</span></span>

<span data-ttu-id="2fa98-128">Dans un espace de travail Microsoft Access, si vous spécifiez autre chose qu'une chaîne de longueur nulle pour le nom lorsque vous créez un objet **QueryDef**, l'objet **QueryDef** résultant est automatiquement ajouté à la collection **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="2fa98-128">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="2fa98-129">Si l’objet spécifié par un nom est déjà membre de la collection **QueryDefs** , une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="2fa98-129">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="2fa98-130">Vous pouvez créer un **objet QueryDef** temporaire à l’aide d’une chaîne de longueur nulle pour l’argument nom lorsque vous exécutez la méthode **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2fa98-130">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="2fa98-131">Vous obtenez un résultat identique en affectant à la propriété **[Name](querydef-name-property-dao.md)** d'un nouvel objet **QueryDef** une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="2fa98-131">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="2fa98-132">Les objets **QueryDef** temporaires sont utiles si vous souhaitez utiliser à plusieurs reprises des instructions SQL dynamiques sans créer de nouveaux objets permanents dans la collection **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="2fa98-132">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="2fa98-133">Vous ne pouvez pas ajouter d'objet **QueryDef** temporaire à une collection car une chaîne nulle ne constitue pas un nom valide pour un objet **QueryDef** permanent.</span><span class="sxs-lookup"><span data-stu-id="2fa98-133">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="2fa98-134">Vous avez toujours la possibilité de définir les propriétés **Name** et **SQL** du nouvel objet **QueryDef** et ajouter par la suite l'objet **QueryDef** à la collection **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="2fa98-134">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="2fa98-135">Pour exécuter l'instruction SQL dans un objet **QueryDef**, utilisez la méthode **[Execute](querydef-execute-method-dao.md)** ou **[OpenRecordset](database-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="2fa98-135">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="2fa98-136">Le recours à un objet **QueryDef** est la méthode généralement utilisée pour exécuter des requêtes SQL directes avec des bases de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="2fa98-136">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="2fa98-137">Pour supprimer un objet **QueryDef** d'une collection **QueryDefs** dans une base de données de moteur de base de données Microsoft Access, appelez la méthode **[Delete](querydefs-delete-method-dao.md)** sur la collection.</span><span class="sxs-lookup"><span data-stu-id="2fa98-137">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="2fa98-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="2fa98-138">Example</span></span>

<span data-ttu-id="2fa98-p104">Cet exemple utilise la méthode **CreateQueryDef** pour créer et exécuter un objet **QueryDef** à la fois temporaire et permanent. La fonction GetrstTemp est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2fa98-p104">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="2fa98-p105">Cet exemple utilise les méthodes **CreateQueryDef** et **OpenRecordset** ainsi que la propriété **SQL** pour interroger la table de titres dans la base de données exemple Microsoft SQL Server, Pubs et renvoyer le titre et la référence du titre du best-seller. L'exemple interroge ensuite la table des auteurs et indique à l'utilisateur d'envoyer une prime à chaque auteur en fonction de son pourcentage de droits d'auteur (la prime totale s'élève à 1 000 euros et chaque auteur doit recevoir un pourcentage de ce montant).</span><span class="sxs-lookup"><span data-stu-id="2fa98-p105">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="2fa98-143">L'exemple suivant montre comment créer une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="2fa98-143">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="2fa98-144">Une requête nommée **myQuery** est créée avec deux paramètres, nommés Param1 et Param2.</span><span class="sxs-lookup"><span data-stu-id="2fa98-144">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="2fa98-145">Pour ce faire, la propriété SQL de la requête est définie sur une instruction SQL (Structured Query Language) qui définit les paramètres.</span><span class="sxs-lookup"><span data-stu-id="2fa98-145">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="2fa98-146">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2fa98-146">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
