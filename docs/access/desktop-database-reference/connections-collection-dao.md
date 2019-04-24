---
title: Connections, collection (DAO)
TOCTitle: Connections collection
ms:assetid: 65d073be-a84b-e3f2-cb43-b87ffa60e497
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195178(v=office.15)
ms:contentKeyID: 48545330
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 66f122b7bdaa9069b839cd5884b5da5da48a15f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295785"
---
# <a name="connections-collection-dao"></a><span data-ttu-id="b7af7-102">Connections, collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7af7-102">Connections collection (DAO)</span></span>

<span data-ttu-id="b7af7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7af7-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="b7af7-p101">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b7af7-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="b7af7-106">Une \*\*\*\* collection Connects contient les objets **Connection** actifs d'un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="b7af7-106">A **Connections** collection contains the current **Connection** objects of a **Workspace** object.</span></span> <span data-ttu-id="b7af7-107">(Espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="b7af7-107">(ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7af7-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7af7-108">Remarks</span></span>

<span data-ttu-id="b7af7-p103">Lorsque vous ouvrez un objet **Connection**, il est automatiquement ajouté à la collection **Connections** de l'objet **Workspace**. Lorsque vous fermez un objet **Connection** à l'aide de la méthode **[Close](connection-close-method-dao.md)**, il est supprimé de la collection **Connections**. Il convient de fermer tous les objets **[Recordset](recordset-object-dao.md)** ouverts de l'objet **Connection** avant de le fermer.</span><span class="sxs-lookup"><span data-stu-id="b7af7-p103">When you open a **Connection** object, it is automatically appended to the **Connections** collection of the **Workspace**. When you close a **Connection** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Connections** collection. You should close all open **[Recordset](recordset-object-dao.md)** objects within the **Connection** before closing it.</span></span>

<span data-ttu-id="b7af7-p104">Lorsque vous ouvrez un objet **Connection**, un objet **[Database](database-object-dao.md)** correspondant est créé et ajouté à la collection **[Databases](databases-collection-dao.md)** dans le même objet **Workspace** et vice versa. De la même manière, lorsque vous fermez l'objet **Connection**, l'objet **Database** correspondant est supprimé de la collection **Databases**, etc.</span><span class="sxs-lookup"><span data-stu-id="b7af7-p104">At the same time you open a **Connection** object, a corresponding **[Database](database-object-dao.md)** object is created and appended to the **[Databases](databases-collection-dao.md)** collection in the same **Workspace**, and vice versa. Similarly, when you close the **Connection**, the corresponding **Database** is deleted from the **Databases** collection, and so on.</span></span>

<span data-ttu-id="b7af7-p105">Le paramètre de propriété **Name** d'un objet **Connection** est une chaîne qui spécifie le chemin d'accès au fichier de base de données. Pour faire référence à un objet **Connection** d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7af7-p105">The **Name** property setting of a **Connection** is a string that specifies the path of the database file. To refer to a **Connection** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="b7af7-116">**Connexions** 0</span><span class="sxs-lookup"><span data-stu-id="b7af7-116">**Connections**(0)</span></span>

- <span data-ttu-id="b7af7-117">**Connexions** ("*nom*")</span><span class="sxs-lookup"><span data-stu-id="b7af7-117">**Connections**("*name*")</span></span>

- <span data-ttu-id="b7af7-118">\*\*\*\*\!\[*Nom* des connexions\]</span><span class="sxs-lookup"><span data-stu-id="b7af7-118">**Connections**\!\[*name*\]</span></span>


> [!NOTE]
> <span data-ttu-id="b7af7-p106">[!REMARQUE] Vous pouvez ouvrir la même source de données plusieurs fois, ce qui crée des noms dupliqués dans la collection **Connections**. Il convient d'affecter des objets **Connection** aux variables d'objet et de s'y référer par nom de variables.</span><span class="sxs-lookup"><span data-stu-id="b7af7-p106">You can open the same data source more than once, creating duplicate names in the **Connections** collection. You should assign **Connection** objects to object variables and refer to them by variable name.</span></span>


## <a name="example"></a><span data-ttu-id="b7af7-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="b7af7-121">Example</span></span>

<span data-ttu-id="b7af7-122">Cet exemple illustre l'objet **Connection** et la collection **Connections** en ouvrant un objet **Database** et deux objets **Connection** ODBCDirect et en répertoriant les propriétés disponibles pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="b7af7-122">This example demonstrates the **Connection** object and **Connections** collection by opening a **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
   Dim wrkAcc as Workspace 
   Dim dbsNorthwind As Database 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conLoop As Connection 
   Dim prpLoop As Property 
 
   ' Open a Database object. 
   Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
      "admin", "", dbUseJet) 
   Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
   ' Create ODBCDirect Workspace object and open Connection 
   ' objects. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
       
   ' Note: The DSNs referenced below must be configured to  
   '       use Microsoft Windows NT Authentication Mode to  
   '       authorize user access to the Microsoft SQL Server. 
   Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
      "ODBC;DATABASE=pubs;DSN=Publishers") 
       
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
      True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   Debug.Print "Database properties:" 
 
   With dbsNorthwind 
      ' Enumerate Properties collection of Database object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         Debug.Print "  " & prpLoop.Name & " = " & _ 
            prpLoop.Value 
         On Error GoTo 0 
      Next prpLoop 
   End With 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   dbsNorthwind.Close 
   conPubs.Close 
   conPubs2.Close 
   wrkAcc.Close 
   wrkODBC.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="b7af7-123">Cet exemple utilise la méthode **OpenConnection** avec différents paramètres pour ouvrir trois objets **Connection** différents.</span><span class="sxs-lookup"><span data-stu-id="b7af7-123">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conPubs3 As Connection 
   Dim conLoop As Connection 
 
   ' Create ODBCDirect Workspace object. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
 
   ' Open Connection object using supplied information in  
   ' the connect string. If this information were  
   ' insufficient, you could trap for an error rather than  
   ' go to an ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection1..." 
       
    ' Note: The DSN referenced below must be set to  
    '       use Microsoft Windows NT Authentication Mode to  
    '       authorize user access to the Microsoft SQL Server. 
    Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
       dbDriverNoPrompt, , _ 
       "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   ' Open read-only Connection object based on information  
   ' you enter in the ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection2..." 
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
      dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
   ' Open read-only Connection object by entering only the  
   ' missing information in the ODBC Driver Manager dialog  
   ' box. 
   MsgBox "Opening Connection3..." 
   Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
      dbDriverCompleteRequired, True, _ 
      "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   conPubs.Close 
   conPubs2.Close 
   conPubs3.Close 
   wrkODBC.Close 
 
End Sub 
 
```

