---
title: Workspace, objet (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308357"
---
# <a name="workspace-object-dao"></a><span data-ttu-id="6b517-102">Workspace, objet (DAO)</span><span class="sxs-lookup"><span data-stu-id="6b517-102">Workspace Object (DAO)</span></span>

<span data-ttu-id="6b517-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b517-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b517-p101">A **espace de travail** objet définit une session nommée pour un utilisateur. Il contient des bases de données ouverts et fournit des mécanismes pour les transactions simultanées et, dans les espaces de travail Microsoft Access, groupe de travail support sécurisé.</span><span class="sxs-lookup"><span data-stu-id="6b517-p101">A **Workspace** object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b517-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b517-106">Remarks</span></span>

<span data-ttu-id="6b517-p102">A **espace de travail** est un objet non persistant qui définit la manière dont votre application interagit avec les données à l’aide du moteur de base de données Microsoft Access. Utilisez le **espace de travail** objet pour gérer la session actuelle ou en démarrer une session de messagerie supplémentaires. Dans une session, vous pouvez ouvrir plusieurs bases de données ou des connexions et gérer des transactions. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="6b517-p102">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine. Use the **Workspace** object to manage the current session or to start an additional session. In a session, you can open multiple databases or connections, and manage transactions. For example, you can:</span></span>

- <span data-ttu-id="6b517-p103">Utilisez le **nom**, **nom d’utilisateur**, et **Type** propriétés à établir une session nommée. La session crée une étendue dans lequel vous pouvez ouvrir plusieurs bases de données et diriger une instance de transactions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="6b517-p103">Use the **Name**, **UserName**, and **Type** properties to establish a named session. The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="6b517-113">Utilisez le **fermer** méthode clôturer une session.</span><span class="sxs-lookup"><span data-stu-id="6b517-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="6b517-114">Utilisez le **OpenDatabase** méthode pour ouvrir une ou plusieurs bases de données existantes sur un **espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="6b517-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="6b517-115">Utiliser le **BeginTrans**, **CommitTrans**, et **restauration** méthodes permettent de gérer des transactions imbriquées processing au sein d’un **espace de travail** et utiliser plusieurs **espace de travail** objets pour effectuer les transactions multiples, simultanées et qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="6b517-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="6b517-116">Lorsque vous utilisez ou référencez un objet **Workspace** pour la première fois, vous créez automatiquement l’espace de travail par défaut DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="6b517-116">When you first refer to or use a Workspace object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="6b517-117">Les paramètres des propriétés **Name** et **UserName** de l’espace de travail par défaut sont respectivement « \##Default Workspace#\# » et « Admin ».</span><span class="sxs-lookup"><span data-stu-id="6b517-117">The settings of the Name and UserName properties of the default workspace are "#Default Workspace#" and "Admin," respectively.</span></span> <span data-ttu-id="6b517-118">Si la sécurité est activée, la **nom d’utilisateur** paramètre de la propriété est le nom de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="6b517-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="6b517-p105">Lorsque vous utilisez des transactions, toutes les bases de données de la valeur **espace de travail** sont affectés, même si plusieurs **base de données** objets sont ouverts dans le **espace de travail**. Par exemple, vous utilisez un **BeginTrans** méthode, mettre à jour plusieurs enregistrements dans une base de données, puis supprimer des enregistrements dans une autre base de données. Si vous utilisez ensuite la **restauration** méthode, les opérations de mise à jour et supprimer sont et annulées. Vous pouvez créer supplémentaires **espace de travail** objets gérer séparément ensemble des transactions **base de données** objets.</span><span class="sxs-lookup"><span data-stu-id="6b517-p105">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**. For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database. If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back. You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="6b517-p106">Vous pouvez créer **espace de travail** objets avec la **CreateWorkspace** méthode. Après avoir créé un nouveau **espace de travail** objet, vous devez ajouter pour le **espaces de travail** collection de sites si vous avez besoin faire référence à partir du **espaces de travail** collection de sites.</span><span class="sxs-lookup"><span data-stu-id="6b517-p106">You can create **Workspace** objects with the **CreateWorkspace** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="6b517-p107">Vous pouvez utiliser nouvellement créé **espace de travail** objet sans en ajoutant le **espaces de travail** collection de sites. Toutefois, vous devez y faire référence pour par la variable objet auquel vous l’avez attribué.</span><span class="sxs-lookup"><span data-stu-id="6b517-p107">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection. However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="6b517-127">Pour faire référence à un objet **TableDef** dans une collection par son nombre ordinal ou par son paramètre de propriété **Name**, utilisez l’une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b517-127">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="6b517-128">**DBEngine**.**Workspaces**(0)</span><span class="sxs-lookup"><span data-stu-id="6b517-128">**DBEngine**. **Workspaces**(0)</span></span>

<span data-ttu-id="6b517-129">**DBEngine**.**Workspaces**("name")</span><span class="sxs-lookup"><span data-stu-id="6b517-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="6b517-130">**DBEngine**.**Workspaces**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="6b517-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="6b517-p108">Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6b517-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="6b517-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="6b517-133">Example</span></span>

<span data-ttu-id="6b517-p109">Cet exemple crée un objet espace de travail Microsoft Access et qu’il ajoute le **espaces de travail** collection de sites. Il énumère ensuite la **espaces de travail** collections de sites et le **propriétés** ensemble de la **espace de travail** objet.</span><span class="sxs-lookup"><span data-stu-id="6b517-p109">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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

Cet exemple utilise la **CreateWorkspace** méthode pour créer un espace de travail Microsoft Access. <span data-ttu-id="6b517-137">Il répertorie les propriétés de l’espace d’ensuite.</span><span class="sxs-lookup"><span data-stu-id="6b517-137">It then lists the properties of theworkspace.</span></span>

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

<span data-ttu-id="6b517-138">L’exemple suivant montre comment utiliser une transaction dans un espace de travail Data Access Objects (DAO).</span><span class="sxs-lookup"><span data-stu-id="6b517-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="6b517-139">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6b517-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
