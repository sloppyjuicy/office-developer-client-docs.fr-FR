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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329406"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="a571d-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a571d-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="a571d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a571d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a571d-105">Ouvre une section du profil actif et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a571d-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="a571d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a571d-106">Parameters</span></span>

 <span data-ttu-id="a571d-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="a571d-107">_lpUID_</span></span>
  
> <span data-ttu-id="a571d-108">dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil.</span><span class="sxs-lookup"><span data-stu-id="a571d-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="a571d-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a571d-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a571d-110">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="a571d-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="a571d-111">En passant la valeur NULL, le paramètre _lppProfSect_ renvoie un pointeur vers l'interface standard de la section profil, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="a571d-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="a571d-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a571d-112">_ulFlags_</span></span>
  
> <span data-ttu-id="a571d-113">dans Masque de des indicateurs qui contrôle l'accès à la section profil.</span><span class="sxs-lookup"><span data-stu-id="a571d-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="a571d-114">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="a571d-114">The following flags can be set:</span></span>
    
<span data-ttu-id="a571d-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a571d-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a571d-116">Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="a571d-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="a571d-117">Si la section profil n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="a571d-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="a571d-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a571d-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="a571d-119">Autorise l'accès à une section de profil qui n'appartient pas au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a571d-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="a571d-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a571d-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a571d-121">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a571d-121">Requests read/write permission.</span></span> <span data-ttu-id="a571d-122">Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée.</span><span class="sxs-lookup"><span data-stu-id="a571d-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a571d-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="a571d-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="a571d-124">remarquer Pointeur vers un pointeur vers la section profil.</span><span class="sxs-lookup"><span data-stu-id="a571d-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a571d-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a571d-125">Return value</span></span>

<span data-ttu-id="a571d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="a571d-126">S_OK</span></span> 
  
> <span data-ttu-id="a571d-127">La section profil a été ouverte avec succès.</span><span class="sxs-lookup"><span data-stu-id="a571d-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="a571d-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a571d-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a571d-129">Une tentative d'accès à une section de profil pour laquelle l'appelant ne dispose pas des autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="a571d-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="a571d-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a571d-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a571d-131">La section de profil demandée n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="a571d-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a571d-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="a571d-132">Remarks</span></span>

<span data-ttu-id="a571d-133">La méthode **IMAPISession:: OpenProfileSection** ouvre une section de profil ou un objet qui prend en charge l'interface **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="a571d-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="a571d-134">Les sections de profil sont utilisées pour lire des informations et écrire des informations dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="a571d-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="a571d-135">Vous ne pouvez pas utiliser **OpenProfileSection** pour ouvrir les sections de profil que les fournisseurs de services individuels possèdent, sauf si vous spécifiez MAPI_FORCE_ACCESS dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a571d-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a571d-136">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="a571d-136">Notes to callers</span></span>

<span data-ttu-id="a571d-137">Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a571d-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="a571d-138">Si un autre client a une section de profil ouverte que vous tentez d'ouvrir en appelant **OpenProfileSection** avec l'indicateur MAPI_MODIFY défini, l'appel échouera, renvoyant MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="a571d-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="a571d-139">Une opération d'ouverture en lecture seule échoue si la section est ouverte en écriture.</span><span class="sxs-lookup"><span data-stu-id="a571d-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="a571d-140">Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l'indicateur MAPI_MODIFY et une structure **MAPIUID** inexistante dans le paramètre _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="a571d-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="a571d-141">Veillez à spécifier MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="a571d-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="a571d-142">Si vous définissez _lpUID_ de sorte qu'elle pointe vers un **MAPIUID** inexistant et que **OpenProfileSection** soit configuré pour utiliser le mode d'accès par défaut en lecture seule, l'appel échouera avec MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="a571d-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a571d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a571d-143">See also</span></span>



[<span data-ttu-id="a571d-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a571d-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="a571d-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a571d-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="a571d-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a571d-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a571d-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a571d-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

