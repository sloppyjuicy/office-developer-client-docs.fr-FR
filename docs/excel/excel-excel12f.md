---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- fonction Excel [Excel 2007], fonction Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310912"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque Framework. **Excel** est un wrapper de la fonction [Excel4](excel4-excel12.md) . **Excel12f** est un wrapper de la fonction [Excel12](excel4-excel12.md) . Chaque contrôle vérifie qu'aucun des arguments n'a la valeur zéro, ce qui signifie que la création d'un élément **XLOPER** ou **XLOPER12** temporaire a échoué. Si une erreur se produit, chacune imprime un message de débogage. Lorsque vous avez terminé, chaque opération libère la totalité de la mémoire temporaire qui a pu être créée pour les objets **XLOPER**et **XLOPER12**temporaires.
  
 **Excel12f** peut uniquement être appelé à partir d'une dll à partir de la bibliothèque d'API C d'Excel 2007. En outre, elle ne fonctionne qu'avec Excel 2007, et échoue avec **xlretFailed** dans le cas contraire. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Paramètres

 _IFunction_ (**int**)
  
Nombre indiquant la commande ou la fonction que vous souhaitez appeler. Pour plus d'informations, consultez la rubrique [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Pointeur vers le résultat de la fonction évaluée. Toute mémoire pointée dans le résultat est allouée par Excel et doit être libérée dans un appel à [xlFree](xlfree.md) une fois qu'elle n'est plus nécessaire, ou en définissant **xlbitXLFree** si elle est renvoyée à Excel. 
  
 _iCount_ (**int**)
  
Nombre d'arguments qui seront transmis à la fonction. À partir d'Excel 2007, la limite est de 255 arguments. Dans les versions antérieures, la limite est de 30.
  
 _argument1,..._
  
Arguments facultatifs de la fonction. Tous les arguments doivent être des pointeurs vers des objets **XLOPER**dans le cas d' **Excel**ou de **XLOPER12**s dans le cas de **Excel12f**.
  
## <a name="return-value"></a>Valeur renvoyée

Ces deux fonctions renvoient les mêmes codes d'erreur et de succès que **Excel4**, **Excel4v**, **Excel12**et **Excel12v**. Pour une description complète de ces codes, voir [Excel4/Excel12](excel4-excel12.md) . En outre, ces fonctions d'infrastructure renvoient **xlretFailed** sans appeler l'API C si un pointeur null vers un paramètre est détecté. 
  
## <a name="example"></a>Exemple

Cet exemple transmet un argument incorrect à la fonction **Excel12f** , qui envoie un message au débogueur. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Excel4/Excel12](excel4-excel12.md)


[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

