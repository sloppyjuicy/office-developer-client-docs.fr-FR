---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410356"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="98291-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="98291-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="98291-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98291-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98291-105">Modifie le mot de passe d'un fournisseur de services sans afficher d'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98291-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="98291-106">Cette méthode est éventuellement prise en charge dans les objets d'État implémentés par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="98291-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="98291-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98291-107">Parameters</span></span>

 <span data-ttu-id="98291-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="98291-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="98291-109">dans Pointeur vers l'ancien mot de passe.</span><span class="sxs-lookup"><span data-stu-id="98291-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="98291-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="98291-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="98291-111">dans Pointeur vers le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="98291-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="98291-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98291-112">_ulFlags_</span></span>
  
> <span data-ttu-id="98291-113">dans Masque de des indicateurs qui contrôle le format des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="98291-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="98291-114">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="98291-114">The following flag can be set:</span></span>
    
<span data-ttu-id="98291-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98291-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="98291-116">Les mots de passe sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="98291-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="98291-117">Si l'indicateur MAPI_UNICODE n'est pas défini, les mots de passe sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="98291-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98291-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98291-118">Return value</span></span>

<span data-ttu-id="98291-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="98291-119">S_OK</span></span> 
  
> <span data-ttu-id="98291-120">La modification du mot de passe a réussi.</span><span class="sxs-lookup"><span data-stu-id="98291-120">The password modification was successful.</span></span>
    
<span data-ttu-id="98291-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="98291-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="98291-122">L'ancien mot de passe désigné par _lpOldPass_ n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="98291-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="98291-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="98291-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="98291-124">L'objet Status ne prend pas en charge cette opération, comme indiqué par l'absence de l'indicateur STATUS_CHANGE_PASSWORD dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l'objet Status.</span><span class="sxs-lookup"><span data-stu-id="98291-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98291-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="98291-125">Remarks</span></span>

<span data-ttu-id="98291-126">Tous les objets d'État ne prennent pas en charge la méthode **IMAPIStatus:: ChangePassword** .</span><span class="sxs-lookup"><span data-stu-id="98291-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="98291-127">Il est pris en charge uniquement par les fournisseurs de services qui nécessitent des clients pour entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="98291-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="98291-128">Aucun des objets d'État que MAPI implémente ne prend en charge l'opération de modification de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="98291-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="98291-129">**ChangePassword** modifie un mot de passe par programme, sans intervention de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98291-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="98291-130">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="98291-130">Notes to implementers</span></span>

<span data-ttu-id="98291-131">Les fournisseurs de transport à distance implémentent **ChangePassword** comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="98291-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="98291-132">Il n'y a aucune considération particulière.</span><span class="sxs-lookup"><span data-stu-id="98291-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98291-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98291-133">See also</span></span>



[<span data-ttu-id="98291-134">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="98291-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="98291-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="98291-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

