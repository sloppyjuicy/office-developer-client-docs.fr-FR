---
title: Propriété canonique PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786731"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsMerged

  
  
**S’applique à**: Outlook 
  
Contient une liste des mois pour les données et de disponibilité de type occupé (e) ou une absence du bureau (OOF) message est présente dans le message et de disponibilité. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Identificateur :  <br/> |0x684F  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Zone :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Événements de type disponible/occupé provisoire ne sont pas inclus dans cette propriété. La syntaxe/format et les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) mais faire référence à un rendez-vous qui sont marqués absent du bureau ou occupé (e) sur l’objet calendar associé. 
  
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

