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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427086"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="38e82-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="38e82-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="38e82-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38e82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38e82-105">Permet au fournisseur de magasin de messages d’effectuer un traitement sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="38e82-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="38e82-106">Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="38e82-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="38e82-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="38e82-107">Parameters</span></span>

 <span data-ttu-id="38e82-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38e82-108">_ulFlags_</span></span>
  
> <span data-ttu-id="38e82-109">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="38e82-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="38e82-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="38e82-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="38e82-111">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="38e82-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="38e82-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="38e82-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="38e82-113">[in] Pointeur vers l’identificateur d’entrée du message à traiter.</span><span class="sxs-lookup"><span data-stu-id="38e82-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38e82-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38e82-114">Return value</span></span>

<span data-ttu-id="38e82-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="38e82-115">S_OK</span></span> 
  
> <span data-ttu-id="38e82-116">Le traitement sur le message envoyé a réussi.</span><span class="sxs-lookup"><span data-stu-id="38e82-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="38e82-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="38e82-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="38e82-118">Le fournisseur de la boutique de messages ne prend pas en charge le traitement des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="38e82-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="38e82-119">Cette valeur d’erreur est renvoyée si l’appelant n’est pas lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="38e82-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38e82-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="38e82-120">Remarks</span></span>

<span data-ttu-id="38e82-121">La **méthode IMsgStore::FinishedMsg** effectue un traitement sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="38e82-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="38e82-122">Ce traitement peut impliquer la suppression du message, son déplacement vers un autre dossier ou les deux actions.</span><span class="sxs-lookup"><span data-stu-id="38e82-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="38e82-123">Le type de traitement varie selon que les propriétés **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) et **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sont définies.</span><span class="sxs-lookup"><span data-stu-id="38e82-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="38e82-124">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="38e82-124">Notes to implementers</span></span>

<span data-ttu-id="38e82-125">Dans votre implémentation de **FinishedMsg,** déverrouillez le message identifié par  _lpEntryID_ et effectuez le traitement approprié.</span><span class="sxs-lookup"><span data-stu-id="38e82-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="38e82-126">Le message cible est toujours verrouillé . lepooler MAPI ne transmet jamais l’identificateur d’entrée d’un message déverrouillé à **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="38e82-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="38e82-127">Il est possible qu’aucun **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** ne soit définie, que les deux soient définies ou que l’une ou l’autre soit définie.</span><span class="sxs-lookup"><span data-stu-id="38e82-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="38e82-128">Le tableau suivant décrit l’action que vous devez prendre en fonction des paramètres :</span><span class="sxs-lookup"><span data-stu-id="38e82-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38e82-129">Si aucune des deux propriétés n’est définie :</span><span class="sxs-lookup"><span data-stu-id="38e82-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="38e82-130">Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d’envoi).</span><span class="sxs-lookup"><span data-stu-id="38e82-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="38e82-131">Si les deux propriétés sont définies :</span><span class="sxs-lookup"><span data-stu-id="38e82-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="38e82-132">Déplacez le message dans le dossier indiqué, si vous le souhaitez, puis supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="38e82-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="38e82-133">Si PR_SENTMAIL_ENTRYID est définie :</span><span class="sxs-lookup"><span data-stu-id="38e82-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="38e82-134">Déplacez le message vers le dossier indiqué.</span><span class="sxs-lookup"><span data-stu-id="38e82-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="38e82-135">Si PR_DELETE_AFTER_SUBMIT est définie :</span><span class="sxs-lookup"><span data-stu-id="38e82-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="38e82-136">Supprimez le message.</span><span class="sxs-lookup"><span data-stu-id="38e82-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="38e82-137">Une fois que vous avez pris les mesures appropriées, appelez la méthode [IMAPISupport::D oSentMail.](imapisupport-dosentmail.md)</span><span class="sxs-lookup"><span data-stu-id="38e82-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38e82-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e82-138">See also</span></span>



[<span data-ttu-id="38e82-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="38e82-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="38e82-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="38e82-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

