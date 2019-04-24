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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301546"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="da548-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="da548-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="da548-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da548-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da548-105">Ouvre une section de profil à partir du profil actuel et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="da548-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="da548-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da548-106">Parameters</span></span>

 <span data-ttu-id="da548-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="da548-107">_lpUID_</span></span>
  
> <span data-ttu-id="da548-108">dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique de la section de profil à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="da548-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="da548-109">Les clients ne doivent pas transmettre de valeur NULL pour le paramètre _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="da548-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="da548-110">Les fournisseurs de services peuvent transmettre la valeur NULL pour récupérer le **MAPIUID** lorsqu'ils appellent à partir de leurs fonctions de point d'entrée de service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="da548-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="da548-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="da548-111">_lpInterface_</span></span>
  
> <span data-ttu-id="da548-112">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="da548-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="da548-113">Le passage de la valeur NULL entraîne le renvoi de l'interface standard de la section de profil (**IProfSect**).</span><span class="sxs-lookup"><span data-stu-id="da548-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="da548-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da548-114">_ulFlags_</span></span>
  
> <span data-ttu-id="da548-115">dans Masque de des indicateurs qui contrôle l'ouverture de la section profil.</span><span class="sxs-lookup"><span data-stu-id="da548-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="da548-116">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="da548-116">The following flags can be set:</span></span>
    
<span data-ttu-id="da548-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="da548-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="da548-118">Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour l'appelant.</span><span class="sxs-lookup"><span data-stu-id="da548-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="da548-119">Si la section profil n'est pas disponible, un appel ultérieur de celle-ci peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="da548-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="da548-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="da548-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="da548-121">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="da548-121">Requests read/write permission.</span></span> <span data-ttu-id="da548-122">Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée.</span><span class="sxs-lookup"><span data-stu-id="da548-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="da548-123">Les clients ne sont pas autorisés à accéder en lecture/écriture aux sections du fournisseur du profil.</span><span class="sxs-lookup"><span data-stu-id="da548-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="da548-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="da548-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="da548-125">Autorise l'accès à toutes les sections de profil, même celles appartenant à des fournisseurs de services individuels.</span><span class="sxs-lookup"><span data-stu-id="da548-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="da548-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="da548-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="da548-127">remarquer Pointeur vers un pointeur vers la section profil.</span><span class="sxs-lookup"><span data-stu-id="da548-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da548-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da548-128">Return value</span></span>

<span data-ttu-id="da548-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="da548-129">S_OK</span></span> 
  
> <span data-ttu-id="da548-130">La section profil a été ouverte avec succès.</span><span class="sxs-lookup"><span data-stu-id="da548-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="da548-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="da548-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="da548-132">Une tentative de modification d'une section de profil en lecture seule ou d'accès à un objet pour lequel l'utilisateur ne dispose pas des autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="da548-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="da548-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="da548-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="da548-134">La section de profil demandée n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="da548-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da548-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="da548-135">Remarks</span></span>

<span data-ttu-id="da548-136">La méthode **IProviderAdmin:: OpenProfileSection** ouvre une section de profil, permettant ainsi à l'appelant de lire les informations et de les écrire dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="da548-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="da548-137">Les clients ne peuvent pas ouvrir les sections de profil qui appartiennent à des fournisseurs à l'aide de la méthode **OpenProfileSection** .</span><span class="sxs-lookup"><span data-stu-id="da548-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="da548-138">Plusieurs clients ou fournisseurs de services peuvent simultanément ouvrir une section de profil avec une autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="da548-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="da548-139">Toutefois, lorsqu'une section de profil est ouverte avec une autorisation en lecture/écriture, aucun autre appel ne peut être effectué pour ouvrir la section, quel que soit le type d'accès.</span><span class="sxs-lookup"><span data-stu-id="da548-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="da548-140">Si une section de profil est ouverte avec une autorisation en lecture seule, un appel ultérieur à la demande d'autorisation de lecture/écriture échouera avec MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="da548-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="da548-141">De même, si une section est ouverte avec une autorisation en lecture/écriture, un appel ultérieur à la demande en lecture seule échouera également.</span><span class="sxs-lookup"><span data-stu-id="da548-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="da548-142">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="da548-142">Notes to callers</span></span>

<span data-ttu-id="da548-143">Si vous demandez qu' **OpenProfileSection** ouvre une section de profil inexistante en transmettant MAPI_MODIFY dans _UlFlags_ et un **MAPIUID** inconnu dans _lpUID_, la section de profil est créée.</span><span class="sxs-lookup"><span data-stu-id="da548-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="da548-144">Si vous demandez à **OpenProfileSection** ouvrir une section inexistante avec l'autorisation en lecture seule, elle renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="da548-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="da548-145">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="da548-145">MFCMAPI reference</span></span>

<span data-ttu-id="da548-146">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="da548-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da548-147">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="da548-147">**File**</span></span>|<span data-ttu-id="da548-148">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="da548-148">**Function**</span></span>|<span data-ttu-id="da548-149">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="da548-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da548-150">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="da548-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="da548-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="da548-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="da548-152">MFCMAPI utilise la méthode **IProviderAdmin:: OpenProfileSection** pour ouvrir une section de profil à partir du profil actuel.</span><span class="sxs-lookup"><span data-stu-id="da548-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da548-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da548-153">See also</span></span>



[<span data-ttu-id="da548-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da548-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="da548-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="da548-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="da548-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="da548-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="da548-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da548-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="da548-158">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="da548-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

