---
title: Enregistrement d'un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420930"
---
# <a name="saving-a-message"></a>Enregistrement d'un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant qu'un message ne soit enregistré, les clients appellent généralement la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) du message pour définir quelques propriétés en plus des propriétés Text du message, des propriétés des pièces jointes, des **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et des propriétés. associé à la liste des destinataires.
  
Définissez la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sur une chaîne de caractères telle que IPM. Notez que décrit la classe du message sortant. Bien que les clients doivent définir **PR_MESSAGE_CLASS** sur tous les messages sortants, une valeur par défaut est fournie par le fournisseur de banque de messages si vous ne le configurez pas. La classe de message par défaut pour les messages sortants est IPM. 
  
Définissez l'indicateur MSGFLAG_UNSENT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si vous le souhaitez, définissez également les indicateurs MSGFLAG_READ et MSGFLAG_UNMODIFIED. La définition de MSGFLAG_UNMODIFIED permet à un message en cours de composition de simuler un message remis. MSGFLAG_UNMODIFIED ne peut être défini que par les clients avant la première sauvegarde d'un message. 
  
Lorsque vous êtes prêt à créer une copie permanente d'un message non envoyé, appelez [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur le message et toutes ses pièces jointes. Si vous envisagez d'envoyer le message immédiatement, il n'est pas nécessaire d'appeler **SaveChanges**. L'appel à **SubmitMessage** enregistre en interne le message dans le cadre de son traitement. 
  
Lors de l'appel de **SaveChanges**, il est recommandé de spécifier l'indicateur KEEP_OPEN_READWRITE, qui permet de modifier le message ultérieurement. D'autres indicateurs définissables incluent FORCE_SAVE, qui indique que le message ou la pièce jointe doit être fermé une fois les modifications validées, KEEP_OPEN_READONLY, qui indique qu'aucune autre modification ne sera apportée, et l'indicateur pour autoriser le fournisseur de banque de messages à demandes de client par lots, MAPI_DEFERRED_ERRORS.
  
Avant d'appeler **SaveChanges** pour le message, il est essentiel d'appeler **SaveChanges** pour chaque pièce jointe du message. Si vous ne parvenez pas à enregistrer une pièce jointe, elle ne sera pas incluse dans le message lors de son envoi et n'apparaîtra pas dans la table des pièces jointes du message. Si vous ne parvenez pas à enregistrer le message après avoir enregistré toutes les pièces jointes, le message et les pièces jointes seront perdus. 
  
Lorsque **SaveChanges** est appelé, le fournisseur de banque de messages met à jour les propriétés suivantes: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) répertorie tous les destinataires principaux.
    
- **PR_DISPLAY_TO** répertorie tous les destinataires de copie carbone. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) répertorie tous les destinataires en copie carbone invisible.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** définit MSGFLAG_HASATTACH si une ou plusieurs pièces jointes ont été enregistrées et efface MSGFLAG_UNMODIFIED pour afficher le message a été modifié. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contient la taille de message la plus récente.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) permet d'accéder au tableau des pièces jointes.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) fournit l'accès à la table de destinataires.
    
Certaines propriétés de message sont généralement fournies par des clients ou des fournisseurs de services lors de la création d'un message. Si un client oublie de les définir, il revient au fournisseur de banque de messages de les mettre à jour au moment de l'appel de **SaveChanges** . Par exemple, si les propriétés **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) d'un message ont été définies lors de la création du message, elles n'ont pas besoin d'être modifiées lors de l'enregistrement. Toutefois, les fournisseurs de banque de messages qui négligent de les définir lors de la création de messages doivent les définir lors du premier appel de **SaveChanges** . 
  
Si **SaveChanges** renvoie MAPI_E_CORRUPT_DATA, partez du principe que les données enregistrées sont maintenant perdues. Les fournisseurs de banques de messages qui utilisent un modèle de serveur client pour leur implémentation peuvent renvoyer cette valeur lorsqu'une connexion réseau est perdue ou que le serveur n'est pas en cours d'exécution. Avant de renvoyer une erreur à l'utilisateur, essayez d'écrire et d'enregistrer les données une seconde fois en appelant **SetProps** suivi d'un autre appel à **SaveChanges**. Si les données sont mises en cache localement, cela ne doit pas être un problème. Toutefois, s'il n'y a pas de cache local ou si le deuxième appel de **SaveChanges** échoue, affiche une erreur pour alerter l'utilisateur. 
  

