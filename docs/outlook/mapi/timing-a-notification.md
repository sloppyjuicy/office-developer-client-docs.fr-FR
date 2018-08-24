---
title: Minutage d’une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4b0292ab16eabe30755fe84885a29fb8e3ce295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595194"
---
# <a name="timing-a-notification"></a><span data-ttu-id="8dfeb-103">Minutage d’une notification</span><span class="sxs-lookup"><span data-stu-id="8dfeb-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="8dfeb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dfeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dfeb-105">Notification d’événement étant un processus asynchrone, vous pouvez être averti à tout moment, pas nécessairement immédiatement après que l’événement s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="8dfeb-106">La durée des appels à votre méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varie selon le fournisseur de services l’implémentation de la source de notification.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="8dfeb-107">Fournisseurs de services peuvent informer votre client soit :</span><span class="sxs-lookup"><span data-stu-id="8dfeb-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="8dfeb-108">Simultanément avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="8dfeb-109">Directement après l’événement.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-109">Directly after the event.</span></span>
    
- <span data-ttu-id="8dfeb-110">À plus tard un moment donné à la suite de l’événement, éventuellement après un appel **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="8dfeb-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="8dfeb-111">La plupart des fournisseurs de services d’appel **OnNotify** après que la méthode MAPI responsable de l’événement a renvoyé à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="8dfeb-112">Par exemple, les notifications sur les messages sont envoyées lorsque des modifications apportées au message sont enregistrées, après l’appel de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , ou lorsque le message est lancé, après l’appel **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="8dfeb-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="8dfeb-113">Jusqu'à ce que la notification est envoyée, aucune modification n’est visible dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="8dfeb-114">Vous pouvez recevoir des notifications à partir d’une source advise après avoir appelé **Unadvise** pour annuler l’inscription d’une.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="8dfeb-115">Veillez à libérer votre récepteur de notifications qu’après que son décompte de références est réduit à zéro, un appel réussi de **Unadvise** ne pas suivant.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="8dfeb-116">Ne supposent que parce que vous avez appelé **Unadvise** le récepteur de notifications n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8dfeb-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

