---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Définit le démarrage de l’heure, quand le retour à l’heure standard se produit et le nombre d’heures du passage de MAJ est.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782840"
---
# <a name="tzreg"></a>TZREG

Définit le démarrage de l’heure, quand le retour à l’heure standard se produit et le nombre d’heures du passage de MAJ est.
  
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
  
> Décalage de l’heure de Greenwich (GMT).
    
_lStandardBias_
  
> Décalage de décalage au cours de l’heure standard.
    
_lDaylightBias_
  
> Décalage de décalage de l’heure d’été.
    
_stStandardDate_
  
> Le temps de passer à l’heure standard.
    
_stDaylightDate_
  
> Le temps de passer à l’heure d’été.
    
## <a name="remarks"></a>Remarques

Cette structure est similaire à **TIME_ZONE_INFORMATION**. Il s’agit de la structure permet de stocker les informations de fuseau horaire pour les réunions périodiques par les clients hérités.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

