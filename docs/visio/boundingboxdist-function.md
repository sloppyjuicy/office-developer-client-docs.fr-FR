---
title: BOUNDINGBOXDIST, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.
ms.openlocfilehash: f8b71238f177283d829ab0bd948d24ab3dcebda0
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372716"
---
# <a name="boundingboxdist-function"></a>Fonction BOUNDINGBOXDIST

Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

BOUNDINGBOXDIST(***Index*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *Index* <br/> |Obligatoire  <br/> |**Number** <br/> |Partie du cadre de limite de la forme à mesurer et à renvoyer. Les valeurs possibles, reportez-vous à la section Remarques. |

### <a name="return-value"></a>Valeur renvoyée

 **Number**
  
## <a name="remarks"></a>Remarques

 *Index* peut prendre l’une des valeurs suivantes.
  
|**Item**|**Valeur**|
|:-----|:-----|
|Largeur  <br/> |0  <br/> |
|Hauteur  <br/> |1  <br/> |
|Bord gauche à l’axe de la forme  <br/> |2  <br/> |
|Axe de la forme au bord droit  <br/> |3  <br/> |
|Axe de la forme au bord supérieur  <br/> |4  <br/> |
|Bord inférieur à l’axe de la forme  <br/> |5  <br/> |
|Centre du cadre englobant à AxeX  <br/> |6   <br/> |
|Centre du cadre englobant à AxeY  <br/> |7   <br/> |
