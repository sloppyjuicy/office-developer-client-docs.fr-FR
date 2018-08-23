---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589951"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="90cac-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="90cac-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="90cac-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90cac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90cac-105">Active le fournisseur de banque de messages effectuer le traitement sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="90cac-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="90cac-106">Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="90cac-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="90cac-107">Param�tres</span><span class="sxs-lookup"><span data-stu-id="90cac-107">Parameters</span></span>

 <span data-ttu-id="90cac-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90cac-108">_ulFlags_</span></span>
  
> <span data-ttu-id="90cac-109">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="90cac-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="90cac-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="90cac-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="90cac-111">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="90cac-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="90cac-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="90cac-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="90cac-113">[in] Pointeur vers l’identificateur d’entrée du message à traiter.</span><span class="sxs-lookup"><span data-stu-id="90cac-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90cac-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="90cac-114">Return value</span></span>

<span data-ttu-id="90cac-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="90cac-115">S_OK</span></span> 
  
> <span data-ttu-id="90cac-116">Traitement sur le message envoyé a réussi.</span><span class="sxs-lookup"><span data-stu-id="90cac-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="90cac-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="90cac-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="90cac-118">Le fournisseur de banque de messages ne gère pas le traitement du message envoyé.</span><span class="sxs-lookup"><span data-stu-id="90cac-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="90cac-119">Cette valeur d’erreur est renvoyée si l’appelant n’est pas le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="90cac-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90cac-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="90cac-120">Remarks</span></span>

<span data-ttu-id="90cac-121">La méthode **IMsgStore::FinishedMsg** effectue un traitement dans un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="90cac-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="90cac-122">Ce traitement peut impliquer la suppression du message, son déplacement vers un autre dossier, ou les deux actions.</span><span class="sxs-lookup"><span data-stu-id="90cac-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="90cac-123">Le type de traitement dépend si les **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) et les propriétés de **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sont définies.</span><span class="sxs-lookup"><span data-stu-id="90cac-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="90cac-124">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="90cac-124">Notes to implementers</span></span>

<span data-ttu-id="90cac-125">Dans votre implémentation de **FinishedMsg**, déverrouiller le message identifié par _lpEntryID_ et effectuer le traitement approprié.</span><span class="sxs-lookup"><span data-stu-id="90cac-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="90cac-126">Le message cible doit toujours être verrouillé ; le spouleur MAPI passe jamais l’identificateur d’entrée pour un message déverrouillé à **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="90cac-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="90cac-127">Il est possible que **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** est définie, les deux sont définies, ni une ou l’autre est défini.</span><span class="sxs-lookup"><span data-stu-id="90cac-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="90cac-128">Le tableau suivant décrit l’action que vous devez prendre en fonction des paramètres :</span><span class="sxs-lookup"><span data-stu-id="90cac-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90cac-129">Si aucune propriété n’est définie :</span><span class="sxs-lookup"><span data-stu-id="90cac-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="90cac-130">Laissez le message dans le dossier à partir de laquelle il a été envoyé (généralement la boîte d’envoi).</span><span class="sxs-lookup"><span data-stu-id="90cac-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="90cac-131">Si les deux propriétés sont définies :</span><span class="sxs-lookup"><span data-stu-id="90cac-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="90cac-132">Déplacer le message vers le dossier indiqué, si vous le souhaitez, puis supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="90cac-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="90cac-133">Si PR_SENTMAIL_ENTRYID est défini :</span><span class="sxs-lookup"><span data-stu-id="90cac-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="90cac-134">Déplacer le message vers le dossier indiqué.</span><span class="sxs-lookup"><span data-stu-id="90cac-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="90cac-135">Si PR_DELETE_AFTER_SUBMIT est défini :</span><span class="sxs-lookup"><span data-stu-id="90cac-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="90cac-136">Supprimer le message.</span><span class="sxs-lookup"><span data-stu-id="90cac-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="90cac-137">Après avoir mis quelque action est appropriée, appelez la méthode de [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) .</span><span class="sxs-lookup"><span data-stu-id="90cac-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90cac-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90cac-138">See also</span></span>



[<span data-ttu-id="90cac-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="90cac-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="90cac-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="90cac-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

