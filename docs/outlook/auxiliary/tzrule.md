---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Spécifie les informations d’une règle de fuseau horaire concernant le début de l’heure d’été et l’année pendant laquelle cette règle de fuseau horaire prend effet pour la première fois.
ms.openlocfilehash: cd77840da1ff391ec3027787e902893fe701382b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631110"
---
# <a name="tzrule"></a>TZRULE

Spécifie les informations d’une règle de fuseau horaire concernant le début de l’heure d’été et l’année pendant laquelle cette règle de fuseau horaire prend effet pour la première fois. 
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Membres

_wFlags_
  
> Les indicateurs de ce membre identifient des détails spécifiques pour cette règle de fuseau horaire. Les indicateurs possibles sont les suivants :
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** : identifie la règle comme celle qui doit être utilisée actuellement. Une seule règle peut être marquée comme règle effective. Toutes les autres règles sont uniquement à des fins de comparaison. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** — Lors de réunions périodiques, identifie la règle comme correspondant à la règle dans [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Cela peut être utilisé pour détecter si **PidLidTimeZoneStruct** a été modifié de manière significative par un client hérité, qui ne serait autrement pas conscient de la nouvelle propriété plus complète. 
    
_stStart_
  
> Heure UTC (Temps universel coordonné) à l’heure de début de la règle de fuseau horaire.
    
_TZReg_
  
> Informations de fuseau horaire pour la règle de fuseau horaire.
    
## <a name="remarks"></a>Remarques

Cette structure augmente [le TZREG](tzreg.md) en fournissant des informations supplémentaires indiquant à quel moment les règles de fuseau horaire prennent effet. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

