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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309988"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="3f3f0-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="3f3f0-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="3f3f0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f3f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f3f0-105">Supprime un service de messagerie d'un profil.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="3f3f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f3f0-106">Parameters</span></span>

 <span data-ttu-id="3f3f0-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="3f3f0-107">_lpuid_</span></span>
  
> <span data-ttu-id="3f3f0-108">dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de messagerie à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f3f0-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f3f0-109">Return value</span></span>

<span data-ttu-id="3f3f0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f3f0-110">S_OK</span></span> 
  
> <span data-ttu-id="3f3f0-111">Le service de messagerie a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-111">The message service was deleted.</span></span>
    
<span data-ttu-id="3f3f0-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3f3f0-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3f3f0-113">Le **MAPIUID** pointé par _lpuid_ ne correspond pas à un service de messagerie existant.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f3f0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f3f0-114">Remarks</span></span>

<span data-ttu-id="3f3f0-115">La méthode **IMsgServiceAdmin::D eletemsgservice** supprime un service de messagerie d'un profil.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="3f3f0-116">**DeleteMsgService** supprime toutes les sections de profil liées au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="3f3f0-117">**DeleteMsgService** effectue les étapes suivantes pour supprimer le service de messagerie:</span><span class="sxs-lookup"><span data-stu-id="3f3f0-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="3f3f0-118">Appelle la fonction de point d'entrée du service de messagerie avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE avant la suppression des sections de profil.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="3f3f0-119">Cela permet au service d'effectuer des tâches spécifiques aux services.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="3f3f0-120">Supprime le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="3f3f0-121">Supprime la section de profil du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="3f3f0-122">La fonction de point d'entrée du service de messagerie n'est pas rappelée une fois que le service a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3f3f0-123">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3f3f0-123">Notes to callers</span></span>

<span data-ttu-id="3f3f0-124">Pour récupérer la structure **MAPIUID** pour le service de messagerie à supprimer, récupérez la colonne de propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de messagerie dans la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="3f3f0-125">Pour plus d'informations, reportez-vous à la procédure décrite dans la méthode [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3f0-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f3f0-126">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3f3f0-126">MFCMAPI reference</span></span>

<span data-ttu-id="3f3f0-127">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f3f0-128">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3f3f0-128">**File**</span></span>|<span data-ttu-id="3f3f0-129">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3f3f0-129">**Function**</span></span>|<span data-ttu-id="3f3f0-130">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3f3f0-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f3f0-131">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="3f3f0-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="3f3f0-132">CMsgServiceTableDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="3f3f0-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="3f3f0-133">MFCMAPI utilise la méthode **IMsgServiceAdmin::D eletemsgservice** pour supprimer le service sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3f3f0-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f3f0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f3f0-134">See also</span></span>



[<span data-ttu-id="3f3f0-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3f3f0-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3f3f0-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f3f0-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="3f3f0-137">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3f3f0-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

