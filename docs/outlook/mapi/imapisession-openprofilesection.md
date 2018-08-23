---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568188"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="0c7ff-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0c7ff-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="0c7ff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c7ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c7ff-105">Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="0c7ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c7ff-106">Parameters</span></span>

 <span data-ttu-id="0c7ff-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0c7ff-107">_lpUID_</span></span>
  
> <span data-ttu-id="0c7ff-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="0c7ff-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0c7ff-109">_lpInterface_</span></span>
  
> <span data-ttu-id="0c7ff-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="0c7ff-111">Passage de NULL entraîne le paramètre _lppProfSect_ renvoyer un pointeur vers l’interface standard de la section de profil, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="0c7ff-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c7ff-112">_ulFlags_</span></span>
  
> <span data-ttu-id="0c7ff-113">[in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="0c7ff-114">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="0c7ff-114">The following flags can be set:</span></span>
    
<span data-ttu-id="0c7ff-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0c7ff-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0c7ff-116">Permet **OpenProfileSection** retournée correctement, éventuellement avant le profil de section est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="0c7ff-117">Si la section profil n’est pas disponible, vous appelez suivante lui peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0c7ff-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0c7ff-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="0c7ff-119">Permet d’accéder à une section de profil n’appartenant pas au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="0c7ff-120">N'</span><span class="sxs-lookup"><span data-stu-id="0c7ff-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0c7ff-121">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-121">Requests read/write permission.</span></span> <span data-ttu-id="0c7ff-122">Par défaut, les sections de profil sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="0c7ff-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="0c7ff-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="0c7ff-124">[out] Pointeur vers un pointeur vers la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c7ff-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0c7ff-125">Return value</span></span>

<span data-ttu-id="0c7ff-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c7ff-126">S_OK</span></span> 
  
> <span data-ttu-id="0c7ff-127">La section profil a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="0c7ff-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0c7ff-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0c7ff-129">Une tentative a été effectuée pour accéder à une section de profil pour lequel l’appelant dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="0c7ff-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0c7ff-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0c7ff-131">La section profil demandée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c7ff-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c7ff-132">Remarks</span></span>

<span data-ttu-id="0c7ff-133">La méthode **IMAPISession::OpenProfileSection** ouvre une section de profil ou un objet qui prend en charge l’interface **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="0c7ff-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="0c7ff-134">Les sections de profil sont utilisées pour la lecture et l’écriture d’informations sur le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="0c7ff-135">Vous ne pouvez pas utiliser **OpenProfileSection** pour ouvrir des sections de profil que propre de fournisseurs de services individuels, sauf si vous spécifiez dans le paramètre _ulFlags_ MAPI_FORCE_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0c7ff-136">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="0c7ff-136">Notes to callers</span></span>

<span data-ttu-id="0c7ff-137">Plusieurs clients peuvent ouvrir une section de profil avec l’autorisation en lecture seule, mais qu’un seul client peut ouvrir une section de profil avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="0c7ff-138">Si un autre client a une section de profil ouvrir que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur n’est défini, l’appel échoue, renvoi MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="0c7ff-139">Une opération d’ouverture en lecture seule échoue si la section est ouverte en écriture.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="0c7ff-140">Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur n’et une structure **MAPIUID** qui n’existe pas dans le paramètre _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="0c7ff-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="0c7ff-141">N’oubliez pas que vous spécifiez ne.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="0c7ff-142">Si vous définissez _lpUID_ pour pointer vers un inexistante **MAPIUID** et **OpenProfileSection** est configuré pour utiliser le mode par défaut l’accès en lecture seule, l’appel échoue avec le message MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="0c7ff-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c7ff-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c7ff-143">See also</span></span>



[<span data-ttu-id="0c7ff-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c7ff-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="0c7ff-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0c7ff-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="0c7ff-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0c7ff-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0c7ff-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c7ff-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

