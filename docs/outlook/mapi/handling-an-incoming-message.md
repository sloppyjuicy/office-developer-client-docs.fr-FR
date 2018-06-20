---
title: Gestion d’un message entrant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5705af6c8efaf42ae27d1b39bb28d162971ebf9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783421"
---
# <a name="handling-an-incoming-message"></a>Gestion d’un message entrant

**S’applique à**: Outlook 
  
Un message entrant est un message qui a été envoyé entre un ou plusieurs systèmes de messagerie. Il peut avoir envoyé qu’à vous ou à plusieurs autres destinataires. Les messages entrants sont placés dans un dossier de réception conçu pour stocker les messages d’une classe particulière. Vous pouvez configurer un autre dossier pour chaque classe de message que vous gérez ou utilisez un dossier pour toutes les classes de réception.
  
Si vous êtes inscrit pour les notifications de nouveau courrier avec la banque d’informations, vous serez averti chaque fois qu’un message est placé dans un dossier de réception. Si vous n’avez pas enregistré pour les notifications de nouveau courrier, vous devez ouvrir le dossier régulièrement pour vérifier manuellement l’arrivée de nouveaux messages de réception.
  
Clients s’inscrire pour les notifications de nouveau courrier en définissant les paramètres pour [IMsgStore::Advise](imsgstore-advise.md) comme suit : 
  
- Définissez _cbEntryID_ sur 0. 
    
- _LpEntryID_ la valeur NULL. 
    
- La valeur _ulEventMask_ fnevNewMail. 
    
Le paramètre _lpNotifications_ dans l’appel à la méthode **IMAPIAdviseSink::OnNotify** pointe vers un **NEWMAIL\_NOTIFICATION** structure qui contient des informations sur le message entrant, telles que sa classe de message, son entrée identificateur de l’identificateur d’entrée de son dossier parent et le contenu de sa propriété **PR_MESSAGE_FLAGS** . Pour plus d’informations sur l’enregistrement pour et gestion des notifications, voir [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) et [Gestion des Notifications](handling-notifications.md). 
  
Avant d’afficher un message entrant à un utilisateur, déterminez si sa classe de message est une classe qui prend en charge de votre client. Si ce n’est pas le cas, ignorez le message. Si la classe est pris en charge, vous pouvez ouvrir et afficher le message avec un formulaire qui est approprié pour la classe de message du message. Le choix de formulaires est basé sur la classe de message. Les messages qui appartiennent à la classe IPM utiliser un formulaire par défaut implémenté par MAPI. Les messages qui appartiennent à des classes personnalisées définies par les clients peuvent utiliser pour les formulaires spécialisés défini par le client ou le formulaire par défaut MAPI.
  
## <a name="open-and-display-an-incoming-message"></a>Ouvrir et afficher un message entrant
  
1. Appelez **IMsgStore::GetReceiveFolder** pour récupérer l’identificateur d’entrée du dossier de réception pour la classe de message du message et le secret de cet identificateur d’entrée pour **IMsgStore::OpenEntry** pour ouvrir le dossier. Pour plus d’informations, voir [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)et [l’ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).
    
2. Appelez la méthode de **IMAPIContainer::GetContentsTable** de réception du dossier pour récupérer la table des matières. Pour plus d’informations, voir [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Appelez la méthode la table **IMAPITable::QueryRows** pour récupérer toutes les lignes dans le tableau. Pour plus d’informations, voir [IMAPITable::QueryRows](imapitable-queryrows.md) et les [Tables des matières](contents-tables.md). Pour plus d’informations sur l’affichage d’une table des matières, voir [affichage d’une Table de contenu de dossier](displaying-a-folder-contents-table.md).
    
3. Si votre client est interactive, autorise l’utilisateur à sélectionner un message dans la table et de déterminer le formulaire à utiliser pour afficher ce message. Clients peuvent utiliser le formulaire par défaut fourni par MAPI ou d’un formulaire personnalisé. Pour plus d’informations, voir [Gestion des formulaires MAPI](handling-mapi-forms.md).
    
4. Appelez **IMsgStore::OpenEntry** pour ouvrir le message. Pour plus d’informations, consultez [ouverture d’un Message](opening-a-message.md).
    
5. Traiter le texte du message. Pour plus d’informations, voir [L’ouverture du message](opening-message-text.md).
    
6. Rendu de chacune des pièces jointes des messages. Pour plus d’informations, voir [rendu d’une pièce jointe en texte brut](rendering-an-attachment-in-plain-text.md) ou le [rendu d’une pièce jointe dans le texte RTF](rendering-an-attachment-in-rtf-text.md).
    
7. Ouvrez une pièce jointe si vous le souhaitez. Pour plus d’informations, voir [l’ouverture d’une pièce jointe](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Dans cette section

- [Texte du Message d’ouverture](opening-message-text.md): décrit comment ouvrir le texte du message.
    
- [Rendu d’une pièce jointe en texte brut](rendering-an-attachment-in-plain-text.md): décrit comment afficher une pièce jointe en texte brut.
    
- [Rendu d’une pièce jointe dans le texte RTF](rendering-an-attachment-in-rtf-text.md): décrit comment afficher une pièce jointe dans le texte mis en forme.
    
- [L’ouverture d’une pièce jointe](opening-an-attachment.md): décrit comment ouvrir une pièce jointe.
    

