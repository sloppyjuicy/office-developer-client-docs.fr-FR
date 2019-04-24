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
- fonction tempbool [Excel 2007], fonction TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310352"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure qui crée une expression **XLOPER**/ **** temporaire contenant la valeur **booléenne** **true** ou **false**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Paramètres

 _b_ (**int**)
  
Utilisez 0 pour renvoyer la **valeur false**; Utilisez n'importe quelle autre valeur pour renvoyer la valeur **true**.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie une valeur de **type Boolean** **xltypeBool** qui contient la valeur logique passée. 
  
## <a name="example"></a>Exemple

L'exemple suivant utilise la fonction **TempBool12** pour effacer la barre d'État. La mémoire temporaire est libérée lors de l'appel de la fonction [Excel/Excel12f](excel-excel12f.md) . 
  
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

