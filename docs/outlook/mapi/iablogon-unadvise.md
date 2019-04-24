---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348880"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="e4040-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e4040-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="e4040-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4040-105">Annule les notifications précédemment configurées avec un appel à la méthode [IABLogon:: Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="e4040-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e4040-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4040-106">Parameters</span></span>

 <span data-ttu-id="e4040-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="e4040-107">_ulConnection_</span></span>
  
> <span data-ttu-id="e4040-108">dans Numéro de connexion associé à l'enregistrement de notifications actif.</span><span class="sxs-lookup"><span data-stu-id="e4040-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="e4040-109">Un appel précédent à **Advise** doit avoir renvoyé la valeur de _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="e4040-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4040-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4040-110">Return value</span></span>

<span data-ttu-id="e4040-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4040-111">S_OK</span></span> 
  
> <span data-ttu-id="e4040-112">L'inscription de la notification a été annulée.</span><span class="sxs-lookup"><span data-stu-id="e4040-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4040-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4040-113">Remarks</span></span>

<span data-ttu-id="e4040-114">MAPI appelle la \*\*\*\* méthode Unadvise pour annuler une inscription de notification pour un conteneur, un utilisateur de messagerie ou un objet de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="e4040-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e4040-115">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e4040-115">Notes to implementers</span></span>

<span data-ttu-id="e4040-116">L'implémentation de \*\*\*\* Unadvise varie selon que vous prenez en charge la notification avec l'aide de MAPI ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="e4040-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="e4040-117">Si MAPI fournit votre prise en charge, appelez la méthode [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) pour annuler l'inscription.</span><span class="sxs-lookup"><span data-stu-id="e4040-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="e4040-118">Si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification, il peut être retardé jusqu'à ce que **OnNotify** ait renvoyé.</span><span class="sxs-lookup"><span data-stu-id="e4040-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="e4040-119">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e4040-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="e4040-120">Pour plus d'informations sur l'utilisation des méthodes [IMAPISupport: IUnknown](imapisupportiunknown.md) pour prendre en charge la notification, consultez la rubrique [notification d'événement de prise en](supporting-event-notification.md)charge.</span><span class="sxs-lookup"><span data-stu-id="e4040-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4040-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4040-121">See also</span></span>



[<span data-ttu-id="e4040-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="e4040-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="e4040-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e4040-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="e4040-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4040-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

