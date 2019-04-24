---
title: Connection. Cancel, méthode (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0826a30f22cc46eb6ff9a114dbf02cab1d9f76a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295967"
---
# <a name="connectioncancel-method-dao"></a><span data-ttu-id="bac24-102">Connection. Cancel, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="bac24-102">Connection.Cancel method (DAO)</span></span>

<span data-ttu-id="bac24-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bac24-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="bac24-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bac24-104">Syntax</span></span>

<span data-ttu-id="bac24-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="bac24-105">*expression* .Cancel</span></span>

<span data-ttu-id="bac24-106">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="bac24-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac24-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="bac24-107">Remarks</span></span>

<span data-ttu-id="bac24-108">Utilisez la méthode **Cancel** pour mettre fin à l'exécution d'un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été appelée avec l'option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="bac24-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="bac24-109">**Cancel** renvoie une erreur d'exécution si dbRunAsync n'a pas été utilisé dans la méthode que vous essayez de terminer.</span><span class="sxs-lookup"><span data-stu-id="bac24-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

<span data-ttu-id="bac24-110">Une erreur se produira si, après un appel de la méthode **Cancel**, vous tentez de référencer l'objet qui aurait été créé par une appel de la méthode **OpenConnection** asynchrone (à savoir, l'objet **Connection** à partir duquel vous avez appelé la méthode **Cancel**).</span><span class="sxs-lookup"><span data-stu-id="bac24-110">An error will occur if, following a **Cancel** method call, you try to reference the object that would have been created by an asynchronous **OpenConnection** call (that is, the **Connection** object from which you called the **Cancel** method).</span></span>

## <a name="example"></a><span data-ttu-id="bac24-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="bac24-111">Example</span></span>

<span data-ttu-id="bac24-112">Cet exemple utilise la propriété **StillExecuting** et la méthode **Cancel** pour ouvrir un objet **Connection** en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bac24-112">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

```vb
    Sub CancelConnectionX() 
     
     Dim wrkMain As Workspace 
     Dim conMain As Connection 
     Dim sngTime As Single 
     
     Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
     "admin", "", dbUseODBC) 
     ' Open the connection asynchronously. 
     
     ' Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conMain = wrkMain.OpenConnection("Publishers", _ 
     dbDriverNoPrompt + dbRunAsync, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     sngTime = Timer 
     
     ' Wait five seconds. 
     Do While Timer - sngTime < 5 
     Loop 
     
     ' If the connection has not been made, ask the user 
     ' if she wants to keep waiting. If she does not, cancel 
     ' the connection and exit the procedure. 
     Do While conMain.StillExecuting 
     
     If MsgBox("No connection yet--keep waiting?", _ 
     vbYesNo) = vbNo Then 
     conMain.Cancel 
     MsgBox "Connection cancelled!" 
     wrkMain.Close 
     Exit Sub 
     End If 
     
     Loop 
     
     With conMain 
     ' Use the Connection object conMain. 
     .Close 
     End With 
     
     wrkMain.Close 
     
    End Sub
```
