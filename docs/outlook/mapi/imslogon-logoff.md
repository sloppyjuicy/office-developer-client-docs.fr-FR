---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348873"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="f182c-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="f182c-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="f182c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f182c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f182c-105">DéConnecte un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f182c-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f182c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f182c-106">Parameters</span></span>

 <span data-ttu-id="f182c-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f182c-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f182c-108">dans MSR doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="f182c-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f182c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f182c-109">Return value</span></span>

<span data-ttu-id="f182c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f182c-110">S_OK</span></span> 
  
> <span data-ttu-id="f182c-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f182c-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f182c-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f182c-112">Remarks</span></span>

<span data-ttu-id="f182c-113">Les fournisseurs de banque de messages implémentent la méthode **IMSLogon:: Logoff** pour forcer l'arrêt d'un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f182c-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="f182c-114">**IMSLogon:: Logoff** est appelé dans les situations suivantes:</span><span class="sxs-lookup"><span data-stu-id="f182c-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="f182c-115">MAPI se déconnecte d'un client après un appel à la méthode [IMAPISession:: Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="f182c-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="f182c-116">MAPI se déconnecte d'un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f182c-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="f182c-117">Dans ce cas, **IMSLogon:: Logoff** est appelé dans le cadre du traitement MAPI de la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l'objet de prise en charge créé par le fournisseur de banque de messages pendant qu'il traite une [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) ou \*\*IUnknown:: \*\*Appel de la méthode Release sur un objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f182c-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f182c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f182c-118">See also</span></span>



[<span data-ttu-id="f182c-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="f182c-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="f182c-120">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f182c-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="f182c-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="f182c-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="f182c-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="f182c-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="f182c-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f182c-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f182c-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f182c-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

