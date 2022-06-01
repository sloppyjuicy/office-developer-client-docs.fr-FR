---
title: PidLidLogDuration, propriété canonique
description: Décrit la propriété canonique PidLidLogDuration, qui représente la durée, en minutes, d’un message de journal.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
ms.openlocfilehash: 8e9f2e1bfda46b2ca34877c1aeb6b2397ae06019
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811773"
---
# <a name="pidlidlogduration-canonical-property"></a>PidLidLogDuration, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la durée, en minutes, d’un message de journal.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidLogDuration  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Log  <br/> |
|ID long (LID) :  <br/> |0x00008707  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Remarques

Durée, en minutes, de l’activité qui doit être la différence entre les propriétés **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) et **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les journaux.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

