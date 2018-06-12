---
title: GUARD, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protège l’expression contre la suppression ou la modification par les actions effectuées dans la fenêtre de dessin, par exemple, que le déplacement, le redimensionnement, le regroupement ou la dissociation des formes.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788739"
---
# <a name="guard-function"></a>GUARD, fonction

Protège *l’expression* contre la suppression ou la modification par les actions effectuées dans la fenêtre de dessin, par exemple, que le déplacement, le redimensionnement, le regroupement ou la dissociation des formes. 
  
## <a name="syntax"></a>Syntaxe

GUARD (** *expression* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.  <br/> |
   
## <a name="remarks"></a>Note

Les cellules les plus souvent concernées par la fonction GUARD sont les cellules Width, Height, PinX et PinY. 
  
La protection d’une formule dans n’importe quelle cellule empêche que la valeur de cette dernière ne soit modifiée par des actions exécutées dans la fenêtre de dessin. Une même action peut toutefois avoir une incidence sur plusieurs cellules et chacune d’elles doit être protégée pour éviter des modifications inattendues de l’aspect des formes. 
  
## <a name="example"></a>Exemple

GUARD(TEXTWIDTH(TheText) + 0,5 po) 
  
Cette expression dans la cellule Largeur de la section Transformation de la forme évite que l’expression (TEXTWIDTH(TheText) + 0,5 po) ne soit remplacée par une autre valeur lorsque la largeur de la forme est modifiée dans la fenêtre de dessin. La cellule TheText est générée lorsque la composition du texte de la forme qui y est associée est modifiée. 
  

