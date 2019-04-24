---
title: Chronométrage d'une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360395"
---
# <a name="timing-a-notification"></a><span data-ttu-id="3dc3a-103">Chronométrage d'une notification</span><span class="sxs-lookup"><span data-stu-id="3dc3a-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="3dc3a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dc3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dc3a-105">Étant donné que la notification d'événement est un processus asynchrone, vous pouvez être notifié à tout moment, pas nécessairement immédiatement après la survenue de l'événement.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="3dc3a-106">Le moment des appels à votre méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) varie en fonction du fournisseur de services qui implémente la source de notification.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="3dc3a-107">Les fournisseurs de services peuvent informer votre client:</span><span class="sxs-lookup"><span data-stu-id="3dc3a-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="3dc3a-108">En même temps que l'événement.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="3dc3a-109">Directement après l'événement.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-109">Directly after the event.</span></span>
    
- <span data-ttu-id="3dc3a-110">À un moment ultérieur, après l'événement, éventuellement après \*\*\*\* un appel Unadvise.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="3dc3a-111">La plupart des fournisseurs de services appellent **OnNotify** après que la méthode MAPI responsable de l'événement a renvoyé à son appelant.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="3dc3a-112">Par exemple, les notifications sur les messages sont envoyées lorsque les modifications apportées au message sont enregistrées, après l'appel de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , ou lorsque le message est libéré, après l'appel **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="3dc3a-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="3dc3a-113">Tant que la notification n'est pas envoyée, aucune modification n'est visible dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="3dc3a-114">Vous pouvez recevoir des notifications à partir d'une source d' \*\*\*\* avis une fois que vous avez appelé Unadvise pour annuler une inscription.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="3dc3a-115">N'oubliez pas de libérer votre récepteur d'avertissement une fois que son nombre de références est tombé à zéro, \*\*\*\* et non à la suite d'un appel Unadvise réussi.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="3dc3a-116">Ne partez pas du principe que vous \*\*\*\* avez appelé Unadvise que le récepteur de notification n'est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3dc3a-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

