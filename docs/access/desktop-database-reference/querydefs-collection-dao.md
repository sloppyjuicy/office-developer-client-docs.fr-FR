---
title: Collection QueryDefs (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93f089d2bc5302329b5f4e3a0c267055921534b8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927549"
---
# <a name="querydefs-collection-dao"></a><span data-ttu-id="eafbc-102">Collection QueryDefs (DAO)</span><span class="sxs-lookup"><span data-stu-id="eafbc-102">QueryDefs collection (DAO)</span></span>

<span data-ttu-id="eafbc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eafbc-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="eafbc-104">Une collection **QueryDefs** contient tous les objets **QueryDef** d'un objet **Database** dans une base de données de moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="eafbc-104">A **QueryDefs** collection contains all **QueryDef** objects of a **Database** object in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="eafbc-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="eafbc-105">Remarks</span></span>

<span data-ttu-id="eafbc-106">Pour créer un objet **QueryDef**, utilisez la méthode **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="eafbc-106">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="eafbc-107">Dans un espace de travail Microsoft Access, si vous fournissez une chaîne pour l’argument nom ou si vous définissez explicitement la propriété **Name** du nouvel objet **QueryDef** sur une chaîne non nulle, vous allez créer une **QueryDef** permanent qui sera automatiquement ajouté à la collection **QueryDefs** et enregistré sur le disque.</span><span class="sxs-lookup"><span data-stu-id="eafbc-107">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="eafbc-108">Fournir une chaîne de longueur nulle en tant qu’argument nom ou définir explicitement la propriété **Name** sur une chaîne de longueur nulle entraînera un objet **QueryDef** temporaire.</span><span class="sxs-lookup"><span data-stu-id="eafbc-108">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="eafbc-109">Pour faire référence à un objet **QueryDef** dans une collection selon son nombre ordinal ou son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="eafbc-109">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="eafbc-110">**QueryDefs** (0)</span><span class="sxs-lookup"><span data-stu-id="eafbc-110">**QueryDefs**(0)</span></span>

<span data-ttu-id="eafbc-111">**QueryDefs** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="eafbc-111">**QueryDefs**("name")</span></span>

<span data-ttu-id="eafbc-112">**QueryDefs**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="eafbc-112">**QueryDefs**\!\[name\]</span></span>

<span data-ttu-id="eafbc-113">Vous ne pouvez faire référence aux objets **QueryDef** temporaires que selon les variables objet que vous leur avez attribuées.</span><span class="sxs-lookup"><span data-stu-id="eafbc-113">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

## <a name="example"></a><span data-ttu-id="eafbc-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="eafbc-114">Example</span></span>

<span data-ttu-id="eafbc-p102">Cet exemple crée un objet **QueryDef** et l'ajoute à la collection **QueryDefs** de l'objet de **Database** Northwind. Il énumère ensuite la collection **QueryDefs** et la collection **Properties** du nouvel objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="eafbc-p102">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

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

<span data-ttu-id="eafbc-p103">Cet exemple utilise la méthode **CreateQueryDef** pour créer et exécuter deux objets **QueryDef**, l'un temporaire et l'autre permanent. La fonction GetrstTemp est obligatoire pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="eafbc-p103">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="eafbc-p104">L'exemple suivant montre comment exécuter une requête avec paramètres. La collection Parameters est utilisée pour définir le paramètre Organization de la requête myActionQuery avant l'exécution de cette dernière.</span><span class="sxs-lookup"><span data-stu-id="eafbc-p104">The following example shows how to execute a parameter query. The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="eafbc-121">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="eafbc-121">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="eafbc-122">L'exemple suivant montre comment ouvrir un objet Recordset basé sur une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="eafbc-122">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

