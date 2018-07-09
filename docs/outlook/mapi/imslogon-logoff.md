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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5d9a57cee371675493ba71b2df52b83941d34fc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784308"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="06ec3-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="06ec3-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="06ec3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06ec3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06ec3-105">Fournisseur de magasins de journaux d’un message.</span><span class="sxs-lookup"><span data-stu-id="06ec3-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="06ec3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06ec3-106">Parameters</span></span>

 <span data-ttu-id="06ec3-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="06ec3-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="06ec3-108">[in] Réservé ; doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="06ec3-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06ec3-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="06ec3-109">Return value</span></span>

<span data-ttu-id="06ec3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="06ec3-110">S_OK</span></span> 
  
> <span data-ttu-id="06ec3-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="06ec3-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06ec3-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="06ec3-112">Remarks</span></span>

<span data-ttu-id="06ec3-113">Fournisseurs de banque de messages implémentent la méthode **IMSLogon::Logoff** pour forcer l’arrêt un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="06ec3-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="06ec3-114">**IMSLogon::Logoff** est appelée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="06ec3-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="06ec3-115">Alors que MAPI se déconnecte un client après un appel à la méthode [IMAPISession::Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="06ec3-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="06ec3-116">Alors que MAPI se déconnecte un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="06ec3-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="06ec3-117">Dans ce cas, **IMSLogon::Logoff** est appelée dans le cadre de MAPI de traitement de la méthode [IUnknown::Release](http://msdn.microsoft.com/fr-fr/library/ms682317%28v=VS.85%29.aspx) de l’objet de prise en charge créés par le fournisseur de banque de messages pendant le traitement d’un [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou un **IUnknown :: Version** appel de méthode sur un objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="06ec3-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](http://msdn.microsoft.com/fr-fr/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="06ec3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06ec3-118">See also</span></span>



[<span data-ttu-id="06ec3-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="06ec3-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="06ec3-120">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06ec3-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="06ec3-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="06ec3-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="06ec3-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="06ec3-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="06ec3-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="06ec3-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="06ec3-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06ec3-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

