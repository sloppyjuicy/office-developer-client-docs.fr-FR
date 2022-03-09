---
title: RED, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
ms.localizationpriority: medium
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Renvoie le composant rouge d’une couleur.
ms.openlocfilehash: 327f4693e9931b36f584939fd3dfa5ecb8bd0d56
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406088"
---
# <a name="red-function"></a>Fonction RED

Renvoie le composant rouge d’une couleur.
  
## <a name="syntax"></a>Syntaxe

RED(***expression*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**Varie** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs. |

### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index. Si l’argument *expression* n’est pas valide, la fonction renvoie 0 (noir).
  
## <a name="example-1"></a>Exemple 1

RED(22)
  
Renvoie 51 si le document utilise la palette de couleurs par défaut de Microsoft Office Visio, où le gris foncé a l’index de couleur 22.
  
## <a name="example-2"></a>Exemple 2

RED(Char.Color)
  
Renvoie la valeur de la composante rouge de la couleur de police actuelle.
  
## <a name="example-3"></a>Exemple 3

RED(RVB(10, 20, 30))
  
Renvoie 10.
  