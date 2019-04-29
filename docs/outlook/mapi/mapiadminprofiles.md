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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412351"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="ff8ec-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="ff8ec-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="ff8ec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff8ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff8ec-105">Crée un objet d'administration de profil.</span><span class="sxs-lookup"><span data-stu-id="ff8ec-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff8ec-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ff8ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff8ec-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="ff8ec-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ff8ec-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ff8ec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff8ec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff8ec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff8ec-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ff8ec-110">Called by:</span></span>  <br/> |<span data-ttu-id="ff8ec-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="ff8ec-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="ff8ec-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff8ec-112">Parameters</span></span>

 <span data-ttu-id="ff8ec-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff8ec-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ff8ec-114">dans Masque de réindicateur des indicateurs indiquant les options de la fonction d'entrée de service.</span><span class="sxs-lookup"><span data-stu-id="ff8ec-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="ff8ec-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="ff8ec-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="ff8ec-116">remarquer Pointeur vers un pointeur vers le nouvel objet d'administration de profil.</span><span class="sxs-lookup"><span data-stu-id="ff8ec-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff8ec-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff8ec-117">Return value</span></span>

<span data-ttu-id="ff8ec-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff8ec-118">S_OK</span></span> 
  
> <span data-ttu-id="ff8ec-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ff8ec-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff8ec-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff8ec-120">MFCMAPI reference</span></span>

<span data-ttu-id="ff8ec-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ff8ec-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff8ec-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ff8ec-122">**File**</span></span>|<span data-ttu-id="ff8ec-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ff8ec-123">**Function**</span></span>|<span data-ttu-id="ff8ec-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ff8ec-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff8ec-125">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="ff8ec-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="ff8ec-126">CMapiObjects:: GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="ff8ec-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="ff8ec-127">MFCMAPI utilise la méthode **MAPIAdminProfiles** pour obtenir l'objet d'administration des profils.</span><span class="sxs-lookup"><span data-stu-id="ff8ec-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff8ec-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff8ec-128">See also</span></span>



[<span data-ttu-id="ff8ec-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="ff8ec-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="ff8ec-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ff8ec-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

