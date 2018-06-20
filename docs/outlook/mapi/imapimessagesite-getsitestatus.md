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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783838"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="d48ac-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d48ac-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="d48ac-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d48ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d48ac-105">Retourne des informations à partir d’un objet de site message sur le message fonctionnalités du site pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="d48ac-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="d48ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d48ac-106">Parameters</span></span>

 <span data-ttu-id="d48ac-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="d48ac-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="d48ac-108">[out] Pointeur vers un masque de bits d’indicateurs qui fournit des informations sur le statut du message.</span><span class="sxs-lookup"><span data-stu-id="d48ac-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="d48ac-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="d48ac-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d48ac-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="d48ac-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="d48ac-111">Le message peut être copié.</span><span class="sxs-lookup"><span data-stu-id="d48ac-111">The message can be copied.</span></span> 
    
<span data-ttu-id="d48ac-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="d48ac-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="d48ac-113">Le message peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="d48ac-113">The message can be deleted.</span></span>
    
<span data-ttu-id="d48ac-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="d48ac-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="d48ac-115">Lors de la suppression, un message est déplacé vers le dossier **Éléments supprimés** dans la base de messages au lieu immédiatement supprimé à partir de la base de messages.</span><span class="sxs-lookup"><span data-stu-id="d48ac-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="d48ac-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="d48ac-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="d48ac-117">Le message peut être déplacé.</span><span class="sxs-lookup"><span data-stu-id="d48ac-117">The message can be moved.</span></span>
    
<span data-ttu-id="d48ac-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d48ac-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="d48ac-119">Un message peut être créé.</span><span class="sxs-lookup"><span data-stu-id="d48ac-119">A new message can be created.</span></span>
    
<span data-ttu-id="d48ac-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="d48ac-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="d48ac-121">Le message peut être enregistré.</span><span class="sxs-lookup"><span data-stu-id="d48ac-121">The message can be saved.</span></span>
    
<span data-ttu-id="d48ac-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="d48ac-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="d48ac-123">Le message peut être envoyé.</span><span class="sxs-lookup"><span data-stu-id="d48ac-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d48ac-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d48ac-124">Return value</span></span>

<span data-ttu-id="d48ac-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d48ac-125">S_OK</span></span> 
  
> <span data-ttu-id="d48ac-126">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d48ac-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d48ac-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="d48ac-127">Remarks</span></span>

<span data-ttu-id="d48ac-128">Objets de formulaire appeler la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir les fonctionnalités de l’objet de site de message pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="d48ac-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="d48ac-129">Les indicateurs retournés dans le paramètre _lpulStatus_ fournissent des informations sur le site de message.</span><span class="sxs-lookup"><span data-stu-id="d48ac-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="d48ac-130">En règle générale, un formulaire active ou désactive les commandes de menu, en fonction des informations que fournissent les indicateurs sur les possibilités de l’implémentation de sites de message.</span><span class="sxs-lookup"><span data-stu-id="d48ac-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="d48ac-131">Si un nouveau message est chargé dans un formulaire par la méthode [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou la méthode [IPersistMessage::Load](ipersistmessage-load.md) , les indicateurs d’état doivent être vérifiées.</span><span class="sxs-lookup"><span data-stu-id="d48ac-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="d48ac-132">Certains objets du site de message, notamment les objets en lecture seule, ne pas autorisent les messages d’être enregistré ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="d48ac-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d48ac-133">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="d48ac-133">Notes to implementers</span></span>

<span data-ttu-id="d48ac-134">La méthode **IMAPIMessageSite::GetSiteStatus** peut nécessiter l’application cliente pour effectuer des calculs pour déterminer les opérations peuvent ou ne peut pas être effectuées sur le message en cours.</span><span class="sxs-lookup"><span data-stu-id="d48ac-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="d48ac-135">En règle générale, qui implique la recherche au niveau de la ligne d’état pour le fournisseur de banque de messages du message en cours, ou l’application cliente interroger le fournisseur de banque pour déterminer les actions qui permettre effectuer à l’aide de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d48ac-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="d48ac-136">Par exemple, pour déterminer s’il faut retourner l’indicateur MAPI_DELETE_IS_MOVE, vérifiez propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) de l’objet de banque de messages pour voir s’il existe un dossier **Éléments supprimés** dans le banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d48ac-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="d48ac-137">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d48ac-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d48ac-138">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d48ac-138">MFCMAPI reference</span></span>

<span data-ttu-id="d48ac-139">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d48ac-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d48ac-140">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d48ac-140">**File**</span></span>|<span data-ttu-id="d48ac-141">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d48ac-141">**Function**</span></span>|<span data-ttu-id="d48ac-142">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d48ac-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d48ac-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d48ac-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d48ac-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d48ac-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="d48ac-145">MFCMAPI utilise la méthode **IMAPIMessageSite::GetSiteStatus** pour obtenir l’état du site spécifié.</span><span class="sxs-lookup"><span data-stu-id="d48ac-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="d48ac-146">Elle peut renvoyer VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="d48ac-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d48ac-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d48ac-147">See also</span></span>



[<span data-ttu-id="d48ac-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="d48ac-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="d48ac-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="d48ac-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="d48ac-150">Propriété canonique PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="d48ac-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="d48ac-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d48ac-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d48ac-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d48ac-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d48ac-153">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="d48ac-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

