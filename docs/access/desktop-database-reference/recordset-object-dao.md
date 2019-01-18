---
title: Objet Recordset (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 19999159f7987be87031f88d1eec87980585f369
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699743"
---
# <a name="recordset-object-dao"></a>Objet Recordset (DAO)

**S’applique à**: Access 2013, Office 2013

Un objet **Recordset** représente les enregistrements dans une table de base ou les enregistrements obtenus par l'exécution d'une requête.

## <a name="remarks"></a>Remarques

Vous utilisez des objets **Recordset** pour manipuler des données dans une base de données au niveau enregistrement. Lorsque vous utilisez des objets DAO, vous manipulez les données presque exclusivement à l'aide d'objets **Recordset**. Tous les objets **Recordset** sont créés à l'aide d'enregistrements (lignes) et de champs (colonnes). Il existe cinq types d'objets **Recordset**:

- Recordset de type table : représentation en code d'une table de base que vous pouvez utiliser pour ajouter, modifier ou supprimer des enregistrements à partir d'une table de base de données unique (espaces de travail Microsoft Access uniquement).

- Recordset de type feuille de réponse dynamique : résultat d'une requête qui peut contenir des enregistrements pouvant être mis à jour. Un objet **Recordset** de type feuille de réponse dynamique est un jeu d'enregistrements dynamique que vous pouvez utiliser pour ajouter, modifier ou supprimer des enregistrements à partir d'une ou de plusieurs tables de base de données sous-jacentes. Un objet **Recordset** de type feuille de réponse dynamique peut contenir des champs provenant d'une ou plusieurs tables de base de données. Ce type correspond à un curseur de jeu de clés ODBC.

- Recordset de type capture instantanée : copie statique d'un jeu d'enregistrements que vous pouvez utiliser pour rechercher des données ou générer des rapports. Un objet **Recordset** de type capture instantanée peut contenir des champs provenant d'une ou de plusieurs tables de base de données, mais ne peut pas être mis à jour. Ce type correspond à un curseur ODBC statique.

- Recordset de type transfert uniquement : identique au type capture instantanée, sauf qu'aucun curseur n'est fourni. Vous pouvez uniquement faire défiler en avant les enregistrements. Cela améliore les performances lorsque vous devez uniquement effectuer un seul passage dans un jeu de résultats. Ce type correspond à un curseur ODBC de transfert uniquement.

- Recordset de type dynamique : un résultat de requête défini à partir d'une ou de plusieurs tables de base dans lequel vous pouvez ajouter, modifier ou supprimer des enregistrements à partir d'une requête de renvoi de ligne. En outre, les enregistrements que d'autres utilisateurs ajoutent, suppriment ou modifient dans les tables de base apparaissent également dans votre **Recordset**. Ce type correspond à un curseur ODBC dynamique (espaces de travail ODBCDirect uniquement).

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.

Vous pouvez choisir le type d’objet **Recordset** à créer à l’aide de l’argument type de la méthode **OpenRecordset** .

Dans un espace de travail Microsoft Access, si vous ne spécifiez pas un type, DAO tente de créer le type **d’objet Recordset** avec la plupart des fonctionnalités disponibles, en commençant par table. Si ce type n'est pas disponible, DAO tente de créer un objet **Recordset** de type de feuille de réponse dynamique, puis de type capture instantanée et enfin de type transfert uniquement.

Dans un espace de travail ODBCDirect, si vous ne spécifiez pas un type, DAO tente de créer le type **d’objet Recordset** avec la réponse de requête plus rapide, commençant par avant uniquement. Si ce type n'est pas disponible, DAO tente de créer un objet **Recordset** de type capture instantanée, puis de type feuille de réponse dynamique, et enfin de type dynamique.

Lors de la création d'un objet **Recordset** à l'aide d'un objet **[TableDef](tabledef-object-dao.md)** non lié dans un espace de travail Microsoft Access, les objets **Recordset** de type table sont créés. Seuls les objets **Recordset** de type feuille de réponse dynamique ou de type capture instantanée peuvent être créés avec des tables liées ou des tables de bases de données ODBC connectées au moteur de base de données Microsoft Access.

Un nouvel objet **Recordset** est automatiquement ajouté à la collection **Recordsets** lorsque vous ouvrez l'objet, et est automatiquement supprimé lorsque vous le fermez.

> [!NOTE]
> [!REMARQUE] Si vous utilisez des variables pour représenter un objet **Recordset** et l'objet **Database** qui contient cet objet **Recordset**, assurez-vous que les variables ont la même étendue ou durée de vie. Par exemple, si vous déclarez une variable publique représentant un objet **Recordset**, assurez-vous que la variable qui représente la **base de données** contenant le **Recordset** est également publique, ou qu'elle est déclarée dans une procédure **Sub** ou **Function** à l'aide du mot clé **statique**.

Vous pouvez créer autant de variables d'objet **Recordset** que nécessaire. Plusieurs objets **Recordset** peuvent accéder aux mêmes tables, requêtes et champs sans risque de conflit.

Feuille de réponse dynamique, instantané et objets **Recordset** de type avant uniquement sont stockés dans la mémoire locale. Si l'espace disponible dans la mémoire locale n'est pas suffisant pour stocker les données, le moteur de base de données Microsoft Access enregistre les données supplémentaires dans l'espace disque TEMP. Si cet espace est saturé, une erreur interceptable se produit.

La collection par défaut d'un objet **Recordset** est la collection **Fields**, et la propriété par défaut d'un objet **[Field](field-object-dao.md)** est la propriété **[Value](field-value-property-dao.md)**. Utilisez ces valeurs par défaut pour simplifier votre code.

Lorsque vous créez un objet **Recordset**, l'enregistrement actif est positionné sur le premier enregistrement s'il existe des enregistrements. S'il n'existe aucun enregistrement, le paramètre de propriété **RecordCount** est défini sur 0, et les propriétés **BOF** et **EOF** ont la valeur **True**.

Vous pouvez utiliser les méthodes **MoveNext**, **MovePrevious**, **MoveFirst** et **MoveLast** pour repositionner l’enregistrement actif. Les objets **Recordset** de type transfert uniquement ne prennent en charge que la méthode **MoveNext**. Lorsque vous utilisez les méthodes Move pour parcourir chaque enregistrement (ou vous « promener » dans le **Recordset**), vous pouvez utiliser les propriétés **BOF** et **EOF** pour vérifier le début et la fin de l’objet **Recordset**.

Avec des objets **Recordset** de type feuille de réponse dynamique et capture instantanée dans un espace de travail Microsoft Access, vous pouvez également utiliser les méthodes Find, comme **FindFirst**, pour localiser un enregistrement spécifique en fonction de certains critères. Si l'enregistrement est introuvable, la propriété **NoMatch** est définie sur **True**. Pour les objets **Recordset** de type table, vous pouvez analyser les enregistrements à l'aide de la méthode **Seek**.

La propriété **Type** indique le type d'objet **Recordset** créé, et la propriété **Updatable** indique si vous pouvez modifier les enregistrements de l'objet.

Les informations sur la structure d'une table de base, comme les noms et les types de données de chaque objet **Field** et des objets **Index**, sont stockées dans un objet **TableDef**.

Pour faire référence à un objet **Recordset** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

- **Recordsets**(0)

- **Jeux d’enregistrements** (« nom »)

- **Jeux d’enregistrements**\!\[nom\]

> [!NOTE]
> [!REMARQUE] Vous pouvez ouvrir plusieurs fois un objet **Recordset** à partir de la même source de données ou base de données en créant des noms en double dans la collection **Recordsets**. Vous devez attribuer des objets **Recordset** à des variables d'objet et y faire référence par nom de variable.

## <a name="example"></a>Exemple

L'exemple ci-dessous illustre les objets **Recordset** et la collection **Recordsets** en ouvrant quatre types d'objet **Recordsets** différents, en énumérant la collection Recordsets de l'objet **Database** actif et en énumérant la collection **Properties** de chaque objet **Recordset**.

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

Cet exemple utilise la méthode **OpenRecordset** pour ouvrir cinq objets **Recordset** différents et afficher leur contenu. La procédure OpenRecordsetOutput est obligatoire pour l'exécution de cette procédure.

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

Cet exemple ouvre un objet **Recordset** de type dynamique et énumère ses enregistrements.

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

Cet exemple ouvre un objet **Recordset** de type feuille de réponse dynamique et indique dans quelle mesure ses champs peuvent être mis à jour.

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple ouvre un objet **Recordset** de type transfert uniquement, illustre ses caractéristiques de lecture seule et avance pas à pas dans le **Recordset** avec la méthode **MoveNext**.

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

Cet exemple ouvre un objet **Recordset** de type capture instantanée et illustre ses caractéristiques de lecture seule.

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple ouvre un **Recordset** de type table, définit sa propriété **Index** et énumère ses enregistrements.

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

L'exemple suivant montre comment utiliser la méthode Seek pour rechercher un enregistrement dans une table liée.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

<br/>

L'exemple suivant montre comment ouvrir un objet Recordset basé sur une requête avec paramètres.

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

<br/>

L'exemple suivant montre comment ouvrir un Recordset basé sur une table ou une requête.

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

L'exemple suivant montre comment ouvrir un Recordset basé sur une instruction SQL (Structured Query Language).

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

L'exemple suivant montre comment utiliser les méthodes FindFirst et FindNext pour rechercher un enregistrement dans un Recordset.

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

L'exemple suivant montre comment copier les résultats d'une requête vers une feuille de calcul dans un nouveau classeur Microsoft Excel.

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

