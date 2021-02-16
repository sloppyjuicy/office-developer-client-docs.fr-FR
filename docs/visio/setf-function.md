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
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425973"
---
# <a name="setf-function"></a>Fonction SETF

Définit la formule d’une cellule. 
  
## <a name="syntax"></a>Syntaxe

SETF( GETREF(** *cell* ** ), ** *formula* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cell_ <br/> |Obligatoire  <br/> |**String** <br/> |Cellule dont la formule doit être définie.  <br/> |
| _formula_ <br/> |Obligatoire  <br/> |**String** <br/> |Formule à utiliser  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’elle est évaluée, le résultat de l’expression _dans_ la formule devient la nouvelle formule dans la _cellule._ Si _la formule_ est entre guillemets, l’expression entre guillemets est écrite dans la _cellule._ Pour définir  _une cellule_ sur une chaîne, inséz-la  _entre_ trois guillemets. 
  
La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.
  
Si  _la cellule_ n’est pas spécifiée à l’aide de GETREF ou en tant que chaîne, la fonction renvoie une erreur et aucune formule de cellule n’est modifiée. Si _la formule_ contient une erreur de syntaxe, la fonction renvoie une erreur et la formule de la cellule n’est pas modifiée.  
  
## <a name="example-1"></a>Exemple 1

SETF( GETREF(Scratch.A1), 1,5 en \* 6 + 1 pi)
  
Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.
  
## <a name="example-2"></a>Exemple 2

SETF( GETREF(Scratch.A1), « 1,5 en \* 6 + 1 m »)
  
Définit la formule de Scratch. A1 to the expression 1.5 in \* 6+1 ft.
  
## <a name="example-3"></a>Exemple 3

SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")
  
Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".
  

