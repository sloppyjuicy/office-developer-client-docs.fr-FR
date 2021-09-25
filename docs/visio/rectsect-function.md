---
title: RECTSECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
ms.localizationpriority: medium
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcule le secteur d’un rectangle associé à x et y et renvoie un nombre integer de 0 à 4, indiquant le secteur.
ms.openlocfilehash: 73e7e3aa440d67eed2a6a2706321092ec101cfdf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607912"
---
# <a name="rectsect-function"></a>Fonction RECTSECT

Calcule le secteur d’un rectangle associé à  *x*  et  *y*  et renvoie un nombre integer de 0 à 4, indiquant le secteur. 
  
## <a name="syntax"></a>Syntaxe

RECTSECT(***width** _, _*_height_*_, _*_x_*_, _*_y_*_, _ *_option_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Obligatoire  <br/> |**String** <br/> |Largeur du rectangle.  <br/> |
| _height_ <br/> |Obligatoire  <br/> |**String** <br/> |Hauteur du rectangle.  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée x.  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée y.  <br/> |
| _option_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment les points des diagonales sont traités. Attribuez la valeur 0 pour utiliser les secteurs de gauche et de droite pour les points d’une diagonale. Attribuez la valeur 1 pour utiliser les secteurs du haut et du bas.  <br/> |
   
## <a name="remarks"></a>Remarques

Considérons un rectangle qui a une  *largeur*  et une  *hauteur,*  et un point (*x,y*) à partir du point central du rectangle. Tracez des lignes diagonales reliant les coins du rectangle pour le diviser en quatre secteurs avec un point central. Les secteurs de 0 à 4 représentent respectivement le point central, la droite, le haut, le bas et la gauche. 
  
![Les secteurs 0 à 4 représentent respectivement le point central, la droite, le haut, la gauche et le bas](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Exemple

RECTSECT(25,4 mm; 50,8 mm; 25,4 mm; -177,8 mm; 0) 
  
Renvoie 4. 
  

