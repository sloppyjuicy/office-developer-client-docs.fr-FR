---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- fonction func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408914"
---
# <a name="func1"></a>Func1

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
L’exemple de fonction de feuille de calcul définie par l’utilisateur illustre le retour d’une valeur de chaîne statique. Lorsque GENERIC.xll est chargé, il inscrit cette fonction afin qu’elle puisse être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Paramètres

 _px_ (**LPXLOPER**)
  
Cet argument est ignoré et sert uniquement à déclencher l’appel de la fonction par Microsoft Excel.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 **LPXLOPER12**: toujours la chaîne « Func1 »
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

