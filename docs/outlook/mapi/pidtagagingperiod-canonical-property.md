---
title: Propriété canonique PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: caaa01982ff9e66fe7e17df4eaf37dcd25281d4e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569553"
---
# <a name="pidtagagingperiod-canonical-property"></a>Propriété canonique PidTagAgingPeriod

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Représente le nombre d’unités de temps qui sont utilisés pour déterminer la durée pendant laquelle un élément est conservée dans un dossier avant de l’élément est archivé.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AGING_PERIOD  <br/> |
|Identificateur :  <br/> |0x36EC  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

La durée pendant laquelle un élément est conservée dans un dossier avant de l’élément est archivé est déterminée par les deux propriétés, **PR_AGING_PERIOD** et **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** représente l’unité de temps dans laquelle **PR_AGING_PERIOD** est exprimé, lors de la détermination de cette durée. 
  
Les valeurs possibles de **PR_AGING_GRANULARITY** peuvent être une des options suivantes. 
  
****

|**Nom**|**Description**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** est défini dans le nombre de mois.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** est défini dans le nombre de semaines.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** est défini dans le nombre de jours.  <br/> |
   
Par exemple, si un archives de dossier est un élément uniquement une fois que l’élément a été dans le dossier pour les deux semaines, puis **PR_AGING_GRANULARITY** **AG_WEEKS** et **PR_AGING_PERIOD** est 2. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de base de données qui sont utilisés dans les opérations à distance.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
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

