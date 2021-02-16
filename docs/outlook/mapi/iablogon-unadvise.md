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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424076"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="175f0-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="175f0-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="175f0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="175f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="175f0-105">Annule les notifications précédemment définies avec un appel à la [méthode IABLogon::Advise.](iablogon-advise.md)</span><span class="sxs-lookup"><span data-stu-id="175f0-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="175f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="175f0-106">Parameters</span></span>

 <span data-ttu-id="175f0-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="175f0-107">_ulConnection_</span></span>
  
> <span data-ttu-id="175f0-108">[in] Numéro de connexion associé à un enregistrement de notification actif.</span><span class="sxs-lookup"><span data-stu-id="175f0-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="175f0-109">Un appel précédent à **Advise** doit avoir renvoyé la valeur  _de ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="175f0-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="175f0-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="175f0-110">Return value</span></span>

<span data-ttu-id="175f0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="175f0-111">S_OK</span></span> 
  
> <span data-ttu-id="175f0-112">L’inscription de la notification a été annulée avec succès.</span><span class="sxs-lookup"><span data-stu-id="175f0-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="175f0-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="175f0-113">Remarks</span></span>

<span data-ttu-id="175f0-114">MAPI appelle la **méthode Unadvise** pour annuler l’inscription d’une notification pour un objet conteneur, utilisateur de messagerie ou liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="175f0-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="175f0-115">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="175f0-115">Notes to implementers</span></span>

<span data-ttu-id="175f0-116">Votre implémentation **d’Unadvise** dépend de la prise en charge de la notification avec l’aide de MAPI ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="175f0-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="175f0-117">Si MAPI fournit votre prise en charge, appelez la méthode [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="175f0-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="175f0-118">Si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de conseil, il peut être retardé jusqu’à ce que **OnNotify** soit renvoyé.</span><span class="sxs-lookup"><span data-stu-id="175f0-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="175f0-119">Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="175f0-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="175f0-120">Pour plus d’informations sur l’utilisation des méthodes [IMAPISupport : IUnknown](imapisupportiunknown.md) pour prendre en charge la notification, voir [Notification d’événement de prise en charge.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="175f0-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="175f0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="175f0-121">See also</span></span>



[<span data-ttu-id="175f0-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="175f0-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="175f0-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="175f0-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="175f0-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="175f0-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

