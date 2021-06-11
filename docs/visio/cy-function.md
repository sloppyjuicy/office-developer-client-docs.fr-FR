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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433555"
---
# <a name="cy-function"></a>Fonction CY

Renvoie une valeur monétaire.
  
## <a name="syntax"></a>Syntaxe

CY(** *value* **, ** *cyID* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Facultatif  <br/> |**Numéro ou Chaîne** <br/> |Nombre ou chaîne qui inclut une mise en forme spécifique à la devise. Si elle n’est pas spécifiée, la valeur monétaire est mise en forme en fonction du style monétaire dans les paramètres région et langue du système.  <br/> |
| _cyID_ <br/> |Facultatif  <br/> |**Number** <br/> |ID monétaire numérique ou chaîne entre deux caractères pour l’abréviation ISO 4217.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour spécifier une autre devise, vous devez inclure un _cyID valide._ Pour obtenir la liste des constantes monétaires, reportez-vous à la rubrique [À propos des constantes monétaires](about-currency-constants.md).
  
Si  _la valeur_ n’est pas compatible avec le type de devise désigné, ou si un argument non valide tel que « pas un nombre » est spécifié, un #VALUE! est renvoyée. Si  la valeur est supérieure à 922 337 203 685 477,5807 ou inférieure à -922 337 203 685 477,5808, un #VALUE! est renvoyée. 
  
Pour une meilleure précision avec des valeurs monétaires très élevées qui incluent des fractions d’une unité, telles que 3,6 billions, utilisez des arguments de chaîne pour la _valeur._
  
La spécification d’un  _cyID non valide_ renvoie une erreur. 
  
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
  

