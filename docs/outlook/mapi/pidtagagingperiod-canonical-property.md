---
title: PidTagAgingPeriod, propriété canonique
description: Décrit la propriété canonique PidTagAgingPeriod, qui représente un certain nombre d’unités de temps déterminant la durée avant l’archivage d’un élément.
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
ms.openlocfilehash: bd2f77b1237287deaabf914c37525508333adf06
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815995"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagAgingPeriod, propriété canonique

**S’applique à** : Outlook 2013 | Outlook 2016
  
Représente le nombre d’unités de temps utilisées pour déterminer la durée pendant laquelle un élément reste dans un dossier avant que l’élément ne soit archivé.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AGING_PERIOD  <br/> |
|Identificateur :  <br/> |0x36EC  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |

## <a name="remarks"></a>Remarques

La durée pendant laquelle un élément reste dans un dossier avant d’être archivé est déterminée par deux propriétés, **PR_AGING_PERIOD** et **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** représente l’unité de temps dans laquelle **PR_AGING_PERIOD** est exprimée, lors de la détermination de cette durée.
  
Les valeurs possibles pour **PR_AGING_GRANULARITY** peuvent être l’une des suivantes.
  
|**Name**|**Description**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** est défini en nombre de mois. |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** est défini en nombre de semaines. |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** est défini en nombre de jours. |

Par exemple, si un dossier archive un élément uniquement après que l’élément a été dans le dossier pendant deux semaines, **PR_AGING_GRANULARITY** est **AG_WEEKS** et **PR_AGING_PERIOD** est 2.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.

[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de données de base utilisées dans les opérations à distance.

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de courrier électronique.

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.

Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.

## <a name="see-also"></a>Voir aussi

[Propriétés MAPI](mapi-properties.md)  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
