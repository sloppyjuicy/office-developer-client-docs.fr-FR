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
description: Définit la formule d'une cellule.
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325836"
---
# <a name="setf-function"></a>Fonction SETF

Définit la formule d'une cellule. 
  
## <a name="syntax"></a>Syntaxe

SETF (GETREF (* * *Cell* * *), * * *Formula* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _Cell_ <br/> |Obligatoire  <br/> |**String** <br/> |Cellule dont la formule doit être définie.  <br/> |
| _formula_ <br/> |Obligatoire  <br/> |**String** <br/> |Formule à utiliser  <br/> |
   
## <a name="remarks"></a>Remarques

Lors de l'évaluation, le résultat de l'expression dans _Formula_ devient la nouvelle formule dans la _cellule_. Si la _formule_ est placée entre guillemets, l'expression quotée est écrite dans la _cellule_. Pour définir la _cellule_ sur une chaîne, mettez la _formule_ entre trois guillemets. 
  
La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.
  
Si la _cellule_ n'est pas spécifiée à l'aide de getRef ou sous forme de chaîne, la fonction renvoie une erreur et aucune formule de cellule n'est modifiée. Si la _formule_ contient une erreur de syntaxe, la fonction renvoie une erreur et la formule dans la _cellule_ n'est pas modifiée. 
  
## <a name="example-1"></a>Exemple 1

SETF (GETREF (Scratch. a1), 1,5 en \* 6 + 1 ft)
  
Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.
  
## <a name="example-2"></a>Exemple 2

SETF (GETREF (Scratch. a1), "1,5 en \* 6 + 1 ft")
  
Définit la formule de travail. A1 à l'expression 1,5 en\*6 + 1 ft.
  
## <a name="example-3"></a>Exemple 3

SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")
  
Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".
  

