---
title: Fournisseurs de magasin d’envoi de messages à l’aide de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: aaba816ca7efab6cee939087a18332561f31b81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787111"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Fournisseurs de magasin d’envoi de messages à l’aide de message

**S’applique à**: Outlook 
  
Fournisseurs de banque de messages ne sont pas nécessaire pour prendre en charge les envois de messages sortants (autrement dit, la possibilité pour les applications clientes à utiliser le fournisseur de banque de messages pour envoyer des messages). Applications clientes doivent utiliser une banque de messages lors de l’envoi de messages, car les données du message doivent être stockée dans un endroit entre le moment où l’utilisateur a terminé compose il et l’heure à laquelle le spouleur MAPI donne le message à un fournisseur de transport pour envoi au système de messagerie sous-jacent. Si votre fournisseur de banque de messages n’accepte pas les envois de messages sortants, il ne peut être utilisé en tant que la banque de messages par défaut.
  
Pour prendre en charge d’envoi de messages, votre fournisseur de magasin de message procédez comme suit :
  
- Implémenter une file d’attente de messages sortants.
    
- Prise en charge de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) sur les objets de message dans la banque de messages. 
    
- Prendre en charge les méthodes **IMsgStore** qui sont spécifiques au spouleur MAPI : [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)et [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
La méthode **SetLockState** est importante pour l’interopérabilité appropriée entre les clients et le spouleur MAPI. Lorsque le spouleur MAPI appelle **SetLockState** sur un message sortant, le fournisseur de banque de message ne doit pas permettre aux clients d’ouvrir le message. Si un client essaie d’ouvrir un message qui est verrouillé par le spouleur MAPI, le fournisseur de banque de message doit renvoyer MAPI_E_NO_ACCESS. L’état de verrouillage d’un message ne dispose pas être persistante en cas d’arrêt de la banque d’informations pendant que le message est verrouillé par le spouleur MAPI. 
  
Quel que soit ou non le spouleur MAPI a verrouillé un message sortant, le fournisseur de banque de messages n’autorisez pas un message dans la file d’attente de message sortant pour être ouvert en écriture. Si un client appelle la méthode [IMSgStore::OpenEntry](imsgstore-openentry.md) sur un message sortant avec l’indicateur ne, l’appel doit échouer et retourner MAPI_E_SUBMITTED. Si une application cliente appelle **OpenEntry** sur un message sortant avec l’indicateur MAPI_BEST_ACCESS, le fournisseur de banque de message doit autoriser l’accès en lecture seule au message. 
  
Lorsqu’un message doit être gérés par le spouleur MAPI, le fournisseur de banque de messages définit la propriété du message **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) sur SUBMITFLAG_LOCKED. La valeur SUBMITFLAG_LOCKED indique que le spouleur MAPI a verrouillé le message pour son usage exclusif. L’autre valeur pour **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, est définie lorsque le message nécessite un prétraitement par une ou plusieurs fonctions préprocesseur enregistrées par un fournisseur de transport.
  
Les procédures suivantes décrivent l’interagissent entre la banque de messages, de transport et spouleur MAPI pour envoyer un message à partir d’un client à un ou plusieurs destinataires. 
  
L’application cliente appelle la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . Dans **SubmitMessage**, le fournisseur de banque de messages effectue les opérations suivantes :
  
1. Appelle [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). Si MAPI renvoie une erreur, le fournisseur de banque de message renvoie cette erreur au client.
    
2. Définit le bit dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message MSGFLAG_SUBMIT.
    
3. S’assurer qu’il est une colonne de la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) dans la table de destinataires et lui affecte la valeur FALSE pour indiquer qu’aucun transport n’a encore la responsabilité de transmission de message.
    
4. Définit la date et l’heure d’origine dans la propriété **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Appelle [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) pour effectuer les opérations suivantes : 
    
    1. D�veloppez toutes les listes de distribution personnelles et des destinataires personnalis�s et remplacez tous les noms d'affichage modifi� par leur nom d'origine.
        
    2. Supprimer les doublons.
        
    3. Recherchez tout prétraitement requis et, si le prétraitement est requise, définir l’indicateur NEEDS_PREPROCESSING et la propriété **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), qui est réservée pour MAPI. 
        
    4. D�finir l'indicateur NEEDS_SPOOLER si la banque de messages est fortement coupl�e � un type de transport et qu'il ne peut pas g�rer tous les destinataires. 
    
