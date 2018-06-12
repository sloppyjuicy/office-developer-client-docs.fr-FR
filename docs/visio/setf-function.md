---
title: SETF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Définit la formule d’une cellule.
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789619"
---
# <a name="setf-function"></a>SETF, fonction

Définit la formule d’une cellule. 
  
## <a name="syntax"></a>Syntaxe

SETF (GETREF (** *cellule* **), ** *formule* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellule_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |La cellule dont la formule à définir.  <br/> |
| _formula_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Formule à utiliser  <br/> |
   
## <a name="remarks"></a>Note

Lors de l’évaluation, le résultat de l’expression _formule_ devient la nouvelle formule de _cellule_. Si la _formule_ est placé entre guillemets, l’expression entre guillemets est écrit dans la _cellule_. Pour définir la _cellule_ à une chaîne, mettez-le _formule_ dans trois jeux de guillemets doubles. 
  
La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.
  
Si la _cellule_ n’est pas spécifié à l’aide de GETREF ou sous forme de chaîne, la fonction renvoie une erreur, et pas la cellule est modifiée. Si la _formule_ contient une erreur de syntaxe, la fonction renvoie une erreur et la formule de _cellule_ n’est pas modifiée. 
  
## <a name="example-1"></a>Exemple 1

SETF (GETREF(Scratch.A1), 1,5 dans \* 6 + 1 ft)
  
Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.
  
## <a name="example-2"></a>Exemple 2

SETF (GETREF(Scratch.A1), « 1,5 pouces \* 6 + 1 ft »)
  
Définir la formule Scratch.a1. A1 à l’expression 1,5 dans\*ft 6 + 1.
  
## <a name="example-3"></a>Exemple 3

SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")
  
Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".
  

