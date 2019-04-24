---
title: Propriété canonique PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359758"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsTentative

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les mois marqués «provisoire» dans le message de disponibilité.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6851  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Le nombre de valeurs de cette propriété doit être compris entre zéro et le nombre de mois couverts par la plage de publication, qui correspond à la période entre le **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) et **PR_FREEBUSY_PUBLISH_END **Propriétés ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Chaque valeur de cette propriété possède un mois et une année codés. Ce calcul est calculé à l'aide de l'expression «Year × 16 + month» où l'année et le mois sont basés sur le calendrier grégorien. Les valeurs sont triées par ordre croissant et sont codées au format Little endian. Si un événement est réparti sur plusieurs mois ou plusieurs années, il doit y avoir une valeur pour chacun des mois appartenant à la plage de publication. S'il n'existe aucun événement provisoire dans la plage de publication, cette propriété et **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) ne doit pas être définie ou doit être supprimée si elle existe déjà. Dans le cas contraire, cette propriété doit être définie.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d'un utilisateur ou d'une ressource.
    
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

