---
title: Propriété canonique PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cc2d52ec183cc336bf126b1fda9a85d41f704f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785283"
---
# <a name="pidlidlogduration-canonical-property"></a>Propriété canonique PidLidLogDuration

  
  
**S’applique à**: Outlook 
  
Représente la durée, en minutes, d’un message de journal.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidLogDuration  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Log  <br/> |
|ID de type long (capot) :  <br/> |0x00008707  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Remarques

La durée, en minutes, de l’activité doit correspondre à la différence entre les **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) et les propriétés de **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

