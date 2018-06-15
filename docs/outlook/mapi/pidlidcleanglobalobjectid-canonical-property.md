---
title: Propriété canonique PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a784c91a04cce572c8e30085b1760c28296a1d53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19785107"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Propriété canonique PidLidCleanGlobalObjectId

  
  
**S’applique à**: Outlook 
  
Spécifie nettoyage global **ObjectID**.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCleanGlobalObjId  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID de type long (capot) :  <br/> |0 x 00000023  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Note

Le format de cette propriété est la même que celle du **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). La valeur de cette propriété doit être égale à la valeur de **LID_GLOBAL_OBJID**, à l’exception de la YH, YL M, et les champs D doivent être égal à zéro. Tous les objets qui font référence à une Instance d’une série périodique (y compris une instance orpheline), ainsi que la série périodique lui-même, aura la même valeur pour cette propriété.
  
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

