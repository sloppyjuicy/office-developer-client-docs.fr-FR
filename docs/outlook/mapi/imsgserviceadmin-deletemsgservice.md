---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571142"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="cf725-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="cf725-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="cf725-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf725-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf725-105">Supprime un service de message d’un profil.</span><span class="sxs-lookup"><span data-stu-id="cf725-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="cf725-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf725-106">Parameters</span></span>

 <span data-ttu-id="cf725-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="cf725-107">_lpuid_</span></span>
  
> <span data-ttu-id="cf725-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message à supprimer.</span><span class="sxs-lookup"><span data-stu-id="cf725-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cf725-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="cf725-109">Return value</span></span>

<span data-ttu-id="cf725-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf725-110">S_OK</span></span> 
  
> <span data-ttu-id="cf725-111">Le service de message a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="cf725-111">The message service was deleted.</span></span>
    
<span data-ttu-id="cf725-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cf725-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cf725-113">Le **MAPIUID** désignés par _lpuid_ ne correspond pas à un service de message existant.</span><span class="sxs-lookup"><span data-stu-id="cf725-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf725-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf725-114">Remarks</span></span>

<span data-ttu-id="cf725-115">La méthode **IMsgServiceAdmin::DeleteMsgService** supprime un service de message d’un profil.</span><span class="sxs-lookup"><span data-stu-id="cf725-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="cf725-116">**DeleteMsgService** supprime toutes les sections profil liées au service de message.</span><span class="sxs-lookup"><span data-stu-id="cf725-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="cf725-117">**DeleteMsgService** effectue les étapes suivantes pour supprimer le service de message :</span><span class="sxs-lookup"><span data-stu-id="cf725-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="cf725-118">Appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ la valeur MSG_SERVICE_DELETE avant que les sections de profil sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="cf725-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="cf725-119">Cela permet au service exécuter des tâches spécifiques aux services.</span><span class="sxs-lookup"><span data-stu-id="cf725-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="cf725-120">Supprime le service de message.</span><span class="sxs-lookup"><span data-stu-id="cf725-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="cf725-121">Supprime la section de profil du service de message.</span><span class="sxs-lookup"><span data-stu-id="cf725-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="cf725-122">Fonction de point d’entrée du service de message n’est pas appelée à nouveau une fois que le service a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="cf725-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf725-123">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="cf725-123">Notes to callers</span></span>

<span data-ttu-id="cf725-124">Pour récupérer la structure **MAPIUID** pour le service de message à supprimer, récupérez la colonne de la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="cf725-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="cf725-125">Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="cf725-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf725-126">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cf725-126">MFCMAPI reference</span></span>

<span data-ttu-id="cf725-127">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cf725-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf725-128">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="cf725-128">**File**</span></span>|<span data-ttu-id="cf725-129">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="cf725-129">**Function**</span></span>|<span data-ttu-id="cf725-130">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="cf725-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf725-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cf725-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="cf725-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="cf725-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="cf725-133">MFCMAPI utilise la méthode **IMsgServiceAdmin::DeleteMsgService** pour supprimer le service sélectionné.</span><span class="sxs-lookup"><span data-stu-id="cf725-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf725-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf725-134">See also</span></span>



[<span data-ttu-id="cf725-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cf725-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cf725-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf725-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="cf725-137">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="cf725-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

