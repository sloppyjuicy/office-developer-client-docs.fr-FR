---
title: HSL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Renvoie une valeur représentant un index dans la palette de couleurs. Il spécifie une couleur en sa teinte, la saturation et composants de luminosité.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788789"
---
# <a name="hsl-function"></a>HSL, fonction

Renvoie une valeur représentant un index dans la palette de couleurs. Il spécifie une couleur en sa teinte, la saturation et composants de luminosité.
  
## <a name="syntax"></a>Syntaxe

TSL (** *teinte* **, ** *saturation* **, ** *luminosité* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _teinte_ <br/> |Obligatoire  <br/> |**Number** <br/> |Teinte de la couleur, exprimée par une valeur de 0 à 239 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
| _saturation_ <br/> |Obligatoire  <br/> |**Number** <br/> |Saturation de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
| _luminosité_ <br/> |Obligatoire  <br/> |**Number** <br/> | Luminosité de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs du document actif, elle est ajoutée dans la liste des couleurs associée au document. 
  
Le tableau suivant répertorie les couleurs standard ainsi que la teinte, la saturation et la luminosité qui leur sont associées. 
  
|**Color**|**Teinte**|**Valeur de la saturation**|**Luminosité**|
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

HSL(160,240,120)
  
Renvoie l’index associé à la couleur bleue.
  
## <a name="example-2"></a>Exemple 2

HSL(Hue(FillForegnd),SAT(FillForegnd),min(Lum(FillForegnd)+100,240))
  
Renvoie l’index de la couleur de remplissage de premier plan en augmentant la luminosité.
  

