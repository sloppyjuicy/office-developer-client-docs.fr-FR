---
title: Texte mis en forme dans MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bfaa4fd5f561c8138461db6ce8b9033c2a75b96b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580627"
---
# <a name="formatted-text-in-mapi"></a>Texte mis en forme dans MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le texte d’un message peut être stocké et transmises à l’aide de texte brut ou texte mis en forme. Texte mis en forme améliore le texte du message en modifiant son apparence avec, par exemple, une ou plusieurs polices, les tailles de police ou les couleurs de texte. Il est recommandé que tous les clients et la mesure du possible, tous les fournisseurs de banque de messages, prennent en charge le texte mis en forme. Prise en charge de texte mis en forme dans les messages enrichit en améliorer la lisibilité de message et en gestion des messages plus facile et plus efficace.
  
Texte mis en forme peut être implémenté de plusieurs façons. Le moyen le plus courant est avec le Format de texte enrichi (RTF). MAPI définit trois propriétés transmissible pour conserver les informations de texte de message : **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour le texte brut, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour le HTML et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) pour le texte RTF qui a été compressé. La version mise en forme d’un texte de message pouvant être deux fois aussi grande que la version sans la mise en forme, le texte RTF est compressé avant d’être transféré avec le message et stocké dans la propriété **PR_RTF_COMPRESSED** . Lorsqu’il est temps pour afficher le message sur l’écran, il est décompressé à l’aide d’une fonction utilitaire fournie par MAPI. 
  
MAPI définit ces deux propriétés de texte du message et pour la conversion entre les mécanismes de sorte que les clients prenant en charge les RTF peuvent interagir avec les clients et les systèmes de messagerie ne prenant pas en charge texte mis en forme.
  
### 

[Synchronisation du texte et de la mise en forme](synchronizing-text-and-formatting.md)
  
> Décrit comment maintenir la synchronisation avec la mise en forme du texte de message RTF.
    
[Prise en charge du texte mis en forme dans les messages sortants : responsabilités du client](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Décrit les responsabilités du client application pour prendre en charge le texte mis en forme dans les messages sortants.
    
[Prise en charge du texte mis en forme dans les messages entrants : responsabilités du client](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Décrit les responsabilités du client application pour prendre en charge le texte mis en forme dans les messages entrants.
    
[Prise en charge du texte mis en forme : responsabilités de la banque de messages](supporting-formatted-text-message-store-responsibilities.md)
  
> Décrit les responsabilités du magasin de message pour prendre en charge le texte mis en forme.
    
[Prise en charge du texte mis en forme : rendu des pièces jointes](supporting-formatted-text-rendering-attachments.md)
  
> Décrit comment choisir où les pièces jointes sont rendus.
    
[Prise en charge du texte mis en forme : responsabilités de passerelle](supporting-formatted-text-gateway-responsibilities.md)
  
> Décrit les responsabilités de passerelle pour les messages texte mis en forme entrants et sortants.
    

