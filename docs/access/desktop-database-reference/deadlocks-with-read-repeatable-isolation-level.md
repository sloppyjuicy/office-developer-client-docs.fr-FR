---
title: Blocages avec niveau d'isolation récurrent de lecture
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a5fbf4686fc5b8bffc984b4b483f1ee506eb7dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882986"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="97f7c-102">Blocages avec niveau d'isolation récurrent de lecture</span><span class="sxs-lookup"><span data-stu-id="97f7c-102">Deadlocks With Read Repeatable Isolation Level</span></span>


<span data-ttu-id="97f7c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97f7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97f7c-p101">Si un objet métier personnalisé utilise un niveau d'isolation récurrent de lecture pour accéder à un serveur SQL Server et si l'objet métier est appelé simultanément par deux clients qui envoient une requête et se mettent à jour dans la même transaction, un blocage est possible. Le service RDS est conçu de telle sorte que l'un des processus expire et libère ainsi le blocage. Toutefois, la mise à jour échoue pour ce client.</span><span class="sxs-lookup"><span data-stu-id="97f7c-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="97f7c-106">Utilisez la propriété dynamique**Command Time Out** de [Service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md)pour modifier le délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="97f7c-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

