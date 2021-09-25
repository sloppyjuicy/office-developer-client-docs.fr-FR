---
title: Gestion d’un message sortant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 18fe188f7906b3a2fdd8192a353cc8ba39ad0247
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556692"
---
# <a name="handling-an-outgoing-message"></a>Gestion d’un message sortant

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un message sortant est un message qui peut être envoyé à un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie ou être publié dans un dossier dans une magasin de messages.
  
## <a name="create-and-send-an-outgoing-message"></a>Créer et envoyer un message sortant
  
1. Ouvrez la boutique de messages par défaut. Pour plus d’informations, voir [Ouverture d’une magasin de messages](opening-a-message-store.md) et ouverture de la boutique de messages par [défaut.](opening-the-default-message-store.md)
    
2. Ouvrez le dossier Boîte d’envoi. Pour plus d’informations, voir [Ouverture d’un dossier de la boutique de messages.](opening-a-message-store-folder.md)
    
3. Appelez la méthode **IMAPIFolder::CreateMessage** du dossier Outbox pour créer le nouveau message. Pour plus d’informations, [voir IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Créez une liste de destinataires avec un ou plusieurs destinataires résolus. Pour plus d’informations, voir [Création d’une liste de destinataires.](creating-a-recipient-list.md)
    
5. Vous pouvez éventuellement ajouter un objet. Pour plus d’informations, voir [Création d’un objet de message.](creating-a-message-subject.md)
    
6. Ajoutez le texte du message. Pour plus d’informations, voir [Création de texte de message.](creating-message-text.md)
    
7. Si le texte du message est formaté, ajoutez des informations de rendu. Pour plus d’informations, voir [Ajout d’informations de rendu au texte formaté.](adding-rendering-information-to-formatted-text.md)
    
8. Vous pouvez éventuellement ajouter une ou plusieurs pièces jointes. Pour plus d’informations, voir [Création d’une pièce jointe de message.](creating-a-message-attachment.md)
    
9. Définissez d’autres propriétés de message comme vous le souhaitez, puis enregistrez et envoyez le message en appelant **IMessage::SubmitMessage**. Pour plus d’informations, [voir IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Supprimez le message envoyé si la propriété **\_ PR DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) est définie sur TRUE ou déplacez-la vers le dossier identifié par la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Pour plus d’informations, [voir Traitement d’un message envoyé.](processing-a-sent-message.md)
    
Si vous souhaitez enregistrer le message de manière intermittante avant de l’envoyer, appelez la méthode [IMAPIProp::SaveChanges du](imapiprop-savechanges.md) message. Pour plus d’informations, voir [l’enregistrement d’un message](saving-a-message.md) [ou l’envoi d’un message.](sending-a-message.md) 
  
## <a name="in-this-section"></a>Dans cette section

- [Création d’une liste de](creating-a-recipient-list.md)destinataires : décrit comment créer une liste de destinataires.
    
- [Création d’un objet de message](creating-a-message-subject.md): décrit comment créer un objet facultatif pour un message.
    
- [Création d’un](creating-message-text.md)texte de message : décrit comment créer du texte de message.
    
- [Ajout d’informations de rendu au texte formaté](adding-rendering-information-to-formatted-text.md): décrit l’endroit où une pièce jointe doit être rendue dans le texte formaté.
    
- [Création d’une pièce jointe de](creating-a-message-attachment.md)message : décrit comment créer des pièces jointes.
    
- [Enregistrement d’un message](saving-a-message.md): décrit comment les clients enregistrent les messages.
    
- [Envoi d’un message](sending-a-message.md): décrit comment envoyer un message.
    
- [Traitement d’un message envoyé](processing-a-sent-message.md): décrit comment traiter les messages envoyés.
    

