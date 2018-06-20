---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784390"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="c68f6-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="c68f6-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="c68f6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c68f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c68f6-105">Supprime un profil.</span><span class="sxs-lookup"><span data-stu-id="c68f6-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c68f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c68f6-106">Parameters</span></span>

 <span data-ttu-id="c68f6-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="c68f6-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="c68f6-108">[in] Pointeur vers le nom du profil à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c68f6-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="c68f6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c68f6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c68f6-110">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="c68f6-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c68f6-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c68f6-111">Return value</span></span>

<span data-ttu-id="c68f6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c68f6-112">S_OK</span></span> 
  
> <span data-ttu-id="c68f6-113">Le profil a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c68f6-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="c68f6-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c68f6-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c68f6-115">Le profil spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c68f6-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c68f6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c68f6-116">Remarks</span></span>

<span data-ttu-id="c68f6-117">La méthode **IProfAdmin::DeleteProfile** supprime un profil.</span><span class="sxs-lookup"><span data-stu-id="c68f6-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="c68f6-118">Si le profil à supprimer est en cours d’utilisation lorsque **DeleteProfile** est appelée, **DeleteProfile** renvoie S_OK mais ne supprime pas le profil immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c68f6-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="c68f6-119">Au lieu de cela, **DeleteProfile** marque le profil de suppression et le supprime une fois qu’il est n’est plus utilisé, lorsque toutes les sessions actives sont terminées.</span><span class="sxs-lookup"><span data-stu-id="c68f6-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="c68f6-120">La fonction de point d’entrée pour chaque service de message dans le profil est appelée avec la valeur MSG_SERVICE_DELETE définie dans le paramètre _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="c68f6-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="c68f6-121">Tout d’abord, la fonction supprime le service, puis il supprime la section de profil du service.</span><span class="sxs-lookup"><span data-stu-id="c68f6-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="c68f6-122">La fonction de point d’entrée de message service n’est pas encore appelée une fois que le service a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c68f6-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="c68f6-123">Aucun mot de passe n’est requis pour supprimer un profil.</span><span class="sxs-lookup"><span data-stu-id="c68f6-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c68f6-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c68f6-124">MFCMAPI reference</span></span>

<span data-ttu-id="c68f6-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c68f6-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c68f6-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c68f6-126">**File**</span></span>|<span data-ttu-id="c68f6-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c68f6-127">**Function**</span></span>|<span data-ttu-id="c68f6-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c68f6-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c68f6-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c68f6-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c68f6-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="c68f6-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="c68f6-131">MFCMAPI utilise la méthode **IProfAdmin::DeleteProfile** pour supprimer le profil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c68f6-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c68f6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c68f6-132">See also</span></span>



[<span data-ttu-id="c68f6-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="c68f6-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="c68f6-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c68f6-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c68f6-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c68f6-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="c68f6-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c68f6-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

