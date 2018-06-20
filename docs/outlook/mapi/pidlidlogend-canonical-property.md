---
title: Propriété canonique PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ef1c9814aa6d1f81a44883d09ac635a5eed76517
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785281"
---
# <a name="pidlidlogend-canonical-property"></a>Propriété canonique PidLidLogEnd

  
  
**S’applique à**: Outlook 
  
Représente la date de fin et l’heure pour le message de journal.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidLogEnd  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Log  <br/> |
|ID de type long (capot) :  <br/> |0x00008708  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Zone :  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Remarques

L’heure de l’activité de fin en temps universel coordonné le (UTC), qui doit être égale à la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) et supérieure ou égale à la propriété **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
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

