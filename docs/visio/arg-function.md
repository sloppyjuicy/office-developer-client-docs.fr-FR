---
title: ARG, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Spécifie un argument que la cellule d’appel peut passer à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d’appel ne transmet une valeur pour l’argument. Renvoie la valeur spécifiée par la cellule d’appel et le paramètre argName correspondant.
ms.openlocfilehash: 3d0e126e0fa075ff2a07773197c1973e6b0249d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788051"
---
# <a name="arg-function"></a>ARG, fonction

Spécifie un argument que la cellule d’appel peut passer à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d’appel ne transmet une valeur pour l’argument. Renvoie la valeur spécifiée par la cellule d’appel et le paramètre argName correspondant.
  
## <a name="syntax"></a>Syntaxe

ARG (** *argName* **, [** *defaultValue* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Le nom d’un argument que peut transmettre la cellule d’appel à la fonction.  <br/> |
| _Valeur par défaut_ <br/> |Facultatif  <br/> |**Numérique** <br/> |La valeur renvoyée par ARG si la cellule d’appel n’a pas transmis de valeur pour le paramètre _argName_ .  <br/> |
   
## <a name="remarks"></a>Note

Si vous développez des formes, vous pouvez créer des fonctions personnalisées en plaçant une expression dans une cellule et en appelant cette expression d’une ou plusieurs autres cellules. L’expression peut inclure des chaînes littérales, des fonctions ShapeSheet et des références de cellules. L’expression peut aussi inclure des arguments spécifiques transmis par la cellule d’appel. 
  
La cellule d’appel spécifie la cellule qui contient la fonction personnalisée, ainsi que tous les arguments à transmettre à la fonction. La cellule d’expression est évaluée et le résultat renvoyé à la cellule d’appel.
  
## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser la fonction ARG conjointement avec la fonction EVALCELL pour trouver la valeur médiane parmi un ensemble de trois valeurs. 
  
Dans la cellule d’expression, placez le code suivant qui définit la fonction personnalisée : 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

Dans les cellules d’appel, placez le code suivant qui appelle la fonction personnalisée :
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


