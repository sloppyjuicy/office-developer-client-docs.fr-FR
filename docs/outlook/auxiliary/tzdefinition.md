---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier comprenant toutes les règles de décalage de fuseau horaire historique, actuelle et future pour l’heure d’été.
ms.openlocfilehash: 845d2cb2195eb6736fe03f0b66e5110d692538ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631131"
---
# <a name="tzdefinition"></a>TZDEFINITION

Représente un fuseau horaire entier comprenant toutes les règles de décalage de fuseau horaire historique, actuelle et future pour l’heure d’été.
  
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
  
> Indique que le nom de clé qui représente le fuseau horaire dans le Windows registre est valide. Étant donné que chaque fuseau horaire doit toujours être identifié par un nom de **clé,** ce membre doit toujours avoir la valeur TZDEFINITION_FLAG_VALID_KEYNAME .
    
_pwszKeyName_
  
> Nom de la clé pour ce fuseau horaire dans le Windows registre. Ce nom ne doit pas être localisée. Il a une taille maximale de **MAX_PATH**, qui est définie dans le fichier d’en-tête du Kit de développement logiciel (SDK) Windows windows.h. 
    
_cRules_
  
> Nombre de règles de fuseau horaire pour cette définition. Le nombre maximal de règles est **TZ_MAX_RULES**. 
    
_rgRules_
  
> Tableau de règles qui décrivent quand des changements se produisent.
    
## <a name="remarks"></a>Remarques

Il doit y avoir au moins une règle  *dans rgRules*  . La première règle de  *rgRules*  est considérée comme la règle à utiliser jusqu’au démarrage de la deuxième règle, quel que soit le  *stStart*  de la première règle. 
  
Les règles doivent être triées du plus ancien au plus récent. Il n’y a pas de chevauchement autorisé entre les règles, de sorte qu’une règle antérieure est considérée comme se terminer au démarrage d’une nouvelle règle.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

