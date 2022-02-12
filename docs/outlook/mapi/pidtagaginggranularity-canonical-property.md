---
title: Propriété canonique PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c233aa48643368194ba3dcdd9adf780cdb89b950
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779727"
---
# <a name="pidtagaginggranularity-canonical-property"></a>Propriété canonique PidTagAgingGranularity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente l’unité de temps utilisée pour déterminer la durée pendant qu’un élément reste dans un dossier avant l’archivage de l’élément.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AGING_GRANULARITY  <br/> |
|Identificateur :  <br/> |0x36EE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs possibles **pour PR_AGING_GRANULARITY** peuvent être l’une des valeurs suivantes. 
  
|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |0  <br/> |**PR_AGING_PERIOD** est défini en nombre de mois. |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD** est défini en nombre de semaines. |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD** est défini en nombre de jours. |
   
La durée pendante pendant qui reste un élément dans un dossier avant d’être archivé est déterminée par deux propriétés, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) et **PR_AGING_GRANULARITY**. **PR_AGING_PERIOD** représente le nombre d’unités de temps pendant que l’élément reste dans le dossier avant d’être archivé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de données de base utilisées dans les opérations distantes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
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

