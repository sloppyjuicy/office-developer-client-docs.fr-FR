---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784224"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="0aaa7-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0aaa7-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="0aaa7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0aaa7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0aaa7-105">Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="0aaa7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aaa7-106">Parameters</span></span>

 <span data-ttu-id="0aaa7-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0aaa7-107">_lpUID_</span></span>
  
> <span data-ttu-id="0aaa7-108">Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="0aaa7-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0aaa7-109">_lpInterface_</span></span>
  
> <span data-ttu-id="0aaa7-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="0aaa7-111">Transmission NULL se traduit par un pointeur vers son interface standard retourné dans le paramètre _lppProfSect_ .</span><span class="sxs-lookup"><span data-stu-id="0aaa7-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="0aaa7-112">L’interface standard pour une section de profil est **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="0aaa7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0aaa7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="0aaa7-114">[in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="0aaa7-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="0aaa7-115">The following flags can be set:</span></span>
    
<span data-ttu-id="0aaa7-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0aaa7-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0aaa7-117">Permet **OpenProfileSection** retournée correctement, éventuellement avant le profil de section est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="0aaa7-118">Si la section profil n’est pas disponible, vous appelez suivante pour qu’il peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="0aaa7-119">N'</span><span class="sxs-lookup"><span data-stu-id="0aaa7-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0aaa7-120">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-120">Requests read/write permission.</span></span> <span data-ttu-id="0aaa7-121">Par défaut, les sections de profil sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="0aaa7-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0aaa7-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="0aaa7-123">Permet d’accéder à toutes les sections de profil, y compris ceux détenus par les fournisseurs de services individuels.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="0aaa7-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="0aaa7-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="0aaa7-125">[out] Pointeur vers un pointeur vers la section de profil.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0aaa7-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0aaa7-126">Return value</span></span>

<span data-ttu-id="0aaa7-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aaa7-127">S_OK</span></span> 
  
> <span data-ttu-id="0aaa7-128">La section profil a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="0aaa7-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0aaa7-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0aaa7-130">Une tentative a été effectuée pour accéder à une section de profil pour lequel l’appelant dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="0aaa7-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0aaa7-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0aaa7-132">La section profil demandée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aaa7-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="0aaa7-133">Remarks</span></span>

<span data-ttu-id="0aaa7-134">La méthode **IMsgServiceAdmin::OpenProfileSection** ouvre une section de profil, un objet qui prend en charge l’interface [IProfSect](iprofsectimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="0aaa7-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="0aaa7-135">Les sections de profil sont utilisées pour la lecture et l’écriture d’informations sur le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="0aaa7-136">**OpenProfileSection** ne peut pas être utilisé pour ouvrir des sections profil détenues par les fournisseurs de services individuels, sauf si MAPI_FORCE_ACCESS est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0aaa7-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="0aaa7-137">Notes to callers</span></span>

<span data-ttu-id="0aaa7-138">Plusieurs clients peuvent ouvrir une section de profil avec l’autorisation en lecture seule, mais qu’un seul client peut ouvrir une section de profil avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="0aaa7-139">Si un autre client a une section de profil ouvrir que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur n’est défini, l’appel échoue, renvoi MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="0aaa7-140">Une opération d’ouverture en lecture seule échoue si la section est ouverte en écriture.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="0aaa7-141">Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur n’et une structure [MAPIUID](mapiuid.md) qui n’existe pas dans le paramètre _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="0aaa7-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="0aaa7-142">N’oubliez pas que vous spécifiez ne.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="0aaa7-143">Si vous définissez _lpUID_ pour pointer vers un inexistante **MAPIUID** et **OpenProfileSection** est configuré pour utiliser le mode par défaut l’accès en lecture seule, l’appel échoue avec le message MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0aaa7-144">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0aaa7-144">MFCMAPI reference</span></span>

<span data-ttu-id="0aaa7-145">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0aaa7-146">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0aaa7-146">**File**</span></span>|<span data-ttu-id="0aaa7-147">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0aaa7-147">**Function**</span></span>|<span data-ttu-id="0aaa7-148">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0aaa7-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0aaa7-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="0aaa7-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0aaa7-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0aaa7-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="0aaa7-151">MFCMAPI utilise la méthode **IMsgServiceAdmin::OpenProfileSection** pour ouvrir une section de profil.</span><span class="sxs-lookup"><span data-stu-id="0aaa7-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0aaa7-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aaa7-152">See also</span></span>



[<span data-ttu-id="0aaa7-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aaa7-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="0aaa7-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0aaa7-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="0aaa7-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0aaa7-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="0aaa7-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0aaa7-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0aaa7-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aaa7-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="0aaa7-158">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="0aaa7-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

