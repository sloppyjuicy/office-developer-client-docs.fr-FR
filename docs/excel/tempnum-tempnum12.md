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
- fonction tempnum12 [Excel 2007], fonction TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310359"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure qui crée une expression **XLOPER**/ **** temporaire contenant un numéro de feuille de calcul Microsoft Excel (un type IEEE de 8 octets). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Paramètres

 _d_ (**double**)
  
Valeur prévue. Notez que les numéros IEEE sous-normaux ne sont actuellement pas pris en charge et arrondis à zéro. L'infini négatif est pris en charge.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie un **xltypeNum** numérique contenant la valeur transmise ou zéro si la valeur passée est Sub-normal. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempNum12** pour transmettre un argument à **xlfGetWorkspace**.
  
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

