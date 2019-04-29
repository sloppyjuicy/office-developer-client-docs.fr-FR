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
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419519"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="e1920-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="e1920-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="e1920-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1920-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1920-105">Affecte un nouveau nom à un profil.</span><span class="sxs-lookup"><span data-stu-id="e1920-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e1920-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1920-106">Parameters</span></span>

 <span data-ttu-id="e1920-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="e1920-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="e1920-108">dans Pointeur vers le nom actuel du profil à renommer.</span><span class="sxs-lookup"><span data-stu-id="e1920-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="e1920-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="e1920-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="e1920-110">dans Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="e1920-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="e1920-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="e1920-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="e1920-112">dans Pointeur vers le nouveau nom du profil à renommer.</span><span class="sxs-lookup"><span data-stu-id="e1920-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="e1920-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e1920-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="e1920-114">dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="e1920-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="e1920-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1920-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e1920-116">dans Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="e1920-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1920-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e1920-117">Return value</span></span>

<span data-ttu-id="e1920-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1920-118">S_OK</span></span> 
  
> <span data-ttu-id="e1920-119">Le profil a été renommé.</span><span class="sxs-lookup"><span data-stu-id="e1920-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="e1920-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="e1920-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="e1920-121">Le mot de passe du profil est incorrect.</span><span class="sxs-lookup"><span data-stu-id="e1920-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="e1920-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e1920-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e1920-123">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e1920-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e1920-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1920-124">Remarks</span></span>

<span data-ttu-id="e1920-125">La méthode **IProfAdmin:: RenameProfile** affecte un nouveau nom à un profil, s'il en a un.</span><span class="sxs-lookup"><span data-stu-id="e1920-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="e1920-126">Si le profil à renommer est utilisé par un client lors de l'appel de **RenameProfile** , **RenameProfile** marque le profil et renvoie S_OK au lieu de tenter l'opération de changement de nom pendant l'utilisation du profil.</span><span class="sxs-lookup"><span data-stu-id="e1920-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="e1920-127">Lorsque le profil n'est plus utilisé, **RenameProfile** lui attribue le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="e1920-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="e1920-128">L'ancien et le nouveau nom du profil peuvent contenir jusqu'à 64 caractères et peuvent inclure les caractères suivants:</span><span class="sxs-lookup"><span data-stu-id="e1920-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="e1920-129">Tous les caractères alphanumériques, y compris les caractères d'accentuation et le trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="e1920-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="e1920-130">Espaces incorporés, mais pas d'espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="e1920-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="e1920-131">L' _lpszPassword_ doit toujours être null ou un pointeur vers une chaîne de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="e1920-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1920-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1920-132">See also</span></span>



[<span data-ttu-id="e1920-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1920-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

