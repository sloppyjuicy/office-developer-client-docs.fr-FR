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
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420198"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Envoi de messages: tâches du spouleur MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le spouleur MAPI est impliqu� dans le processus de transmission de message lors de la banque de messages pas fortement coupl�e � un fournisseur de transport, lorsque la banque �troitement coupl� et transport ne peut pas traiter un destinataire, et lorsque le message n�cessite un pr�traitement.
  
 **Apr�s tout pr�traitement n�cessaires, le spouleur MAPI effectue les �tapes suivantes :**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Le fournisseur de transport envoie le message à tous les destinataires dont la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) a la valeur false. 
    
3. Appelle la fonction appropriée ([RemovePreprocessInfo](removepreprocessinfo.md)) pour nettoyer les informations supplémentaires qui ont été ajoutées au message afin de les utiliser lors du prétraitement si la propriété **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) a été définie. This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - D�verrouille le message.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. Il copie ensuite le message dans le dossier identifié par l'identificateur d'entrée dans la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), s'il n'est pas remplacé par un traitement de message envoyé par un fournisseur de hook de messagerie. Enfin, il supprime le message si la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) a été définie sur true. 
    

