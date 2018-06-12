---
title: EVALCELL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Prend une référence à une cellule qui contient une fonction personnalisée ainsi que sur une ou plusieurs paires nom-valeur à passer à la fonction personnalisée comme arguments (facultatif). Renvoie le résultat de la fonction personnalisée les arguments spécifiés et les valeurs calculé.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788565"
---
# <a name="evalcell-function"></a>EVALCELL, fonction

Prend une référence à une cellule qui contient une fonction personnalisée ainsi que sur une ou plusieurs paires nom-valeur à passer à la fonction personnalisée comme arguments (facultatif). Renvoie le résultat de la fonction personnalisée les arguments spécifiés et les valeurs calculé.
  
## <a name="syntax"></a>Syntaxe

EVALCELL (** *cellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **], …) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Une référence à la cellule contenant la fonction personnalisée. Références entre différentes feuilles sont autorisées.  <br/> |
| _arg1Name_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Nom du premier argument à transmettre à la fonction personnalisée. Les espaces sont acceptés.  <br/> |
| _arg1_ <br/> |Facultatif  <br/> |**Varie** <br/> |Valeur du paramètre _arg1_ .  <br/> |
| _arg2Name_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Le nom du deuxième argument à transmettre à la fonction personnalisée. Les espaces sont autorisés.  <br/> |
| _Arg2_ <br/> |Facultatif  <br/> |**Varie** <br/> |Valeur du paramètre _arg2_ .  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

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


