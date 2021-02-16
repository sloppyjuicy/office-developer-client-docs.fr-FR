---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432120"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="db296-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="db296-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="db296-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db296-105">Copie un service de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="db296-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="db296-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db296-106">Parameters</span></span>

 <span data-ttu-id="db296-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="db296-107">_lpUID_</span></span>
  
> <span data-ttu-id="db296-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à copier.</span><span class="sxs-lookup"><span data-stu-id="db296-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="db296-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="db296-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="db296-110">[in] Ce paramètre a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="db296-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="db296-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="db296-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="db296-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil du service de message à copier.</span><span class="sxs-lookup"><span data-stu-id="db296-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="db296-113">Transmission de résultats NULL dans l’interface de section de profil standard, [IProfSect](iprofsectimapiprop.md), utilisé.</span><span class="sxs-lookup"><span data-stu-id="db296-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="db296-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="db296-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="db296-115">[in] Pointeur vers l’IID qui représente l’interface à utiliser pour accéder à l’objet pointé par le paramètre _lpObjectDst._</span><span class="sxs-lookup"><span data-stu-id="db296-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="db296-116">Transmission de résultats NULL dans l’interface de session, [IMAPISession](imapisessioniunknown.md), en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="db296-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="db296-117">Le  _paramètre lpInterfaceDst_ peut également être IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="db296-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="db296-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="db296-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="db296-119">[in] Pointeur vers un pointeur vers un objet d’administration de service de session ou de message.</span><span class="sxs-lookup"><span data-stu-id="db296-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="db296-120">Le type d’objet doit correspondre à l’identificateur d’interface transmis  _dans lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="db296-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="db296-121">Les pointeurs d’objet valides sont LPMAPISESSION et LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="db296-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="db296-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="db296-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="db296-123">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="db296-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="db296-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="db296-124">_ulFlags_</span></span>
  
> <span data-ttu-id="db296-125">[in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est copié.</span><span class="sxs-lookup"><span data-stu-id="db296-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="db296-126">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="db296-126">The following flags can be set:</span></span>
    
<span data-ttu-id="db296-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="db296-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="db296-128">Demande au service de message d’afficher toujours une feuille des propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="db296-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db296-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db296-129">Return value</span></span>

<span data-ttu-id="db296-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="db296-130">S_OK</span></span> 
  
> <span data-ttu-id="db296-131">Le service de message a été correctement copié.</span><span class="sxs-lookup"><span data-stu-id="db296-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="db296-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="db296-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="db296-133">Le service de message est déjà dans le profil et n’autorise pas plusieurs instances d’elle-même.</span><span class="sxs-lookup"><span data-stu-id="db296-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="db296-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="db296-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="db296-135">Le **MAPIUID pointé** par  _lpUID_ ne fait pas référence à un service de message existant.</span><span class="sxs-lookup"><span data-stu-id="db296-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="db296-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="db296-136">Remarks</span></span>

<span data-ttu-id="db296-137">La **méthode IMsgServiceAdmin::CopyMsgService** copie un service de message dans un profil, le profil actif ou un autre profil.</span><span class="sxs-lookup"><span data-stu-id="db296-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="db296-138">Le profil qui contient le service de message à copier et la destination ne doivent pas être du même profil, mais ils peuvent l’être.</span><span class="sxs-lookup"><span data-stu-id="db296-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="db296-139">La fonction de point d’entrée du service de message n’est pas appelée pour une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="db296-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="db296-140">Le service de message copié a les mêmes paramètres de configuration que son original.</span><span class="sxs-lookup"><span data-stu-id="db296-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="db296-141">Pour modifier ces paramètres, un client doit appeler la méthode [IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="db296-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db296-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db296-142">See also</span></span>



[<span data-ttu-id="db296-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="db296-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="db296-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="db296-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="db296-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db296-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

