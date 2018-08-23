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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0f917989d9bac403f2bea5b2d6699b7a1caf2008
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573011"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="5eabf-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5eabf-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="5eabf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eabf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eabf-105">Ouvre une section de profil du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="5eabf-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="5eabf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5eabf-106">Parameters</span></span>

 <span data-ttu-id="5eabf-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5eabf-107">_lpUID_</span></span>
  
> <span data-ttu-id="5eabf-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique de la section de profil à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="5eabf-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="5eabf-109">Les clients ne doivent pas passer NULL pour le paramètre _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="5eabf-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="5eabf-110">Fournisseurs de services peuvent passer la valeur NULL pour récupérer le **MAPIUID** quand ils appellent à partir de leurs fonctions de point d’entrée de message service.</span><span class="sxs-lookup"><span data-stu-id="5eabf-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="5eabf-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5eabf-111">_lpInterface_</span></span>
  
> <span data-ttu-id="5eabf-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="5eabf-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="5eabf-113">Interface standard de la section de profil (**IProfSect**) renvoyé génère passant NULL.</span><span class="sxs-lookup"><span data-stu-id="5eabf-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="5eabf-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5eabf-114">_ulFlags_</span></span>
  
> <span data-ttu-id="5eabf-115">[in] Masque de bits d’indicateurs qui contrôle le mode d’ouverture de la section de profil.</span><span class="sxs-lookup"><span data-stu-id="5eabf-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="5eabf-116">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="5eabf-116">The following flags can be set:</span></span>
    
<span data-ttu-id="5eabf-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5eabf-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5eabf-118">Permet **OpenProfileSection** renvoyer avec succès, éventuellement avant la section profil est entièrement disponible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5eabf-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="5eabf-119">Si la section profil n’est pas disponible, vous appelez suivante pour qu’il peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="5eabf-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="5eabf-120">N'</span><span class="sxs-lookup"><span data-stu-id="5eabf-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5eabf-121">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5eabf-121">Requests read/write permission.</span></span> <span data-ttu-id="5eabf-122">Par défaut, les objets sont ouverts avec l’autorisation en lecture seule, et les appelants ne doivent pas travailler sur l’hypothèse que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5eabf-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="5eabf-123">Autorisation de lecture/écriture aux sections du fournisseur du profil ne sont pas autorisés par les clients.</span><span class="sxs-lookup"><span data-stu-id="5eabf-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="5eabf-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5eabf-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="5eabf-125">Permet d’accéder à toutes les sections de profil, y compris ceux détenus par les fournisseurs de services individuels.</span><span class="sxs-lookup"><span data-stu-id="5eabf-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="5eabf-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="5eabf-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="5eabf-127">[out] Pointeur vers un pointeur vers la section de profil.</span><span class="sxs-lookup"><span data-stu-id="5eabf-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5eabf-128">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5eabf-128">Return value</span></span>

<span data-ttu-id="5eabf-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="5eabf-129">S_OK</span></span> 
  
> <span data-ttu-id="5eabf-130">La section profil a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="5eabf-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="5eabf-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5eabf-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5eabf-132">Une tentative a été effectuée pour modifier une section de profil en lecture seule ou pour accéder à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="5eabf-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="5eabf-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5eabf-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5eabf-134">La section profil demandée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="5eabf-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5eabf-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="5eabf-135">Remarks</span></span>

<span data-ttu-id="5eabf-136">La méthode **IProviderAdmin::OpenProfileSection** ouvre une section de profil, l’activation de l’appelant et lire des informations d’écrire éventuellement des informations dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="5eabf-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="5eabf-137">Les clients ne peuvent pas ouvrir les sections profil qui appartiennent à un fournisseur à l’aide de la méthode **OpenProfileSection** .</span><span class="sxs-lookup"><span data-stu-id="5eabf-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="5eabf-138">Plusieurs clients ou fournisseurs de services peuvent ouvrir simultanément une section de profil avec l’autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5eabf-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="5eabf-139">Toutefois, lorsqu’une section de profil est ouverte avec l’autorisation de lecture/écriture, aucun autre appel ne peut être effectuées pour ouvrir la section, quel que soit le type d’accès.</span><span class="sxs-lookup"><span data-stu-id="5eabf-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="5eabf-140">Si une section de profil est ouverte avec l’autorisation en lecture seule, un autre appel à la demande d’autorisation de lecture/écriture échoue avec MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="5eabf-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="5eabf-141">De même, si une section est ouverte avec l’autorisation de lecture/écriture, un appel suivant à la demande d’autorisation en lecture seule échouera également.</span><span class="sxs-lookup"><span data-stu-id="5eabf-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5eabf-142">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="5eabf-142">Notes to callers</span></span>

<span data-ttu-id="5eabf-143">Si vous avez demandé qui **OpenProfileSection** ouvrir une section de profil inexistant en transmettant _n’ulFlags_ et un inconnu **MAPIUID** dans _lpUID_, la section profil sera créée.</span><span class="sxs-lookup"><span data-stu-id="5eabf-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="5eabf-144">Si vous avez demandé que **OpenProfileSection** ouvrir une section inexistante disposant d’une autorisation en lecture seule, elle renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="5eabf-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5eabf-145">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5eabf-145">MFCMAPI reference</span></span>

<span data-ttu-id="5eabf-146">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5eabf-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5eabf-147">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5eabf-147">**File**</span></span>|<span data-ttu-id="5eabf-148">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5eabf-148">**Function**</span></span>|<span data-ttu-id="5eabf-149">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5eabf-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5eabf-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5eabf-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5eabf-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5eabf-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="5eabf-152">MFCMAPI utilise la méthode **IProviderAdmin::OpenProfileSection** pour ouvrir une section de profil du profil actuel.</span><span class="sxs-lookup"><span data-stu-id="5eabf-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5eabf-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5eabf-153">See also</span></span>



[<span data-ttu-id="5eabf-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5eabf-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="5eabf-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5eabf-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="5eabf-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5eabf-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5eabf-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5eabf-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="5eabf-158">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5eabf-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

