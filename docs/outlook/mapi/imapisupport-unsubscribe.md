---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421213"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="7d211-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="7d211-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="7d211-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d211-105">Annule la responsabilité de l’envoi de notifications précédemment établies avec un appel à la méthode [IMAPISupport::Subscribe.](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="7d211-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7d211-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d211-106">Parameters</span></span>

 <span data-ttu-id="7d211-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="7d211-107">_ulConnection_</span></span>
  
> <span data-ttu-id="7d211-108">[in] Numéro de connexion autre que zéro qui représente l’inscription de notification précédemment établie via **IMAPISupport::Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="7d211-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d211-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7d211-109">Return value</span></span>

<span data-ttu-id="7d211-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d211-110">S_OK</span></span> 
  
> <span data-ttu-id="7d211-111">L’inscription de la notification a été annulée.</span><span class="sxs-lookup"><span data-stu-id="7d211-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="7d211-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7d211-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7d211-113">Le numéro de connexion transmis dans le  _paramètre ulConnection_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="7d211-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7d211-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d211-114">Remarks</span></span>

<span data-ttu-id="7d211-115">La **méthode IMAPISupport::Unsubscribe** est implémentée pour tous les objets de support du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7d211-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="7d211-116">Les fournisseurs de services **appellent Unsubscribe** pour annuler une inscription de notification précédemment définie par **Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="7d211-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="7d211-117">**Annuler l’abonnement annule** l’inscription en libérant le pointeur de sink de conseil transmis dans **l’appel d’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="7d211-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="7d211-118">En règle générale, la méthode **IUnknown::Release** du sink de conseil est appelée pendant l’appel **de désabonnement.**</span><span class="sxs-lookup"><span data-stu-id="7d211-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="7d211-119">Toutefois, si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de sink de conseil, l’appel de publication est différé jusqu’à ce que la méthode **OnNotify** renvoie. </span><span class="sxs-lookup"><span data-stu-id="7d211-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d211-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d211-120">See also</span></span>



[<span data-ttu-id="7d211-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7d211-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7d211-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="7d211-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="7d211-123">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d211-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

