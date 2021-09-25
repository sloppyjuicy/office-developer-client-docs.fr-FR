---
title: RGB Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
ms.localizationpriority: medium
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants rouge, vert et bleu, où chacun d’eux est un nombre compris entre 0 et 255 inclus, ou une expression qui évalue un tel nombre.
ms.openlocfilehash: 9705d0e4c881a2d98e176a9982bbc7a95140755c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573522"
---
# <a name="rgb-function-visioshapesheet"></a>RGB Function (VisioShapeSheet)

Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants rouge, vert et bleu, où chacun d’eux est un nombre compris entre 0 et 255 inclus, ou une expression qui évalue un tel nombre. 
  
## <a name="syntax"></a>Syntaxe

RVB(** *rouge* **, ** *vert* **, ** *bleu* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _rouge_ <br/> |Obligatoire  <br/> |**Number** <br/> |Composante rouge  <br/> |
| _green_ <br/> |Obligatoire  <br/> |**Number** <br/> |Composante vert  <br/> |
| _blue_ <br/> |Obligatoire  <br/> |**Nmber** <br/> |Composante bleu  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs actuelle, elle est automatiquement ajoutée.
  
Le tableau ci-après présente les couleurs standard et les valeurs Rouge, Vert et Bleu qui leur sont associées.
  
|**Color**|**Valeur rouge**|**Valeur vert**|**Valeur bleue**|
|:-----|:-----|:-----|:-----|
|Noir  <br/> |0  <br/> |0  <br/> |0  <br/> |
|Bleu  <br/> |0  <br/> |0  <br/> |255  <br/> |
|Vert  <br/> |0  <br/> |255  <br/> |0  <br/> |
|Cyan  <br/> |0  <br/> |255  <br/> |255  <br/> |
|Rouge  <br/> |255  <br/> |0  <br/> |0  <br/> |
|Magenta  <br/> |255  <br/> |0  <br/> |255  <br/> |
|Jaune  <br/> |255  <br/> |255  <br/> |0  <br/> |
|Blanc  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>Exemple 1

RVB(0,0,255)
  
Renvoie l’index associé à la couleur bleue.
  
## <a name="example-2"></a>Exemple 2

RGB(RED(Sheet.1! FillForegnd),120,0)
  
Renvoie l’index d’une couleur dont la composante rouge correspond au premier plan du remplissage de Feuille.1.
  

