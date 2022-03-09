---
title: HSL, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
ms.localizationpriority: medium
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants de teinte, de saturation et de luminosité.
ms.openlocfilehash: 241617415b4684e06eff1ed4445450476c141665
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405472"
---
# <a name="hsl-function"></a>Fonction HSL

Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants de teinte, de saturation et de luminosité.
  
## <a name="syntax"></a>Syntaxe

HSL(***hue** _, _*_saturation_*_, _ *_luminosity_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *teinte* <br/> |Requis  <br/> |**Number** <br/> |Teinte de la couleur, exprimée par une valeur de 0 à 239 inclus, ou par une expression ayant cette valeur pour résultat. |
| *saturation* <br/> |Requis  <br/> |**Number** <br/> |Saturation de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat. |
| *luminosity* <br/> |Requis  <br/> |**Number** <br/> | Luminosité de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat. |

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
  