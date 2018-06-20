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
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786723"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsTentative

  
  
**S’applique à**: Outlook 
  
Contient les mois marqués provisoires dans le message et de disponibilité.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6851  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Zone :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Le nombre de valeurs dans cette propriété doit être comprise entre 0 et le nombre de mois couverts par la plage de publication, qui est la période entre la **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) et **PR_FREEBUSY_PUBLISH_END **Propriétés ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Chaque valeur de cette propriété, a un mois et l’année codé de celui-ci. Il est calculé à l’aide de l’expression « an x 16 + mois » où les mois et année sont basées sur le calendrier grégorien. Les valeurs sont triées par ordre croissant et sont encodés au format little-endian. Si un événement s’étend sur plusieurs mois ou plusieurs années, il doit être une valeur pour chacun des mois qui figurent dans la plage de publication. S’il n’y a aucun événement provisoire dans la plage de publication, cette propriété et la **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) ne doivent pas être définie, ou doivent être supprimés s’ils existent déjà. Dans le cas contraire, cette propriété doit être définie.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou une ressource.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

