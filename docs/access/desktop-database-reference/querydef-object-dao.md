---
title: Objet QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301056"
---
# <a name="querydef-object-dao"></a>Objet QueryDef (DAO)

**S’applique à** : Access 2013 | Office 2013 

Un objet **QueryDef** est une définition stockée d’une requête dans une base de données du moteur de base de données Microsoft Access.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’objet **QueryDef** pour définir une requête. Par exemple, vous pouvez :

- Utiliser la propriété **SQL** pour définir ou renvoyer la définition de requête.

- Utiliser la collection **Parameters** de l’objet **QueryDef** pour définir ou renvoyer des paramètres de requête.

- Utiliser la propriété **Type** pour renvoyer une valeur indiquant si la requête sélectionne des enregistrements dans une table existante, crée une table, insère des enregistrements d’une table dans une autre table, supprime des enregistrements ou met à jour des enregistrements.

- Utiliser la propriété **MaxRecords** pour limiter le nombre d’enregistrements renvoyés par une requête.

- Utiliser la propriété **ODBCTimeout** pour indiquer la durée d’attente avant que la requête renvoie des enregistrements. La propriété **ODBCTimeout** s’applique aux requêtes qui accèdent aux données ODBC.

- Utiliser la propriété **ReturnsRecords** pour indiquer que la requête renvoie des enregistrements. La propriété **ReturnsRecords** est valable uniquement pour les requêtes SQL directes.

- Utiliser la propriété **Connect** pour créer une requête SQL directe vers une base de données ODC.

Vous pouvez également créer des objets **QueryDef** temporaires. Contrairement aux objets **QueryDef** permanents, les objets **QueryDef** temporaires ne sont pas enregistrés sur le disque ou ajoutés à la collection **QueryDefs**. Les objets **QueryDef** temporaires sont utiles pour les requêtes que vous devez exécuter de manière répétée au moment de l’exécution, mais qui n’ont pas besoin d’être enregistrées sur le disque, surtout si vous créez leurs instructions SQL pendant l’exécution.

Vous pouvez envisager un objet **QueryDef** permanent dans un espace de travail Microsoft Access comme une instruction SQL compilée. Si vous exécutez une requête à partir d’un objet **QueryDef** permanent, son exécution est plus rapide que si vous exécutiez l’instruction SQL équivalente à l’aide de la méthode **OpenRecordset**. En effet, le moteur de base de données Microsoft Access n’a pas besoin de compiler la requête avant de l’exécuter.

Pour utiliser le dialecte SQL natif d’un moteur de base de données externe accessible via le moteur de base de données Microsoft Access, il est recommandé d’utiliser des objets **QueryDef**. Par exemple, vous pouvez créer une requête Microsoft SQL Server et l’enregistrer dans un objet **QueryDef**. Lorsque vous devez utiliser une requête SQL d’un moteur de base de données non-Microsoft Access, vous devez fournir une chaîne de propriété **Connect** faisant référence à la source de données externe. Les requêtes contenant des propriétés **Connect** valables contournent le moteur de base de données Microsoft Access et transmettent directement la requête au serveur de base de données externe à des fins de traitement.

Pour créer un objet **QueryDef**, utilisez la méthode **CreateQueryDef**. Dans un espace de travail Microsoft Access, si vous fournissez une chaîne pour l’argument name ou si vous définissez explicitement la propriété **Name** du nouvel objet **QueryDef** sur une chaîne comportant au moins un caractère, vous créez un objet **QueryDef** permanent qui est automatiquement ajouté à la collection **QueryDefs** et enregistré sur le disque. La fourniture d’une chaîne nulle en tant qu’argument name ou la définition explicite de la propriété **Name** sur une chaîne nulle entraîne la création d’un objet **QueryDef** temporaire.

Pour faire référence à un objet **QueryDef** dans une collection selon son nombre ordinal ou son paramètre de propriété **Name**, utilisez l’une des formes de syntaxe suivantes :

QueryDefs(0)

QueryDefs("name")

QueryDefs\!\[ name\]

Vous ne pouvez faire référence aux objets **QueryDef** temporaires que selon les variables objet que vous leur avez attribuées.

**Lien fourni par** la communauté [UtterAccess](https://www.utteraccess.com). UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.

- [Requêtes : SQL vers Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

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

Cet exemple utilise la méthode **CreateQueryDef** pour créer et exécuter un objet **QueryDef** à la fois temporaire et permanent. La fonction GetrstTemp est nécessaire à l’exécution de cette procédure.

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

L’exemple suivant montre comment remplacer l’instruction SQL (Structured Query Language) dans une requête enregistrée.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

