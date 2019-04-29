---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Définit à quel moment l'heure d'été commence, lorsque le retour à l'heure standard se produit, et le nombre d'heures d'évolution de l'heure d'été.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419365"
---
# <a name="tzreg"></a>TZREG

Définit à quel moment l'heure d'été commence, lorsque le retour à l'heure standard se produit, et le nombre d'heures d'évolution de l'heure d'été.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a>Membres

_lBias_
  
> Décalage par rapport à l'heure de Greenwich (GMT).
    
_lStandardBias_
  
> Décalage par rapport au décalage pendant l'heure standard.
    
_lDaylightBias_
  
> Décalage par rapport à l'heure d'été.
    
_stStandardDate_
  
> Temps de basculement vers l'heure standard.
    
_stDaylightDate_
  
> Durée de passage à l'heure d'été.
    
## <a name="remarks"></a>Remarques

Cette structure est similaire à **TIME_ZONE_INFORMATION**. Il s'agit de la structure utilisée par les clients hérités pour stocker les informations de fuseau horaire pour les réunions périodiques.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

