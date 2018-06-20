---
title: Propriété canonique PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c21f2885f7e9475c2149e42e2a8d947311916b4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785271"
---
# <a name="pidlidisrecurring-canonical-property"></a>Propriété canonique PidLidIsRecurring

  
  
**S’applique à**: Outlook 
  
Spécifie si l’objet est associé à une série périodique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |LID_IS_RECURRING  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID de type long (capot) :  <br/> |0 x 00000005  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur TRUE indique que l’objet représente une série périodique, ou une exception (y compris une instance orpheline). La valeur FALSE, ou l’absence de cette propriété, indique que l’objet représente une instance unique. Notez la différence entre cette propriété et la propriété **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

