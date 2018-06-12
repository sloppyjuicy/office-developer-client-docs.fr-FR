---
title: SIGN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Renvoie une valeur qui représente le signe d’un nombre.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789747"
---
# <a name="sign-function"></a>SIGN, fonction

Renvoie une valeur qui représente le signe d’un nombre. 
  
## <a name="syntax"></a>Syntaxe

CONNEXION (** *numéro* **, ** *robustesse* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> | Nombre dont vous voulez déterminer le signe.  <br/> |
| _aléatoires_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Spécifie à partir de quelle valeur proche de zéro le nombre sera considéré comme égal à zéro.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Numérique
  
## <a name="remarks"></a>Note

La fonction SIGN renvoie 1 si le _nombre_ est positif, 0 si le _nombre_ est égal à zéro ou -1 si le _nombre_ est négatif. 
  
Specifyin une valeur _aléatoire_ permet d’éviter les erreurs de l’argument à virgule flottante lorsqu’un calcul est presque égale à zéro. Si vous ne spécifiez pas une valeur _robustesse_ , Visio utilise 1E-9 (0,000000001). Vous souhaiterez peut-être fournir une valeur différente lorsque vous redimensionnez dessins ou lorsque vous souhaitez une comparaison exacte. 
  
## <a name="example-1"></a>Exemple 1

SIGN(-5)
  
Renvoie -1.
  
## <a name="example-2"></a>Exemple 2

SIGN(0)
  
Renvoie 0.
  
## <a name="example-3"></a>Exemple 3

SIGN(0.00000000001)
  
Renvoie 0.
  
## <a name="example-4"></a>Exemple 4

SIGN(0.00000000001,0)
  
Renvoie 1.
  

