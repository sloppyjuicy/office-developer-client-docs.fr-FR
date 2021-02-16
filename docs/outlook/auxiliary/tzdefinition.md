---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier comprenant toutes les règles de décalage de fuseau horaire historique, actuelle et future pour l’heure d’été.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429340"
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
  
> Indique que le nom de clé qui représente le fuseau horaire dans le Registre Windows est valide. Étant donné que chaque fuseau horaire doit toujours être identifié par un nom de **clé,** ce membre doit toujours avoir la valeur TZDEFINITION_FLAG_VALID_KEYNAME .
    
_pwszKeyName_
  
> Nom de la clé pour ce fuseau horaire dans le Registre Windows. Ce nom ne doit pas être localisée. Sa taille maximale est **MAX_PATH,** qui est définie dans le fichier d’en-tête du Kit de développement logiciel (SDK) Windows windows.h. 
    
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

