---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- fonction xlfCaller [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310226"
---
# <a name="xlfcaller"></a>xlfCaller

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie des informations sur la cellule, une plage de cellules, une commande d'un menu, un outil sur une barre d'outils ou un objet qui a appelé la commande ou la fonction DLL en cours d'exécution.
  
|**Code appelé depuis**|**Renvoie**|
|:-----|:-----|
|FICHIER  <br/> |ID de registre.  <br/> |
|Une cellule unique  <br/> |Une référence à cellule unique.  <br/> |
|Une formule matricielle à cellules multiples  <br/> |Une référence à plusieurs cellules.  <br/> |
|Expression de mise en forme conditionnelle  <br/> |Référence à la cellule à laquelle la condition de mise en forme est appliquée.  <br/> |
|Un menu  <br/> | Un tableau à ligne unique à quatre éléments:  <br/>  ID de la barre.  <br/>  Position du menu.  <br/>  Position du sous-menu.  <br/>  Position de la commande.  <br/> |
|Barre d'outils  <br/> | Un tableau à une seule ligne à deux éléments:  <br/>  Numéro de la barre d'outils pour les barres d'outils intégrées ou nom de la barre d'outils pour les barres d'outils personnalisées.  <br/>  Position de la barre d'outils.  <br/> |
|Un objet graphique  <br/> |Identificateur d'objet (nom de l'objet).  <br/> |
|Commande associée à un xlcOnEnter, ON. ENTRÉE, notification d'événement  <br/> |Référence à la ou aux cellules entrées.  <br/> |
|Commande associée à un xlcOnDoubleclick, ON. DOUBLECLICK, reception d'événement.  <br/> |Cellule sur laquelle l'utilisateur a cliqué deux fois (pas nécessairement la cellule active).  <br/> |
|Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate, macro  <br/> |Nom de la feuille d'appel.  <br/> |
|Autres méthodes non indiquées  <br/> |#REF! Erreur  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La valeur renvoyée est l'un des types de données**XLOPER12** d' **XLOPER**/ suivants: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**ou **xltypeMulti**. Étant donné que trois de ces types pointent vers la mémoire allouée, la valeur de retour de **xlfCaller** doit toujours être libérée dans un appel à la [fonction xlFree](xlfree.md) lorsqu'elle n'est plus nécessaire. 
  
Pour plus d'informations sur les **XLOPER**/ **XLOPER12** , consultez la rubrique [gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Remarques

Cette fonction n'est pas une fonction de feuille de calcul qui peut être appelée à partir d'une fonction de feuille de calcul DLL/XLL. Les autres fonctions d'informations XLM ne peuvent être appelées qu'à partir de commandes ou de fonctions équivalentes de feuille macro.
  
## <a name="example"></a>Exemple

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Cette fonction appelle une macro de commande (xlcSelect) et fonctionne correctement uniquement lorsqu'elle est appelée à partir d'une feuille macro.
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

