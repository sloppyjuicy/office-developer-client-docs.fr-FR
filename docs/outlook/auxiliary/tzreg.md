---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Définit le début de l’heure d’été, le retour à l’heure standard et le nombre d’heures d’été de l’heure d’été.
ms.openlocfilehash: ff0cda4da16a141be73955af5dcd758d575fe434
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605243"
---
# <a name="tzreg"></a>TZREG

Définit le début de l’heure d’été, le retour à l’heure standard et le nombre d’heures d’été de l’heure d’été.
  
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
  
> Décalage par rapport à l’heure de Greenwich (GMT).
    
_lStandardBias_
  
> Décalage par rapport à l’décalage au moment de l’heure standard.
    
_lDaylightBias_
  
> Décalage par rapport à l’décalage lors de l’heure d’été.
    
_stStandardDate_
  
> Heure de passage à l’heure standard.
    
_stDaylightDate_
  
> Heure de passage à l’heure d’été.
    
## <a name="remarks"></a>Remarques

Cette structure est similaire à **TIME_ZONE_INFORMATION**. Il s’agit de la structure utilisée par les clients hérités pour stocker les informations de fuseau horaire pour les réunions périodiques.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

