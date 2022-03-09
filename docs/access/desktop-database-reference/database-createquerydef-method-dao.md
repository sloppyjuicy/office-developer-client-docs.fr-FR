---
title: Database.CreateQueryDef, méthode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 28f2b037d3e9698d1f19f37cfaa793a42162ea24
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465674"
---
# <a name="databasecreatequerydef-method-dao"></a>Database.CreateQueryDef, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* .CreateQueryDef(***Name** _, _*_SQLText_**)

*expression* Variable qui représente un objet **Database**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui représente une instruction SQL définissant l’objet <strong>QueryDef</strong>. Si vous ne spécifiez pas cet argument, vous pouvez définir l’objet <strong>QueryDef</strong> en paramétrant sa propriété <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> avant ou après son ajout à une collection.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

QueryDef

## <a name="remarks"></a>Remarques

Dans un espace de travail Microsoft Access, si vous spécifiez autre chose qu’une chaîne de longueur nulle pour le nom lorsque vous créez un objet **QueryDef**, l’objet **QueryDef** résultant est automatiquement ajouté à la collection **[QueryDefs](querydefs-collection-dao.md)**.

Si l’objet spécifié par l’argument name est déjà membre de la collection **QueryDefs**, une erreur d’exécution se produit. Vous pouvez créer un objet **QueryDef** temporaire en utilisant une chaîne nulle pour l’argument name lorsque vous exécutez la méthode **CreateQueryDef**. Vous obtenez un résultat identique en affectant à la propriété [**Name**](querydef-name-property-dao.md) d’un nouvel objet **QueryDef** une chaîne nulle (""). 

Les objets **QueryDef** temporaires sont utiles si vous souhaitez utiliser à plusieurs reprises des instructions SQL dynamiques sans créer de nouveaux objets permanents dans la collection **QueryDefs**. Vous ne pouvez pas ajouter d’objet **QueryDef** temporaire à une collection car une chaîne nulle ne constitue pas un nom valide pour un objet **QueryDef** permanent. Vous avez toujours la possibilité de définir les propriétés **Name** et **SQL** du nouvel objet **QueryDef** et ajouter par la suite l’objet **QueryDef** à la collection **QueryDefs**.

Pour exécuter l’instruction SQL dans un objet **QueryDef**, utilisez la méthode **[Execute](querydef-execute-method-dao.md)** ou **[OpenRecordset](database-openrecordset-method-dao.md)**.

Le recours à un objet **QueryDef** est la méthode généralement utilisée pour exécuter des requêtes SQL directes avec des bases de données ODBC.

Pour supprimer un objet **QueryDef** d’une collection **QueryDefs** dans une base de données de moteur de base de données Microsoft Access, appelez la méthode **[Delete](querydefs-delete-method-dao.md)** sur la collection.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **CreateQueryDef** pour créer et exécuter un objet **QueryDef** à la fois temporaire et permanent. La fonction GetrstTemp est nécessaire à l'exécution de cette procédure.

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


Cet exemple utilise les méthodes **CreateQueryDef** et **OpenRecordset**, ainsi que la propriété **SQL**, pour exécuter une requête sur la table de titres de la base de données exemple Microsoft SQL Server, Pubs, et renvoyer le titre et l’identificateur du titre du best-seller. Ensuite, il exécute une requête sur la table des auteurs et indique à l’utilisateur d’envoyer un chèque de bonification à chaque auteur en fonction de son pourcentage de droits d’auteur (la bonification totale s’élève à 1 000 euros et chaque auteur doit recevoir un pourcentage de ce montant).

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


L'exemple suivant montre comment créer une requête avec paramètres. Une requête nommée **myQuery** est créée avec deux paramètres, nommés  Param1 et  Param2. Pour ce faire, la propriété SQL de la requête est définie sur une instruction SQL (Structured Query Language) qui définit les paramètres.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
