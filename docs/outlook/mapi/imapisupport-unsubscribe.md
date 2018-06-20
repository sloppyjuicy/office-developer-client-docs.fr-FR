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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784056"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="138a2-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="138a2-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="138a2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="138a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="138a2-105">Annule la responsabilité de l’envoi de notifications précédemment établie par un appel à la méthode [IMAPISupport::Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="138a2-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="138a2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="138a2-106">Parameters</span></span>

 <span data-ttu-id="138a2-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="138a2-107">_ulConnection_</span></span>
  
> <span data-ttu-id="138a2-108">[in] Le numéro de connexion différente de zéro qui représente l’enregistrement de notification précédemment établie par le biais de **IMAPISupport::Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="138a2-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="138a2-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="138a2-109">Return value</span></span>

<span data-ttu-id="138a2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="138a2-110">S_OK</span></span> 
  
> <span data-ttu-id="138a2-111">L’inscription de notification a été annulée.</span><span class="sxs-lookup"><span data-stu-id="138a2-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="138a2-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="138a2-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="138a2-113">Le numéro de connexion passé dans le paramètre _ulConnection_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="138a2-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="138a2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="138a2-114">Remarks</span></span>

<span data-ttu-id="138a2-115">La méthode **IMAPISupport::Unsubscribe** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="138a2-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="138a2-116">Fournisseurs de services d’appel **désabonnement** pour annuler un enregistrement de notification précédemment configuré par **abonnement**.</span><span class="sxs-lookup"><span data-stu-id="138a2-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="138a2-117">**Annuler l’abonnement** annule l’inscription en libérant le pointeur du récepteur advise passé dans l’appel de **s’abonner** .</span><span class="sxs-lookup"><span data-stu-id="138a2-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="138a2-118">En règle générale, méthode de **IUnknown::Release** du récepteur advise est appelé pendant l’appel de **désabonnement** .</span><span class="sxs-lookup"><span data-stu-id="138a2-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="138a2-119">Toutefois, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="138a2-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="138a2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="138a2-120">See also</span></span>



[<span data-ttu-id="138a2-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="138a2-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="138a2-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="138a2-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="138a2-123">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="138a2-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

