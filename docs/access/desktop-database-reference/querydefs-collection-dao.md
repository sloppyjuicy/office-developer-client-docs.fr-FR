---
title: Collection QueryDefs (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 740b128ce246c108f283489f8e2e172c12eb868c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568606"
---
# <a name="querydefs-collection-dao"></a>Collection QueryDefs (DAO)

**S’applique à** : Access 2013, Office 2013 

Une collection **QueryDefs** contient tous les objets **QueryDef** d’un objet **Database** dans une base de données de moteur de base de données Microsoft Access.

## <a name="remarks"></a>Remarques

Pour créer un nouvel objet **QueryDef**, utilisez la méthode **CreateQueryDef**. Dans un espace de travail Microsoft Access, si vous fournissez une chaîne pour l'argument de nom ou si vous définissez explicitement la propriété **Name** du nouvel objet **QueryDef** sur une chaîne comportant au moins un caractère, vous créez un objet **QueryDef** permanent qui est automatiquement ajouté à la collection **QueryDefs** et enregistré sur le disque. La fourniture d'une chaîne nulle en tant qu'argument de nom ou la définition explicite de la propriété **Name** sur une chaîne nulle entraîne la création d'un objet **QueryDef** temporaire.

Pour faire référence à un objet **QueryDef** dans une collection selon son nombre ordinal ou son paramètre de propriété **Name**, utilisez l’une des formes de syntaxe suivantes :

**QueryDefs**(0)

**QueryDefs**("name")

**QueryDefs**\!\[name\]

Vous ne pouvez faire référence aux objets **QueryDef** temporaires que selon les variables objet que vous leur avez attribuées.

## <a name="example"></a>Exemple

Cet exemple crée un objet **QueryDef** et l’ajoute à la collection **QueryDefs** de l’objet de **Database** Northwind. Il énumère ensuite la collection **QueryDefs** et la collection **Properties** du nouvel objet **QueryDef**.

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

Cet exemple utilise la méthode **CreateQueryDef** pour créer et exécuter deux objets **QueryDef**, l'un temporaire et l'autre permanent. La fonction GetrstTemp est obligatoire pour l'exécution de cette procédure.

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

L'exemple suivant montre comment exécuter une requête avec paramètres. La collection Parameters est utilisée pour définir le paramètre Organization de la requête myActionQuery avant l'exécution de cette dernière.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

L’exemple suivant montre comment ouvrir un objet Recordset basé sur une requête avec paramètres.

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

