---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- fonction xlfcaller [excel 2007]
ms.localizationpriority: medium
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c4728136a34cc2b2cd60c6f7ec2e057d366df7c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605595"
---
# <a name="xlfcaller"></a>xlfCaller

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Retourne des informations sur la cellule, la plage de cellules, la commande d’un menu, l’outil d’une barre d’outils ou l’objet qui a appelé la commande ou la fonction DLL en cours d’exécution.
  
|**Code appelé à partir de**|**Renvoie**|
|:-----|:-----|
|DLL  <br/> |ID d’inscription.  <br/> |
|Une seule cellule  <br/> |Référence à une seule cellule.  <br/> |
|Formule de tableau à cellules multiples  <br/> |Référence à plusieurs cellules.  <br/> |
|Expression de mise en forme conditionnelle  <br/> |Référence à la cellule à laquelle la condition de mise en forme est appliquée.  <br/> |
|Un menu  <br/> | Tableau à une seule ligne à quatre éléments :  <br/>  ID de la barre.  <br/>  Position du menu.  <br/>  Position du sous-menu.  <br/>  Position de la commande.  <br/> |
|Barre d’outils  <br/> | Tableau à une seule ligne à deux éléments :  <br/>  Numéro de barre d’outils pour les barres d’outils intégrées ou nom de barre d’outils pour les barres d’outils personnalisées.  <br/>  Position sur la barre d’outils.  <br/> |
|Objet graphique  <br/> |Identificateur d’objet (nom de l’objet).  <br/> |
|Commande associée à un xlcOnEnter, ON. ENTRÉE, capture d’événement  <br/> |Référence à la ou aux cellules entrées.  <br/> |
|Commande associée à un xlcOnDoubleclick, ON. DOUBLECLICK, capture d’événement.  <br/> |Cellule sur qui l’utilisateur a double-cliqué (pas nécessairement la cellule active).  <br/> |
|Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate macro  <br/> |Nom de la feuille d’appel.  <br/> |
|Autres méthodes non répertoriées  <br/> |#REF! Erreur  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La valeur de retour est l’un des types de données **XLOPER** /  **XLOPER12** suivants : **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** ou **xltypeMulti**. Étant donné que trois de ces types pointent vers la mémoire allouée, la valeur de retour de **xlfCaller** doit toujours être libérée dans un appel à la fonction [xlFree](xlfree.md) lorsqu’elle n’est plus nécessaire. 
  
Pour plus d’informations **sur LES XLOPERS** /  **XLOPER12,** voir Gestion de la [mémoire dans Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Remarques

Cette fonction est la seule fonction non-feuille de calcul qui peut être appelée à partir d’une fonction de feuille de calcul DLL/XLL. D’autres fonctions d’informations XLM peuvent uniquement être appelées à partir de commandes ou de fonctions équivalentes à une feuille macro.
  
## <a name="example"></a>Exemple

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Cette fonction appelle une macro de commande (xlcSelect) et ne fonctionne correctement qu’en cas d’appel à partir d’une feuille macro.
  
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

