---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- fonction xlset [excel 2007]
ms.localizationpriority: medium
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a99d904c4aa9845146ffe2d05dff45859de3b434
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576603"
---
# <a name="xlset"></a>xlSet

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Place très rapidement des valeurs constantes dans des cellules ou des plages. Pour plus d’informations, voir « xlSet et workbooks with Array Formulas » dans [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Paramètres

_pxReference_ (**xltypeRef** ou **xltypeSRef**)
  
Référence rectangulaire décrivant la ou les cellules cibles. La référence doit décrire les cellules adjacentes, de sorte que dans un **xltypeRef** `val.mref.lpmref->count` doit être définie sur 1. 
  
_pxValue_
  
Valeur ou valeur à placer dans la ou les cellules. Pour plus d’informations, voir la section « Remarques ».
  
## <a name="remarks"></a>Remarques

### <a name="pxvalue-argument"></a>Argument pxValue

_pxValue peut_ être une valeur ou un tableau. S’il s’agit d’une valeur, la plage de destination entière est remplie avec cette valeur. S’il s’agit d’un tableau (**xltypeMulti**), les éléments du tableau sont placés aux emplacements correspondants dans le rectangle.
  
Si vous utilisez un tableau horizontal pour le deuxième argument, il est dupliqué vers le bas pour remplir le rectangle entier. Si vous utilisez un tableau vertical, il est dupliqué à droite pour remplir le rectangle entier. Si vous utilisez un tableau rectangulaire et qu’il est trop petit pour la plage rectangulaire que vous souhaitez y placer, cette plage est ajoutée avec **#N/A.**
  
Si la plage cible est plus petite que le tableau source, les valeurs sont copiées dans les limites de la plage cible et les données supplémentaires sont ignorées.
  
Pour effacer un élément du rectangle de destination, utilisez un élément de tableau de type **xltypeNil** dans le tableau source. Pour effacer l’intégralité du rectangle de destination, omettez le deuxième argument. 
  
### <a name="restrictions"></a>Restrictions

**XlSet ne** peut pas être annulé. En outre, il détruit toutes les informations d’annuler qui auraient pu être disponibles auparavant. 
  
**XlSet peut** placer uniquement des constantes, et non des formules, dans les cellules. 
  
**XlSet se** comporte comme une fonction équivalente à une commande de classe 3 ; autrement dit, elle est disponible uniquement à l’intérieur d’une DLL lorsque la DLL  est appelée à partir d’un  objet, d’une macro, d’un menu, d’une barre d’outils, d’une touche de raccourci ou du bouton Exécuter dans la boîte de dialogue **Macro** (accessible à partir de l’onglet Affichage du ruban à partir de Excel 2007 et du **menu** Outils dans les versions antérieures). 
  
## <a name="example"></a>Exemple

L’exemple suivant remplit B205:B206 avec la valeur transmise à partir d’une macro. Cet exemple de fonction de commande nécessite un argument et fonctionne uniquement s’il est appelé à partir d’une feuille macro XLM ou d’un module VBA à l’aide de la méthode **Application.Run.** 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [xlCoerce](xlcoerce.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

