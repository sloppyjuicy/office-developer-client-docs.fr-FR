---
title: Report du traitement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430930"
---
# <a name="deferring-processing"></a><span data-ttu-id="95287-103">Report du traitement</span><span class="sxs-lookup"><span data-stu-id="95287-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="95287-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95287-105">Passez l’MAPI_DEFERRED_ERRORS aux appels de méthode autant que possible.</span><span class="sxs-lookup"><span data-stu-id="95287-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="95287-106">De nombreux appels de méthode MAPI ont été optimisés pour accepter cet indicateur, ce qui a pour effet que le fournisseur ajournait la tâche demandée jusqu’à ce que plusieurs tâches soient effectuées en même temps ou que vous ne pouvez plus attendre les résultats.</span><span class="sxs-lookup"><span data-stu-id="95287-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="95287-107">Par exemple, si vous passez MAPI_DEFERRED_ERRORS à [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir un dossier, l’ouverture du dossier et un appel distant possible peuvent être reportés jusqu’à ce que vous appelez à nouveau les méthodes **GetHierarchyTable** ou **GetProps** du dossier.</span><span class="sxs-lookup"><span data-stu-id="95287-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="95287-108">**GetHierarchyTable** et **GetProps** nécessitent le retour des données du fournisseur de services, une tâche qui doit être effectuée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="95287-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="95287-109">Une autre façon de différer le traitement consiste simplement à ne pas effectuer d’appel.</span><span class="sxs-lookup"><span data-stu-id="95287-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="95287-110">En étant conscient de l’utilisateur et du moment où il peut percevoir un drainage des ressources ou du temps de traitement, vous pouvez déterminer à quel moment il est logique d’effectuer des appels.</span><span class="sxs-lookup"><span data-stu-id="95287-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="95287-111">Il est possible d’améliorer les performances en faisant des appels à un moment où l’utilisateur ne le remarque pas ou en ne les rendant pas du tout.</span><span class="sxs-lookup"><span data-stu-id="95287-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="95287-112">Par exemple, prenons la situation dans laquelle vous recevez plus d’une notification par seconde à partir d’une boutique de messages qui déplace un grand nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="95287-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="95287-113">Un indicateur de progression s’affiche pour indiquer le pourcentage d’achèvement de l’opération.</span><span class="sxs-lookup"><span data-stu-id="95287-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="95287-114">En règle générale, les utilisateurs ne percevoiraient pas cette opération comme lente tant que quelques secondes n’ont pas été écoulées.</span><span class="sxs-lookup"><span data-stu-id="95287-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="95287-115">Par conséquent, si vous met à jour l’indicateur de progression, n’a lieu aucune modification avant au moins quatre secondes après le lancement de l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="95287-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="95287-116">Cela permet de gagner du temps dans les cas courants où l’opération est rapide et d’informer les utilisateurs en temps voulu lorsque l’opération est lente.</span><span class="sxs-lookup"><span data-stu-id="95287-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

