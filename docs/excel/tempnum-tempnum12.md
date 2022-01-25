---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- fonction tempnum12 [excel 2007],tempNum function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
ms.openlocfilehash: 30b29ef9733e1718708896d20b9876c1e0880d62
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198196"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **xlOPER** XLOPER12 temporaire contenant un numéro Microsoft Excel feuille de calcul (un double de /   8 byte IEEE). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Paramètres

 _d_ (**double**)
  
Valeur prévue. Notez que les nombres sous-normaux de l’IEEE ne sont actuellement pas pris en charge et sont arrondis à zéro. L’infini négatif est pris en charge.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **xltypeNum** numérique contenant la valeur transmise dans ou zéro si la valeur transmise était sous-normale. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction TempNum12** pour passer un argument à **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

