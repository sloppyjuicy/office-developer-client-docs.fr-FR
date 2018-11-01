---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 619357a608dd160cbe4811cc7db7ae3b392db858
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576889"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="334ba-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="334ba-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="334ba-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="334ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="334ba-105">Ouvre un dossier ou un objet de message et retourne un pointeur vers l’objet pour fournir un accès plus.</span><span class="sxs-lookup"><span data-stu-id="334ba-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="334ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="334ba-106">Parameters</span></span>

 <span data-ttu-id="334ba-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="334ba-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="334ba-108">[in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="334ba-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="334ba-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="334ba-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="334ba-110">[in] Pointeur vers l’adresse de l’identificateur d’entrée de l’objet de dossier ou un message à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="334ba-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="334ba-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="334ba-111">_lpInterface_</span></span>
  
> <span data-ttu-id="334ba-112">[in] Pointeur vers l’identificateur d’interface (IID) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="334ba-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="334ba-113">Valeur null indique que l’objet est convertie à l’interface standard pour ce type d’objet.</span><span class="sxs-lookup"><span data-stu-id="334ba-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="334ba-114">Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="334ba-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="334ba-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="334ba-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="334ba-116">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="334ba-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="334ba-117">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="334ba-117">The following flags can be set:</span></span>
    
<span data-ttu-id="334ba-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="334ba-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="334ba-119">L’objet doit être ouvert avec les autorisations maximales autorisées pour l’utilisateur et les autorisations d’application client maximale.</span><span class="sxs-lookup"><span data-stu-id="334ba-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="334ba-120">Par exemple, si le client a l’autorisation de lecture/écriture, l’objet est ouvert avec l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, l’objet est ouvert avec l’autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="334ba-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="334ba-121">Le client peut extraire le niveau d’autorisation en obtenant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="334ba-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="334ba-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="334ba-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="334ba-123">L’appel est autorisé à fonctionne même si l’objet sous-jacent n’est pas disponible pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="334ba-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="334ba-124">Si l’objet n’est pas disponible, un appel à l’objet suivant renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="334ba-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="334ba-125">N'</span><span class="sxs-lookup"><span data-stu-id="334ba-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="334ba-126">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="334ba-126">Requests read/write permission.</span></span> <span data-ttu-id="334ba-127">Par défaut, les objets sont créés avec l’autorisation en lecture seule, et les clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="334ba-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="334ba-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="334ba-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="334ba-129">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="334ba-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="334ba-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="334ba-130">_lppUnk_</span></span>
  
> <span data-ttu-id="334ba-131">[out] Pointeur vers le pointeur vers l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="334ba-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="334ba-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="334ba-132">Return value</span></span>

<span data-ttu-id="334ba-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="334ba-133">S_OK</span></span> 
  
> <span data-ttu-id="334ba-134">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="334ba-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="334ba-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="334ba-135">Remarks</span></span>

<span data-ttu-id="334ba-136">MAPI appelle la méthode **IMSLogon::OpenEntry** pour ouvrir un dossier ou un message dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="334ba-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="334ba-137">MAPI transmet l’identificateur d’entrée de l’objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="334ba-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="334ba-138">Le fournisseur de banque de message doit retourner un pointeur qui permet l’accès à l’objet spécifié dans le paramètre _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="334ba-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="334ba-139">Avant que les appels MAPI **IMSLogon::OpenEntry**, il détermine d’abord que le message donné ou l’identificateur d’entrée de dossier correspond à une enregistré par ce fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="334ba-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="334ba-140">Pour plus d’informations sur comment enregistrent des fournisseurs de magasins d’identificateurs d’entrée, voir [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="334ba-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="334ba-141">**IMSLogon::OpenEntry** est identique à la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) de l’objet store de message, sauf que le client n’appelle pas **IMSLogon::OpenEntry**; Les appels MAPI **IMSLogon::OpenEntry** lorsqu’il traite une méthode **IMAPISession::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="334ba-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="334ba-142">Objets ouverts à l’aide de **IMSLogon::OpenEntry** doivent être traités exactement comme objets ouverts en utilisant le message stockent l’objet ; en particulier, objets ouverts à l’aide de cet appel doivent être invalidés lors de l’objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="334ba-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="334ba-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="334ba-143">See also</span></span>



[<span data-ttu-id="334ba-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="334ba-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="334ba-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="334ba-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="334ba-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="334ba-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

