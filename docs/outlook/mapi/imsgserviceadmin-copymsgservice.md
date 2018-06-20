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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784237"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="1a48e-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="1a48e-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="1a48e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a48e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a48e-105">Copie un service de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="1a48e-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="1a48e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a48e-106">Parameters</span></span>

 <span data-ttu-id="1a48e-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="1a48e-107">_lpUID_</span></span>
  
> <span data-ttu-id="1a48e-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à copier.</span><span class="sxs-lookup"><span data-stu-id="1a48e-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="1a48e-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="1a48e-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="1a48e-110">[in] Ce paramètre est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="1a48e-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="1a48e-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="1a48e-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="1a48e-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section profil du service de message à copier.</span><span class="sxs-lookup"><span data-stu-id="1a48e-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="1a48e-113">Résultats de la transmission NULL dans l’interface de section de profil standard, [IProfSect](iprofsectimapiprop.md), utilisée.</span><span class="sxs-lookup"><span data-stu-id="1a48e-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="1a48e-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="1a48e-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="1a48e-115">[in] Un pointeur vers l’IID qui représente l’interface à utiliser pour accéder à l’objet indiqué par le paramètre _lpObjectDst_ .</span><span class="sxs-lookup"><span data-stu-id="1a48e-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="1a48e-116">Résultats de la transmission NULL dans l’interface de session, [IMAPISession](imapisessioniunknown.md), utilisée.</span><span class="sxs-lookup"><span data-stu-id="1a48e-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="1a48e-117">Le paramètre _lpInterfaceDst_ peut également être défini à IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="1a48e-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="1a48e-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="1a48e-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="1a48e-119">[in] Pointeur vers un pointeur vers un objet d’administration service session ou de message.</span><span class="sxs-lookup"><span data-stu-id="1a48e-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="1a48e-120">Le type d’objet doit correspondre à l’identificateur d’interface _lpInterfaceDst_passé.</span><span class="sxs-lookup"><span data-stu-id="1a48e-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="1a48e-121">LPMAPISESSION et LPSERVICEADMIN sont des pointeurs d’objet valide.</span><span class="sxs-lookup"><span data-stu-id="1a48e-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="1a48e-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1a48e-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="1a48e-123">[in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="1a48e-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="1a48e-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a48e-124">_ulFlags_</span></span>
  
> <span data-ttu-id="1a48e-125">[in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est copié.</span><span class="sxs-lookup"><span data-stu-id="1a48e-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="1a48e-126">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="1a48e-126">The following flags can be set:</span></span>
    
<span data-ttu-id="1a48e-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="1a48e-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="1a48e-128">Demande que le service de message toujours affiche une feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="1a48e-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a48e-129">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1a48e-129">Return value</span></span>

<span data-ttu-id="1a48e-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a48e-130">S_OK</span></span> 
  
> <span data-ttu-id="1a48e-131">Le service de message a été correctement copié.</span><span class="sxs-lookup"><span data-stu-id="1a48e-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="1a48e-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1a48e-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1a48e-133">Le service de message est déjà dans le profil et n’autorise pas plusieurs instances de lui-même.</span><span class="sxs-lookup"><span data-stu-id="1a48e-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="1a48e-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1a48e-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1a48e-135">Le **MAPIUID** désignés par _lpUID_ ne fait pas référence à un service de message existant.</span><span class="sxs-lookup"><span data-stu-id="1a48e-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1a48e-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a48e-136">Remarks</span></span>

<span data-ttu-id="1a48e-137">La méthode **IMsgServiceAdmin::CopyMsgService** copie un service de message dans un profil, le profil actif ou un autre profil.</span><span class="sxs-lookup"><span data-stu-id="1a48e-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="1a48e-138">Le profil qui contient le service de message à copier et la destination n’ont pas être le même profil, mais ils peuvent être.</span><span class="sxs-lookup"><span data-stu-id="1a48e-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="1a48e-139">Fonction de point d’entrée du service de message n’est pas appelée pour une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="1a48e-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="1a48e-140">Le service de message copié a les mêmes paramètres de configuration que l’original.</span><span class="sxs-lookup"><span data-stu-id="1a48e-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="1a48e-141">Pour modifier ces paramètres, un client doit appeler la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1a48e-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a48e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a48e-142">See also</span></span>



[<span data-ttu-id="1a48e-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="1a48e-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="1a48e-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1a48e-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="1a48e-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a48e-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

