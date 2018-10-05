---
title: Propriété canonique PidTagScheduleInfoFreeBusyBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395713"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a>Propriété canonique PidTagScheduleInfoFreeBusyBusy

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les blocs de temps dont le statut est occupé (e).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_FREEBUSY_BUSY  <br/> |
|Identificateur :  <br/> |0x6854  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Format, calcul les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) mais faire référence à des rendez-vous sont marquées comme occupé (e) sur l’objet calendar associé.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou une ressource.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

