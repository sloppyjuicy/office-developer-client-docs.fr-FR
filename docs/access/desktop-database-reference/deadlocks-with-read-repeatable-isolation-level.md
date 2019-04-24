---
title: Blocages avec niveau d'isolation extensible de lecture
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294175"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="0d070-102">Blocages avec niveau d'isolation extensible de lecture</span><span class="sxs-lookup"><span data-stu-id="0d070-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="0d070-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d070-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d070-p101">Si un objet métier personnalisé utilise un niveau d'isolation récurrent de lecture pour accéder à un serveur SQL Server et si l'objet métier est appelé simultanément par deux clients qui envoient une requête et se mettent à jour dans la même transaction, un blocage est possible. Le service RDS est conçu de telle sorte que l'un des processus expire et libère ainsi le blocage. Toutefois, la mise à jour échoue pour ce client.</span><span class="sxs-lookup"><span data-stu-id="0d070-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="0d070-106">Utilisez la propriété dynamique**Command Time Out** du [service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md)pour modifier la longueur du délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="0d070-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

