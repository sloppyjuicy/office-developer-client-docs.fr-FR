---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335699"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="683b1-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="683b1-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="683b1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="683b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="683b1-105">Annule l'envoi de notifications précédemment configurées avec un appel à la méthode [IMAPISession:: Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="683b1-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="683b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="683b1-106">Parameters</span></span>

 <span data-ttu-id="683b1-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="683b1-107">_ulConnection_</span></span>
  
> <span data-ttu-id="683b1-108">dans Numéro de connexion associé à un enregistrement de notifications actif.</span><span class="sxs-lookup"><span data-stu-id="683b1-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="683b1-109">La valeur de _ulConnection_ doit avoir été renvoyée par un appel précédent à **IMAPISession:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="683b1-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="683b1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="683b1-110">Return value</span></span>

<span data-ttu-id="683b1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="683b1-111">S_OK</span></span> 
  
> <span data-ttu-id="683b1-112">L'inscription a été annulée.</span><span class="sxs-lookup"><span data-stu-id="683b1-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="683b1-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="683b1-113">Remarks</span></span>

<span data-ttu-id="683b1-114">La méthode **IMAPISession::** Unadvise annule une inscription pour la notification.</span><span class="sxs-lookup"><span data-stu-id="683b1-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="683b1-115">\*\*\*\* Unadvise libère son pointeur vers le récepteur de notification de l'appelant, qu'il a reçu dans l'appel de **notification** utilisé pour l'inscription.</span><span class="sxs-lookup"><span data-stu-id="683b1-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="683b1-116">En règle \*\*\*\* générale, Unadvise appelle la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du récepteur de notification lors de l'appel Unadvise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="683b1-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="683b1-117">Toutefois, si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification, l'appel de la **libération** est retardé jusqu'à ce que la méthode **OnNotify** soit renvoyée.</span><span class="sxs-lookup"><span data-stu-id="683b1-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="683b1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="683b1-118">See also</span></span>



[<span data-ttu-id="683b1-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="683b1-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="683b1-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="683b1-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="683b1-121">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="683b1-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

