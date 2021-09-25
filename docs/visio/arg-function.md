---
title: ARG, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Spécifie un argument que la cellule d’appel peut transmettre à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d’appel ne passe pas de valeur pour l’argument. Renvoie la valeur spécifiée par la cellule d’appel et le paramètre argName correspondant.
ms.openlocfilehash: df1e3106eb624064be48bed76201dae6fe40e3cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628856"
---
# <a name="arg-function"></a>Fonction ARG

Spécifie un argument que la cellule d’appel peut transmettre à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d’appel ne passe pas de valeur pour l’argument. Renvoie la valeur spécifiée par la cellule d’appel et le paramètre argName correspondant.
  
## <a name="syntax"></a>Syntaxe

ARG(***argName** _,[ _ *_defaultValue_** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Obligatoire  <br/> |**String** <br/> |Le nom d’un argument que peut transmettre la cellule d’appel à la fonction.  <br/> |
| _valeur par défaut_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Valeur renvoyée par ARG si la cellule d’appel n’a pas passé de valeur pour le _paramètre argName._  <br/> |
   
## <a name="remarks"></a>Remarques

Si vous développez des formes, vous pouvez créer des fonctions personnalisées en plaçant une expression dans une cellule et en appelant cette expression d’une ou plusieurs autres cellules. L’expression peut inclure des chaînes littérales, des fonctions ShapeSheet et des références de cellules. L’expression peut aussi inclure des arguments spécifiques transmis par la cellule d’appel. 
  
La cellule d’appel spécifie la cellule contenant la fonction personnalisée ainsi que les arguments qu’elle a besoin de transmettre à la fonction. La cellule d’expression est évaluée et le résultat renvoyé à la cellule d’appel.
  
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


