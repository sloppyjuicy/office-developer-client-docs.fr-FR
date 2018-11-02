---
title: Envoi de Messages  T�ches de spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: eef65990637d9c164ffe75f682e01ed134510e32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570274"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="8911f-103">Envoi de Messages : T�ches de spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="8911f-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="8911f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8911f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8911f-105">Le spouleur MAPI est impliqu� dans le processus de transmission de message lors de la banque de messages pas fortement coupl�e � un fournisseur de transport, lorsque la banque �troitement coupl� et transport ne peut pas traiter un destinataire, et lorsque le message n�cessite un pr�traitement.</span><span class="sxs-lookup"><span data-stu-id="8911f-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="8911f-106">**Apr�s tout pr�traitement n�cessaires, le spouleur MAPI effectue les �tapes suivantes :**</span><span class="sxs-lookup"><span data-stu-id="8911f-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="8911f-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="8911f-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="8911f-108">Est le fournisseur de transport envoyer le message à tous les destinataires qui ont leur propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="8911f-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="8911f-109">Appelle la fonction appropriée ([RemovePreprocessInfo](removepreprocessinfo.md)) pour le nettoyage des informations supplémentaires qui a été ajoutées au message pour une utilisation pendant le prétraitement si la propriété **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) a été définie.</span><span class="sxs-lookup"><span data-stu-id="8911f-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="8911f-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="8911f-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="8911f-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="8911f-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="8911f-113">D�verrouille le message.</span><span class="sxs-lookup"><span data-stu-id="8911f-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="8911f-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="8911f-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="8911f-115">Il copie ensuite le message dans le dossier identifié par l’identificateur d’entrée dans la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si ne pas remplacé par une messagerie crochet fournisseur envoie le traitement des messages.</span><span class="sxs-lookup"><span data-stu-id="8911f-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="8911f-116">Enfin, il supprime le message si la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) a été définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="8911f-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

