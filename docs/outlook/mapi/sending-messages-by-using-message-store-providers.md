---
title: Envoi de messages via les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b34714a230adb44417624d149d34ed6a14a2dfa5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437608"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Envoi de messages via les fournisseurs de banques de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages ne sont pas tenus de prendre en charge les envois de messages sortants (autrement dit, la possibilité pour les applications clientes d’utiliser le fournisseur de magasin de messages pour envoyer des messages). Les applications clientes doivent utiliser un magasin de messages lors de l’envoi de messages, car les données du message doivent être stockées quelque part entre le moment où l’utilisateur a terminé de le composer et le moment où lepooler MAPI envoie le message à un fournisseur de transport pour l’envoi au système de messagerie sous-jacent. Si votre fournisseur de magasins de messages ne prend pas en charge les envois de messages sortants, il ne peut pas être utilisé comme magasin de messages par défaut.
  
Pour prendre en charge l’envoi de messages, votre fournisseur de magasins de messages doit :
  
- Implémenter une file d’attente de messages sortants.
    
- Prise en charge de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) sur les objets de message créés dans la magasin de messages. 
    
- Prendre en charge les méthodes **IMsgStore** spécifiques aupooler MAPI : [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)et [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
La **méthode SetLockState** est importante pour une interopérabilité appropriée entre lepooler MAPI et les clients. Lorsque lepooler MAPI appelle **SetLockState** sur un message sortant, le fournisseur de magasin de messages ne doit pas laisser les clients ouvrir le message. Si un client tente d’ouvrir un message verrouillé par lepooler MAPI, le fournisseur de la boutique de messages doit MAPI_E_NO_ACCESS. L’état verrouillé d’un message n’a pas besoin d’être persistant au cas où la boutique serait fermée pendant que le message serait verrouillé par lepooler MAPI. 
  
Que lepooler MAPI ait verrouillé ou non un message sortant, le fournisseur de la boutique de messages ne doit pas autoriser l’ouverture d’un message dans la file d’attente de messages sortants pour l’écriture. Si un client appelle la méthode [IMSgStore::OpenEntry](imsgstore-openentry.md) sur un message sortant avec l’indicateur MAPI_MODIFY, l’appel doit échouer et MAPI_E_SUBMITTED. Si une application cliente appelle **OpenEntry** sur un message sortant avec l’indicateur MAPI_BEST_ACCESS, le fournisseur de magasins de messages doit autoriser l’accès en lecture seule au message. 
  
Lorsqu’un message doit être géré par lepooler MAPI, le fournisseur de la boutique de messages définit la propriété **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) du message sur SUBMITFLAG_LOCKED. La SUBMITFLAG_LOCKED indique que lepooler MAPI a verrouillé le message pour son usage exclusif. L’autre valeur **pour PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, est définie lorsque le message nécessite un prétraitage par une ou plusieurs fonctions de préprocesseur inscrites par un fournisseur de transport.
  
Les procédures suivantes décrivent comment le magasin de messages, le transport et lepooler MAPI interagissent pour envoyer un message d’un client à un ou plusieurs destinataires. 
  
L’application cliente appelle [la méthode IMessage::SubmitMessage.](imessage-submitmessage.md) Dans **SubmitMessage,** le fournisseur de magasin de messages fait les choses suivantes :
  
1. Appelle [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). Si MAPI renvoie une erreur, le fournisseur de la boutique de messages renvoie cette erreur au client.
    
2. Définit le MSGFLAG_SUBMIT bit dans la **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.
    
3. Garantit qu’il existe une colonne pour la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) dans la table des destinataires et la définit sur FALSE pour indiquer qu’aucun transport n’a encore pris en charge la transmission du message.
    
4. Définit la date et l’heure d’origine dans **la propriété PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Appelle [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) pour : 
    
    1. D�veloppez toutes les listes de distribution personnelles et des destinataires personnalis�s et remplacez tous les noms d'affichage modifi� par leur nom d'origine.
        
    2. Supprimer les doublons.
        
    3. Vérifiez les prétraitons requis et, si le prétraitage est requis, définissez l’indicateur NEEDS_PREPROCESSING et la propriété **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), qui est réservée à MAPI. 
        
    4. D�finir l'indicateur NEEDS_SPOOLER si la banque de messages est fortement coupl�e � un type de transport et qu'il ne peut pas g�rer tous les destinataires. 
    
