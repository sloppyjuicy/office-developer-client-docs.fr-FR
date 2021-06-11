---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418637"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="63b33-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="63b33-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="63b33-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63b33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63b33-105">Obtient l’état associé à un message dans un dossier particulier (par exemple, si ce message est marqué pour suppression).</span><span class="sxs-lookup"><span data-stu-id="63b33-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="63b33-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="63b33-106">Parameters</span></span>

 <span data-ttu-id="63b33-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="63b33-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="63b33-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="63b33-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="63b33-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="63b33-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="63b33-110">[in] Pointeur vers l’identificateur d’entrée du message dont l’état est obtenu.</span><span class="sxs-lookup"><span data-stu-id="63b33-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="63b33-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63b33-111">_ulFlags_</span></span>
  
> <span data-ttu-id="63b33-112">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="63b33-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="63b33-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="63b33-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="63b33-114">[out] Pointeur vers un pointeur vers un masque de bits d’indicateurs qui indiquent l’état du message.</span><span class="sxs-lookup"><span data-stu-id="63b33-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="63b33-115">Les bits 0 à 15 sont réservés et doivent être zéro ; Les bits 16 à 31 sont disponibles pour une utilisation spécifique à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="63b33-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="63b33-116">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="63b33-116">The following flags can be set:</span></span>
    
<span data-ttu-id="63b33-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="63b33-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="63b33-118">Le message a été marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="63b33-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="63b33-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="63b33-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="63b33-120">Le message ne doit pas être affiché.</span><span class="sxs-lookup"><span data-stu-id="63b33-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="63b33-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="63b33-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="63b33-122">Le message doit être affiché en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="63b33-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="63b33-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="63b33-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="63b33-124">Le message a été marqué pour suppression dans la boutique de messages distante sans téléchargement vers le client local.</span><span class="sxs-lookup"><span data-stu-id="63b33-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="63b33-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="63b33-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="63b33-126">Le message a été marqué pour téléchargement à partir de la boutique de messages distante vers le client local.</span><span class="sxs-lookup"><span data-stu-id="63b33-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="63b33-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="63b33-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="63b33-128">Le message a été marqué à des fins définies par le client.</span><span class="sxs-lookup"><span data-stu-id="63b33-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63b33-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63b33-129">Return value</span></span>

<span data-ttu-id="63b33-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="63b33-130">S_OK</span></span> 
  
> <span data-ttu-id="63b33-131">L’état du message a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="63b33-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63b33-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="63b33-132">Remarks</span></span>

<span data-ttu-id="63b33-133">La **méthode IMAPIFolder::GetMessageStatus** renvoie l’état d’un message.</span><span class="sxs-lookup"><span data-stu-id="63b33-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="63b33-134">L’état du message est stocké dans la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63b33-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="63b33-135">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="63b33-135">Notes to implementers</span></span>

<span data-ttu-id="63b33-136">La façon dont les bits d’état du message sont définies, effacées et utilisées dépend entièrement de votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être zéro.</span><span class="sxs-lookup"><span data-stu-id="63b33-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="63b33-137">Si vous stockez des messages dans la sous-arbre IPM, MAPI réserve les bits 16 à 31 pour une utilisation par les clients IPM.</span><span class="sxs-lookup"><span data-stu-id="63b33-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="63b33-138">Si vous stockez des messages dans d’autres sous-arbre, vous pouvez utiliser les bits 16 à 31 à vos propres fins.</span><span class="sxs-lookup"><span data-stu-id="63b33-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="63b33-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="63b33-139">MFCMAPI reference</span></span>

<span data-ttu-id="63b33-140">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="63b33-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63b33-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="63b33-141">**File**</span></span>|<span data-ttu-id="63b33-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="63b33-142">**Function**</span></span>|<span data-ttu-id="63b33-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="63b33-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63b33-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="63b33-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="63b33-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="63b33-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="63b33-146">MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message suivant à afficher.</span><span class="sxs-lookup"><span data-stu-id="63b33-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="63b33-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="63b33-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="63b33-148">OpenMessageNonModal et OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="63b33-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="63b33-149">MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message à afficher pour passer à la visionneuse de formulaires, c’est-à-dire CMyMAPIFormViewer ou [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="63b33-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63b33-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63b33-150">See also</span></span>



[<span data-ttu-id="63b33-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="63b33-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="63b33-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="63b33-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="63b33-153">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="63b33-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="63b33-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="63b33-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="63b33-155">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="63b33-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

