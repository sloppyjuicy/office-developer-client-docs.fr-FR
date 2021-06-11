---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417272"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="8fe91-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8fe91-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="8fe91-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fe91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fe91-105">Définit l’état associé à un message (par exemple, si ce message est marqué pour suppression).</span><span class="sxs-lookup"><span data-stu-id="8fe91-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="8fe91-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8fe91-106">Parameters</span></span>

 <span data-ttu-id="8fe91-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8fe91-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8fe91-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="8fe91-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8fe91-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8fe91-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8fe91-110">[in] Pointeur vers l’identificateur d’entrée du message dont l’état est définie.</span><span class="sxs-lookup"><span data-stu-id="8fe91-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="8fe91-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="8fe91-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="8fe91-112">[in] Nouveau statut à attribuer.</span><span class="sxs-lookup"><span data-stu-id="8fe91-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="8fe91-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="8fe91-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="8fe91-114">[in] Masque de bits d’indicateurs qui est appliqué au nouvel état et indique les indicateurs à définir.</span><span class="sxs-lookup"><span data-stu-id="8fe91-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="8fe91-115">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="8fe91-115">The following flags can be set:</span></span>
    
<span data-ttu-id="8fe91-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="8fe91-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="8fe91-117">Le message a été marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="8fe91-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="8fe91-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="8fe91-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="8fe91-119">Le message ne doit pas être affiché.</span><span class="sxs-lookup"><span data-stu-id="8fe91-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="8fe91-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="8fe91-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="8fe91-121">Le message doit être affiché en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="8fe91-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="8fe91-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="8fe91-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="8fe91-123">Le message a été marqué pour suppression dans la boutique de messages distante sans téléchargement vers le client local.</span><span class="sxs-lookup"><span data-stu-id="8fe91-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="8fe91-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="8fe91-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="8fe91-125">Le message a été marqué pour téléchargement à partir de la boutique de messages distante vers le client local.</span><span class="sxs-lookup"><span data-stu-id="8fe91-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="8fe91-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="8fe91-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="8fe91-127">Le message a été marqué à des fins définies par le client.</span><span class="sxs-lookup"><span data-stu-id="8fe91-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="8fe91-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="8fe91-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="8fe91-129">[out] Pointeur vers l’état précédent du message.</span><span class="sxs-lookup"><span data-stu-id="8fe91-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8fe91-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8fe91-130">Return value</span></span>

<span data-ttu-id="8fe91-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fe91-131">S_OK</span></span> 
  
> <span data-ttu-id="8fe91-132">L’état du message a été correctement définie.</span><span class="sxs-lookup"><span data-stu-id="8fe91-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8fe91-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="8fe91-133">Remarks</span></span>

<span data-ttu-id="8fe91-134">La **méthode IMAPIFolder::SetMessageStatus** définit l’état du message sur la valeur stockée dans sa propriété **PR_MSG_STATUS** ([PidTagMessageStatus).](pidtagmessagestatus-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8fe91-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8fe91-135">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8fe91-135">Notes to implementers</span></span>

<span data-ttu-id="8fe91-136">La façon dont les bits d’état du message sont définies, effacées et utilisées dépend entièrement de votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être zéro.</span><span class="sxs-lookup"><span data-stu-id="8fe91-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="8fe91-137">L’implémentation de cette méthode par un fournisseur de transport distant doit suivre la sémantique décrite ici.</span><span class="sxs-lookup"><span data-stu-id="8fe91-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="8fe91-138">Il n’existe aucune considération particulière.</span><span class="sxs-lookup"><span data-stu-id="8fe91-138">There are no special considerations.</span></span> <span data-ttu-id="8fe91-139">Les clients utilisent cette méthode pour définir les bits MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE pour indiquer qu’un message particulier doit être téléchargé ou supprimé de la boutique de messages distante.</span><span class="sxs-lookup"><span data-stu-id="8fe91-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="8fe91-140">Un fournisseur de transport distant n’a pas besoin d’implémenter la méthode [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) associée.</span><span class="sxs-lookup"><span data-stu-id="8fe91-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="8fe91-141">Les clients doivent rechercher dans la table des matières du dossier pour déterminer l’état d’un message.</span><span class="sxs-lookup"><span data-stu-id="8fe91-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8fe91-142">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8fe91-142">Notes to callers</span></span>

<span data-ttu-id="8fe91-143">Vous pouvez utiliser la **propriété PR_MSG_STATUS** d’un message pour négocier une opération de verrouillage de message avec d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="8fe91-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="8fe91-144">Désignez un bit comme bit de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="8fe91-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="8fe91-145">Pour déterminer si le bit de verrouillage a été définie, examinez la valeur précédente pour l’état du message dans le paramètre _lpulOldStatus._</span><span class="sxs-lookup"><span data-stu-id="8fe91-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="8fe91-146">Utilisez les autres bits du paramètre  _ulNewStatus_ pour suivre l’état du message sans interférer avec le bit de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="8fe91-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fe91-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe91-147">See also</span></span>



[<span data-ttu-id="8fe91-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8fe91-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="8fe91-149">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8fe91-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="8fe91-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8fe91-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

