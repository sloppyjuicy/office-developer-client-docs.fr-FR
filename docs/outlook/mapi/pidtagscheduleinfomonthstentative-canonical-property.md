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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b58413809a562b6a2b1310e573e531ae7320c0e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599430"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsTentative

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les mois marqués comme provisoires dans le message de libre/occupé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6851  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Le nombre de valeurs de cette propriété doit être entre zéro et le nombre de mois couverts par la plage de publication, qui est la période entre les propriétés **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) et **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Chaque valeur de cette propriété est codée sur un mois et une année. Cette valeur est calculée à l’aide de l’expression « year × 16 + month », où l’année et le mois sont basés sur le calendrier grégorien. Les valeurs sont triées dans l’ordre croissant et sont codées au format little endian. Si un événement est réparti sur plusieurs mois ou plusieurs années, il doit y avoir une valeur pour chacun des mois qui se trouve dans la plage de publication. S’il n’existe aucun événement provisoire dans la plage de publication, cette propriété et **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) ne doivent pas être définies ou supprimées s’ils existent déjà. Sinon, cette propriété doit être définie.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
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

