---
title: Propriété canonique PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: Contient les mois marqués comme provisoires dans le message gratuit Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 4e24ad1715caab08988f71f467721e8e6168fecc
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524196"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsTentative

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les mois marqués comme provisoires dans le message de libre/occupé.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6851  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Le nombre de valeurs de cette propriété doit être entre zéro et le nombre de mois couverts par la plage de publication, qui est la période entre les propriétés **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) et **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Chaque valeur de cette propriété est codée mois et année. Cette valeur est calculée à l’aide de l’expression « year × 16 + month », où l’année et le mois sont basés sur le calendrier grégorien. Les valeurs sont triées dans l’ordre croissant et sont codées au format little endian. Si un événement est réparti sur plusieurs mois ou plusieurs années, il doit y avoir une valeur pour chacun des mois qui se trouve dans la plage de publication. S’il n’existe aucun événement provisoire dans la plage de publication, cette propriété et **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) ne doivent pas être définies ou supprimées s’ils existent déjà. Sinon, cette propriété doit être définie.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou d’une ressource.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

