---
title: BOUNDINGBOXDIST, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348964"
---
# <a name="boundingboxdist-function"></a>Fonction BOUNDINGBOXDIST

Renvoie la mesure de la partie spécifiée du cadre englobant de la forme. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

BOUNDINGBOXDIST (* * *index* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatoire  <br/> |**Number** <br/> |Partie de la zone de délimitation de la forme à mesurer et à renvoyer. Les valeurs possibles, reportez-vous à la section Remarques.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Number**
  
## <a name="remarks"></a>Remarques

 *Index* peut prendre l'une des valeurs suivantes. 
  
|**Item**|**Valeur**|
|:-----|:-----|
|Largeur  <br/> |0  <br/> |
|Hauteur  <br/> |0,1  <br/> |
|Bord gauche à l’axe de la forme  <br/> |n°2  <br/> |
|Axe de la forme au bord droit  <br/> |3  <br/> |
|Axe de la forme au bord supérieur  <br/> |4  <br/> |
|Bord inférieur à l’axe de la forme  <br/> |disque  <br/> |
|Centre du cadre englobant à AxeX  <br/> |6.x  <br/> |
|Centre du cadre englobant à AxeY  <br/> |7j/7  <br/> |
   

