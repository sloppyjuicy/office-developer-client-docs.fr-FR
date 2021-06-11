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
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411385"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="ba376-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ba376-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="ba376-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba376-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba376-105">Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ba376-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="ba376-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ba376-106">Parameters</span></span>

 <span data-ttu-id="ba376-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="ba376-107">_lpUid_</span></span>
  
> <span data-ttu-id="ba376-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ba376-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="ba376-109">La transmission de la valeur NULL  _pour le paramètre lpUid_ ouvre la section de profil de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ba376-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="ba376-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ba376-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ba376-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont la section de profil est ouverte.</span><span class="sxs-lookup"><span data-stu-id="ba376-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="ba376-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="ba376-112">The following flags can be set:</span></span>
    
<span data-ttu-id="ba376-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ba376-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ba376-114">Permet à **OpenProfileSection** de renvoyer correctement, éventuellement avant que la section de profil ne soit entièrement accessible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ba376-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="ba376-115">Si la section de profil n’est pas accessible, un appel d’objet ultérieur peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="ba376-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="ba376-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ba376-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ba376-117">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ba376-117">Requests read/write permission.</span></span> <span data-ttu-id="ba376-118">Par défaut, les objets sont ouverts en lecture seule et les appelants ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture a été accordée.</span><span class="sxs-lookup"><span data-stu-id="ba376-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="ba376-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="ba376-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="ba376-120">[out] Pointeur vers un pointeur vers la section de profil ouverte.</span><span class="sxs-lookup"><span data-stu-id="ba376-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba376-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ba376-121">Return value</span></span>

<span data-ttu-id="ba376-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba376-122">S_OK</span></span> 
  
> <span data-ttu-id="ba376-123">La section profil a été ouverte avec succès.</span><span class="sxs-lookup"><span data-stu-id="ba376-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="ba376-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ba376-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ba376-125">Une tentative de modification d’une section de profil en lecture seule ou d’accès à un objet pour lequel l’appelant dispose d’autorisations insuffisantes a été tentée.</span><span class="sxs-lookup"><span data-stu-id="ba376-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="ba376-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ba376-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ba376-127">Il n’existe pas de section de profil associée à l’identificateur d’entrée transmis  _dans lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="ba376-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="ba376-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ba376-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="ba376-129">Des indicateurs réservés ou non pris en cas d’utilisation ont été utilisés et, par conséquent, l’opération n’a pas été achevée.</span><span class="sxs-lookup"><span data-stu-id="ba376-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba376-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba376-130">Remarks</span></span>

<span data-ttu-id="ba376-131">La **méthode IMAPISupport::OpenProfileSection** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ba376-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="ba376-132">Les fournisseurs de services et les services de messagerie appellent **OpenProfileSection** pour ouvrir une section de profil et récupérer un pointeur vers son implémentation d’interface **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="ba376-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ba376-133">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ba376-133">Notes to callers</span></span>

 <span data-ttu-id="ba376-134">**OpenProfileSection** ouvre les sections de profil en lecture seule, sauf si vous définissez l’indicateur MAPI_MODIFY dans le paramètre  _ulFlags_ et que votre autorisation est suffisante.</span><span class="sxs-lookup"><span data-stu-id="ba376-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="ba376-135">La définition de cet indicateur ne garantit pas l’autorisation de lecture/écriture . Les autorisations qui vous sont accordées dépendent de votre niveau d’accès et de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ba376-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="ba376-136">Si **OpenProfileSection** tente d’ouvrir une section de profil inexistante en lecture seule, elle renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="ba376-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="ba376-137">Si **OpenProfileSection** tente d’ouvrir une section de profil inexistante en lecture/écriture, il crée la section de profil et renvoie le pointeur **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="ba376-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ba376-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba376-138">See also</span></span>



[<span data-ttu-id="ba376-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba376-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ba376-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ba376-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="ba376-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ba376-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ba376-142">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba376-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

