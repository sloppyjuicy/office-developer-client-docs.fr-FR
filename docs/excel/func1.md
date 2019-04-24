---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- fonction func1 [Excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304080"
---
# <a name="func1"></a>Func1

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction de feuille de calcul définie par l'utilisateur illustre le retour d'une valeur de chaîne statique. Lorsque GENERIC. xll est chargé, il enregistre cette fonction afin qu'elle puisse être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Paramètres

 _PX_ (**LPXLOPER**)
  
Cet argument est ignoré et sert uniquement à déclencher Microsoft Excel pour appeler la fonction.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 **LPXLOPER12**: toujours la chaîne «func1»
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

