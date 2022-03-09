---
title: CY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
ms.localizationpriority: medium
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Renvoie une valeur monétaire.
ms.openlocfilehash: a493631aa6af9db3ccd3f9337f00ec4d17a8d759
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404572"
---
# <a name="cy-function"></a>Fonction CY

Renvoie une valeur monétaire.
  
## <a name="syntax"></a>Syntaxe

CY(***value** _, _ *_cyID_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *value* <br/> |Facultatif  <br/> |**Numéro ou Chaîne** <br/> |Nombre ou chaîne qui inclut une mise en forme spécifique à la devise. Si elle n’est pas spécifiée, la valeur monétaire est mise en forme en fonction du style monétaire dans les paramètres région et langue du système. |
| *cyID* <br/> |Facultatif  <br/> |**Number** <br/> |ID monétaire numérique ou chaîne entre deux caractères pour l’abréviation ISO 4217. |

## <a name="remarks"></a>Remarques

Pour spécifier une autre devise, vous devez inclure un  *cyID valide*. Pour obtenir la liste des constantes monétaires, reportez-vous à la rubrique [À propos des constantes monétaires](about-currency-constants.md).
  
Si  *la valeur* n’est pas compatible avec le type de devise désigné ou si un argument non valide tel que « pas un nombre » est spécifié, un #VALUE! est renvoyée. Si  la valeur est supérieure à 922 337 203 685 477,5807 ou inférieure à -922 337 203 685 477,5808, #VALUE ! est renvoyée.
  
Pour une meilleure précision avec des valeurs monétaires très élevées qui incluent des fractions d’une unité, telles que 3,6 billions, utilisez des arguments de chaîne pour la  *valeur*.
  
La spécification d’un  *cyID non valide* renvoie une erreur.
  
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
  