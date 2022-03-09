---
title: GREEN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
ms.localizationpriority: medium
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Renvoie le composant vert d’une couleur.
ms.openlocfilehash: 42242afa505f381fd44211452decc6390aa5d5c2
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404536"
---
# <a name="green-function"></a>Fonction GREEN

Renvoie le composant vert d’une couleur.
  
## <a name="syntax"></a>Syntaxe

GREEN(***expression*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**Varie** <br/> |Index d’une couleur dans le tableau des couleurs du document, expression qui se résout en une couleur personnalisée (par exemple, RVB ou HSL) ou une référence à une cellule qui contient un index de couleur ou un résultat de couleur. |

### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index. Si  *l’expression*  n’est pas valide, elle renvoie 0 (noir).
  
## <a name="example-1"></a>Exemple 1

GREEN(Sheet.4! FillForegnd)
  
Renvoie la composante verte de la couleur de premier plan de remplissage de Sheet.4.
  
## <a name="example-2"></a>Exemple 2

GREEN(11)
  
Renvoie 128 si le document utilise la palette de couleurs Visio par défaut, où le jaune foncé est la couleur à l’index 11.
  
## <a name="example-3"></a>Exemple 3

GREEN(RVB(10, 20, 30))
  
Renvoie 20.
  