---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317275"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="c7e47-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c7e47-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="c7e47-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7e47-105">Supprime l'inscription d'un objet pour la notification des modifications de banque de messages précédemment établies à l'aide d'un appel à la méthode [IMSLogon:: Advise](imslogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e47-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c7e47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7e47-106">Parameters</span></span>

 <span data-ttu-id="c7e47-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="c7e47-107">_ulConnection_</span></span>
  
> <span data-ttu-id="c7e47-108">dans Numéro de la connexion d'inscription renvoyée par un appel à **IMSLogon:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="c7e47-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7e47-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7e47-109">Return value</span></span>

<span data-ttu-id="c7e47-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7e47-110">S_OK</span></span> 
  
> <span data-ttu-id="c7e47-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c7e47-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7e47-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7e47-112">Remarks</span></span>

<span data-ttu-id="c7e47-113">Les fournisseurs de banque de messages implémentent la méthode **IMSLogon::** Unadvise pour libérer le pointeur vers l'objet de récepteur de notifications transmis dans le paramètre _lpAdviseSink_ dans l'appel précédent à **IMSLogon:: Advise**, ce qui a pour effet d'annuler une notification. son.</span><span class="sxs-lookup"><span data-stu-id="c7e47-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="c7e47-114">Dans le cadre du rejet du pointeur vers l'objet de récepteur de notification, la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l'objet est appelée.</span><span class="sxs-lookup"><span data-stu-id="c7e47-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="c7e47-115">En règle générale, la **publication** est appelée pendant l'appel Unadvise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c7e47-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="c7e47-116">Toutefois, si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet de récepteur de notifications, l'appel de **libération** est retardé jusqu'à ce que la méthode **OnNotify** soit renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c7e47-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7e47-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7e47-117">See also</span></span>



[<span data-ttu-id="c7e47-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c7e47-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c7e47-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="c7e47-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="c7e47-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7e47-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

