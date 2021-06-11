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
# <a name="imapistatuschangepassword"></a><span data-ttu-id="061f2-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="061f2-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="061f2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="061f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="061f2-105">Modifie le mot de passe d’un fournisseur de services sans afficher d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="061f2-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="061f2-106">Cette méthode est éventuellement prise en charge dans les objets d’état implémentés par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="061f2-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="061f2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="061f2-107">Parameters</span></span>

 <span data-ttu-id="061f2-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="061f2-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="061f2-109">[in] Pointeur vers l’ancien mot de passe.</span><span class="sxs-lookup"><span data-stu-id="061f2-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="061f2-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="061f2-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="061f2-111">[in] Pointeur vers le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="061f2-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="061f2-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="061f2-112">_ulFlags_</span></span>
  
> <span data-ttu-id="061f2-113">[in] Masque de bits d’indicateurs qui contrôle le format des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="061f2-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="061f2-114">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="061f2-114">The following flag can be set:</span></span>
    
<span data-ttu-id="061f2-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="061f2-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="061f2-116">Les mots de passe sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="061f2-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="061f2-117">Si l’MAPI_UNICODE n’est pas définie, les mots de passe sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="061f2-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="061f2-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="061f2-118">Return value</span></span>

<span data-ttu-id="061f2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="061f2-119">S_OK</span></span> 
  
> <span data-ttu-id="061f2-120">La modification du mot de passe a réussi.</span><span class="sxs-lookup"><span data-stu-id="061f2-120">The password modification was successful.</span></span>
    
<span data-ttu-id="061f2-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="061f2-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="061f2-122">L’ancien mot de passe pointé par  _lpOldPass_ n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="061f2-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="061f2-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="061f2-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="061f2-124">L’objet status ne prend pas en charge cette opération, comme indiqué par l’absence de l’indicateur STATUS_CHANGE_PASSWORD dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="061f2-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="061f2-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="061f2-125">Remarks</span></span>

<span data-ttu-id="061f2-126">Les objets d’état ne sont pas tous en charge par la méthode **IMAPIStatus::ChangePassword.**</span><span class="sxs-lookup"><span data-stu-id="061f2-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="061f2-127">Il est uniquement pris en charge par les fournisseurs de services qui exigent que les clients entrent un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="061f2-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="061f2-128">Aucun des objets d’état implémentés par MAPI ne permet de modifier le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="061f2-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="061f2-129">**ChangePassword** modifie un mot de passe par programme, sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="061f2-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="061f2-130">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="061f2-130">Notes to implementers</span></span>

<span data-ttu-id="061f2-131">Les fournisseurs de transport distant **implémentent ChangePassword** comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="061f2-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="061f2-132">Il n’existe aucune considération particulière.</span><span class="sxs-lookup"><span data-stu-id="061f2-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="061f2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="061f2-133">See also</span></span>



[<span data-ttu-id="061f2-134">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="061f2-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="061f2-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="061f2-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

