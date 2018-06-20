---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- fonction funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782132"
---
# <a name="funcsum"></a>FuncSum

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction définie par l’utilisateur la feuille de calcul qui accepte les arguments de 1 à 29 et calcule leur somme. Chaque argument peut être un numéro unique, une plage ou un tableau. Lorsque GENERIC.xll est chargé, il enregistre cette fonction afin qu’elle peut être appelée à partir de la feuille de calcul. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Paramètres

 _PX1-px29_ (**LPXLOPER12**)
  
Pointeurs vers **XLOPER12** arguments. La fonction accepte n’importe quel type de type d’entrée, mais codée uniquement pour fonctionner sur des nombres, tableaux littérales de numéros et plages contenant uniquement des nombres ou des cellules vides. Si moins de 29 arguments sont fournis, les autres arguments sont fournis en tant que **xltypeMissing**.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

(**LPXLOPER12 xltypeNum** ou **xltypeErr**)
  
La somme des arguments ou #VALUE ! s’il y a les valeurs non numériques dans la liste d’arguments fournis ou d’une cellule dans une plage ou un élément dans un tableau.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

