---
title: Objet QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bad2f4795dad8e308af85d3cca4ca0f71d88d9c2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470020"
---
# <a name="querydef-object-dao"></a><span data-ttu-id="4eae1-102">Objet QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="4eae1-102">QueryDef Object (DAO)</span></span>

<span data-ttu-id="4eae1-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eae1-103">**Applies to:** Access 2013 | Office 2013</span></span> 

<span data-ttu-id="4eae1-104">Un objet **QueryDef** est une définition stockée d'une requête dans une base de données du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4eae1-104">A **QueryDef** object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eae1-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="4eae1-105">Remarks</span></span>

<span data-ttu-id="4eae1-p101">Vous pouvez utiliser l'objet **QueryDef** pour définir une requête. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="4eae1-p101">You can use the **QueryDef** object to define a query. For example, you can:</span></span>

- <span data-ttu-id="4eae1-108">Utiliser la propriété **SQL** pour définir ou renvoyer la définition de requête.</span><span class="sxs-lookup"><span data-stu-id="4eae1-108">Use the **SQL** property to set or return the query definition.</span></span>

- <span data-ttu-id="4eae1-109">Utiliser la collection **Parameters** de l'objet **QueryDef** pour définir ou renvoyer des paramètres de requête.</span><span class="sxs-lookup"><span data-stu-id="4eae1-109">Use the **QueryDef** object's **Parameters** collection to set or return query parameters.</span></span>

- <span data-ttu-id="4eae1-110">Utiliser la propriété **Type** pour renvoyer une valeur indiquant si la requête sélectionne des enregistrements dans une table existante, crée une table, insère des enregistrements d'une table dans une autre table, supprime des enregistrements ou met à jour des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4eae1-110">Use the **Type** property to return a value indicating whether the query selects records from an existing table, makes a new table, inserts records from one table into another table, deletes records, or updates records.</span></span>

- <span data-ttu-id="4eae1-111">Utiliser la propriété **MaxRecords** pour limiter le nombre d'enregistrements renvoyés par une requête.</span><span class="sxs-lookup"><span data-stu-id="4eae1-111">Use the **MaxRecords** property to limit the number of records returned from a query.</span></span>

- <span data-ttu-id="4eae1-p102">Utiliser la propriété **ODBCTimeout** pour indiquer la durée d'attente avant que la requête renvoie des enregistrements. La propriété **ODBCTimeout** s'applique aux requêtes qui accèdent aux données ODBC.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p102">Use the **ODBCTimeout** property to indicate how long to wait before the query returns records. The **ODBCTimeout** property applies to any query that accesses ODBC data.</span></span>

- <span data-ttu-id="4eae1-p103">Utiliser la propriété **ReturnsRecords** pour indiquer que la requête renvoie des enregistrements. La propriété **ReturnsRecords** est valable uniquement pour les requêtes SQL directes.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p103">Use the **ReturnsRecords** property to indicate that the query returns records. The **ReturnsRecords** property is only valid on SQL pass-through queries.</span></span>

- <span data-ttu-id="4eae1-116">Utiliser la propriété **Connect** pour créer une requête SQL directe vers une base de données ODC.</span><span class="sxs-lookup"><span data-stu-id="4eae1-116">Use the **Connect** property to make an SQL pass-through query to an ODC database.</span></span>

<span data-ttu-id="4eae1-p104">Vous pouvez également créer des objets **QueryDef** temporaires. Contrairement aux objets **QueryDef** permanents, les objets **QueryDef** temporaires ne sont pas enregistrés sur le disque ou ajoutés à la collection **QueryDefs**. Les objets **QueryDef** temporaires sont utiles pour les requêtes que vous devez exécuter de manière répétée au moment de l'exécution, mais qui n'ont pas besoin d'être enregistrées sur le disque, surtout si vous créez leurs instructions SQL pendant l'exécution.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p104">You can also create temporary **QueryDef** objects. Unlike permanent **QueryDef** objects, temporary **QueryDef** objects are not saved to disk or appended to the **QueryDefs** collection. Temporary **QueryDef** objects are useful for queries that you must run repeatedly during run time but do not not need to save to disk, particularly if you create their SQL statements during run time.</span></span>