6. Ex�cute les t�ches suivantes si l'indicateur de message NEEDS_PREPROCESSING est d�fini :
    
    1. Place le message dans la file d’attente sortant avec le bit SUBMITFLAG_PREPROCESS défini dans la propriété **PR_SUBMIT_FLAGS** . 
        
    2. Avertit le spouleur MAPI que la file d'attente a �t� modifi�e.
        
    3. Rend le contr�le au client et le flux de messages continue dans le spouleur MAPI. Le spouleur MAPI effectue les t�ches suivantes : 
    
       1. Verrouille le message en appelant [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Effectue le prétraitement nécessaires en appelant toutes les fonctions de prétraitement dans l’ordre d’inscription. Fournisseurs de transport appellent [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour enregistrer les fonctions de prétraitement. 
            
       3. Appels [IMessage::SubmitMessage](imessage-submitmessage.md) sur le message pour indiquer au message ouvert stocker ce prétraitement est terminée. 
    
Si il n’a pas de prétraitement, ou il a été prétraitement et le spouleur MAPI appelé **SubmitMessage**, le fournisseur de banque de messages effectue les opérations suivantes dans le processus client : 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - G�re tous les destinataires pouvoir prendre en charge.
    
   - D�finit la propri�t� de **PR_RESPONSIBILITY** la valeur True pour tous les destinataires qu'il g�re. 
    
   - Ex�cute les t�ches suivantes si tous les destinataires sont connus � ce magasin �troitement coupl� et de transport : 
    
     - Appelle [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) si le message a été prétraité ou le fournisseur de banque de messages souhaite le spouleur MAPI au traitement du message terminée. Flux des messages se poursuit avec le spouleur MAPI. 
    
     - Exécute les tâches suivantes si le message a été prétraité pas ou le fournisseur de banque de messages ne souhaite pas le spouleur MAPI pour effectuer le traitement des messages :
    
       1. Copie le message vers le dossier identifié par l’identificateur d’entrée dans la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), s’il est défini.
            
       2. Supprime le message si la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) a été définie sur TRUE.
            
       3. Déverrouille le message s’il est verrouillé.
            
       4. Renvoie au client. Flux de messages est terminé.
    
  - Exécute les tâches suivantes si le message a été prétraité ou le fournisseur souhaite le spouleur MAPI pour effectuer le traitement des messages :
    
    1. Appelle [IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Poursuit le flux des messages avec le spouleur MAPI. Pour plus d’informations, voir [envoi de Messages : tâches de spouleur MAPI](sending-messages-mapi-spooler-tasks.md).
    
  - Exécute les tâches suivantes si le message a été prétraité pas ou le fournisseur ne souhaite pas le spouleur pour effectuer le traitement des messages :
    
    1. Copie le message vers le dossier identifié par l’identificateur d’entrée dans la propriété **PR_SENTMAIL_ENTRYID** , s’il est défini. 
        
    2. Supprime le message si la propriété **PR_DELETE_AFTER_SUBMIT** a été définie sur TRUE. 
        
    3. Déverrouille le message s’il est verrouillé. 
        
    4. Retourne à l’appelant. Flux de messages est terminé.
    
- Ex�cute les t�ches suivantes si la banque de messages n'est pas �troitement coupl�e � un type de transport, pas tous les destinataires ont �t� connus pour la banque de messages ou l'indicateur NEEDS_SPOOLER est d�fini :
    
  1. Le message est plac� dans la file d'attente sortante sans d�finir le bit SUBMITFLAG_PREPROCESS dans la propri�t� **PR_SUBMIT_FLAGS**. 
    
  2. Avertit le spouleur MAPI que la file d'attente sortante a chang� en g�n�rant une notification de la table. 
    
  3. Renvoie au client et le flux des messages se poursuit avec un ensemble de t�ches effectu�es par le spouleur MAPI.
    
## <a name="see-also"></a>Voir aussi

- [Fonctionnalit�s de la banque de messages](message-store-features.md)

