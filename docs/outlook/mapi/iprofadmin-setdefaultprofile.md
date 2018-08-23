---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587704"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="14a21-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a21-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="14a21-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14a21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14a21-105">Active ou désactive le profil par défaut d’un client.</span><span class="sxs-lookup"><span data-stu-id="14a21-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="14a21-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14a21-106">Parameters</span></span>

 <span data-ttu-id="14a21-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="14a21-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="14a21-108">[in] Pointeur vers le nom du profil qui deviennent les valeurs par défaut, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="14a21-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="14a21-109">Définition de _lpszProfileName_ sur NULL indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, quitter le client sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="14a21-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="14a21-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14a21-110">_ulFlags_</span></span>
  
> <span data-ttu-id="14a21-111">[in] Un masque de bits d’indicateurs qui contrôle le type de la chaîne indiquée par _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="14a21-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="14a21-112">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="14a21-112">The following flag can be set:</span></span>
    
<span data-ttu-id="14a21-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="14a21-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="14a21-114">Le nom de profil est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="14a21-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="14a21-115">Si l’indicateur MAPI_UNICODE n’est pas définie, le nom de profil est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="14a21-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14a21-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="14a21-116">Return value</span></span>

<span data-ttu-id="14a21-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="14a21-117">S_OK</span></span> 
  
> <span data-ttu-id="14a21-118">Un profil par défaut a été correctement établi ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="14a21-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="14a21-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="14a21-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="14a21-120">Le profil spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="14a21-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14a21-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="14a21-121">Remarks</span></span>

<span data-ttu-id="14a21-122">La méthode **IProfAdmin::SetDefaultProfile** établit un profil spécifique comme le profil du client par défaut ou efface le profil par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="14a21-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="14a21-123">Le profil par défaut est le profil qui est utilisé automatiquement chaque fois que le client commence une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="14a21-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="14a21-124">**SetDefaultProfile** définit également une propriété de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du nouveau profil par défaut la valeur True.</span><span class="sxs-lookup"><span data-stu-id="14a21-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="14a21-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="14a21-125">Notes to callers</span></span>

<span data-ttu-id="14a21-126">Pour démarrer une session avec le profil par défaut, passez l’indicateur MAPI_USE_DEFAULT à la fonction [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="14a21-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14a21-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14a21-127">See also</span></span>



[<span data-ttu-id="14a21-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="14a21-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="14a21-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="14a21-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="14a21-130">Propriété canonique PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a21-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="14a21-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14a21-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

