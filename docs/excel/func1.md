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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782126"
---
# <a name="func1"></a>Func1

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction définie par l’utilisateur la feuille de calcul illustre le retour d’une valeur de chaîne statique. Lorsque GENERIC.xll est chargé, il enregistre cette fonction afin qu’elle peut être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Paramètres

 _px_ (**LPXLOPER**)
  
Cet argument est ignoré et sert uniquement à Microsoft Excel pour appeler la fonction de déclencheur.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

 **LPXLOPER12**: toujours la chaîne « Func1 »
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

