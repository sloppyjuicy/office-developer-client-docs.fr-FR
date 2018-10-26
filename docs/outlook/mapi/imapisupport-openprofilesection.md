---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2e1f546d33d4781f60df56b12fce437d1e7bd675
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588222"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="8f52f-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8f52f-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="8f52f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f52f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f52f-105">Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="8f52f-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="8f52f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f52f-106">Parameters</span></span>

 <span data-ttu-id="8f52f-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="8f52f-107">_lpUid_</span></span>
  
> <span data-ttu-id="8f52f-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section profil à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="8f52f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="8f52f-109">Passage de NULL pour le paramètre _lpUid_ ouvre la section profil de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8f52f-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="8f52f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f52f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8f52f-111">[in] Masque de bits d’indicateurs qui contrôle le mode d’ouverture de la section de profil.</span><span class="sxs-lookup"><span data-stu-id="8f52f-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="8f52f-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="8f52f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="8f52f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8f52f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8f52f-114">Permet **OpenProfileSection** retournée correctement, éventuellement avant le profil de section est accessible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8f52f-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="8f52f-115">Si la section profil n’est pas accessible, passer un appel d’objet suivantes permettre provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="8f52f-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="8f52f-116">N'</span><span class="sxs-lookup"><span data-stu-id="8f52f-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8f52f-117">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8f52f-117">Requests read/write permission.</span></span> <span data-ttu-id="8f52f-118">Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler sur l’hypothèse que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8f52f-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="8f52f-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="8f52f-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="8f52f-120">[out] Pointeur vers un pointeur vers la section profil ouvert.</span><span class="sxs-lookup"><span data-stu-id="8f52f-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f52f-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8f52f-121">Return value</span></span>

<span data-ttu-id="8f52f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f52f-122">S_OK</span></span> 
  
> <span data-ttu-id="8f52f-123">La section profil a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="8f52f-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="8f52f-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8f52f-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8f52f-125">Une tentative a été effectuée pour modifier une section de profil en lecture seule ou pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="8f52f-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="8f52f-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8f52f-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8f52f-127">Il n’est pas une section de profil associée à l’identificateur d’entrée passé _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="8f52f-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="8f52f-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8f52f-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="8f52f-129">Indicateurs réservés ou non prises en charge ont été utilisés et, par conséquent, l’opération ne s’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="8f52f-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f52f-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f52f-130">Remarks</span></span>

<span data-ttu-id="8f52f-131">La méthode **IMAPISupport::OpenProfileSection** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8f52f-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="8f52f-132">Fournisseurs de services et les services de messagerie d’appel **OpenProfileSection** pour ouvrir une section de profil et de récupérer un pointeur vers son implémentation d’interface **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="8f52f-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8f52f-133">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="8f52f-133">Notes to callers</span></span>

 <span data-ttu-id="8f52f-134">**OpenProfileSection** ouvre sections profil en lecture seule, sauf si vous définissez l’indicateur ne dans le paramètre _ulFlags_ et votre autorisation est suffisante.</span><span class="sxs-lookup"><span data-stu-id="8f52f-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="8f52f-135">Définition de cet indicateur ne garantit pas l’autorisation de lecture/écriture ; les autorisations qui vous sont accordées dépendent de votre niveau d’accès et de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f52f-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="8f52f-136">Si **OpenProfileSection** tente d’ouvrir une section de profil inexistant en lecture seule, elle renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="8f52f-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="8f52f-137">Si **OpenProfileSection** tente d’ouvrir une section de profil inexistant en lecture-écriture, il crée la section profil et retourne le pointeur **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="8f52f-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f52f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f52f-138">See also</span></span>



[<span data-ttu-id="8f52f-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f52f-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8f52f-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8f52f-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="8f52f-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8f52f-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8f52f-142">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f52f-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

