---
title: Fonction RGB (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Renvoie une valeur représentant un index dans la palette de couleurs. Il spécifie une couleur en ses composants rouges, verts et bleus, chacune étant un nombre compris entre 0 et 255, inclus, ou une expression qui renvoie un nombre.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789479"
---
# <a name="rgb-function-visioshapesheet"></a>Fonction RGB (VisioShapeSheet)

Renvoie une valeur représentant un index dans la palette de couleurs. Il spécifie une couleur en ses composants rouges, verts et bleus, chacune étant un nombre compris entre 0 et 255, inclus, ou une expression qui renvoie un nombre. 
  
## <a name="syntax"></a>Syntaxe

RVB (** *rouge* **, ** *vert* **, ** *bleu* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _rouge_ <br/> |Obligatoire  <br/> |**Number** <br/> |Composante rouge  <br/> |
| _vert_ <br/> |Obligatoire  <br/> |**Number** <br/> |Composante vert  <br/> |
| _bleu_ <br/> |Obligatoire  <br/> |**Nmber** <br/> |Composante bleu  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs actuelle, elle est automatiquement ajoutée.
  
Le tableau ci-après présente les couleurs standard et les valeurs Rouge, Vert et Bleu qui leur sont associées.
  
|**Color**|**Valeur rouge**|**Valeur vert**|**Valeur bleu**|
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

RGB(0,0,255)
  
Renvoie l’index associé à la couleur bleue.
  
## <a name="example-2"></a>Exemple 2

RVB (rouge (Sheet.1 ! FillForegnd), 120, 0)
  
Renvoie l’index d’une couleur dont la composante rouge correspond au premier plan du remplissage de Feuille.1.
  

