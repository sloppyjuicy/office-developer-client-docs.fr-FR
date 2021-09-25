---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- fonction xlstack [excel 2007]
ms.localizationpriority: medium
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 455de097446af6e96e2655cef66fcc84adbbd203
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621296"
---
# <a name="xlstack"></a>xlStack

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Vérifie la quantité d’espace laissé sur la pile.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie le nombre d’octets **(xltypeInt)** restants sur la pile.
  
## <a name="remarks"></a>Remarques

La quantité d’espace de pile disponible des versions récentes déborde de l’integer signé 16 bits de **la XLOPER**. Cela signifie que **xlStack** peut renvoyer une valeur entre -32767 et 32768 lorsqu’il est appelé à l’aide de **XLOPER** s et **Excel4** ou **Excel4v**. Pour obtenir la valeur correcte dans ce cas, vous devez caster la valeur renvoyée en un raccourci non signé.
  
À partir de Excel 2007, vous devez appeler cette fonction à l’aide de **XLOPER12** s et **Excel12** ou **Excel12v**, auquel cas la valeur renvoyée est la quantité d’espace pile disponible ou 64 Ko, selon la valeur la plus faible.
  
Excel dispose d’une quantité limitée d’espace sur la pile et vous devez prendre soin de ne pas dépasser cet espace. Ne placez jamais de très grandes structures de données sur la pile et faites autant de variables locales que possible statiques. Évitez d’appeler des fonctions de manière récursive, car cela remplira rapidement la pile.
  
Si vous pensez que vous appelez cette fonction fréquemment pour voir la quantité d’espace de pile qui reste.
  
## <a name="example"></a>Exemple

Le premier exemple affiche un message d’alerte contenant la quantité d’espace de pile gauche et est contenu dans  `\SAMPLES\EXAMPLE\EXAMPLE.C` . Le deuxième exemple fait la même chose, en travaillant avec **xlOPER** et n’est pas contenu dans l’exemple de code SDK.
  
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

