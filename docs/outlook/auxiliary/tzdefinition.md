---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier comprenant toutes les règles de décalage de fuseau horaire historique, actuelle et future pour l’heure d’été.
ms.openlocfilehash: 02de84f2438adc4d7cbf2af7dd4aecb61479f97f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381609"
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
  
> Indique que le nom de clé qui représente le fuseau horaire dans le Windows registre est valide. Étant donné que chaque fuseau horaire doit toujours être identifié par un nom de clé, ce membre doit toujours avoir la **valeur TZDEFINITION_FLAG_VALID_KEYNAME**.

_pwszKeyName_
  
> Nom de la clé pour ce fuseau horaire dans le Windows registre. Ce nom ne doit pas être localisée. Il a une taille maximale de **MAX_PATH**, qui est définie dans le fichier d’en-tête du Kit de développement logiciel (SDK) Windows windows.h.

_cRules_
  
> Nombre de règles de fuseau horaire pour cette définition. Le nombre maximal de règles est **TZ_MAX_RULES**.

_rgRules_
  
> Tableau de règles qui décrivent quand des changements se produisent.

## <a name="remarks"></a>Remarques

Il doit y avoir au moins une règle _dans rgRules_. La première règle de _rgRules_ est considérée comme la règle à utiliser jusqu’au démarrage de la deuxième règle, quel que soit le _stStart_ de la première règle.
  
Les règles doivent être triées du plus ancien au plus récent. Il n’y a aucun chevauchement autorisé entre les règles, de sorte qu’une règle antérieure est considérée comme se terminer au démarrage d’une nouvelle règle.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
