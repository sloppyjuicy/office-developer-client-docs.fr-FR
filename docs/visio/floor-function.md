---
title: FLOOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arrondit un nombre proche de 0 (zéro), à l’entier suivant ou sur l’occurrence suivante du dénominateur.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788643"
---
# <a name="floor-function"></a>FLOOR, fonction

Arrondit un nombre proche de 0 (zéro), à l’entier suivant ou sur l’occurrence suivante de _multiple_.
  
## <a name="syntax"></a>Syntaxe

FLOOR (** *numéro* **, ** *plusieurs* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir.  <br/> |
| _plusieurs_ <br/> |Obligatoire  <br/> |**Number** <br/> |Multiple vers lequel arrondir.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Remarques

Si _plusieurs_ n’est pas spécifié, le nombre est arrondi proche de 0 à l’entier. 
  
 _Nombre_ et _plusieurs_ doivent avoir le même signe, sinon une #NUM ! erreur est renvoyée. Si _nombre_ ou _multiple_ ne peut pas être convertie en une valeur, un #VALUE ! erreur est renvoyée. Si le _nombre_ ou le _multiple_ est égal à 0, le résultat est 0. 
  
## <a name="example-1"></a>Exemple 1

FLOOR(3.7)
  
Renvoie 3.
  
## <a name="example-2"></a>Exemple 2

FLOOR(-3.7)
  
Renvoie -3.
  
## <a name="example-3"></a>Exemple 3

FLOOR (3.7, 0,5)
  
Renvoie 3,5.
  

