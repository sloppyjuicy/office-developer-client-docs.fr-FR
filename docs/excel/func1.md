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
ms.localizationpriority: medium
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ec4d0646cb1525f517a57ace5cee52325548cec0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552226"
---
# <a name="func1"></a>Func1

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L’exemple de fonction de feuille de calcul définie par l’utilisateur illustre le retour d’une valeur de chaîne statique. Lorsque GENERIC.xll est chargé, il inscrit cette fonction afin qu’elle puisse être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Paramètres

 _px_ (**LPXLOPER**)
  
Cet argument est ignoré et sert uniquement à déclencher Microsoft Excel pour appeler la fonction.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 **LPXLOPER12**: toujours la chaîne « Func1 »
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

