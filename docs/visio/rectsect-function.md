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
ms.openlocfilehash: e498ef20f09b4e7b2acc78e39f1a2d885c77e5bf
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773998"
---
# <a name="rectsect-function"></a>Fonction RECTSECT

Calcule le secteur d’un rectangle associé à  *x*  et  *y*  et renvoie un nombre integer de 0 à 4, indiquant le secteur. 
  
## <a name="syntax"></a>Syntaxe

RECTSECT(***width** _, _*_height_*_, _*_x_*_, _*_y_*_, _ *_option_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Requis  <br/> |**String** <br/> |Largeur du rectangle. |
| _height_ <br/> |Requis  <br/> |**String** <br/> |Hauteur du rectangle. |
| _x_ <br/> |Requis  <br/> |**String** <br/> |Coordonnée x. |
| _y_ <br/> |Requis  <br/> |**String** <br/> |Coordonnée y. |
| _option_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment les points des diagonales sont traités. Attribuez la valeur 0 pour utiliser les secteurs de gauche et de droite pour les points d’une diagonale. Attribuez la valeur 1 pour utiliser les secteurs du haut et du bas. |
   
## <a name="remarks"></a>Remarques

Considérons un rectangle qui a une  *largeur et*  une  *hauteur, et*  un point (*x,y*) à partir du point central du rectangle. Tracez des lignes diagonales reliant les coins du rectangle pour le diviser en quatre secteurs avec un point central. Les secteurs de 0 à 4 représentent respectivement le point central, la droite, le haut, le bas et la gauche. 
  
![Les secteurs 0 à 4 représentent respectivement le point central, la droite, le haut, la gauche et le bas](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Exemple

RECTSECT(25,4 mm; 50,8 mm; 25,4 mm; -177,8 mm; 0) 
  
Renvoie 4. 
  

