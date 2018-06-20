---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- fonction xlStack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782236"
---
# <a name="xlstack"></a>xlStack

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Vérifie la quantité d’espace libre sur la pile.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Renvoie le nombre d’octets (**xltypeInt**) restant sur la pile.
  
## <a name="remarks"></a>Remarques

Nombre entier signé de 16 bits de la **XLOPER**de dépassement de la quantité d’espace de pile disponible des versions récentes. Cela signifie que **xlStack** peut renvoyer une valeur entre-32767 et 32768 lorsqu’elle est appelée à l’aide de s **XLOPER**et **Excel4** ou **Excel4v**. Pour obtenir la valeur correcte dans ce cas, vous devez effectuer un cast de la valeur renvoyée pour un court non signé.
  
À compter d’Excel 2007, vous devez appeler cette fonction à l’aide de s **XLOPER12**et **Excel12** ou **Excel12v**, auquel cas la valeur renvoyée est la quantité d’espace de pile ou de 64 Ko, selon ce qui est le plus petit.
  
Excel dispose de peu d’espace sur la pile, et vous devez veiller ne pas pour cet espace de saturation. Ne jamais placer des structures de données très volumineuses sur la pile et rendre statiques variables autant que possible. Éviter d’appeler des fonctions de manière récursive, car remplira rapidement la pile.
  
Si vous pensez que vous sont saturer la pile, appelez cette fonction fréquemment pour voir la quantité d’espace pile de gauche.
  
## <a name="example"></a>Exemple

Le premier exemple affiche un message d’alerte contenant la quantité d’espace pile et se trouve dans `\SAMPLES\EXAMPLE\EXAMPLE.C`. Le deuxième exemple effectue la même chose, utilisation de s **XLOPER**et ne figure pas dans l’exemple de code SDK.
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

