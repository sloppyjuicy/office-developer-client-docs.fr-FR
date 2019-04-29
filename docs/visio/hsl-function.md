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
description: Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants teinte, saturation et luminosité.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420961"
---
# <a name="hsl-function"></a>Fonction HSL

Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants teinte, saturation et luminosité.
  
## <a name="syntax"></a>Syntaxe

TSL (* * *teinte* * *, * * *saturation* * *, * * *luminosité* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _couleurs_ <br/> |Obligatoire  <br/> |**Number** <br/> |Teinte de la couleur, exprimée par une valeur de 0 à 239 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
| _curseur_ <br/> |Obligatoire  <br/> |**Number** <br/> |Saturation de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
| _luminosité_ <br/> |Obligatoire  <br/> |**Number** <br/> | Luminosité de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs du document actif, elle est ajoutée dans la liste des couleurs associée au document. 
  
Le tableau suivant répertorie les couleurs standard ainsi que la teinte, la saturation et la luminosité qui leur sont associées. 
  
|**Couleur**|**Teinte**|**Saturation**|**Luminosité**|
|:-----|:-----|:-----|:-----|
|Noir  <br/> |0  <br/> |0  <br/> |heures/24  <br/> |
|Bleu  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Vert  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Cyan  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Rouge  <br/> |0  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Jaune  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Blanc  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Exemple 1

TSL (160240120)
  
Renvoie l’index associé à la couleur bleue.
  
## <a name="example-2"></a>Exemple 2

TSL (TEINTe (FillForegnd), SAT (FillForegnd), MIN (LUM (FillForegnd) + 100240))
  
Renvoie l’index de la couleur de remplissage de premier plan en augmentant la luminosité.
  

