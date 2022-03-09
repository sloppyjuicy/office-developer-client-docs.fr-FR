---
title: Texte mis en forme dans MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
ms.openlocfilehash: 7c169aee00958fd2cd03401067638cbfe0b5a90a
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403934"
---
# <a name="formatted-text-in-mapi"></a>Texte mis en forme dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016
  
Le texte d’un message peut être stocké et transmis à l’aide de texte simple ou de texte formaté. Le texte formaté améliore le texte du message en modifiant son apparence avec, par exemple, une ou plusieurs polices, tailles de police ou couleurs de texte. Il est recommandé que tous les clients et, dans la mesure du possible, tous les fournisseurs de magasins de messages, supportent le texte formaté. La prise en charge du texte formaté dans les messages apporte de la valeur ajoutée en améliorant la lisibilité des messages et en rendant la gestion des messages plus simple et plus efficace.
  
Le texte mis en forme peut être implémenté de différentes manières. Le moyen le plus courant est le format RTF (Rich Text Format). MAPI définit trois propriétés transmises pour la tenue des informations de texte de message : **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour le texte brut, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour html et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) pour le texte RTF qui a été compressé. Étant donné que la version mise en forme d’un texte de message peut être deux fois plus grande que la version sans mise en forme, le texte RTF est compressé avant d’être transféré avec le message et stocké dans la propriété **PR_RTF_COMPRESSED** . Lorsqu’il est temps d’afficher le message à l’écran, il est décompressé à l’aide d’une fonction utilitaire fournie par MAPI.
  
MAPI définit ces deux propriétés et mécanismes de conversion de texte de message entre eux afin que les clients sensibles au format RTF peuvent interopérer avec les clients et les systèmes de messagerie qui ne peuvent pas prendre en charge le texte mis en forme.
  
[Synchronisation du texte et de la mise en forme](synchronizing-text-and-formatting.md)
  
> Indique comment maintenir la synchronisation du texte du message RTF avec la mise en forme.

[Prise en charge du texte formaté dans les messages sortants : responsabilités du client](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Décrit les responsabilités de l’application cliente pour la prise en charge du texte formaté dans les messages sortants.

[Prise en charge du texte formaté dans les messages entrants : responsabilités du client](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Décrit les responsabilités de l’application cliente pour la prise en charge du texte formaté dans les messages entrants.

[Prise en charge du texte formaté : responsabilités de la boutique de messages](supporting-formatted-text-message-store-responsibilities.md)
  
> Décrit les responsabilités de la boutique de messages pour la prise en charge du texte formaté.

[Prise en charge du texte formaté : rendu des pièces jointes](supporting-formatted-text-rendering-attachments.md)
  
> Indique comment choisir l’endroit où les pièces jointes sont rendues.

[Prise en charge du texte formaté : responsabilités de la passerelle](supporting-formatted-text-gateway-responsibilities.md)
  
> Décrit les responsabilités de la passerelle pour les messages texte formatés sortants et entrants.
