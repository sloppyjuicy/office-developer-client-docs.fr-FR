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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414381"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="0039f-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="0039f-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="0039f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0039f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0039f-105">Tente de supprimer un message de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="0039f-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0039f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0039f-106">Parameters</span></span>

 <span data-ttu-id="0039f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0039f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0039f-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="0039f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0039f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0039f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0039f-110">[in] Pointeur vers l’identificateur d’entrée du message à supprimer de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="0039f-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="0039f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0039f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="0039f-112">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="0039f-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0039f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0039f-113">Return value</span></span>

<span data-ttu-id="0039f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0039f-114">S_OK</span></span> 
  
> <span data-ttu-id="0039f-115">Le message a été supprimé de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="0039f-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="0039f-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="0039f-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="0039f-117">Le message identifié par  _lpEntryID_ ne se trouve plus dans la file d’attente sortante de la boutique de messages, généralement parce qu’il a déjà été envoyé.</span><span class="sxs-lookup"><span data-stu-id="0039f-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="0039f-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="0039f-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="0039f-119">Le message identifié par  _lpEntryID_ est verrouillé par lepooler MAPI et l’opération ne peut pas être abandonnée.</span><span class="sxs-lookup"><span data-stu-id="0039f-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0039f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="0039f-120">Remarks</span></span>

<span data-ttu-id="0039f-121">La **méthode IMsgStore::AbortSubmit** tente de supprimer un message envoyé de la file d’attente sortante de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="0039f-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0039f-122">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="0039f-122">Notes to callers</span></span>

<span data-ttu-id="0039f-123">Une fois qu’un message est envoyé, l’abandon de la soumission en appelant **AbortSubmit** est la seule action qui peut être effectuée sur le message.</span><span class="sxs-lookup"><span data-stu-id="0039f-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="0039f-124">Ne vous attendez **pas à ce que AbortSubmit** réussisse toujours.</span><span class="sxs-lookup"><span data-stu-id="0039f-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="0039f-125">Selon la façon dont le système de messagerie sous-jacent est implémenté, il peut être impossible d’annuler l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="0039f-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0039f-126">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0039f-126">MFCMAPI reference</span></span>

<span data-ttu-id="0039f-127">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0039f-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0039f-128">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0039f-128">**File**</span></span>|<span data-ttu-id="0039f-129">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0039f-129">**Function**</span></span>|<span data-ttu-id="0039f-130">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0039f-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0039f-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0039f-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="0039f-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="0039f-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="0039f-133">MFCMAPI utilise la méthode **IMsgStore::AbortSubmit** pour abandonner l’envoi du message sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0039f-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0039f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0039f-134">See also</span></span>



[<span data-ttu-id="0039f-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0039f-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="0039f-136">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0039f-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="0039f-137">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="0039f-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

