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
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349216"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Propriété canonique PidLidCleanGlobalObjectId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l' **ObjectID**global propre.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCleanGlobalObjId  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Meeting  <br/> |
|ID long (couvercle):  <br/> |0x00000023  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Le format de cette propriété est le même que celui de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). La valeur de cette propriété doit être égale à la valeur de **LID_GLOBAL_OBJID**, sauf que les champs YH, yl, M et D doivent être nuls. Tous les objets qui font référence à une instance d'une série périodique (y compris une instance orpheline), ainsi que la série périodique elle-même, auront la même valeur pour cette propriété.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

