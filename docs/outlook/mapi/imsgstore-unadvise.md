---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 72a26875802b2b7f94261f11e78fe560e9cc49d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583427"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="bd0ca-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="bd0ca-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="bd0ca-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd0ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd0ca-105">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="bd0ca-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bd0ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd0ca-106">Parameters</span></span>

 <span data-ttu-id="bd0ca-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="bd0ca-107">_ulConnection_</span></span>
  
> <span data-ttu-id="bd0ca-108">[in] Le numéro de connexion associé à un enregistrement de notification actif.</span><span class="sxs-lookup"><span data-stu-id="bd0ca-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="bd0ca-109">La valeur de _ulConnection_ doit avoir été renvoyée par un appel précédent à la méthode **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="bd0ca-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bd0ca-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bd0ca-110">Return value</span></span>

<span data-ttu-id="bd0ca-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd0ca-111">S_OK</span></span> 
  
> <span data-ttu-id="bd0ca-112">L’enregistrement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="bd0ca-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd0ca-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd0ca-113">Remarks</span></span>

<span data-ttu-id="bd0ca-114">La méthode **IMsgStore::Unadvise** annule une inscription pour la notification.</span><span class="sxs-lookup"><span data-stu-id="bd0ca-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="bd0ca-115">Versions **Unadvise** récepteur, à laquelle il a reçu l’appel **Advise** utilisées pour l’inscription de notification de son pointeur vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="bd0ca-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="bd0ca-116">En règle générale, **Unadvise** appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du récepteur advise pendant l’appel **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="bd0ca-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="bd0ca-117">Toutefois, si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="bd0ca-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd0ca-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd0ca-118">See also</span></span>



[<span data-ttu-id="bd0ca-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bd0ca-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bd0ca-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="bd0ca-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="bd0ca-121">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bd0ca-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

