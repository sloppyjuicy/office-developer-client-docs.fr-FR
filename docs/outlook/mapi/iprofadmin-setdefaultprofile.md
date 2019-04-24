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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270167"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="f9dc2-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dc2-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="f9dc2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9dc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9dc2-105">Définit ou efface le profil par défaut d'un client.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f9dc2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9dc2-106">Parameters</span></span>

 <span data-ttu-id="f9dc2-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="f9dc2-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="f9dc2-108">dans Pointeur vers le nom du profil qui deviendra la valeur par défaut, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="f9dc2-109">La définition de _lpszProfileName_ sur null indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, en laissant le client sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="f9dc2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9dc2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f9dc2-111">dans Masque de des indicateurs qui contrôle le type de la chaîne désignée par _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="f9dc2-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="f9dc2-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f9dc2-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9dc2-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f9dc2-114">Le nom du profil est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="f9dc2-115">Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du profil est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9dc2-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9dc2-116">Return value</span></span>

<span data-ttu-id="f9dc2-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9dc2-117">S_OK</span></span> 
  
> <span data-ttu-id="f9dc2-118">Un profil par défaut a été correctement établi ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="f9dc2-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f9dc2-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f9dc2-120">Le profil spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9dc2-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9dc2-121">Remarks</span></span>

<span data-ttu-id="f9dc2-122">La méthode **IProfAdmin:: SetDefaultProfile** établit un profil particulier en tant que profil par défaut du client ou efface le profil par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="f9dc2-123">Le profil par défaut est le profil qui est utilisé automatiquement chaque fois que le client lance une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="f9dc2-124">**SetDefaultProfile** définit également la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du profil par défaut sur true.</span><span class="sxs-lookup"><span data-stu-id="f9dc2-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f9dc2-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="f9dc2-125">Notes to callers</span></span>

<span data-ttu-id="f9dc2-126">Pour démarrer une session avec le profil par défaut, transmettez l'indicateur MAPI_USE_DEFAULT à la fonction [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="f9dc2-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9dc2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9dc2-127">See also</span></span>



[<span data-ttu-id="f9dc2-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="f9dc2-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="f9dc2-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="f9dc2-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="f9dc2-130">Propriété canonique PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dc2-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="f9dc2-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9dc2-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

