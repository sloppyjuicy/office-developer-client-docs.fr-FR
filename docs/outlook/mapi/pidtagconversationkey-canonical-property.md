---
title: Propriété canonique PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389763"
---
# <a name="pidtagconversationkey-canonical-property"></a>Propriété canonique PidTagConversationKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la clé de conversation utilisée dans Microsoft Outlook uniquement lors de la recherche **IPM. MessageManager** messages, tels que le message qui contient l’historique de téléchargement d’un compte Post Office Protocol (POP3). Cette propriété a été déconseillée dans Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSATION_KEY  <br/> |
|Identificateur :  <br/> |0x000B  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous accédez à des messages électroniques en tant que conversations et la conversion des propriétés de message pour le [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), n’utilisez pas cette propriété ; au lieu de cela, utilisez les propriétés canoniques [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Sous-arborescence IPM](ipm-subtree.md)
  
[Dossiers sp�ciaux MAPI](mapi-special-folders.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

