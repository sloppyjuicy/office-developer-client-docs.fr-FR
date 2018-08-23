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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e72c947a6e0d4052d3335c3e3cfaf5ffb94da669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593003"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="f9439-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="f9439-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="f9439-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9439-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9439-105">Fournisseur de magasins de journaux d’un message.</span><span class="sxs-lookup"><span data-stu-id="f9439-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f9439-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9439-106">Parameters</span></span>

 <span data-ttu-id="f9439-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9439-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f9439-108">[in] Réservé ; doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="f9439-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9439-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f9439-109">Return value</span></span>

<span data-ttu-id="f9439-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9439-110">S_OK</span></span> 
  
> <span data-ttu-id="f9439-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f9439-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9439-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9439-112">Remarks</span></span>

<span data-ttu-id="f9439-113">Fournisseurs de banque de messages implémentent la méthode **IMSLogon::Logoff** pour forcer l’arrêt un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="f9439-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="f9439-114">**IMSLogon::Logoff** est appelée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9439-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="f9439-115">Alors que MAPI se déconnecte un client après un appel à la méthode [IMAPISession::Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="f9439-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="f9439-116">Alors que MAPI se déconnecte un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="f9439-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="f9439-117">Dans ce cas, **IMSLogon::Logoff** est appelée dans le cadre de MAPI de traitement de la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) de l’objet de prise en charge créés par le fournisseur de banque de messages pendant le traitement d’un [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou un **IUnknown :: Version** appel de méthode sur un objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f9439-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f9439-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9439-118">See also</span></span>



[<span data-ttu-id="f9439-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="f9439-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="f9439-120">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9439-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="f9439-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="f9439-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="f9439-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="f9439-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="f9439-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f9439-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f9439-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9439-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

