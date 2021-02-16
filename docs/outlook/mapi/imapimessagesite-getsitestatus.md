---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430125"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="c7aef-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="c7aef-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="c7aef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7aef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7aef-105">Renvoie des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="c7aef-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="c7aef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7aef-106">Parameters</span></span>

 <span data-ttu-id="c7aef-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="c7aef-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="c7aef-108">[out] Pointeur vers un masque de bits d’indicateurs qui fournit des informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="c7aef-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="c7aef-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="c7aef-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c7aef-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="c7aef-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="c7aef-111">Le message peut être copié.</span><span class="sxs-lookup"><span data-stu-id="c7aef-111">The message can be copied.</span></span> 
    
<span data-ttu-id="c7aef-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="c7aef-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="c7aef-113">Le message peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="c7aef-113">The message can be deleted.</span></span>
    
<span data-ttu-id="c7aef-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="c7aef-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="c7aef-115">Lorsqu’il est supprimé, un  message est déplacé vers un dossier Éléments supprimés de sa boutique de messages au lieu d’être immédiatement supprimé de sa boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="c7aef-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="c7aef-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="c7aef-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="c7aef-117">Le message peut être déplacé.</span><span class="sxs-lookup"><span data-stu-id="c7aef-117">The message can be moved.</span></span>
    
<span data-ttu-id="c7aef-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c7aef-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="c7aef-119">Un nouveau message peut être créé.</span><span class="sxs-lookup"><span data-stu-id="c7aef-119">A new message can be created.</span></span>
    
<span data-ttu-id="c7aef-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="c7aef-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="c7aef-121">Le message peut être enregistré.</span><span class="sxs-lookup"><span data-stu-id="c7aef-121">The message can be saved.</span></span>
    
<span data-ttu-id="c7aef-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="c7aef-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="c7aef-123">Le message peut être envoyé.</span><span class="sxs-lookup"><span data-stu-id="c7aef-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7aef-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7aef-124">Return value</span></span>

<span data-ttu-id="c7aef-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7aef-125">S_OK</span></span> 
  
> <span data-ttu-id="c7aef-126">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c7aef-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7aef-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7aef-127">Remarks</span></span>

<span data-ttu-id="c7aef-128">Les objets form appellent la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir les fonctionnalités de l’objet de site de message pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="c7aef-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="c7aef-129">Les indicateurs renvoyés dans le  _paramètre lpulStatus_ fournissent des informations sur le site de message.</span><span class="sxs-lookup"><span data-stu-id="c7aef-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="c7aef-130">En règle générale, un formulaire active ou désactive les commandes de menu, en fonction des informations fournies par les indicateurs sur les fonctionnalités de l’implémentation du site de message.</span><span class="sxs-lookup"><span data-stu-id="c7aef-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="c7aef-131">Si un nouveau message est chargé dans un formulaire par la méthode [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou [IPersistMessage::Load,](ipersistmessage-load.md) les indicateurs d’état doivent être vérifiés.</span><span class="sxs-lookup"><span data-stu-id="c7aef-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="c7aef-132">Certains objets de site de message, en particulier les objets en lecture seule, n’autorisent pas l’enregistré ou la suppression des messages.</span><span class="sxs-lookup"><span data-stu-id="c7aef-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c7aef-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c7aef-133">Notes to implementers</span></span>

<span data-ttu-id="c7aef-134">La **méthode IMAPIMessageSite::GetSiteStatus** peut exiger que l’application cliente effectue un calcul pour déterminer les opérations qui peuvent ou ne peuvent pas être effectuées sur le message actuel.</span><span class="sxs-lookup"><span data-stu-id="c7aef-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="c7aef-135">En règle générale, cela implique de regarder la ligne d’état du fournisseur de la boutique de messages du message actuel ou d’interroger le fournisseur de magasin pour déterminer les actions que l’application cliente peut effectuer à l’aide de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="c7aef-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="c7aef-136">Par exemple, pour déterminer s’il faut renvoyer l’indicateur MAPI_DELETE_IS_MOVE, vérifiez la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) de l’objet de la boutique de messages pour voir s’il existe un dossier Éléments supprimés dans la magasin de messages. </span><span class="sxs-lookup"><span data-stu-id="c7aef-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="c7aef-137">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c7aef-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c7aef-138">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c7aef-138">MFCMAPI reference</span></span>

<span data-ttu-id="c7aef-139">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c7aef-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c7aef-140">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c7aef-140">**File**</span></span>|<span data-ttu-id="c7aef-141">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c7aef-141">**Function**</span></span>|<span data-ttu-id="c7aef-142">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c7aef-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7aef-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c7aef-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c7aef-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="c7aef-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="c7aef-145">MFCMAPI utilise la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir l’état du site spécifié.</span><span class="sxs-lookup"><span data-stu-id="c7aef-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="c7aef-146">Elle peut renvoyer VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="c7aef-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7aef-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7aef-147">See also</span></span>



[<span data-ttu-id="c7aef-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="c7aef-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="c7aef-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="c7aef-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="c7aef-150">Propriété canonique PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="c7aef-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="c7aef-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7aef-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c7aef-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c7aef-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c7aef-153">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="c7aef-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

