---
title: Propriété canonique PidTagScheduleInfoMonthsBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: Contient les mois pendant lesquels des données de type occupé(s) de type occupé(s) sont présentes dans le message de libre/occupé.
ms.openlocfilehash: 05c935a7c6fbbee09badcfeee5a6b26290047079
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524321"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsBusy

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les mois pendant lesquels des données de type occupé(s) de type occupé(s) sont présentes dans le message de libre/occupé.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_BUSY  <br/> |
|Identificateur :  <br/> |0x6853  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Le format, le calcul et les contraintes de cette propriété sont identiques à ceux de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mais font référence aux rendez-vous qui sont marqués comme occupés sur l’objet calendrier associé.
  
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

