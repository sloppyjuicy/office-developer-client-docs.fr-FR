---
title: Traitement des mises à jour échouées
TOCTitle: Dealing with Failed Updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3af3026052954ec74b10026e0cf288a6aa5249
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469471"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="d3a08-102">Traitement des mises à jour échouées</span><span class="sxs-lookup"><span data-stu-id="d3a08-102">Dealing with Failed Updates</span></span>


<span data-ttu-id="d3a08-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3a08-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="d3a08-104">Traitement des mises à jour échouées</span><span class="sxs-lookup"><span data-stu-id="d3a08-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="d3a08-p101">Lorsqu'une mise à jour se solde par un échec, la résolution des erreurs dépend de leur nature, de leur sévérité et de la logique de votre application. Toutefois, si la base de données est partagée avec d'autres utilisateurs, une erreur commune consiste à ce qu'une autre personne modifie le champ avant vous. Ce type d'erreur est appelé un *conflit*. ADO détecte cette situation et signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="d3a08-p101">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application. However, if the database is shared with other users, a typical error is that someone else modifies the field before you do. This type of error is called a *conflict.* ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="d3a08-109">Si des erreurs de mise à jour surviennent, elles sont dirigées dans un programme de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="d3a08-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="d3a08-110">Pour que seules les lignes présentant des conflits soient visibles, filtrez le **jeu d'enregistrements** avec la constante **adFilterConflictingRecords**.</span><span class="sxs-lookup"><span data-stu-id="d3a08-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="d3a08-111">Dans cet exemple, la stratégie de résolution des erreurs consiste tout simplement à imprimer l’auteur du premier et du prénom (**au\_fname** et **au\_lname**).</span><span class="sxs-lookup"><span data-stu-id="d3a08-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="d3a08-112">Le code permettant d'alerter l'utilisateur du conflit de mise à jour ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="d3a08-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

