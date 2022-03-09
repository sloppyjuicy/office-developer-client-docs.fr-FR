---
title: BOUNDINGBOXRECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.
ms.openlocfilehash: 838a898203bd87665c43203d196855df93a1ee8e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373549"
---
# <a name="boundingboxrect-function"></a>Fonction BOUNDINGBOXRECT

Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

BOUNDINGBOXRECT(***Index*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *Index* <br/> |Obligatoire  <br/> |**Entier** <br/> |Bord du cadre englobant de la forme pour lequel récupérer les coordonnées. Voir la section Remarques pour les valeurs possibles. |

### <a name="return-value"></a>Valeur renvoyée

 **Number**
  
## <a name="remarks"></a>Remarques

 *Index* peut prendre l’une des valeurs suivantes.
  
|**Item**|**Valeur**|
|:-----|:-----|
|Bord gauche  <br/> |0  <br/> |
|Bord droit  <br/> |1  <br/> |
|Bord supérieur  <br/> |2  <br/> |
|Bord inférieur  <br/> |3  <br/> |

Si la forme a un parent, la valeur de retour se trouve dans le système de coordonnées de ce parent.
  