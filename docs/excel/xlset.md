---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- fonction xlSet [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782247"
---
# <a name="xlset"></a>xlSet

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Place les valeurs de constantes dans des cellules ou plages très rapidement. Pour plus d’informations, voir « xlSet et classeurs avec des formules matricielles » dans [Les problèmes connus dans le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Paramètres

_pxReference_ (**xltypeRef** ou **xltypeSRef**)
  
Référence rectangulaire décrivant la cible ou les cellules. La référence doit décrire les cellules adjacentes, ainsi que dans une **xltypeRef** `val.mref.lpmref->count` doit être défini sur 1. 
  
_pxValue_
  
L’ou les valeurs à placer dans l’ou les cellules. Pour plus d’informations, voir la section « Remarques ».
  
## <a name="remarks"></a>Remarques

### <a name="pxvalue-argument"></a>argument pxValue

_pxValue_ peut être une valeur ou un tableau. Si elle est une valeur, la plage de destination entière est remplie avec cette valeur. S’il est un tableau (**xltypeMulti**), les éléments du tableau sont placés dans les emplacements correspondants dans le rectangle.
  
Si vous utilisez une matrice pour le second argument, elle est dupliquée vers le bas pour remplir l’ensemble du rectangle. Si vous utilisez une matrice verticale, elle est dupliquée de droite à remplir l’ensemble du rectangle. Si vous utilisez un tableau rectangulaire, et il est trop petit pour la plage rectangulaire dans que doivent figurer, cette plage est remplie avec s **# N/a**.
  
Si la plage cible est inférieure à la baie source, les valeurs sont copiées dans les limites de la plage cible et les données supplémentaires sont ignorées.
  
Pour supprimer un élément du rectangle de destination, utilisez un élément de tableau de type **xltypeNil** dans le tableau source. Pour effacer le rectangle de destination entière, omettez le deuxième argument. 
  
### <a name="restrictions"></a>Restrictions

**xlSet** ne peut pas être annulée. En outre, il supprime toutes les informations annulation sont peut-être disponibles avant. 
  
**xlSet** pouvez placer uniquement des constantes, ni les formules dans des cellules. 
  
**xlSet** se comporte comme une fonction équivaut à la commande de classe 3 ; Autrement dit, il est disponible uniquement à l’intérieur d’une DLL lorsque la DLL est appelée à partir d’un objet, macro, menu, barre d’outils, touche de raccourci ou le bouton **exécuter** dans la boîte de dialogue **Macro** (accédé à partir de l’onglet **affichage** du ruban à compter d’Excel 2007 et les outils ** **menu dans les versions antérieures). 
  
## <a name="example"></a>Exemple

L’exemple suivant remplit B205:B206 avec la valeur qui a été passée à partir d’une macro. Cet exemple de fonction commande requiert un argument et donc ne fonctionnera que si elle est appelée à partir d’une feuille de macro XLM, ou d’un module VBA à l’aide de la méthode **Application.Run** . 
  
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
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

