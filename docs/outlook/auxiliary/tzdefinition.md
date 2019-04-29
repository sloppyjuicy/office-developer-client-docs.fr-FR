---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier, y compris toutes les règles d'évolution des fuseaux horaires, actuelles et futures, pour l'heure d'été.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429340"
---
# <a name="tzdefinition"></a>TZDEFINITION

Représente un fuseau horaire entier, y compris toutes les règles d'évolution des fuseaux horaires, actuelles et futures, pour l'heure d'été.
  
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
  
> Indique que le nom de la clé qui représente le fuseau horaire dans le Registre Windows est valide. Étant donné que chaque fuseau horaire doit toujours être identifié par un nom de clé, ce membre doit toujours avoir la valeur **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> Nom de la clé pour ce fuseau horaire dans le Registre Windows. Ce nom ne doit pas être localisé. Il a une taille maximale de **MAX_PATH**, qui est définie dans le fichier d'en-tête Windows. h du kit de développement logiciel (SDK) Windows. 
    
_cRules_
  
> Nombre de règles de fuseau horaire pour cette définition. Le nombre maximal de règles est de **TZ_MAX_RULES**. 
    
_rgRules_
  
> Tableau de règles qui décrivent le moment où les équipes se produisent.
    
## <a name="remarks"></a>Remarques

Il doit y avoir au moins une règle dans *rgRules* . La première règle dans *rgRules* est considérée comme étant la règle à utiliser jusqu'à ce que la deuxième règle démarre, indépendamment de la *stStart* de la première règle. 
  
Les règles doivent être triées de la plus ancienne à la plus récente. Il n'y a aucun chevauchement autorisé entre les règles, de sorte qu'une règle préalable est considérée comme terminée lorsqu'une nouvelle règle commence.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

