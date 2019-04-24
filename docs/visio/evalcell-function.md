---
title: EVALCELL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Prend une référence à une cellule qui contient une fonction personnalisée, ainsi qu'une ou plusieurs paires nom-valeur à transmettre à la fonction personnalisée en tant qu'arguments (facultatif). Renvoie le résultat calculé de la fonction personnalisée selon les arguments et les valeurs spécifiés.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329070"
---
# <a name="evalcell-function"></a>Fonction EVALCELL

Prend une référence à une cellule qui contient une fonction personnalisée, ainsi qu'une ou plusieurs paires nom-valeur à transmettre à la fonction personnalisée en tant qu'arguments (facultatif). Renvoie le résultat calculé de la fonction personnalisée selon les arguments et les valeurs spécifiés.
  
## <a name="syntax"></a>Syntaxe

EVALCELL (* * *cellRef* * *, [* * *arg1Name, arg1* * *], [* * *arg2Name, arg2* * *],...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à la cellule contenant la fonction personnalisée. Les références inter-feuilles sont acceptées.  <br/> |
| _arg1Name_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Nom du premier argument à transmettre à la fonction personnalisée. Les espaces sont acceptés.  <br/> |
| _Arg1_ <br/> |Facultatif  <br/> |**Réelle** <br/> |Valeur du paramètre _Arg1_ .  <br/> |
| _arg2Name_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Nom du deuxième argument à transmettre à la fonction personnalisée. Les espaces sont acceptés.  <br/> |
| _Arg2_ <br/> |Facultatif  <br/> |**Réelle** <br/> |Valeur du paramètre _Arg2_ .  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

La cellule d’appel n’a pas besoin de spécifier chaque argument utilisé par la fonction personnalisée. 
  
## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser la fonction EVALCELL conjointement avec la fonction ARG pour trouver la valeur médiane parmi un ensemble de trois valeurs. 
  
Dans la cellule d’expression, placez le code suivant qui définit la fonction personnalisée : 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

Dans les cellules d’appel, placez le code suivant qui appelle la fonction personnalisée :
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


