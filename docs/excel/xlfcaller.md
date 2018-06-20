---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- fonction xlfCaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782215"
---
# <a name="xlfcaller"></a>xlfCaller

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Retourne des informations sur la cellule, une plage de cellules, la commande sur un menu, l’outil sur une barre d’outils ou objet qui a appelé la commande DLL ou la fonction qui est en cours d’exécution.
  
|**Appelée à partir de code**|**Renvoie**|
|:-----|:-----|
|DLL  <br/> |L’ID du Registre.  <br/> |
|Une cellule unique  <br/> |Une référence à une cellule unique.  <br/> |
|Une formule de tableau de cellules  <br/> |Une référence à plusieurs cellule.  <br/> |
|Une expression de mise en forme conditionnelle  <br/> |Une référence à la cellule à laquelle la condition de mise en forme est appliquée.  <br/> |
|Un menu  <br/> | Un tableau à ligne unique quatre éléments :  <br/>  ID de la barre.  <br/>  La position du menu.  <br/>  La position du sous-menu.  <br/>  La position de la commande.  <br/> |
|Une barre d’outils  <br/> | Un seule ligne tableau à deux éléments :  <br/>  Numéro de barres d’outils intégrées ou le nom de la barre d’outils des barres d’outils personnalisées dans la barre d’outils.  <br/>  La position de la barre d’outils.  <br/> |
|Un objet graphique  <br/> |L’identificateur d’objet (nom de l’objet).  <br/> |
|Une commande associée à un xlcOnEnter, sur. Entrez, événements  <br/> |Une référence à l’ou les cellules en cours de saisie.  <br/> |
|Une commande associée à un xlcOnDoubleclick, sur. DOUBLECLICK, événement interruption.  <br/> |La cellule qui était un double-clic (pas nécessairement la cellule active).  <br/> |
|Macro Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate  <br/> |Le nom de la feuille d’appel.  <br/> |
|Autres méthodes non répertoriés  <br/> |#REF! Erreur  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La valeur renvoyée est parmi les suivants **XLOPER**/ **XLOPER12** des types de données : **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**ou **xltypeMulti**. Étant donné que trois de ces types de point de mémoire allouée, la valeur de retour de **xlfCaller** doit toujours être libérée dans un appel à la [fonction xlFree](xlfree.md) lorsqu’il n’est plus nécessaire. 
  
Pour plus d’informations sur **XLOPER**/ **XLOPER12s** voir [Gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Remarques

Cette fonction est la fonction uniquement non-feuille de calcul qui peut être appelée à partir d’une fonction de feuille de calcul DLL/XLL. Autres fonctions d’informations XLM ne peuvent être appelées à partir de commandes ou l’équivalent de feuille macro fonctions.
  
## <a name="example"></a>Exemple

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Cette fonction appelle une macro de commande (xlcSelect) et que l’opération correctement appelée à partir d’une feuille macro.
  
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



[Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

