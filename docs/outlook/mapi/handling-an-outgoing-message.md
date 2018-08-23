---
title: Gestion d’un message sortant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3f3330c132abdf35d0e4f67775c03f7d2e9fcc76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563988"
---
# <a name="handling-an-outgoing-message"></a>Gestion d’un message sortant

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un message sortant est un message qui peut être envoyé à un ou plusieurs destinataires via un ou plusieurs systèmes de messagerie ou être publié dans un dossier dans une banque de messages.
  
## <a name="create-and-send-an-outgoing-message"></a>Créer et envoyer un message sortant
  
1. Ouvrez la banque de messages par défaut. Pour plus d’informations, voir [l’ouverture d’une banque de messages](opening-a-message-store.md) et de [l’ouverture de la banque de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier boîte d’envoi. Pour plus d’informations, consultez [ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).
    
3. Appeler la méthode de **IMAPIFolder::CreateMessage** du dossier boîte d’envoi pour créer le nouveau message. Pour plus d’informations, voir [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Créer une liste de destinataires avec un ou plusieurs destinataires résolus. Pour plus d’informations, voir [Création d’une liste de destinataires](creating-a-recipient-list.md).
    
5. Si vous le souhaitez, ajoutez un objet. Pour plus d’informations, consultez [Création d’un objet du Message](creating-a-message-subject.md).
    
6. Ajoutez le texte du message. Pour plus d’informations, voir [Création de texte du Message](creating-message-text.md).
    
7. Si le texte du message est mis en forme, ajouter des informations de rendu. Pour plus d’informations, voir [Ajout d’informations d’affichage au texte mis en forme](adding-rendering-information-to-formatted-text.md).
    
8. Si vous le souhaitez, ajoutez une ou plusieurs pièces jointes. Pour plus d’informations, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).
    
9. Définir d’autres propriétés de message comme vous le souhaitez puis enregistrer et envoyer le message en appelant **IMessage::SubmitMessage**. Pour plus d’informations, voir [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Supprimer le message envoyé si le **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) propriété a la valeur TRUE ou les déplacer vers le dossier identifié par la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Pour plus d’informations, voir [traitement d’un Message envoyé](processing-a-sent-message.md).
    
Si vous souhaitez intermittantly enregistrer le message avant de l’envoyer, appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message. Pour plus d’informations, consultez la rubrique, [L’enregistrement d’un Message](saving-a-message.md) ou [l’envoi d’un Message](sending-a-message.md). 
  
## <a name="in-this-section"></a>Dans cette section

- [Création d’une liste de destinataires](creating-a-recipient-list.md): explique comment créer une liste de destinataires.
    
- [Création d’un objet du Message](creating-a-message-subject.md): explique comment créer un objet facultative pour un message.
    
- [Création de texte du Message](creating-message-text.md): explique comment créer le texte du message.
    
- [Ajout d’informations d’affichage au texte mis en forme](adding-rendering-information-to-formatted-text.md): décrit où dans le texte mis en forme une pièce jointe doit être affiché.
    
- [Création d’une pièce jointe](creating-a-message-attachment.md): décrit comment créer des pièces jointes.
    
- [L’enregistrement d’un Message](saving-a-message.md): décrit comment enregistrent les messages clients.
    
- [Envoi d’un Message](sending-a-message.md): comment faire envoyer un message.
    
- [Traitement d’un Message envoyé](processing-a-sent-message.md): décrit l’envoi de messages peuvent être traités.
    

