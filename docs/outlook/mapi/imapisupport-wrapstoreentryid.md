---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430447"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="6fb18-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="6fb18-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="6fb18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fb18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fb18-105">Convertit l’identificateur d’entrée interne d’une boutique de messages en identificateur d’entrée au format mapi standard.</span><span class="sxs-lookup"><span data-stu-id="6fb18-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="6fb18-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6fb18-106">Parameters</span></span>

 <span data-ttu-id="6fb18-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6fb18-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="6fb18-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpOrigEntry._</span><span class="sxs-lookup"><span data-stu-id="6fb18-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="6fb18-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6fb18-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="6fb18-110">[in] Pointeur vers l’identificateur d’entrée privée de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6fb18-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="6fb18-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6fb18-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="6fb18-112">[out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par _le paramètre lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="6fb18-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="6fb18-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6fb18-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="6fb18-114">[out] Pointeur vers un pointeur vers l’identificateur d’entrée wrapped.</span><span class="sxs-lookup"><span data-stu-id="6fb18-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fb18-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6fb18-115">Return value</span></span>

<span data-ttu-id="6fb18-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fb18-116">S_OK</span></span> 
  
> <span data-ttu-id="6fb18-117">L’identificateur d’entrée a été correctement wrapped.</span><span class="sxs-lookup"><span data-stu-id="6fb18-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fb18-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fb18-118">Remarks</span></span>

<span data-ttu-id="6fb18-119">La **méthode IMAPISupport::WrapStoreEntryID** est implémentée pour tous les objets de support du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="6fb18-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="6fb18-120">Les fournisseurs de services **utilisent WrapStoreEntryID** pour que MAPI génère un identificateur d’entrée pour une magasin de messages qui encapsule l’identificateur d’entrée interne de la boutique.</span><span class="sxs-lookup"><span data-stu-id="6fb18-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6fb18-121">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="6fb18-121">Notes to callers</span></span>

<span data-ttu-id="6fb18-122">Lorsqu’un client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de votre banque de messages pour récupérer sa propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)), et que votre banque de messages utilise un identificateur d’entrée dans un format privé, appelez **WrapStoreEntryID** et renvoyez l’identificateur d’entrée pointé par le paramètre _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="6fb18-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="6fb18-123">Les appels aux méthodes [IMSProvider::Logon](imsprovider-logon.md) et [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) obtiennent toujours l’identificateur d’entrée privée du magasin ; La version wrapped est utilisée uniquement entre les applications clientes et MAPI.</span><span class="sxs-lookup"><span data-stu-id="6fb18-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="6fb18-124">Libérez la mémoire de l’identificateur d’entrée pointé par le paramètre  _lppWrappedEntry_ à l’aide de la [fonction MAPIFreeBuffer](mapifreebuffer.md) lorsque vous avez terminé d’utiliser l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6fb18-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fb18-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fb18-125">See also</span></span>



[<span data-ttu-id="6fb18-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6fb18-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="6fb18-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6fb18-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="6fb18-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6fb18-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="6fb18-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="6fb18-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="6fb18-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6fb18-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6fb18-131">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fb18-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

