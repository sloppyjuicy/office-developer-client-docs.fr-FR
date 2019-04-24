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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317282"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="af4b5-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="af4b5-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="af4b5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af4b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af4b5-105">Ouvre un objet Folder ou message et renvoie un pointeur vers l'objet pour fournir un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="af4b5-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="af4b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af4b5-106">Parameters</span></span>

 <span data-ttu-id="af4b5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="af4b5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="af4b5-108">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="af4b5-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="af4b5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="af4b5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="af4b5-110">dans Pointeur vers l'adresse de l'identificateur d'entrée du dossier ou de l'objet de message à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="af4b5-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="af4b5-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="af4b5-111">_lpInterface_</span></span>
  
> <span data-ttu-id="af4b5-112">dans Pointeur vers l'identificateur d'interface (IID) de l'objet.</span><span class="sxs-lookup"><span data-stu-id="af4b5-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="af4b5-113">La transmission de la valeur NULL indique que l'objet est casté en interface standard pour ce type d'objet.</span><span class="sxs-lookup"><span data-stu-id="af4b5-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="af4b5-114">Le paramètre _lpInterface_ peut également être défini sur un identificateur pour une interface appropriée pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="af4b5-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="af4b5-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="af4b5-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="af4b5-116">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet.</span><span class="sxs-lookup"><span data-stu-id="af4b5-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="af4b5-117">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="af4b5-117">The following flags can be set:</span></span>
    
<span data-ttu-id="af4b5-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="af4b5-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="af4b5-119">L'objet doit être ouvert avec les autorisations maximales accordées à l'utilisateur et les autorisations d'application client maximales.</span><span class="sxs-lookup"><span data-stu-id="af4b5-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="af4b5-120">Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet est ouvert avec une autorisation en lecture/écriture; Si le client dispose d'une autorisation en lecture seule, l'objet est ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="af4b5-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="af4b5-121">Le client peut récupérer le niveau d'autorisation en obtenant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="af4b5-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="af4b5-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="af4b5-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="af4b5-123">L'appel est autorisé même si l'objet sous-jacent n'est pas disponible pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="af4b5-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="af4b5-124">Si l'objet n'est pas disponible, un appel ultérieur à l'objet peut renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="af4b5-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="af4b5-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="af4b5-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="af4b5-126">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="af4b5-126">Requests read/write permission.</span></span> <span data-ttu-id="af4b5-127">Par défaut, les objets sont créés avec l'autorisation lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée.</span><span class="sxs-lookup"><span data-stu-id="af4b5-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="af4b5-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="af4b5-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="af4b5-129">remarquer Pointeur vers le type de l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="af4b5-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="af4b5-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="af4b5-130">_lppUnk_</span></span>
  
> <span data-ttu-id="af4b5-131">remarquer Pointeur vers le pointeur vers l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="af4b5-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af4b5-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af4b5-132">Return value</span></span>

<span data-ttu-id="af4b5-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="af4b5-133">S_OK</span></span> 
  
> <span data-ttu-id="af4b5-134">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="af4b5-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af4b5-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="af4b5-135">Remarks</span></span>

<span data-ttu-id="af4b5-136">MAPI appelle la méthode **IMSLogon:: OpenEntry** pour ouvrir un dossier ou un message dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="af4b5-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="af4b5-137">MAPI transmet l'identificateur d'entrée de l'objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="af4b5-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="af4b5-138">Le fournisseur de banque de messages doit renvoyer un pointeur qui permet un accès supplémentaire à l'objet spécifié dans le paramètre _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="af4b5-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="af4b5-139">Avant que MAPI appelle **IMSLogon:: OpenEntry**, il détermine d'abord que l'identificateur d'entrée de dossier ou de message donné correspond à l'un des éléments inscrits par ce fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="af4b5-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="af4b5-140">Pour plus d'informations sur la façon dont les fournisseurs de magasins inscrivent les identificateurs d'entrée, voir [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="af4b5-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="af4b5-141">**IMSLogon:: OpenEntry** est identique à la méthode [IMsgStore:: OpenEntry](imsgstore-openentry.md) de l'objet de banque de messages, sauf que le client n'appelle pas **IMSLogon:: OpenEntry**; MAPI appelle **IMSLogon:: OpenEntry** lorsqu'il traite une méthode **IMAPISession:: OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="af4b5-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="af4b5-142">Les objets ouverts à l'aide de **IMSLogon:: OpenEntry** doivent être traités exactement de la même façon que les objets ouverts à l'aide de l'objet de banque de messages; en particulier, les objets ouverts à l'aide de cet appel doivent être invalidés lors de la publication de l'objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="af4b5-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af4b5-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af4b5-143">See also</span></span>



[<span data-ttu-id="af4b5-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="af4b5-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="af4b5-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="af4b5-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="af4b5-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af4b5-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

