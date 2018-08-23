---
title: Les opérations de table asynchrone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569420"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="68da4-103">Les opérations de table asynchrone</span><span class="sxs-lookup"><span data-stu-id="68da4-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="68da4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68da4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68da4-105">L’interface **IMAPITable** inclut trois méthodes qui fonctionnent de manière asynchrone et trois méthodes pour le contrôle d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="68da4-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="68da4-106">Le tableau suivant répertorie les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="68da4-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="68da4-107">**Opération asynchrone**</span><span class="sxs-lookup"><span data-stu-id="68da4-107">**Asynchronous operation**</span></span>|<span data-ttu-id="68da4-108">**Méthode de contrôle asynchrone**</span><span class="sxs-lookup"><span data-stu-id="68da4-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68da4-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="68da4-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="68da4-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="68da4-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="68da4-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="68da4-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="68da4-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="68da4-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="68da4-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="68da4-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="68da4-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="68da4-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="68da4-115">**Pour récupérer les informations d’état sur le type et l’opération en cours d’une table**</span><span class="sxs-lookup"><span data-stu-id="68da4-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="68da4-116">Appelez [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="68da4-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="68da4-117">Avec **GetStatus**, un utilisateur de la table peut déterminer si le tableau est statiques ou dynamiques, si une opération est en cours ou a terminé, et si une erreur s’est produite à partir d’une opération terminée.</span><span class="sxs-lookup"><span data-stu-id="68da4-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="68da4-118">Par exemple, si un client a besoin d’annuler une opération de tri, car elle prend trop de temps, le client peut appeler tout d’abord **GetStatus** pour déterminer si, en fait, une opération de tri est actuellement de traitement.</span><span class="sxs-lookup"><span data-stu-id="68da4-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="68da4-119">Ensuite, le client peut appeler [IMAPITable::Abort](imapitable-abort.md) pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="68da4-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="68da4-120">**Pour suspendre l’activité jusqu'à ce qu’une tâche asynchrone est terminée.**</span><span class="sxs-lookup"><span data-stu-id="68da4-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="68da4-121">Appelez [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="68da4-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="68da4-122">L’appel **WaitForCompletion** permet la tâche se termine sans interruption.</span><span class="sxs-lookup"><span data-stu-id="68da4-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="68da4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68da4-123">See also</span></span>

- [<span data-ttu-id="68da4-124">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="68da4-124">MAPI Tables</span></span>](mapi-tables.md)

