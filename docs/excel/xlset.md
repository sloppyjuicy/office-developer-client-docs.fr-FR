---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- fonction xlSet [Excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404602"
---
# <a name="xlset"></a>xlSet

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Place les valeurs constantes dans des cellules ou des plages très rapidement. Pour plus d'informations, voir «xlSet et classeurs avec des formules matricielles» dans [problèmes connus dans le développement XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Paramètres

_pxReference_ (**xltypeRef** ou **xltypeSRef**)
  
Référence rectangulaire décrivant la ou les cellules cibles. La référence doit décrire les cellules adjacentes, de sorte que dans un **xltypeRef** `val.mref.lpmref->count` doit être défini sur 1. 
  
_pxValue_
  
Valeur ou valeurs à placer dans la ou les cellules. Pour plus d'informations, reportez-vous à la section «Remarques».
  
## <a name="remarks"></a>Remarques

### <a name="pxvalue-argument"></a>argument pxValue

_pxValue_ peut être une valeur ou un tableau. S'il s'agit d'une valeur, la plage de destination entière est remplie avec cette valeur. S'il s'agit d'un tableau (**xltypeMulti**), les éléments du tableau sont placés dans les emplacements correspondants dans le rectangle.
  
Si vous utilisez une matrice horizontale pour le deuxième argument, celle-ci est dupliquée pour remplir le rectangle entier. Si vous utilisez un tableau vertical, il est dupliqué de façon à ce qu'il remplisse tout le rectangle. Si vous utilisez un tableau rectangulaire et qu'il est trop petit pour la plage rectangulaire dans laquelle vous souhaitez l'insérer, cette plage est remplie avec **#N/a**s.
  
Si la plage cible est plus petite que la matrice source, les valeurs sont copiées dans les limites maximales de la plage cible et les données supplémentaires sont ignorées.
  
Pour effacer un élément du rectangle de destination, utilisez un élément de tableau de types **xltypeNil** dans le tableau source. Pour effacer tout le rectangle de destination, omettez le deuxième argument. 
  
### <a name="restrictions"></a>Restrictions

**xlSet** ne peut pas être annuler. En outre, il détruit toutes les informations d'annulation qui ont pu être disponibles. 
  
**xlSet** ne peut placer que des constantes, et non des formules, dans des cellules. 
  
**xlSet** se comporte comme une fonction équivalente à une commande de classe 3; autrement dit, il est disponible uniquement à l'intérieur d'une DLL lorsque la DLL est appelée à partir d'un objet, d'une macro, d'un menu, d'une barre d'outils, d'une touche de raccourci ou du bouton **exécuter** dans la boîte de dialogue **macro** (accessible à partir de l'onglet **affichage** du ruban à partir d'Excel 2007, ainsi que les **Outils **menu dans les versions antérieures). 
  
## <a name="example"></a>Exemple

L'exemple suivant remplit B205: B206 avec la valeur qui a été transmise à partir d'une macro. Cet exemple de fonction Command requiert un argument et ne fonctionnera que s'il est appelé à partir d'une feuille macro XLM ou à partir d'un module VBA à l'aide de la méthode **application. Run** . 
  
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

