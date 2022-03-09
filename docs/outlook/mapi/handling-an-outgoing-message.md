---
title: Gestion d’un message sortant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
ms.openlocfilehash: 5e00c1a91ae7522cb356621b287f0465f6759d9a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381270"
---
# <a name="handling-an-outgoing-message"></a>Gestion d’un message sortant

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un message sortant est un message qui peut être envoyé à un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie ou être publié dans un dossier dans une magasin de messages.
  
## <a name="create-and-send-an-outgoing-message"></a>Créer et envoyer un message sortant
  
1. Ouvrez la boutique de messages par défaut. Pour plus d’informations, voir [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).
    
2. Ouvrez le dossier Boîte d’envoi. Pour plus d’informations, voir [Ouverture d’un dossier de la boutique de messages](opening-a-message-store-folder.md).
    
3. Appelez la méthode **IMAPIFolder::CreateMessage** du dossier Boîte d’envoi pour créer le nouveau message. Pour plus d’informations, [voir IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Créez une liste de destinataires avec un ou plusieurs destinataires résolus. Pour plus d’informations, voir [Création d’une liste de destinataires](creating-a-recipient-list.md).
    
5. Vous pouvez éventuellement ajouter un objet. Pour plus d’informations, voir [Création d’un objet de message](creating-a-message-subject.md).
    
6. Ajoutez le texte du message. Pour plus d’informations, voir [Création de texte de message](creating-message-text.md).
    
7. Si le texte du message est formaté, ajoutez des informations de rendu. Pour plus d’informations, voir [Ajout d’informations de rendu au texte formaté](adding-rendering-information-to-formatted-text.md).
    
8. Vous pouvez éventuellement ajouter une ou plusieurs pièces jointes. Pour plus d’informations, voir [Création d’une pièce jointe de message](creating-a-message-attachment.md).
    
9. Définissez d’autres propriétés de message comme vous le souhaitez, puis enregistrez et envoyez le message en appelant **IMessage::SubmitMessage**. Pour plus d’informations, [voir IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Supprimez le message envoyé si la propriété **PR\_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) est définie sur TRUE ou déplacez-la vers le dossier identifié par la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Pour plus d’informations, [voir Traitement d’un message envoyé](processing-a-sent-message.md).
    
Si vous souhaitez enregistrer le message de manière intermittante avant de l’envoyer, appelez la méthode [IMAPIProp::SaveChanges du](imapiprop-savechanges.md) message. Pour plus d’informations, voir [Enregistrement d’un message](saving-a-message.md) ou [Envoi d’un message](sending-a-message.md). 
  
## <a name="in-this-section"></a>Dans cette section

- [Création d’une liste de](creating-a-recipient-list.md) destinataires : décrit comment créer une liste de destinataires.
    
- [Création d’un objet de](creating-a-message-subject.md) message : décrit comment créer un objet facultatif pour un message.
    
- [Création de texte de](creating-message-text.md) message : décrit comment créer du texte de message.
    
- [Ajout d’informations de rendu au texte formaté](adding-rendering-information-to-formatted-text.md) : décrit l’endroit où une pièce jointe doit être rendue dans le texte formaté.
    
- [Création d’une pièce jointe de](creating-a-message-attachment.md) message : décrit comment créer des pièces jointes.
    
- [Enregistrement d’un message](saving-a-message.md) : décrit comment les clients enregistrent les messages.
    
- [Envoi d’un message](sending-a-message.md) : décrit comment envoyer un message.
    
- [Traitement d’un message envoyé](processing-a-sent-message.md) : décrit comment traiter les messages envoyés.
    