6. Ex�cute les t�ches suivantes si l'indicateur de message NEEDS_PREPROCESSING est d�fini :
    
    1. Place le message dans la file d’attente sortante avec SUBMITFLAG_PREPROCESS bits dans la **PR_SUBMIT_FLAGS** sortante. 
        
    2. Avertit le spouleur MAPI que la file d'attente a �t� modifi�e.
        
    3. Rend le contr�le au client et le flux de messages continue dans le spouleur MAPI. Le spouleur MAPI effectue les t�ches suivantes : 
    
       1. Verrouille le message en appelant [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Effectue le prétraitage nécessaire en appelant toutes les fonctions de prétraitation dans l’ordre d’inscription. Les fournisseurs de transport [appellent IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour enregistrer les fonctions de prétraitment. 
            
       3. Appelle [IMessage::SubmitMessage](imessage-submitmessage.md) sur le message ouvert pour indiquer à la boutique de messages que le prétraitement est terminé. 
    
S’il n’y a pas eu de prétraitement, ou s’il y a eu un prétraitement et que lepooler MAPI a appelé **SubmitMessage,** le fournisseur de magasin de messages fait les opérations suivantes dans le processus client : 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - G�re tous les destinataires pouvoir prendre en charge.
    
   - D�finit la propri�t� de **PR_RESPONSIBILITY** la valeur True pour tous les destinataires qu'il g�re. 
    
   - Ex�cute les t�ches suivantes si tous les destinataires sont connus � ce magasin �troitement coupl� et de transport : 
    
     - Appelle [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) si le message a été prétraité ou si le fournisseur de magasins de messages souhaite que lepooler MAPI termine le traitement des messages. Le flux de messages se poursuit avec lepooler MAPI. 
    
     - Effectue les tâches suivantes si le message n’a pas été prétraité ou si le fournisseur de la boutique de messages ne souhaite pas que lepooler MAPI termine le traitement des messages :
    
       1. Copie le message dans le dossier identifié par l’identificateur d’entrée dans la **propriété PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si elle est définie.
            
       2. Supprime le message si la **propriété PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) a été définie sur TRUE.
            
       3. Déverrouille le message s’il est verrouillé.
            
       4. Renvoie au client. Le flux de messages est terminé.
    
  - Effectue les tâches suivantes si le message a été prétraité ou si le fournisseur souhaite que lepooler MAPI termine le traitement des messages :
    
    1. Appelle [IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Continue le flux de messages avec lepooler MAPI. Pour plus d’informations, [voir Sending Messages: MAPI Spooler Tasks](sending-messages-mapi-spooler-tasks.md).
    
  - Effectue les tâches suivantes si le message n’a pas été prétraité ou si le fournisseur ne souhaite pas que lepooler termine le traitement des messages :
    
    1. Copie le message dans le dossier identifié par l’identificateur d’entrée dans **la propriété PR_SENTMAIL_ENTRYID, si** elle est définie. 
        
    2. Supprime le message si la **propriété PR_DELETE_AFTER_SUBMIT** a été définie sur TRUE. 
        
    3. Déverrouille le message s’il est verrouillé. 
        
    4. Renvoie à l’appelant. Le flux de messages est terminé.
    
- Ex�cute les t�ches suivantes si la banque de messages n'est pas �troitement coupl�e � un type de transport, pas tous les destinataires ont �t� connus pour la banque de messages ou l'indicateur NEEDS_SPOOLER est d�fini :
    
  1. Le message est plac� dans la file d'attente sortante sans d�finir le bit SUBMITFLAG_PREPROCESS dans la propri�t� **PR_SUBMIT_FLAGS**. 
    
  2. Avertit le spouleur MAPI que la file d'attente sortante a chang� en g�n�rant une notification de la table. 
    
  3. Renvoie au client et le flux des messages se poursuit avec un ensemble de t�ches effectu�es par le spouleur MAPI.
    
## <a name="see-also"></a>Voir aussi

- [Fonctionnalit�s de la banque de messages](message-store-features.md)

