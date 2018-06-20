---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- fonction tempbool [excel 2007], fonction TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782192"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant la **valeur booléenne** **TRUE** ou **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Paramètres

 _b_ (**int**)
  
Utilisez 0 pour renvoyer la **valeur FALSE**; utiliser une autre valeur pour renvoyer **la valeur TRUE**.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Renvoie un **xltypeBool** **Boolean** contenant la valeur logique passée. 
  
## <a name="example"></a>Exemple

L’exemple suivant utilise la fonction **TempBool12** pour effacer la barre d’état. Mémoire temporaire est libérée lorsque la fonction [Excel/Excel12f](excel-excel12f.md) est appelée. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

