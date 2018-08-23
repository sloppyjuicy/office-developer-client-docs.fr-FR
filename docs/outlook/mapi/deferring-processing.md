---
title: Report de traitement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2c4577a35315c9df0055e97de26dd0baf1a2b489
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580585"
---
# <a name="deferring-processing"></a><span data-ttu-id="5f58b-103">Report de traitement</span><span class="sxs-lookup"><span data-stu-id="5f58b-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="5f58b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f58b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f58b-105">Passez l’indicateur MAPI_DEFERRED_ERRORS pour les appels de méthode autant que possible.</span><span class="sxs-lookup"><span data-stu-id="5f58b-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="5f58b-106">Beaucoup d’appels de méthode MAPI ont été optimisés pour accepter cet indicateur, à l’origine du fournisseur à soit attendre la tâche demandée plusieurs tâches peuvent être effectuées à la fois, ou vous pouvez attendre ne sont plus les résultats.</span><span class="sxs-lookup"><span data-stu-id="5f58b-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="5f58b-107">Par exemple, si vous transmettez MAPI_DEFERRED_ERRORS à [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir un dossier, l’ouverture du dossier et un appel à distance possible peut être différée jusqu'à ce que vous effectuez un autre appel comme un appel du dossier **GetHierarchyTable** ou ** GetProps** méthodes.</span><span class="sxs-lookup"><span data-stu-id="5f58b-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="5f58b-108">À la fois **GetHierarchyTable** et **GetProps** requièrent le retour de données à partir du fournisseur de service, une tâche qui doit être exécutée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="5f58b-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="5f58b-109">Une autre manière de différer le traitement est simplement ne pas pour émettre un appel.</span><span class="sxs-lookup"><span data-stu-id="5f58b-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="5f58b-110">En ayant connaissance de l’utilisateur et de l’utilisateur peut percevoir une charge de ressources ou de temps de traitement, vous pouvez déterminer quand il est judicieux de passer des appels.</span><span class="sxs-lookup"><span data-stu-id="5f58b-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="5f58b-111">Il existe une opportunité pour améliorer les performances en effectuant des appels, soit à la fois lorsque l’utilisateur ne remarqueront ou ne pas les rendant tout.</span><span class="sxs-lookup"><span data-stu-id="5f58b-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="5f58b-112">Par exemple, considérez la situation lorsque vous recevez une plusieurs notification par seconde à partir d’une banque de messages est de déplacer un grand nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="5f58b-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="5f58b-113">Un indicateur de progression est affiché pour indiquer le pourcentage d’achèvement de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5f58b-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="5f58b-114">Les utilisateurs généralement pas voit cette opération pour être lente jusqu'à ce que quelques secondes se sont écoulées.</span><span class="sxs-lookup"><span data-stu-id="5f58b-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="5f58b-115">Par conséquent, si vous mettez à jour l’indicateur de progression, n’apportez aucune modification jusqu’au moins quatre secondes après l’ouverture de l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="5f58b-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="5f58b-116">Cela gagner du temps dans les cas lorsque l’opération est rapide et informer les utilisateurs en temps voulu lorsque l’opération est lente.</span><span class="sxs-lookup"><span data-stu-id="5f58b-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

