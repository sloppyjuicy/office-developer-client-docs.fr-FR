---
title: Gestion d’un message entrant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f3fbe34793e3520b26b984f4bd6b14fbcab7a951
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299404"
---
# <a name="handling-an-incoming-message"></a>Gestion d’un message entrant

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un message entrant est un message qui a été envoyé à travers un ou plusieurs systèmes de messagerie. Il a peut-être été envoyé uniquement à vous ou à de nombreux autres destinataires. Les messages entrants sont placés dans un dossier de réception destiné à contenir les messages d'une classe particulière. Vous pouvez configurer un dossier de réception différent pour chaque classe de message que vous gérez ou utilisez un dossier pour toutes les classes.
  
Si vous avez enregistré des notifications de nouveau courrier avec la Banque de messages, vous serez averti dès qu'un message est placé dans un dossier de réception. Si vous ne vous êtes pas inscrit pour les notifications de nouveau courrier, vous devez ouvrir le dossier de réception approprié régulièrement pour vérifier manuellement l'arrivée de nouveaux messages.
  
Les clients s'inscrivent pour les notifications de nouveau courrier en définissant les paramètres sur [IMsgStore:: Advise](imsgstore-advise.md) comme suit: 
  
- Définissez _cbEntryID_ sur 0. 
    
- Définissez _lpEntryID_ sur null. 
    
- Définissez _ulEventMask_ sur fnevNewMail. 
    
Le paramètre _lpNotifications_ dans l'appel de votre méthode **IMAPIAdviseSink:: OnNotify** pointe vers une structure de **notification NEWMAIL\_** qui contient des informations sur le message entrant, telles que sa classe de message, son entrée identificateur, l'identificateur de l'entrée de son dossier parent et le contenu de sa propriété **PR_MESSAGE_FLAGS** . Pour plus d'informations sur l'inscription et la gestion des notifications, voir [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) et [gestion](handling-notifications.md)des notifications. 
  
Avant d'afficher un message entrant destiné à un utilisateur, déterminez si sa classe de message est une classe prise en charge par votre client. Si ce n'est pas le cas, ignorez le message. Si la classe est l'une des classes que vous prenez en charge, vous pouvez ouvrir et afficher le message avec un formulaire approprié pour la classe de message du message. Le choix des formulaires est basé sur la classe de message. Les messages qui appartiennent à la classe IPM utilisent un formulaire par défaut implémenté par MAPI. Les messages qui appartiennent à des classes personnalisées définies par des clients peuvent utiliser des formulaires spécialisés définis par le client ou le formulaire MAPI par défaut.
  
## <a name="open-and-display-an-incoming-message"></a>Ouvrir et afficher un message entrant
  
1. Appelez **IMsgStore:: GetReceiveFolder** pour récupérer l'identificateur d'entrée du dossier de réception pour la classe de message du message et transmettez cet identificateur d'entrée à **IMsgStore:: OpenEntry** pour ouvrir le dossier. Pour plus d'informations, voir [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md)et [ouverture d'un dossier de banque de messages](opening-a-message-store-folder.md).
    
2. Appelez la méthode **IMAPIContainer:: GetContentsTable** du dossier de réception pour extraire sa table des matières. Pour plus d'informations, voir [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md). Appelez la méthode **IMAPITable:: QueryRows** pour extraire toutes les lignes du tableau. Pour plus d'informations, consultez la rubrique [IMAPITable:: QueryRows](imapitable-queryrows.md) et [tables des matières](contents-tables.md). Pour plus d'informations sur l'affichage d'une table des matières, voir [affichage d'un tableau de contenu de dossier](displaying-a-folder-contents-table.md).
    
3. Si votre client est interactif, autorisez l'utilisateur à sélectionner un message dans le tableau et déterminez le formulaire à utiliser pour afficher ce message. Les clients peuvent utiliser le formulaire par défaut fourni par MAPI ou un formulaire personnalisé. Pour plus d'informations, consultez la rubrique [gestion des formulaires MAPI](handling-mapi-forms.md).
    
4. Appelez **IMsgStore:: OpenEntry** pour ouvrir le message. Pour plus d'informations, consultez [la rubrique ouverture d'un message](opening-a-message.md).
    
5. Traite le texte du message. Pour plus d'informations, consultez la rubrique ouverture d'un [texte de message](opening-message-text.md).
    
6. Affichez chacune des pièces jointes du message. Pour plus d'informations, consultez la rubrique [rendu d'une pièce jointe en texte brut](rendering-an-attachment-in-plain-text.md) ou [rendu d'une pièce jointe au format RTF](rendering-an-attachment-in-rtf-text.md).
    
7. Si vous le souhaitez, ouvrez une pièce jointe. Pour plus d'informations, consultez la rubrique [ouverture d'une pièce jointe](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Contenu de cette section

- [Ouverture du texte](opening-message-text.md)du message: décrit comment ouvrir le texte du message.
    
- [Rendu d'une pièce jointe en texte brut](rendering-an-attachment-in-plain-text.md): décrit comment afficher une pièce jointe en texte brut.
    
- [Rendu d'une pièce jointe au format RTF](rendering-an-attachment-in-rtf-text.md): décrit comment afficher une pièce jointe dans du texte mis en forme.
    
- [Ouverture d'une pièce jointe](opening-an-attachment.md): décrit comment ouvrir une pièce jointe.
    

