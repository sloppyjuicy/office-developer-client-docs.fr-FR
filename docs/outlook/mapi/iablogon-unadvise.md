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
ms.openlocfilehash: 3fbf8b423cfd4206a0143b5639c85dbcacce2fae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570981"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="33578-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="33578-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="33578-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33578-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33578-105">Annule les notifications qui ont été précédemment configurées avec un appel à la méthode [IABLogon::Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="33578-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="33578-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33578-106">Parameters</span></span>

 <span data-ttu-id="33578-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="33578-107">_ulConnection_</span></span>
  
> <span data-ttu-id="33578-108">[in] Le numéro de connexion associé à un enregistrement de notification actif.</span><span class="sxs-lookup"><span data-stu-id="33578-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="33578-109">Un appel précédent à **Advise** doit renvoyer la valeur de la _classe ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="33578-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33578-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="33578-110">Return value</span></span>

<span data-ttu-id="33578-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="33578-111">S_OK</span></span> 
  
> <span data-ttu-id="33578-112">L’inscription de notification a été annulée.</span><span class="sxs-lookup"><span data-stu-id="33578-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33578-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="33578-113">Remarks</span></span>

<span data-ttu-id="33578-114">MAPI appelle la méthode **Unadvise** pour annuler un enregistrement de notification pour un conteneur, utilisateur ou objet liste de distribution de messagerie.</span><span class="sxs-lookup"><span data-stu-id="33578-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33578-115">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="33578-115">Notes to implementers</span></span>

<span data-ttu-id="33578-116">Votre implémentation de **Unadvise** varient selon que vous prenez en charge la notification manuellement ou à l’aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="33578-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="33578-117">Si MAPI propose votre prise en charge, appelez la méthode [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="33578-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="33578-118">Si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, elle peut être retardée jusqu'à ce que **OnNotify** a renvoyé.</span><span class="sxs-lookup"><span data-stu-id="33578-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="33578-119">Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="33578-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="33578-120">Pour plus d’informations sur l’utilisation de la [IMAPISupport : IUnknown](imapisupportiunknown.md) méthodes pour prendre en charge la notification, consultez [Prise en charge de Notification d’événement](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="33578-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33578-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33578-121">See also</span></span>



[<span data-ttu-id="33578-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="33578-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="33578-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="33578-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="33578-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33578-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

