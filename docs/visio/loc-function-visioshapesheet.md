---
title: Loc, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Prend un point défini dans le système de coordonnées local d’une forme et renvoie le point équivalent exprimé dans le système de coordonnées locales de la forme associée à la formule.
ms.openlocfilehash: 196e2c92ea6ab410b6ecca9767b68605e4eb4d30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788984"
---
# <a name="loc-function-visioshapesheet"></a>Loc, fonction (VisioShapeSheet)

Prend un point défini dans le système de coordonnées local d’une forme et renvoie le point équivalent exprimé dans le système de coordonnées locales de la forme associée à la formule. 
  
## <a name="syntax"></a>Syntaxe

LOC (** *point* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Point défini dans les coordonnées locales d’une forme.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Les coordonnées locales sont mesurées à partir du coin inférieur gauche du rectangle de sélection de la forme. Les deux formes doivent figurer sur la même page.
  
## <a name="example"></a>Exemple

LOC (PNT (feuille.5 ! LocPinX, feuille.5 ! LocPinY)) 
  
Dans cette expression, PNT convertit un ensemble de coordonnées locales de Feuille.5 en un point (Feuille.5 est une autre forme sur la même page de dessin). LOC convertit ensuite ce point en un point équivalent dans le système de coordonnées locales de la forme active en se basant sur le coin inférieur gauche du rectangle de sélection de la forme active. 
  
Le chiffre 5 de la feuille.5 est le numéro d’identification de la forme qui s’affiche dans la boîte de dialogue **Nom de la forme** (onglet**développeur** ). 
  

