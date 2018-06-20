---
title: Propriété canonique PidTagOriginalDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c4fc8ef6dd67eb5187bbc0bac8c4f4f9bee13826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786313"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a>Propriété canonique PidTagOriginalDisplayCc

  
  
**S’applique à**: Outlook 
  
Contient les noms complets des destinataires en copie carbone (CC) du message d’origine.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W  <br/> |
|Identificateur :  <br/> |0x0073  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent une liste séparée par des points-virgules. Il est fourni par MAPI et est copié directement à partir de **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) lorsqu’une remise ou rapport de non-remise ou en lecture ou nonread rapport est généré. Cette propriété peut être présente sur les autres messages tel que défini par les classes de message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

