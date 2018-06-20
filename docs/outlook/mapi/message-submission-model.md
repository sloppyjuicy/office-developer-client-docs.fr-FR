---
title: Modèle d’envoi de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784900"
---
# <a name="message-submission-model"></a>Modèle d’envoi de message

  
  
**S’applique à**: Outlook 
  
Envoi du message est effectuée par une série d’appels du spouleur MAPI vers le fournisseur de transport. Les appels sont classés comme suit :
  
1. Le spouleur MAPI appelle [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), en passant un [IMessage : IMAPIProp](imessageimapiprop.md) instance, pour lancer le processus. 
    
2. Le fournisseur de transport place ensuite une valeur de référence : un transport définies par l’identificateur utilisé dans les futures références à ce message, à l’emplacement référencé dans **SubmitMessage**.
    
3. Le fournisseur de transport accède aux données message à l’aide de l’instance **IMessage** passée. Pour chaque destinataire dans passé **IMessage** pour laquelle il accepte la responsabilité, le fournisseur de transport définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) et renvoie.
    
4. Le fournisseur de transport peut utiliser la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour indiquer si elle reconnaît tous les destinataires qui ne peuvent pas être remis à, ou pour créer un rapport de remise standard. **StatusRecips** est pratique pour les fournisseurs de transport que vous avez déterminé que certains destinataires ne peuvent pas être remis à ou qui ont reçu les informations de remise à partir de leur système de messagerie sous-jacent qui peut l’utilisateur ou l’application cliente utiles. 
    
5. Appel de spouleur MAPI [IXPLogon::EndMessage](ixplogon-endmessage.md) est la main finale responsabilité désactivé pour le message du spouleur MAPI pour le fournisseur de transport. 
    
6. Le spouleur MAPI permet [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour annuler pendant les appels **SubmitMessage** ou **EndMessage** de traitement du message. 
    

