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
ms.openlocfilehash: a00505b765abdcb7b8fe9d68052774b30bbdf692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786726"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Propriété canonique PidTagScheduleInfoFreeBusyTentative

  
  
**S’applique à**: Outlook 
  
Contient les blocs de temps pour lequel l’état de disponibilité est provisoire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Identificateur :  <br/> |0x6852  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Zone :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété a les valeurs autant que le nombre de valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Chaque valeur binaire représente un mois et correspond à la valeur dans le même index dans **PR_SCHDINFO_MONTHS_TENTATIVE**. Les valeurs binaires sont triés dans le même ordre que les valeurs de **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Chaque valeur binaire a un ou plusieurs blocs de 4 octets et chacune d'entre elles contient l’heure de début dans les deux premiers octets et l’heure de fin dans les deux octets au format little-endian. L’heure de début est le nombre de minutes entre minuit temps universel coordonné (UTC) du premier jour du mois et l’heure de début de l’événement au format UTC. L’heure de fin est le nombre de minutes entre minuit UTC du premier jour du mois et l’heure de fin de l’événement au format UTC. Les blocs de 4 octets sont triés par ordre croissant.
  
Blocs consécutifs ou qui se chevauchent de temps sont fusionnés dans un bloc avec l’heure de début comme heure de début du premier bloc et heure de fin comme heure de fin du dernier bloc. Si un événement s’étend sur plusieurs mois ou années, l’événement est divisée en plusieurs blocs, une pour chaque mois. S’il n’y a aucun événement provisoire dans la plage de publication, cette propriété et la **PR_SCHDINFO_MONTHS_TENTATIVE** ne doivent pas être définie, ou doivent être supprimés s’ils existent déjà. Dans le cas contraire, cette propriété doit être définie. 
  
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

