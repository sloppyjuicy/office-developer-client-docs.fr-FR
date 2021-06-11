---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405659"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="c46e5-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="c46e5-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="c46e5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c46e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c46e5-105">Ouvre une section de profil à partir du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c46e5-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="c46e5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c46e5-106">Parameters</span></span>

 <span data-ttu-id="c46e5-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c46e5-107">_lpUID_</span></span>
  
> <span data-ttu-id="c46e5-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique de la section de profil à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="c46e5-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="c46e5-109">Les clients ne doivent pas transmettre null pour _le paramètre lpUID._</span><span class="sxs-lookup"><span data-stu-id="c46e5-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="c46e5-110">Les fournisseurs de services peuvent transmettre la valeur NULL pour récupérer **le MAPIUID** lorsqu’ils appellent à partir de leurs fonctions de point d’entrée de service de message.</span><span class="sxs-lookup"><span data-stu-id="c46e5-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="c46e5-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c46e5-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c46e5-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="c46e5-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="c46e5-113">La transmission DE NULL entraîne le retour de l’interface standard de la section de profil **(IProfSect).**</span><span class="sxs-lookup"><span data-stu-id="c46e5-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="c46e5-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c46e5-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c46e5-115">[in] Masque de bits d’indicateurs qui contrôle la façon dont la section de profil est ouverte.</span><span class="sxs-lookup"><span data-stu-id="c46e5-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="c46e5-116">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="c46e5-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c46e5-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c46e5-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c46e5-118">Permet à **OpenProfileSection** de renvoyer correctement, éventuellement avant que la section de profil ne soit entièrement disponible pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c46e5-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="c46e5-119">Si la section de profil n’est pas disponible, un appel ultérieur à celui-ci peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="c46e5-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="c46e5-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c46e5-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c46e5-121">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c46e5-121">Requests read/write permission.</span></span> <span data-ttu-id="c46e5-122">Par défaut, les objets sont ouverts avec une autorisation en lecture seule et les appelants ne doivent pas fonctionner sur l’hypothèse que l’autorisation lecture/écriture a été accordée.</span><span class="sxs-lookup"><span data-stu-id="c46e5-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="c46e5-123">Les clients ne sont pas autorisés à lire/écrire des sections fournisseur du profil.</span><span class="sxs-lookup"><span data-stu-id="c46e5-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="c46e5-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c46e5-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="c46e5-125">Permet d’accéder à toutes les sections de profil, même celles qui sont propriétés de fournisseurs de services individuels.</span><span class="sxs-lookup"><span data-stu-id="c46e5-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="c46e5-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="c46e5-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="c46e5-127">[out] Pointeur vers un pointeur vers la section de profil.</span><span class="sxs-lookup"><span data-stu-id="c46e5-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c46e5-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c46e5-128">Return value</span></span>

<span data-ttu-id="c46e5-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="c46e5-129">S_OK</span></span> 
  
> <span data-ttu-id="c46e5-130">La section profil a été ouverte avec succès.</span><span class="sxs-lookup"><span data-stu-id="c46e5-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="c46e5-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c46e5-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c46e5-132">Une tentative de modification d’une section de profil en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été tentée.</span><span class="sxs-lookup"><span data-stu-id="c46e5-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c46e5-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c46e5-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c46e5-134">La section de profil demandée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c46e5-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c46e5-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="c46e5-135">Remarks</span></span>

<span data-ttu-id="c46e5-136">La **méthode IProviderAdmin::OpenProfileSection** ouvre une section de profil, permettant à l’appelant de lire des informations dans le profil actif et éventuellement d’écrire des informations dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c46e5-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="c46e5-137">Les clients ne peuvent pas ouvrir les sections de profil appartenant à des fournisseurs à l’aide de la méthode **OpenProfileSection.**</span><span class="sxs-lookup"><span data-stu-id="c46e5-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="c46e5-138">Plusieurs clients ou fournisseurs de services peuvent ouvrir simultanément une section de profil avec une autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c46e5-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="c46e5-139">Toutefois, lorsqu’une section de profil est ouverte avec une autorisation de lecture/écriture, aucun autre appel ne peut être effectué pour ouvrir la section, quel que soit le type d’accès.</span><span class="sxs-lookup"><span data-stu-id="c46e5-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="c46e5-140">Si une section de profil est ouverte avec une autorisation en lecture seule, un appel ultérieur pour demander une autorisation de lecture/écriture échouera avec MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="c46e5-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="c46e5-141">De même, si une section est ouverte avec une autorisation de lecture/écriture, un appel ultérieur pour demander une autorisation en lecture seule échouera également.</span><span class="sxs-lookup"><span data-stu-id="c46e5-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c46e5-142">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="c46e5-142">Notes to callers</span></span>

<span data-ttu-id="c46e5-143">Si vous demandez **qu’OpenProfileSection** ouvre une section de profil inexistante en passant des MAPI_MODIFY dans  _ulFlags_ et un **MAPIUID** inconnu dans  _lpUID,_ la section de profil est créée.</span><span class="sxs-lookup"><span data-stu-id="c46e5-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="c46e5-144">Si vous demandez **qu’OpenProfileSection** ouvre une section inexistante avec une autorisation en lecture seule, elle renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="c46e5-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c46e5-145">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c46e5-145">MFCMAPI reference</span></span>

<span data-ttu-id="c46e5-146">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c46e5-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c46e5-147">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c46e5-147">**File**</span></span>|<span data-ttu-id="c46e5-148">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c46e5-148">**Function**</span></span>|<span data-ttu-id="c46e5-149">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c46e5-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c46e5-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c46e5-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c46e5-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="c46e5-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="c46e5-152">MFCMAPI utilise la méthode **IProviderAdmin::OpenProfileSection** pour ouvrir une section de profil à partir du profil actuel.</span><span class="sxs-lookup"><span data-stu-id="c46e5-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c46e5-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c46e5-153">See also</span></span>



[<span data-ttu-id="c46e5-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c46e5-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="c46e5-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c46e5-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="c46e5-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c46e5-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c46e5-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c46e5-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="c46e5-158">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c46e5-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

