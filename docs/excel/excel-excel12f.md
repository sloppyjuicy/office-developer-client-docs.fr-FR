---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- fonction Excel [excel 2007], fonction Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782055"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque Framework. **Excel** est un wrapper de la fonction [Excel4](excel4-excel12.md) . **Excel12f** est un wrapper de la fonction [Excel12](excel4-excel12.md) . Chaque vérifie qu’aucun des arguments est zéro, ce qui indique que la création d’un temporaire **XLOPER** **XLOPER12** a échoué. Si une erreur se produit, chacun affiche un message de débogage. Lorsque vous avez terminé, chacun libère toute la mémoire temporaire qui peut ont été créée pour temporaire **XLOPER**et **XLOPER12**.
  
 **Excel12f** peut être appelée uniquement à partir d’une DLL à partir de la bibliothèque d’interface API C Excel 2007. En outre, il seulement fonctionne lors de l’exécution de démarrage d’Excel 2007 et échoue avec **xlretFailed** dans le cas contraire. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Paramètres

 _iFunction_ (**int**)
  
Un nombre indiquant la commande ou la fonction que vous voulez appeler. Pour plus d’informations, voir [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Un pointeur vers le résultat de la fonction évaluée. Mémoire vers lequel pointe dans le résultat sera ont été utilisé par Excel et doit être libéré dans un appel à [xlFree](xlfree.md) une fois qu’il n’est plus nécessaire, ou en définissant **xlbitXLFree** si elle de retour dans Excel. 
  
 _iCount_ (**int**)
  
Le nombre d’arguments qui sera passé à la fonction. À compter d’Excel 2007, la limite est de 255 arguments. Dans les versions antérieures, la limite est de 30.
  
 _argument1..._
  
Les arguments facultatifs à la fonction. Tous les arguments doivent être des pointeurs vers **XLOPER**dans le cas **d’Excel**, ou **XLOPER12**dans le cas **Excel12f**.
  
## <a name="return-value"></a>Valeur renvoy�e

Les deux fonctions renvoient la même erreur et les codes de réussite en tant que **Excel4**, **Excel4v**, **Excel12**et **Excel12v**. Voir [Excel4/Excel12](excel4-excel12.md) pour une description complète de ces codes. En outre, ces fonctions de Framework renvoient **xlretFailed** sans appeler l’API C si un pointeur NULL à un paramètre est détecté. 
  
## <a name="example"></a>Exemple

Cet exemple transmet un argument non valide pour la fonction **Excel12f** , qui envoie un message pour le débogueur. 
  
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

