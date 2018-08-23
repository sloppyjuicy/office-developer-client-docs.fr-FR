---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581285"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="6a0c8-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="6a0c8-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="6a0c8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a0c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a0c8-105">Crée un objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a0c8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6a0c8-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a0c8-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="6a0c8-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6a0c8-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6a0c8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a0c8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a0c8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a0c8-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6a0c8-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a0c8-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="6a0c8-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="6a0c8-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="6a0c8-112">Parameters</span></span>

 <span data-ttu-id="6a0c8-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a0c8-113">_ulFlags_</span></span>
  
> <span data-ttu-id="6a0c8-114">[in] Masque de bits d’indicateurs indiquant les options pour la fonction de l’entrée de service.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="6a0c8-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="6a0c8-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="6a0c8-116">[out] Pointeur vers un pointeur vers le nouvel objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a0c8-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6a0c8-117">Return value</span></span>

<span data-ttu-id="6a0c8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a0c8-118">S_OK</span></span> 
  
> <span data-ttu-id="6a0c8-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6a0c8-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6a0c8-120">MFCMAPI reference</span></span>

<span data-ttu-id="6a0c8-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6a0c8-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6a0c8-122">**File**</span></span>|<span data-ttu-id="6a0c8-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6a0c8-123">**Function**</span></span>|<span data-ttu-id="6a0c8-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6a0c8-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6a0c8-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="6a0c8-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="6a0c8-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="6a0c8-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="6a0c8-127">MFCMAPI utilise la méthode **MAPIAdminProfiles** pour obtenir l’objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a0c8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0c8-128">See also</span></span>



[<span data-ttu-id="6a0c8-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="6a0c8-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="6a0c8-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6a0c8-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

