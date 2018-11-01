---
title: Envoi de Messages  T�ches de fournisseur de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4af052cdbd354d321a1d9e1dd0feb004501c8eb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587613"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Envoi de Messages : T�ches de fournisseur de banque de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
Le fournisseur de banque de messages d�termine s'il faut mettent en �uvre le spouleur MAPI. Si le fournisseur de banque de messages n'est pas fortement coupl�, le message n�cessite un pr�traitement, ou la banque �troitement coupl� et transport ne peuvent pas g�rer tous les destinataires, le spouleur MAPI doit �tre impliqu�. 
  
La proc�dure suivante d�crit les t�ches requises d'un fournisseur de banque de messages pour envoyer un message. 
  
**Dans IMessage::SubmitMessage, la banque de messages fournisseur**:
  
1. Appelle [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) si le message a l’indicateur MSGFLAG_RESEND dans sa propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) et renvoie des erreurs au client. **PrepareSubmit** vérifie la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de chaque destinataire dans la liste des destinataires du message.
    
   - Si l’indicateur MAPI_SUBMITTED est défini, indiquant que le destinataire n’a pas reçu le message d’origine, **PrepareSubmit** efface l’indicateur et définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) à TRUE. 
    
   - Si l'indicateur MAPI_SUBMITTED n'est pas d�fini, indiquant que le destinataire n'a re�u le message d'origine, **PrepareSubmit** modifie la propri�t� **PR_RECIPIENT_TYPE** MAPI_P1 et d�finit la propri�t� **PR_RESPONSIBILITY** sur TRUE et renvoie des erreurs g�n�r�es par **PrepareSubmit** au client. 
    
2. D�finit l'indicateur MSGFLAG_SUBMIT dans la propri�t� **PR_MESSAGE_FLAGS** du message. 
    
3. Permet de s'assurer qu'il est une colonne pour **PR_RESPONSIBILITY** dans la table de destinataires et lui affecte la valeur FALSE pour indiquer qu'aucun transport n'a de responsabilit� encore suppos�e pour transmettre le message. 
    
4. Définit la date et l’heure d’origine dans la propriété **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - D�veloppez toutes les listes de distribution personnelles et des destinataires personnalis�s et remplacez tous les noms d'affichage modifi� par leur nom d'origine.
   - Supprimer les doublons.
   - Recherchez tout prétraitement nécessaires et si prétraitement est requise, définir l’indicateur NEEDS_PREPROCESSING et la propriété **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), une propriété réservée pour MAPI. 
   - D�finir l'indicateur NEEDS_SPOOLER si la banque de messages est fortement coupl�e � un type de transport et qu'il ne peut pas g�rer tous les destinataires. 
    
6. Ex�cute les t�ches suivantes si l'indicateur de message NEEDS_PREPROCESSING est d�fini :
    
   - Place le message dans la file d’attente sortant avec le bit SUBMITFLAG_PREPROCESS défini dans la propriété **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)).
   - Avertit le spouleur MAPI que la file d'attente a �t� modifi�e.
   - Rend le contr�le au client et le flux de messages continue dans le spouleur MAPI. 
   - Le spouleur MAPI effectue les t�ches suivantes :
     - Verrouille le message en appelant IMsgStore::SetLockState. 
     - Effectue le prétraitement nécessaires en appelant toutes les fonctions de prétraitement dans l’ordre d’inscription. Fournisseurs de transport appellent IMAPISupport::RegisterPreprocessor à enregistrer les fonctions de prétraitement. 
     - Appelle IMessage::SubmitMessage sur le message ouvert pour indiquer à la banque de messages que le prétraitement est terminé.

<br/>

Les deux étapes suivantes se produisent dans le processus client si il n’a pas de prétraitement et lorsque le spouleur MAPI appelle **SubmitMessage** si il a été prétraitement. 

**La banque de messages fournisseur**:

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - G�re tous les destinataires pouvoir prendre en charge.
   - D�finit la propri�t� de **PR_RESPONSIBILITY** la valeur True pour tous les destinataires qu'il g�re. 
   - Ex�cute les t�ches suivantes si tous les destinataires sont connus � ce magasin �troitement coupl� et de transport :
     - Appelle IMAPISupport::CompleteMsg si le message a été prétraité ou la banque de messages fournisseur souhaite le spouleur MAPI pour effectuer le traitement des messages, ce qui est recommandé afin que la messagerie crochets peuvent être appelées. Flux des messages se poursuit avec le spouleur MAPI comme décrit dans la procédure suivante.  
     - Exécute les tâches suivantes si le message a été prétraité pas ou le fournisseur de banque de messages ne souhaite pas le spouleur MAPI pour effectuer le traitement des messages :
       - Copie le message vers le dossier identifié par l’identificateur d’entrée dans la propriété PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), s’il est défini.
       - Supprime le message si la propriété PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) a été définie sur TRUE.
       - Déverrouille le message s’il est verrouillé.
       - Renvoie au client. Flux de messages est terminé. 
   
2. Ex�cute les t�ches suivantes si la banque de messages n'est pas �troitement coupl�e � un type de transport, pas tous les destinataires ont �t� connus pour la banque de messages ou l'indicateur NEEDS_SPOOLER est d�fini :
    
   - Le message est plac� dans la file d'attente sortante sans d�finir le bit SUBMITFLAG_PREPROCESS dans la propri�t� **PR_SUBMIT_FLAGS**. 
   - Avertit le spouleur MAPI que la file d'attente sortante a chang� en g�n�rant une notification de la table. 
   - Renvoie au client et le flux des messages se poursuit avec un ensemble de t�ches effectu�es par le spouleur MAPI.
    
Lorsqu'un message doit �tre g�r�e par le spouleur MAPI, le fournisseur de banque de messages d�finit la propri�t� du message **PR_SUBMIT_FLAGS** � SUBMITFLAG_LOCKED. L'indicateur SUBMITFLAG_LOCKED indique que le spouleur MAPI a verrouill� le message pour son usage exclusif. L'autre valeur pour **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, est d�finie lorsque le message n�cessite un pr�traitement par une ou plusieurs fonctions pr�processeur enregistr�es par un fournisseur de transport. 
  

