---
title: SIGN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
ms.localizationpriority: medium
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Renvoie une valeur qui représente le signe d’un nombre.
ms.openlocfilehash: a428db01c0afba9e30f081b2ff7cf4e67a90649b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779235"
---
# <a name="sign-function"></a>Fonction SIGN

Renvoie une valeur qui représente le signe d’un nombre. 
  
## <a name="syntax"></a>Syntaxe

SIGN(** *number* **, ** *fuzz* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Numérique** <br/> | Nombre dont vous voulez déterminer le signe. |
| _fuzz_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Spécifie à partir de quelle valeur proche de zéro le nombre sera considéré comme égal à zéro. |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="remarks"></a>Remarques

La fonction SIGN renvoie 1 si _le nombre_ est positif, 0 si le  nombre est zéro, ou -1 si _le nombre_ est négatif. 
  
Spécifier une  _valeur fuzz_ permet d’éviter les erreurs d’arrondi à un point flottant lorsqu’un calcul est proche de zéro. Si vous ne spécifiez pas de valeur _fuzz_, Visio utilise 1E-9 (0,000000001). Cette option vous permet de fournir une valeur différente lorsque vous mettez des dessins à l’échelle ou lorsque vous souhaitez faire une comparaison exacte. 
  
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
  

