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
ms.openlocfilehash: d06523625a20760faec7a6c73a6beaef757818b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575076"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="b6283-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b6283-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="b6283-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6283-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6283-105">Définit l’état associé à un message (par exemple, si ce message est marqué pour suppression).</span><span class="sxs-lookup"><span data-stu-id="b6283-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="b6283-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6283-106">Parameters</span></span>

 <span data-ttu-id="b6283-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6283-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b6283-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b6283-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b6283-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6283-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b6283-110">[in] Pointeur vers l’identificateur d’entrée du message dont le statut est défini.</span><span class="sxs-lookup"><span data-stu-id="b6283-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="b6283-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="b6283-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="b6283-112">[in] Le nouveau statut à affecter.</span><span class="sxs-lookup"><span data-stu-id="b6283-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="b6283-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="b6283-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="b6283-114">[in] Masque de bits d’indicateurs qui est appliqué à l’état de nouveau et indique les indicateurs à définir.</span><span class="sxs-lookup"><span data-stu-id="b6283-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="b6283-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="b6283-115">The following flags can be set:</span></span>
    
<span data-ttu-id="b6283-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="b6283-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="b6283-117">Le message a été marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="b6283-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="b6283-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="b6283-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="b6283-119">Le message ne pas doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="b6283-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="b6283-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="b6283-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="b6283-121">Le message doit être affichée en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="b6283-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="b6283-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="b6283-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="b6283-123">Le message a été marqué pour suppression au niveau de la banque de messages à distance sans télécharger sur le client local.</span><span class="sxs-lookup"><span data-stu-id="b6283-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="b6283-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="b6283-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="b6283-125">Le message a été marqué pour téléchargement à partir de la banque de messages à distance au client local.</span><span class="sxs-lookup"><span data-stu-id="b6283-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="b6283-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="b6283-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="b6283-127">Le message a été marqué pour un usage défini par le client.</span><span class="sxs-lookup"><span data-stu-id="b6283-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="b6283-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="b6283-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="b6283-129">[out] Pointeur vers l’état précédent du message.</span><span class="sxs-lookup"><span data-stu-id="b6283-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6283-130">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b6283-130">Return value</span></span>

<span data-ttu-id="b6283-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6283-131">S_OK</span></span> 
  
> <span data-ttu-id="b6283-132">Le statut du message a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="b6283-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6283-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6283-133">Remarks</span></span>

<span data-ttu-id="b6283-134">La méthode **IMAPIFolder::SetMessageStatus** définit l’état de message à la valeur qui est stockée dans sa propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b6283-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b6283-135">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b6283-135">Notes to implementers</span></span>

<span data-ttu-id="b6283-136">Comment les bits d’état message définis, désactivées et utilisés dépendent complètement votre implémentation, sauf que les bits 0 à 15 sont réservés et doivent être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b6283-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="b6283-137">Implémentation d’un fournisseur de transport à distance de cette méthode doit suivre la sémantique décrite ici.</span><span class="sxs-lookup"><span data-stu-id="b6283-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="b6283-138">Il n’existe pas de considérations particulières.</span><span class="sxs-lookup"><span data-stu-id="b6283-138">There are no special considerations.</span></span> <span data-ttu-id="b6283-139">Les clients utilisent cette méthode pour définir les bits MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE pour indiquer qu’un message particulier doivent être téléchargées ou supprimé de la banque de messages à distance.</span><span class="sxs-lookup"><span data-stu-id="b6283-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="b6283-140">Un fournisseur de transport à distance ne dispose pas d’implémenter la méthode [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) associée.</span><span class="sxs-lookup"><span data-stu-id="b6283-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="b6283-141">Clients doivent rechercher dans le tableau de contenu du dossier pour déterminer l’état d’un message.</span><span class="sxs-lookup"><span data-stu-id="b6283-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b6283-142">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="b6283-142">Notes to callers</span></span>

<span data-ttu-id="b6283-143">Vous pouvez utiliser la propriété **PR_MSG_STATUS** d’un message de négocier une opération de verrouillage du message avec d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="b6283-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="b6283-144">Désigner un peu comme le bit de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="b6283-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="b6283-145">Pour déterminer si le bit de verrouillage a été défini, examinez la valeur précédente pour le statut du message dans le paramètre _lpulOldStatus_ .</span><span class="sxs-lookup"><span data-stu-id="b6283-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="b6283-146">Utilisez les autres fichiers binaires dans le paramètre _ulNewStatus_ pour effectuer le suivi du statut du message sans interférer avec le bit de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="b6283-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6283-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6283-147">See also</span></span>



[<span data-ttu-id="b6283-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b6283-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="b6283-149">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b6283-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="b6283-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b6283-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

