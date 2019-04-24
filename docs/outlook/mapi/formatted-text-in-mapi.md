---
title: Texte mis en forme dans MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327467"
---
# <a name="formatted-text-in-mapi"></a>Texte mis en forme dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le texte d'un message peut être stocké et transmis à l'aide de texte brut ou de texte mis en forme. Le texte mis en forme améliore le texte du message en modifiant son apparence, par exemple, une ou plusieurs polices, tailles de police ou couleurs de texte. Il est recommandé que tous les clients et, dans la mesure du possible, tous les fournisseurs de banques de messages prennent en charge le texte mis en forme. La prise en charge du texte mis en forme dans les messages ajoute de la valeur en améliorant la lisibilité et en facilitant l'efficacité de la gestion des messages.
  
Le texte mis en forme peut être implémenté de différentes manières. La façon la plus courante est d'utiliser le format RTF (Rich Text Format). MAPI définit trois propriétés transmissibles pour la conservation des informations de texte du message: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour le texte brut, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour html et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) pour le texte RTF qui a été compressé. Étant donné que la version mise en forme d'un texte de message peut être deux fois plus grande que la version sans mise en forme, le texte RTF est compressé avant d'être transféré avec le message et stocké dans la propriété **PR_RTF_COMPRESSED** . Lorsque le message est affiché à l'écran, il n'est pas compressé à l'aide d'une fonction utilitaire fournie par MAPI. 
  
MAPI définit ces deux propriétés et mécanismes de texte de message pour la conversion entre ceux-ci afin que les clients compatibles RTF puissent interagir avec les clients et les systèmes de messagerie qui ne prennent pas en charge le texte mis en forme.
  
### 

[Synchronisation du texte et de la mise en forme](synchronizing-text-and-formatting.md)
  
> Indique comment conserver le texte du message RTF synchronisé avec la mise en forme.
    
[Prise en charge du texte mis en forme dans les messages sortants: responsabilités du client](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Décrit les responsabilités des applications clientes pour la prise en charge du texte mis en forme dans les messages sortants.
    
[Prise en charge du texte mis en forme dans les messages entrants: responsabilités du client](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Décrit les responsabilités des applications clientes pour la prise en charge du texte mis en forme dans les messages entrants.
    
[Prise en charge du texte mis en forme: responsabilités de la Banque de messages](supporting-formatted-text-message-store-responsibilities.md)
  
> Décrit les responsabilités du magasin de messages pour la prise en charge du texte mis en forme.
    
[Prise en charge du texte mis en forme: rendu des pièces jointes](supporting-formatted-text-rendering-attachments.md)
  
> Indique comment choisir où les pièces jointes sont affichées.
    
[Prise en charge du texte mis en forme: responsabilités de passerelle](supporting-formatted-text-gateway-responsibilities.md)
  
> Décrit les responsabilités de passerelle pour les messages texte au format sortant et entrant.
    

