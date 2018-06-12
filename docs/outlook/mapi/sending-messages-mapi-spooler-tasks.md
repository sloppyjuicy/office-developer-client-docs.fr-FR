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
ms.openlocfilehash: ff40eddf63e67f45495e90c1a960e45b7cc6cfb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787122"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Envoi de Messages : T�ches de spouleur MAPI

  
  
**S’applique à**: Outlook 
  
Le spouleur MAPI est impliqu� dans le processus de transmission de message lors de la banque de messages pas fortement coupl�e � un fournisseur de transport, lorsque la banque �troitement coupl� et transport ne peut pas traiter un destinataire, et lorsque le message n�cessite un pr�traitement.
  
 **Apr�s tout pr�traitement n�cessaires, le spouleur MAPI effectue les �tapes suivantes :**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Est le fournisseur de transport envoyer le message à tous les destinataires qui ont leur propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) la valeur FALSE. 
    
3. Appelle la fonction appropriée ([RemovePreprocessInfo](removepreprocessinfo.md)) pour le nettoyage des informations supplémentaires qui a été ajoutées au message pour une utilisation pendant le prétraitement si la propriété **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) a été définie. This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - D�verrouille le message.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. Il copie ensuite le message dans le dossier identifié par l’identificateur d’entrée dans la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si ne pas remplacé par une messagerie crochet fournisseur envoie le traitement des messages. Enfin, il supprime le message si la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) a été définie sur TRUE. 
    

