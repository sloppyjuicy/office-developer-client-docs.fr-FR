---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437237"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="6ecc4-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="6ecc4-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="6ecc4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ecc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ecc4-105">Copie un profil.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6ecc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ecc4-106">Parameters</span></span>

 <span data-ttu-id="6ecc4-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="6ecc4-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="6ecc4-108">dans Pointeur vers le nom du profil à copier.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="6ecc4-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="6ecc4-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="6ecc4-110">dans Pointeur vers le mot de passe du profil à copier.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="6ecc4-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="6ecc4-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="6ecc4-112">dans Pointeur vers le nouveau nom du profil copié.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="6ecc4-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6ecc4-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6ecc4-114">dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="6ecc4-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ecc4-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6ecc4-116">dans Masque de des indicateurs qui contrôle la manière dont le profil est copié.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="6ecc4-117">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="6ecc4-117">The following flags can be set:</span></span>
    
<span data-ttu-id="6ecc4-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6ecc4-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6ecc4-119">Affiche une boîte de dialogue qui invite l'utilisateur à indiquer le mot de passe correct du profil à copier.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="6ecc4-120">Si cet indicateur n'est pas défini, aucune boîte de dialogue ne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ecc4-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ecc4-121">Return value</span></span>

<span data-ttu-id="6ecc4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ecc4-122">S_OK</span></span> 
  
> <span data-ttu-id="6ecc4-123">Le profil a été correctement copié.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="6ecc4-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="6ecc4-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="6ecc4-125">Le nouveau nom de profil est identique à celui d'un profil existant.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="6ecc4-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="6ecc4-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="6ecc4-127">Le mot de passe du profil à copier est incorrect et une boîte de dialogue n'a pas pu être affichée à l'utilisateur pour demander le mot de passe correct car MAPI_DIALOG n'a pas été défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6ecc4-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="6ecc4-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6ecc4-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6ecc4-129">Le profil spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="6ecc4-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6ecc4-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6ecc4-131">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6ecc4-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ecc4-132">Remarks</span></span>

<span data-ttu-id="6ecc4-133">La méthode **IProfAdmin:: CopyProfile** effectue une copie du profil désigné par _lpszOldProfileName_, lui donnant le nom indiqué par _lpszNewProfileName_.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="6ecc4-134">La copie d'un profil laisse la copie avec le même mot de passe que l'original.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="6ecc4-135">Le nom du profil d'origine, son mot de passe et la copie peuvent contenir jusqu'à 64 caractères et peuvent inclure les caractères suivants:</span><span class="sxs-lookup"><span data-stu-id="6ecc4-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="6ecc4-136">Tous les caractères alphanumériques, y compris les caractères d'accentuation et le trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="6ecc4-137">Espaces incorporés, mais pas d'espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="6ecc4-138">Les mots de passe de profil ne sont pas pris en charge sur tous les systèmes d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="6ecc4-139">Sur les systèmes d'exploitation qui ne prennent pas en charge les mots de passe de profil, _lpszOldPassword_ peut être null ou un pointeur vers une chaîne de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="6ecc4-140">Si _lpszOldPassword_ est défini sur null, le profil à copier requiert un mot de passe et l'indicateur MAPI_DIALOG est défini; une boîte de dialogue invitant l'utilisateur à indiquer le mot de passe est affichée.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="6ecc4-141">Si un mot de passe est requis, mais que _lpszOldPassword_ est défini sur null et que l'indicateur MAPI_DIALOG n'est pas défini, **CopyProfile** renvoie MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="6ecc4-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ecc4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ecc4-142">See also</span></span>



[<span data-ttu-id="6ecc4-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ecc4-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

