---
title: Gestion d’un message entrant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 643e55871a94d5d4ef9707e1971f89b282ceec2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580159"
---
# <a name="handling-an-incoming-message"></a>Gestion d’un message entrant

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un message entrant est un message qui a été envoyé sur un ou plusieurs systèmes de messagerie. Il peut avoir été envoyé uniquement à vous ou à de nombreux autres destinataires. Les messages entrants sont placés dans un dossier de réception désigné pour contenir les messages d’une classe particulière. Vous pouvez configurer un dossier de réception différent pour chaque classe de message que vous traitez ou utilisez un dossier pour toutes les classes.
  
Si vous vous êtes inscrit à de nouvelles notifications par courrier électronique auprès de la boutique de messages, vous êtes averti chaque fois qu’un message est placé dans un dossier de réception. Si vous ne vous êtes pas inscrit aux nouvelles notifications par courrier électronique, vous devez ouvrir régulièrement le dossier de réception approprié pour vérifier manuellement l’arrivée de nouveaux messages.
  
Les clients s’inscrivent pour les nouvelles notifications par courrier électronique en paramétant les paramètres [sur IMsgStore::Advise](imsgstore-advise.md) comme suit : 
  
- Définissez  _cbEntryID_ sur 0. 
    
- Définissez  _lpEntryID_ sur NULL. 
    
- Définissez  _ulEventMask_ sur fnevNewMail. 
    
Le paramètre _lpNotifications_ dans l’appel à votre méthode **IMAPIAdviseSink::OnNotify** pointe vers une structure **DE \_ NOTIFICATION NEWMAIL** qui contient des informations sur le message entrant, telles que sa classe de message, son identificateur d’entrée, l’identificateur d’entrée de son dossier parent et le contenu de sa propriété **PR_MESSAGE_FLAGS.** Pour plus d’informations sur l’inscription et la gestion des notifications, voir [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) et [Handling Notifications](handling-notifications.md). 
  
Avant d’afficher un message entrant à un utilisateur, déterminez si sa classe de message est une classe que votre client prend en charge. Si ce n’est pas le cas, ignorez le message. Si la classe est prise en charge, vous pouvez ouvrir et afficher le message avec un formulaire approprié pour la classe de message du message. Le choix des formulaires est basé sur la classe de message. Les messages qui appartiennent à la classe IPM utilisent un formulaire par défaut implémenté par MAPI. Les messages qui appartiennent à des classes personnalisées définies par les clients peuvent utiliser des formulaires spécialisés définis par le client ou le formulaire MAPI par défaut.
  
## <a name="open-and-display-an-incoming-message"></a>Ouvrir et afficher un message entrant
  
1. Appelez **IMsgStore::GetReceiveFolder** pour récupérer l’identificateur d’entrée du dossier de réception pour la classe de message du message et passez cet identificateur d’entrée à **IMsgStore::OpenEntry** pour ouvrir le dossier. Pour plus d’informations, voir [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)et [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
2. Appelez la méthode **IMAPIContainer::GetContentsTable** du dossier de réception pour récupérer sa table des matières. Pour plus d’informations, [voir IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Appelez la méthode **IMAPITable::QueryRows** de la table pour récupérer toutes les lignes de la table. Pour plus d’informations, [voir IMAPITable::QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md). Pour plus d’informations sur l’affichage d’une table des matières, voir [Affichage d’une table des matières des dossiers.](displaying-a-folder-contents-table.md)
    
3. Si votre client est interactif, autorisez l’utilisateur à sélectionner un message dans la table et à déterminer le formulaire à utiliser pour afficher ce message. Les clients peuvent utiliser le formulaire par défaut fourni par MAPI ou un formulaire personnalisé. Pour plus d’informations, [voir Handling MAPI Forms](handling-mapi-forms.md).
    
4. Appelez **IMsgStore::OpenEntry** pour ouvrir le message. Pour plus d’informations, voir [Ouverture d’un message.](opening-a-message.md)
    
5. Traiter le texte du message. Pour plus d’informations, voir [l’ouverture du texte du message.](opening-message-text.md)
    
6. Restituer chacune des pièces jointes du message. Pour plus d’informations, voir [Rendu d’une pièce jointe en](rendering-an-attachment-in-plain-text.md) texte simple ou rendu [d’une pièce jointe en texte RTF.](rendering-an-attachment-in-rtf-text.md)
    
7. Ouvrez une pièce jointe si vous le souhaitez. Pour plus d’informations, [voir Ouverture d’une pièce jointe.](opening-an-attachment.md)
    
## <a name="in-this-section"></a>Dans cette section

- [Ouverture du texte](opening-message-text.md)du message : décrit comment ouvrir le texte du message.
    
- [Rendu d’une pièce jointe en texte simple](rendering-an-attachment-in-plain-text.md): décrit comment restituer une pièce jointe en texte simple.
    
- [Rendu d’une pièce jointe dans un](rendering-an-attachment-in-rtf-text.md)texte RTF : décrit comment restituer une pièce jointe dans du texte formaté.
    
- [Ouverture d’une](opening-an-attachment.md)pièce jointe : décrit comment ouvrir une pièce jointe.
    

