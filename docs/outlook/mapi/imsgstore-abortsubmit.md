---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784253"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="3059f-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="3059f-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="3059f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3059f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3059f-105">Tente de supprimer un message de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="3059f-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3059f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3059f-106">Parameters</span></span>

 <span data-ttu-id="3059f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3059f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="3059f-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="3059f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3059f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3059f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="3059f-110">[in] Pointeur vers l’identificateur d’entrée du message à supprimer de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="3059f-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="3059f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3059f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="3059f-112">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="3059f-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3059f-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3059f-113">Return value</span></span>

<span data-ttu-id="3059f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3059f-114">S_OK</span></span> 
  
> <span data-ttu-id="3059f-115">Le message a été supprimé de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="3059f-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="3059f-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="3059f-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="3059f-117">Le message identifié par _lpEntryID_ n’est plus dans la file d’attente de la banque de messages sortants, en règle générale, car il a déjà été envoyé.</span><span class="sxs-lookup"><span data-stu-id="3059f-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="3059f-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="3059f-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="3059f-119">Le message identifié par _lpEntryID_ est verrouillé par le spouleur MAPI, et l’opération ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="3059f-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3059f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="3059f-120">Remarks</span></span>

<span data-ttu-id="3059f-121">La méthode **IMsgStore::AbortSubmit** tente de supprimer un message envoyé à partir de la file d’attente sortante de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="3059f-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3059f-122">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="3059f-122">Notes to callers</span></span>

<span data-ttu-id="3059f-123">Une fois un message est envoyé, abandon de l’envoi en appelant **AbortSubmit** est la seule action peut être effectuée sur le message.</span><span class="sxs-lookup"><span data-stu-id="3059f-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="3059f-124">Ne pensez pas **AbortSubmit** réussissent toujours.</span><span class="sxs-lookup"><span data-stu-id="3059f-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="3059f-125">Selon la façon dont le système de messagerie sous-jacent est implémenté, il est parfois pas possible d’annuler l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="3059f-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3059f-126">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3059f-126">MFCMAPI reference</span></span>

<span data-ttu-id="3059f-127">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3059f-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3059f-128">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3059f-128">**File**</span></span>|<span data-ttu-id="3059f-129">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3059f-129">**Function**</span></span>|<span data-ttu-id="3059f-130">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3059f-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3059f-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3059f-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="3059f-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="3059f-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="3059f-133">MFCMAPI utilise la méthode **IMsgStore::AbortSubmit** pour annuler l’envoi du message sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3059f-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3059f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3059f-134">See also</span></span>



[<span data-ttu-id="3059f-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="3059f-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="3059f-136">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3059f-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="3059f-137">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3059f-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

