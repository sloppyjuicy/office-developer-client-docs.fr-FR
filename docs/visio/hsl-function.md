---
title: HSL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
ms.localizationpriority: medium
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants de teinte, de saturation et de luminosité.
ms.openlocfilehash: 1cf21354c5c514327b5cf3a8bd0fd76e5bd099f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570476"
---
# <a name="hsl-function"></a>Fonction HSL

Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants de teinte, de saturation et de luminosité.
  
## <a name="syntax"></a>Syntaxe

HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _teinte_ <br/> |Obligatoire  <br/> |**Number** <br/> |Teinte de la couleur, exprimée par une valeur de 0 à 239 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
| _saturation_ <br/> |Obligatoire  <br/> |**Number** <br/> |Saturation de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
| _luminosity_ <br/> |Obligatoire  <br/> |**Number** <br/> | Luminosité de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs du document actif, elle est ajoutée dans la liste des couleurs associée au document. 
  
Le tableau suivant répertorie les couleurs standard ainsi que la teinte, la saturation et la luminosité qui leur sont associées. 
  
|**Color**|**Teinte**|**Saturation**|**Luminosité**|
|:-----|:-----|:-----|:-----|
|Noir  <br/> |0  <br/> |0  <br/> |24  <br/> |
|Bleu  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Vert  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Cyan  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Rouge  <br/> |0  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Jaune  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Blanc  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Exemple 1

HSL(160 240 120)
  
Renvoie l’index associé à la couleur bleue.
  
## <a name="example-2"></a>Exemple 2

HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))
  
Renvoie l’index de la couleur de remplissage de premier plan en augmentant la luminosité.
  

