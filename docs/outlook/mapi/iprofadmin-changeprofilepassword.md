---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420240"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="1164d-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="1164d-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="1164d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1164d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1164d-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="1164d-105">Deprecated.</span></span> <span data-ttu-id="1164d-106">Modifie le mot de passe d'un profil.</span><span class="sxs-lookup"><span data-stu-id="1164d-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1164d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1164d-107">Parameters</span></span>

 <span data-ttu-id="1164d-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1164d-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1164d-109">dans Pointeur vers le nom du profil associé au mot de passe à modifier.</span><span class="sxs-lookup"><span data-stu-id="1164d-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="1164d-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="1164d-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="1164d-111">dans Pointeur vers le mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="1164d-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="1164d-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="1164d-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="1164d-113">dans Pointeur vers le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1164d-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="1164d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1164d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="1164d-115">dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises.</span><span class="sxs-lookup"><span data-stu-id="1164d-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="1164d-116">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="1164d-116">The following flag can be set:</span></span>
    
<span data-ttu-id="1164d-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1164d-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1164d-118">Le nom du profil et les mots de passe sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="1164d-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="1164d-119">Si l'indicateur MAPI_UNICODE n'est pas défini, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="1164d-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1164d-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1164d-120">Return value</span></span>

<span data-ttu-id="1164d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="1164d-121">S_OK</span></span> 
  
> <span data-ttu-id="1164d-122">Si cette méthode est appelée, elle renverra S_OK.</span><span class="sxs-lookup"><span data-stu-id="1164d-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="1164d-123">Toutefois, aucune action n'est effectuée.</span><span class="sxs-lookup"><span data-stu-id="1164d-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1164d-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="1164d-124">Remarks</span></span>

<span data-ttu-id="1164d-125">N'utilisez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1164d-125">Do not use this method.</span></span> <span data-ttu-id="1164d-126">MAPI ne prend pas en charge les mots de passe des profils.</span><span class="sxs-lookup"><span data-stu-id="1164d-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1164d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1164d-127">See also</span></span>



[<span data-ttu-id="1164d-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1164d-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

