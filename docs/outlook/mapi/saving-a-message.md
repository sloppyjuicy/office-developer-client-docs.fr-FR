---
title: L’enregistrement d’un Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e61a72691309b2ac632b764c0607f5b1e36b291b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787046"
---
# <a name="saving-a-message"></a>L’enregistrement d’un Message

  
  
**S’applique à**: Outlook 
  
Avant l’enregistrée d’un message, clients appellent généralement la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour définir plusieurs propriétés en plus des propriétés de texte de message, les propriétés de pièce jointe, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et les propriétés associée à la liste des destinataires.
  
Définissez la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) à une chaîne de caractères comme IPM. Notez que décrit la classe de message sortant. Bien que les clients doivent définir **PR_MESSAGE_CLASS** sur tous les messages sortants, une valeur par défaut est fournie par le fournisseur de banque de message si vous ne le définissez pas. La classe de message par défaut pour les messages sortants est IPM. 
  
Définir l’indicateur MSGFLAG_UNSENT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si vous le souhaitez, définissez également les indicateurs MSGFLAG_READ et MSGFLAG_UNMODIFIED. Définition de la MSGFLAG_UNMODIFIED permet à un message dans la composition simuler un message remis. MSGFLAG_UNMODIFIED peut uniquement être définie par les clients avant un message a été enregistré pour la première fois. 
  
Lorsque vous êtes prêt à effectuer une copie d’un message en attente permanente, appelez [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message et toutes ses pièces jointes. Si vous souhaitez envoyer le message immédiatement, il est inutile d’appeler **SaveChanges**. En interne, l’appel à **SubmitMessage** enregistre le message dans le cadre de son traitement. 
  
Lorsque vous appelez **SaveChanges**, il est conseillé de spécifier l’indicateur KEEP_OPEN_READWRITE, ce qui autorise le message de modification à une date ultérieure. Autres indicateurs définissables incluent FORCE_SAVE, ce qui indique que le message ou une pièce jointe doit être fermé une fois que les modifications soient validées, KEEP_OPEN_READONLY, ce qui indique qu’aucune modification ne seront, et l’indicateur pour autoriser le fournisseur de banque de messages à traitement par lots des demandes des clients, MAPI_DEFERRED_ERRORS.
  
Il est essentiel que vous appelez **SaveChanges** pour chaque pièce jointe dans le message avant d’appeler **SaveChanges** pour le message. Si vous ne parvenez pas à enregistrer une pièce jointe, la pièce jointe ne sera pas incluse dans le message lorsqu’il est envoyé et il n’apparaît pas dans la table des pièces jointes du message. Si vous ne parvenez pas à enregistrer le message après avoir enregistré toutes les pièces jointes, le message et les pièces jointes seront perdues. 
  
Lorsque **SaveChanges** est appelée, le fournisseur de banque de messages met à jour les propriétés suivantes : 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) répertorie tous les destinataires principales.
    
- **PR_DISPLAY_TO** répertorie tous les destinataires en copie carbone. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) répertorie tous les destinataires en copie carbone invisible.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** définit MSGFLAG_HASATTACH si une ou plusieurs pièces jointes ont été enregistrées et efface MSGFLAG_UNMODIFIED pour afficher que le message a été modifié. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contient la taille du message plus récente.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) permet d’accéder à la table des pièces jointes.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) permet d’accéder à la table de destinataires.
    
Certaines propriétés de message sont généralement fournies par les clients ou fournisseurs de services lors de la création d’un message. Si un client oublie leur définition, il est le fournisseur de magasin de message pour les mettre à jour en temps **que SaveChanges** est appelée. Par exemple, si **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et des propriétés **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) d’un message ont été définies lorsque le message a été créé, ils ne doivent pas être modifiés à gagner du temps. Toutefois, les fournisseurs de magasins de message négligent les définir lors de la création du message doivent les définir la première fois **SaveChanges** est appelée. 
  
Si **SaveChanges** renvoie MAPI_E_CORRUPT_DATA, partent du principe que les données enregistrées sont maintenant perdu. Les fournisseurs de magasins de message qui utilisent un modèle client-serveur de mise en oeuvre peuvent retourner cette valeur lorsqu’une connexion réseau est perdue ou le serveur n’est pas en cours d’exécution. Avant de retourner une erreur à l’utilisateur, essayez d’écrire et enregistrer les données d’une deuxième fois en effectuant un appel à **SetProps** suivi par un autre appel à **SaveChanges**. Si les données sont mis en cache localement, il ne doit pas être un problème. Toutefois, si aucun cache local ou si l’appel de **SaveChanges** deuxième échoue, affiche une erreur pour avertir l’utilisateur au problème. 
  

