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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284517"
---
# <a name="recordset-object-dao"></a><span data-ttu-id="c798a-102">Objet Recordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="c798a-102">Recordset Object (DAO)</span></span>

<span data-ttu-id="c798a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c798a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c798a-104">Un objet **Recordset** représente les enregistrements dans une table de base ou les enregistrements obtenus par l’exécution d’une requête.</span><span class="sxs-lookup"><span data-stu-id="c798a-104">A **Recordset** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="c798a-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c798a-105">Remarks</span></span>

<span data-ttu-id="c798a-p101">Vous utilisez des objets **Recordset** pour manipuler des données dans une base de données au niveau enregistrement. Lorsque vous utilisez des objets DAO, vous manipulez les données presque exclusivement à l’aide d’objets **Recordset**. Tous les objets **Recordset** sont créés à l’aide d’enregistrements (lignes) et de champs (colonnes). Il existe cinq types d’objets **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="c798a-p101">You use **Recordset** objects to manipulate data in a database at the record level. When you use DAO objects, you manipulate data almost entirely using **Recordset** objects. All **Recordset** objects are constructed using records (rows) and fields (columns). There are five types of **Recordset** objects:</span></span>

- <span data-ttu-id="c798a-110">Recordset de type table : représentation en code d'une table de base que vous pouvez utiliser pour ajouter, modifier ou supprimer des enregistrements à partir d'une table de base de données unique (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="c798a-110">Table-type Recordset— representation in code of a base table that you can use to add, change, or delete records from a single database table (Microsoft Access workspaces only).</span></span>

- <span data-ttu-id="c798a-p102">Recordset de type feuille de réponse dynamique : résultat d'une requête qui peut contenir des enregistrements pouvant être mis à jour. Un objet **Recordset** de type feuille de réponse dynamique est un jeu d'enregistrements dynamique que vous pouvez utiliser pour ajouter, modifier ou supprimer des enregistrements à partir d'une ou de plusieurs tables de base de données sous-jacentes. Un objet **Recordset** de type feuille de réponse dynamique peut contenir des champs provenant d'une ou plusieurs tables de base de données. Ce type correspond à un curseur de jeu de clés ODBC.</span><span class="sxs-lookup"><span data-stu-id="c798a-p102">Dynaset-type Recordset— the result of a query that can have updatable records. A dynaset-type **Recordset** object is a dynamic set of records that you can use to add, change, or delete records from an underlying database table or tables. A dynaset-type **Recordset** object can contain fields from one or more tables in a database. This type corresponds to an ODBC keyset cursor.</span></span>

- <span data-ttu-id="c798a-p103">Recordset de type capture instantanée : copie statique d'un jeu d'enregistrements que vous pouvez utiliser pour rechercher des données ou générer des rapports. Un objet **Recordset** de type capture instantanée peut contenir des champs provenant d'une ou de plusieurs tables de base de données, mais ne peut pas être mis à jour. Ce type correspond à un curseur ODBC statique.</span><span class="sxs-lookup"><span data-stu-id="c798a-p103">Snapshot-type Recordset— a static copy of a set of records that you can use to find data or generate reports. A snapshot-type **Recordset** object can contain fields from one or more tables in a database but can't be updated. This type corresponds to an ODBC static cursor.</span></span>

- <span data-ttu-id="c798a-p104">Recordset de type transfert uniquement : identique au type capture instantanée, sauf qu'aucun curseur n'est fourni. Vous pouvez uniquement faire défiler en avant les enregistrements. Cela améliore les performances lorsque vous devez uniquement effectuer un seul passage dans un jeu de résultats. Ce type correspond à un curseur ODBC de transfert uniquement.</span><span class="sxs-lookup"><span data-stu-id="c798a-p104">Forward-only-type Recordset— identical to a snapshot except that no cursor is provided. You can only scroll forward through records. This improves performance in situations where you only need to make a single pass through a result set. This type corresponds to an ODBC forward-only cursor.</span></span>

- <span data-ttu-id="c798a-p105">Recordset de type dynamique : un résultat de requête défini à partir d'une ou de plusieurs tables de base dans lequel vous pouvez ajouter, modifier ou supprimer des enregistrements à partir d'une requête de renvoi de ligne. En outre, les enregistrements que d'autres utilisateurs ajoutent, suppriment ou modifient dans les tables de base apparaissent également dans votre **Recordset**. Ce type correspond à un curseur ODBC dynamique (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="c798a-p105">Dynamic-type Recordset— a query result set from one or more base tables in which you can add, change, or delete records from a row-returning query. Further, records other users add, delete, or edit in the base tables also appear in your **Recordset**. This type corresponds to an ODBC dynamic cursor (ODBCDirect workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="c798a-p106">Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c798a-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="c798a-127">Vous pouvez choisir le type d'objet**Recordset** que vous voulez créer à l'aide de l'argument type de la méthode**OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="c798a-127">You can choose the type of **Recordset** object you want to create using the  type argument of the **OpenRecordset** method.</span></span>

<span data-ttu-id="c798a-128">Dans un espace de travail Microsoft Access, si vous ne spécifiez pas de type, DAO tente de créer le type de**Recordset**avec le plus de fonctionnalités disponibles, en commençant par un tableau.</span><span class="sxs-lookup"><span data-stu-id="c798a-128">In a Microsoft Access workspace, if you don't specify a  type, DAO attempts to create the type of Recordset with the most functionality available, starting with table.</span></span> <span data-ttu-id="c798a-129">Si ce type n’est pas disponible, DAO tente une feuille de réponse dynamique, un instantané et pour finir un objet **Recordset** de type transfert uniquement.</span><span class="sxs-lookup"><span data-stu-id="c798a-129">If this type isn't available, DAO attempts a dynaset, then a snapshot, and finally a forward-only type **Recordset** object.</span></span>

<span data-ttu-id="c798a-130">Dans un espace de travail ODBCDirect, si vous ne spécifiez pas de type, DAO tente de créer le type de**Recordset**avec la réponse de requête la plus rapide, à partir du type de transfert uniquement.</span><span class="sxs-lookup"><span data-stu-id="c798a-130">In an ODBCDirect workspace, if you don't specify a  type, DAO attempts to create the type of Recordset with the fastest query response, starting with forward-only.</span></span> <span data-ttu-id="c798a-131">Si ce type n'est pas disponible, DAO tente de créer un objet **Recordset** de type capture instantanée, puis de type feuille de réponse dynamique, et enfin de type dynamique.</span><span class="sxs-lookup"><span data-stu-id="c798a-131">If this type isn't available, DAO attempts a snapshot, then a dynaset, and finally a dynamic- type **Recordset** object.</span></span>

<span data-ttu-id="c798a-p109">Lors de la création d’un objet **Recordset** à l’aide d’un objet **[TableDef](tabledef-object-dao.md)** non lié dans un espace de travail Microsoft Access, les objets **Recordset** de type table sont créés. Seuls les objets **Recordset** de type feuille de réponse dynamique ou de type capture instantanée peuvent être créés avec des tables liées ou des tables de bases de données ODBC connectées au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c798a-p109">When creating a **Recordset** object using a non-linked **[TableDef](tabledef-object-dao.md)** object in a Microsoft Access workspace, table-type **Recordset** objects are created. Only dynaset-type or snapshot-type **Recordset** objects can be created with linked tables or tables in Microsoft Access database engine-connected ODBC databases.</span></span>

<span data-ttu-id="c798a-134">Un nouvel objet **Recordset** est automatiquement ajouté à la collection **Recordsets** lorsque vous ouvrez l’objet, et est automatiquement supprimé lorsque vous le fermez.</span><span class="sxs-lookup"><span data-stu-id="c798a-134">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the object, and is automatically removed when you close it.</span></span>

> [!NOTE]
> <span data-ttu-id="c798a-p110">Si vous utilisez des variables pour représenter un objet **Recordset** et l’objet **Database** qui contient cet objet **Recordset**, assurez-vous que les variables ont la même étendue ou durée de vie. Par exemple, si vous déclarez une variable publique représentant un objet **Recordset**, assurez-vous que la variable qui représente la **base de données** contenant le **Recordset** est également publique, ou qu’elle est déclarée dans une procédure **Sub** ou **Function** à l’aide du mot clé **statique**.</span><span class="sxs-lookup"><span data-stu-id="c798a-p110">If you use variables to represent a **Recordset** object and the **Database** object that contains the **Recordset**, make sure the variables have the same scope, or lifetime. For example, if you declare a public variable that represents a **Recordset** object, make sure the variable that represents the **Database** containing the **Recordset** is also public, or is declared in a **Sub** or **Function** procedure using the **Static** keyword.</span></span>

<span data-ttu-id="c798a-p111">Vous pouvez créer autant de variables d’objet **Recordset** que nécessaire. Plusieurs objets **Recordset** peuvent accéder aux mêmes tables, requêtes et champs sans risque de conflit.</span><span class="sxs-lookup"><span data-stu-id="c798a-p111">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="c798a-p112">Les objets **Recordset** de type feuille de réponse dynamique, capture instantanée et transfert uniquement sont stockés dans la mémoire locale. Si l’espace disponible dans la mémoire locale n’est pas suffisant pour stocker les données, le moteur de base de données Microsoft Access enregistre les données supplémentaires dans l’espace disque TEMP. Si cet espace est saturé, une erreur interceptable se produit.</span><span class="sxs-lookup"><span data-stu-id="c798a-p112">Dynaset–, snapshot–, and forward–only–type **Recordset** objects are stored in local memory. If there isn't enough space in local memory to store the data, the Microsoft Access database engine saves the additional data to TEMP disk space. If this space is exhausted, a trappable error occurs.</span></span>

<span data-ttu-id="c798a-p113">La collection par défaut d’un objet **Recordset** est la collection **Fields**, et la propriété par défaut d’un objet **[Field](field-object-dao.md)** est la propriété **[Value](field-value-property-dao.md)**. Utilisez ces valeurs par défaut pour simplifier votre code.</span><span class="sxs-lookup"><span data-stu-id="c798a-p113">The default collection of a **Recordset** object is the **Fields** collection, and the default property of a **[Field](field-object-dao.md)** object is the **[Value](field-value-property-dao.md)** property. Use these defaults to simplify your code.</span></span>

<span data-ttu-id="c798a-p114">Lorsque vous créez un objet **Recordset**, l’enregistrement actif est positionné sur le premier enregistrement s’il existe des enregistrements. S’il n’existe aucun enregistrement, le paramètre de propriété **RecordCount** est défini sur 0, et les propriétés **BOF** et **EOF** ont la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="c798a-p114">When you create a **Recordset** object, the current record is positioned to the first record if there are any records. If there are no records, the **RecordCount** property setting is 0, and the **BOF** and **EOF** property settings are **True**.</span></span>

<span data-ttu-id="c798a-146">Vous pouvez utiliser les méthodes **MoveNext**, **MovePrevious**, **MoveFirst** et **MoveLast** pour repositionner l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="c798a-146">You can use the **MoveNext**, **MovePrevious**, **MoveFirst**, and **MoveLast** methods to reposition the current record.</span></span> <span data-ttu-id="c798a-147">Les objets **Recordset** de type transfert uniquement ne prennent en charge que la méthode **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="c798a-147">Forward–only–type **Recordset** objects support only the **MoveNext** method.</span></span> <span data-ttu-id="c798a-148">Lorsque vous utilisez les méthodes Move pour parcourir chaque enregistrement (ou vous « promener » dans le **Recordset**), vous pouvez utiliser les propriétés **BOF** et **EOF** pour vérifier le début et la fin de l’objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c798a-148">When using the Move methods to visit each record (or "walk" through the **Recordset**), you can use the **BOF** and **EOF** properties to check for the beginning or end of the **Recordset** object.</span></span>

<span data-ttu-id="c798a-149">Avec des objets **Recordset** de type feuille de réponse dynamique et capture instantanée dans un espace de travail Microsoft Access, vous pouvez également utiliser les méthodes Find, comme **FindFirst**, pour localiser un enregistrement spécifique en fonction de certains critères.</span><span class="sxs-lookup"><span data-stu-id="c798a-149">With dynaset- and snapshot-type **Recordset** objects in a Microsoft Access workspace, you can also use the Find methods, such as **FindFirst**, to locate a specific record based on criteria.</span></span> <span data-ttu-id="c798a-150">Si l'enregistrement est introuvable, la propriété **NoMatch** est définie sur **True**.</span><span class="sxs-lookup"><span data-stu-id="c798a-150">If the record isn't found, the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="c798a-151">Pour les objets **Recordset** de type table, vous pouvez analyser les enregistrements à l'aide de la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="c798a-151">For table-type **Recordset** objects, you can scan records using the **Seek** method.</span></span>

<span data-ttu-id="c798a-152">La propriété **Type** indique le type d’objet **Recordset** créé, et la propriété **Updatable** indique si vous pouvez modifier les enregistrements de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c798a-152">The **Type** property indicates the type of **Recordset** object created, and the **Updatable** property indicates whether you can change the object's records.</span></span>

<span data-ttu-id="c798a-153">Les informations sur la structure d’une table de base, comme les noms et les types de données de chaque objet **Field** et des objets **Index**, sont stockées dans un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="c798a-153">Information about the structure of a base table, such as the names and data types of each **Field** object and any **Index** objects, is stored in a **TableDef** object.</span></span>

<span data-ttu-id="c798a-154">Pour faire référence à un objet **Recordset** dans une collection par son nombre ordinal ou par son paramètre de propriété **Name**, utilisez l’une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="c798a-154">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="c798a-155">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="c798a-155">**Recordsets**(0)</span></span>

- <span data-ttu-id="c798a-156">**Recordsets**(«nom»)</span><span class="sxs-lookup"><span data-stu-id="c798a-156">**Recordsets**("name")</span></span>

- <span data-ttu-id="c798a-157">**Recordsets**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="c798a-157">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="c798a-p117">Vous pouvez ouvrir un objet **Recordset** plusieurs fois à partir de la même source de données ou base de données en créant des noms en double dans la collection **Recordsets**. Vous devez attribuer des objets **Recordset** aux variables d’objet et y faire référence par un nom de variable.</span><span class="sxs-lookup"><span data-stu-id="c798a-p117">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="c798a-160">Exemple</span><span class="sxs-lookup"><span data-stu-id="c798a-160">Example</span></span>

<span data-ttu-id="c798a-161">L'exemple ci-dessous illustre les objets **Recordset** et la collection **Recordsets** en ouvrant quatre types d'objet **Recordsets** différents, en énumérant la collection Recordsets de l'objet **Database** actif et en énumérant la collection **Properties** de chaque objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c798a-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

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

Cet exemple utilise la méthode **OpenRecordset** pour ouvrir cinq objets **Recordset** différents et afficher leur contenu.  <span data-ttu-id="c798a-163">La procédure OpenRecordsetOutput est obligatoire pour l’exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="c798a-163">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="c798a-164">Cet exemple ouvre un objet **Recordset** de type dynamique et énumère ses enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c798a-164">This example opens a dynamic-type **Recordset** object and enumerates its records.</span></span>

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

<span data-ttu-id="c798a-165">Cet exemple ouvre un objet **Recordset** de type feuille de réponse dynamique et indique dans quelle mesure ses champs peuvent être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c798a-165">This example opens a dynaset-type **Recordset** and shows the extent to which its fields are updatable.</span></span>

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

<span data-ttu-id="c798a-166">Cet exemple ouvre un objet **Recordset** de type transfert uniquement, illustre ses caractéristiques de lecture seule et avance pas à pas dans le **Recordset** avec la méthode **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="c798a-166">This example opens a forward-only-type **Recordset**, demonstrates its read-only characteristics, and steps through the **Recordset** with the **MoveNext** method.</span></span>

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

<span data-ttu-id="c798a-167">Cet exemple ouvre un objet **Recordset** de type capture instantanée et illustre ses caractéristiques de lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c798a-167">This example opens a snapshot-type **Recordset** and demonstrates its read-only characteristics.</span></span>

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

<span data-ttu-id="c798a-168">Cet exemple ouvre un **Recordset** de type table, définit sa propriété **Index** et énumère ses enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c798a-168">This example opens a table-type **Recordset**, sets its **Index** property, and enumerates its records.</span></span>

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

<span data-ttu-id="c798a-169">L’exemple suivant montre comment utiliser la méthode Recherche pour rechercher un enregistrement dans un tableau lié.</span><span class="sxs-lookup"><span data-stu-id="c798a-169">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="c798a-170">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c798a-170">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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

<span data-ttu-id="c798a-171">L’exemple suivant montre comment ouvrir un Recordset basé sur une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="c798a-171">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

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

<span data-ttu-id="c798a-172">L’exemple suivant montre comment ouvrir un Recordset basé sur un tableau ou une requête.</span><span class="sxs-lookup"><span data-stu-id="c798a-172">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="c798a-173">L’exemple suivant montre comment ouvrir un Recordset basé sur une instruction SQL (Structured Query Language).</span><span class="sxs-lookup"><span data-stu-id="c798a-173">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="c798a-174">L’exemple suivant montre comment utiliser les méthodes TrouverPremier et TrouverSuivant pour rechercher un enregistrement dans un Recordset.</span><span class="sxs-lookup"><span data-stu-id="c798a-174">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

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

<span data-ttu-id="c798a-175">L’exemple suivant montre comment copier les résultats d’une requête vers une feuille de calcul dans un nouveau classeur Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c798a-175">The following example shows how to copy the results of a query to a worksheet in a new Microsoft Excel workbook.</span></span>

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

