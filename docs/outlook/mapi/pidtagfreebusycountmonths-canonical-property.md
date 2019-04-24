---
title: Propriété canonique PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316190"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a>Propriété canonique PidTagFreeBusyCountMonths

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur pour le calcul des dates de début et de fin de la plage de données de disponibilité à publier dans les dossiers publics.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FREEBUSY_COUNT_MONTHS  <br/> |
|Identificateur :  <br/> |0x6869  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Transmission définie par la classe de message  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être supérieure ou égale à 0 et inférieure ou égale à 36. Cette propriété n'est pas obligatoire.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d'un utilisateur ou d'une ressource.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

