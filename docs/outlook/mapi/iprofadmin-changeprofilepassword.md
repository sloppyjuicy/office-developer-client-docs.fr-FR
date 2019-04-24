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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317121"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="e5a41-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="e5a41-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="e5a41-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5a41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5a41-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="e5a41-105">Deprecated.</span></span> <span data-ttu-id="e5a41-106">Modifie le mot de passe d'un profil.</span><span class="sxs-lookup"><span data-stu-id="e5a41-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e5a41-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5a41-107">Parameters</span></span>

 <span data-ttu-id="e5a41-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="e5a41-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="e5a41-109">dans Pointeur vers le nom du profil associé au mot de passe à modifier.</span><span class="sxs-lookup"><span data-stu-id="e5a41-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="e5a41-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="e5a41-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="e5a41-111">dans Pointeur vers le mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="e5a41-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="e5a41-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="e5a41-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="e5a41-113">dans Pointeur vers le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e5a41-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="e5a41-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5a41-114">_ulFlags_</span></span>
  
> <span data-ttu-id="e5a41-115">dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises.</span><span class="sxs-lookup"><span data-stu-id="e5a41-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="e5a41-116">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="e5a41-116">The following flag can be set:</span></span>
    
<span data-ttu-id="e5a41-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5a41-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e5a41-118">Le nom du profil et les mots de passe sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e5a41-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="e5a41-119">Si l'indicateur MAPI_UNICODE n'est pas défini, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e5a41-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5a41-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5a41-120">Return value</span></span>

<span data-ttu-id="e5a41-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5a41-121">S_OK</span></span> 
  
> <span data-ttu-id="e5a41-122">Si cette méthode est appelée, elle renverra S_OK.</span><span class="sxs-lookup"><span data-stu-id="e5a41-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="e5a41-123">Toutefois, aucune action n'est effectuée.</span><span class="sxs-lookup"><span data-stu-id="e5a41-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5a41-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5a41-124">Remarks</span></span>

<span data-ttu-id="e5a41-125">N'utilisez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e5a41-125">Do not use this method.</span></span> <span data-ttu-id="e5a41-126">MAPI ne prend pas en charge les mots de passe des profils.</span><span class="sxs-lookup"><span data-stu-id="e5a41-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5a41-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5a41-127">See also</span></span>



[<span data-ttu-id="e5a41-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5a41-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

