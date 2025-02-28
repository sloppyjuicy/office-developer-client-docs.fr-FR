---
title: Propriété canonique PidLidCleanGlobalObjectId
description: Décrit la propriété canonique PidLidCleanGlobalObjectId, qui spécifie l’ObjectID global propre.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
ms.openlocfilehash: e0ad0812f4b92944af6db57a0368c3eed0170d72
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852928"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Propriété canonique PidLidCleanGlobalObjectId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie **l’ObjectID** global propre.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCleanGlobalObjId  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID long (LID) :  <br/> |0x00000023  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Le format de cette propriété est le même que celui de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). La valeur de cette propriété doit être égale à la valeur de **LID_GLOBAL_OBJID**, sauf que les champs YH, YL, M et D doivent être zéro. Tous les objets qui font référence à une instance d’une série périodique (y compris une instance orpheline), ainsi que la série périodique elle-même, ont la même valeur pour cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

