---
title: Propriété canonique PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ee2add6e8b33b5108697068cc7100bc0f946015d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587026"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoFreeBusyTentative

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les blocs de heures pour lesquels l’état de libre/occupé est provisoire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6852  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a autant de valeurs que le nombre de valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Chaque valeur binaire représente un mois et correspond à la valeur au même index dans **PR_SCHDINFO_MONTHS_TENTATIVE**. Les valeurs binaires sont triées dans le même ordre que les valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Chaque valeur binaire comporte un ou plusieurs blocs de 4 octets et chacun d’eux contient l’heure de début dans les deux premiers octets et l’heure de fin dans les deux deuxièmes octets au format little-endian. L’heure de début est le nombre de minutes entre l’heure UTC (Temps universel coordonné) de minuit du premier jour du mois et l’heure de début de l’événement en UTC. L’heure de fin est le nombre de minutes entre minuit UTC du premier jour du mois et l’heure de fin de l’événement en UTC. Les blocs 4-BYTE sont triés dans l’ordre croissant.
  
Les blocs de temps consécutifs ou qui se chevauchent sont fusionnés en un seul bloc avec l’heure de début comme heure de début du premier bloc et l’heure de fin comme heure de fin du dernier bloc. Si un événement est réparti sur plusieurs mois ou années, l’événement est divisé en plusieurs blocs, un par mois. S’il n’existe aucun événement provisoire dans  la plage de publication, cette propriété et cette PR_SCHDINFO_MONTHS_TENTATIVE ne doivent pas être définies ou supprimées s’ils existent déjà. Sinon, cette propriété doit être définie. 
  
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

