---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier, y compris toutes les règles de MAJ historiques, actuelles et futures fuseau horaire pour l’heure d’été.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782850"
---
# <a name="tzdefinition"></a>TZDEFINITION

Représente un fuseau horaire entier, y compris toutes les règles de MAJ historiques, actuelles et futures fuseau horaire pour l’heure d’été.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Membres

_wFlags_
  
> Indique que le nom de la clé qui représente le fuseau horaire dans le Registre Windows est valid. Étant donné que chaque fuseau horaire doit toujours être identifiée par un nom de clé, ce membre doit avoir toujours la valeur **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> Le nom de la clé de ce fuseau horaire dans le Registre Windows. Ce nom ne doit pas être localisé. Il possède une taille maximale de **MAX_PATH**, qui est définie dans le windows.h de fichier d’en-tête Kit de développement logiciel (SDK) Windows. 
    
_cRules_
  
> Le nombre de règles de fuseau horaire pour cette définition. Le nombre maximal de règles est **TZ_MAX_RULES**. 
    
_rgRules_
  
> Tableau des règles qui décrivent le cas d’équipes.
    
## <a name="remarks"></a>Remarques

Il doit exister au moins une règle dans *rgRules* . La première règle de *rgRules* est considéré comme la règle à utiliser jusqu'à ce que la deuxième règle commence, quel que soit le *stStart* sur la première règle. 
  
Les règles de tri de la plus ancienne à la plus récente. Ne se chevauchent pas autorisée entre les règles, pour une règle précédente est considéré comme fin au démarrage d’une nouvelle règle.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

