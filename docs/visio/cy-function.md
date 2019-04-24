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
description: Renvoie une valeur monétaire.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344988"
---
# <a name="cy-function"></a>Fonction CY

Renvoie une valeur monétaire.
  
## <a name="syntax"></a>Syntaxe

CY (* * *valeur* * *, * * *cyID* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Facultatif  <br/> |**Numéro ou Chaîne** <br/> |Nombre ou chaîne qui inclut la mise en forme spécifique à la monnaie. Si ce paramètre n'est pas spécifié, la valeur de la devise est mise en forme selon le style monétaire défini dans les paramètres région et langue du système.  <br/> |
| _cyID_ <br/> |Facultatif  <br/> |**Number** <br/> |Un numéro de devise numérique ou une chaîne entre guillemets à trois caractères pour l'abréviation ISO 4217.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour spécifier une autre devise, vous devez inclure un _cyID_valide. Pour obtenir la liste des constantes monétaires, reportez-vous à la rubrique [À propos des constantes monétaires](about-currency-constants.md).
  
Si la _valeur_ n'est pas compatible avec le type de devise désigné, ou si un argument non valide comme «pas un numéro» est spécifié, une #VALUE! est renvoyée. Si _value_ est supérieur à 922 337 203 685 477,5807 ou inférieur à-922 337 203 685 477,5808, un #VALUE! est renvoyée. 
  
Pour une meilleure précision des valeurs monétaires très importantes incluant des fractions d'une unité, comme 3 600 000 000 000, utilisez des arguments de chaîne pour _value_.
  
La spécification d'un _cyID_ non valide renvoie une erreur. 
  
## <a name="example-1"></a>Exemple 1

Si les paramètres régionaux et de langue de l’utilisateur indiquent le dollar des États-Unis :
  
CY (999998.993)
  
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
  

