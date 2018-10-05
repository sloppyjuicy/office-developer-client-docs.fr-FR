---
title: RECTSECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcule le secteur d’un rectangle associé à x et y et renvoie un entier entre 0 et 4 indiquant le secteur.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395083"
---
# <a name="rectsect-function"></a>Fonction RECTSECT

Calcule le secteur d’un rectangle associé à *x* et *y* et renvoie un entier entre 0 et 4 indiquant le secteur. 
  
## <a name="syntax"></a>Syntaxe

RECTSECT (** *largeur* **, ** *hauteur* **, ** *x* **, ** *y* **, ** *option* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Largeur du rectangle.  <br/> |
| _height_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Hauteur du rectangle.  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Coordonnée x  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Coordonnée y  <br/> |
| _option_ <br/> |Obligatoire  <br/> |**Boolean** <br/> |Indique comment les points des diagonales sont traités. Attribuez la valeur 0 pour utiliser les secteurs de gauche et de droite pour les points d’une diagonale. Attribuez la valeur 1 pour utiliser les secteurs du haut et du bas.  <br/> |
   
## <a name="remarks"></a>Remarques

Considérez un rectangle avec une *largeur* et une *hauteur* et un point (*x, y*) à partir du centre du rectangle. Dessiner des lignes diagonales reliant les coins du rectangle pour le diviser en quatre secteurs avec un point central. Les secteurs de 0 à 4 représentent le point central, droite, haut, gauche et en bas respectivement. 
  
![Secteurs de 0 à 4 représentent le point central, droite, haut, gauche et respectivement en bas](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Exemple

RECTSECT(25,4 mm; 50,8 mm; 25,4 mm; -177,8 mm; 0) 
  
Renvoie 4. 
  

