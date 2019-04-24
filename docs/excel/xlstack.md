---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- fonction xlStack [Excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310156"
---
# <a name="xlstack"></a>xlStack

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Vérifie la quantité d'espace restant sur la pile.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie le nombre d'octets (**xltypeInt**) restants sur la pile.
  
## <a name="remarks"></a>Remarques

La quantité d'espace de pile disponible des versions récentes déborde de l'entier signé 16 bits de **XLOPER**. Cela signifie que **xlStack** peut renvoyer une valeur comprise entre-32767 et 32768 lorsqu'il est appelé à l'aide de **XLOPER**s et **Excel4** ou **Excel4v**. Pour obtenir la valeur correcte dans ce cas, vous devez effectuer un cast de la valeur renvoyée en un type unsigned short.
  
À partir d'Excel 2007, vous devez appeler cette fonction à l'aide de **XLOPER12**s et **Excel12** ou **Excel12v**, auquel cas la valeur renvoyée est la quantité d'espace de pile disponible ou 64 Ko, la valeur la plus faible étant retenue.
  
Excel dispose d'un espace limité sur la pile et vous devez veiller à ne pas saturer cet espace. Ne jamais placer de très grandes structures de données sur la pile et définir autant de variables locales que possible. Évitez d'appeler des fonctions de manière récursive, car cela remplira rapidement la pile.
  
Si vous pensez que vous avez le temps de relancer la pile, appelez fréquemment cette fonction pour voir la taille de l'espace de pile restant.
  
## <a name="example"></a>Exemple

Le premier exemple affiche un message d'alerte contenant la quantité d'espace de pile à gauche et `\SAMPLES\EXAMPLE\EXAMPLE.C`est contenu dans. Le deuxième exemple effectue la même chose, en travaillant avec **XLOPER**s et n'est pas inclus dans l'exemple de code du kit de développement logiciel (SDK).
  
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

- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

