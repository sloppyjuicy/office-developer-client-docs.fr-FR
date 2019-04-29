---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- fonction FuncSum [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406940"
---
# <a name="funcsum"></a>FuncSum

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction de feuille de calcul définie par l'utilisateur qui prend 1 à 29 arguments et calcule leur somme. Chaque argument peut être un nombre unique, une plage ou un tableau. Lorsque GENERIC. xll est chargé, il enregistre cette fonction afin qu'elle puisse être appelée à partir de la feuille de calcul. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Paramètres

 _PX1-px29_ (**LPXLOPER12**)
  
Pointeurs vers des arguments de **XLOPER12** . La fonction accepte n'importe quel type de type d'entrée, mais n'est codée que pour fonctionner sur des nombres, des tableaux littéraux de nombres et des plages qui contiennent uniquement des nombres ou des cellules vides. Si moins de 29 arguments sont fournis, les autres arguments sont fournis en tant que **xltypeMissing**.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

(**LPXLOPER12 xltypeNum** ou **xltypeErr**)
  
La somme des arguments ou des #VALUE! s'il y a des valeurs non numériques dans la liste d'arguments fournie ou dans une cellule d'une plage ou d'un élément d'un tableau.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

