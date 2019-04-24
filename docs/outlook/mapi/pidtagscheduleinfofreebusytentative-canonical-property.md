---
title: Propriété canonique PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359773"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoFreeBusyTentative

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les blocs de temps pendant lesquels l'état de disponibilité est provisoire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6852  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a autant de valeurs que le nombre de valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Chaque valeur binaire représente un mois et correspond à la valeur dans le même index dans **PR_SCHDINFO_MONTHS_TENTATIVE**. Les valeurs binaires sont triées dans le même ordre que les valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Chaque valeur binaire comporte un ou plusieurs blocs de 4 octets et chacune d'entre elles contient l'heure de début dans les deux premiers octets et l'heure de fin dans les deux octets au format Little-endian. L'heure de début est le nombre de minutes entre minuit UTC (temps universel coordonné) du premier jour du mois et l'heure de début de l'événement au format UTC. L'heure de fin est le nombre de minutes entre minuit UTC (temps universel) du premier jour du mois et l'heure de fin de l'événement au format UTC. Les blocs de 4 octets sont triés par ordre croissant.
  
Les blocs de temps consécutifs ou superposés sont fusionnés en un bloc avec l'heure de début comme heure de début du premier bloc et l'heure de fin comme heure de fin du dernier bloc. Si un événement est réparti sur plusieurs mois ou années, l'événement est fractionné en plusieurs blocs, un par mois. S'il n'y a pas d'événements provisoires dans la plage de publication, cette propriété et **PR_SCHDINFO_MONTHS_TENTATIVE** ne doit pas être définie ou doit être supprimée si elle existe déjà. Dans le cas contraire, cette propriété doit être définie. 
  
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

