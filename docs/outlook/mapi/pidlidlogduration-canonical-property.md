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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400340"
---
# <a name="pidlidlogduration-canonical-property"></a>Propriété canonique PidLidLogDuration

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la durée, en minutes, d’un message de journal.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidLogDuration  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Log  <br/> |
|ID de type long (capot) :  <br/> |0x00008707  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Remarques

La durée, en minutes, de l’activité doit correspondre à la différence entre les **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) et les propriétés de **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

