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
- tempbool function [excel 2007],TempBool12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 47c86ac41c49ae1e3de9a5f065294215f95822db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576673"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **XLOPER** /  **XLOPER12** temporaire contenant **booléen** **TRUE** ou **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Paramètres

 _b_ (**int**)
  
Utilisez 0 pour renvoyer **FALSE**; utilisez n’importe quelle autre valeur pour renvoyer **TRUE**.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie un **booléen xltypeBool** **contenant** la valeur logique transmise. 
  
## <a name="example"></a>Exemple

L’exemple suivant utilise la **fonction TempBool12** pour effacer la barre d’état. La mémoire temporaire est libérée lorsque la [fonction Excel/Excel12f](excel-excel12f.md) est appelée. 
  
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

