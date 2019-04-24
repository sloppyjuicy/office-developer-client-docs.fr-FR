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
description: Renvoie une valeur qui représente le signe d'un nombre.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357455"
---
# <a name="sign-function"></a>Fonction SIGN

Renvoie une valeur qui représente le signe d'un nombre. 
  
## <a name="syntax"></a>Syntaxe

SIGNE (* * *nombre* * *, * * *Fuzz* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> | Nombre dont vous voulez déterminer le signe.  <br/> |
| _approximative_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Spécifie à partir de quelle valeur proche de zéro le nombre sera considéré comme égal à zéro.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="remarks"></a>Remarques

La fonction SIGN renvoie 1 si le _nombre_ est positif, 0 si le _nombre_ est égal à zéro ou-1 si le _nombre_ est négatif. 
  
Spécification une valeur __ de robustesse permet d'éviter les erreurs de roundoff de virgule flottante lorsqu'un calcul est presque égal à zéro. Si vous ne spécifiez pas de valeur de _Fuzz_ , Visio utilise 1e-9 (0,000000001). Cette option vous permet de fournir une valeur différente lorsque vous mettez des dessins à l’échelle ou lorsque vous souhaitez faire une comparaison exacte. 
  
## <a name="example-1"></a>Exemple 1

SIGN (-5)
  
Renvoie -1.
  
## <a name="example-2"></a>Exemple 2

SIGNE (0)
  
Renvoie 0.
  
## <a name="example-3"></a>Exemple 3

SIGN (0.00000000001)
  
Renvoie 0.
  
## <a name="example-4"></a>Exemple 4

SIGN (0.00000000001, 0)
  
Renvoie 1.
  

