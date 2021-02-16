---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- fonction Excel [excel 2007],fonction Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431672"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de bibliothèque d’infrastructure. **Excel** est un wrapper pour la [fonction Excel4.](excel4-excel12.md) **Excel12f est** un wrapper pour la [fonction Excel12.](excel4-excel12.md) Chaque vérification vérifie qu’aucun des arguments n’est nul, ce qui indique que la création d’une **XLOPER** ou **d’une XLOPER12** temporaire a échoué. Si une erreur se produit, chacun imprime un message de débogage. Lorsque vous avez terminé, chacune libère toute la mémoire temporaire qui a peut-être été créée pour les **xlOPER** et **XLOPER12** temporaires.
  
 **Excel12f ne** peut être appelé qu’à partir d’une DLL commençant par la bibliothèque d’API C d’Excel 2007. En outre, il fonctionne uniquement lors de l’exécution à partir d’Excel 2007 et échoue avec **xlretFailed dans le** cas contraire. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Paramètres

 _iFunction_ (**int**)
  
Numéro indiquant la commande ou la fonction que vous souhaitez appeler. Pour plus d’informations, [voir Excel4/Excel12.](excel4-excel12.md)
  
 _pxRes_
  
Pointeur vers le résultat de la fonction évaluée. Toute mémoire pointée vers le résultat a été allouée par Excel et doit être libérée dans un appel à [xlFree](xlfree.md) une fois qu’elle n’est plus nécessaire, ou en paramètre **xlbitXLFree** en cas de renvoi vers Excel. 
  
 _iCount_ (**int**)
  
Nombre d’arguments qui seront transmis à la fonction. À compter d’Excel 2007, la limite est de 255 arguments. Dans les versions antérieures, la limite est de 30.
  
 _argument1, ..._
  
Arguments facultatifs de la fonction. Tous les arguments doivent être des pointeurs vers **xlOPER** s dans le cas **d’Excel**, ou **XLOPER12** s dans le cas **d’Excel12f**.
  
## <a name="return-value"></a>Valeur renvoyée

Les deux fonctions retournent les mêmes codes d’erreur et de réussite **qu’Excel4,** **Excel4v,** **Excel12** et **Excel12v.** Pour obtenir une description complète de ces codes, voir [Excel4/Excel12.](excel4-excel12.md) En outre, ces fonctions Framework retournent **xlretFailed** sans appeler l’API C si un pointeur NULL vers un paramètre est détecté. 
  
## <a name="example"></a>Exemple

Cet exemple transmet un argument non positif à la fonction **Excel12f,** qui envoie un message au débogger. 
  
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

