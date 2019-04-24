---
title: Report de traitement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336931"
---
# <a name="deferring-processing"></a><span data-ttu-id="cee92-103">Report de traitement</span><span class="sxs-lookup"><span data-stu-id="cee92-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="cee92-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cee92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cee92-105">TransMettez l'indicateur MAPI_DEFERRED_ERRORS aux appels de méthode autant que possible.</span><span class="sxs-lookup"><span data-stu-id="cee92-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="cee92-106">De nombreux appels de méthode MAPI ont été optimisés pour accepter cet indicateur, ce qui a pour effet de reporter la tâche demandée jusqu'à ce que plusieurs tâches puissent être exécutées en même temps ou que vous ne puissiez plus attendre les résultats.</span><span class="sxs-lookup"><span data-stu-id="cee92-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="cee92-107">Par exemple, si vous transmettez MAPI_DEFERRED_ERRORS à [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir un dossier, l'ouverture du dossier et un éventuel appel distant peut être repoussé jusqu'à ce que vous appeliez un autre appel au **GetHierarchyTable** du dossier ou \*\* Méthodes GetProps\*\* .</span><span class="sxs-lookup"><span data-stu-id="cee92-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="cee92-108">**GetHierarchyTable** et **GetProps** requièrent le retour de données du fournisseur de services, une tâche qui doit être exécutée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="cee92-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="cee92-109">Un autre moyen de différer le traitement est simplement de ne pas passer un appel.</span><span class="sxs-lookup"><span data-stu-id="cee92-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="cee92-110">En étant conscient de l'utilisateur et lorsque l'utilisateur peut percevoir une décharge sur les ressources ou le temps de traitement, vous pouvez déterminer quand il est judicieux d'effectuer des appels.</span><span class="sxs-lookup"><span data-stu-id="cee92-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="cee92-111">Il est possible d'améliorer les performances en effectuant des appels à la fois lorsque l'utilisateur ne les remarquera pas ou en ne les apportant pas du tout.</span><span class="sxs-lookup"><span data-stu-id="cee92-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="cee92-112">Par exemple, considérez la situation lorsque vous recevez plusieurs notifications par seconde d'une banque de messages qui déplace un grand nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="cee92-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="cee92-113">Un indicateur de progression s'affiche pour indiquer le pourcentage d'achèvement de l'opération.</span><span class="sxs-lookup"><span data-stu-id="cee92-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="cee92-114">En règle générale, les utilisateurs ne considèrent pas que cette opération est lente avant que quelques secondes ne se soient écoulées.</span><span class="sxs-lookup"><span data-stu-id="cee92-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="cee92-115">Par conséquent, si vous mettez à jour l'indicateur de progression, n'effectuez aucune modification pendant au moins quatre secondes après l'initialisation de l'opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="cee92-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="cee92-116">Cela permet de gagner du temps dans les cas courants où l'opération est rapide et d'informer les utilisateurs en temps opportun lorsque l'opération est lente.</span><span class="sxs-lookup"><span data-stu-id="cee92-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

