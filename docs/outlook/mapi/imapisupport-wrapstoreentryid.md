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
ms.openlocfilehash: b3850da2917dbf463590643b9e7ba8420f4ea219
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576056"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="e49c4-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="e49c4-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="e49c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e49c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e49c4-105">Convertit un identificateur d’entrée dans le format standard MAPI identificateur d’entrée interne d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e49c4-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="e49c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e49c4-106">Parameters</span></span>

 <span data-ttu-id="e49c4-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="e49c4-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="e49c4-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpOrigEntry_ .</span><span class="sxs-lookup"><span data-stu-id="e49c4-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="e49c4-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="e49c4-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="e49c4-110">[in] Pointeur vers l’identificateur d’entrée privé pour la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e49c4-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="e49c4-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="e49c4-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="e49c4-112">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="e49c4-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="e49c4-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="e49c4-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="e49c4-114">[out] Pointeur vers un pointeur vers l’identificateur d’entrée justifiés.</span><span class="sxs-lookup"><span data-stu-id="e49c4-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e49c4-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e49c4-115">Return value</span></span>

<span data-ttu-id="e49c4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e49c4-116">S_OK</span></span> 
  
> <span data-ttu-id="e49c4-117">L’identificateur d’entrée a été correctement entourée.</span><span class="sxs-lookup"><span data-stu-id="e49c4-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e49c4-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="e49c4-118">Remarks</span></span>

<span data-ttu-id="e49c4-119">La méthode **IMAPISupport::WrapStoreEntryID** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="e49c4-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e49c4-120">Fournisseurs de services utilisent **WrapStoreEntryID** pour MAPI génère un identificateur d’entrée pour une banque de messages qui encapsule l’identificateur d’entrée interne du magasin.</span><span class="sxs-lookup"><span data-stu-id="e49c4-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e49c4-121">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="e49c4-121">Notes to callers</span></span>

<span data-ttu-id="e49c4-122">Lorsqu’un client appelle la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour extraire sa propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) et la banque de messages utilise un identificateur d’entrée dans un format privé, appelez **WrapStoreEntryID **et renvoyer l’identificateur d’entrée indiqué par le paramètre _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="e49c4-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="e49c4-123">Les appels vers les méthodes [IMSProvider::Logon](imsprovider-logon.md) et [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) obtenir toujours un identificateur d’entrée privé du magasin ; la version encapsulée est utilisée uniquement entre les applications clientes et MAPI.</span><span class="sxs-lookup"><span data-stu-id="e49c4-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="e49c4-124">Libérer de la mémoire pour l’identificateur d’entrée indiqué par le paramètre _lppWrappedEntry_ à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous avez terminé, à l’aide de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e49c4-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e49c4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e49c4-125">See also</span></span>



[<span data-ttu-id="e49c4-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e49c4-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="e49c4-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e49c4-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="e49c4-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e49c4-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="e49c4-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="e49c4-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="e49c4-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e49c4-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e49c4-131">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e49c4-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

