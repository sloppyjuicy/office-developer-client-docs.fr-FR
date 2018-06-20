---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Spécifie les informations d’une règle de fuseau horaire au démarrage de l’heure et l’année dans laquelle cette règle de fuseau horaire prend tout d’abord l’effet.
ms.openlocfilehash: 77d56d238d959992bfadd2d8c143391ca6fa4d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782838"
---
# <a name="tzrule"></a>TZRULE

Spécifie les informations d’une règle de fuseau horaire au démarrage de l’heure et l’année dans laquelle cette règle de fuseau horaire prend tout d’abord l’effet. 
  
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
  
> Les indicateurs définis pour ce membre identifient des détails plus spécifiques pour cette règle de fuseau horaire. Les indicateurs possibles sont les suivantes :
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** — identifie la règle que celui qui doit être utilisé actuellement. Une seule règle peut être marquée comme la règle efficace. Toutes les autres règles sont uniquement à des fins de comparaison. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** — des réunions périodiques, identifie la règle de correspondance de la règle de [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Cela peut être utilisé pour détecter si **PidLidTimeZoneStruct** a été modifié considérablement par un client hérité, qui doit être ignore la nouvelle propriété plus complète. 
    
_stStart_
  
> L’heure en temps universel coordonné (UTC) qui a démarré la règle de fuseau horaire.
    
_TZReg_
  
> Les informations de fuseau horaire pour la règle de fuseau horaire.
    
## <a name="remarks"></a>Remarques

Cette structure augmente [TZREG](tzreg.md) en fournissant des informations supplémentaires indiquant le moment où les règles de fuseau horaire prennent effet. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

