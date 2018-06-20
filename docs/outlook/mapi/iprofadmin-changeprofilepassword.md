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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784384"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="6948f-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="6948f-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="6948f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6948f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6948f-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="6948f-105">Deprecated.</span></span> <span data-ttu-id="6948f-106">Modifie le mot de passe pour un profil.</span><span class="sxs-lookup"><span data-stu-id="6948f-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6948f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6948f-107">Parameters</span></span>

 <span data-ttu-id="6948f-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6948f-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6948f-109">[in] Pointeur vers le nom du profil associé avec le mot de passe à modifier.</span><span class="sxs-lookup"><span data-stu-id="6948f-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="6948f-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="6948f-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="6948f-111">[in] Pointeur vers le mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="6948f-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="6948f-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="6948f-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="6948f-113">[in] Pointeur vers le nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="6948f-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="6948f-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6948f-114">_ulFlags_</span></span>
  
> <span data-ttu-id="6948f-115">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé.</span><span class="sxs-lookup"><span data-stu-id="6948f-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="6948f-116">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="6948f-116">The following flag can be set:</span></span>
    
<span data-ttu-id="6948f-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6948f-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6948f-118">Le nom de profil et les mots de passe sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="6948f-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="6948f-119">Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="6948f-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6948f-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6948f-120">Return value</span></span>

<span data-ttu-id="6948f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6948f-121">S_OK</span></span> 
  
> <span data-ttu-id="6948f-122">Si cette méthode est appelée, elle renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="6948f-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="6948f-123">Toutefois, aucune action ne sera entreprise.</span><span class="sxs-lookup"><span data-stu-id="6948f-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6948f-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="6948f-124">Remarks</span></span>

<span data-ttu-id="6948f-125">N’utilisez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6948f-125">Do not use this method.</span></span> <span data-ttu-id="6948f-126">MAPI ne gère pas les mots de passe pour les profils.</span><span class="sxs-lookup"><span data-stu-id="6948f-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6948f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6948f-127">See also</span></span>



[<span data-ttu-id="6948f-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6948f-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

