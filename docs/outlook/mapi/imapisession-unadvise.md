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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 25f80ddce60ab5a8966a62761d234accafbb54be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783957"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="f3e6c-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f3e6c-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="f3e6c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3e6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3e6c-105">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMAPISession::Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e6c-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f3e6c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3e6c-106">Parameters</span></span>

 <span data-ttu-id="f3e6c-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="f3e6c-107">_ulConnection_</span></span>
  
> <span data-ttu-id="f3e6c-108">[in] Un numéro de connexion associé à un enregistrement de notification actif.</span><span class="sxs-lookup"><span data-stu-id="f3e6c-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="f3e6c-109">La valeur de _ulConnection_ doit avoir été renvoyée par un appel précédent à **IMAPISession::Advise**.</span><span class="sxs-lookup"><span data-stu-id="f3e6c-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3e6c-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f3e6c-110">Return value</span></span>

<span data-ttu-id="f3e6c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3e6c-111">S_OK</span></span> 
  
> <span data-ttu-id="f3e6c-112">L’enregistrement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="f3e6c-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3e6c-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3e6c-113">Remarks</span></span>

<span data-ttu-id="f3e6c-114">La méthode **IMAPISession::Unadvise** annule une inscription pour la notification.</span><span class="sxs-lookup"><span data-stu-id="f3e6c-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="f3e6c-115">Versions **Unadvise** récepteur, à laquelle il a reçu l’appel **Advise** utilisées pour l’inscription de notification de son pointeur vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f3e6c-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="f3e6c-116">En règle générale, **Unadvise** appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du récepteur advise pendant l’appel **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="f3e6c-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="f3e6c-117">Toutefois, si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="f3e6c-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3e6c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3e6c-118">See also</span></span>



[<span data-ttu-id="f3e6c-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f3e6c-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f3e6c-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="f3e6c-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="f3e6c-121">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3e6c-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

