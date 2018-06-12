---
title: BOUNDINGBOXDIST, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788179"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST, fonction

Renvoie la mesure de la partie spécifiée du cadre englobant de la forme. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

BOUNDINGBOXDIST (** *Index* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatoire  <br/> |**Number** <br/> |La partie de la forme englobant pour mesurer et retourner. Voir la section Remarques pour les valeurs possibles.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **Number**
  
## <a name="remarks"></a>Note

 *Index* peut être une des valeurs suivantes. 
  
|**Item**|**Valeur**|
|:-----|:-----|
|Largeur  <br/> |0  <br/> |
|Hauteur  <br/> |1  <br/> |
|Bord gauche à l’axe de la forme  <br/> |2  <br/> |
|Axe de la forme au bord droit  <br/> |3  <br/> |
|Axe de la forme au bord supérieur  <br/> |4  <br/> |
|Bord inférieur à l’axe de la forme  <br/> |5  <br/> |
|Centre du cadre englobant à AxeX  <br/> |6  <br/> |
|Centre du cadre englobant à AxeY  <br/> |7  <br/> |
   

