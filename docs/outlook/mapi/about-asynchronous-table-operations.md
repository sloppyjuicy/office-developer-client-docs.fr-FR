---
title: Opérations des tables asynchrones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439568"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="54ad4-103">Opérations des tables asynchrones</span><span class="sxs-lookup"><span data-stu-id="54ad4-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="54ad4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ad4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ad4-105">L'interface **IMAPITable** comprend trois méthodes qui fonctionnent de manière asynchrone et trois méthodes pour contrôler une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="54ad4-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="54ad4-106">Le tableau suivant répertorie ces méthodes:</span><span class="sxs-lookup"><span data-stu-id="54ad4-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="54ad4-107">**Opération asynchrone**</span><span class="sxs-lookup"><span data-stu-id="54ad4-107">**Asynchronous operation**</span></span>|<span data-ttu-id="54ad4-108">**Méthode de contrôle asynchrone**</span><span class="sxs-lookup"><span data-stu-id="54ad4-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54ad4-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="54ad4-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="54ad4-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="54ad4-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="54ad4-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="54ad4-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="54ad4-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="54ad4-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="54ad4-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="54ad4-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="54ad4-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="54ad4-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="54ad4-115">**Pour récupérer des informations d'État sur le type et l'opération en cours d'une table**</span><span class="sxs-lookup"><span data-stu-id="54ad4-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="54ad4-116">Appeler [IMAPITable:: GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="54ad4-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="54ad4-117">Avec **GetStatus**, un utilisateur de tableau peut déterminer si la table est statique ou dynamique, si une opération est en cours ou est terminée, et si une erreur s'est produite à partir d'une opération terminée.</span><span class="sxs-lookup"><span data-stu-id="54ad4-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="54ad4-118">Par exemple, si un client a besoin d'annuler une opération de tri parce qu'il prend trop de temps, le client peut tout d'abord appeler **GetStatus** pour déterminer si une opération de tri est actuellement en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="54ad4-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="54ad4-119">Le client peut alors appeler [IMAPITable:: Abort](imapitable-abort.md) pour l'arrêter.</span><span class="sxs-lookup"><span data-stu-id="54ad4-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="54ad4-120">**Pour suspendre l'activité jusqu'à la fin d'une tâche asynchrone**</span><span class="sxs-lookup"><span data-stu-id="54ad4-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="54ad4-121">Appeler [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="54ad4-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="54ad4-122">L'appel de **WaitForCompletion** permet à la tâche de se terminer sans interruption.</span><span class="sxs-lookup"><span data-stu-id="54ad4-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="54ad4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54ad4-123">See also</span></span>

- [<span data-ttu-id="54ad4-124">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="54ad4-124">MAPI Tables</span></span>](mapi-tables.md)

