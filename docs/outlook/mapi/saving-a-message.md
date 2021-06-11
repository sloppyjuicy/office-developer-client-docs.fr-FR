---
title: Enregistrement d’un message
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
# <a name="saving-a-message"></a>Enregistrement d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant l’enregistré, les clients appellent généralement la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour définir quelques propriétés en plus des propriétés de texte du message, des propriétés de pièce jointe, **de PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et des propriétés associées à la liste des destinataires.
  
Définissez **la PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sur une chaîne de caractères telle que IPM. Notez que décrit la classe du message sortant. Bien que les clients doivent **PR_MESSAGE_CLASS** sur tous les messages sortants, une valeur par défaut est fournie par le fournisseur de la boutique de messages si vous ne la définissez pas. La classe de message par défaut pour les messages sortants est IPM. 
  
Définissez MSGFLAG_UNSENT’indicateur de PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si vous le souhaitez, définissez également MSGFLAG_READ et MSGFLAG_UNMODIFIED indicateurs. La définition MSGFLAG_UNMODIFIED permet à un message sous composition de simuler un message remis. MSGFLAG_UNMODIFIED peuvent uniquement être définies par les clients avant qu’un message ait été enregistré pour la première fois. 
  
Lorsque vous êtes prêt à effectuer une copie permanente d’un message non envoyé, appelez [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message et toutes ses pièces jointes. Si vous avez l’intention d’envoyer le message immédiatement, vous n’avez pas besoin d’appeler **SaveChanges**. L’appel **à SubmitMessage** enregistre le message en interne dans le cadre de son traitement. 
  
Lorsque vous **appelez SaveChanges,** il est bon de spécifier l’indicateur KEEP_OPEN_READWRITE, ce qui permet de modifier le message ultérieurement. D’autres indicateurs settables incluent FORCE_SAVE, qui indique que le message ou la pièce jointe doit être fermé après la engagement des modifications, KEEP_OPEN_READONLY, qui indique qu’aucune autre modification ne sera apportée, et l’indicateur permettant au fournisseur de magasin de messages de traitement par lots des demandes clientes, MAPI_DEFERRED_ERRORS.
  
Il est essentiel d’appeler **SaveChanges** pour chaque pièce jointe du message avant d’appeler **SaveChanges** pour le message. Si vous ne parviennent pas à enregistrer une pièce jointe, elle n’est pas incluse dans le message lors de son envoi et n’apparaît pas dans la table des pièces jointes du message. Si vous ne parviennent pas à enregistrer le message après l’enregistrement de toutes les pièces jointes, le message et les pièces jointes seront perdus. 
  
Lorsque **SaveChanges est appelé,** le fournisseur de magasins de messages met à jour les propriétés suivantes : 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) répertorie tous les destinataires principaux.
    
- **PR_DISPLAY_TO** répertorie tous les destinataires en copie carbone. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) répertorie tous les destinataires en copie carbone non voyante.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** définit MSGFLAG_HASATTACH si une ou plusieurs pièces jointes ont été enregistrées et MSGFLAG_UNMODIFIED pour afficher que le message a changé. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contient la taille la plus actuelle du message.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) fournit l’accès à la table des pièces jointes.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) fournit l’accès à la table des destinataires.
    
Certaines propriétés de message sont généralement fournies par des clients ou des fournisseurs de services lors de la création d’un message. Si un client oublie de les définir, c’est au fournisseur de la boutique de messages de les mettre à jour au moment de l’appel de **SaveChanges.** Par exemple, si les propriétés **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) d’un message ont été définies lors de la création du message, elles n’ont pas besoin d’être modifiées au moment de l’enregistrer. Toutefois, les fournisseurs de magasins de messages qui oublient de les définir lors de la création du message doivent les définir la première fois que **SaveChanges** est appelé. 
  
Si **SaveChanges renvoie** MAPI_E_CORRUPT_DATA, supposons que les données enregistrées sont maintenant perdues. Les fournisseurs de magasins de messages qui utilisent un modèle client-serveur pour leur implémentation peuvent renvoyer cette valeur lorsqu’une connexion réseau est perdue ou que le serveur n’est pas en cours d’exécution. Avant de renvoyer une erreur à l’utilisateur, essayez d’écrire et d’enregistrer les données une deuxième fois en appelant **SetProps** suivi d’un autre appel à **SaveChanges**. Si les données sont mises en cache localement, cela ne doit pas être un problème. Toutefois, en l’absence de cache local ou si le deuxième appel **SaveChanges** échoue, affichez une erreur pour alerter l’utilisateur du problème. 
  

