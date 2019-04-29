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
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439624"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="fc027-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc027-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="fc027-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc027-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc027-105">Définit ou efface le profil par défaut d'un client.</span><span class="sxs-lookup"><span data-stu-id="fc027-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fc027-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc027-106">Parameters</span></span>

 <span data-ttu-id="fc027-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="fc027-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="fc027-108">dans Pointeur vers le nom du profil qui deviendra la valeur par défaut, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="fc027-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="fc027-109">La définition de _lpszProfileName_ sur null indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, en laissant le client sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc027-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="fc027-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc027-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fc027-111">dans Masque de des indicateurs qui contrôle le type de la chaîne désignée par _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="fc027-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="fc027-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="fc027-112">The following flag can be set:</span></span>
    
<span data-ttu-id="fc027-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc027-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fc027-114">Le nom du profil est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="fc027-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="fc027-115">Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du profil est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="fc027-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc027-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc027-116">Return value</span></span>

<span data-ttu-id="fc027-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc027-117">S_OK</span></span> 
  
> <span data-ttu-id="fc027-118">Un profil par défaut a été correctement établi ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="fc027-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="fc027-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fc027-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fc027-120">Le profil spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="fc027-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc027-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc027-121">Remarks</span></span>

<span data-ttu-id="fc027-122">La méthode **IProfAdmin:: SetDefaultProfile** établit un profil particulier en tant que profil par défaut du client ou efface le profil par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="fc027-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="fc027-123">Le profil par défaut est le profil qui est utilisé automatiquement chaque fois que le client lance une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="fc027-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="fc027-124">**SetDefaultProfile** définit également la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du profil par défaut sur true.</span><span class="sxs-lookup"><span data-stu-id="fc027-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="fc027-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="fc027-125">Notes to callers</span></span>

<span data-ttu-id="fc027-126">Pour démarrer une session avec le profil par défaut, transmettez l'indicateur MAPI_USE_DEFAULT à la fonction [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="fc027-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc027-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc027-127">See also</span></span>



[<span data-ttu-id="fc027-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="fc027-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="fc027-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="fc027-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="fc027-130">Propriété canonique PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc027-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="fc027-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc027-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

