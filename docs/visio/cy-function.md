---
title: CY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Renvoie une valeur de devise.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788382"
---
# <a name="cy-function"></a>CY, fonction

Renvoie une valeur de devise.
  
## <a name="syntax"></a>Syntaxe

CY (** *valeur* **, ** *IDdev* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _valeur_ <br/> |Facultatif  <br/> |**Nombre ou chaîne** <br/> |Nombre ou chaîne qui inclut la mise en forme spécifique à une devise. Le cas contraire, la valeur de devise est formatée selon le style défini dans les paramètres régionaux et de langue du système.  <br/> |
| _IDdev_ <br/> |Facultatif  <br/> |**Number** <br/> |ID monétaire numérique ou une chaîne entre guillemets trois caractères pour l’abréviation ISO 4217.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour spécifier une autre devise, vous devez inclure un _argument IDdev_valide. Pour obtenir la liste, voir [à propos des constantes de devise](about-currency-constants.md).
  
Si la _valeur_ n’est pas compatible avec le type de devise défini ou si un argument non valide, tel que « pas un nombre » est spécifié, un #VALUE ! erreur est renvoyée. Si la _valeur_ est supérieure à 922,337,203,685,477.5807 ou inférieur à-922,337,203,685,477.5808, un #VALUE ! erreur est renvoyée. 
  
Pour améliorer la précision des valeurs monétaires très élevées contenant des fractions d’une unité, telles que 3,6 trillions, utilisez des arguments de chaîne pour _valeur_.
  
Spécifier un _argument IDdev_ incorrect renvoie une erreur. 
  
## <a name="example-1"></a>Exemple 1

Si les paramètres régionaux et de langue de l’utilisateur indiquent le dollar des États-Unis :
  
CY(999998.993)
  
Renvoie 999 998,99 USD
  
## <a name="example-2"></a>Exemple 2

CY (12345678,993, "USD")
  
Renvoie 12 345 678,99 USD
  
## <a name="example-3"></a>Exemple 3

CY(12345678,993, "EUR")
  
Renvoie 12 345 678,99 EUR
  
## <a name="example-4"></a>Exemple 4

CY(12345678,7832, "XXX")
  
Renvoie 12 345 678,78
  

