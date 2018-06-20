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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783736"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="a2e2e-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a2e2e-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="a2e2e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2e2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2e2e-105">Obtient l’état associé à un message dans un dossier spécifique (par exemple, si ce message est marqué pour suppression).</span><span class="sxs-lookup"><span data-stu-id="a2e2e-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="a2e2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2e2e-106">Parameters</span></span>

 <span data-ttu-id="a2e2e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a2e2e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a2e2e-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a2e2e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a2e2e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a2e2e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a2e2e-110">[in] Pointeur vers l’identificateur d’entrée du message dont l’état est obtenu.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="a2e2e-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2e2e-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a2e2e-112">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a2e2e-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="a2e2e-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="a2e2e-114">[out] Pointeur vers un pointeur vers un masque de bits d’indicateurs qui indiquent l’état du message.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="a2e2e-115">Bits 0 à 15 sont réservés et doivent être égal à zéro ; bits 16 à 31 sont disponibles pour une utilisation spécifique à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="a2e2e-116">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="a2e2e-116">The following flags can be set:</span></span>
    
<span data-ttu-id="a2e2e-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="a2e2e-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="a2e2e-118">Le message a été marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="a2e2e-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="a2e2e-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="a2e2e-120">Le message ne pas doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="a2e2e-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="a2e2e-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="a2e2e-122">Le message doit être affichée en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="a2e2e-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a2e2e-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="a2e2e-124">Le message a été marqué pour suppression au niveau de la banque de messages à distance sans télécharger sur le client local.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="a2e2e-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a2e2e-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="a2e2e-126">Le message a été marqué pour téléchargement à partir de la banque de messages à distance au client local.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="a2e2e-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="a2e2e-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="a2e2e-128">Le message a été marqué pour un usage défini par le client.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a2e2e-129">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a2e2e-129">Return value</span></span>

<span data-ttu-id="a2e2e-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2e2e-130">S_OK</span></span> 
  
> <span data-ttu-id="a2e2e-131">Le statut du message a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2e2e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2e2e-132">Remarks</span></span>

<span data-ttu-id="a2e2e-133">La méthode **IMAPIFolder::GetMessageStatus** renvoie l’état d’un message.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="a2e2e-134">Statut du message est stocké dans la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a2e2e-135">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a2e2e-135">Notes to implementers</span></span>

<span data-ttu-id="a2e2e-136">Comment les bits d’état message définis, désactivées et utilisés dépendent complètement votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="a2e2e-137">Si vous stockez les messages dans la sous-arborescence IPM, MAPI réserve bits 16 à 31 pour une utilisation par les clients IPM.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="a2e2e-138">Si vous stockez les messages dans d’autres sous-arborescences, vous pouvez utiliser les bits 16 à 31 selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a2e2e-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a2e2e-139">MFCMAPI reference</span></span>

<span data-ttu-id="a2e2e-140">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a2e2e-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a2e2e-141">**File**</span></span>|<span data-ttu-id="a2e2e-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a2e2e-142">**Function**</span></span>|<span data-ttu-id="a2e2e-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a2e2e-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2e2e-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a2e2e-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a2e2e-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="a2e2e-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="a2e2e-146">MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message suivant s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="a2e2e-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a2e2e-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a2e2e-148">OpenMessageNonModal et OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="a2e2e-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="a2e2e-149">MFCMAPI utilise la méthode **IMAPIFolder::GetMessageStatus** pour obtenir l’état du message à afficher à transmettre à la visionneuse de formulaire, qui est CMyMAPIFormViewer ou [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="a2e2e-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2e2e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2e2e-150">See also</span></span>



[<span data-ttu-id="a2e2e-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a2e2e-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="a2e2e-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="a2e2e-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="a2e2e-153">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a2e2e-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="a2e2e-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a2e2e-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="a2e2e-155">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a2e2e-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

