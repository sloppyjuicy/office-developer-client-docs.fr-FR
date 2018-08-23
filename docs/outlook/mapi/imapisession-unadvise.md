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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3b582b48773b9f6f1a6f46f9c0e4c6dcb9782b86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592065"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="725e1-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="725e1-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="725e1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="725e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="725e1-105">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMAPISession::Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="725e1-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="725e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="725e1-106">Parameters</span></span>

 <span data-ttu-id="725e1-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="725e1-107">_ulConnection_</span></span>
  
> <span data-ttu-id="725e1-108">[in] Un numéro de connexion associé à un enregistrement de notification actif.</span><span class="sxs-lookup"><span data-stu-id="725e1-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="725e1-109">La valeur de _ulConnection_ doit avoir été renvoyée par un appel précédent à **IMAPISession::Advise**.</span><span class="sxs-lookup"><span data-stu-id="725e1-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="725e1-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="725e1-110">Return value</span></span>

<span data-ttu-id="725e1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="725e1-111">S_OK</span></span> 
  
> <span data-ttu-id="725e1-112">L’enregistrement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="725e1-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="725e1-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="725e1-113">Remarks</span></span>

<span data-ttu-id="725e1-114">La méthode **IMAPISession::Unadvise** annule une inscription pour la notification.</span><span class="sxs-lookup"><span data-stu-id="725e1-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="725e1-115">Versions **Unadvise** récepteur, à laquelle il a reçu l’appel **Advise** utilisées pour l’inscription de notification de son pointeur vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="725e1-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="725e1-116">En règle générale, **Unadvise** appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du récepteur advise pendant l’appel **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="725e1-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="725e1-117">Toutefois, si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="725e1-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="725e1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="725e1-118">See also</span></span>



[<span data-ttu-id="725e1-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="725e1-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="725e1-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="725e1-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="725e1-121">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="725e1-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

