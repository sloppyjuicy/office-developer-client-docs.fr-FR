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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4ee17799fc42faf383461af7eed9d700d17b868e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582384"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="a4db9-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a4db9-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="a4db9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4db9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4db9-105">Supprime l’inscription d’un objet pour la notification des modifications de banque de messages précédemment établie à l’aide d’un appel à la méthode [IMSLogon::Advise](imslogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="a4db9-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a4db9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4db9-106">Parameters</span></span>

 <span data-ttu-id="a4db9-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="a4db9-107">_ulConnection_</span></span>
  
> <span data-ttu-id="a4db9-108">[in] Le numéro de la connexion d’enregistrement renvoyé par un appel à **IMSLogon::Advise**.</span><span class="sxs-lookup"><span data-stu-id="a4db9-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4db9-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a4db9-109">Return value</span></span>

<span data-ttu-id="a4db9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4db9-110">S_OK</span></span> 
  
> <span data-ttu-id="a4db9-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a4db9-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4db9-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4db9-112">Remarks</span></span>

<span data-ttu-id="a4db9-113">La méthode **IMSLogon::Unadvise** pour libérer le pointeur vers l’objet de récepteur advise transmis dans le paramètre _lpAdviseSink_ dans l’appel précédent à **IMSLogon::Advise**, annulant ainsi une notification implémentés par les fournisseurs la base de messages inscription.</span><span class="sxs-lookup"><span data-stu-id="a4db9-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="a4db9-114">Dans le cadre d’ignorer le pointeur vers l’objet de récepteur advise, la méthode l’objet [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) est appelée.</span><span class="sxs-lookup"><span data-stu-id="a4db9-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="a4db9-115">En règle générale, la **version** est appelé pendant l’appel **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="a4db9-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="a4db9-116">Toutefois, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="a4db9-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4db9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4db9-117">See also</span></span>



[<span data-ttu-id="a4db9-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="a4db9-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="a4db9-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="a4db9-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="a4db9-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4db9-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

