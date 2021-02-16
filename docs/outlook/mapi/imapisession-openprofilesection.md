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
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439918"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="9e6b1-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="9e6b1-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="9e6b1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e6b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e6b1-105">Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="9e6b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e6b1-106">Parameters</span></span>

 <span data-ttu-id="9e6b1-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="9e6b1-107">_lpUID_</span></span>
  
> <span data-ttu-id="9e6b1-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="9e6b1-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9e6b1-109">_lpInterface_</span></span>
  
> <span data-ttu-id="9e6b1-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="9e6b1-111">La transmission de null entraîne  _le paramètre lppProfSect_ à renvoyer un pointeur vers l’interface standard de la section de profil, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="9e6b1-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e6b1-112">_ulFlags_</span></span>
  
> <span data-ttu-id="9e6b1-113">[in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="9e6b1-114">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="9e6b1-114">The following flags can be set:</span></span>
    
<span data-ttu-id="9e6b1-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9e6b1-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9e6b1-116">Permet à **OpenProfileSection** de renvoyer correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="9e6b1-117">Si la section de profil n’est pas disponible, un appel ultérieur à celui-ci peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="9e6b1-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9e6b1-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="9e6b1-119">Permet d’accéder à une section de profil qui n’appartient pas au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="9e6b1-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9e6b1-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9e6b1-121">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-121">Requests read/write permission.</span></span> <span data-ttu-id="9e6b1-122">Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule et les clients ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture a été accordée.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="9e6b1-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="9e6b1-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="9e6b1-124">[out] Pointeur vers un pointeur vers la section de profil.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e6b1-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9e6b1-125">Return value</span></span>

<span data-ttu-id="9e6b1-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e6b1-126">S_OK</span></span> 
  
> <span data-ttu-id="9e6b1-127">La section de profil a été ouverte avec succès.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="9e6b1-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9e6b1-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9e6b1-129">Une tentative d’accès à une section de profil pour laquelle l’appelant dispose d’autorisations insuffisantes a été tentée.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="9e6b1-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9e6b1-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9e6b1-131">La section de profil demandée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e6b1-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e6b1-132">Remarks</span></span>

<span data-ttu-id="9e6b1-133">La **méthode IMAPISession::OpenProfileSection** ouvre une section de profil ou un objet qui prend en charge l’interface **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="9e6b1-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="9e6b1-134">Les sections de profil sont utilisées pour lire et écrire des informations dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="9e6b1-135">Vous ne pouvez pas utiliser **OpenProfileSection** pour ouvrir des sections de profil propres à des fournisseurs de services individuels, sauf si vous spécifiez MAPI_FORCE_ACCESS dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="9e6b1-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e6b1-136">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="9e6b1-136">Notes to callers</span></span>

<span data-ttu-id="9e6b1-137">Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="9e6b1-138">Si une section de profil est ouverte sur un autre client que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY, l’appel échoue et retourne MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="9e6b1-139">Une opération d’ouverture en lecture seule échoue si la section est ouverte pour écriture.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="9e6b1-140">Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY et une structure **MAPIUID** inexistante dans le paramètre _lpUID._</span><span class="sxs-lookup"><span data-stu-id="9e6b1-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="9e6b1-141">Assurez-vous de spécifier MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="9e6b1-142">Si vous définissez _lpUID_ de façon à pointer vers un **MAPIUID** inexistant et qu’OpenProfileSection est définie pour utiliser le mode d’accès par défaut en lecture seule, l’appel échouera avec MAPI_E_NOT_FOUND. </span><span class="sxs-lookup"><span data-stu-id="9e6b1-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e6b1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e6b1-143">See also</span></span>



[<span data-ttu-id="9e6b1-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e6b1-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="9e6b1-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9e6b1-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="9e6b1-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9e6b1-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9e6b1-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e6b1-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

