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
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309722"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="b5dc5-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b5dc5-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="b5dc5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5dc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5dc5-105">Annule l’envoi de notifications précédemment définies avec un appel à la [méthode IMsgStore::Advise.](imsgstore-advise.md)</span><span class="sxs-lookup"><span data-stu-id="b5dc5-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b5dc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5dc5-106">Parameters</span></span>

 <span data-ttu-id="b5dc5-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="b5dc5-107">_ulConnection_</span></span>
  
> <span data-ttu-id="b5dc5-108">[in] Numéro de connexion associé à un enregistrement de notification actif.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="b5dc5-109">La valeur _de ulConnection_ doit avoir été renvoyée par un appel précédent à la **méthode IMsgStore::Advise.**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b5dc5-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5dc5-110">Return value</span></span>

<span data-ttu-id="b5dc5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5dc5-111">S_OK</span></span> 
  
> <span data-ttu-id="b5dc5-112">L’inscription a été annulée.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5dc5-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b5dc5-113">Remarks</span></span>

<span data-ttu-id="b5dc5-114">La **méthode IMsgStore::Unadvise** annule l’inscription à la notification.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="b5dc5-115">**Unadvise relâche** son pointeur vers le réception de conseil de l’appelant, qu’il a reçu dans l’appel **De** conseil utilisé pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="b5dc5-116">En règle **générale, Unadvise** appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du sink de conseil pendant l’appel **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="b5dc5-117">Toutefois, si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de conseil, l’appel de publication est différé jusqu’à ce que la méthode **OnNotify** soit de retour. </span><span class="sxs-lookup"><span data-stu-id="b5dc5-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5dc5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5dc5-118">See also</span></span>



[<span data-ttu-id="b5dc5-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b5dc5-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b5dc5-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="b5dc5-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="b5dc5-121">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b5dc5-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