<span data-ttu-id="4eae1-p105">Vous pouvez envisager un objet **QueryDef** permanent dans un espace de travail Microsoft Access comme une instruction SQL compilée. Si vous exécutez une requête à partir d'un objet **QueryDef** permanent, son exécution est plus rapide que si vous exécutiez l'instruction SQL équivalente à l'aide de la méthode **OpenRecordset**. En effet, le moteur de base de données Microsoft Access n'a pas besoin de compiler la requête avant de l'exécuter.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p105">You can think of a permanent **QueryDef** object in a Microsoft Access workspace as a compiled SQL statement. If you execute a query from a permanent **QueryDef** object, the query will run faster than if you run the equivalent SQL statement from the **OpenRecordset** method. This is because the Microsoft Access database engine doesn't need to compile the query before executing it.</span></span>

<span data-ttu-id="4eae1-p106">Pour utiliser le dialecte SQL natif d'un moteur de base de données externe accessible via le moteur de base de données Microsoft Access, il est recommandé d'utiliser des objets **QueryDef**. Par exemple, vous pouvez créer une requête Microsoft SQL Server et l'enregistrer dans un objet **QueryDef**. Lorsque vous devez utiliser une requête SQL d'un moteur de base de données non-Microsoft Access, vous devez fournir une chaîne de propriété **Connect** faisant référence à la source de données externe. Les requêtes contenant des propriétés **Connect** valables contournent le moteur de base de données Microsoft Access et transmettent directement la requête au serveur de base de données externe à des fins de traitement.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p106">The preferred way to use the native SQL dialect of an external database engine accessed through the Microsoft Access database engine is through **QueryDef** objects. For example, you can create a Microsoft SQL Server query and store it in a **QueryDef** object. When you need to use a non-Microsoft Access database engine SQL query, you must provide a **Connect** property string that points to the external data source. Queries with valid **Connect** properties bypass the Microsoft Access database engine and pass the query directly to the external database server for processing.</span></span>

<span data-ttu-id="4eae1-127">Pour créer un objet **QueryDef**, utilisez la méthode **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4eae1-127">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="4eae1-128">Dans un espace de travail Microsoft Access, si vous fournissez une chaîne pour l’argument nom ou si vous définissez explicitement la propriété **Name** du nouvel objet **QueryDef** sur une chaîne non nulle, vous allez créer une **QueryDef** permanent qui sera automatiquement ajouté à la collection **QueryDefs** et enregistré sur le disque.</span><span class="sxs-lookup"><span data-stu-id="4eae1-128">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="4eae1-129">Fournir une chaîne de longueur nulle en tant qu’argument nom ou définir explicitement la propriété **Name** sur une chaîne de longueur nulle entraînera un objet **QueryDef** temporaire.</span><span class="sxs-lookup"><span data-stu-id="4eae1-129">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="4eae1-130">Pour faire référence à un objet **QueryDef** dans une collection selon son nombre ordinal ou son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="4eae1-130">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="4eae1-131">QueryDefs(0)</span><span class="sxs-lookup"><span data-stu-id="4eae1-131">QueryDefs(0)</span></span>

<span data-ttu-id="4eae1-132">QueryDefs("name")</span><span class="sxs-lookup"><span data-stu-id="4eae1-132">QueryDefs("name")</span></span>

<span data-ttu-id="4eae1-133">QueryDefs\! \[ nom\]</span><span class="sxs-lookup"><span data-stu-id="4eae1-133">QueryDefs\!\[ name\]</span></span>

<span data-ttu-id="4eae1-134">Vous ne pouvez faire référence aux objets **QueryDef** temporaires que selon les variables objet que vous leur avez attribuées.</span><span class="sxs-lookup"><span data-stu-id="4eae1-134">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

<span data-ttu-id="4eae1-135">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="4eae1-135">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="4eae1-136">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4eae1-136">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="4eae1-137">Requêtes : documents SQL pour Word </span><span class="sxs-lookup"><span data-stu-id="4eae1-137">Queries: Document SQL to Word</span></span>](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a><span data-ttu-id="4eae1-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="4eae1-138">Example</span></span>

<span data-ttu-id="4eae1-p109">Cet exemple crée un objet **QueryDef** et l'ajoute à la collection **QueryDefs** de l'objet de **Database** Northwind. Il énumère ensuite la collection **QueryDefs** et la collection **Properties** du nouvel objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p109">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="4eae1-p110">Cet exemple utilise la méthode **CreateQueryDef** pour créer et exécuter deux objets **QueryDef** (un temporaire et un permanent). La fonction GetrstTemp est requise pour exécuter de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="4eae1-p110">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="4eae1-143">L'exemple suivant montre comment remplacer l'instruction de langage SQL (Structured Query Language) dans une requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="4eae1-143">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

<span data-ttu-id="4eae1-144">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4eae1-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    ‘To change the Where clause in a saved query  
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

