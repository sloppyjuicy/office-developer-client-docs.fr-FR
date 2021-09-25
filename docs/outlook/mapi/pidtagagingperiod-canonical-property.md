---
title: Propriété canonique PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9628cbde8bf136f4be4536e26ee9c2624cdea05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595328"
---
# <a name="pidtagagingperiod-canonical-property"></a>Propriété canonique PidTagAgingPeriod

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente le nombre d’unités de temps utilisées pour déterminer la durée pendant combien de temps un élément reste dans un dossier avant l’archivage de l’élément.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AGING_PERIOD  <br/> |
|Identificateur :  <br/> |0x36EC  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

La durée pendant qu’un élément reste dans un dossier avant d’être archivé est déterminée par deux propriétés, **PR_AGING_PERIOD** et **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** représente l’unité de temps dans laquelle **PR_AGING_PERIOD** est exprimée, lors de la détermination de cette durée. 
  
Les valeurs possibles **pour PR_AGING_GRANULARITY** peuvent être l’une des valeurs suivantes. 
  
****

|**Name**|**Description**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** est défini en nombre de mois.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** est défini en nombre de semaines.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** est défini en nombre de jours.  <br/> |
   
Par exemple, si un dossier archive un élément uniquement après avoir été dans le  dossier pendant deux semaines, **PR_AGING_GRANULARITY** est AG_WEEKS et **PR_AGING_PERIOD** est 2. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
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

