---
title: HUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
ms.localizationpriority: medium
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Renvoie la valeur du composant de teinte d’une couleur.
ms.openlocfilehash: d69aa5dde59ac5d74a8223a18b3f82e33604ea76
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405465"
---
# <a name="hue-function"></a>Fonction HUE

Renvoie la valeur du composant de teinte d’une couleur.
  
## <a name="syntax"></a>Syntaxe

HUE(***expression*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**String** <br/> |Expression qui renvoie à une couleur. |

### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 239 inclus. L’entrée est l’index d’une couleur de la table du document, une expression qui produit une couleur personnalisée (telle que RVB ou TSL) ou une référence à une cellule contenant un index ou un résultat de couleurs. La fonction renvoie 0 si l’entrée n’est pas valide.
  
## <a name="example-1"></a>Exemple 1

HUE(Sheet.4! FillForegnd)
  
Renvoie la composante teinte de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

HUE(7)
  
Renvoie 120 si le document utilise la palette de couleurs par défaut de Microsoft Visio, où cyan est la couleur figurant à l’index 7.
  
## <a name="example-3"></a>Exemple 3

HUE(HSL(10, 20, 30) )
  
Renvoie 10.
  