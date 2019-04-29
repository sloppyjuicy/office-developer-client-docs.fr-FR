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
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407626"
---
# <a name="handling-an-outgoing-message"></a>Gestion d’un message sortant

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un message sortant est un message qui peut être envoyé à un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie ou être publié dans un dossier d'une banque de messages.
  
## <a name="create-and-send-an-outgoing-message"></a>Créer et envoyer un message sortant
  
1. Ouvrez la Banque de messages par défaut. Pour plus d'informations, consultez la rubrique [ouverture d'une banque de messages](opening-a-message-store.md) et [ouverture de la Banque de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier boîte d'envoi. Pour plus d'informations, consultez [la rubrique ouverture d'un dossier de banque de messages](opening-a-message-store-folder.md).
    
3. Appelez la méthode **IMAPIFolder:: CreateMessage** du dossier boîte d'envoi pour créer le nouveau message. Pour plus d'informations, voir [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),
    
4. Créer une liste de destinataires avec un ou plusieurs destinataires résolus. Pour plus d'informations, consultez [la rubrique Création d'une liste de destinataires](creating-a-recipient-list.md).
    
5. Si vous le souhaitez, ajoutez un objet. Pour plus d'informations, consultez [la rubrique Création d'un objet de message](creating-a-message-subject.md).
    
6. Ajoutez le texte du message. Pour plus d'informations, consultez la rubrique [création de texte de message](creating-message-text.md).
    
7. Si le texte du message est mis en forme, ajoutez des informations de rendu. Pour plus d'informations, consultez la rubrique [Ajout d'informations de rendu au texte mis en forme](adding-rendering-information-to-formatted-text.md).
    
8. Si vous le souhaitez, ajoutez une ou plusieurs pièces jointes. Pour plus d'informations, consultez [la rubrique Création d'une pièce jointe](creating-a-message-attachment.md).
    
9. Définissez d'autres propriétés de message si vous le souhaitez, puis enregistrez et envoyez le message en appelant **IMessage:: SubmitMessage**. Pour plus d'informations, consultez [IMessage:: SubmitMessage](imessage-submitmessage.md).
    
10. Supprimez le message envoyé si **la\_propriété PR DELETE_AFTER_SUBMIT** ([PIDTAGDELETEAFTERSUBMIT](pidtagdeleteaftersubmit-canonical-property.md)) est définie sur true ou déplacez-la dans le dossier identifié par la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Pour plus d'informations, consultez [la rubrique traitement d'un message envoyé](processing-a-sent-message.md).
    
Si vous souhaitez intermittantly enregistrer le message avant de l'envoyer, appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message. Pour plus d'informations, reportez-vous à [la rubrique enregistrement d'un message](saving-a-message.md) ou [envoi d'un message](sending-a-message.md). 
  
## <a name="in-this-section"></a>Dans cette section

- [Création d'une liste](creating-a-recipient-list.md)de destinataires: décrit comment créer une liste de destinataires.
    
- [Création d'un objet de message](creating-a-message-subject.md): explique comment créer un objet facultatif pour un message.
    
- [Création](creating-message-text.md)d'un texte de message: explique comment créer un texte de message.
    
- [Ajout d'informations de rendu au texte mis en forme](adding-rendering-information-to-formatted-text.md): décrit l'emplacement du texte mis en forme d'une pièce jointe.
    
- [Création d'une pièce jointe de message](creating-a-message-attachment.md): explique comment créer des pièces jointes.
    
- [Enregistrement d'un message](saving-a-message.md): décrit la manière dont les clients enregistrent les messages.
    
- [Envoi d'un message](sending-a-message.md): décrit comment envoyer un message.
    
- [Traitement d'un message envoyé](processing-a-sent-message.md): décrit comment les messages envoyés peuvent être traités.
    

