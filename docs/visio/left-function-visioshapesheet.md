---
title: Fonction LEFT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Renvoie l’ou les caractères de la plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788932"
---
# <a name="left-function-visioshapesheet"></a>Fonction LEFT (VisioShapeSheet)

Renvoie l’ou les caractères de la plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

GAUCHE (** *texte* **, [, ** *nb_cars_opt* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chaîne de texte qui contient les caractères à extraire.  <br/> |
| _nb_cars_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Nombre de caractères à extraire.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de _nb_cars_opt_ doit être supérieure ou égale à zéro (0). 
  
Si _nb_cars_opt_ est supérieur à la longueur du texte, gauche renvoie tout le texte. Si _nb_cars_opt_ est omis, il est supposé pour être 1. 
  
## <a name="example"></a>Exemple

LEFT ("Janvier 1 2004", 3) 
  
Renvoie la valeur "Jan". 
  

