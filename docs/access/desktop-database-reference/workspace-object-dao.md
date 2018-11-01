---
title: Workspace Object (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17e8bd561858c8cb1eeb9bf84f6fc636a37f812b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875062"
---
# <a name="workspace-object-dao"></a>Workspace Object (DAO)

**S’applique à**: Access 2013, Office 2013

Un objet **Workspace** définit une session nommée pour un utilisateur. Il contient des bases de données ouvertes et fournit les mécanismes destinés aux transactions simultanées, ainsi que la prise en charge des groupes de travail sécurisés dans les espaces de travail Microsoft Access.

## <a name="remarks"></a>Remarques

Un objet **Workspace** est un objet non persistant qui détermine le mode d'interaction entre l'application et les données, à savoir à l'aide du moteur de base de données Microsoft Access. Utilisez l'objet **Workspace** pour gérer la session active ou pour démarrer une session supplémentaire. Dans une session, vous pouvez ouvrir plusieurs bases de données ou connexions et gérer les transactions. Par exemple, vous pouvez :

- Utiliser les propriétés **Name**, **UserName** et **Type** pour établir une session nommée. La session crée une étendue dans laquelle vous pouvez ouvrir plusieurs bases de données et exécuter une instance de transactions imbriquées.

- Utiliser la méthode **Close** pour fermer une session.

- Utiliser la méthode **OpenDatabase** pour ouvrir une ou plusieurs bases de données existantes dans un objet **Workspace**.

- Utiliser les méthodes **BeginTrans**, **CommitTrans** et **Rollback** pour gérer le traitement des transactions imbriquées dans un objet **Workspace** et utiliser plusieurs objets **Workspace** pour exécuter des transactions multiples, simultanées et se chevauchant.

Lorsque vous consultez ou utilisez un objet **Workspace** , vous créez automatiquement l’espace de travail par défaut, DBEngine.Workspaces(0). Les paramètres des propriétés **Name** et **UserName** de l’espace de travail par défaut sont «\#espace de travail par défaut\#» et « Admin », respectivement. Si la sécurité est activée, le paramètre de propriété **UserName** correspond au nom de l'utilisateur connecté.

Lorsque vous utilisez des transactions, toutes les bases de données de l'objet **Workspace** spécifié sont concernés, même si plusieurs objets **Database** sont ouverts dans l'objet **Workspace**. Par exemple, vous utilisez une méthode **BeginTrans**, mettez à jour plusieurs enregistrements d'une base de données, puis supprimez des enregistrements d'une autre base de données. Si vous utilisez à présent la méthode **Rollback**, les opérations de mise à jour et de suppression sont annulées et restaurées. Vous pouvez créer d'autres objets **Workspace** afin de gérer les transactions de manière indépendante dans les objets **Database**.

Vous pouvez créer des objets de **l’espace de travail** avec la méthode **CreateWorkspace** . Après avoir créé un nouvel objet **Workspace** , vous devez l’ajouter à la collection **Workspaces** si vous devez faire référence à partir de la collection **Workspaces** .

Vous pouvez utiliser un nouvel objet **Workspace** sans l'ajouter à la collection **Workspaces**. Toutefois, dans ce cas, vous devez y faire référence en fonction de la variable d'objet à laquelle il est attribué.

Pour faire référence à un objet **Workspace** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

**DBEngine**. **Espaces de travail** (0)

**DBEngine**. **Espaces de travail** (« nom »)

**DBEngine**. **Espaces de travail** \! \[nom\]

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.


## <a name="example"></a>Exemple

Cet exemple crée un nouvel objet Microsoft Access et l'ajoute aux collections **Workspaces**. Il énumère ensuite les collections **Workspaces** et la collection **Properties** de chaque objet **Workspace**.

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

Cet exemple utilise la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il répertorie ensuite les propriétés de l'espace de travail.

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

L’exemple suivant montre comment utiliser une transaction dans un espace de travail Data Access Objects (DAO).

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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
