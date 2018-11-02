---
title: Objet espace de travail (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f658822255e090594bdb43cd1b5e9ec1f30199cc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925743"
---
# <a name="workspace-object-dao"></a><span data-ttu-id="74883-102">Objet espace de travail (DAO)</span><span class="sxs-lookup"><span data-stu-id="74883-102">Workspace object (DAO)</span></span>

<span data-ttu-id="74883-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74883-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74883-p101">Un objet **Workspace** définit une session nommée pour un utilisateur. Il contient des bases de données ouvertes et fournit les mécanismes destinés aux transactions simultanées, ainsi que la prise en charge des groupes de travail sécurisés dans les espaces de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="74883-p101">A **Workspace** object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="74883-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="74883-106">Remarks</span></span>

<span data-ttu-id="74883-p102">Un objet **Workspace** est un objet non persistant qui détermine le mode d'interaction entre l'application et les données, à savoir à l'aide du moteur de base de données Microsoft Access. Utilisez l'objet **Workspace** pour gérer la session active ou pour démarrer une session supplémentaire. Dans une session, vous pouvez ouvrir plusieurs bases de données ou connexions et gérer les transactions. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="74883-p102">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine. Use the **Workspace** object to manage the current session or to start an additional session. In a session, you can open multiple databases or connections, and manage transactions. For example, you can:</span></span>

- <span data-ttu-id="74883-p103">Utiliser les propriétés **Name**, **UserName** et **Type** pour établir une session nommée. La session crée une étendue dans laquelle vous pouvez ouvrir plusieurs bases de données et exécuter une instance de transactions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="74883-p103">Use the **Name**, **UserName**, and **Type** properties to establish a named session. The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="74883-113">Utiliser la méthode **Close** pour fermer une session.</span><span class="sxs-lookup"><span data-stu-id="74883-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="74883-114">Utiliser la méthode **OpenDatabase** pour ouvrir une ou plusieurs bases de données existantes dans un objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="74883-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="74883-115">Utiliser les méthodes **BeginTrans**, **CommitTrans** et **Rollback** pour gérer le traitement des transactions imbriquées dans un objet **Workspace** et utiliser plusieurs objets **Workspace** pour exécuter des transactions multiples, simultanées et se chevauchant.</span><span class="sxs-lookup"><span data-stu-id="74883-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="74883-116">Lorsque vous consultez ou utilisez un objet **Workspace** , vous créez automatiquement l’espace de travail par défaut, DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="74883-116">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="74883-117">Les paramètres des propriétés **Name** et **UserName** de l’espace de travail par défaut sont «\#espace de travail par défaut\#» et « Admin », respectivement.</span><span class="sxs-lookup"><span data-stu-id="74883-117">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="74883-118">Si la sécurité est activée, le paramètre de propriété **UserName** correspond au nom de l'utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="74883-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="74883-p105">Lorsque vous utilisez des transactions, toutes les bases de données de l'objet **Workspace** spécifié sont concernés, même si plusieurs objets **Database** sont ouverts dans l'objet **Workspace**. Par exemple, vous utilisez une méthode **BeginTrans**, mettez à jour plusieurs enregistrements d'une base de données, puis supprimez des enregistrements d'une autre base de données. Si vous utilisez à présent la méthode **Rollback**, les opérations de mise à jour et de suppression sont annulées et restaurées. Vous pouvez créer d'autres objets **Workspace** afin de gérer les transactions de manière indépendante dans les objets **Database**.</span><span class="sxs-lookup"><span data-stu-id="74883-p105">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**. For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database. If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back. You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="74883-123">Vous pouvez créer des objets de **l’espace de travail** avec la méthode **CreateWorkspace** .</span><span class="sxs-lookup"><span data-stu-id="74883-123">You can create **Workspace** objects with the **CreateWorkspace** method.</span></span> <span data-ttu-id="74883-124">Après avoir créé un nouvel objet **Workspace** , vous devez l’ajouter à la collection **Workspaces** si vous devez faire référence à partir de la collection **Workspaces** .</span><span class="sxs-lookup"><span data-stu-id="74883-124">After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="74883-p107">Vous pouvez utiliser un nouvel objet **Workspace** sans l'ajouter à la collection **Workspaces**. Toutefois, dans ce cas, vous devez y faire référence en fonction de la variable d'objet à laquelle il est attribué.</span><span class="sxs-lookup"><span data-stu-id="74883-p107">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection. However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="74883-127">Pour faire référence à un objet **Workspace** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="74883-127">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="74883-128">**DBEngine**. **Espaces de travail** (0)</span><span class="sxs-lookup"><span data-stu-id="74883-128">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="74883-129">**DBEngine**. **Espaces de travail** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="74883-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="74883-130">**DBEngine**. **Espaces de travail** \! \[nom\]</span><span class="sxs-lookup"><span data-stu-id="74883-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="74883-p108">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="74883-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="74883-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="74883-133">Example</span></span>

<span data-ttu-id="74883-p109">Cet exemple crée un nouvel objet Microsoft Access et l'ajoute aux collections **Workspaces**. Il énumère ensuite les collections **Workspaces** et la collection **Properties** de chaque objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="74883-p109">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="74883-p110">Cet exemple utilise la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il répertorie ensuite les propriétés de l'espace de travail.</span><span class="sxs-lookup"><span data-stu-id="74883-p110">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="74883-138">L’exemple suivant montre comment utiliser une transaction dans un espace de travail Data Access Objects (DAO).</span><span class="sxs-lookup"><span data-stu-id="74883-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="74883-139">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="74883-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
