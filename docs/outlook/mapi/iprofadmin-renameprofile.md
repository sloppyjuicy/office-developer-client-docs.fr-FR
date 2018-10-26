---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4453465c04d7a5a3de79f2ae34d13095863487cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569504"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="4cf08-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="4cf08-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="4cf08-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cf08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cf08-105">Affecte un nouveau nom à un profil.</span><span class="sxs-lookup"><span data-stu-id="4cf08-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4cf08-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cf08-106">Parameters</span></span>

 <span data-ttu-id="4cf08-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="4cf08-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="4cf08-108">[in] Pointeur vers le nom actuel du profil à renommer.</span><span class="sxs-lookup"><span data-stu-id="4cf08-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="4cf08-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="4cf08-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="4cf08-110">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="4cf08-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="4cf08-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="4cf08-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="4cf08-112">[in] Pointeur vers le nouveau nom du profil à renommer.</span><span class="sxs-lookup"><span data-stu-id="4cf08-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="4cf08-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4cf08-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="4cf08-114">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4cf08-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="4cf08-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cf08-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4cf08-116">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="4cf08-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4cf08-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4cf08-117">Return value</span></span>

<span data-ttu-id="4cf08-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cf08-118">S_OK</span></span> 
  
> <span data-ttu-id="4cf08-119">Le profil a été renommé.</span><span class="sxs-lookup"><span data-stu-id="4cf08-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="4cf08-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="4cf08-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="4cf08-121">Le mot de passe de profil est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="4cf08-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="4cf08-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4cf08-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4cf08-123">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4cf08-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4cf08-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="4cf08-124">Remarks</span></span>

<span data-ttu-id="4cf08-125">La méthode **IProfAdmin::RenameProfile** attribue un nouveau nom à un profil, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4cf08-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="4cf08-126">Si le profil pour renommer est en cours d’utilisation par un client lorsque **RenameProfile** est appelée, **RenameProfile** marque le profil et renvoie S_OK au lieu d’essayer de l’opération de changement alors que le profil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4cf08-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="4cf08-127">Lorsque le profil est n’est plus utilisé, **RenameProfile** assigne le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="4cf08-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="4cf08-128">Les noms anciens et nouveaux du profil peuvent contenir jusqu'à 64 caractères et peuvent inclure les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="4cf08-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="4cf08-129">Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement.</span><span class="sxs-lookup"><span data-stu-id="4cf08-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="4cf08-130">Des espaces, mais pas espaces à gauche ou.</span><span class="sxs-lookup"><span data-stu-id="4cf08-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="4cf08-131">Le _lpszPassword_ doit toujours être NULL ou un pointeur vers une chaîne de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="4cf08-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cf08-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cf08-132">See also</span></span>



[<span data-ttu-id="4cf08-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4cf08-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

