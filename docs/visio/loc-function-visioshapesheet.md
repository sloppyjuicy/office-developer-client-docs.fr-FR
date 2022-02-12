---
title: LOC Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
ms.localizationpriority: medium
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Prend un point défini dans les coordonnées locales d’une forme et renvoie le point équivalent exprimé dans les coordonnées locales de la forme associée à la formule.
ms.openlocfilehash: cd1daa7c4db47af61c56c4195414381c7a53884d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62786811"
---
# <a name="loc-function-visioshapesheet"></a>LOC Function (VisioShapeSheet)

Prend un point défini dans les coordonnées locales d’une forme et renvoie le point équivalent exprimé dans les coordonnées locales de la forme associée à la formule. 
  
## <a name="syntax"></a>Syntaxe

LOC(** *point* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Requis  <br/> |**String** <br/> | Point défini dans les coordonnées locales d’une forme. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Les coordonnées locales sont mesurées à partir du coin inférieur gauche du rectangle de sélection de la forme. Les deux formes doivent figurer sur la même page.
  
## <a name="example"></a>Exemple

LOC(PNT(Sheet.5! LocPinX, Sheet.5! LocPinY)) 
  
Dans cette expression, PNT convertit un ensemble de coordonnées locales de Feuille.5 en un point (Feuille.5 est une autre forme sur la même page de dessin). LOC convertit ensuite ce point en un point équivalent dans le système de coordonnées locales de la forme active en se basant sur le coin inférieur gauche du rectangle de sélection de la forme active. 
  
Le chiffre 5 de la Feuille.5 est l’identificateur de la forme, tel qu’il s’affiche dans la boîte de dialogue **Nom de la forme** (onglet **Développeur**). 
  

